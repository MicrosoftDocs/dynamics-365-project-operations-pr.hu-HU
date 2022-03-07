---
title: Lehetőség fejléc/összegzés
description: Ez a témakör a projektalapú üzleteket és a projektalapú lehetőségsorokat ismerteti.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 83a47502112a4862fa7b99a7821c82730e0de0938cabe65b0dd4fc382bdd5515
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996394"
---
# <a name="header-details-for-project-based-opportunities"></a>Fejlécadatok projektalapú lehetőségek esetében

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_


A Lehetőség fejléc vagy összegzés a projektalapú ügylet összes olyan adatát rögzíti, amely a projektalapú lehetőség összes sorára vonatkozik.

A projektalapú lehetőségek a Dynamics 365 Project Operations rendszerben a Dynamics 365 Sales lehetőségek bővítményei. Ezek a bővítmények további funkciókat biztosítanak, amelyek a projektalapú lehetőségekre jellemzőek és szükségesek. Ezek a bővítmények tartalmazhatnak új mezőket és menüszalag-műveleteket, amelyek a projektalapú lehetőségekben érhetők el. Előfordulhat, hogy a Sales alkalmazásban elérhető egyes mezők, funkciók és alapértelmezett logika nem érhető el a Project Operations programban.

Az alábbi táblázat egy projektalapú lehetőség azon mezőit tartalmazza, amelyek vagy egyediek a Project Operationsben, vagy viselkedésük néhány fontos tekintetben változott a Sales lehetőségeihez képest.

| **Mező** | **Hely** | **Leírás** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- | --- |
| Típus szerint | Általános lap (rejtett) | Ez a értékkészlet mező a következő értékekkel rendelkezik:</br>- Munkaalapú (csak akkor érhető el, ha a Project Operations telepítve van)</br>- Cikkalapú (csak akkor érhető el, ha a Project Operations és a Sales telepítve van)</br>- Szolgáltatáskarbantartás-alapú (elérhető, ha a Field Service telepítve van) | A Project Operations alkalmazás használatakor a program automatikusan **Munkaalapú** értékre állítja a mezőt, amely projektalapúként osztályozza a lehetőséget. Projektalapú lehetőség szükséges ahhoz, hogy az adott üzletre vonatkozóan a későbbi értékesítési folyamatban az összes projektspecifikus kiterjesztés és funkció engedélyezve legyen. |
| Tulajdonos vállalat | Általános lap | Ez az a vállalat vagy jogi személy, amely a projektet az ügyfél számára szállítja. | A program ezt a mezőinformációt a lehetőségből létrehozott projektárajánlat megfelelő mezőjébe másolja. |
| KAPCSOLATTARTÓ | Általános lap | Hivatkozás az ügyfél elsődleges kapcsolattartójára az ügylethez. | |
| Fiók | Általános lap | Hivatkozás az ügyfél vállalati vagy partneri rekordjára. | |
| Partnerkezelő | Általános lap | A projektalapú lehetőség partnerkezelőjének neve. | A partnerkezelő felelős az ügyféllel való kapcsolat kezeléséért a projekt teljesítése során. A partnerkezelőhöz kötött foglalható erőforrásrekord alapján a szerződő részleg az alapértelmezett értéket veszi fel. |
| Szerződő részleg | Általános lap | Az ügylethez kapcsolódó projekt vagy projektek teljesítéséért felelős szervezeti egység. | A szerződő egység a vállalat azon részlege, amely a projekteket az üzlet lezárását követően teljesíti. Minden egyes szerződő egység pénznemmel rendelkezik, és ez a pénznem kerül felhasználásra a projekthez kapcsolódó becsült és ténylegesen felmerült költségek jelentésére. |

A lehetőség **Összegzés** lapjának minden egyéb mezője és szakasza esetében lásd: [Lehetőségek létrehozása és szerkesztése (Sales és Értékesítési központ)](/dynamics365/sales-enterprise/create-edit-opportunity-sales).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
