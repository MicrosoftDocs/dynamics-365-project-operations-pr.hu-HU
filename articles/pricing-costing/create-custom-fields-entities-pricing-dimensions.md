---
title: Egyéni mezők és entitások létrehozása árazási dimenzióként
description: Ez a témakör az egyéni értékkészletek és entitások létrehozását ismerteti.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 616bcd5758b434b45bd06aa1a026f32efc8b7f99
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130896"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="20dd1-103">Egyéni mezők és entitások létrehozása árazási dimenzióként</span><span class="sxs-lookup"><span data-stu-id="20dd1-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="20dd1-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="20dd1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="20dd1-105">Ha egyéni értékkészletet vagy entitást szeretne létrehozni, hajtsa végre az alábbi lépéseket.</span><span class="sxs-lookup"><span data-stu-id="20dd1-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="20dd1-106">Javasoljuk, hogy minden egyéni árképzési dimenziót külön megoldásban hajtson végre.</span><span class="sxs-lookup"><span data-stu-id="20dd1-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="20dd1-107">Ez a fontos gyakorlati tanács rugalmasságot biztosít a jövőben a változtatások frissítéséhez vagy eltávolításához szükség szerint, segítséget nyújt munkájának újbóli felhasználásában, és megkönnyíti a módosítások másik példányra való átvitelét.</span><span class="sxs-lookup"><span data-stu-id="20dd1-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="20dd1-108">Miután elvégezte az összes szükséges módosítást, exportálja a megoldást **Felügyelt megoldásként**, majd importálja azt más példányokra az árképzési beállítások újbóli felhasználása céljából.</span><span class="sxs-lookup"><span data-stu-id="20dd1-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="20dd1-109">Egyéni megoldás létrehozása árképzési dimenziókra</span><span class="sxs-lookup"><span data-stu-id="20dd1-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="20dd1-110">Új megoldás létrehozásához lépjen a **Beállítások** > **Megoldások** részre, és válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="20dd1-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="20dd1-111">Nevezze el a megoldást, (**\<your organization name> árképzési dimenziók**), írja be a további szükséges információkat, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="20dd1-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="20dd1-112">Egyéni mezők és értékkészletek létrehozása az árképzési dimenzió megoldásban</span><span class="sxs-lookup"><span data-stu-id="20dd1-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="20dd1-113">Az árképzési dimenzió lehet értékkészlet vagy entitás.</span><span class="sxs-lookup"><span data-stu-id="20dd1-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="20dd1-114">Mindkettőt létre kell hozni az árképzési megoldásban.</span><span class="sxs-lookup"><span data-stu-id="20dd1-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="20dd1-115">Az eljárás lépései ismertetik az entitás alapú dimenziók és az értékkészlet-alapú dimenziók létrehozását.</span><span class="sxs-lookup"><span data-stu-id="20dd1-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="20dd1-116">Entitásalapú dimenziók</span><span class="sxs-lookup"><span data-stu-id="20dd1-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="20dd1-117">Lépjen a **Beállítások** > **Megoldások** részre, és kattintson duplán a(z) **\<your organization name> árképzési dimenzióira**.</span><span class="sxs-lookup"><span data-stu-id="20dd1-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="20dd1-118">A Solution Explorerben a bal oldali navigációs panelen válassza az **Entitások** elemet.</span><span class="sxs-lookup"><span data-stu-id="20dd1-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="20dd1-119">Válassza az **Új** lehetőséget, és hozzon létre egy **Standard cím** nevű új entitást.</span><span class="sxs-lookup"><span data-stu-id="20dd1-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="20dd1-120">Írja be a további szükséges információt, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="20dd1-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="20dd1-121">Értékkészlet-alapú dimenziók</span><span class="sxs-lookup"><span data-stu-id="20dd1-121">Option set-based dimensions</span></span> 
<span data-ttu-id="20dd1-122">Két értékkészlet-alapú dimenziót hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="20dd1-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="20dd1-123">Használja az **Erőforrás munkahelye** elemet az **Otthon** végzett munka és a **Helyszíni** munka árának nyomon követéséhez, és használja az **Erőforrás munkaideje** elemet a **Rendszeres** és a **Túlóra** értékekkel, hogy jelöléssel láthassa el az elkészült munkát.</span><span class="sxs-lookup"><span data-stu-id="20dd1-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="20dd1-124">Lépjen a **Beállítások** > **Megoldások** részre, és kattintson duplán a(z) **\<your organization name> árképzési dimenzióira**.</span><span class="sxs-lookup"><span data-stu-id="20dd1-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="20dd1-125">A Solution Explorerben a bal oldali navigációs panelen válassza az **Értékkészletek** elemet.</span><span class="sxs-lookup"><span data-stu-id="20dd1-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="20dd1-126">Új értékkészlet létrehozásához kattintson az **Új** elemre, majd írja be a további szükséges információkat, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="20dd1-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="20dd1-127">Adatok létrehozása entitásalapú dimenziókhoz</span><span class="sxs-lookup"><span data-stu-id="20dd1-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="20dd1-128">Entitásalapú dimenziókhoz manuálisan vagy Microsoft Excel importálással vagy szolgáltatáshívások használatával hozhat létre adatokat.</span><span class="sxs-lookup"><span data-stu-id="20dd1-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="20dd1-129">Az eljárás lépéseinek követésévek hozhat létre két szabványos címet: a **Szabványos cím** entitásalapú dimenzióból származó **Rendszermérnök** és **Vezető rendszermérnök**.</span><span class="sxs-lookup"><span data-stu-id="20dd1-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="20dd1-130">Ha a létrehozni kívánt adat kis méretű, a következő példához hasonlóan használhat szabványos űrlapot.</span><span class="sxs-lookup"><span data-stu-id="20dd1-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="20dd1-131">Válassza az **Irányított keresés** lehetőséget, válassza ki az entitás **Normál címét**, majd válassza az **Eredmények** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="20dd1-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="20dd1-132">A **Szabványos cím** összes sora megjelenik.</span><span class="sxs-lookup"><span data-stu-id="20dd1-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="20dd1-133">Válassza az **Új** lehetőséget, és a **Név** mezőbe írja be a „Rendszermérnök” elemet, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="20dd1-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="20dd1-134">Az űrlap bezárása.</span><span class="sxs-lookup"><span data-stu-id="20dd1-134">Close the form.</span></span> 
4. <span data-ttu-id="20dd1-135">Ismételje meg az 1–3. lépést egy újabb szabványos cím létrehozásához a „Vezető rendszermérnök” esetében.</span><span class="sxs-lookup"><span data-stu-id="20dd1-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="20dd1-136">Adja hozzá az összes szükséges entitást és a kapcsolódó komponenseket az árképzési dimenzió megoldáshoz.</span><span class="sxs-lookup"><span data-stu-id="20dd1-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="20dd1-137">A következő entitásokat kell hozzáadnia az árképzési megoldáshoz.</span><span class="sxs-lookup"><span data-stu-id="20dd1-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="20dd1-138">Az eljárás lépéseit követve végezzen el néhány fontos sémaváltoztatást az árképzési megoldásban, hogy az entitások megismerjék az új árképzési dimenziókat.</span><span class="sxs-lookup"><span data-stu-id="20dd1-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="20dd1-139">Válassza a **Beállítások** > **Megoldások** lehetőséget, és kattintson duplán a(z) **\<your organization name> árazási dimenzióira**.</span><span class="sxs-lookup"><span data-stu-id="20dd1-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="20dd1-140">A Solution Explorerben a bal oldali navigációs panelen válassza a **Meglévő hozzáadása** > **Entitások** elemet.</span><span class="sxs-lookup"><span data-stu-id="20dd1-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="20dd1-141">A **Megoldás összetevői** párbeszédpanelen válassza ki a következő entitásokat:</span><span class="sxs-lookup"><span data-stu-id="20dd1-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="20dd1-142">Tény</span><span class="sxs-lookup"><span data-stu-id="20dd1-142">Actual</span></span>
  - <span data-ttu-id="20dd1-143">Lefoglalható erőforrás</span><span class="sxs-lookup"><span data-stu-id="20dd1-143">Bookable Resource</span></span>
  - <span data-ttu-id="20dd1-144">Becsléssor</span><span class="sxs-lookup"><span data-stu-id="20dd1-144">Estimate Line</span></span>
  - <span data-ttu-id="20dd1-145">Számlasor részletei</span><span class="sxs-lookup"><span data-stu-id="20dd1-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="20dd1-146">Naplósor</span><span class="sxs-lookup"><span data-stu-id="20dd1-146">Journal Line</span></span>
  - <span data-ttu-id="20dd1-147">Projektszerződés sorának részletei</span><span class="sxs-lookup"><span data-stu-id="20dd1-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="20dd1-148">Projektcsoporttag</span><span class="sxs-lookup"><span data-stu-id="20dd1-148">Project Team Member</span></span>
  - <span data-ttu-id="20dd1-149">Árajánlatsor részletei</span><span class="sxs-lookup"><span data-stu-id="20dd1-149">Quote Line Detail</span></span>
  - <span data-ttu-id="20dd1-150">Szerepkörárrés</span><span class="sxs-lookup"><span data-stu-id="20dd1-150">Role Price Markup</span></span>
  - <span data-ttu-id="20dd1-151">Szerepkörár</span><span class="sxs-lookup"><span data-stu-id="20dd1-151">Role Price</span></span> 
  - <span data-ttu-id="20dd1-152">Időbejegyzés</span><span class="sxs-lookup"><span data-stu-id="20dd1-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="20dd1-153">Ügyeljen arra, hogy minden kiválasztott entitás tartalmazzon minden űrlapot és nézetet.</span><span class="sxs-lookup"><span data-stu-id="20dd1-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="20dd1-154">Amikor a rendszer felkéri a függő entitás fent megadott entitásokhoz való felvételére, kattintson a **Nem** elemre.</span><span class="sxs-lookup"><span data-stu-id="20dd1-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

