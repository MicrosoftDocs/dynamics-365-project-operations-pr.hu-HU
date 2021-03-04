---
title: Egyéni mezők és entitások létrehozása
description: A témakör ismerteti, hogyan hozhatók létre értékkészlet-halmazok és entitások saját megoldásban a Power Apps platformon.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: b9e32c8871a8986ba827f742baf4e4d5cd9dd235
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144866"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="b8a75-103">Egyéni mezők és entitások létrehozása</span><span class="sxs-lookup"><span data-stu-id="b8a75-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b8a75-104">Hajtsa végre az alábbi lépéseket minden olyan alkalommal, amikor egyéni értékkészletet vagy entitást szeretne létrehozni a Power Apps platformon.</span><span class="sxs-lookup"><span data-stu-id="b8a75-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="b8a75-105">A témakör eljárásait a Project Service Automation (PSA) webfelületének használatával kell elvégezni.</span><span class="sxs-lookup"><span data-stu-id="b8a75-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8a75-106">Javasoljuk, hogy minden egyéni árképzési dimenziót külön megoldásban hajtson végre.</span><span class="sxs-lookup"><span data-stu-id="b8a75-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="b8a75-107">Ez a fontos gyakorlati tanács rugalmasságot biztosít a jövőben a változtatások frissítéséhez vagy eltávolításához szükség szerint, segítséget nyújt munkájának újbóli felhasználásában, és megkönnyíti a módosítások másik példányra való átvitelét.</span><span class="sxs-lookup"><span data-stu-id="b8a75-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="b8a75-108">Miután elvégezte az összes szükséges módosítást, exportálja a megoldást **Felügyelt megoldásként**, majd importálja azt más példányokra az árképzési beállítások újbóli felhasználása céljából.</span><span class="sxs-lookup"><span data-stu-id="b8a75-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="b8a75-109">Egyéni mezők és értékkészletek létrehozása az árképzési dimenzió megoldásban</span><span class="sxs-lookup"><span data-stu-id="b8a75-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="b8a75-110">Az árképzési dimenzió lehet értékkészlet vagy entitás.</span><span class="sxs-lookup"><span data-stu-id="b8a75-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="b8a75-111">Mindkettőt létre kell hozni az árképzési megoldásban.</span><span class="sxs-lookup"><span data-stu-id="b8a75-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="b8a75-112">Az eljárás lépései ismertetik az entitás alapú dimenziók és az értékkészlet-alapú dimenziók létrehozását.</span><span class="sxs-lookup"><span data-stu-id="b8a75-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="b8a75-113">Entitásalapú dimenziók</span><span class="sxs-lookup"><span data-stu-id="b8a75-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="b8a75-114">A PSA-ban válassza ki a **Beállítások** > **Megoldások** lehetőséget, és kattintson duplán a(z) **\<your organization name> árazási dimenzióira**.</span><span class="sxs-lookup"><span data-stu-id="b8a75-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="b8a75-115">A Solution Explorerben a bal oldali navigációs panelen válassza az **Entitások** elemet.</span><span class="sxs-lookup"><span data-stu-id="b8a75-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="b8a75-116">Kattintson az **Új** elemre, és hozzon létre egy új entitást, melynek neve: **Standard cím**.</span><span class="sxs-lookup"><span data-stu-id="b8a75-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="b8a75-117">Írja be a további szükséges információkat, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="b8a75-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![A standard című entitás meghatározása](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="b8a75-119">Értékkészlet-alapú dimenziók</span><span class="sxs-lookup"><span data-stu-id="b8a75-119">Option set-based dimensions</span></span> 
<span data-ttu-id="b8a75-120">Két értékkészlet-alapú dimenziót hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="b8a75-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="b8a75-121">Használja az **Erőforrás munkahelye** elemet az **Otthon** végzett munka és a **Helyszíni** munka árának nyomon követéséhez, és használja az **Erőforrás munkaideje** elemet a **Rendszeres** és a **Túlóra** értékekkel, hogy jelöléssel láthassa el az elkészült munkát.</span><span class="sxs-lookup"><span data-stu-id="b8a75-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="b8a75-122">A PSA-ban válassza a **Beállítások** > **Megoldások** lehetőséget, és kattintson duplán a(z) **\<your organization name> árazási dimenzióira**.</span><span class="sxs-lookup"><span data-stu-id="b8a75-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="b8a75-123">A Solution Explorerben a bal oldali navigációs panelen válassza az **Értékkészletek** elemet.</span><span class="sxs-lookup"><span data-stu-id="b8a75-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="b8a75-124">Új értékkészlet létrehozásához kattintson az **Új** elemre, majd írja be a további szükséges információkat, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="b8a75-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="b8a75-125">Erőforrás munkahelye nevű értékkészlet-alapú árképzési dimenzió</span><span class="sxs-lookup"><span data-stu-id="b8a75-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="b8a75-126">Erőforrás munkaideje nevű értékkészlet-alapú árképzési dimenzió</span><span class="sxs-lookup"><span data-stu-id="b8a75-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="b8a75-127">Adatok létrehozása entitásalapú dimenziókhoz</span><span class="sxs-lookup"><span data-stu-id="b8a75-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="b8a75-128">Entitásalapú dimenziókhoz manuálisan vagy Microsoft Excel importálással vagy szolgáltatáshívások használatával hozhat létre adatokat.</span><span class="sxs-lookup"><span data-stu-id="b8a75-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="b8a75-129">Az eljárás lépéseinek követésévek hozhat létre két szabványos címet: a **Szabványos cím** entitásalapú dimenzióból származó **Rendszermérnök** és **Vezető rendszermérnök**.</span><span class="sxs-lookup"><span data-stu-id="b8a75-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="b8a75-130">Ha a létrehozni kívánt adat kis méretű, a következő példához hasonlóan használhat szabványos űrlapot.</span><span class="sxs-lookup"><span data-stu-id="b8a75-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="b8a75-131">A PSA-ban kattintson a **Speciális keresés** elemre.</span><span class="sxs-lookup"><span data-stu-id="b8a75-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="b8a75-132">Válassza ki a **Szabványos cím** entitást, majd kattintson az **Eredmények** elemre.</span><span class="sxs-lookup"><span data-stu-id="b8a75-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="b8a75-133">A **Szabványos cím** összes sora megjelenik.</span><span class="sxs-lookup"><span data-stu-id="b8a75-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="b8a75-134">Kattintson az **Új** elemre.</span><span class="sxs-lookup"><span data-stu-id="b8a75-134">Click **New**.</span></span> <span data-ttu-id="b8a75-135">A **Név** mezőbe írja be a „Rendszermérnök” elemet, majd kattintson a **Mentés** elemre.</span><span class="sxs-lookup"><span data-stu-id="b8a75-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="b8a75-136">Zárja be az űrlapot.</span><span class="sxs-lookup"><span data-stu-id="b8a75-136">Close the form.</span></span> 
4. <span data-ttu-id="b8a75-137">Ismételje meg az 1–3. lépést egy újabb szabványos cím létrehozásához a „Vezető rendszermérnök” esetében.</span><span class="sxs-lookup"><span data-stu-id="b8a75-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="b8a75-138">Mintaadatok a szabványos cím entitáshoz</span><span class="sxs-lookup"><span data-stu-id="b8a75-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)


