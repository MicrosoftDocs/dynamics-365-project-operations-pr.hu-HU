---
title: Erőforrás hozzárendelése egy feladathoz
description: Ez a témakör információkat nyújt az erőforrások hozzárendeléséről feladatokhoz.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 486371df2de8b400f200dbf38e66cb5e2dec7ae7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286251"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="a8025-103">Erőforrás hozzárendelése egy feladathoz</span><span class="sxs-lookup"><span data-stu-id="a8025-103">Assign a resource to a task</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a8025-104">Három módon lehet erőforrásokat hozzárendelni egy feladathoz a Microsoft Dynamics 365 Project Service Automation felületén.</span><span class="sxs-lookup"><span data-stu-id="a8025-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="a8025-105">Foglalja le az erőforrást csapattagként, majd rendelje hozzá az erőforrást egy feladathoz.</span><span class="sxs-lookup"><span data-stu-id="a8025-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="a8025-106">Felvehet erőforrást a projektcsapatba, majd hozzárendelheti az erőforrást a projekt ütemezésében szereplő feladatokhoz.</span><span class="sxs-lookup"><span data-stu-id="a8025-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="a8025-107">A **Csapattag** lapon vegyen fel új csapattagot az **Új** lehetőség kiválasztásával.</span><span class="sxs-lookup"><span data-stu-id="a8025-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="a8025-108">Megnyílik a **Csapattagok gyors létrehozása** panel, ahol kiválaszthatja a foglalható erőforrás nevét, és beállíthat egy szerepkört.</span><span class="sxs-lookup"><span data-stu-id="a8025-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="a8025-109">Válassza ki az alábbi beosztási módszerek egyikét az erőforrás lefoglalására:</span><span class="sxs-lookup"><span data-stu-id="a8025-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="a8025-110">**Teljes kapacitás** – legfoglalja az erőforrás teljes kapacitását a megadott kezdő és záró dátum között.</span><span class="sxs-lookup"><span data-stu-id="a8025-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="a8025-111">**Százalékos kapacitás** – legfoglalja az erőforrást az erőforrás kapacitásának bizonyos százalékára a megadott kezdő és záró dátum között.</span><span class="sxs-lookup"><span data-stu-id="a8025-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="a8025-112">Az **Egyenlően elosztott órák alapján** módszer az erőforrást meghatározott óraszámban foglalja le napi szinten a megadott kezdő és befejező dátum között.</span><span class="sxs-lookup"><span data-stu-id="a8025-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="a8025-113">**Órák lefoglalása minél hamarabb** – legfoglalja az erőforrást bizonyos mennyiségű órára, minél gyorsabban felhasználva a napi órákat a megadott kezdő és záró dátum között.</span><span class="sxs-lookup"><span data-stu-id="a8025-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="a8025-114">**Nincs** – hozzáadja az erőforrást a csoporthoz, de nem hoz létre a foglalásokat, amelyek felveszik az erőforrás kapacitását.</span><span class="sxs-lookup"><span data-stu-id="a8025-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="a8025-115">A feladat **Ütemezés** rácsán válassza az **Erőforrás** ikont az erőforrás cellájában, majd a **Csapattagok** részen válassza ki az éppen hozzáadott csapattagot.</span><span class="sxs-lookup"><span data-stu-id="a8025-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="a8025-116">A **Csapattag** és az **Egyeztetés** lapon az erőforrás megmutatja a lefoglalt és a hozzárendelt órákat.</span><span class="sxs-lookup"><span data-stu-id="a8025-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="a8025-117">Az óráknak azonosnak kell lenniük, de ez nem követelmény, mivel a foglalások és a hozzárendelések nincsenek szorosan összekapcsolva.</span><span class="sxs-lookup"><span data-stu-id="a8025-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="a8025-118">Az **Egyeztetés** lapon információkat kaphat róluk, ha különböznek, például amikor több órát rendel hozzá egy erőforráshoz, mint amennyit lefoglalt.</span><span class="sxs-lookup"><span data-stu-id="a8025-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="a8025-119">Szükség esetén helyesbítheti az információkat az erőforrás foglalásainak kibővítésével vagy a hozzárendelés megváltoztatásával.</span><span class="sxs-lookup"><span data-stu-id="a8025-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="a8025-120">Általános csapattag létrehozása feladat-hozzárendeléssel</span><span class="sxs-lookup"><span data-stu-id="a8025-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="a8025-121">Amikor egy általános csapattagot feladat-hozzárendeléssel hoz létre, akkor létrehoz egy helyőrzőt vagy általános erőforrást, amely leírja annak a megnevezett erőforrásnak a tulajdonságait, amelyet végül a feladatok elvégzéséhez kíván használni.</span><span class="sxs-lookup"><span data-stu-id="a8025-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="a8025-122">Ezután előállít egy követelményt (vagy kérést nyújt be a követelmény alapján), amely a megnevezett erőforrás keresésére és lefoglalására használható.</span><span class="sxs-lookup"><span data-stu-id="a8025-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="a8025-123">A feladat **Ütemezés** rácsán válassza az **Erőforrás** ikont az erőforrás cellájában.</span><span class="sxs-lookup"><span data-stu-id="a8025-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="a8025-124">Gépelje be a helyőrző erőforrásának nevét.</span><span class="sxs-lookup"><span data-stu-id="a8025-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="a8025-125">Például: Programkezelő.</span><span class="sxs-lookup"><span data-stu-id="a8025-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="a8025-126">Válassza a **Létrehozás** lehetőséget, majd a **Gyors létrehozás: Projektcsapattag** mezőben adja meg az általános erőforrás szerepkörét.</span><span class="sxs-lookup"><span data-stu-id="a8025-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="a8025-127">Folytathatja a feladatok hozzárendelését e helyőrző erőforrásához, ha az **Erőforrásválasztóban** kiválasztja az erőforrást a feladathoz.</span><span class="sxs-lookup"><span data-stu-id="a8025-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="a8025-128">Az erőforrások a **Csapattagok** területen vannak felsorolva.</span><span class="sxs-lookup"><span data-stu-id="a8025-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="a8025-129">Ha befejezte az általános erőforrás hozzárendelését, válassza ki az általános erőforrást a **Csapat** lapon, majd válassza a **Követelmény generálása** lehetőséget az általános erőforrás erőforrásigényének létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="a8025-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="a8025-130">Válassza a **Foglalás** lehetőséget az általános erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="a8025-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="a8025-131">Ezután az Ütemezés táblát használhatja valódi erőforrások megkereséséhez és lefoglalásához.</span><span class="sxs-lookup"><span data-stu-id="a8025-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="a8025-132">El is küldheti a követelményt egy erőforrás-menedzser általi teljesítésre.</span><span class="sxs-lookup"><span data-stu-id="a8025-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="a8025-133">Ha az általános erőforrás teljesítése elnevezett erőforrással történik, az általános erőforrás törlődik a csoportból, és az általános erőforrás feladat-hozzárendelései az elnevezett erőforráshoz lesznek rendelve, aki végrehajtotta az általán erőforrás erőforrás-követelményét.</span><span class="sxs-lookup"><span data-stu-id="a8025-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="a8025-134">Elnevezett erőforrás hozzárendelése az összes foglalható erőforrás listájából</span><span class="sxs-lookup"><span data-stu-id="a8025-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="a8025-135">Használhatja az **Erőforrásválasztó** keresési mezőjét, hogy minden foglalható erőforrásra kereshessen, és hozzárendelhesse őket feladathoz.</span><span class="sxs-lookup"><span data-stu-id="a8025-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="a8025-136">Az így hozzárendelt erőforrások foglalás nélkül lesznek hozzáadva a csapathoz.</span><span class="sxs-lookup"><span data-stu-id="a8025-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="a8025-137">Ez hasonló ahhoz, amikor csapattagot ad hozzá, és a „Nincs” beosztási módszert választja.</span><span class="sxs-lookup"><span data-stu-id="a8025-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="a8025-138">Az erőforrás a **Csapat** és az **Egyeztetés** lapon jelenik meg csak hozzárendelésekkel és beosztási hiánnyal rendelkező erőforrásokként.</span><span class="sxs-lookup"><span data-stu-id="a8025-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="a8025-139">Ha a rendelkezésre állásukat használni kívánja, foglalja le őket.</span><span class="sxs-lookup"><span data-stu-id="a8025-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="a8025-140">A feladat **Ütemezés** rácsán válassza az **Erőforrás** ikont az erőforrás cellájában.</span><span class="sxs-lookup"><span data-stu-id="a8025-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="a8025-141">Kezdjen el beírni egy nevet.</span><span class="sxs-lookup"><span data-stu-id="a8025-141">Start typing a name.</span></span> <span data-ttu-id="a8025-142">A név keresési eredményei megjelennek az **Erőforrás választóban** az **Egyéb erőforrások** részen.</span><span class="sxs-lookup"><span data-stu-id="a8025-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="a8025-143">Válassza ki azt az erőforrást, amelyet hozzá szeretne rendelni a feladathoz.</span><span class="sxs-lookup"><span data-stu-id="a8025-143">Select the resource that you want to assign to the task.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]