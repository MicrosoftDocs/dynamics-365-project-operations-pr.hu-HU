---
title: Költség- és értékesítési árak beállítása a katalógustermékekhez
description: Ez a témakör a költség és értékesítési ráták beállításával kapcsolatban tartalmaz tájékoztatást a termékkatalógus cikkeire vonatkozóan.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078159"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Költség- és értékesítési árak beállítása a katalógustermékekhez

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_


A termékkatalógusban szereplő termékek árazásának beállítása a Dynamics 365 Project Operationsban ugyanaz, mint a Dynamics 365 Salesben.

Mivel a termékek nem becsülhető meg, illetve nem használhatók fel a Project Operations projektjeinél, nem kell megadnia a termékkatalógus árát az ajánlatokhoz és a szerződésekhez tartozó projektárlisták esetében.

A termékkatalógus árát be kell állítani az ajánlat, a szerződés vagy a partner **termék ára** mezőjében. Ne állítson be Termékkatalógus-árakat az ilyen entitások projektárlistáiban. A projektárlisták kizárólag a Project Operationshoz kapcsolódnak. Van alkalmazásspecifikus üzleti logika, amely az árajánlatokból a szerződésbe másolja az árlisták listáját. Ennek eredménye a szerződésspecifikus projektárlista. A másolási művelet késleltetheti az árajánlat megnyerésének folyamatát, ha az árajánlaton szereplő projektárlista túl nagy lesz. A termékárlisták nem kerülnek másolásra, ha a szerződéseken egyéni árlistát hoz létre. Ez azt jelenti, hogy a termékárlisták nem befolyásolják az árajánlat megnyerési folyamat teljesítményét.
