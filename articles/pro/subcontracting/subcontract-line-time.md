---
title: Alvállalkozói szerződés sorai időre
description: Ez a cikk azt ismerteti, hogyan rögzítheti az alvállalkozói sorokat az időre vonatkozóan, és hogyan rögzítheti a szállítóktól való idővásárlási időt.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8e9619dc713fde3127f552234e4a7427d99be683
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261985"
---
# <a name="subcontract-lines-for-time"></a>Alvállalkozói szerződés sorai időre

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Dynamics 365 Project Operations rendszerben egy alvállalkozói szerződésnek lehet egy alvállalkozói szerződés sora az időre vonatkozóan. Az alvállalkozói idősorok lehetővé teszik a projektmenedzser számára, hogy a projektfeladatok és az erőforrásigények ellátásához szállítói erőforrás-időt vásároljon.

Ha a Project Operations rendszerben szeretne létrehozni egy alvállalkozói szerződéssort az időre vonatkozóan, hajtsa végre a következő lépéseket.

1. A navigációs ablaktáblán válassza az **Alvállalkozói szerződések** elemet, és nyisson meg egy alvállalkozói szerződést.
2. Az **Alvállalkozói szerződéssorok** lapon válassza az **Új** lehetőséget egy új alvállalkozói szerződéssor létrehozásához.
3. A **Gyors létrehozás** lapon a **Tranzakcióosztály** mezőben válassza az **Idő** elemet.
4. Adja meg a fennmaradó mezőinformációkat, majd válassza a **Mentés** lehetőséget.

  A következő táblázat az **Alvállalkozói szerződés sor** lap és a **Gyors létrehozás** lap mezőivel kapcsolatos információkat tartalmazza.

| **Mező** | **Leírás** | **Funkcionális hatás** |
| --- | --- | --- |
| Adatfolyam neve | Az alvállalkozói szerződéssor neve, amely segítséget nyújt az azonosításában. | Ez lesz megjelenítve első oszlopként minden olyan keresésben, amelyek az alvállalkozói sorokon alapulnak. |
| Ismertetés | Az alvállalkozói szerződéssoron vásárolt szolgáltatások rövid leírása. |Egyik sem |
| Sor típusa |   Ennek a mezőnek az alapértelmezett értéke **Mennyiségalapú**.| Egyik sem |
| Számlázási mód | Ez egy olyan értékkészlet, amely a Project Operations által támogatott két fő szerződési modelljét jelképezi: **Rögzített ár** és **Idő és anyag**. | A kiválasztott számlázási módtól függően a rögzített árú számlázási mód kiválasztása esetén a mérföldkőkalapú számlaütemezés elérhetővé válik az alvállalkozói szerződéssorok számára. |
| Tranzakcióosztály | Alapértelmezett értéke **Idő**. | Ez azt jelzi, hogy az alvállalkozói szerződéssor az alvállalkozói idő vásárlásának rögzítésére használatos. |
| Beosztás | Jelölje ki annak az alvállalkozói erőforrásnak a szerepkörét, amelynek az idejét vásárolják. | Az alvállalkozói erőforrások által betöltött szerepkör határozza meg a vásárlás költségét. |
| Kért kezdés | Adja meg azt a dátumot, amikor az alvállalkozó erőforrásokra szükség van a munka elkezdéséhez. | Ez egy projektárlista kiválasztására használható az alvállalkozói szerződéshez csatolt projektárlistákból. Az alvállalkozói szerződéssor szerepkörköltsége az adott árlistából származik. |
| Kért befejezése | Adja meg az alvállalkozó erőforrás hozzárendelésének végét. | Ez figyelmeztetés megjelenítéséhez lesz használható, ha a projektvezető ki használ a kapacitásból az ezt a dátumot követő erőforráskövetelményekhez. |
| Megrendelt mennyiség | Adja meg, hogy hány órát vásárol ebből a szerepkörből a szállítótól. | Ez figyelmeztetések megjelenítéséhez lesz használható, ha a projektvezető felülhasználja ezt a kapacitást az erőforráskövetelményekhez. |
| Egységcsoport | Az alapértelmezett érték az **Időegység csoport**, amely nem módosítható. | Egyik sem|
| Kiszerelés | A mező alapértelmezett beállítása az **Időegység csoport** alapegysége, az óra. Ezt az értéket úgy módosíthatja, hogy az **Időegység csoport** bármelyik egységét, például napot vagy hetet vásárolhassa meg. | A rendszer a **Szerepkör** és az **Egység** kombinációját használja az alvállalkozói szerződéssor egységárának alapértelmezett vagy számított értékként. |
| Egységár | Az alapértelmezett egységár a **Szerepkör** és **Egység** kombinációját használja a projektárlistából, ami az alvállakozói szerződéssor **Kért kezdés** dátumára vonatkozik. | Ha az alkalmazandó projektárlista az árat az alvállalkozói szerződés sorában szereplő egységtől eltérő egységben határozza meg, a rendszer az egységár kiszámításához az egységre történő átváltást használja. |
| Részösszeg |    Ez egy csak olvasható mező, amely a Mennyiség és Egységár szorzataként van számítva, ha a mennyiség és az egységár is meg van adva. Ha a mennyiség, az egységár vagy mindkettő üres, akkor a mezőbe beírhat egy értéket. | Egyik sem|
| Forgalmi adó |   Adja meg az áfa összegét. |Egyik sem |
| Teljes összeg | Az alvállalkozói szerződés sorának teljes összege az adókkal együtt. Ez a mező a Részösszeg + Forgalmi adó összegeként kerül kiszámításra.|Egyik sem |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
