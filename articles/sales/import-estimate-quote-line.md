---
title: Projektbecslések importálása egy projekt árajánlatsorhoz
description: Ez témakör a projektből történő becslések importálása egy projekt árajánlatsorába műveletről nyújt tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 40facf002ca8aa77cbd7f1cfa29dab24842fd932
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858746"
---
# <a name="import-estimates-for-a-project-to-a-project-quote-line"></a>Projektbecslések importálása egy projekt árajánlatsorhoz

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_


Ha egy projekt az értékesítést megelőző fázisban jön létre, megadhatja, hogy a projektből a pénzügyi becslést importálja a projektalapú ajánlatsorba.

1. Ügyeljen arra, hogy a projektalapú árajánlatsor a projektadatokat a **Projekt** mezőben tartalmazza.
2. Az **Árajánlatsor részletei** lapon válassza az **Importálás projektbecslésből** lehetőséget.
3. A megnyíló párbeszédpanelen válasszon egyet az alábbi összefoglalási lehetőségek közül:

  - **Tranzakcióosztály**
  - **Kategória**
  - **Szerepkör** 
  - **Projektfeladat**

A kiválasztott érték alapján a program átmásolja a projekt becslését az árajánlatsorban található összes tranzakcióosztály esetében. Annak ellenőrzéséhez, hogy milyen tranzakciós osztályok szerepelnek a rendszerben, jelölje ki az **Általános** lapot a projektalapú árajánlatsorban, és ellenőrizze az **Idővel együtt**, a **Kiadásokkal együtt** és a **Díjakkal együtt** értékeit.

A becslések importálásakor a rendszer alapértelmezés szerint az árajánlathoz kapcsolt projektárlisták és a projektalapú árajánlatsorban beállított számlázási típus alapján állítja be az árképzést. Ha a projektalapú érajánlatsorban egy szerepkör vagy kategória nem számlázhatóként van beállítva, az importált becslési sor nem számlázhatóként lesz beállítva, és nem fog szerepelni az árajánlatsor ajánlott értékében.

Amikor egy árajánlatsor sorrészletekkel rendelkezik, az árajánlatsor **Ajánlati érték** és **Becsült adó** mezői összesítve vannak, és nem szerkeszthetők.

Ha több összesítési beállítás van kiválasztva, a rendszer megkísérli az összes kijelölt beállítás összesítését. Ennek eredménye, hogy az importált árajánlatsorok kimenete nagyobb lesz, mint ha csak egy összesítési beállítást jelölt volna ki.

Ha például a projekt a következő becslési sorokkal rendelkezik a kiadások esetében.

| Feladatok | Kategória | Dátum | Mennyiség | Egységár | Mennyiség |
| --- | --- | --- | --- | --- | --- |
| A feladat | Légi szállítás | 2020.01.10. | 4 | 400 | 1600 |
| B feladat | Szálloda | 2020.01.10. | 4 | 200 | 800 |
| C feladat | Szálloda | 2020.01.11. | 2 | 200 | 400 |

Amikor a felhasználó a tranzakciós osztály szerint összesíti az adatokat, a következő információkat importálja a rendszer.

| Feladatok | Kategória | Dátum | Mennyiség | Egységár | Mennyiség |
| --- | --- | --- | --- | --- | --- |
| | | 2020.01.10. | 3.34 | 840 | 2800 |

Amikor a felhasználó a tranzakciós osztály és kategória szerint összesíti az adatokat, a következő információkat importálja a rendszer.

| Feladatok | Kategória | Dátum | Mennyiség | Egységár | Mennyiség |
| --- | --- | --- | --- | --- | --- |
| A feladat | Légi szállítás | 2020.01.10. | 4 | 400 | 1600 |
| | Szálloda | 2020.01.10. | 6 | 200 | 1200 |

Amikor a felhasználó a tranzakciós osztály, kategória és levélcsomópont-feladat szerint összesíti az adatokat, a következő információkat importálja a rendszer. Figyelje meg, hogy ez az eredmény ugyanaz, mint ami a projekten volt.

| Feladatok | Kategória | Dátum | Mennyiség | Egységár | Mennyiség |
| --- | --- | --- | --- | --- | --- |
| A feladat | Légi szállítás | 2020.01.10. | 4 | 400 | 1600 |
| B feladat | Szálloda | 2020.01.10. | 4 | 200 | 800 |
| C feladat | Szálloda | 2020.01.11. | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
