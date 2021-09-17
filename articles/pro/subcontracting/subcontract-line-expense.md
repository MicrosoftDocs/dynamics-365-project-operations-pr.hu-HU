---
title: Költségkategóriák alvállalkozói szerződéssorai
description: Ez a témakör elmagyarázza, hogyan rögzítheti az alvállalkozói szerződés sorokat a költségekre, és hogyan használhatja a mezőket a szállítóktól történő idővásárlás rögzítésére.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323824"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Költségkategóriák alvállalkozói szerződéssorai

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Dynamics 365 Project Operations oldalon egy alvállalkozói szerződésnek lehet egy sora a költségkategóriák számára. A költségkategóriák alvállalkozói sorai lehetővé teszik a projektmenedzser számára, hogy olyan szolgáltatás- vagy termékkategóriákat vásároljon a szállítóktól, amelyeket a projektre terhelhet.

A Project Operations rendszerben a költségkategóriákhoz tartozó alvállalkozói szerződéssor létrehozásához hajtsa végre a következő lépéseket.

1. A navigációs ablaktáblán válassza az **Alvállalkozói szerződések** lehetőséget, és nyissa meg azt az alvállalkozói szerződést, amellyel dolgozni szeretne.
2. Az **Alvállalkozói szerződés sorai** lapon válassza az **Új** lehetőséget egy új sor létrehozásához.
3. A **Gyors létrehozás** oldalon a **Tranzakcióosztály** mezőben válassza a **Költség** elemet, és adja meg vagy válassza ki a többi szükséges mező információit.

A következő táblázat az **Alvállalkozói szerződés sorának** részletei lap és a **Gyors létrehozás** lap mezőivel kapcsolatos információkat tartalmazza.

| **Mező** |  **Leírás** |
| ----------| ---------------- |
| Adatfolyam neve | Az alvállalkozói szerződés sorának neve. |
| Ismertetés | Az alvállalkozói szerződéssoron vásárolt szolgáltatás- vagy termékkategóriák rövid leírása. |
| Sor típusa | Ennek a mezőnek az alapértelmezett értéke **Mennyiségalapú**.  |
| Számlázási mód | Az alvállalkozói szerződéssor számlázási módja. A sor számlázási módszere alapján mérföldkő alapú számlázási ütemterv áll rendelkezésre a fix áras számlázási módszerhez.  |
| Tranzakcióosztály | Ennek a mezőnek az alapértelmezett értéke **Idő**. Ha alvállalkozói szerződéssorokat szeretne létrehozni a termékek beszerzéséhez, állítsa a **Tranzakcióosztály** mezőt **Költségre**. Ez a mezőérték azt jelzi, hogy az alvállalkozói szerződés sort a projektekben felhasználandó termék- vagy szolgáltatáskategória beszerzésének rögzítésére használják. |
| Tranzakció kategóriája | Válassza ki a tranzakciókategóriát. |
| Kért kezdés | Az az időpont, amikor a beszerzési kategóriáknak a szállítótól rendelkezésre kell állniuk. A kért kezdés az alvállalkozói szerződéshez csatolt projektárlisták közül a projektárlista kiválasztására szolgál. Az alvállalkozói szerződés sorában a kategória költsége alapértelmezés szerint ebből az árlistából származik. |
| Kért végpont | Az a dátum, amikor a vásárlási kategóriákra már nincs szükség. Ez a dátum figyelmeztető jelzést ad, amikor a projektmenedzser ezt az alvállalkozói szerződéssort az ezen időpont után keltezett projektek konkrét költségbecsléseivel társítja. |
| Megrendelt mennyiség | A szállítótól vásárolt kategória mennyisége. Ha a projektmenedzser túllépi a vásárolt mennyiséget, figyelmeztetés jelenik meg.  |
| Egységcsoport | Ez a mező értéke alapértelmezés szerint a kiválasztott kategóriához beállított alapértelmezett egységcsoporton alapul. |
| Kiszerelés | Ez a mező értéke alapértelmezés szerint a kiválasztott kategóriához beállított alapértelmezett egységen alapul. A kategória és az egység kombinációja az alvállalkozói szerződés sorában az egységár alapértelmezett értékének meghatározására szolgál. |
| Egységár | Az egységár mező értéke alapértelmezés szerint az alvállalkozói szerződés sorának kért kezdésére vonatkozó projektárlistához kapcsolódó kategória és egység kombinációja.  |
| Részösszeg | Ez a csak olvasható mező automatikusan a mennyiség egységáraként kerül kiszámításra, ha mind a mennyiség, mind az egységár értékét megadja. Ha valamelyik vagy mindkét mező üres, akkor manuálisan adhat meg egy értéket ebben a mezőben.  |
| Forgalmi adó | Adja meg az áfa összegét.  |
| Teljes összeg | Az alvállalkozói szerződés sorának teljes összege az adókkal együtt. Ez a mező a részösszeg + forgalmi adó összegeként kerül kiszámításra.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
