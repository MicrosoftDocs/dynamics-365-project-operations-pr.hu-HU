---
title: Becslések importálása projektből projektajánlat-sorba
description: Ez a cikk arról nyújt tájékoztatást, hogyan importálhat becsléseket egy projektből egy projektajánlati sorba.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 61c9660f18882d12a7da8965c23b65e408256219
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824489"
---
# <a name="import-estimates-from-a-project-to-a-project-quote-line"></a>Becslések importálása projektből projektajánlat-sorba 

_**A következőre vonatkozik:** Egyszerű központi telepítés – proforma számlázás, Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ha egy projekt az értékesítést megelőző fázisban jön létre, megadhatja, hogy a projektből a pénzügyi becslést importálja a projektalapú ajánlatsorba.

1. Ügyeljen arra, hogy a projektalapú árajánlatsor a projektadatokat a **Projekt** mezőben tartalmazza.
2. Az **Árajánlatsor részletei** lapon válassza az **Importálás projektbecslésből** lehetőséget.
3. A megnyíló párbeszédpanelen válasszon egyet az alábbi összefoglalási lehetőségek közül.

  - **Tranzakcióosztály**
  - **Kategória**
  - **Szerepkör** 
  - **Projektfeladat**

A kiválasztott érték alapján a program átmásolja a projekt becslését az árajánlatsorban található összes tranzakcióosztály esetében. Ha ellenőrizni akarja, hogy milyen tranzakcióosztályok szerepelnek, jelölje be a projektalapú ajánlatsor **Általános** fület, és ellenőrizze az **Idővel együtt**, a **Költségekkel együtt**, az **Anyagokkal együtt**, és a **Díjakkal együtt** értékeket.  Ha szeretné megtekinteni, hogy milyen feladatok szerepelnek,válassza a **Számlázható feladatok** lapot az ajánlatsorok között.

A hozzárendelt Feladatoktól és a belefoglalt tranzakciós osztályoktól függően, a rendszer a feladathoz és a tranzakciós osztályok kombinációhoz tartozó összes becslést a szerződéssorba importálja.

A becslések importálásakor a rendszer alapértelmezés szerint az árajánlathoz kapcsolt projektárlisták és a projektalapú árajánlatsorban beállított számlázási típus alapján állítja be az árképzést. Ha a projektalapú árajánlatsorban egy feladat, szerepkör vagy kategória nem számlázhatóként van beállítva, az importált becslési sor nem számlázhatóként lesz beállítva, és nem fog szerepelni az árajánlatsor ajánlott értékében.

Amikor egy árajánlatsor sorrészletekkel rendelkezik, az árajánlatsor **Ajánlati érték** és **Becsült adó** mezői összesítve vannak, és nem szerkeszthetők.

Ha több összesítési beállítás van kiválasztva, a rendszer megkísérli az összes kijelölt beállítás összesítését. Ennek eredménye, hogy az importált árajánlatsorok kimenete nagyobb lesz, mint ha csak egy összesítési beállítást jelölt volna ki.

Ha például a projekt a következő becslési sorokkal rendelkezett a kiadások esetében.

| Feladatok | Kategória | Dátum | Mennyiség | Egységár | Mennyiség |
| --- | --- | --- | --- | --- | --- |
| A feladat | Légi szállítás | 2020.01.10. | 4 | 400 | 1600 |
| B feladat | Szálloda | 2020.01.10. | 4 | 200 | 800 |
| C feladat | Szálloda | 2020.01.11. | 2 | 200 | 400 |

Amikor a felhasználó a tranzakciós osztály szerint összesíti az adatokat, a következő információkat importálja a rendszer.

| Feladatok | Kategória | Dátum | Mennyiség | Egységár | Mennyiség |
| --- | --- | --- | --- | --- | --- |
|||2020.01.10. | 3.34 | 840 | 2800 |

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
