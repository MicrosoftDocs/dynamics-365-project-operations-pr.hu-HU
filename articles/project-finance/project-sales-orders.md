---
title: Projektre vonatkozó értékesítési rendelések idő és anyag típusú projekteknél
description: Ez a témakör elmagyarázza, hogyan lehet projektalapú értékesítési rendeléseket létrehozni idő és anyag típusú projekteknél.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752180"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projektre vonatkozó értékesítési rendelések idő és anyag típusú projekteknél

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Ez a témakör ismerteti, hogyan hozhat létre egy értékesítési rendelést egy projekthez. Az értékesítési rendelések csak **idő és anyag** típusú projektekhez hozhatók létre.

Ha egy idő és anyagelszámolású projekthez több finanszírozási forrás tartozik a projektszerződésben, engedélyeznie kell az **Értékesítési rendelések engedélyezése több finanszírozási forrású projektekhez** paramétert a **Projektmenedzsment és könyvelési paraméterek** oldalon. 

> [!NOTE]
> - A több finanszírozási forrású projektek értékesítési rendeléseinek támogatása az alkalmazás 10.0.2 és magasabb verziójú kiadásaitól érhető el.
> - A több finanszírozási forrású projektekre vonatkozó értékesítési rendelések támogatásának engedélyezésére szolgáló paraméter a 2020 áprilisi kiadási hullámban kerül eltávolításra, amely után a szolgáltatás mindig engedélyezve lesz.

A projektalapú értékesítési rendelések kétféleképpen hozhatók létre:

- Lépjen magára a projekre. A Művelet panelen válassza a **Kezelés > Cikkfeladatok > Értékesítési rendelés** lehetőséget. A projektadatok alapértelmezés szerint a projektből származó értékesítési rendelésre állnak be. Ha a projektben egynél több finanszírozási forrás van, akkor ki kell választania a finanszírozási forrást az értékesítési rendelés ügyfelének beállításához. Ha a projekthez csak egy finanszírozási forrás tartozik, a rendszer automatikusan beállítja az ügyfelet.
- Nyissa meg az **Összes értékesítési rendelés** listaoldalt, és hozzon létre egy új értékesítési rendelést. Ki kell választania az értékesítési rendelés projektjét. A projekt kiválasztása után az ügyfél a finanszírozási forrásból lesz beállítva, vagy ha a projektszerződés több finanszírozási forrással rendelkezik, akkor ki kell választania a finanszírozási forrást.

