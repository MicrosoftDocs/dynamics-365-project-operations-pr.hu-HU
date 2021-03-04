---
title: Időbejegyzések készítése
description: Ez a témakör információkat nyújt az időbejegyzések létrehozásáról.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 520d3a6e6cc3d486d778c66c2ef7fd3ff20cd582
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149681"
---
# <a name="create-time-entries"></a><span data-ttu-id="bc2e2-103">Időbejegyzések készítése</span><span class="sxs-lookup"><span data-stu-id="bc2e2-103">Create time entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="bc2e2-104">A Dynamics 365 Project Service Automation korábbi verzióiban az időbejegyzéseket hetenként adták meg.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="bc2e2-105">A Project Service Automation 3. verziójában az időbejegyzéseket naponta kell beírni.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="bc2e2-106">Néhány alkalommal a bejegyzések létrehozása után azonban tömegesen létrehozhat vagy lemásolhatja azokat.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="bc2e2-107">Időbejegyzés létrehozása</span><span class="sxs-lookup"><span data-stu-id="bc2e2-107">Create a time entry</span></span>

<span data-ttu-id="bc2e2-108">Időbejegyzés létrehozásához kövesse ezeket a lépéseket.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="bc2e2-109">Az **Időbejegyzés** oldalon válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="bc2e2-110">A **Gyors létrehozás: Időbevitel** párbeszédpanelen adja meg az időbevitel időtartamát percben, órában vagy napban.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="bc2e2-111">Az időtartamot a következő formátumban kell megadni: *x* perc, *x* óra vagy *x* nap.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="bc2e2-112">Órák és napok decimális értékként is megadhatók, például *xx* óra vagy *xx* nap.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="bc2e2-113">Válassza ki az időbevitel típusát és azt a projektet, amelyhez beírja az időbejegyzést.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="bc2e2-114">A **Projektfeladat** mezőben keresse meg az időbejegyzés feladatát.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bc2e2-115">Ha létrehoz egy időbejegyzést a feladathoz, amely nincs hozzárendelve egy felhasználóhoz, a **Projektfeladat** mezőben válassza ki a **Keresés** gombot, válassza a **Nézet módosítása** elemet, majd válassza az **Összes aktív projektfeladat** elemet az összes feladat felsorolásához.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="bc2e2-116">Írja be a leírást, ha leírásra van szükség, majd válassza a **Mentés és bezárás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="bc2e2-117">Az időbejegyzés létrehozása és mentése után szerkesztheti azt az időbeviteli rácsban.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="bc2e2-118">Az időbeviteli rács két formátumot támogat:</span><span class="sxs-lookup"><span data-stu-id="bc2e2-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="bc2e2-119">Az időbevitelt **hh:mm** formátumban adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="bc2e2-120">Ezt a formátumot ezután órákra és frakciókra konvertálják.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="bc2e2-121">Az órákat és a frakciókat közvetlenül megadhatja.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="bc2e2-122">Vegye figyelembe, hogy az egy óra töredéke nem perc.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="bc2e2-123">Ezért az 1,5 óra 1 óra és 30 perc.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="bc2e2-124">Ugyanez a szabály vonatkozik a napi részekre.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="bc2e2-125">Egy nap 24 óra, a 0,5 nap pedig 12 órát jelent.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="bc2e2-126">Időbejegyzések tömeges létrehozása</span><span class="sxs-lookup"><span data-stu-id="bc2e2-126">Bulk create time entries</span></span>

<span data-ttu-id="bc2e2-127">Néhány időbejegyzés létrehozása után másolhatja őket, hogy tömegesen hozzon létre további időbejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="bc2e2-128">Az **Időbevitel** oldalon válassza a **Hét másolása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="bc2e2-129">A **Periódusból** mezőcsoportban a **Kezdő dátum** és **Befejező dátum** mezőkben határozza meg az időtartományt, ahonnan az időbejegyzéseket másolni lehet.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="bc2e2-130">A **Periódusba** mezőcsoportban a **Kezdő dátum** mezőben adja meg a dátumot, ahova időbejegyzéseket hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="bc2e2-131">Válassza a **Másolás** lehetőséget , hogy az **Periódusba** mezőcsoportban megadott hét napjának megfelelő időbejegyzések másolatát hozzon létre.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="bc2e2-132">Például a múlt hét hétfőjének időbejegyzését átmásolja arra a hét hétfőjére, amelyet a **Periódusba** mezőcsoport határoz meg.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="bc2e2-133">Adatok importálása az időbejegyzésekhez</span><span class="sxs-lookup"><span data-stu-id="bc2e2-133">Import data for time entries</span></span>

<span data-ttu-id="bc2e2-134">Adatokat importálhat a projektfoglalásokból és a megbízásokból.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="bc2e2-135">Adatok importálásakor meghatározhatja az importálandó foglalások dátumtartományát, majd kifejezetten kiválaszthatja azokat a foglalásokat, amelyeket **Vázlat** időbejegyzésként kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="bc2e2-136">Csoportosítás, rendezés, keresés és szűrési lehetőségek</span><span class="sxs-lookup"><span data-stu-id="bc2e2-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="bc2e2-137">Az időbejegyzéseket az oszlopokban megadott méretek szerint csoportosíthatja és szűrheti.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="bc2e2-138">A **Csoportosítás** mezőben válassza ki az időbejegyzések szűréséhez használandó dimenziót.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="bc2e2-139">Az időbeviteli rekordokat növekvő vagy csökkenő sorrendbe is rendezheti az oszlopfejléceken található rendezési nyíl segítségével.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="bc2e2-140">Ezenkívül a bejegyzéseket megjelenítheti vagy elrejtheti, ha kiválasztja a **Szűrés** gombot az oszlopfejlécekben, majd a **Keresés** mezőbe írja be azt a szöveget, amelyet az időbejegyzés keresésére használnak a projekt neve, a projekt feladata, az idő szerint bejegyzés vagy erőforrás.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
