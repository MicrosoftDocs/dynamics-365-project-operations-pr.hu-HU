---
title: Termékek alvállalkozói sorai
description: Ez a témakör elmagyarázza, hogyan rögzítse a termékek alvállalkozói sorait, és hogyan használja a különböző mezőket a szállítóktól történő termékbeszerzések rögzítésére.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323689"
---
# <a name="subcontract-lines-for-products"></a>Termékek alvállalkozói sorai

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Dynamics 365 Project Operations rendszerben található alvállalkozói szerződésnek lehet egy alvállalkozói sora a termékekhez. Ezek a sorok lehetővé teszik a projektmenedzser számára, hogy termékeket vásároljon a szállítóktól, amelyeket aztán felhasználhat a projektfeladatokhoz.

A következő lépésekkel hozzon létre alvállalkozói sort a termékekhez a Project Operations-ben.

1. A navigációs oldalon válassza az **Alvállalkozói szerződések** lehetőséget, majd nyissa meg azt az alvállalkozói szerződést, amellyel dolgozni szeretne. 
2. Az **Alvállalkozói szerződéssorok** lapon válassza az **+ Új** lehetőséget egy új alvállalkozói szerződéssor létrehozásához.
3. A **Gyors létrehozás** oldalon a **Tranzakciós osztály** mezőben válassza az **Anyagot**, és adja meg vagy válassza ki a szükséges mezőinformációkat. 
4. Válassza a **Mentés** parancsot.

A következő táblázat az **Alvállalkozói szerződéssor részletezése** lap és a **Gyors létrehozás** lap mezőiről nyújt információt, mivel azok a termékek beszerzése szempontjából relevánsak.

| Mező | Ismertetés |
| ----- | ----------- |
| Adatfolyam neve | Az alvállalkozói szerződés sorának neve. |
| Ismertetés | Az alvállalkozói soron megrendelt termékek rövid leírása. |
| Sor típusa | A mező értéke alapértelmezés szerint **Mennyiségalapú**. |
| Számlázási mód |  Az alvállalkozói szerződéssor számlázási módja. A fix áras számlázási módszerekhez mérföldkőalapú számlázási ütemterv áll rendelkezésre. |
| Tranzakcióosztály | A mező értéke alapértelmezés szerint **Idő**. A beszerzési termékek alvállalkozói sorainak létrehozásához a **Tranzakciós osztály** mezőben válassza az **Anyagot**. Ez a kiválasztás azt jelzi, hogy az alvállalkozói szerződés sort a projektekben felhasználandó termékek beszerzésének nyilvántartására használják. |
| Termék kiválasztása | Válassza ki, hogy a megvásárolni kívánt termék szerepel-e a termékkatalógusban, vagy beírt termékről van-e szó. |
| Termék | Válasszon ki egy aktív terméket a katalógusból. Ez a mező csak akkor érhető el, ha a **Termék kiválasztása** a **Létező** beállításra van állítva. |
| Manuálisan rögzített termék | Írja be a beírandó termék nevét. Ez a mező csak akkor érhető el, ha a **Termék kiválasztása** **Beírásra** van állítva.  |
| Kért szállítási dátum | Válassza ki a termékek kívánt szállítási dátumát. Ezt a dátumot arra is használják, hogy kiválasszák a projektárlistát az alvállalkozói szerződéshez csatolt projektárlisták közül. Az alvállalkozói soron szereplő termék ára ezután az adott árlistából adódik. |
| Szerződés szerinti szállítási határidő | Válassza ki azt az időpontot, amikor a termékeket szerződés szerint leszállítják.  |
| Megrendelt mennyiség | Adja meg a szállítótól vásárolt termék mennyiségét. Ha a projektmenedzser túllépi ezt a mennyiséget, figyelmeztetés jelenik meg. |
| Egységcsoport | Ez az érték alapértelmezés szerint csak a katalógus termékek esetében érvényes. Ha a **Termék** és a **Kért szállítási dátum** is ki van választva, a rendszer a szállítási dátum alapján választja ki az alkalmazandó árlistát. A kapcsolódó árlista tételekből lekérdezzük a megfelelő terméket. Az egység és az egységcsoport értékei alapértelmezés szerint az árlista tételrekordjának beállításaiból származnak. |
| Kiszerelés | Ez az érték alapértelmezés szerint az árlista tételrekordjában beállított egység. Ezt szükség szerint megváltoztathatja egy másik egységre. A termék és az egység kombinációja a meglévő katalógustermékek alvállalkozói sorában az egységár alapértelmezett beállítására szolgál. |
| Egységár | Az egységár alapértelmezés szerint a projekt árlistájához kapcsolódó árlistatételekből a termék és az egység kombinációját használja, amely az alvállalkozói szerződéssor kért szállítási dátumára vonatkozik.  |
| Részösszeg | Ez a csak olvasható mező a Mennyiség x Egységár számítással kerül kiszámításra, ha mindkét mezőbe értéket adtak meg. Ha a **Mennyiség** mező, az **Egységár** mező vagy mindkettő üres, akkor manuálisan adhat meg egy értéket.  |
| Forgalmi adó | Adja meg a forgalmi adó értékét. |
| Teljes összeg | Ez a számított mező az alvállalkozói szerződés sorának teljes összegét mutatja az adók figyelembevétele után. Az ebben a mezőben szereplő érték a részösszeg + adó összegeként kerül kiszámításra. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
