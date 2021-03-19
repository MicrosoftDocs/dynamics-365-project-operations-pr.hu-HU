---
title: Költség- és értékesítési árak beállítása a kiadásokhoz
description: Ez a témakör a költség és értékesítési ráták tranzakciós és költségkategóriákhoz való beállításával kapcsolatban tartalmaz tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee52daae18c5f9f0b630e54359021fffe1759274
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274911"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Költség- és értékesítési árak beállítása a kiadásokhoz

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations tranzakciókategóriáihoz tartozó költségeket és értékesítési árakat állíthat be. Mivel a költség- és értékesítési árakat a kiadásokhoz tervezték, az összes olyan tranzakciós kategóriát, amely tartalmazza ezeket, szintén költségkategóriaként kell beállítani. Ez a beállítás biztosítja a későbbi funkciók pontosságát. A tranzakciós kategóriákhoz tartozó költség- és értékesítési árak csak egy pénznemben szerepelhetnek, amelynek a pénznemnek kell lennie az árlista fejlécében.

A tranzakciós kategóriákhoz tartozó költség- és értékesítési árak beállításához hajtsa végre az alábbi lépéseket. 

1. Hozzon létre egy árlistát az árlista fejléce alapján. 
2. A **Kategóriaárak** helyen a részrács menüben válassza az **+ Új kategóriaár** lehetőséget. 
3. A **gyors létrehozás** lapon adja meg a tranzakció kategóriáját és azt az egységet, amelyhez új árat hoz létre.

Az alábbi táblázat egy kategória ársorának **általános** lap és a **gyors létrehozás** oldalának mezőit sorolja fel, amelyeket érdemes szem előtt tartani, amikor értékesítési vagy önköltségi árlistát hoz létre a kategóriaárakon.

| Mező | Hely | Adatfolyam leírása | Alsóbb rétegbeli hatás |
| --- | --- | --- | --- |
| Tranzakció kategóriája | **Általános** lap és a **Gyorslétrehozás** oldalak | Válassza ki azt a tranzakciós kategóriát, amelyhez értékesítési vagy önköltségi árat hoz létre. | A bejövő becslésen vagy a tényleges költségértéken szereplő tranzakciós kategóriát ezzel a sorral kell összehangolni a tranzakciós kategória alapértelmezett költség- vagy értékesítési díjának meghatározásához. |
| Egységütemezés | **Általános** lap és a **Gyorslétrehozás** oldalak | Az egység ütemezése alapértelmezett értéke a tranzakció kategóriájának egységütemezéséből származik. | Ennek a mezőnek nincs későbbi hatása. |
| Kiszerelés | **Általános** lap és a **Gyorslétrehozás** oldalak | Válassza ki azt az egységet, amelyhez be vannak állítva az árak. | A bejövő becslésen vagy a tényleges értéken szereplő egység a sorban szereplő egységgel van megfeleltetve, hogy a költségbecslés vagy a tényleges érték díjának alapértelmezett értékét megadja. |
| Árképzési mód | **Általános** lap és a **Gyorslétrehozás** oldalak | Az **árképzési mód** mező lehetséges értékei a következők: **Egységár**, **költségen** és **haszonkulcs a költségnél**. | Az ár beállítása közben az **Egységár** kiválasztásával zárolja a Kategória ára sor **százalékos** mezőjét. Ha a **Költségen** van kiválasztva, az **Ár** és a **Százalék** mezők zárolva vannak az értékesítési árlistán. A **Haszonkulcs a költség felett** zárolja az értékesítési árlista **Ár** mezőjét. A tényleges költségre vonatkozó bejövő aktuális sorban a **Költségen** vagy **Haszonkulcs a költség felett** árképzési módszer eredménye, hogy a kapcsolódó számlázatlan értékesítési sort olyan árhoz rendelik hozzá, amely megegyezik az ár felett haszonkulcsként számított ár vagy a tényleges kölség árával. |
| Ár | **Általános** lap és a **Gyorslétrehozás** oldalak | Állítson be egy egységárat a tranzakció kategóriára és az egység kombinációra vonatkozóan. Például a útiköltség ára 10 USD mérföldenként és a 8 USD kilométerenként. | Az útiköltség díja azt a költséget adja meg, amely a bejövő becslés vagy a tényleges sor egységnyi árára vagy költségére érvényes a költség tranzakciós osztályban.|
| Százalék | **Általános** lap és a **Gyorslétrehozás** oldalak | Állítson be egy költség százalékot a tranzakció kategóriára és az egység kombinációra vonatkozóan. Például a repülőjegy értékesítési rátánál 10 százalék hoszonkulcsot kell alkalmazni a felmerült repülőjegy költségén felül. | Ez a költség feletti százalék csak akkor alkalmazható egy értékesítési árlistán, ha a kiválasztott árképzési mód **Haszonkulcs a költség felett**. |
| Pénznem | **Általános** lap és a **Gyorslétrehozás** oldalak | Ez az érték alapértelmezés szerint az árlista fejlécében szereplő pénznemből származik. A tranzakciós kategóriák árazása esetén a pénznemet nem lehet felülírni. | Ez a pénznem alapértelmezett értéke a bejövő tényleges sor egységnyi ára, a költségre és értékesítésre vonatkozó költségtranzakciós osztályhoz. |

## <a name="pricing-methods-for-expenses"></a>A kiadások árképzési módszerei

Ha olyan kategóriájú árakat állít be, amelyek csak a költségek árazásával kapcsolatosak, a következő három árazási módszer egyike használható:

- **Egységár**
- **Költségen**
- **Haszonkulcs feletti költség**

### <a name="price-per-unit"></a>Kiszerelésenkénti ár
Ha ez az árképzési mód van kiválasztva egy értékesítési árlistához tartozó kategóriaár sorában, akkor a kategória -és az egység-kombinációra vonatkozó alapértelmezett ár a becslésben és a tényleges értékben is szerint szerepel. A becslés a projektek becsült soraira, az ajánlati sor részleteire és a szerződéssorok részleteire hivatkozik a kiadások esetében.

### <a name="at-cost"></a>Költségen
Ha ez az árképzési mód van kiválasztva az értékesítési árlistához tartozó kategóriaár sorában, akkor a kategória -és az egység-kombinációra vonatkozó alapértelmezett ár csak a tényleges költségértékben szerepel. Például a kiadási tranzakció osztály nem számlázott értékesítési adatai. Az Egységár az adott költség tényleges értékének megfelelő egységáron állítható be a számlázatlan értékesítés tényleges értékéből. A költségekre alapuló alapértelmezett ár nem a projektek becsült költségeire, illetve az ajánlati sorra, valamint a kiadásokra vonatkozó szerződéssorok részleteire vonatkozóan történik.

### <a name="markup-over-cost"></a>Haszonkulcs feletti költség
Ha ez az árképzési mód van kiválasztva az értékesítési árlistához tartozó kategóriaár sorában, akkor a kategória -és az egység-kombinációra vonatkozó alapértelmezett ár csak a tényleges költségértékben szerepel. Például a kiadási tranzakció osztály nem számlázott értékesítési adatai. Ezt az egységárat a rendszer az adott költségre vonatkozó tényleges költség aktuális értéke alapján számított értékre állítja be a számlázott értékesítésre vonatkozóan, miután a megadott haszonkulcsi százalékot alkalmazza. A költségekre alapuló alapértelmezett ár nem a projektek becsült költségeire, illetve az ajánlati sorra, valamint a kiadásokra vonatkozó szerződéssorok részleteire vonatkozóan történik.


[!INCLUDE[footer-include](../includes/footer-banner.md)]