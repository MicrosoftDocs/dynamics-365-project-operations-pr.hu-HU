---
title: Költségkategóriák alvállalkozói szerződéssorai
description: Ez a cikk azt ismerteti, hogyan rögzíthet alvállalkozói sorokat a költségekhez, és hogyan használhatja a mezőket a szállítóktól való idővásárlás rögzítésére.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7166642abc2187a53f7019639df6f0d7124f4765
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261843"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Költségkategóriák alvállalkozói szerződéssorai

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Dynamics 365 Project Operations oldalon egy alvállalkozói szerződésnek lehet egy sora a költségkategóriák számára. A költségkategóriák alvállalkozói sorai lehetővé teszik a projektmenedzser számára, hogy olyan szolgáltatás- vagy termékkategóriákat vásároljon a szállítóktól, amelyeket a projektre terhelhet.

A Project Operations rendszerben a költségkategóriákhoz tartozó alvállalkozói szerződéssor létrehozásához hajtsa végre a következő lépéseket.

1. A navigációs ablaktáblán válassza az **Alvállalkozói szerződések** lehetőséget, és nyissa meg azt az alvállalkozói szerződést, amellyel dolgozni szeretne.
2. Az **Alvállalkozói szerződés sorai** lapon válassza az **Új** lehetőséget egy új sor létrehozásához.
3. A **Gyors létrehozás** oldalon a **Tranzakcióosztály** mezőben válassza a **Költség** elemet, és adja meg vagy válassza ki a többi szükséges mező információit.

A következő táblázat az **Alvállalkozói szerződés sorának** részletei lap és a **Gyors létrehozás** lap mezőivel kapcsolatos információkat tartalmazza.

| **Mező** | **Leírás** | **Funkcionális hatás** |
| --- | --- | --- |
| Adatfolyam neve | Az alvállalkozói szerződéssor neve, amely segítséget nyújt az azonosításában. | Ez lesz megjelenítve első oszlopként minden olyan keresésben, amelyek az alvállalkozói sorokon alapulnak. |
| Ismertetés | Az alvállalkozói szerződéssorban megvásárolt költségkategóriák rövid leírása. | Egyik sem |
|Sor típusa | Ennek a mezőnek az alapértelmezett értéke **Mennyiségalapú**. |Egyik sem |
| Számlázási mód | Ez egy olyan értékkészlet, amely a Project Operations által támogatott két fő szerződési modelljét jelképezi: **Rögzített ár** és **Idő és anyag**. | A rögzített árú számlázási mód kiválasztása esetén a mérföldkőkalapú számlaütemezés elérhetővé válik az alvállalkozói szerződéssorok számára. |
| Tranzakcióosztály | Ennek a mezőnek az alapértelmezett értéke **Idő**. Ha alvállalkozói szerződéssorokat szeretne létrehozni a termékek beszerzéséhez, állítsa a **Tranzakcióosztály** mezőt **Költségre**.  | Ez azt jelzi, hogy az alvállalkozói szerződéssor a projektekben használt költségkategóriák vásárlásának rögzítésére használatos. |
| Tranzakció kategóriája | Megjeleníti a rendszerben az aktív tranzakciókategóriák listáját. |Egyik sem |
| Kért kezdés | Adja meg azt a dátumot, amikor a vásárlási kategóriáknak elérhetőnek kell lennie a szállítótól. | A kért kezdés egy projektárlista választására használható az alvállalkozói szerződéshez csatolt projektárlistákból. Az alvállalkozói szerződéssor kategóriaköltsége az adott árlistából származik. |
| Kért befejezése | Adja meg azt a dátumot, amikor már nem lesz szükség a vásárlási kategóriákra. | Ez figyelmeztetések megjelenítésekor használatos, amikor a projektmenedzser az alvállalkozói szerződéssort a projekt adott költségbecsléséhez társítja, amelyekre ezen dátum után van szükség. |
| Megrendelt mennyiség | Az szállítótól megvásárolt kategória mennyisége. | Ez figyelmeztetések megjelenítésére használatos, ha a projektmenedzser túllép ezt a mennyiséget.|
| Egységcsoport | Az alapértelmezett érték a kiválasztott kategóriához beállított alapértelmezett egységcsoporton alapul. |Egyik sem |
| Kiszerelés | Az alapértelmezés a kiválasztott kategóriához beállított alapértelmezett egységen alapul.  | A rendszer a **Kategória** és az **Egység** kombinációját használja az alvállalkozói szerződéssor egységárának alapértelmezett vagy számított értékként.  |
| Egységár | Az alapértelmezett érték a **Kategória** és **Egység** kombinációját használja a projektárlistához kapcsolódó kategóriaárakból, amely az alvállalkozói szerződéssor kért kezdéséhez alkalmazható. |Egyik sem |
| Részösszeg | Ez egy csak olvasható mező, amely X mennyiség egységáraként van számítva, ha a mennyiség és az egységár is meg van adva. Ha bármelyik mező üres, akkor ebben a mezőben is megadhatja az értéket. |Egyik sem |
| Forgalmi adó | Adja meg az áfa összegét. |Egyik sem |
| Teljes összeg | Az alvállalkozói szerződés sorának teljes összege az adókkal együtt. Ez a mező a Részösszeg + Forgalmi adó összegeként kerül kiszámításra. |Egyik sem |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
