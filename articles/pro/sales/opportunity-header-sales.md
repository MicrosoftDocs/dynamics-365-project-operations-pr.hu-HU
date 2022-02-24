---
title: Lehetőség beállításai - Lite
description: Ez a témakör a projektalapú ajánlatokról és a projektalapú lehetőségsorokról nyújt tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6631e136572b958ca616d708a5e3c3c2d9f2675c
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663822"
---
# <a name="header-details-for-project-opportunities"></a>Fejlécadatok projektlehetőségek esetében

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Lehetőség fejléc a projektalapú ügylet összes olyan adatát rögzíti, amely a projektalapú lehetőség összes sorára vonatkozik.

A projektalapú lehetőségek a Dynamics 365 Project Operations rendszerben a Dynamics 365 Sales lehetőségek bővítményei. Ezek a bővítmények további funkciókat biztosítanak, amelyek a projektalapú lehetőségekre jellemzőek és szükségesek. Ezek a bővítmények tartalmazhatnak új mezőket és menüszalag-műveleteket, amelyek a projektalapú lehetőségekben érhetők el. Előfordulhat, hogy a Sales alkalmazásban elérhető egyes mezők, funkciók és alapértelmezett logika nem érhető el a Project Operations programban.

Az alábbi táblázat egy projektalapú lehetőség azon mezőit tartalmazza, amelyek vagy egyediek a Project Operationsben, vagy viselkedésük néhány fontos tekintetben változott a Sales lehetőségeihez képest.

| **Mező** | **Hely** | **Leírás** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- | --- |
| Típus szerint | Általános lap (rejtett) | Ez a értékkészlet mező a következő értékekkel rendelkezik:</br>- Munkaalapú (csak akkor érhető el, ha a Project Operations telepítve van)</br>- Cikkalapú (csak akkor érhető el, ha a Project Operations és a Sales telepítve van)</br>- Szolgáltatáskarbantartás-alapú (elérhető, ha a Field Service telepítve van) | A Project Operations alkalmazás használatakor a program automatikusan **Munkaalapú** értékre állítja a mezőt, amely projektalapúként osztályozza a lehetőséget. Projektalapú lehetőség szükséges ahhoz, hogy az adott üzletre vonatkozóan a későbbi értékesítési folyamatban az összes projektspecifikus kiterjesztés és funkció engedélyezve legyen. |
| KAPCSOLATTARTÓ | Általános lap | Hivatkozás az ügyfél elsődleges kapcsolattartójára az ügylethez. | |
| Fiók | Általános lap | Hivatkozás az ügyfél vállalati vagy partneri rekordjára. | |
| Partnerkezelő | Általános lap | A projektalapú lehetőség partnerkezelőjének neve. | A partnerkezelő felelős az ügyféllel való kapcsolat kezeléséért a projekt teljesítése során. A partnerkezelőhöz kötött foglalható erőforrásrekord alapján a szerződő részleg az alapértelmezett értéket veszi fel. |
| Szerződő részleg | Általános lap | Az ügylethez kapcsolódó projekt vagy projektek teljesítéséért felelős szervezeti egység. | A szerződő egység a vállalat azon részlege, amely a projekteket az üzlet lezárását követően teljesíti. Minden egyes szerződő egység pénznemmel rendelkezik, és ez a pénznem kerül felhasználásra a projekthez kapcsolódó becsült és ténylegesen felmerült költségek jelentésére. |

A lehetőség **Összegzés** lapjának minden egyéb mezője és szakasza esetében lásd: [Lehetőségek létrehozása és szerkesztése (Sales és Értékesítési központ)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
