---
title: Alvállalkozói szerződés sorai időre
description: Ez a témakör elmagyarázza, hogyan kell rögzíteni az alvállalkozói szerződéssorokat az időre vonatkozóan, és hogyan kell rögzíteni az idő beszerzését a szállítóktól.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323869"
---
# <a name="subcontract-lines-for-time"></a>Alvállalkozói szerződés sorai időre

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Dynamics 365 Project Operations rendszerben egy alvállalkozói szerződésnek lehet egy alvállalkozói szerződés sora az időre vonatkozóan. Az alvállalkozói idősorok lehetővé teszik a projektmenedzser számára, hogy a projektfeladatok és az erőforrásigények ellátásához szállítói erőforrás-időt vásároljon.

Ha a Project Operations rendszerben szeretne létrehozni egy alvállalkozói szerződéssort az időre vonatkozóan, hajtsa végre a következő lépéseket.

1. A navigációs ablaktáblán válassza az **Alvállalkozói szerződések** elemet, és nyisson meg egy alvállalkozói szerződést.
2. Az **Alvállalkozói szerződéssorok** lapon válassza az **Új** lehetőséget egy új alvállalkozói szerződéssor létrehozásához.
3. A **Gyors létrehozás** lapon a **Tranzakcióosztály** mezőben válassza az **Idő** elemet.
4. Adja meg a fennmaradó mezőinformációkat, majd válassza a **Mentés** lehetőséget.

  A következő táblázat az **Alvállalkozói szerződés sor** lap és a **Gyors létrehozás** lap mezőivel kapcsolatos információkat tartalmazza.

| **Mező** | **Leírás** |
| --- | --- |
| Adatfolyam neve | Az alvállalkozói szerződés sorának neve. |
| Ismertetés | Az alvállalkozói szerződéssoron vásárolt szolgáltatások rövid leírása. | 
| Sor típusa | Ez a mező alapértelmezett érték.  |
| Számlázási mód | Válassza ki a számlázási módot. A hivatkozott alvállalkozói szerződéssor számlázási módszere alapján a fix áras számlázási módszerhez mérföldkő alapú számlázási ütemterv áll rendelkezésre. |
| Tranzakcióosztály | Ez a mező egy alapértelmezett érték, amely azt jelzi, hogy az alvállalkozói szerződéssort az alvállalkozói idő beszerzésének rögzítésére használják. |
| Beosztás | Azon alvállalkozói erőforrások szerepe, akiknek az idejét megvásárolják. Az alvállalkozói erőforrásokhoz rendelt szerepkör határozza meg a beszerzés költségét. |
| Kért kezdés | Az az időpont, amikor az alvállalkozói erőforrásoknak meg kell kezdeniük a munkát. A kért kezdés az alvállalkozói szerződéshez csatolt projektárlisták közül a projektárlista kiválasztására szolgál. A szerep költsége az alvállalkozói szerződés soron ezután az adott árlistából adódik. |
| Kért befejezés | Az alvállalkozói erőforrások megbízásának lejárati dátuma. Ez a dátum arra szolgál, hogy figyelmeztetéseket jelenítsen meg, amikor a projektmenedzser az ezen időpont után felmerülő erőforrásigényekre vonatkozóan ebből a kapacitásból merít. |
| Megrendelt mennyiség | A szállítótól vásárolt Szerepkör órák száma. Ez az érték figyelmeztetések megjelenítésére szolgál, amikor a projektmenedzser túlterheli ezt a kapacitást az erőforrásigényeire. |
| Egységcsoport | Ennek a mezőnek az értéke alapértelmezés szerint az Időegység csoportot jelenti, és nem módosítható.  |
| Kiszerelés | Ez a mező alapértelmezés szerint az Időegység csoportból az órák alapegységét tartalmazza. Ezt az értéket úgy módosíthatja, hogy az Időegység csoport bármelyik egységét, például napot vagy hetet vásárolhassa meg. A Szerep és az Egység kombinációja az alvállalkozói szerződéssor egységárának kiszámítására szolgál. |
| Egységár | Az egységár alapértelmezés szerint a projektárlistában szereplő, az alvállalkozói szerződéssor kért kezdőnapjára vonatkozó Szerep és Egység kombinációjából adódik. Ha az alkalmazandó projektárlista az árat az alvállalkozói szerződés sorában szereplő egységtől eltérő egységben határozza meg, a rendszer az egységár kiszámításához az egységre történő átváltást használja. |
| Részösszeg | Ez egy csak olvasható mező, amely automatikusan a **Mennyiség x Egységár** számítással kerül kiszámításra, ha mind a mennyiség, mind az egységár értékét megadják. Ha a mennyiség, az egységár vagy mindkettő üres, akkor a mezőbe beírhat egy értéket. |
| Forgalmi adó |  Adja meg az áfa összegét. |
| Teljes összeg | Az alvállalkozói szerződés sorának teljes összege az adók figyelembevétele után. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
