---
title: Egyéni mezők és entitások létrehozása
description: A témakör ismerteti, hogyan hozhatók létre értékkészlet-halmazok és entitások saját megoldásban a Power Apps platformon.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752291"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="28152-103">Egyéni mezők és entitások létrehozása</span><span class="sxs-lookup"><span data-stu-id="28152-103">Create custom fields and entities</span></span> 

<span data-ttu-id="28152-104">Hajtsa végre az alábbi lépéseket minden olyan alkalommal, amikor egyéni értékkészletet vagy entitást szeretne létrehozni a Power Apps platformon.</span><span class="sxs-lookup"><span data-stu-id="28152-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="28152-105">A témakör eljárásait a Project Service Automation (PSA) webfelületének használatával kell elvégezni.</span><span class="sxs-lookup"><span data-stu-id="28152-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28152-106">Javasoljuk, hogy minden egyéni árképzési dimenziót külön megoldásban hajtson végre.</span><span class="sxs-lookup"><span data-stu-id="28152-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="28152-107">Ez a fontos gyakorlati tanács rugalmasságot biztosít a jövőben a változtatások frissítéséhez vagy eltávolításához szükség szerint, segítséget nyújt munkájának újbóli felhasználásában, és megkönnyíti a módosítások másik példányra való átvitelét.</span><span class="sxs-lookup"><span data-stu-id="28152-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="28152-108">Miután elvégezte az összes szükséges módosítást, exportálja a megoldást **Felügyelt megoldásként**, majd importálja azt más példányokra az árképzési beállítások újbóli felhasználása céljából.</span><span class="sxs-lookup"><span data-stu-id="28152-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="28152-109">Egyéni megoldás létrehozása árképzési dimenziókra</span><span class="sxs-lookup"><span data-stu-id="28152-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="28152-110">A PSA-ban kattintson a **Beállítások** > **Megoldások** lehetőségre, majd az **Új** lehetőségre új megoldás létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="28152-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="28152-111">Nevezze el a megoldást, **\<a szervezet neve> árképzési dimenziók**, írja be a további szükséges információkat, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="28152-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Egyéni megoldás létrehozása árképzési dimenziókra](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="28152-113">Egyéni mezők és értékkészletek létrehozása az árképzési dimenzió megoldásban</span><span class="sxs-lookup"><span data-stu-id="28152-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="28152-114">Az árképzési dimenzió lehet értékkészlet vagy entitás.</span><span class="sxs-lookup"><span data-stu-id="28152-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="28152-115">Mindkettőt létre kell hozni az árképzési megoldásban.</span><span class="sxs-lookup"><span data-stu-id="28152-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="28152-116">Az eljárás lépései ismertetik az entitás alapú dimenziók és az értékkészlet-alapú dimenziók létrehozását.</span><span class="sxs-lookup"><span data-stu-id="28152-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="28152-117">Entitásalapú dimenziók</span><span class="sxs-lookup"><span data-stu-id="28152-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="28152-118">A PSA-ban kattintson a **Beállítások** > **Megoldások** elemre, majd kattintson duplán a **\<szervezet neve> árazási dimenziók** elemre.</span><span class="sxs-lookup"><span data-stu-id="28152-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="28152-119">A Solution Explorerben a bal oldali navigációs panelen válassza az **Entitások** elemet.</span><span class="sxs-lookup"><span data-stu-id="28152-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="28152-120">Kattintson az **Új** elemre, és hozzon létre egy új entitást, melynek neve: **Standard cím**.</span><span class="sxs-lookup"><span data-stu-id="28152-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="28152-121">Írja be a további szükséges információkat, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="28152-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![A standard című entitás meghatározása](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="28152-123">Értékkészlet-alapú dimenziók</span><span class="sxs-lookup"><span data-stu-id="28152-123">Option set-based dimensions</span></span> 
<span data-ttu-id="28152-124">Két értékkészlet-alapú dimenziót hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="28152-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="28152-125">Használja az **Erőforrás munkahelye** elemet az **Otthon** végzett munka és a **Helyszíni** munka árának nyomon követéséhez, és használja az **Erőforrás munkaideje** elemet a **Rendszeres** és a **Túlóra** értékekkel, hogy jelöléssel láthassa el az elkészült munkát.</span><span class="sxs-lookup"><span data-stu-id="28152-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="28152-126">A PSA-ban kattintson a **Beállítások** > **Megoldások** elemre, majd kattintson duplán a **\<szervezet neve> árképzési dimenziók** elemre.</span><span class="sxs-lookup"><span data-stu-id="28152-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="28152-127">A Solution Explorerben a bal oldali navigációs panelen válassza az **Értékkészletek** elemet.</span><span class="sxs-lookup"><span data-stu-id="28152-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="28152-128">Új értékkészlet létrehozásához kattintson az **Új** elemre, majd írja be a további szükséges információkat, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="28152-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="28152-129">Erőforrás munkahelye nevű értékkészlet-alapú árképzési dimenzió</span><span class="sxs-lookup"><span data-stu-id="28152-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="28152-130">Erőforrás munkaideje nevű értékkészlet-alapú árképzési dimenzió</span><span class="sxs-lookup"><span data-stu-id="28152-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="28152-131">Adatok létrehozása entitásalapú dimenziókhoz</span><span class="sxs-lookup"><span data-stu-id="28152-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="28152-132">Entitásalapú dimenziókhoz manuálisan vagy Microsoft Excel importálással vagy szolgáltatáshívások használatával hozhat létre adatokat.</span><span class="sxs-lookup"><span data-stu-id="28152-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="28152-133">Az eljárás lépéseinek követésévek hozhat létre két szabványos címet: a **Szabványos cím** entitásalapú dimenzióból származó **Rendszermérnök** és **Vezető rendszermérnök**.</span><span class="sxs-lookup"><span data-stu-id="28152-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="28152-134">Ha a létrehozni kívánt adat kis méretű, a következő példához hasonlóan használhat szabványos űrlapot.</span><span class="sxs-lookup"><span data-stu-id="28152-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="28152-135">A PSA-ban kattintson a **Speciális keresés** elemre.</span><span class="sxs-lookup"><span data-stu-id="28152-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="28152-136">Válassza ki a **Szabványos cím** entitást, majd kattintson az **Eredmények** elemre.</span><span class="sxs-lookup"><span data-stu-id="28152-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="28152-137">A **Szabványos cím** összes sora megjelenik.</span><span class="sxs-lookup"><span data-stu-id="28152-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="28152-138">Kattintson az **Új** elemre.</span><span class="sxs-lookup"><span data-stu-id="28152-138">Click **New**.</span></span> <span data-ttu-id="28152-139">A **Név** mezőbe írja be a „Rendszermérnök” elemet, majd kattintson a **Mentés** elemre.</span><span class="sxs-lookup"><span data-stu-id="28152-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="28152-140">Zárja be az űrlapot.</span><span class="sxs-lookup"><span data-stu-id="28152-140">Close the form.</span></span> 
4. <span data-ttu-id="28152-141">Ismételje meg az 1–3. lépést egy újabb szabványos cím létrehozásához a „Vezető rendszermérnök” esetében.</span><span class="sxs-lookup"><span data-stu-id="28152-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="28152-142">Mintaadatok a szabványos cím entitáshoz</span><span class="sxs-lookup"><span data-stu-id="28152-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="28152-143">Adja hozzá az összes szükséges PSA-entitást és kapcsolódó komponenseket az árképzési dimenzió megoldáshoz.</span><span class="sxs-lookup"><span data-stu-id="28152-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="28152-144">A következő Project Service entitásokat kell hozzáadnia az árképzési megoldáshoz.</span><span class="sxs-lookup"><span data-stu-id="28152-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="28152-145">Az eljárás lépéseit követve végezzen el néhány fontos sémaváltoztatást az árképzési megoldásban, hogy az entitások megismerjék az új árképzési dimenziókat.</span><span class="sxs-lookup"><span data-stu-id="28152-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="28152-146">A PSA-ban kattintson a **Beállítások** > **Megoldások** elemre, majd kattintson duplán a **\<szervezet neve> árazási dimenziók** elemre.</span><span class="sxs-lookup"><span data-stu-id="28152-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="28152-147">A Solution Explorerben a bal oldali navigációs panelen válassza a **Meglévő hozzáadása** > **Entitások** elemet.</span><span class="sxs-lookup"><span data-stu-id="28152-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="28152-148">A **Megoldás összetevői** párbeszédpanelen válassza ki a következő entitásokat:</span><span class="sxs-lookup"><span data-stu-id="28152-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="28152-149">Tény</span><span class="sxs-lookup"><span data-stu-id="28152-149">Actual</span></span>
- <span data-ttu-id="28152-150">Lefoglalható erőforrás</span><span class="sxs-lookup"><span data-stu-id="28152-150">Bookable Resource</span></span>
- <span data-ttu-id="28152-151">Becsléssor</span><span class="sxs-lookup"><span data-stu-id="28152-151">Estimate Line</span></span>
- <span data-ttu-id="28152-152">Számlasor részletei</span><span class="sxs-lookup"><span data-stu-id="28152-152">Invoice Line Detail</span></span>
- <span data-ttu-id="28152-153">Naplósor</span><span class="sxs-lookup"><span data-stu-id="28152-153">Journal Line</span></span>
- <span data-ttu-id="28152-154">Projektszerződés sorának részletei</span><span class="sxs-lookup"><span data-stu-id="28152-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="28152-155">Projektcsoporttag</span><span class="sxs-lookup"><span data-stu-id="28152-155">Project Team Member</span></span>
- <span data-ttu-id="28152-156">Árajánlatsor részletei</span><span class="sxs-lookup"><span data-stu-id="28152-156">Quote Line Detail</span></span>
- <span data-ttu-id="28152-157">Szerepkörárrés</span><span class="sxs-lookup"><span data-stu-id="28152-157">Role Price Markup</span></span>
- <span data-ttu-id="28152-158">Szerepkörár</span><span class="sxs-lookup"><span data-stu-id="28152-158">Role Price</span></span> 
- <span data-ttu-id="28152-159">Időbejegyzés</span><span class="sxs-lookup"><span data-stu-id="28152-159">Time Entry</span></span> 

> ![Adjon hozzá meglévő elemeket az árképzési dimenzió megoldáshoz](media/Existing-entities-to-PD-solution.png)

> ![Megoldás-összetevők kiválasztása](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="28152-162">Ügyeljen arra, hogy minden kiválasztott entitás tartalmazzon minden űrlapot és nézetet.</span><span class="sxs-lookup"><span data-stu-id="28152-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="28152-163">Amikor a rendszer felkéri függő entitásának felvételére a fentebb kiválasztott entitásokhoz, kattintson a **Nem** elemre.</span><span class="sxs-lookup"><span data-stu-id="28152-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Ne adja hozzá az összes kapcsolódó komponenst](media/Do-not-include-required.png)


