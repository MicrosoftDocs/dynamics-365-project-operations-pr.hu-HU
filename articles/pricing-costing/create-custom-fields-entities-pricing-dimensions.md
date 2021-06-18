---
title: Egyéni mezők és entitások létrehozása árazási dimenzióként
description: Ez a témakör az egyéni értékkészletek és entitások létrehozását ismerteti.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 41c57690fecbc3bee2a1eb5d26f8a6aa56d8bea9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000529"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="37bf3-103">Egyéni mezők és entitások létrehozása árazási dimenzióként</span><span class="sxs-lookup"><span data-stu-id="37bf3-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="37bf3-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="37bf3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="37bf3-105">Hajtsa végre az alábbi lépéseket, amikor egyéni értékkészletet vagy entitást szeretne létrehozni, hogy azt árazási dimenzióként használja.</span><span class="sxs-lookup"><span data-stu-id="37bf3-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="37bf3-106">További információkért lásd: [Árazási dimenziók áttekintése](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="37bf3-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="37bf3-107">Javasoljuk, hogy minden egyéni árképzési dimenziót külön megoldásban hajtson végre.</span><span class="sxs-lookup"><span data-stu-id="37bf3-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="37bf3-108">Ez a fontos gyakorlati tanács rugalmasságot biztosít a jövőben a szükséges változtatások frissítéséhez vagy eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="37bf3-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="37bf3-109">Ez a művelet a munkájának újbóli felhasználását is segíti, és megkönnyíti a változtatások egy másik példányra történő portolását, miután elvégezte az összes szükséges változtatást, exportálja ezt a megoldást **Felügyelt megoldásként**, és importálja más példányokra az árképzési beállítások újbóli felhasználása céljából.</span><span class="sxs-lookup"><span data-stu-id="37bf3-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="37bf3-110">Egyéni mezők és értékkészletek létrehozása az árképzési dimenzió megoldásban</span><span class="sxs-lookup"><span data-stu-id="37bf3-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="37bf3-111">Az árképzési dimenzió lehet értékkészlet vagy entitás.</span><span class="sxs-lookup"><span data-stu-id="37bf3-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="37bf3-112">Mindkettőt létre kell hozni az árképzési megoldásban.</span><span class="sxs-lookup"><span data-stu-id="37bf3-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="37bf3-113">Az eljárás lépései ismertetik az entitás alapú dimenziók és az értékkészlet-alapú dimenziók létrehozását.</span><span class="sxs-lookup"><span data-stu-id="37bf3-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="37bf3-114">Entitásalapú dimenziók</span><span class="sxs-lookup"><span data-stu-id="37bf3-114">Entity-based dimensions</span></span>
<span data-ttu-id="37bf3-115">Az entitásalapú dimenziók létrehozásához tegye a következőket:</span><span class="sxs-lookup"><span data-stu-id="37bf3-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="37bf3-116">Lépjen a **Beállítások** > **Megoldások** részre, és kattintson duplán a(z) **\<your organization name> árképzési dimenzióira**.</span><span class="sxs-lookup"><span data-stu-id="37bf3-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="37bf3-117">A Megoldástallózóban a bal oldali navigációs panelen válassza az **Entitások** elemet.</span><span class="sxs-lookup"><span data-stu-id="37bf3-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="37bf3-118">Válassza az **Új** lehetőséget, és hozzon létre egy **Standard cím** nevű új entitást.</span><span class="sxs-lookup"><span data-stu-id="37bf3-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="37bf3-119">Írja be a további szükséges információt, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="37bf3-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![A standard című entitás meghatározása](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="37bf3-121">Értékkészlet-alapú dimenziók</span><span class="sxs-lookup"><span data-stu-id="37bf3-121">Option set-based dimensions</span></span> 
<span data-ttu-id="37bf3-122">Két értékkészlet-alapú dimenziót hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="37bf3-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="37bf3-123">Az **Erőforrás-munkaterület** segítségével nyomon követheti az **Otthoni** munka és a **Helyszíni** munkavégzés árát.</span><span class="sxs-lookup"><span data-stu-id="37bf3-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="37bf3-124">Az **Erőforrások munkaóráit** használja a **Normál** és a **Túlóra** értékkel , ha a munka befejezésekor a felárat kell alkalmazni.</span><span class="sxs-lookup"><span data-stu-id="37bf3-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="37bf3-125">A következő ábra az **Erőforrás munkavégzési helyének** dimenzióját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="37bf3-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Erőforrás munkahelye nevű értékkészlet-alapú árképzési dimenzió](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="37bf3-127">A következő ábra az **Erőforrás munkaóráinak** dimenzióját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="37bf3-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Erőforrás munkaideje nevű értékkészlet-alapú árképzési dimenzió](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="37bf3-129">Lépjen a **Beállítások** > **Megoldások** részre, és kattintson duplán a(z) **\<your organization name> árképzési dimenzióira**.</span><span class="sxs-lookup"><span data-stu-id="37bf3-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="37bf3-130">A Solution Explorerben a bal oldali navigációs panelen válassza az **Értékkészletek** elemet.</span><span class="sxs-lookup"><span data-stu-id="37bf3-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="37bf3-131">Új értékkészlet létrehozásához kattintson az **Új** elemre, majd írja be a további szükséges információkat, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="37bf3-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="37bf3-132">Adatok létrehozása entitásalapú dimenziókhoz</span><span class="sxs-lookup"><span data-stu-id="37bf3-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="37bf3-133">Entitásalapú dimenziókhoz manuálisan vagy Microsoft Excel importálással vagy szolgáltatáshívások használatával hozhat létre adatokat.</span><span class="sxs-lookup"><span data-stu-id="37bf3-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="37bf3-134">Az eljárás lépéseinek követésévek hozhat létre két szabványos címet: a **Szabványos cím** entitásalapú dimenzióból származó **Rendszermérnök** és **Vezető rendszermérnök**.</span><span class="sxs-lookup"><span data-stu-id="37bf3-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="37bf3-135">Ha a létrehozni kívánt adat kis méretű, a következő példához hasonlóan használhat szabványos űrlapot.</span><span class="sxs-lookup"><span data-stu-id="37bf3-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="37bf3-136">Válassza az **Irányított keresés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="37bf3-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="37bf3-137">Válassza ki a **Szabványos cím** entitást, majd válassza az **Eredmények** elemet.</span><span class="sxs-lookup"><span data-stu-id="37bf3-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="37bf3-138">A **Szabványos cím** összes sora megjelenik.</span><span class="sxs-lookup"><span data-stu-id="37bf3-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="37bf3-139">Válassza az **Új** lehetőséget, és a **Név** mezőbe írja be a „Rendszermérnök” elemet, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="37bf3-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="37bf3-140">Zárja be a lapot.</span><span class="sxs-lookup"><span data-stu-id="37bf3-140">Close the page.</span></span> 
5. <span data-ttu-id="37bf3-141">Ismételje meg az 1–3. lépést egy újabb szabványos cím létrehozásához a „Vezető rendszermérnök” esetében.</span><span class="sxs-lookup"><span data-stu-id="37bf3-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Mintaadatok a szabványos cím entitáshoz](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]