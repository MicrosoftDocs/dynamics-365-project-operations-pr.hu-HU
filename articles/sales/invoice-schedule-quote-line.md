---
title: Projektalapú árajánlatsorok számlaütemezései
description: Ez a témakör a számlaütemezések és az árajánlatsorok mérföldköveinek létrehozásával kapcsolatban tartalmaz tájékoztatást.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0d07596b299d71b229487faf80a09e368059575ea37095d2c82d35561d009c96
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988609"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Projektalapú árajánlatsorok számlaütemezései

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A projektalapú árajánlatsor lehetőséget biztosít egy számlaütemezés kifejezésére. Ez az árajánlati fázisban nem kötelező, mert az alkalmazás nem támogatja a projekt számlázását, amikor az az árajánlatsorhoz kötődik. A számlázás csak az árajánlat megnyerése után engedélyezett. A számlaütemezés árajánlati fázisában történő létrehozásának egyetlen alsóbb rétegbeli hatása az, hogy a rendszer átmásolja ezt a számlaütemezést a projektalapú szerződéssorba. Ha az árajánlati fázisban nem hoz létre számlaütemezést, akkor a projektalapú szerződéssor segítségével is megteheti.

Összességében a számlaütemezések célja, hogy lehetővé tegyék a számlavázlatok automatikus létrehozását a projektalapú szerződéssor esetében. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Idő- és anyagelszámolású számlaütemezés létrehozása projektalapú árajánlatsorhoz

Amikor a projektalapú árajánlatsor számlázási módja Idő és anyag típusú, a rendszer egy dátumalapú számlaütemezést hoz létre. Ha automatikusan szeretne létrehozni egy dátumalapú számlaütemezést, hajtsa végre az alábbi lépéseket.

1. Válassza a **Beállítások** > **Számlázási gyakoriság** lehetőséget, és állítson be egy számlázási gyakoriságot.
2. Az **Árajánlatok** oldalon nyissa meg a projektárajánlatot, és az **Összegzés** lapon állítsa be a kért szállítási dátumot.
3. Nyissa meg azt az idő-és anyag árajánlatsort, amelyhez dátumalapú számlaütemezést kell létrehoznia. 
4. A **Számlaütemezés** lapon válassza ki a kívánt értékeket a **Számlázás kezdete** és a **Számlázási gyakoriság** mezőkben. 
5. Az alrácson válassza a **Számlaütemezés előállítása** lehetőséget.
6. Az alkalmazás létrehozza a számlaütemezést a **Számlakészítés dátuma**, a **Tranzakció határideje** és a **Futtatás állapota** mezőket a következő módon beállítva:

    - A **Számlakészítés dátuma** a számla gyakorisága által meghatározott dátumra van beállítva.
    - A **Tranzakció határideje** a **Számlakészítés dátuma** előtti napra van beállítva.
    - A **Futtatás állapota** beállítás automatikusan a **Nem fut** értékre van beállítva. Amikor az automatikus számlalétrehozási feladat egy bizonyos számlázási futtatási dátumnál fut, akkor a program a **Futtatás sikerült** vagy a **Futtatás nem sikerült** értékre módosítja a mezőt.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Rögzített áras számlaütemezés létrehozása projektalapú árajánlatsorhoz

Ha a projektalapú árajánlatsor **Rögzített** számlázási móddal rendelkezik, akkor a rendszer mérföldkőre épülő számlaütemezést hoz létre. Hajtsa végre az alábbi lépéseket, hogy automatikusan előállítsa ezt az ütemezést mérföldkövek egy rögzített, a naptári időszakra egyformán elosztott készletéhez.

1. Válassza a **Beállítások** > **Számlázási gyakoriság** lehetőséget, és állítson be egy számlázási gyakoriságot.
2. Az **Árajánlatok** oldalon nyissa meg a projektárajánlatot, és az **Összegzés** lapon állítsa be a kért szállítási dátumot.
3. Nyissa meg azt a rögzített áras árajánlatsort, amelyhez mérföldkő-ütemezést kell létrehoznia. 
4. A **Számlaütemezés** lapon válassza ki a kívánt értékeket a **Számlázás kezdete** és a **Számlázási gyakoriság** mezőkben. 
5. Az alrácson válassza az **Időszakos mérföldkövek létrehozása** lehetőséget.
6. Az alkalmazás a számlaütemezést mérföldkőnévvel, dátummal és összeggel hozza létre.

    - A mérföldkőnév a számla gyakorisága által meghatározott dátumra van beállítva.
    - A mérföldkő dátuma a számla gyakorisága által meghatározott dátumra van beállítva.
    - A mérföldkő összegét úgy számítja ki a program, hogy a projektalapú árajánlatsorban szereplő árajánlat összegét elosztja a mérföldköveknek a gyakoriság, valamint a számlázás kezdete és a kért szállítási dátumok által megkövetelt számával.
    - Ha az árajánlatsor becsült áfaösszeggel is rendelkezik, akkor ez az érték az egyes mérföldkövek között a periodikus mérföldkövek létrehozásakor egyenlően kerül felosztásra.

### <a name="manually-create-milestones"></a>Mérföldkövek manuális létrehozása

A rögzített árú mérföldkövek létrehozhatók manuálisan is, ha nem időszakosan vannak felosztva. Mérföldkövek manuális létrehozása:

Nyissa meg azt a rögzített áras árajánlatsort, ahol a mérföldkő-ütemezést létre kell hoznia. A **Számlaütemezése** lapon az alrácson válassza a **+ Új ajánlati sor mérföldkő létrehozása** lehetőséget és írja be a következő táblázat alapján a szükséges adatokat.

| **Mező** | **Hely** | **Leírás** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- | --- |
| Mérföldkő neve | Gyorslétrehozás | A mérföldkő neve. | Ez továbbításra kerül a projekt szerződéssor-mérföldkövéhez és a számlához |
| Projektfeladat | Gyorslétrehozás | Ha a mérföldkő a projektfeladathoz van kötve, ezzel a hivatkozással egyéni logikát adhat hozzá a feladat állapota alapján a megadott mérföldkő-állapothoz. | Az alkalmazásnak nincs hatása alsóbb rétegekben ennek a feladathivatkozásnak az esetében. |
| Mérföldkő dátuma | Gyorslétrehozás | Állítsa be azt a dátumot, amikor az automatikus számlalétrehozási folyamatának keresnie kell a mérföldkő állapotát, hogy figyelembe vegye a számlázás szempontjából. | Ez továbbításra kerül a projekt szerződéssor-mérföldkövéhez és a számlához. |
| Számla állapota | Gyorslétrehozás | Mérföldkő létrehozásakor az állapot mindig a **Nem kész a számlázásra** állapotra van beállítva. | Ez továbbításra kerül a projekt szerződéssor-mérföldkövéhez és a számlához. |
| Sor összege | Gyorslétrehozás | Az ügyfélnek számlázott mérföldkő összege vagy értéke. | Ez továbbításra kerül a projekt szerződéssor-mérföldkövéhez és a számlához. |
| Adó | Gyorslétrehozás | A mérföldkőre alkalmazandó adó összege. | Ez továbbításra kerül a projekt szerződéssor-mérföldkövéhez és a számlához. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]