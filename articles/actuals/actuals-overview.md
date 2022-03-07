---
title: Tényadatok
description: A témakör a Microsoft Dynamics 365 Project Operations tényadatokkal való munkára vonatkozó információit mutatja be.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291802"
---
# <a name="actuals"></a>Tények 

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A tények a projektben befejezett munka mennyiségét jelentik. Ezek idő- és költségbejegyzésekként, valamint naplóbejegyzésekként és számlákként kerülnek létrehozásra.

## <a name="journal-lines-and-time-submission"></a>Naplósorok és idő beküldése

Az időbejegyzéssel kapcsolatos további tudnivalókért lásd: [Időbejegyzés áttekintése](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Idő és anyagok

Amikor egy elküldött időbejegyzés egy idő- és anyag szerződéssorra leképezett projekthez van csatolva, a rendszer két naplósort hoz létre, egyet a költség, egy pedig a nem számlázott értékesítés számára.

### <a name="fixed-price"></a>Rögzített ár

Amikor egy rögzített árú szerződéssorra leképezett projekthez kapcsolt időbejegyzést küldenek be, csak a költségekre vonatkozó naplósort hoz létre a rendszer.

### <a name="default-pricing"></a>Alapértelmezett árképzés

Az alapértelmezett árak létrehozásának logikája a naplósorban található. Az időbejegyzésből származó mezőértékek a naplósorba vannak másolva. Ezekben az értékekben szerepel a tranzakció dátuma, a projekthez leképezett szerződéssor, és a megfelelő árlistában szereplő pénznem.

Az alapértelmezett árazásra hatással lévő mezők, például a **Szerepkör** és a **Szervezeti egység** mezők a naplósorban a megfelelő ár meghatározására szolgálnak. Lehetőség van egyéni mező hozzáadására az időbejegyzésen. Ha azt szeretné, hogy a mező értéke a tényadatokra legyen propagálva, hozza létre a mezőt a Tények entitáson, és a mezők leképezésével másolja a mezőt az időbejegyzésből a tényekhez.

## <a name="journal-lines-and-basic-expense-submission"></a>Naplósorok és az alapvető költség benyújtása

A költségbejegyzéssel kapcsolatos további tudnivalókért lásd: [Költség áttekintése](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Idő és anyagok

Amikor egy elküldött alapvető költségbejegyzés egy idő- és anyag szerződéssorra leképezett projekthez van csatolva, a rendszer két naplósort hoz létre, egyet a költség, egy pedig a nem számlázott értékesítés számára.

### <a name="fixed-price"></a>Rögzített ár

Amikor egy rögzített árú szerződéssorra leképezett projekthez kapcsolt alapvető költségbejegyzést küldenek be, csak a költségekre vonatkozó naplósort hoz létre a rendszer.

### <a name="default-pricing"></a>Alapértelmezett árképzés

A költségek alapértelmezett árának megadására vonatkozó logika a költségkategórián alapul. A tranzakció dátuma, a projekthez leképezett szerződéssor és a pénznem mind a megfelelő árlista meghatározására szolgál. Alapértelmezésben azonban az árként megadott össze közvetlenül a kapcsolódó költségnaplósorokban van beállítva a költségre és értékesítésre vonatkozóan.

Nem áll rendelkezésre az egységenkénti alapértelmezett ár kategóriaalapú megadása a költségbejegyzésekre vonatkozóan.

## <a name="use-entry-journals-to-record-costs"></a>Bejegyzésnaplók használata a költségek rögzítésére

A bejegyzésnaplók segítségével rögzítheti a költséget vagy bevételt az anyag-, díj-, idő-, költség- vagy adózási tranzakciók osztályaiban. A naplók a következő célokra használhatók:

- A tényleges anyagok és értékesítés költségének rögzítésére a projektben.
- Tranzakciós tényeket helyezhet egy másik rendszerből a Microsoft Dynamics 365 Project Operations rendszerbe.
- Egy másik rendszerben felmerült költségek rögzítésére. Ezek a költségek beszerzési vagy alvállalkozói költségeket is tartalmazhatnak.

> [!IMPORTANT]
> Az alkalmazás nem ellenőrzi a naplósor típusát vagy a kapcsolódó árazást, amelyet a naplósorban adtak meg. Ezért csak azoknak a felhasználóknak érdemes a bejegyzésnaplókat tényleges adatok létrehozására használniuk, akik teljes mértékben ismeretében vannak annak a számviteli hatásnak, amelyet a tényleges adatok gyakorolnak a projektre. A naplótípus hatása miatt gondosan válassza ki, hogy ki férhet hozzá a bejegyzésnaplók létrehozásához.
## <a name="record-actuals-based-on-project-events"></a>Tényadatok rögzítése projektesemények alapján

A Project Operations rögzíti a projekt során bekövetkező pénzügyi tranzakciókat. Ezeket a tranzakciókat a rendszer tényadatokként rögzíti. A következő táblázatok a létrehozott tényadatok különböző típusait mutatják be attól függően, hogy a projekt idő- és anyagelszámolású vagy rögzített árú projekt, elővásárlási fázisban van-e, vagy belső projekt-e.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Az erőforrás ugyanahhoz a szervezeti egységhez tartozik, mint a projekt szerződő részlege

<table>
<thead>
<tr>
<th rowspan="3">Esemény</th>
<th colspan="4">Számlázható vagy értékesített projekt</th>
<th rowspan="3">Elővásárlási szakaszban lévő projekt</th>
<th rowspan="3">Belső projekt</th>
</tr>
<tr>
<th colspan="2">Idő és anyagok</th>
<th colspan="2">Rögzített ár</th>
</tr>
<tr>
<th>Tények</th>
<th>Tranzakció pénzneme</th>
<th>Rögzített ár</th>
<th>Tranzakció pénzneme</th>
</tr>
</thead>
<tbody>
<tr>
<td>Létrejön egy időbejegyzés.</td>
<td colspan="6">Nincs aktivitás a Tényadatok entitásban</td>
</tr>
<tr>
<td>A rendszer elküld egy időbejegyzést.</td>
<td colspan="6">Nincs aktivitás a Tényadatok entitásban</td>
</tr>
<tr>
<td rowspan="2">Az időt elfogadják, és a jóváhagyáskor nem történik módosítás vagy növekedés a számlázható órák értékében.</td>
<td>Tényleges költség</td>
<td>Szerződő részleg pénzneme</td>
<td rowspan="2">Tényleges költség</td>
<td rowspan="2">Szerződő részleg pénzneme
<td rowspan="2">Tényleges költség</td>
<td rowspan="2">Tényleges költség</td>
</tr>
<tr>
<td>Tényeleges számlázatlan értékesítés – Felszámítható</td>
<td>Projektszerződés pénzneme</td>
</tr>
<tr>
<td rowspan="3">Az időt elfogadják, és a jóváhagyáskor nem történik csökkenés a számlázható órák értékében.</td>
<td>Tényleges költség</td>
<td>Szerződő részleg pénzneme</td>
<td rowspan="3">Tényleges költség</td>
<td rowspan="3">Szerződő részleg pénzneme</td>
<td rowspan="3">Tényleges költség</td>
<td rowspan="3">Tényleges költség</td>
</tr>
<tr>
<td>Tényleges számlázatlan értékesítés – Az új mennyiségnél felszámítható</td>
<td>Projektszerződés pénzneme</td>
</tr>
<tr>
<td>Tényleges számlázatlan értékesítés – Az új mennyiségnél nem számítható fel</td>
<td>Projektszerződés pénzneme</td>
</tr>
<tr>
<td rowspan="2">Egy számla megerősítésekor nem történik módosítás vagy növekedés a számlázható órák értékében.</td>
<td>Sztornózott számlázatlan értékesítés</td>
<td>Projektszerződés pénzneme</td>
<td rowspan="2">Mérföldkőhöz tartozó számlázott értékesítés</td>
<td rowspan="2">Projektszerződés pénzneme</td>
<td rowspan="2">Nem alkalmazható</td>
<td rowspan="2">Nem alkalmazható</td>
</tr>
<tr>
<td>Számlázott értékesítés</td>
<td>Projektszerződés pénzneme</td>
</tr>
<tr>
<td rowspan="3">Egy számla megerősítésekor nem történik csökkenés a számlázható órák értékében.</td>
<td>Sztornózott számlázatlan értékesítés</td>
<td>Projektszerződés pénzneme</td>
<td rowspan="3">Nem alkalmazható</td>
<td rowspan="3">Nem alkalmazható</td>
<td rowspan="3">Nem alkalmazható</td>
<td rowspan="3">Nem alkalmazható</td>
</tr>
<tr>
<td>Számlázott értékesítés – Az új mennyiségnél felszámítható</td>
<td>Projektszerződés pénzneme</td>
</tr>
<tr>
<td>Számlázott értékesítés – Az új mennyiségnél nem számítható fel</td>
<td>Projektszerződés pénzneme</td>
</tr>
<tr>
<td rowspan="2">Egy számla javítva a felszámítható mennyiség növeléséhez.</td>
<td>Számlázott értékesítés – Sztornó</td>
<td>Projektszerződés pénzneme</td>
<td rowspan="5">
<ul>
<li>Mérföldkőhöz tartozó sztornózott értékesítés</li>
<li>A mérföldkő <strong>Számlázott</strong> állapotból <strong>Számlázásra készen áll</strong> állapotba kerül</li>
</ul>
</td>
<td rowspan="5">Projektszerződés pénzneme</td>
<td rowspan="5">Nem alkalmazható</td>
<td rowspan="5">Nem alkalmazható</td>
</tr>
<tr>
<td>Számlázott értékesítés</td>
<td>Projektszerződés pénzneme</td>
</tr>
<tr>
<td rowspan="3">Egy számla javítva a felszámítható mennyiség csökkentéséhez.</td>
<td>Számlázott értékesítés – Sztornó</td>
<td>Projektszerződés pénzneme</td>
</tr>
<tr>
<td>Számlázott értékesítés az új mennyiséghez</td>
<td>Projektszerződés pénzneme</td>
</tr>
<tr>
<td>Számlázatlan értékesítés – Az új mennyiségnél felszámítható</td>
<td>Projektszerződés pénzneme</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Az erőforrás egy olyan szervezeti egységhez tartozik, amely a projekt szerződő részlegétől eltérő

<table>
<thead>
<tr>
<th rowspan="3">Esemény</th>
<th colspan="4">Számlázható vagy értékesített projekt</th>
<th rowspan="3">Elővásárlási szakaszban lévő projekt</th>
<th rowspan="3">Belső projekt</th>
</tr>
<tr>
<th colspan="2">Idő és anyagok</th>
<th colspan="2">Rögzített ár</th>
</tr>
<tr>
<th>Tények</th>
<th>Tranzakció pénzneme</th>
<th>Rögzített ár</th>
<th>Tranzakció pénzneme</th>
</tr>
</thead>
<tbody>
<tr>
<td>Létrejön egy időbejegyzés.</td>
<td colspan="6">Nincs aktivitás a Tényadatok entitásban</td>
</tr>
<tr>
<td>A rendszer elküld egy időbejegyzést.</td>
<td colspan="6">Nincs aktivitás a Tényadatok entitásban</td>
</tr>
<tr>
<td rowspan="4">Az időt elfogadják, és a jóváhagyáskor nem történik módosítás vagy növekedés a számlázható órák értékében.</td>
<td>Tényleges költség</td>
<td>Szerződő részleg pénzneme</td>
<td rowspan="4">Tényleges költség</td>
<td rowspan="4">Szerződő részleg pénzneme</td>
<td rowspan="4">Tényleges költség</td>
<td rowspan="4">Tényleges költség</td>
</tr>
<tr>
<td>Tényeleges számlázatlan értékesítés – Felszámítható</td>
<td>Projektszerződés pénzneme</td>
</tr>
<tr>
<td>Erőforrás-kezelő részleg költsége</td>
<td>Erőforrás-kezelő részleg pénzneme</td>
</tr>
<tr>
<td>Szervezetek közötti értékesítések</td>
<td>Szerződő részleg pénzneme</td>
</tr>
<tr>
<td rowspan="5">Az időt elfogadják, és a jóváhagyáskor nem történik csökkenés a számlázható órák értékében.</td>
<td>Tényleges költség</td>
<td>Szerződő részleg pénzneme</td>
<td rowspan="5">Tényleges költség</td>
<td rowspan="5">Szerződő részleg pénzneme</td>
<td rowspan="5">Tényleges költség</td>
<td rowspan="5">Tényleges költség</td>
</tr>
<tr>
<td>Erőforrás-kezelő részleg költsége</td>
<td>Erőforrás-kezelő részleg pénzneme</td>
</tr>
<tr>
<td>Szervezetek közötti értékesítések</td>
<td>Szerződő részleg pénzneme</td>
</tr>
<tr>
<td>Tényleges számlázatlan értékesítés – Az új mennyiségnél felszámítható</td>
<td>Projektszerződés pénzneme</td>
</tr>
<tr>
<td>Tényleges számlázatlan értékesítés – Az új mennyiségnél nem számítható fel</td>
<td>Projektszerződés pénzneme</td>
</tr>
<tr>
<td rowspan="2">Egy számla megerősítésekor nem történik módosítás vagy növekedés a számlázható órák értékében.</td>
<td>Sztornózott számlázatlan értékesítés</td>
<td>Projektszerződés pénzneme</td>
<td rowspan="2">Mérföldkőhöz tartozó számlázott értékesítés</td>
<td rowspan="2">Projektszerződés pénzneme</td>
<td rowspan="2">Nem alkalmazható</td>
<td rowspan="2">Nem alkalmazható</td>
</tr>
<tr>
<td>Számlázott értékesítés</td>
<td>Projektszerződés pénzneme</td>
</tr>
<tr>
<td rowspan="3">Egy számla megerősítésekor nem történik csökkenés a számlázható órák értékében.</td>
<td>Sztornózott számlázatlan értékesítés</td>
<td>Projektszerződés pénzneme</td>
<td rowspan="3">Nem alkalmazható</td>
<td rowspan="3">Nem alkalmazható</td>
<td rowspan="3">Nem alkalmazható</td>
<td rowspan="3">Nem alkalmazható</td>
</tr>
<tr>
<td>Számlázott értékesítés – Az új mennyiségnél felszámítható</td>
<td>Projektszerződés pénzneme</td>
</tr>
<tr>
<td>Számlázott értékesítés – Az új mennyiségnél nem számítható fel</td>
<td>Projektszerződés pénzneme</td>
</tr>
<tr>
<td rowspan="2">Egy számla javítva a felszámítható mennyiség növeléséhez.</td>
<td>Számlázott értékesítés – Sztornó</td>
<td>Projektszerződés pénzneme</td>
<td rowspan="5">
<ul>
<li>Mérföldkőhöz tartozó sztornózott értékesítés</li>
<li>A mérföldkő <strong>Számlázott</strong> állapotból <strong>Számlázásra készen áll</strong> állapotba kerül</li>
</ul>
</td>
<td rowspan="5">Projektszerződés pénzneme</td>
<td rowspan="5">Nem alkalmazható</td>
<td rowspan="5">Nem alkalmazható</td>
</tr>
<tr>
<td>Számlázott értékesítés</td>
<td>Projektszerződés pénzneme</td>
</tr>
<tr>
<td rowspan="3">Egy számla javítva a felszámítható mennyiség csökkentéséhez.</td>
<td>Számlázott értékesítés – Sztornó</td>
<td>Projektszerződés pénzneme</td>
</tr>
<tr>
<td>Számlázott értékesítés az új mennyiséghez</td>
<td>Projektszerződés pénzneme</td>
</tr>
<tr>
<td>Számlázatlan értékesítés – Az új mennyiségnél felszámítható</td>
<td>Projektszerződés pénzneme</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]