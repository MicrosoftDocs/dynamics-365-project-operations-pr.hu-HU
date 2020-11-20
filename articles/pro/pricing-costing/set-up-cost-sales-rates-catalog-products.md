---
title: Költség- és értékesítési árak beállítása a katalógustermékekhez – Lite
description: Ez a témakör a költség és értékesítési ráták beállításával kapcsolatban tartalmaz tájékoztatást a termékkatalógus cikkeire vonatkozóan.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176704"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Költség- és értékesítési árak beállítása a katalógustermékekhez – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_


A termékkatalógusban szereplő termékek árazásának beállítása a Dynamics 365 Project Operationsban ugyanaz, mint a Dynamics 365 Salesben.

Mivel a termékek nem becsülhető meg, illetve nem használhatók fel a Project Operations projektjeinél, nem kell megadnia a termékkatalógus árát az ajánlatokhoz és a szerződésekhez tartozó projektárlisták esetében.

A termékkatalógus árát be kell állítani az ajánlat, a szerződés vagy a partner **termék ára** mezőjében. Ne állítson be Termékkatalógus-árakat az ilyen entitások projektárlistáiban. A projektárlisták kizárólag a Project Operationshoz kapcsolódnak. Van alkalmazásspecifikus üzleti logika, amely az árajánlatokból a szerződésbe másolja az árlisták listáját. Ennek eredménye a szerződésspecifikus projektárlista. A másolási művelet késleltetheti az árajánlat megnyerésének folyamatát, ha az árajánlaton szereplő projektárlista túl nagy lesz. A termékárlisták nem kerülnek másolásra, ha a szerződéseken egyéni árlistát hoz létre. Ez azt jelenti, hogy a termékárlisták nem befolyásolják az árajánlat megnyerési folyamat teljesítményét.
