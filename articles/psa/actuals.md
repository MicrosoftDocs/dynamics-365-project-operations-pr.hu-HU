---
title: Tényadatok áttekintése
description: Ez a témakör a projektek tényadataival kapcsolatban nyújt tájékoztatást.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cbb3e5c7f74cdf37ae4d259687bf7a98102a8131
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368164"
---
# <a name="actuals-overview"></a>Tényadatok áttekintése

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A tények a projektben befejezett munka mennyiségét jelentik. A projektek tényadatai visszavezethetők a forrásdokumentumokhoz. Ezek a forrásdokumentumok többek között idő-, költség-és naplóbejegyzések, valamint számlák.

![Hogyan vezethetők vissza a projekt tényadatok a forrásdokumentumokhoz](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Időbejegyzés elküldése

A PSA-ban, amikor egy idő- és anyagelszámolású szerződéssorra leképezett projekthez küldenek be időbejegyzést, két naplósor jön létre. Az egyik sor a költségre, míg a másik a számlázatlan értékesítésre szolgál. Amikor egy rögzített árú szerződéssorra leképezett projekthez küldenek be időbejegyzést, csak a költségekre vonatkozó naplósor jön létre. 

Az alapértelmezett árak megadásának logikája a naplósorban található. Az időbejegyzésből származó mezőértékek mindegyike a naplósorba van másolva. Ezekben a mezőkben szerepel a tranzakció dátuma, a projekthez leképezett szerződéssor, és a megfelelő árlistában szereplő pénznem. 

Az alapértelmezett árakra hatással lévő mezők, például a **Szerepkör** és a **Szervezeti egység** mezők a naplósorban alapértelmezés szerint megfelelő áron jelennek meg. Ha egyéni mezőt ad hozzá az időbejegyzéshez, és azt szeretné, hogy a mező értéke a tényadatokra legyen propagálva, hozza létre a mezőt a Tények entitáson, és a mezők leképezésével másolja a mezőt az időbejegyzésből a tényekhez.

## <a name="submitting-an-expense-entry"></a>Költségbejegyzés elküldése

A PSA-ban, amikor egy idő- és anyagelszámolású szerződéssorra leképezett projekthez küldenek be költségbejegyzést, két naplósor jön létre. Az egyik sor a költségre, míg a másik a számlázatlan értékesítésre szolgál. Amikor egy rögzített árú szerződéssorra leképezett projekthez küldenek be költségbejegyzést, csak a költségekre vonatkozó naplósor jön létre.

A költségekre vonatkozó alapértelmezett árak megadásának logikája a **Költségbejegyzés** lapon kiválasztott költségkategórián alapul. A tranzakció dátuma, a projekthez leképezett szerződéssor és a pénznem mind a megfelelő árlista meghatározására szolgál. Az ár esetében azonban a felhasználó által megadott összeg, alapértelmezés szerint közvetlenül a kapcsolódó költség-naplósorokban van beállítva a költségre és értékesítésre vonatkozóan.

A PSA jelenlegi verziójában nem áll rendelkezésre az egységenkénti alapértelmezett ár kategória alapú megadása a költségbejegyzésekre vonatkozóan.

## <a name="using-entry-journals-to-record-costs"></a>Rekordaplók használata a költségek rögzítésére

A PSA-ban a rekordnaplók segítségével rögzítheti a költséget vagy bevételt az anyag-, díj-, idő-, költség- vagy adózási tranzakciók osztályaiban. A napló fejlécet, sorokat és egy **Megerősítés** műveletet tartalmaz. Az alábbi helyzetekben érdemes naplót használni:

- Amikor tényleges költségeket és értékesítéseket kell rögzíteni a projektben.
- Amikor tranzakciós tényeket kell egy másik rendszerből a PSA-ba áthelyezni.
- Amikor rögzítenie kell a másik rendszerben felmerült költségeket, például beszerzési vagy alvállalkozói költségeket.

> [!IMPORTANT]
> A Rekordnaplók létrehozásakor a tényleges adatokat csak olyan felhasználó hozhatja létre, aki teljes mértékben tisztában van azzal, hogy milyen hatással vannak azok a tényleges adatokra a projekten. Ennek oka az, hogy az alkalmazás nem ellenőrzi a naplósor típusát, vagy a kapcsolódó árazást, amelyeket a naplósorban adtak meg. A naplótípus hatása miatt kellő óvatossággal kell eljárnia, hogy ki kapja meg a belépési naplók létrehozásához szükséges hozzáférést.     


## <a name="recording-actuals-based-on-project-events"></a>Tényadatok rögzítése projektesemények alapján

A PSA rögzíti a projekt során bekövetkező pénzügyi tranzakciókat. Ezeket a tranzakciókat a rendszer **tényadatokként** rögzíti. A következő táblázatok a létrehozott tényadatok különböző típusait mutatják be attól függően, hogy a projekt idő- és anyagelszámolású vagy rögzített árú projekt, elővásárlási fázisban van-e, vagy belső projekt-e.

**Az erőforrás ugyanahhoz a szervezeti egységhez tartozik, mint a projekt szerződő részlege**

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

**Az erőforrás egy olyan szervezeti egységhez tartozik, amely a projekt szerződő részlegétől eltérő**

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