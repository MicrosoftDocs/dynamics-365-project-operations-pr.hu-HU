---
title: Költség- és értékesítési árak beállítása a katalógustermékekhez – Lite
description: Ez a témakör a költség és értékesítési ráták beállításával kapcsolatban tartalmaz tájékoztatást a termékkatalógus cikkeire vonatkozóan.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 12e09d99e9832c93c3aea34ec0d4488cdf6b02fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576825"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Költség- és értékesítési árak beállítása a katalógustermékekhez – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_


A termékkatalógus-cikkek árképzésének beállítása ugyanolyan a Dynamics 365 Project Operations-ben, mint a Dynamics 365 Sales rendszerben.

A Project Operations programban a termékek nem becsülhetők meg vagy használhatók fel projektekben, így a termékkatalógus árait nem kell beállítani az ajánlatok és szerződések projektárlistáin.

A termékkatalógus árak beállításához használja az ajánlat, szerződés vagy számla lehetőség **Termékár** mezőjét. Ne állítson be termékkatalógus-árakat a projektárlistákban. A projektárlisták kizárólag a Project Operationshoz kapcsolódnak. Az alkalmazásspecifikus üzleti logika az árlistákat egy ajánlatból a szerződésbe másolja. Ennek eredménye a szerződésspecifikus projektárlista. A másolási művelet késleltetheti az árajánlat megnyerésének folyamatát, ha az árajánlaton szereplő projektárlista túl nagy lesz. A termékárlisták nem kerülnek másolásra, ha a szerződéseken egyéni árlistát hoz létre. Mivel nincs szükség másolásra, az ajánlati folyamat teljesítményét ez nem befolyásolja.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]