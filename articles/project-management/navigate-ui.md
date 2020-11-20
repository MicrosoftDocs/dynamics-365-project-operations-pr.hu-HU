---
title: A felhasználói felületen történő navigálás
description: Ez a témakör információkat nyújt a Dynamics 365 Project Operations Projektmenedzsment funkciójáról.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: deedfe0c6601fd09e09460034c9a0db936b6566e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127521"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="8ed6f-103">A felhasználói felületen történő navigálás</span><span class="sxs-lookup"><span data-stu-id="8ed6f-103">Navigating the user interface</span></span>

<span data-ttu-id="8ed6f-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="8ed6f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="8ed6f-105">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8ed6f-105">Overview</span></span>

<span data-ttu-id="8ed6f-106">A fő projekt űrlapja több lapra van elválasztva.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="8ed6f-107">Minden lap a projekt különböző részletességi szintjének felel meg.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="8ed6f-108">**Összegzés**: A projekt leírását tartalmazza, és összesíti mind a tervezett, mind a tényleges projektteljesítményt.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-108">**Summary**: Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Összegzés lap és mezők](media/navigation7.png)

- <span data-ttu-id="8ed6f-110">**Feladatok**: Egy rács nézet, egy táblázatos nézet és egy gantt segítségével ábrázolt munkalebontási struktúrára vonatkozó részleteket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-110">**Tasks**: Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Feladat lap és mezők](media/navigation8.png)

- <span data-ttu-id="8ed6f-112">**Csoport**: A projekt résztvevőinek részletes ismertetését tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-112">**Team**: Provides details regarding the project participants.</span></span> <span data-ttu-id="8ed6f-113">Az egyes csoporttagokhoz rendelt erőfeszítés szintén ebben a nézetben kerül összesítésre.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Csoport lap és mezők](media/navigation9.png)

- <span data-ttu-id="8ed6f-115">**Erőforrás-hozzárendelések**: A projekt egyes erőforrásaira vonatkozó erőfeszítés időfázisos nézetét biztosítja.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-115">**Resource assignments**: Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Erőforrás-hozzárendelések lap és mezők](media/navigation10.png)

- <span data-ttu-id="8ed6f-117">**Erőforrás-egyeztetés**: Időfázisos nézetet biztosít az egyes megnevezett erőforrások hozzárendelései és a foglalásuk közötti különbségekről.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-117">**Resource reconciliation**: Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Erőforrás-egyeztetés lap és mezők](media/navigation11.png)

- <span data-ttu-id="8ed6f-119">**Becslések**: A projekt költség- és értékesítési becslésének időfázisos nézetét biztosítja.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-119">**Estimates**: Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Becslések lap és mezők](media/navigation12.png)

- <span data-ttu-id="8ed6f-121">**Nyomon követés**: olyan nézetet biztosít, amely mutatja a feladatok előrehaladását a munkalebontási struktúrában az erőkifejtés, a költség és az értékesítés szempontjából.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-121">**Tracking**: Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Nyomon követés lap és mezők](media/navigation13.png)

- <span data-ttu-id="8ed6f-123">**Értékesítés**: Mélyhivatkozásokat tartalmaz a projekthez kapcsolódó ajánlatokhoz és szerződésekhez.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-123">**Sales**: Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="8ed6f-124">**Költségbecslések**: Olyan rácsot biztosít, amely a projektek költségeit definiálja a szervezeti költség kategóriái alapján.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-124">**Expense Estimates**: Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Költségbecslések lap és mezők](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="8ed6f-126">Rácsok vezérlői</span><span class="sxs-lookup"><span data-stu-id="8ed6f-126">Grid controls</span></span>

<span data-ttu-id="8ed6f-127">A következő rész rövid áttekintést nyújt a különböző projekttervezési lapokon található tipikus vezérlőkről.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="8ed6f-128">Frissítés</span><span class="sxs-lookup"><span data-stu-id="8ed6f-128">Refresh</span></span>

<span data-ttu-id="8ed6f-129">**Frissítés**: A legfrissebb adatok beolvasása a kiszolgálóról, ha bármilyen változás történt a rács betöltése után.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-129">**Refresh**: Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Frissítés gomb](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="8ed6f-131">Csoportosítás szempontja</span><span class="sxs-lookup"><span data-stu-id="8ed6f-131">Group by</span></span>

<span data-ttu-id="8ed6f-132">**Csoportosítás alapja**: Frissíti a rács sorainak csoportosítását, hogy az az erőforrásokat, a szerepköröket vagy a kategóriákat tükrözze a felhasználó igényei alapján.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-132">**Group by**: Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Csoportosítás gomb szerint](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="8ed6f-134">Előző/Következő</span><span class="sxs-lookup"><span data-stu-id="8ed6f-134">Previous/Next</span></span>

<span data-ttu-id="8ed6f-135">**Előző**/**Következő**: A látható időszakok frissítése az időfázisos rácsokon.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-135">**Previous**/**Next**: Update the visible time periods on the time-phased grids.</span></span>

![Előző és Következő gombok](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="8ed6f-137">Időskála</span><span class="sxs-lookup"><span data-stu-id="8ed6f-137">Timescale</span></span>

<span data-ttu-id="8ed6f-138">**Időskála**: Az időfázisos adatok közötti összesítés váltása napok, hetek, hónapok és évek között.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-138">**Timescale**: Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Időskála gomb](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="8ed6f-140">Kibontás</span><span class="sxs-lookup"><span data-stu-id="8ed6f-140">Expand</span></span>

<span data-ttu-id="8ed6f-141">**Kibontás**: A látható rácsot teljes képernyőre teszi, így további szerepkörök is megjelenhetnek.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-141">**Expand**: Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![Kibontás gomb](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="8ed6f-143">Időfázis alapja:</span><span class="sxs-lookup"><span data-stu-id="8ed6f-143">Time-phase by</span></span>

<span data-ttu-id="8ed6f-144">**Időfázis alapja**: A rácssorok csoportosításának frissítése az értékesítési becslések becsült költségének tükrözéséhez.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-144">**Time-phase by**: Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="8ed6f-145">Ez a vezérlő a becslési parancsfájlra és a nyomonkövetési rácsra is érvényes.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Időfázis gomb szerint](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="8ed6f-147">Oszlop hozzáadása</span><span class="sxs-lookup"><span data-stu-id="8ed6f-147">Add column</span></span>

<span data-ttu-id="8ed6f-148">**Oszlop hozzáadása**: Lehetővé teszi, hogy a felhasználó a rácsban látható oszlopokat definiálja.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-148">**Add column**: Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="8ed6f-149">A **Projekttervezés** űrlapján csak gyári oszlopok adhatók hozzá a rácsokhoz.</span><span class="sxs-lookup"><span data-stu-id="8ed6f-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Oszlop hozzáadása gomb](media/navigation5.png)
