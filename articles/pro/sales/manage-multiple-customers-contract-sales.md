---
title: Több ügyfél kezelése egy projektszerződésen - Lite
description: Ez a témakör információt nyújt a több ügyfélnek a projektszerződéseken való kezeléséről.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b248dabdbd5239b140da7c99d3f38609facfe75e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181320"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Több ügyfél kezelése egy projektszerződésen - Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A projektszerződések a Dynamics 365 Project Operations szolgáltatásban támogatják az az esetet, ahol a szerződéses megállapodás több ügyfelet tartalmaz, akik finanszírozzák az üzletet. A **Projektszerződés** oldal **Összegzés** lapján szerepel az **Ügyfél** mező. Ez a mező azonosítja az üzlet elsődleges ügyfelét. Az üzlet egyéb ügyfelei a **projektszerződés** oldal **ügyfelek** lapján állíthatók be.

A projektszerződésen felsorolt összes szerződésügyfél alapértelmezés szerint szerződéssor ügyfél lesz a projektszerződéshez létrehozott bármely új projektalapú szerződéssorán. A meglévő Projektalapú szerződéssorok nem öröklik az új szerződéses ügyfeleket új rekordok létrehozásakor.

A termékalapú szerződéssorok automatikusan az elsődleges ügyfélhez vannak társítva.

A szerződésben szereplő ügyfelek és szerződéssorok ügyfelei a szerződés megnyerése előtt bármikor hozzáadhatók, frissíthetők és törölhetők.

## <a name="primary-customer"></a>Elsődleges ügyfél

Az ügyfél a projektszerződés **Összegzés** lapján látható, mivel a lehetséges ügyfél a szerződés elsődleges ügyfele. Amikor megpróbálja törölni az elsődleges ügyfelet a szerződésben szereplő ügyfelek listájáról, hibaüzenet jelenik meg, miszerint a szerződésben szereplő elsődleges ügyfélrekord nem törölhető.

Az elsődleges ügyfél nem frissíthető a szerződésben szereplő ügyfelek listájából. Ehelyett módosítsa a potenciális ügyfelet a Szerződés **Összegzés** lapján. Ha a program a **Szerződés összegzése** lapon frissíti a mezőt , akkor az új vevőt új szerződéses ügyfélként adja hozzá az **elsődleges** jelzővel. A korábbi elsődleges ügyfél továbbra is a szerződésben szereplő ügyfél lesz.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Szerződés ügyfélrekordjának létrehozása, módosítása és törlése

A szerződéses ügyfél létrehozható, frissíthető, illetve törölhető a **projektszerződés** lap **ügyfelek** lapján. A következő táblázatban szereplő mezők a projektszerződés szerződéses ügyfélrekordjában találhatók, és szem előtt kell tartani a szerződés használata során.

| Mező | Hely | Adatfolyam leírása | Alsóbb rétegbeli hatás |
| --- | --- | --- | --- |
| **Partner** | A **szerződéses ügyfelek** lapján a rács szerkeszthető, valamint a szerződésügyfél **fő-** és **gyorslétrehozási** űrlapjai. | Felsorolja az összes aktív partnert. Ez a mező a rekord létrehozása után zárolva van. A partner frissítéséhez törölje a rekordot, és hozza létre újra. Ha bármilyen tényleges adatokat rögzített, vagy ha a szerződés ügyfélrekordja elsődleges ügyfél, a rekordot nem lehet törölni. | A szerződésben szereplő ügyfeleket a rendszer a szerződéssorok létrehozásakor szerződéssorok ügyfeleként átmásolja. |
| **Számlázásfelosztás százaléka** | A **szerződéses ügyfelek** lapján a rács szerkeszthető, valamint a szerződésügyfél **fő-** és **gyorslétrehozási** űrlapjai. | Ez az egyes nem számlázott értékesítési tranzakciók azon hányadát jelenti, amelyet ez a szerződésügyfélhez tulajdonítanak. | Átmásolva az új szerződéssorokba és a projekt szerződéssorának ügyfeleibe egy új projektszerződéssoron. |
| **Számlázási kapcsolattartó neve** | A **szerződéses ügyfelek** lapján a rács szerkeszthető, valamint a szerződésügyfél **fő-** és **gyorslétrehozási** űrlapjai. | Ezzel a szöveges mezővel azonosítható az ügyfélhez tartozó számlázási kapcsolattartó. Ez a mező alapértelmezés szerint a kapcsolódó partnerrekordból származik. | Átmásolva a **Számlázási szerződés neve** mezőbe az adott ügyfélhez létrehozott számlán. |
| **Számlázási név** | A **szerződéses ügyfelek** lapján a rács szerkeszthető, valamint a szerződésügyfél **fő-** és **gyorslétrehozási** űrlapjai | Ezzel a szöveges mezővel azonosítható az ügyfélhez tartozó számlázási kapcsolattartó. Ez a mező alapértelmezés szerint a kapcsolódó partnerrekordból származik. | Átmásolva a **Számlázási szerződés neve** mezőbe az adott ügyfélhez létrehozott számlán. |
| **Fizetési feltételek** | A **szerződéses ügyfelek** lapján a rács szerkeszthető, valamint a szerződésügyfél **fő-** és **gyorslétrehozási** űrlapjai. | Ez az érték alapértelmezés szerint a kapcsolódó partnerrekordból származik. | Átmásolva a **Számlázási szerződés neve** mezőbe az adott ügyfélhez létrehozott számlán. |
| **Kerekítés** | A **szerződéses ügyfelek** lapján a rács szerkeszthető, valamint a szerződésügyfél **fő-** és **gyorslétrehozási** űrlapjai. | Jelzi, ha az ügyfél az adott üzlet alapértelmezett kerekítési ügyfele-e. A Projektszerződésben csak egy kerekítési ügyfél lehet. | Ha a költség és a nem számlázott értékesítés a mennyiségre lebontva kerekítési különbözetet eredményez, akkor a különbözetet a rendszer az adott ügyfélhez hozzárendelt tényleges értékre alkalmazza. |
| **Nem meghaladandó korlát** | A **szerződéses ügyfelek** lapján a rács szerkeszthető, valamint a szerződésügyfél **fő-** és **gyorslétrehozási** űrlapjai | Azt jelzi, hogy van-e megállapodott korlát vagy felső határ az adott ügyfélnek a munkáért számlázott teljes összegre. | A szerződéses ügyfél szintjén beállított **Nem meghaladandó korlátot** a rendszer értékeli a **Nem számlázott értékesítési tényadatok** pontban, amely erre a szerződéses ügyfélre hivatkozik. |

## <a name="edit-billing-split-percentages"></a>Számlázásfelosztási százalékok szerkesztése

A számlázás felosztási százaléka szerkeszthető a sorközi rácsszerkesztési felületen. Ha a számlázásfelosztási százalékértékek nem tesznek ki teljes 100 százalékot, akkor hiba jelenik meg. A számlázási felosztás százalékos értékének módosítása után frissítse a lapot a hiba elvetéséhez.

Kiválaszhatja az **Egyenlő elosztás** lehetőséget is az **szerződéses ügyfelek** részrácsán, hogy a számlázási felosztásokat egyenletesen ossza el az összes szerződéses ügyfél esetén. Ha bármilyen kerekítési tényező van, akkor a rendszer hozzáadja a kerekítési ügyfélhez. A szerződés szerinti ügyfelek egyike mindig a **kerekítési** ügyfélként van címkézve, ami azt jelenti, hogy a szerződéses ügyfél rekordjánál **Igen** értékre van állítva a kerekítési jelző. Ez általában a szerződés elsődleges ügyfele, de szintén megváltoztatható.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]