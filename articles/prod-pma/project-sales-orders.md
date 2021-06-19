---
title: Projektre vonatkozó értékesítési rendelések idő és anyag típusú projekteknél
description: Ez a témakör elmagyarázza, hogyan lehet projektalapú értékesítési rendeléseket létrehozni idő és anyag típusú projekteknél.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: dec9bc700d18f71ec7c9e976b38cb8cbb41f21b5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009664"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projektre vonatkozó értékesítési rendelések idő és anyag típusú projekteknél

[!include[banner](../includes/banner.md)]

Ez a témakör ismerteti, hogyan hozhat létre egy értékesítési rendelést egy projekthez. Az értékesítési rendelések csak **idő és anyag** típusú projektekhez hozhatók létre.

Ha egy idő és anyagelszámolású projekthez több finanszírozási forrás tartozik a projektszerződésben, engedélyeznie kell az **Értékesítési rendelések engedélyezése több finanszírozási forrású projektekhez** paramétert a **Projektmenedzsment és könyvelési paraméterek** oldalon. 

> [!NOTE]
> - A több finanszírozási forrású projektek értékesítési rendeléseinek támogatása az alkalmazás 10.0.2 és magasabb verziójú kiadásaitól érhető el.
> - A több finanszírozási forrású projektekre vonatkozó értékesítési rendelések támogatásának engedélyezésére szolgáló paraméter a 2020 áprilisi kiadási hullámban kerül eltávolításra, amely után a szolgáltatás mindig engedélyezve lesz.

A projektalapú értékesítési rendelések kétféleképpen hozhatók létre:

- Lépjen magára a projekre. A Művelet panelen válassza a **Kezelés > Cikkfeladatok > Értékesítési rendelés** lehetőséget. A projektadatok alapértelmezés szerint a projektből származó értékesítési rendelésre állnak be. Ha a projektben egynél több finanszírozási forrás van, akkor ki kell választania a finanszírozási forrást az értékesítési rendelés ügyfelének beállításához. Ha a projekthez csak egy finanszírozási forrás tartozik, a rendszer automatikusan beállítja az ügyfelet.
- Nyissa meg az **Összes értékesítési rendelés** listaoldalt, és hozzon létre egy új értékesítési rendelést. Ki kell választania az értékesítési rendelés projektjét. A projekt kiválasztása után az ügyfél a finanszírozási forrásból lesz beállítva, vagy ha a projektszerződés több finanszírozási forrással rendelkezik, akkor ki kell választania a finanszírozási forrást.



[!INCLUDE[footer-include](../includes/footer-banner.md)]