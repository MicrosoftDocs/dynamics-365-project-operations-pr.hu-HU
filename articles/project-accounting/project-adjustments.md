---
title: A projekt kiigazításai
description: Ez a cikk a projektmódosításokról nyújt tájékoztatást.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788366"
---
# <a name="project-adjustments"></a>A projekt kiigazításai

_**A következőre vonatkozik:** Project Operations készleten vagy gyártáson alapuló forgatókönyvekhez_

## <a name="adjustments-overview"></a>A kiigazítások áttekintése

A Microsoftot Dynamics 365 Project Operations konfigurálhatja úgy, hogy a felhasználók módosíthassák a feladott tranzakciókat. A projekttranzakciókat külön-külön is módosíthatja, vagy egyszerre több tranzakciót is kiválaszthat az összes projekttranzakció listájában. A projektmódosítások például a számlázható állapot tömeges frissítésére, a konfiguráció módosítása utáni költségek újraszámítására vagy a finanszírozási források frissítésére szolgálnak.

A felhasználók többféleképpen is hozzáférhetnek a projektmódosítási funkcióhoz:

- A Tranzakciók **módosítása oldal használatával**, amely a Projektvezetési és könyvelési **beállításokból** \> **érhető el**.
- A Feladott projekttranzakciók **oldalon található** Korrekció **gomb használatával**, amely a Projektvezetési és könyvelési **tranzakciókból** \> **érhető** el.
- A Feladott projekttranzakciók **oldal Korrekció** gombjának **használatával** egy projekt kontextusában. Ez az oldal a Projektvezetés és könyvelés **Minden** \> **projekt** oldalról érhető el.

A korrekciók engedélyezéséhez engedélyeznie kell egy vagy több tranzakciós állapotot a Projektvezetés és könyvelés **Projektvezetési és könyvelési paraméterek** \> **közül az** Általános **lapon, a** Tranzakciós állapot **korrekciójának engedélyezése szakaszban**. A tranzakciós állapotok közé tartoznak például a feladott tranzakciók, a számlázott tranzakciók vagy a megszüntetett tranzakciók. A Nem **értékre** beállított tranzakciós állapotok tranzakciói abban az állapotban lesznek, amelyek nem jelennek meg a kiigazítási folyamatban a korrekcióhoz kiválaszthatóként.

A Mindig hozzon létre korrekciós tranzakciót **nevű konfigurációs beállítás** jelenleg a Projektvezetési és könyvelési paraméterek között érhető el. Letilthatja ezt a beállítást, ha az eredeti tranzakciót szeretné frissíteni ahelyett, hogy új tranzakciókat hozna létre a korrekció során a forgatókönyvek egy részhalmazában. Bejelentették, hogy ez a paraméter 2023. március 1-ig elavult lesz. 2023. március 1. után a rendszer mindig úgy viselkedik, mintha az opció engedélyezve lenne.

## <a name="adjustments-process-flow"></a>A kiigazítási folyamat folyamata

A következő lépések a beállítások feldolgozásának tipikus folyamatát mutatják be.

1. Nyissa meg a **Projektmódosítások** lapot.
2. Válassza a Kiválasztás **lehetőséget a** várható módosítási feltételeknek megfelelő tranzakciók kereséséhez.
3. A tranzakciók listájában válassza ki az összes tranzakciót vagy a tranzakciók egy részhalmazát korrekcióra.
4. Válassza a Korrekció **lehetőséget, és módosítsa a** vonal attribútumait. Másik lehetőségként, ha az értékeket manuálisan adta meg a tranzakció bevitele során, kiválaszthatja az alapértelmezett rendszerváltozók megadását.
5. A rendszer visszaadja a tranzakciók listáját, és egy pipa jelenik meg a **Függőben lévő korrekció** oszlopban, amely jelzi, hogy hol történtek módosítások. A függőben lévő módosításokkal rendelkező módosítások az oldal alsó felében jelennek meg. Itt további részletes módosításokat hajthat végre az előző oldalon láthatóakon túl.
6. Válassza a Feladás **lehetőséget** a korrekciós tranzakciók feladásához.

A konfigurációtól függően általában új tranzakciók jönnek létre a korrekcióhoz.

- Az **eredeti tranzakció Számlaállapot** mezője Módosítva **értékre** van állítva.
- Létrejön egy sztornírozási tranzakció az eredeti tranzakció sztornírozásához, és az **Állapot** mező Módosítva **értékre** van állítva.
- Létrejön egy új tranzakció, amely tartalmazza a kiigazítási folyamat során végrehajtott módosításokat.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Több feladott projekttranzakció kiválasztása egyszerre a korrekciókhoz és a jóváírásokhoz

A 10.0.30-as kiadásban bevezetett új funkció lehetővé teszi több tranzakció egyszerre történő korrekciójának kiválasztását a **Feladott projekttranzakciók** oldalról.

A funkció használata előtt engedélyezni kell azt a rendszerben. A rendszergazdák a **Funkciókezelés** munkaterületen ellenőrizhetik a funkció állapotát, és szükség esetén engedélyezhetik azt. A Funkciókezelés **munkaterületen keresse meg és válassza a Többszörösen kiválasztott feladott projekttranzakciók korrekciókhoz és jóváírásokhoz**  lehetőséget, majd válassza **az** Engedélyezés most **lehetőséget**.

Ez a szolgáltatás a következő kulcsfontosságú funkciókat teszi lehetővé:

- A projekten belül a feladott tranzakciós oldalról érhető el a meglévő **Korrekció** gombbal.
- Lehetővé teszi a többsoros kiválasztás vezérlőt a **Feladott projekttranzakciók** oldalon. Szűrőket alkalmazhat a listaoldalra, és a korrekciók megkezdése előtt kiválaszthatja a rekordokat.
- Letiltja a Korrekció **gombot, ha egyetlen tranzakció sem módosítható, vagy ha a jóváírások és a** naplók kombinációját választja ki együtt, nem pedig külön-külön.
- A többsoros kijelölési vezérlő hozzáadása miatt a **menüszalag Lekötött költség** hivatkozása már nincs letiltva, ha több sor van kijelölve.
- A következő figyelmeztető üzenetet adja hozzá: "Több mint (kiválasztott számú) rekordot választott ki a korrekcióhoz. A művelet folytatása eltarthat egy ideig. Biztos benne, hogy folytatni szeretné ezt az akciót?"

Ez a funkció a 2. lépést is eltávolítja a cikkben korábban ismertetett folyamatfolyamatból. Ezért a Tranzakciók **korrekciója** oldal megnyitása előtt kiválasztott tranzakciók szerepelnek a korrekcióra szánt tranzakciók listájában. Nem kell a Kiválasztás **gombot használnia a** kereséshez.

> [!NOTE] 
> Még ha ez a funkció le is van tiltva, akkor is kiválaszthat több rekordot a korrekcióhoz. Azonban csak egy rekord *marad kijelölve*, és a Tranzakciók **kiválasztása párbeszédpanel azonnal megjelenik, miután kiválasztotta a** korrekciók megnyitását.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Korrekciós tranzakciós állapotok, amelyek engedélyezhetők vagy letilthatók a korrekciókhoz

A következő állapotok engedélyezhetők vagy tilthatók le a **Projektvezetési** és könyvelési paraméterek **oldal Általános** lapján:

- Közzétett
- Számlajavaslat
- Számlázva
- Becsült
- Megszűnt
- Kezdő egyenleg (óra)

## <a name="adjustment-parameters"></a>Beállítási paraméterek

Ezek a paraméterek a Projektvezetési és könyvelési paraméterek **oldalon vannak felsorolva az** Általános **lap Korrekció** csoportjában **, és módosítják a** korrekciók feldolgozásának viselkedését. 

| Paraméter neve | Description |
|----------------|-------------
| Mindig hozzon létre korrekciós tranzakciót | Ha ez a paraméter engedélyezve van, a kiigazítási folyamat mindig új sztornírozó tranzakciót és új korrigált tranzakciót hoz létre, ha pénzügyi vagy jelentési hatás jelentkezik. Ha a paraméter le van tiltva, a korrekciós folyamat frissíti az eredeti tranzakciót ahelyett, hogy sztornírozást és új tranzakciót hozna létre egy olyan forgatókönyvhöz, mint például a tranzakció szövegének frissítése. |
| Automatikus frissítés mező | Ha ez a paraméter engedélyezve van, a rendszer újraszámítja az önköltségi árat és az eladási árat. |
| Módosítási dátum használata új projektként | Ez a paraméter a tranzakciók jövőbeli pénzügyi időszak való áthelyezésére szolgál, mielőtt a rendszer támogatta volna ezt a funkciót. Nem javasoljuk, hogy használja, mert ez megváltoztatja a tranzakció üzleti dátumát, és egy későbbi kiadásban elavult lesz. |
| Zárt tevékenységek engedélyezése | Általában nem lehet tranzakciókat létrehozni a lezárt tevékenységekhez. Ha ez a paraméter engedélyezve van, a rendszer felülbírálja ezt a viselkedést. Ezért a zárt tevékenységekhez kiigazítások hozhatók létre. |
