---
title: Számlaütemezések létrehozása egy projektalapú szerződéssoron - lite
description: Ez a témakör a számlaütemezések és a mérföldkövek létrehozásával kapcsolatban tartalmaz tájékoztatást.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: edacae144f5c4879d3cfdf9585281858d7312589
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581977"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Számlaütemezések létrehozása egy projektalapú szerződéssoron - lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Számlaütemezést mellékelhet egy projektalapú szerződéssorhoz. A számlázás csak akkor engedélyezett, ha a szerződést megnyerik, hogy létrehoznak egy projektszerződés létrehozásához. A számlaütemezések lehetővé teszik számlavázlatok létrehozását a projektalapú szerződéssorokhoz- Ha azt tervezi, hogy a számlákat mindig manuálisan hozza létre, akkor kihagyhatja a számlázási ütemezéseket létrehozását a projekt alapú szerződéssoron vagy a szerződéssoron.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Idő és anyag számlaütemezés létrehozása egy projektalapú szerződéssorhoz

Amikor a szerződéssor számlázási módja Idő és anyag típusú móddal rendelkezik, létrehozhat dátumalapú számlaütemezést. Ha automatikusan szeretne létrehozni egy dátumalapú számlaütemezést, hajtsa végre az alábbi lépéseket.

1. A számlázási gyakoriság beállításához nyissa meg a **Beállítások** > **Számlázási gyakoriságok** lehetőséget.
2. Nyissa meg a projektszerződést, és az **Összegzés** lapon állítsa be a kért szállítási dátumot.
3. Nyissa meg azt az idő-és anyagelszámolású szerződéssort, amelyhez dátum alapú számlázási ütemezést szeretne létrehozni. 
4. A **Számlaütemezés** lapon válassza ki a számlázás kezdési dátumát és a számlázás gyakoriságát. 
5. Az alrácson válassza a **Számlaütemezés előállítása** lehetőséget.

    A rendszer a következő mező-információkkal hozza létre a számla ütemezését:

    - A **Számla futtatási dátuma** a számla gyakoriságán alapuló dátumra van beállítva.
    - A **Tranzakció határideje** a **Számlakészítés dátuma** előtti napra van beállítva.
    - A **Futtatás állapota** beállítás automatikusan a **Nem fut** értékre van beállítva. Amikor az automatikus számlalétrehozási feladat egy bizonyos **Számlázási futtatási dátumnál** fut, akkor a program a **Futtatás sikerült** vagy a **Futtatás nem sikerült** értékre módosítja majd a mezőt.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Rögzített áru számlaütemezés létrehozása egy projektalapú szerződéssorhoz

Ha egy projektalapú szerződéssor rögzített árú számlázási móddal rendelkezik, akkor mérföldkőre épülő számlázási ütemezést hozhat létre. Hajtsa végre a következő lépéseket, hogy automatikusan létrehozza a mérföldkő alapú számlázási ütemezést mérföld kövek egy fix készletéhez a naptári időszakra vonatkozóan egyenlő elosztással.

1. A számlázási gyakoriság beállításához nyissa meg a **Beállítások** > **Számlázási gyakoriságok** lehetőséget.
2. Nyissa meg a projektszerződést, és az **Összegzés** lapon állítsa be a kért szállítási dátumot.
3. Nyissa meg azt a rögzített árú szerződéssort, amelyre mérföldkő-ütemezést kell létrehoznia. 
4. A **Számlaütemezés (Számlázási mérföldkövek)** lapon válassza ki a számlázás kezdési dátumát és a számlázás gyakoriságát. 
5. Az alrácson válassza az **Időszakos mérföldkövek létrehozása** lehetőséget.

    A rendszer a következő mérföldkő-információkkal hozza létre a számla ütemezését.

    - **Mérföldkő neve** a számla gyakorisága alapján meghatározott dátumra van beállítva.
    - **Mérföldkő dátuma** a számla gyakorisága alapján meghatározott dátumra van beállítva.
    - A **Mérföldkő összege** úgy van kiszámítva hogy a szerződés összegét a projekten alapuló szerződéssor szerint a gyakoriság, a számlázás kezdése és a kért szállítási dátum szerint megadott számú mérföldkőre osztja fel.
    - Ha a szerződéssornak van értéke a **Becsült adóösszeg** mezőben van, akkor a program ezt a mezőt a periodikus mérföldkövek létrehozásakor is az egyes mérföldkőhöz egyenlően számítja fel.

A számlázási mérföldköveknek meg kell egyezniük a projekt alapú szerződéssor szerződéses értékével. Ha nem egyenlőek, hiba történik. A hibát úgy is kijavíthatja, ha ellenőrzi, hogy a számlázási mérföldkövek összege megegyezik a teljes szerződéses összeggel úgy, hogy létrehoz, szerkeszt vagy töröl mérföldköveket. A módosítások elvégzése után frissítse az oldalt.

### <a name="manually-create-milestones"></a>Mérföldkövek manuális létrehozása

A rögzített árú mérföldkövek manuálisan is létrehozhatók, ha nem osztják el időszakosan azokat. Mérföldkő manuális létrehozásához hajtsa végre az alábbi lépéseket.

1. Nyissa meg azt a rögzített árú szerződéssort, amelyre mérföldkövet létre szeretné hozni. 
2. A **Számla ütemezés** lapon az alrácson válassza a **+ új szerződéssor-mérföldkő létrehozása** lehetőséget.
3. A **Mérföldkő létrehozása** űrlapon adja meg a szükséges információkat a következő táblázat alapján. 

| Mező | Hely | Adatfolyam leírása | Alsóbb rétegbeli hatás |
| --- | --- | --- | --- |
| Mérföldkő neve | Gyorslétrehozás | A mérföldkő nevének szövegmezője. | Ez a mező a projekt szerződéssor mérföldkövének és a számlának a része. |
| Projektfeladat | Gyorslétrehozás | Ha a mérföldkő egy projektfeladathoz kötődik, ezzel a hivatkozással egyéni logikát adhat hozzá, és a feladat állapota alapján állíthatja be a mérföldkő állapotát. | Ennek a hivatkozásnak nincs későbbi hatása egy feladatra. |
| Mérföldkő dátuma | Gyorslétrehozás | Az a dátum, amikor az automatikus számlalétrehozási folyamatnak meg kell vizsgálnia a mérföldkő állapotát, hogy figyelembe vegye a számlázáshoz. | Ez a projekt szerződéssor mérföldkövének és a számlának a része. |
| Számla állapota | Gyorslétrehozás | A mérföldkő létrehozásakor az állapot beállítása mindig **Nincs készen a számlázásra** vagy **Nem kezdődött el**. | Ez a projekt szerződéssor mérföldkövének és a számlának a része. |
| Sor összege | Gyorslétrehozás | Az ügyfélnek számlázandó mérföldkő összege vagy értéke. | Ez a mező a projekt szerződéssor mérföldkövének és a számlának a része, |
| Adó | Gyorslétrehozás | A mérföldkőre alkalmazott adó összege. | Ez a projekt szerződéssor mérföldkövének és a számlának a része. |

4. Válassza a **Mentés és bezárás** lehetőséget.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]