---
title: Költség- és értékesítési árak beállítása a katalógustermékekhez – Lite
description: Ez a cikk arról nyújt tájékoztatást, hogyan állíthatja be a termékkatalógus cikkeinek költség- és értékesítési díjait.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4689d6929e24ebaa992232f809a7ec60908ee517
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917395"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Költség- és értékesítési árak beállítása a katalógustermékekhez – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_


A termékkatalógus-cikkek árképzésének beállítása ugyanolyan a Dynamics 365 Project Operations-ben, mint a Dynamics 365 Sales rendszerben.

A Project Operations programban a termékek nem becsülhetők meg vagy használhatók fel projektekben, így a termékkatalógus árait nem kell beállítani az ajánlatok és szerződések projektárlistáin.

A termékkatalógus árak beállításához használja az ajánlat, szerződés vagy számla lehetőség **Termékár** mezőjét. Ne állítson be termékkatalógus-árakat a projektárlistákban. A projektárlisták kizárólag a Project Operationshoz kapcsolódnak. Az alkalmazásspecifikus üzleti logika az árlistákat egy ajánlatból a szerződésbe másolja. Ennek eredménye a szerződésspecifikus projektárlista. A másolási művelet késleltetheti az árajánlat megnyerésének folyamatát, ha az árajánlaton szereplő projektárlista túl nagy lesz. A termékárlisták nem kerülnek másolásra, ha a szerződéseken egyéni árlistát hoz létre. Mivel nincs szükség másolásra, az ajánlati folyamat teljesítményét ez nem befolyásolja.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]