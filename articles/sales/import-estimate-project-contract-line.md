---
title: Becslések importálása egy projektalapú szerződéssorba
description: Ez a témakör azt ismerteti, hogyan lehet becsléseket importálni egy projektből egy szerződéssorba.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6dde924c24dcffe2a8fb690e6eb429e4c3d9fb28
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126396"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Becslések importálása egy projektalapú szerződéssorba

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A Dynamics 365 Project Operations alkalmazásban becsléseket importálhat egy projektből egy projektalapú szerződéssorba.

1. Ellenőrizze, hogy a **Projekt** mező a projektalapú szerződéssoron ki van-e töltve.
2. A **Szerződéssor részletei** lapon, az alrácson válassza az **Importálás projektbecslésből** lehetőséget. Megnyílik egy párbeszédpanel az összesítési lehetőséggel. A rendelkezésre álló összesítési lehetőségek a következők: **Tranzakcióosztály**, **Kategória**, **Szerepkör** és **Projektfeladat**. Az összegzésre kiválasztottak alapján a program átmásolja a projekt becslését a szerződéssorban található összes tranzakcióosztály és feladat esetében. 
3. Annak ellenőrzéséhez, hogy milyen tranzakciós osztályok szerepelnek a rendszerben, az **Általános** lapot az árajánlatsorban, és ellenőrizze az **Idővel együtt**, a **Kiadásokkal együtt** és a **Díjakkal együtt** mezőket.

A becslések importálásakor az alkalmazás alapértelmezés szerint a szerződéshez kapcsolt projektárlisták és a szerződéssorban beállított számlázási típus alapján állítja be az árképzést. Ha a szerződéssorban egy feladat, szerepkör vagy kategória nem számlázhatóként van beállítva, az importált becslési sor ahhoz a szerepkörkategóriához nem számlázhatóként lesz beállítva, és nem lesz hozzáadva a szerződéssor szerződött értékéhez.

Amikor egy szerződéssor sorrészletekkel rendelkezik, a szerződéssor **Szerződés értéke** és a **Becsült adó** mezői összesítve vannak, és nem szerkeszthetők.

Ha több összesítési beállítás van kiválasztva, a rendszer megkísérli az összes kijelölt beállítás összesítését. Az összefoglaló kimenet több importált szerződéssort eredményez, mint ha csak egy összesítési beállítást választ ki.

Ha például a projekt a következő becslési sorokkal rendelkezett a kiadások esetében:

| Feladatok | Kategória | Dátum | Mennyiség | Egységár | Mennyiség |
| --- | --- | --- | --- | --- | --- |
| A feladat | Légi szállítás | 2020.01.10. | 4 | 400 | 1600 |
| B feladat | Szálloda | 2020.01.10. | 4 | 200 | 800 |
| C feladat | Szálloda | 2020.01.11. | 2 | 200 | 400 |

Amikor a felhasználó a **Tranzakciós osztály** szerint összesíti az adatokat, a következő információkat importálja a rendszer:

| Feladatok | Kategória | Dátum | Mennyiség | Egységár | Mennyiség |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 2020.01.10. | 3.34. | 840 | 2800. |

Amikor a felhasználó a **Tranzakciós osztály** és **Kategória** szerint összesíti az adatokat, a következő információkat importálja a rendszer:

| Feladatok | Kategória | Dátum | Mennyiség | Egységár | Mennyiség |
| --- | --- | --- | --- | --- | --- |
| A feladat | Légi szállítás | 2020.01.10. | 4 | 400 | 1600 |
| &nbsp;  | Szálloda | 2020.01.10. | 6 | 200 | 1200 |

Amikor a felhasználó a **Tranzakciós osztály**, **Kategória** és **Levélcsomópont-feladat** szerint összesíti az adatokat, a következő információkat importálja a rendszer. Figyelje meg, hogy ez az eredmény ugyanaz, mint ami a projekten volt:

| Feladatok | Kategória | Dátum | Mennyiség | Egységár | Mennyiség |
| --- | --- | --- | --- | --- | --- |
| A feladat | Légi szállítás | 2020.01.10. | 4 | 400 | 1600 |
| B feladat | Szálloda | 2020.01.10. | 4 | 200 | 800 |
| C feladat | Szálloda | 2020.01.11. | 2 | 200 | 400 |