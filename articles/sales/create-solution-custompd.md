---
title: Megoldás létrehozása egyéni árképzési dimenziókhoz
description: Ez a témakör az árazási dimenziókhoz tartozó megoldások létrehozásáról nyújt információt.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513991"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="716b3-103">Megoldás létrehozása egyéni árképzési dimenziókhoz</span><span class="sxs-lookup"><span data-stu-id="716b3-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="716b3-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="716b3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="716b3-105">Az egyéni árképzésidimenzió-változásoknak külön megoldásban kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="716b3-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="716b3-106">Ez a fontos gyakorlati tanács rugalmasságot biztosít a változtatások frissítéséhez vagy eltávolításához szükség szerint, segítséget nyújt munkájának újbóli felhasználásában, és megkönnyíti a módosítások másik példányra való átvitelét.</span><span class="sxs-lookup"><span data-stu-id="716b3-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="716b3-107">Miután elvégezte az összes szükséges módosítást, exportálja a megoldást **Felügyelt** megoldásként, majd importálja azt más példányokra az újbóli felhasználása céljából.</span><span class="sxs-lookup"><span data-stu-id="716b3-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="716b3-108">Megoldás létrehozása egyéni árképzési dimenziókhoz</span><span class="sxs-lookup"><span data-stu-id="716b3-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="716b3-109">Válassza a **Beállítások** > **Megoldások** opciót, majd az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="716b3-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="716b3-110">Nevezze el a megoldást, *<your organization name> árképzési dimenzióka*.</span><span class="sxs-lookup"><span data-stu-id="716b3-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="716b3-111">Írja be a további szükséges információt, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="716b3-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Egyéni árképzési megoldás létrehozása](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="716b3-113">Adja hozzá az összes szükséges entitást és a kapcsolódó komponenseket az árképzési dimenzió megoldáshoz</span><span class="sxs-lookup"><span data-stu-id="716b3-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="716b3-114">Adja hozzá a következő Project Service-entitásokat az árképzési megoldáshoz, hogy fontos sémamódosításokat hajtson végre az árképzési megoldásban.</span><span class="sxs-lookup"><span data-stu-id="716b3-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="716b3-115">Miután befejezte ezt az eljárást, az entitások felismerik az új árképzési dimenziókat.</span><span class="sxs-lookup"><span data-stu-id="716b3-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="716b3-116">Válassz a **Beállítások** > **Megoldások** elemez, majd kattintson duplán a **<*szervezet neve*> árazási dimenziók** elemre.</span><span class="sxs-lookup"><span data-stu-id="716b3-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="716b3-117">A Solution Explorerben a bal oldali navigációs panelen válassza a **Meglévő hozzáadása** > **Entitások** elemet.</span><span class="sxs-lookup"><span data-stu-id="716b3-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="716b3-118">A **Megoldás összetevői** párbeszédpanelen válassza ki a következő entitásokat:</span><span class="sxs-lookup"><span data-stu-id="716b3-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="716b3-119">**Tényadat**</span><span class="sxs-lookup"><span data-stu-id="716b3-119">**Actual**</span></span>
   - <span data-ttu-id="716b3-120">**Lefoglalható erőforrás**</span><span class="sxs-lookup"><span data-stu-id="716b3-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="716b3-121">**Becsléssor**</span><span class="sxs-lookup"><span data-stu-id="716b3-121">**Estimate Line**</span></span>
   - <span data-ttu-id="716b3-122">**Projektfeladat**</span><span class="sxs-lookup"><span data-stu-id="716b3-122">**Project Task**</span></span>
   - <span data-ttu-id="716b3-123">**Számlasor részletei**</span><span class="sxs-lookup"><span data-stu-id="716b3-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="716b3-124">**Naplósor**</span><span class="sxs-lookup"><span data-stu-id="716b3-124">**Journal Line**</span></span>
   - <span data-ttu-id="716b3-125">**Projektszerződés sorának részletei**</span><span class="sxs-lookup"><span data-stu-id="716b3-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="716b3-126">**Projektcsoporttag**</span><span class="sxs-lookup"><span data-stu-id="716b3-126">**Project Team Member**</span></span>
   - <span data-ttu-id="716b3-127">**Árajánlatsor részletei**</span><span class="sxs-lookup"><span data-stu-id="716b3-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="716b3-128">**Szerepkörárrés**</span><span class="sxs-lookup"><span data-stu-id="716b3-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="716b3-129">**Szerepkörár**</span><span class="sxs-lookup"><span data-stu-id="716b3-129">**Role Price**</span></span>
   - <span data-ttu-id="716b3-130">**Időbejegyzés**</span><span class="sxs-lookup"><span data-stu-id="716b3-130">**Time Entry**</span></span>
 
   ![Adjon hozzá meglévő entitásokat az árképzési dimenzió megoldáshoz](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="716b3-132">Tekintse át az egyes entitások hozzáadott összetevőit és az egyes entitások entitáseszközeinek végleges listáját.</span><span class="sxs-lookup"><span data-stu-id="716b3-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="716b3-133">Minden kiválasztott entitás tartalmazzon minden űrlapot és nézetet.</span><span class="sxs-lookup"><span data-stu-id="716b3-133">Include all forms and views for each of the selected entities.</span></span>

  ![Hozzáadott entitások](./media/solution-component-selection.png)


5.  <span data-ttu-id="716b3-135">Amikor a rendszer kéri, hogy a kijelölt entitások függő entitásait is adja hozzá, válassza a **Nem adom hozzá a szükséges összetevőket** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="716b3-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Függő entitásokkal együtt](./media/Do-not-include-required.png)
