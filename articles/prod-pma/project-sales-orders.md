---
title: Projektre vonatkozó értékesítési rendelések idő és anyag típusú projekteknél
description: Ez a témakör elmagyarázza, hogyan lehet projektalapú értékesítési rendeléseket létrehozni idő és anyag típusú projekteknél.
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 74a90ea0bdb8f760273c0f6b1c61bffcb70b6c8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289057"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="ea0c3-103">Projektre vonatkozó értékesítési rendelések idő és anyag típusú projekteknél</span><span class="sxs-lookup"><span data-stu-id="ea0c3-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ea0c3-104">Ez a témakör ismerteti, hogyan hozhat létre egy értékesítési rendelést egy projekthez.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="ea0c3-105">Az értékesítési rendelések csak **idő és anyag** típusú projektekhez hozhatók létre.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="ea0c3-106">Ha egy idő és anyagelszámolású projekthez több finanszírozási forrás tartozik a projektszerződésben, engedélyeznie kell az **Értékesítési rendelések engedélyezése több finanszírozási forrású projektekhez** paramétert a **Projektmenedzsment és könyvelési paraméterek** oldalon.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="ea0c3-107">A több finanszírozási forrású projektek értékesítési rendeléseinek támogatása az alkalmazás 10.0.2 és magasabb verziójú kiadásaitól érhető el.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="ea0c3-108">A több finanszírozási forrású projektekre vonatkozó értékesítési rendelések támogatásának engedélyezésére szolgáló paraméter a 2020 áprilisi kiadási hullámban kerül eltávolításra, amely után a szolgáltatás mindig engedélyezve lesz.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="ea0c3-109">A projektalapú értékesítési rendelések kétféleképpen hozhatók létre:</span><span class="sxs-lookup"><span data-stu-id="ea0c3-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="ea0c3-110">Lépjen magára a projekre.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-110">Go to the project itself.</span></span> <span data-ttu-id="ea0c3-111">A Művelet panelen válassza a **Kezelés > Cikkfeladatok > Értékesítési rendelés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="ea0c3-112">A projektadatok alapértelmezés szerint a projektből származó értékesítési rendelésre állnak be.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="ea0c3-113">Ha a projektben egynél több finanszírozási forrás van, akkor ki kell választania a finanszírozási forrást az értékesítési rendelés ügyfelének beállításához.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="ea0c3-114">Ha a projekthez csak egy finanszírozási forrás tartozik, a rendszer automatikusan beállítja az ügyfelet.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="ea0c3-115">Nyissa meg az **Összes értékesítési rendelés** listaoldalt, és hozzon létre egy új értékesítési rendelést.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="ea0c3-116">Ki kell választania az értékesítési rendelés projektjét.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="ea0c3-117">A projekt kiválasztása után az ügyfél a finanszírozási forrásból lesz beállítva, vagy ha a projektszerződés több finanszírozási forrással rendelkezik, akkor ki kell választania a finanszírozási forrást.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]