---
title: Projekt foglalása
description: Ez a témakör információt nyújt az erőforrások lefoglalásáról egy projekthez.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 15de5735ba6d25994a68192ebdf80aefec772d6e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998819"
---
# <a name="book-to-a-project"></a><span data-ttu-id="4cf21-103">Projekt foglalása</span><span class="sxs-lookup"><span data-stu-id="4cf21-103">Book to a project</span></span>

<span data-ttu-id="4cf21-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="4cf21-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4cf21-105">Vannak olyan időpontok, amikor egy projektmenedzsernek vagy erőforrás-kezelőnek egy erőforrást kell lefoglalnia a projekthez meghatározott követelmény nélkül egy általános csoporttagtól.</span><span class="sxs-lookup"><span data-stu-id="4cf21-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="4cf21-106">Ez három módon valósítható meg.</span><span class="sxs-lookup"><span data-stu-id="4cf21-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="4cf21-107">Foglalás a csoporttagrácsból</span><span class="sxs-lookup"><span data-stu-id="4cf21-107">Book from the team member grid</span></span>
- <span data-ttu-id="4cf21-108">Foglalás az ütemezési tábláról</span><span class="sxs-lookup"><span data-stu-id="4cf21-108">Book from the schedule board</span></span>
- <span data-ttu-id="4cf21-109">Foglalás a **Projekt** űrlapról</span><span class="sxs-lookup"><span data-stu-id="4cf21-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="4cf21-110">Foglalás a csoporttagrácsból</span><span class="sxs-lookup"><span data-stu-id="4cf21-110">Book from the team member grid</span></span>

<span data-ttu-id="4cf21-111">Ha a szervezet hibrid erőforrás-elosztási módban működik, akkor a projektmenedzser az alábbi lépések végrehajtásával közvetlenül a projekthez tudja lefoglalni az erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="4cf21-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="4cf21-112">A projektből nyissa meg a csoporttagrácsot, és válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="4cf21-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="4cf21-113">Adja meg az erőforrás pozíciójának nevét és szerepét.</span><span class="sxs-lookup"><span data-stu-id="4cf21-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="4cf21-114">Válassza ki a lefoglalható erőforrást a rendelkezésre álló keresésből.</span><span class="sxs-lookup"><span data-stu-id="4cf21-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="4cf21-115">Az erőforrás kiválasztását követően adja meg a következő mezők adatait az erőforrás lefoglalásához:</span><span class="sxs-lookup"><span data-stu-id="4cf21-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="4cf21-116">Kezdődátum</span><span class="sxs-lookup"><span data-stu-id="4cf21-116">Start date</span></span>
    - <span data-ttu-id="4cf21-117">Befejezési dátum</span><span class="sxs-lookup"><span data-stu-id="4cf21-117">Finish date</span></span>
    - <span data-ttu-id="4cf21-118">Felosztási mód</span><span class="sxs-lookup"><span data-stu-id="4cf21-118">Allocation method</span></span>
    - <span data-ttu-id="4cf21-119">Órák száma, ha alkalmazható</span><span class="sxs-lookup"><span data-stu-id="4cf21-119">Hours, if applicable</span></span>
    - <span data-ttu-id="4cf21-120">Projekt jóváhagyója</span><span class="sxs-lookup"><span data-stu-id="4cf21-120">Project approver</span></span>

6. <span data-ttu-id="4cf21-121">Válassza a **Mentés és bezárás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="4cf21-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="4cf21-122">Foglalás az ütemezési tábláról</span><span class="sxs-lookup"><span data-stu-id="4cf21-122">Book from the schedule board</span></span>

<span data-ttu-id="4cf21-123">Amikor egy erőforrás-kezelőnek közvetlenül egy projekthez kell lefoglalnia az erőforrást, az ütemezési táblát és a projektkövetelményt is használhatja.</span><span class="sxs-lookup"><span data-stu-id="4cf21-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="4cf21-124">A projektkövetelmény olyan erőforrás-követelmény, amely minden esetben elérhető a foglaláshoz.</span><span class="sxs-lookup"><span data-stu-id="4cf21-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="4cf21-125">A közvetlenük egy projektűrlapra történő foglaláshoz hajtsa végre b következő lépéseket.</span><span class="sxs-lookup"><span data-stu-id="4cf21-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="4cf21-126">Lépjen az ütemezési táblához, és a bal oldalon szűrje a szükségletre szánt szükséges erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="4cf21-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="4cf21-127">Az alsó ablaktáblában válassza a **Projekt** lapot a projektkövetelmények listájának megjelenítéséhez.</span><span class="sxs-lookup"><span data-stu-id="4cf21-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="4cf21-128">Húzza a követelményt egy erőforrásra, és adja meg a következő adatokat:</span><span class="sxs-lookup"><span data-stu-id="4cf21-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="4cf21-129">Kezdődátum</span><span class="sxs-lookup"><span data-stu-id="4cf21-129">Start date</span></span>
    - <span data-ttu-id="4cf21-130">Befejezési dátum</span><span class="sxs-lookup"><span data-stu-id="4cf21-130">Finish date</span></span>
    - <span data-ttu-id="4cf21-131">Foglalás állapota</span><span class="sxs-lookup"><span data-stu-id="4cf21-131">Booking status</span></span>
    - <span data-ttu-id="4cf21-132">Foglalási módszer</span><span class="sxs-lookup"><span data-stu-id="4cf21-132">Booking method</span></span>
    - <span data-ttu-id="4cf21-133">Időtartam</span><span class="sxs-lookup"><span data-stu-id="4cf21-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="4cf21-134">Foglalás a Projekt űrlapról</span><span class="sxs-lookup"><span data-stu-id="4cf21-134">Book from the Project form</span></span>

<span data-ttu-id="4cf21-135">Projektmenedzserként előfordulhat, hogy erőforrást kell lefoglalnia egy projekthez, de csak a feltételeket tudja megismerni, nem az erőforrás nevét.</span><span class="sxs-lookup"><span data-stu-id="4cf21-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="4cf21-136">Hajtsa végre a következő lépéseket, hogy az ütemezési segéd segítségével megkeresse az erőforrást az erőforrás bármely rendelkezésre álló attribútuma alapján.</span><span class="sxs-lookup"><span data-stu-id="4cf21-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="4cf21-137">Lépjen a projekthez, és válassza a **Foglalás** lehetőséget az ütemezési segéd megnyitásához.</span><span class="sxs-lookup"><span data-stu-id="4cf21-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="4cf21-138">Az ütemezési segéd bal oldalán található szűrők használatával szűkítse a feltételeket, és válassza a **Keresés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="4cf21-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="4cf21-139">Az eredményekben visszaadott erőforrások alapján lefoglalhatja az erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="4cf21-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="4cf21-140">Ez a módszer nem hoz létre az erőforráshoz tartozó foglalásokat.</span><span class="sxs-lookup"><span data-stu-id="4cf21-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="4cf21-141">Ehelyett az erőforrást hozzáadja a projektcsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="4cf21-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="4cf21-142">Miután a csapattagot hozzáadta a projekthez, a projektmenedzser használhatja a foglalások fenntartását vagy a foglalások kiterjesztését, és felveheti a szükséges foglalásokat az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="4cf21-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]