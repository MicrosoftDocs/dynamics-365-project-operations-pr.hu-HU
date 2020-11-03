---
title: Egyéni megoldások létrehozása árképzési dimenziókra
description: Ez a témakör ismerteti, hogyan lehet egyéni megoldást létrehozni egyéni árképzési dimenziók létrehozásakor.
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
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078101"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="27b7a-103">Egyéni megoldások létrehozása árképzési dimenziókra</span><span class="sxs-lookup"><span data-stu-id="27b7a-103">Create custom solutions for pricing dimensions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="27b7a-104">Az egyéni árképzésidimenzió-változásoknak külön megoldásban kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="27b7a-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="27b7a-105">Ez a fontos gyakorlati tanács rugalmasságot biztosít a jövőben a változtatások frissítéséhez vagy eltávolításához szükség szerint, segítséget nyújt munkájának újbóli felhasználásában, és megkönnyíti a módosítások másik példányra való átvitelét.</span><span class="sxs-lookup"><span data-stu-id="27b7a-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="27b7a-106">Miután elvégezte az összes szükséges módosítást, exportálja a megoldást **Felügyelt megoldásként** , majd importálja azt más példányokra az árképzési beállítások újbóli felhasználása céljából.</span><span class="sxs-lookup"><span data-stu-id="27b7a-106">After you make the required changes, export this solution as a **Managed solution** , and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="27b7a-107">Válassza a **Beállítások** > **Megoldások** opciót, majd az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="27b7a-107">Select **Settings** > **Solutions** , and then select **New**.</span></span> 
2. <span data-ttu-id="27b7a-108">Nevezze el a megoldást, ( **\<your organization name> árképzési dimenziók** ), írja be a további szükséges információkat, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="27b7a-108">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>

> ![Egyéni megoldás létrehozása árképzési dimenziókra](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="27b7a-110">Adja hozzá az összes szükséges entitást és a kapcsolódó komponenseket az árképzési dimenzió megoldáshoz</span><span class="sxs-lookup"><span data-stu-id="27b7a-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="27b7a-111">A következő Project Service entitásokat kell hozzáadnia az árképzési megoldáshoz.</span><span class="sxs-lookup"><span data-stu-id="27b7a-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="27b7a-112">Az eljárás lépéseit követve végezzen el néhány fontos sémaváltoztatást az árképzési megoldásban, hogy az entitások megismerjék az új árképzési dimenziókat.</span><span class="sxs-lookup"><span data-stu-id="27b7a-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="27b7a-113">Válassza a **Beállítások** > **Megoldások** lehetőséget, és kattintson duplán a(z) **\<your organization name> árazási dimenzióira**.</span><span class="sxs-lookup"><span data-stu-id="27b7a-113">Select **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="27b7a-114">A Solution Explorerben a bal oldali navigációs panelen válassza a **Meglévő hozzáadása** > **Entitások** elemet.</span><span class="sxs-lookup"><span data-stu-id="27b7a-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="27b7a-115">A **Megoldás összetevői** párbeszédpanelen válassza ki a következő entitásokat:</span><span class="sxs-lookup"><span data-stu-id="27b7a-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="27b7a-116">Tényadat</span><span class="sxs-lookup"><span data-stu-id="27b7a-116">Actual</span></span>
- <span data-ttu-id="27b7a-117">Lefoglalható erőforrás</span><span class="sxs-lookup"><span data-stu-id="27b7a-117">Bookable Resource</span></span>
- <span data-ttu-id="27b7a-118">Becsléssor</span><span class="sxs-lookup"><span data-stu-id="27b7a-118">Estimate Line</span></span>
- <span data-ttu-id="27b7a-119">Projektfeladat</span><span class="sxs-lookup"><span data-stu-id="27b7a-119">Project Task</span></span>
- <span data-ttu-id="27b7a-120">Számlasor részletei</span><span class="sxs-lookup"><span data-stu-id="27b7a-120">Invoice Line Detail</span></span>
- <span data-ttu-id="27b7a-121">Naplósor</span><span class="sxs-lookup"><span data-stu-id="27b7a-121">Journal Line</span></span>
- <span data-ttu-id="27b7a-122">Projektszerződés sorának részletei</span><span class="sxs-lookup"><span data-stu-id="27b7a-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="27b7a-123">Projektcsoporttag</span><span class="sxs-lookup"><span data-stu-id="27b7a-123">Project Team Member</span></span>
- <span data-ttu-id="27b7a-124">Árajánlatsor részletei</span><span class="sxs-lookup"><span data-stu-id="27b7a-124">Quote Line Detail</span></span>
- <span data-ttu-id="27b7a-125">Szerepkörárrés</span><span class="sxs-lookup"><span data-stu-id="27b7a-125">Role Price Markup</span></span>
- <span data-ttu-id="27b7a-126">Szerepkörár</span><span class="sxs-lookup"><span data-stu-id="27b7a-126">Role Price</span></span> 
- <span data-ttu-id="27b7a-127">Időbejegyzés</span><span class="sxs-lookup"><span data-stu-id="27b7a-127">Time Entry</span></span> 

> ![Adjon hozzá meglévő elemeket az árképzési dimenzió megoldáshoz](media/Existing-entities-to-PD-solution.png)

> ![Megoldás-összetevők kiválasztása](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="27b7a-130">Ügyeljen arra, hogy minden kiválasztott entitás tartalmazzon minden űrlapot és nézetet.</span><span class="sxs-lookup"><span data-stu-id="27b7a-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="27b7a-131">Amikor a rendszer felkéri egy függő entitásnak a kiválasztott entitásokhoz való felvételére, kattintson a **Nem** elemre.</span><span class="sxs-lookup"><span data-stu-id="27b7a-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Ne adja hozzá az összes kapcsolódó komponenst](media/Do-not-include-required.png)


