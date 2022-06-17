---
title: Több ügyfél kezelése projektárajánlatokon - Lite
description: Ez a cikk tájékoztatást nyújt az árajánlatok több ügyféllel való munkáról, akik finanszírozzák a projektet. (Sales)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 337619e8d8081cdebd73f9336fa9fa99885a0ab2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921075"
---
# <a name="manage-multiple-customers-on-project-quotes---lite"></a>Több ügyfél kezelése projektárajánlatokon - Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A projektárajánlatok támogatják azt az esetet, amikor a javaslat több ügyfelet is tartalmaz, akik az üzletet finanszírozzák. Az Árajánlat **Összegzés** lapján található a **Potenciális ügyfél** mező, amely azonosítja az üzlet elsődleges ügyfelét. Az üzlet egyéb ügyfelei a projektárajánlat **Ügyfelek** lapján állíthatók be.

Az összes árajánlati ügyfél a projektárajánlat **Ügyfelek** lapján az árajánlatsori ügyfél alapértelmezett értékkel rendelkezik az árajánlathoz létrehozott minden **új** projektalapú árajánlatsor esetében. A meglévő projektalapú árajánlatsorok nem fogják örökölni az utánuk létrehozott új árajánlati ügyfélrekordokat.

A termékalapú árajánlatsorokat a rendszer automatikusan hozzárendeli az elsődleges ügyfélhez, aki egyben az árajánlat **Összegzés** lapjának **Potenciális ügyfél** mezőjében található ügyfél.

Az árajánlatban szereplő ügyfelek és ajánlatsor ügyfelei az árajánlat megnyerése előtt bármikor hozzáadhatók, frissíthetők és törölhetők.

## <a name="concept-of-a-primary-customer"></a>Az elsődleges ügyfél fogalma

Az ügyfél, aki a projektárajánlat összegzés lapján szerepel potenciális ügyfélként, az az árajánlat elsődleges ügyfele. Ha megpróbálja törölni az elsődleges ügyfelet az árajánlat ügyféllistájáról, akkor egy hibaüzenet jelenik meg, amely szerint egy árajánlatban szereplő elsődleges ügyfélrekord nem törölhető.

Az elsődleges ügyfél nem frissíthető az árajánlatban szereplő ügyféllistából. Az elsődleges ügyfélre azonban hatással lehet, ha módosítja a potenciális ügyfelet az árajánlat **Összegzés** lapján. Ha frissíti a mezőt az **Árajánlat összesítése** részben, akkor az újonnan kiválasztott potenciális ügyfél kerül hozzáadásra az **Elsődleges** jelzővel rendelkező új árajánlati ügyfélként. A régi potenciális ügyfél továbbra is ügyfél lesz az árajánlatban.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Árajánlati ügyfélrekord létrehozása, módosítása és törlése

Az árajánlati ügyfél az **Árajánlat** oldal **Árajánlati ügyfelek** lapján hozható létre, frissíthető, illetve törölhető. Az alábbi táblázatban felsorolt mezők a projektárajánlat árajánlati ügyfélrekordjában találhatók.

| **Mező** | **Hely** | **Leírás** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- | --- |
| Fiók | Szerkeszthető rács az árajánlati ügyfél **Árajánlati ügyfelek** lapján és a **Fő** és a **Gyorslétrehozás** űrlapjain. | Felsorolja az összes aktív partnert. Ez a mező a rekord létrehozása után zárolva van. Ha frissíteni kívánja, törölje a rekordot, és hozza létre újra. Ha rögzített tényleges adatokat, vagy ha az idézett ügyfélrekord elsődleges ügyfél, akkor nem törölheti a rekordot. | Az árajánlati ügyfeleket a rendszer az árajánlatsor létrehozásakor árajánlatsori ügyfelekként másolja át. Az árajánlati ügyfelek az árajánlat megnyerése után átmásolásra kerülnek a projektszerződési ügyfelekbe is. |
| Számlázásfelosztás százaléka | Szerkeszthető rács az árajánlati ügyfél **Árajánlati ügyfelek** lapján és a **Fő** és a **Gyorslétrehozás** űrlapjain. | Az adott árajánlati ügyfélnek tulajdonított, nem számlázott értékesítési tranzakciók százalékos arányát jeleníti meg. | Átmásolva az új árajánlatsorokba és a projektszerződés ügyfeleihez. |
| Számlázási kapcsolattartó neve | Szerkeszthető rács az árajánlati ügyfél **Árajánlati ügyfelek** lapján és a **Fő** és a **Gyorslétrehozás** űrlapjain. | Ez egy szöveges mező, amellyel azonosítható az ügyfélhez tartozó számlázási kapcsolattartó. Ezek alapértelmezés szerint a kapcsolódó partner rekordjából származnak. | Átmásolva a projektszerződés ügyfeleihez, amikor egy árajánlatot megnyernek, és ezzel a Számlázási kapcsolattartó neve mező létrehozásra kerül a számlán ehhez az ügyfélhez. |
| Számlázási név | Szerkeszthető rács az árajánlati ügyfél **Árajánlati ügyfelek** lapján és a **Fő** és a **Gyorslétrehozás** űrlapjain. | Ezzel a szöveges mezővel azonosítható az ügyfélhez tartozó számlázási kapcsolattartó. | Átmásolva a projektszerződés ügyfeleihez, amikor egy árajánlatot megnyernek, és ezzel a **Számlázási kapcsolattartó neve** mező létrehozásra kerül a számlán ehhez az ügyfélhez. |
| Fizetési feltételek | Szerkeszthető rács az árajánlati ügyfél **Árajánlati ügyfelek** lapján és a **Fő** és a **Gyorslétrehozás** űrlapjain. | Ez egy értékkészlet, amely a kapcsolódó partnerrekordból alapértelmezésként vett értékeket tartalmaz. | Átmásolva a projektszerződés ügyfeleihez, amikor egy árajánlatot megnyernek, és ezzel a **Számlázási kapcsolattartó neve** mező létrehozásra kerül a számlán ehhez az ügyfélhez. |
| Kerekítés | Szerkeszthető rács az árajánlati ügyfél **Árajánlati ügyfelek** lapján és a **Fő** és a **Gyorslétrehozás** űrlapjain. | Jelzi, ha az ügyfél az adott üzlet alapértelmezett kerekítési ügyfele-e. | Az árajánlat megnyerése esetén a projektszerződések ügyfeleire másolódik. |
| Nem meghaladandó korlát | Szerkeszthető rács az árajánlati ügyfél **Árajánlati ügyfelek** lapján és a **Fő** és a **Gyorslétrehozás** űrlapjain. | Azt jelzi, hogy van-e megállapodás szerinti korlát vagy felső határ az adott ügyfélnek ezzel az aktivitással kapcsolatban számlázott teljes összegre vonatkozóan | Az árajánlat megnyerése esetén a projektszerződések ügyfeleire másolódik. |

## <a name="editing-billing-split-percentages"></a>Számlázásfelosztási százalékok szerkesztése

A számlázásfelosztási százalékokat a soros rácsszerkesztés használatával szerkesztheti. Ha a számlázási felosztási százalékok összege nem 100%, hiba lép fel. A számlázásfelosztási százalékok frissítése után frissítse az oldalt a hiba eltávolításához.

Megpróbálhatja kiválasztani az **Egyenlő elosztás** lehetőséget is az árajánlat ügyfeleinek részrácsán. Ez a művelet a számlázásfelosztásokat az összes árajánlati ügyfél számára elosztja. Ha van kerekítési tényező, az hozzáadódik a kerekítő ügyfélhez. Az árajánlati ügyfelek egyike mindig a kerekítő vevőként van címkézve. Ez azt jelenti, hogy az árajánlat vevői rekordjának esetében a **Kerekítés** jelzője **Igen**. Általában ez az árajánlat elsődleges vevője, de ez módosítható.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
