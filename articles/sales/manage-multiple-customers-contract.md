---
title: Több ügyfél kezelése egy projektszerződésen
description: Ez a cikk arról nyújt tájékoztatást, hogyan kezelhet több ügyfelet egy projektszerződésen.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 78ee117c1068e7af4674cc3b21e1055fd05bb43a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928343"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Több ügyfél kezelése egy projektszerződésen

Ez a cikk arról nyújt tájékoztatást, hogyan kezelhet több ügyfelet egy projektszerződésen. A projektszerződés akkor használható, ha több ügyfélre vonatkozó szerződéses szükséges egy üzlet finanszírozásához. A **Projektszerződés** lapon az **Összegzés** lap információkat tartalmaz az üzlet elsődleges ügyfelével kapcsolatban. Az üzletben részt vevő egyéb ügyfelek hozzáadhatók az **Ügyfelek** laphoz.

Az összes szerződésügyfél a Projektszerződés **Ügyfelek** lapján alapértelmezés szerint a projektszerződéshez létrehozott bármely új projektalapú szerződéssor szerződéssorügyfeleinek felel meg. A meglévő Projektalapú szerződéssorok nem öröklik az új szerződéses ügyfélrekordokat, amelyek később lettel létrehozva.

A szerződésben szereplő ügyfelek és szerződéssorok ügyfelei a szerződés megnyerése előtt hozzáadhatók, frissíthetők és törölhetők. A projektszerződésben szereplő ügyfelet az **Ügyfelek** oldalon kell beállítani ügyfélként a tulajdonos vállalatnál vagy a jogi személynél. A jogi személyek a Dynamics 365 Project Operations **Projektvezetés és könyvelés** moduljában állíthatók be és vállalatként érhetők el a Project Operations **Projektértékesítés** és **Szállítás** moduljaiban.

## <a name="primary-customers"></a>Elsődleges ügyfelek

Az potenciális ügyfél a projektszerződés **Összegzés** lapján látható, és a szerződés elsődleges ügyfele. Az elsődleges ügyfél nem frissíthető a szerződésben szereplő ügyfelek listájából. Amikor megpróbálja törölni az elsődleges ügyfelet a szerződésben szereplő ügyfelek listájáról, hibaüzenet jelenik meg, miszerint a szerződésben szereplő elsődleges ügyfélrekord nem törölhető. Ehelyett projektszerződés **Összegzés** lapján a **Potenciális ügyfél** mezőben módosítsa az ügyfelet. Amikor frissíti ezt a mezőt , akkor az újonnan kiválasztott ügyfelet új szerződéses ügyfélként adja hozzá az **Elsődleges** jelölővel, ami **Igen** értékre van állítva. Az előző elsődleges ügyfél még mindig a szerződésben szereplő ügyfél, de már nem az elsődleges ügyfél.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Szerződés ügyfélrekordjának létrehozása, módosítása és törlése

A szerződéses ügyfél létrehozható, frissíthető, illetve törölhető a **Szerződés** lap **Szerződéses ügyfelek** lapján. A következő mezők megtalálhatók a projektszerződés szerződéses ügyfélrekordjában.

| **Mező** | **Hely** | **Leírás** | 
| --- | --- | --- | 
| Fiók | A **Szerződéses ügyfelek** lapján szerkeszthető rács, valamint a szerződésügyfél fő- és gyorslétrehozási űrlapjai. | Felsorolja az összes aktív partnert. Ez a mező a rekord létrehozása után zárolva van. A rekord frissítéséhez törölje a azt, és hozza létre újra. Ha bármilyen tényleges adatokat rögzített, vagy ha a szerződés ügyfélrekordja elsődleges ügyfél, a rekordot nem lehet törölni. Szerződéssor létrehozásakor a szerződéses ügyfelek szerződéssor ügyfeleiként lesznek másolva. |
| Számlázásfelosztás százaléka | A **Szerződéses ügyfelek** lapján szerkeszthető rács, valamint a szerződésügyfél fő- és gyorslétrehozási űrlapjai. | Ez az egyes nem számlázott értékesítési tranzakciók azon hányadát jelenti, amelyet ez a szerződéses ügyfélhez tulajdonítanak. Az új projektszerződés-sorok létrehozásakor a rendszer a számlázás felosztása százalékértéket átmásolja minden újonnan létrehozott szerződéssorra és projekt szerződéssoros ügyfeleire. |
| Számlázási kapcsolattartó neve | A **Szerződéses ügyfelek** lapján szerkeszthető rács, valamint a szerződésügyfél fő- és gyorslétrehozási űrlapjai. | Ezt a szöveges mezőt kell használni az ügyfélhez tartozó számla kapcsolattartójának azonosításához. Az alapértelmezett érték a kapcsolódó partnerrekordból származik. A szerződés neve át van másolva a **Számlázási szerződés neve** mezőbe az adott ügyfélhez létrehozott számlán. |
| Számlázási név | A **Szerződéses ügyfelek** lapján szerkeszthető rács, valamint a szerződésügyfél fő- és gyorslétrehozási űrlapjai. | Ezt a mezőt használja az ügyfélhez tartozó számla kapcsolattartójának azonosításához. Az alapértelmezett érték a kapcsolódó partnerrekordból származik. Ez név át lesz másolva a **Számlázási szerződés neve** mezőbe az adott ügyfélhez létrehozott számlán. |
| Fizetési feltételek | A **Szerződéses ügyfelek** lapján szerkeszthető rács, valamint a szerződésügyfél fő- és gyorslétrehozási űrlapjai. | Az alapértelmezett érték a kapcsolódó partnerrekordból származik. A feltételek át lesznek másolva a **Számlázási szerződés neve** mezőbe az adott ügyfélhez létrehozott számlán. |
| Tulajdonos vállalat | A **Projektszerződés ügyfelei** lapján szerkeszthető rács, valamint a projektszerződés-ügyfél fő- és gyorslétrehozási űrlapjai. | Az a jogi entitás, amelyben az ügyfél be van állítva a **Projektvezetés és könyvelés** modulban. Ez a mező írásvédett, és a projektszerződés tulajdonos vállalatára van beállítva.</br>A **Partner** mezőben hozzáadni kívánt ügyfelek listáját a rendszer már szűri az adott vállalattól származó listára a Project Operations **Projektmenedzsment és könyvelés** moduljában. A tulajdonos vállalat a Project Operations **Projektvezetés és könyvelés** moduljában szereplő jogi személlyel egyenlő. A projektnél felmerült összes költséget és bevételt elszámolják a tulajdonos vállalat főkönyvében. |
| Kerekítés | A **Szerződéses ügyfelek** lapján szerkeszthető rács, valamint a szerződésügyfél fő- és gyorslétrehozási űrlapjai. | Azt jelzi, hogy az ügyfél az üzlet alapértelmezett kerekítési ügyfele-e. A Projektszerződésben csak egy kerekítési ügyfél lehet. Ha a költség és a nem számlázott értékesítés a mennyiségre lebontva kerekítési különbözetet eredményez, akkor a különbözetet a rendszer az adott ügyfélhez hozzárendelt tényleges értékre alkalmazza. |
| Nem meghaladandó korlát | A **Szerződéses ügyfelek** lapján szerkeszthető rács, valamint a szerződésügyfél fő- és gyorslétrehozási űrlapjai. | Azt jelzi, hogy van-e megállapodott korlát vagy felső határ az adott ügyfélnek a munkáért számlázott teljes összegre. A szerződéses ügyfél szintjén beállított nem meghaladandó korlátot a rendszer értékeli a nem számlázott értékesítési tényadatok pontban, amely erre a szerződéses ügyfélre hivatkozik. |

## <a name="edit-billing-split-percentages"></a>Számlázásfelosztási százalékok szerkesztése

A számlázás felosztási százaléka a rácsban szerkeszthető. Ha a számlázásfelosztási százalékértékek nem tesznek ki teljes 100 százalékot, akkor hiba történik. A számlázási felosztás százalékos értékének módosítása után frissítse a **Projektszerződés** lapot a hiba eltávolításához.

Kiválaszthatja az **Egyenlő elosztás** lehetőséget is a projektszerződés ügyfeleinek részrácsán. A számlázási százalékok egyenletesen vannak elosztva a projektszerződéssoron szereplő összes ügyfél között. Ha bármilyen kerekítési tényező van, akkor a rendszer hozzáadja a tényezőt a kerekítési ügyfélhez. Az egyik szerződésben szereplő ügyfélnek a **Kerekítés** jelölőt mindig **Igen** értékre kell állítani. Az ügyfél a kerekítési ügyfél. A kerekítési ügyfél általában a szerződés elsődleges ügyfele is, de ez nem kötelező.


[!INCLUDE[footer-include](../includes/footer-banner.md)]