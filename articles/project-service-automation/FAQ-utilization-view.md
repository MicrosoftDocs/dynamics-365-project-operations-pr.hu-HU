---
title: Az erőforrások számlázható kihasználtságának megtekintése
description: Ez a témakör információkat nyújt az erőforrás-kihasználtsági nézetről.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Applies to all versions of Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: 656511ac-6851-42d6-abd4-0c7e77ea5d9c
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8953015ced24ff10f0bec2570a840cf4e130b01a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752174"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="77d59-103">Az erőforrások számlázható kihasználtságának megtekintése</span><span class="sxs-lookup"><span data-stu-id="77d59-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="77d59-104">A **Project Service Erőforrás-kihasználtság** oldal **Kihasználtsági nézete** az egyes foglalható erőforrások számlázható kihasználtságát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="77d59-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="77d59-105">Mivel a nézet az ütemezési táblán alapul, így számos funkció azonos.</span><span class="sxs-lookup"><span data-stu-id="77d59-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Képernyőkép: Erőforrás-kihasználtság nézet](media/FAQ-utilization-1.png)
 

<span data-ttu-id="77d59-107">A számlázható kihasználtság számítása a következőképpen történik:</span><span class="sxs-lookup"><span data-stu-id="77d59-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="77d59-108">Számlázható kihasználtság = (számlázható tényleges óra)/(erőforrás kapacitása)</span><span class="sxs-lookup"><span data-stu-id="77d59-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="77d59-109">A cellák a kiválasztott időszakra (nap, hét vagy hónap) számított számlázható kihasználtságot jelentik.</span><span class="sxs-lookup"><span data-stu-id="77d59-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="77d59-110">A színek minden cella esetében az erőforrás számlázható kihasználtságát jelenítik meg a cél számlázható kihasználtsághoz képest.</span><span class="sxs-lookup"><span data-stu-id="77d59-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="77d59-111">A cél kihasználtság az erőforrás alapértelmezett szerepkörén vagy az egyes erőforrásokon állítható be.</span><span class="sxs-lookup"><span data-stu-id="77d59-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="77d59-112">A számítás először az adott személynél keresi a célt, majd az erőforrás alapértelmezett szerepkörén.</span><span class="sxs-lookup"><span data-stu-id="77d59-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="77d59-113">Állítson be célt egy erőforráson</span><span class="sxs-lookup"><span data-stu-id="77d59-113">Set target on a resource</span></span>

1. <span data-ttu-id="77d59-114">Lépjen a **Források** \> **Források** oldalra.</span><span class="sxs-lookup"><span data-stu-id="77d59-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="77d59-115">Válasszon egy erőforrást a rekord megnyitásához.</span><span class="sxs-lookup"><span data-stu-id="77d59-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="77d59-116">A **Project Service** lapon beállíthatja az erőforrás cél kihasználtságát.</span><span class="sxs-lookup"><span data-stu-id="77d59-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![A Project Service lapjának használata a cél kihasználtság megadásához – képernyőkép](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="77d59-118">Állítsa be a cél kihasználtságot egy szerepkörön</span><span class="sxs-lookup"><span data-stu-id="77d59-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="77d59-119">Lépjen az **Erőforrások** \> **Erőforrás-szerepkörök** oldalra.</span><span class="sxs-lookup"><span data-stu-id="77d59-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="77d59-120">Válasszon ki egy szerepkört, és nyissa meg a rekordot.</span><span class="sxs-lookup"><span data-stu-id="77d59-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="77d59-121">A cél kihasználtság beállítása a szerepkörhöz.</span><span class="sxs-lookup"><span data-stu-id="77d59-121">Set the target utilization for the role.</span></span>

> ![Az Erőforrás-szerepkörök használata a cél kihasználtság megadásához – képernyőkép](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="77d59-123">Számítsa ki az erőforrás számlázható kihasználtságát.</span><span class="sxs-lookup"><span data-stu-id="77d59-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="77d59-124">Az erőforrás számlázható kihasználtságának kiszámításához el kell végeznie a szükséges konfigurációs lépéseket.</span><span class="sxs-lookup"><span data-stu-id="77d59-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="77d59-125">Állítsa be az alapértelmezett szerepet az egyes erőforrásokhoz</span><span class="sxs-lookup"><span data-stu-id="77d59-125">Set default role for individual resource</span></span>

<span data-ttu-id="77d59-126">Elsőként a cél kihasználtságot kell beállítani az egyes erőforrásokon vagy erőforrás-szerepkörökön.</span><span class="sxs-lookup"><span data-stu-id="77d59-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="77d59-127">Ha erőforrás-szerepköröket használ a célokhoz, minden egyes erőforrásnak egy alapértelmezett szerepkörrel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="77d59-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="77d59-128">Ennek beállításához lépjen az **Erőforrások** \> **Erőforrások** oldalra.</span><span class="sxs-lookup"><span data-stu-id="77d59-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="77d59-129">Válasszon ki egy erőforrást, nyissa meg a rekordot, majd válassza ki a **Project Service** fület.</span><span class="sxs-lookup"><span data-stu-id="77d59-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="77d59-130">Az **Erőforrás-szerepkör** rácsban ellenőrizze, hogy egy szerep tartozik az erőforráshoz, és az **Alapértelmezett** beállítás **Igen** értékű-e.</span><span class="sxs-lookup"><span data-stu-id="77d59-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="77d59-131">Módosítsa az erőforrás-szerepkör számlázási típusát.</span><span class="sxs-lookup"><span data-stu-id="77d59-131">Change billing type for resource role</span></span>

<span data-ttu-id="77d59-132">Az erőforrás-szerepköröket úgy kell beállítani, hogy a számlázási típus **Számlázható** legyen.</span><span class="sxs-lookup"><span data-stu-id="77d59-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="77d59-133">Lépjen az **Erőforrások** \> **Erőforrás-szerepkörök** oldalra.</span><span class="sxs-lookup"><span data-stu-id="77d59-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="77d59-134">Nyissa meg a frissíteni kívánt rekordot, majd állítsa be a számlázási típus alapértelmezett állapotát **Számlázható** értékre.</span><span class="sxs-lookup"><span data-stu-id="77d59-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="77d59-135">Állítsa be a munkaórákat az erőforrás-szerepkörhöz</span><span class="sxs-lookup"><span data-stu-id="77d59-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="77d59-136">Az erőforrásnak munkaórákkal kell rendelkeznie a kapacitásszámításhoz.</span><span class="sxs-lookup"><span data-stu-id="77d59-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="77d59-137">Lépjen a **Források** \> **Források** oldalra.</span><span class="sxs-lookup"><span data-stu-id="77d59-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="77d59-138">Válasszon egy erőforrást a rekord megnyitásához, majd válassza ki a **Munkaórák megjelenítése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="77d59-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="77d59-139">Tömegesen is frissítheti az erőforrásokat, az **Erőforráslista** nézetből a **Munkaórasablon** alkalmazásával.</span><span class="sxs-lookup"><span data-stu-id="77d59-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="77d59-140">Számlázható tényleges órák hibaelhárítása</span><span class="sxs-lookup"><span data-stu-id="77d59-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="77d59-141">A ténylegesen fizetendő órák a **Tényadatok** entitásból származnak.</span><span class="sxs-lookup"><span data-stu-id="77d59-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="77d59-142">A **számlázható** típusú tényleges órák részei a kiszámításnak, és emiatt rendelkeznie kell olyan projektekkel, ahol tényleges órák számlázhatók.</span><span class="sxs-lookup"><span data-stu-id="77d59-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="77d59-143">Ha nem látható számlázható kihasználtság, az alábbi néhány dolgot ellenőrizheti:</span><span class="sxs-lookup"><span data-stu-id="77d59-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="77d59-144">Az erőforrás kapacitásánál vannak munkaórák.</span><span class="sxs-lookup"><span data-stu-id="77d59-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="77d59-145">Az erőforrásnak van vagy egyedileg meghatározott kihasználtsági célja, vagy egy alapértelmezett szerepkör van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="77d59-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="77d59-146">A szerepkörhöz meg van határozva kihasználtsági cél.</span><span class="sxs-lookup"><span data-stu-id="77d59-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="77d59-147">A tényleges órák rendelkeznek **számlázható** számlázási típussal arra az időszakra, amelyre kihasználtsági számítás elvégzése várható.</span><span class="sxs-lookup"><span data-stu-id="77d59-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="77d59-148">Ellenőrizze a következőket, ha azt látja, hogy a tényleges órák számlázási típusa eltér a számlázhatótól:</span><span class="sxs-lookup"><span data-stu-id="77d59-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="77d59-149">A tényleges órákhoz használt szerepkör alapértelmezett számlázási típusa eltér a számlázhatótól.</span><span class="sxs-lookup"><span data-stu-id="77d59-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="77d59-150">A projekt mögöttes projekt szerződéssorán levő szerepkör nem számlázhatóra van beállítva.</span><span class="sxs-lookup"><span data-stu-id="77d59-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="77d59-151">A projektnek nincs hozzárendelt szerződéssora.</span><span class="sxs-lookup"><span data-stu-id="77d59-151">The project does not have an associated contract line.</span></span>

