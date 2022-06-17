---
title: Több ügyfél kezelése egy projektárajánlaton
description: Ez a cikk tájékoztatást nyújt az árajánlatok munkájáról, amelyek több ügyfelet érintenek, akik finanszírozzák a projektet.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 16cd07527fddd093748a18c1f7c900c8b32be85d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928205"
---
# <a name="manage-multiple-customers-on-a-project-quote"></a>Több ügyfél kezelése egy projektárajánlaton

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A projektárajánlatok támogatják azt az esetet, amikor a javaslat több ügyfelet is tartalmaz, akik az üzletet finanszírozzák. Az Árajánlat **Összegzés** lapján található a **Potenciális ügyfél** mező, amely azonosítja az üzlet elsődleges ügyfelét. Az üzlet egyéb ügyfelei a projektárajánlat **Ügyfelek** lapján állíthatók be.

Az összes árajánlati ügyfél a projektárajánlat **Ügyfelek** lapján az árajánlatsori ügyfél alapértelmezett értékkel rendelkezik az árajánlathoz létrehozott minden **új** projektalapú árajánlatsor esetében. A meglévő projektalapú árajánlatsorok nem fogják örökölni az utánuk létrehozott új árajánlati ügyfélrekordokat.

Az árajánlatban szereplő ügyfelek és ajánlatsor ügyfelei az árajánlat megnyerése előtt bármikor hozzáadhatók, frissíthetők és törölhetők. Az árajánlaton szereplő érvényes ügyfelet üygfélként kell beállítani a Tulajdonos vállalat vagy Jogi entitás részben az **Ügyfelek** oldalon. A jogi személyek a Dynamics 365 Project Operations **Projektmenedzsment és könyvelés** moduljában állíthatók be és Vállalatként érhetők el a Project Operations **Projektértékesítés és szállítás** moduljaiban.

## <a name="concept-of-a-primary-customer"></a>Az elsődleges ügyfél fogalma

Az ügyfél, aki a projektárajánlat **Összegzés** lapján szerepel potenciális ügyfélként, az az árajánlat elsődleges ügyfele. Ha megpróbálja törölni az elsődleges ügyfelet az árajánlat ügyféllistájáról, akkor egy hibaüzenet jelenik meg, amely szerint egy árajánlatban szereplő elsődleges ügyfélrekord nem törölhető.

Az elsődleges ügyfél nem frissíthető az árajánlatban szereplő ügyféllistából. Az elsődleges ügyfélre azonban hatással lehet, ha módosítja a potenciális ügyfelet az árajánlat **Összegzés** lapján. Ha frissíti a mezőt az **Árajánlat összesítése** részben, akkor az újonnan kiválasztott potenciális ügyfél kerül hozzáadásra az **Elsődleges** jelzővel rendelkező új árajánlati ügyfélként. A régi potenciális ügyfél továbbra is ügyfél lesz az árajánlatban.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Árajánlati ügyfélrekord létrehozása, módosítása és törlése

Az árajánlati ügyfél az **Árajánlat** oldal **Árajánlati ügyfelek** lapján hozható létre, frissíthető, illetve törölhető. Az alábbi táblázatban felsorolt mezők a projektárajánlat árajánlati ügyfélrekordjában találhatók.

| **Mező** | **Hely** | **Leírás** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- | --- |
| Fiók | Szerkeszthető rács az árajánlati ügyfél **Árajánlati ügyfelek** lapján és a **Fő** és a **Gyorslétrehozás** űrlapjain. | Felsorolja az összes aktív partnert. Ez a mező a rekord létrehozása után zárolva van. Ha frissíteni kívánja, törölje a rekordot, és hozza létre újra. Ha bármilyen tényleges adatot rögzített, vagy ha az árajánlati ügyfélrekord egy elsődleges ügyfél, akkor a bejegyzést törölheti. | Az árajánlati ügyfeleket a rendszer az árajánlatsor létrehozásakor árajánlatsori ügyfelekként másolja át. Az árajánlati ügyfelek az árajánlat megnyerése után átmásolásra kerülnek a projektszerződési ügyfelekbe is. |
| Számlázásfelosztás százaléka | Szerkeszthető rács az árajánlati ügyfél **Árajánlati ügyfelek** lapján és a **Fő** és a **Gyorslétrehozás** űrlapjain. | Az adott árajánlati ügyfélnek tulajdonított, nem számlázott értékesítési tranzakciók százalékos arányát jeleníti meg. | Átmásolva a létrehozott új árajánlatsorokba és a projektszerződés ügyfeleihez. |
| Számlázási kapcsolattartó neve | Szerkeszthető rács az árajánlati ügyfél **Árajánlati ügyfelek** lapján és a **Fő** és a **Gyorslétrehozás** űrlapjain. | Ez egy szöveges mező, amellyel azonosítható az ügyfélhez tartozó számlázási kapcsolattartó. Ezek alapértelmezés szerint a kapcsolódó partner rekordjából származnak. | Átmásolva a projektszerződés ügyfeleihez, amikor egy árajánlatot megnyernek, és ezzel a Számlázási kapcsolattartó neve mező létrehozásra kerül a számlán ehhez az ügyfélhez. |
| Számlázási név | Szerkeszthető rács az árajánlati ügyfél **Árajánlati ügyfelek** lapján és a **Fő** és a **Gyorslétrehozás** űrlapjain. | Ezzel a szöveges mezővel azonosítható az ügyfélhez tartozó számlázási kapcsolattartó. | Átmásolva a projektszerződés ügyfeleihez, amikor egy árajánlatot megnyernek, és ezzel a **Számlázási kapcsolattartó neve** mező létrehozásra kerül a számlán ehhez az ügyfélhez. |
| Fizetési feltételek | Szerkeszthető rács az árajánlati ügyfél **Árajánlati ügyfelek** lapján és a **Fő** és a **Gyorslétrehozás** űrlapjain. | Ez egy értékkészlet, amely a kapcsolódó partnerrekordból alapértelmezésként vett értékeket tartalmaz. | Átmásolva a projektszerződés ügyfeleihez, amikor egy árajánlatot megnyernek, és ezzel a **Számlázási kapcsolattartó neve** mező létrehozásra kerül a számlán ehhez az ügyfélhez. |
| Kerekítés | Szerkeszthető rács az árajánlati ügyfél **Árajánlati ügyfelek** lapján és a **Fő** és a **Gyorslétrehozás** űrlapjain. | Jelzi, ha az ügyfél az adott üzlet alapértelmezett kerekítési ügyfele-e. | Az árajánlat megnyerése esetén a projektszerződések ügyfeleire másolódik. |
| Tulajdonos vállalat | Szerkeszthető rács az árajánlati ügyfél **Árajánlati ügyfelek** lapján és a **Fő** és a **Gyorslétrehozás** űrlapjain. | Az a jogi entitás, amelyben ez az ügyfél be van állítva a **Projektmenedzsment és könyvelés** modulban. Ez a mező írásvédett, és az árajánlat tulajdonos vállalatára van beállítva. A **Partner** mezőben hozzáadni kívánt ügyfelek listáját a rendszer már szűri az adott vállalattól származó listára a Project Operations **Projektmenedzsment és könyvelés** moduljában. | A tulajdonos vállalat a Project Operations **Projektmenedzsment és könyvelés** moduljában a jogi entitás fogalmának felel meg. A projektből származó összes költséget és bevételt a tulajdonos vállalat főkönyvében kell könyvelni. |
| Nem meghaladandó korlát | Szerkeszthető rács az árajánlati ügyfél **Árajánlati ügyfelek** lapján és a **Fő** és a **Gyorslétrehozás** űrlapjain. | Azt jelzi, hogy van-e megállapodás szerinti korlát vagy felső határ az adott ügyfélnek ezzel az aktivitással kapcsolatban számlázott teljes összegre vonatkozóan. | Az árajánlat megnyerése esetén a projektszerződések ügyfeleire másolódik. |

## <a name="editing-billing-split-percentages"></a>Számlázásfelosztási százalékok szerkesztése

A számlázásfelosztási százalékokat a soros rácsszerkesztés használatával szerkesztheti. Ha a számlázási felosztási százalékok összege nem 100%, hiba lép fel. A számlázásfelosztási százalékok frissítése után frissítse az oldalt a hiba eltávolításához.

Megpróbálhatja kiválasztani az **Egyenlő elosztás** lehetőséget is az árajánlat ügyfeleinek részrácsán. Ez a művelet a számlázásfelosztásokat az összes árajánlati ügyfél számára elosztja. Ha van kerekítési tényező, az hozzáadódik a kerekítő ügyfélhez. Az árajánlati ügyfelek egyike mindig a kerekítő vevőként van címkézve. Ez azt jelenti, hogy az árajánlat vevői rekordjának esetében a **Kerekítés** jelzője **Igen**. Általában ez az árajánlat elsődleges vevője, de ez módosítható.


[!INCLUDE[footer-include](../includes/footer-banner.md)]