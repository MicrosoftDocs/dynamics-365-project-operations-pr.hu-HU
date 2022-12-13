---
title: Projektbecslések importálása egy projektszerződéssorra
description: Ez a cikk azt ismerteti, hogyan lehet pénzügyi becsléseket importálni egy projektből egy szerződéssorba.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 73ae0ccbb5372c9dfbc28ac154094c89add0913d
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824677"
---
# <a name="import-estimates-from-a-project-to-a-project-contract-line"></a>Projektbecslések importálása egy projektszerződéssorra

_**Alkalmazási terület:** Egyszerűsített üzembe helyezés – ajánlat a proforma számlázásra, Project Operations erőforrás/nem készletalapú forgatókönyvekhez_ _

A Dynamics 365 Project Operations alkalmazásban projektbecsléseket importálhat egy projektalapú szerződéssorból.

1. Ellenőrizze, hogy a **Projekt** mező a projektalapú szerződéssoron ki van-e töltve.
2. A **Szerződéssor részletei** lapon, az alrácson válassza az **Importálás projektbecslésből** lehetőséget. Megnyílik egy párbeszédpanel az összesítési lehetőséggel. A rendelkezésre álló összesítési lehetőségek a következők: **Tranzakcióosztály**, **Kategória**, **Szerepkör** és **Projektfeladat**.
3. A kiválasztott összegzés alapján a program átmásolja a projekt becslését a szerződéssorban található összes tranzakcióosztály és feladat esetében. Annak ellenőrzéséhez, hogy milyen tranzakciós osztályok szerepelnek a rendszerben, az **Általános** lapot a projektalapú árajánlatsorban, és ellenőrizze az **Idővel együtt**, a **Kiadásokkal együtt** és a **Díjakkal együtt** mezőket. 
4. Ha szeretné megtekinteni, hogy milyen feladatok szerepelnek,válassza a **Számlázható feladatok** lapot a szerződéssorok között. A hozzárendelt feladatok alapján a **Szerepeltetett tranzakciós osztályok** **Igen** értékre van állítva, a rendszer a feladathoz és a tranzakciós osztályok kombinációhoz tartozó összes becslést a szerződéssorba importálja.

A becslések importálásakor a rendszer alapértelmezés szerint a szerződéshez kapcsolt projektárlisták és a szerződéssorban beállított számlázási típus alapján állítja be az árképzést. Ha a szerződéssorban egy feladat, szerepkör vagy kategória nem számlázhatóként van beállítva, az importált becslési sor nem számlázhatóként lesz beállítva, és nem lesz hozzáadva a szerződéssor szerződött értékéhez.

Amikor egy szerződéssor sorrészletekkel rendelkezik, a szerződéssor **Szerződés értéke** és **Becsült adó** mezői összesítve vannak, és nem szerkeszthetők.

Ha több összesítési beállítás van kiválasztva, a rendszer megkísérli az összes kijelölt beállítás összesítését. Az összefoglaló kimenet több importált szerződéssort eredményez, mint ha csak egy összesítési beállítást választ ki.

Ha például a projekt a következő becslési sorokkal rendelkezik a kiadások esetében:

| Feladatok | Kategória | Dátum | Mennyiség | Egységár | Mennyiség |
| --- | --- | --- | --- | --- | --- |
| A feladat | Légi szállítás | 2020.01.10. | 4 | 400 | 1600 |
| B feladat | Szálloda | 2020.01.10. | 4 | 200 | 800 |
| C feladat | Szálloda | 2020.01.11. | 2 | 200 | 400 |

Amikor a felhasználó a **Tranzakciós osztály** szerint összesíti az adatokat, a következő információkat importálja a rendszer:

| Feladatok | Kategória | Dátum | Mennyiség | Egységár | Mennyiség |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 2020.01.10. | 3.34. | 840 | 2800. |

Amikor a felhasználó a **Tranzakciós osztály** és **Kategória** szerint összesíti az adatokat, a következő információkat importálja a rendszer:

| Feladatok | Kategória | Dátum | Mennyiség | Egységár | Mennyiség |
| --- | --- | --- | --- | --- | --- |
| A feladat | Légi szállítás | 2020.01.10. | 4 | 400 | 1600 |
| &nbsp;| Szálloda | 2020.01.10. | 6 | 200 | 1200 |

Amikor a felhasználó a **Tranzakciós osztály**, **Kategória** és **Levélcsomópont-feladat** szerint összesíti az adatokat, a következő információkat importálja a rendszer. Figyelje meg, hogy ez az eredmény ugyanaz, mint ami a projekten:

| Feladatok | Kategória | Dátum | Mennyiség | Egységár | Mennyiség |
| --- | --- | --- | --- | --- | --- |
| A feladat | Légi szállítás | 2020.01.10. | 4 | 400 | 1600 |
| B feladat | Szálloda | 2020.01.10. | 4 | 200 | 800 |
| C feladat | Szálloda | 2020.01.11. | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
