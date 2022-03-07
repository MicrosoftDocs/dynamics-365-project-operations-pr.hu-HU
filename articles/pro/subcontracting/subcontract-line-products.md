---
title: Termékek alvállalkozói sorai
description: Ez a témakör elmagyarázza, hogyan rögzítse a termékek alvállalkozói sorait, és hogyan használja a különböző mezőket a szállítóktól történő termékbeszerzések rögzítésére.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cda2db2b6beafb943738b35857d091f7ad17390d
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558550"
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

| Mező | Ismertetés | Funkcionális hatás|
| ----- | ----------- | ----------- |
| Adatfolyam neve | Az alvállalkozói szerződéssor neve, amely segítséget nyújt az azonosításában. |Ez lesz megjelenítve első oszlopként minden olyan keresésben, amelyek az alvállalkozói sorokon alapulnak.
| Ismertetés | Az alvállalkozói soron megrendelt termékek rövid leírása. | Egyik sem |
| Sor típusa | Ennek a mezőnek az alapértelmezett értéke **Mennyiségalapú**. |Egyik sem |
| Számlázási mód | Ez egy olyan értékkészlet, amely a Project Operations által támogatott két fő szerződési modelljét jelképezi: **Rögzített ár** és **Idő és anyag**. | A kiválasztott számlázási módtól függően a rögzített árú számlázási mód kiválasztása esetén a mérföldkőkalapú számlaütemezés elérhetővé válik az alvállalkozói szerződéssorok számára. |
| Tranzakcióosztály |Ennek a mezőnek az alapértelmezett értéke **Idő**. Alvállalkozóiszerződés-sorok létrehozásához termékek megvásárlásához állítsa a **Tranzakció osztály** mezőt **Anyag** értékre.  | Ez azt jelzi, hogy az alvállalkozói szerződéssor a projektekben használt termékek vásárlásának rögzítésére használatos. |
| Termék kiválasztása | Válassza ki, hogy a megvásárolni kívánt termék szerepel-e a termékkatalógusban, vagy beírt termékről van-e szó. |Egyik sem |
| Termék | Válasszon ki egy aktív terméket a katalógusból. Ez a mező csak akkor érhető el, ha a **Termék kiválasztása** a **Létező** beállításra van állítva. |A rendszer a **Termék** és az **Egység** kombinációját használja az alvállalkozói szerződéssor egységárának alapértelmezett vagy számított értékként.
| Manuálisan rögzített termék | Írja be a beírandó termék nevét. Ez a mező csak akkor érhető el, ha a **Termék kiválasztása** **Beírásra** van állítva.  |A rendszer nem tölti ki automatikusan a vásárlási árat a nem katalogizált termékekhez.|
| Kért szállítási dátum | Adja meg a termékek kért szállítási dátumát.| Ezt a dátumot arra is használják, hogy kiválasszák a projektárlistát az alvállalkozói szerződéshez csatolt projektárlisták közül. Az alvállalkozói soron szereplő termék ára ezután az adott árlistából adódik. |
| Szerződés szerinti szállítási határidő | Adja meg a termékek szerződésben vállalt kézbesítési dátumát.  |Egyik sem|
| Megrendelt mennyiség | Adja meg a szállítótól vásárolt termék mennyiségét.| Ez figyelmeztetések megjelenítésére használatos, ha a projektmenedzser túllép ezt a mennyiséget.|
| Egységcsoport | Ez az érték alapértelmezés szerint csak a katalógus termékek esetében érvényes. |Ha a **Termék** és a **Kért szállítási dátum** is ki van választva, a rendszer a szállítási dátum alapján választja ki az alkalmazandó árlistát. A kapcsolódó árlista tételekből lekérdezzük a megfelelő terméket. Az egység és az egységcsoport értékei alapértelmezés szerint az árlista tételrekordjának beállításaiból származnak. |
| Kiszerelés | Ez az érték alapértelmezés szerint az árlistaelem-rekordban beállított egység. Ezt szükség szerint megváltoztathatja egy másik egységre.| A termék és az egység kombinációja a meglévő katalógustermékek alvállalkozói sorában az egységár alapértelmezett beállítására szolgál. |
| Egységár | Az egységár alapértelmezés szerint a projekt árlistájához kapcsolódó árlistatételekből a termék és az egység kombinációját használja, amely az alvállalkozói szerződéssor kért szállítási dátumára vonatkozik.  |Egyik sem |
| Részösszeg | Ez a csak olvasható mező a Mennyiség x Egységár számítással kerül kiszámításra, ha mindkét mezőbe értéket adtak meg. Ha a **Mennyiség** mező, az **Egységár** mező vagy mindkettő üres, akkor manuálisan adhat meg egy értéket.  |Egyik sem |
| Forgalmi adó | Adja meg a forgalmi adó értékét. |Egyik sem |
| Teljes összeg | Ez a számított mező az alvállalkozói szerződés sorának teljes összegét mutatja az adók figyelembevétele után. Az ebben a mezőben szereplő érték a Részösszeg + Adó összegeként kerül kiszámításra. |Egyik sem |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
