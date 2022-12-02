---
title: Projektütemezési API teljesítménye
description: Ez a cikk nyújt tájékoztatást a projektütemezési API-k teljesítménymutatóiról, valamint gyakorlati megoldásokat tartalmaz az optimális használathoz.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ee1bd8e4412ee1d10f445628c5dc87cc9fa91d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911185"
---
# <a name="project-schedule-api-performance"></a>Projektütemezési API teljesítménye

_**A következőre érvényes:** Project Operations erőforrás / nem készletezett alapú forgatókönyvek, Lite telepítése – üzlet a proforma számlázáshoz, Project for the Web_

Ez a cikk nyújt tájékoztatást a projektütemezési alkalmazás programozási interfészek (API-k) teljesítménymutatóiról, valamint a legjobb gyakorlati megoldásokat tartalmazza a használat optimalitálásához.

## <a name="project-scheduling-service"></a>Projektütemezési szolgáltatás
A Projektütemezési szolgáltatás egy többbérlős szolgáltatás, amely a Microsoft Azure szolgáltatásban fut. Az együttműködés gyors és folyamatos használatot biztosít a felhasználók számára a projekteken való munka során. Ez a változáskérések elfogadásával, feldolgozásával, majd az eredmény azonnali visszaküldésával érhető el. A szolgáltatás aszinkron módon kitart a Dataverse mellett, és nem tiltja a felhasználókat más műveletek elvégzésében.

A projektütemezési API-k a Projektütemező szolgáltatásra támaszkodnak olyan kérelmek futtatásához, amelyeket a cikk későbbi szakaszaiban részletesebben ismertetünk.

A projekt ütemezési API-k úgy vannak kialakítva, hogy együttműködjön a munkalebontási struktúra (WBS) entitásokkal:

  - Project
  - Projektfeladat
  - Projektfeladat függősége
  - Projektcsoporttag
  - Erőforrás-hozzárendelés
  
Mind a beépített, mind az egyéni mezők támogatottak. Ellenkező megállapodás hiányában minden általános művelet támogatott, például a létrehozás, frissítés és törlés. További tudnivalók: [A Projektütemezési API-k használata műveletek végrehajtásához és az entitások ütemezéséhez](schedule-api-preview.md).

A projekt ütemezési API-k részeként egy munkaegység-minta is hozzá van adva. Ez a minta OperationSet néven ismert, és akkor használható, ha egy tranzakcióban több kérelem feldolgozása is szükséges.

Az alábbi ábrán az látható, hogy a partner mit fog tapasztalni a funkció használata során.

![Dataverse és pojektütemezési szolgáltatási folyamat.](./media/dataverse-project-scheduling-service-flow.png)

**1. lépés**: Az ügyfél API-hívást hoz létre egy Open Data Protocol (OData) végponthoz a Dataverse szolgáltatásban egy OperationSet létrehozásához.

**2. lépés**: Az új OperationSet létrehozása után egy **OperationSetId** értéket ad eredményül.

**3. lépés**: Az ügyfél az **OperationSetId** értéket használja egy másik Projekt ütemezési API-kérés végrehajtásához. Az eredmény egy ütemezési entitásra vonatkozó létrehozási, frissítési vagy törlési kérelem lesz. A kérelem kérésekor a metaadat-ellenőrzés meg is történik. Ha az ellenőrzés sikertelen, a kérelem megszűnik, és a rendszer hibát ad vissza.

**4a–4c lépés**: Ezek a lépések az ACCEPT fázist jelentik. Az ügyfél az **ExecuteOperationSetV1** API-t hívja meg, amely egy kötegben küldi el a projektütemezési szolgáltatás minden változtatását. A Projektütemezési szolgáltatás a kötegben kérések alapján futtatja saját ellenőrzéseit. Az ellenőrzési hibák visszavonják a kötegfájlt, és kivételt térítenek vissza a hívónak. Ha a köteget a Projektütemezési szolgáltatás sikeresen elfogadja, az OperationSet állapota frissül, hogy az tükrözze azt a tényt, hogy az OperationSet szolgáltatást a Projektütemezési szolgáltatás dolgozza fel.

**5. lépés**: Ez a lépés a PERSIST fázist jelképezi. A Projektütemezési szolgáltatás aszinkron módon írja meg a köteget a Dataverse szolgáltatáshoz egy tranzakcióban. Ha az írási művelet sikeres, az OperationSet **Befejezettként** lesz megjelölve. Az esetleges hibák visszaállítják a tranzakciót és a köteget, és az OperationSet **Sikertelenként** van megjelölve.

## <a name="performance-methodology"></a>Teljesítménnyel kapcsolatos módszertan
A végrehajtási idő a hívástól az **ExecuteOperationSetV1** API-ig, amíg a Projektütemezési szolgáltatás be nem fejezi az írást a Dataverse szolgáltatásnak. Minden művelet együttesen 2200-szor fut, és a P99 végrehajtási idő mértékegységei jelentésre kerülnek. Az egyrekordos és tömeges műveleteket mérve vannak.

Egy rekordot tartalmazó művelet esetén az OperationSet egy kérelmet tartalmaz. Tömeges műveletek esetén 20, 50 vagy 100 kérelmet tartalmaz. Minden tömeges méret jelentése külön-külön történik.

Ezek a műveletek egy Észak-Amerikában található UR 15 Project Operations Lite telepítésen futnak.

## <a name="results"></a>EREDMÉNY
### <a name="create-operations"></a>Műveletek létrehozása
#### <a name="single-record-create-operations"></a>Egyrekordos létrehozási műveletek
A következő táblázat bemutatja az egyes bejegyzés létrehozásának végrehajtásiait. Az időpontok másodpercekben vannak.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Rekord&nbsp;&nbsp;&nbsp;típusa</th>
    <th class="tg-0lax" colspan="2">Idő</th>
  </tr>
  <tr>
    <th class="tg-0lax">Kötelező mezők</th>
    <th class="tg-0lax">Az összes támogatott mező</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Feladatok</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Hozzárendelés</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Csoporttag</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Függőség</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Tömeges létrehozási műveletek
A következő táblázat bemutatja több bejegyzés létrehozásának végrehajtási idejeit. A Microsoft egy OperationSetben mérte a végrehajtási időket 20, 50 és 100 bejegyzés létrehozásakor. Az időpontok másodpercekben vannak.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Rekord&nbsp;&nbsp;&nbsp;típusa</th>
    <th class="tg-0lax" colspan="6">Idő</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 rekord</th>
    <th class="tg-0lax" colspan="2">50 rekord</th>
    <th class="tg-0lax" colspan="2">100 rekord</th>
  </tr>
  <tr>
    <th class="tg-0lax">Kötelező mezők</th>
    <th class="tg-0lax">Az összes támogatott mező</th>
    <th class="tg-0lax">Kötelező mezők</th>
    <th class="tg-0lax">Az összes támogatott mező</th>
    <th class="tg-0lax">Kötelező mezők</th>
    <th class="tg-0lax">Az összes támogatott mező</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Feladatok</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Hozzárendelés</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Függőség</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> A **Projekt** és a **Csoporttag** entitások tömeges létrehozási műveletei nem szerepelnek ebben a táblázatban, mert ezeknek a műveleteknek a futásideje hasonlít a futásidőre, amikor az egy bejegyzés létrehozásához használt API-t többször is hivják. Ezek az API-k azonnal futnak a Dataverse szolgáltatásban.

Az alábbi ábrán a **Feladat**, **Hozzárendelés** és **Függőség** entitás végrehajtási idő ábrázolása látható, amikor 20, 50 és 100 bejegyzés jön létre, és minden támogatott mezőt használ.

![Bejegyzés végrehajtási idődiagram létrehozása.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Műveletek frissítése
#### <a name="single-record-update-operations"></a>Egyrekordos frissítési műveletek
A következő táblázat bemutatja egy bejegyzés frissítésének végrehajtásiait. Az időpontok másodpercekben vannak.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Rekord&nbsp;&nbsp;&nbsp;típusa</th>
    <th class="tg-0lax" colspan="2">Idő</th>
  </tr>
  <tr>
    <th class="tg-0lax">Kötelező mezők </th>
    <th class="tg-0lax">Az összes támogatott mező</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Feladatok</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Csoporttag</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> A rendszer nem támogatja az **Erőforrás-hozzárendelések** és a **Projektfeladat-függőség** entitások frissítési műveleteit.

#### <a name="bulk-update-operations"></a>Tömeges frissítési műveletek
A következő táblázat bemutatja több bejegyzés frissítésének végrehajtási idejeit. A Microsoft konkrétan 20, 50 és 100 rekord frissítésének végrehajtási idejét mérte egyetlen OperationSetben. Az időpontok másodpercekben vannak.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Rekord&nbsp;&nbsp;&nbsp;típusa</th>
    <th class="tg-0lax" colspan="6">Idő</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 rekord</th>
    <th class="tg-0lax" colspan="2">50 rekord</th>
    <th class="tg-0lax" colspan="2">100 rekord</th>
  </tr>
  <tr>
    <th class="tg-0lax">Kötelező mezők</th>
    <th class="tg-0lax">Az összes támogatott mező</th>
    <th class="tg-0lax">Kötelező mezők</th>
    <th class="tg-0lax">Az összes támogatott mező</th>
    <th class="tg-0lax">Kötelező mezők</th>
    <th class="tg-0lax">Az összes támogatott mező</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Feladatok</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Csoporttag</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> A rendszer nem támogatja az **Erőforrás-hozzárendelések** és a **Projektfeladat-függőség** entitások frissítési műveleteit.

Az alábbi ábrán a Feladat és Csoporttag entitás végrehajtási idő ábrázolása látható, amikor 20, 50 és 100 bejegyzés frissül, és minden támogatott mezőt használ.

![Bejegyzés végrehajtási idődiagram frissítése.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Törlési műveletek
#### <a name="single-record-delete-operations"></a>Egyrekordos törlési műveletek
A következő táblázat bemutatja egy bejegyzés törlésének végrehajtásiait. Az időpontok másodpercekben vannak.

| Rekordtípus | Idő  |
|-------------|-------|
| Feladatok        | 20.12 |
| Hozzárendelés  | 10.86 |
| Csoporttag | 12.52 |
| Függőség  | 20.89 |

> [!NOTE]
> A **Projekt** entitáson nem támogatottak a törlési műveletek.

#### <a name="bulk-delete-operations"></a>Tömeges törlési műveletek
A következő táblázat bemutatja több bejegyzés törlésének végrehajtási idejeit. A Microsoft egy OperationSetben mérte a végrehajtási időket 20, 50 és 100 bejegyzés törlésekor. Az időpontok másodpercekben vannak.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Rekord&nbsp;&nbsp;&nbsp;típusa</th>
    <th class="tg-0lax" colspan="3">Idő</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 rekord</th>
    <th class="tg-0lax">50 rekord</th>
    <th class="tg-0lax">100 rekord</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Feladatok</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Hozzárendelés</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Csoporttag</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Függőség</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> A **Projekt** entitáson nem támogatottak a törlési műveletek.

Az alábbi ábrán a **Feladat**, **Hozzárendelés** és **Csoporttag** és **Függőség** entitás végrehajtási idő ábrázolása látható, amikor 20, 50 és 100 bejegyzés törölve.

![Bejegyzés végrehajtási idődiagram törlése.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Megfigyelések
Az **ExecuteOperationSet** API minden bejegyzésművelet esetén körülbelül 800 ezredmásodperc alatt küld egy kérelmet a Projektütemezési szolgáltatásnak. A projektütemezési szolgáltatásnak ezután körülbelül öt másodpercig tart a hasznos terhelés és a Dataverse hívásának feldolgozása. A végrehajtási idő hátralevő részében az üzleti logika fut, és az adatbázisba adatokat ír a Dataverse szolgáltatásban .

100 bejegyzés létrehozásakor, frissítésekor vagy törlésekor az **ExecuteOperationSet** API körülbelül három másodperc alatt elküldi a kérelmet a Projektütemezési szolgáltatásnak. A projektütemezési szolgáltatásnak ezután körülbelül öt másodpercig tart a kérelem és a Dataverse hívásának feldolgozása. A tömeges műveleteknek egyszerre kell a **Projektütemezési szolgáltatás adóját fizetniük** az OperationSet összes bejegyzése után. Ezért a tömeges műveletek átlagos végrehajtási ideje lényegesen alacsonyabb az egyrekordos műveletekénél.

## <a name="scenarios"></a>Forgatókönyvek
Az alábbi táblázatban azok a végrehajtási időpontok láthatóak, amikor a projekt ütemezési API-kat használnak bizonyos helyzetek elvégzésére. Az időpontok másodpercekben vannak.

| Forgatókönyv                                                                   | Idő  |
|----------------------------------------------------------------------------|-------|
| Hozzon létre egy olyan projektet, amely 40 feladattal rendelkezik.                                      | 36.01 |
| Hozzon létre egy olyan projektet, amely 40 feladattal és 20 függőséggel rendelkezik.                  | 38.11 |
| Hozzon létre egy olyan projektet, amely 40 feladattal és 30 hozzárendeléssel rendelkezik.                   | 60.17 |
| Hozzon létre egy olyan projektet, amely 40 feladattal és 20 függőséggel és 30 hozzárendeléssel rendelkezik. | 60.27 |

## <a name="best-practices"></a>Gyakorlati tanácsok
Az előző forgatókönyv eredményei alapján az API-k jobban teljesítenek a következő körülmények között:

  - Csoportosítsa a lehető legtöbb műveletet. A tömeges műveletek átlagos futásidejének jobbnak kell lennie, mint az egyrekordos műveletek átlagos futásidejének. Minél kisebb számú OperationSets van használatban, annál gyorsabb az átlagos végrehajtási idő.
  - Csak a forgatókönyvéhez szükséges minimális attribútumokat állítsa be. Ki kell válogatni az OperationSet-kérelemben szereplő, nem kötelező mezők típusait. Az idegen kulcsokat vagy összesítő mezőket tartalmazó mezők negatív hatással vannak a teljesítményre.
