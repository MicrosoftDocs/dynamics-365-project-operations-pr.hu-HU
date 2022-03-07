---
title: Költség- és értékesítési árak beállítása a katalógustermékekhez – Lite
description: Ez a témakör a költség és értékesítési ráták beállításával kapcsolatban tartalmaz tájékoztatást a termékkatalógus cikkeire vonatkozóan.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bfb28e710c7b6da17d94679a72659f81df7a58e376e4bad94b58c36de781b197
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996034"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Költség- és értékesítési árak beállítása a katalógustermékekhez – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_


A termékkatalógus-cikkek árképzésének beállítása ugyanolyan a Dynamics 365 Project Operations-ben, mint a Dynamics 365 Sales rendszerben.

A Project Operations programban a termékek nem becsülhetők meg vagy használhatók fel projektekben, így a termékkatalógus árait nem kell beállítani az ajánlatok és szerződések projektárlistáin.

A termékkatalógus árak beállításához használja az ajánlat, szerződés vagy számla lehetőség **Termékár** mezőjét. Ne állítson be termékkatalógus-árakat a projektárlistákban. A projektárlisták kizárólag a Project Operationshoz kapcsolódnak. Az alkalmazásspecifikus üzleti logika az árlistákat egy ajánlatból a szerződésbe másolja. Ennek eredménye a szerződésspecifikus projektárlista. A másolási művelet késleltetheti az árajánlat megnyerésének folyamatát, ha az árajánlaton szereplő projektárlista túl nagy lesz. A termékárlisták nem kerülnek másolásra, ha a szerződéseken egyéni árlistát hoz létre. Mivel nincs szükség másolásra, az ajánlati folyamat teljesítményét ez nem befolyásolja.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]