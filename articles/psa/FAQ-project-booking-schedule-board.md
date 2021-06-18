---
title: Projektfoglalás létrehozása az Ütemezés tábláról
description: Ez a témakör arról nyújt információt, hogy miként lehet létrehozni egy projektfoglalást az Ütemezés tábláról.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: d33786a5d0a2485a06d174eb7afcbaaa2f337cf6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992969"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="8c0a6-103">Projektfoglalás létrehozása az Ütemezés tábláról</span><span class="sxs-lookup"><span data-stu-id="8c0a6-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8c0a6-104">Az erőforrásokat egy projektre közvetlenül a projekt **Csapat** lapjáról foglalhatja le, vagy generálhat egy erőforrásigényt egy általános csapattag-hozzárendelésből, majd teljesítheti a létrehozott követelményt egy projekten belüli csapattaggal.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="8c0a6-105">Az erőforrásokat a projektekre közvetlenül az Ütemezés tábláról is lefoglalhatja.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="8c0a6-106">Ez három módon oldható meg:</span><span class="sxs-lookup"><span data-stu-id="8c0a6-106">There are three ways to do this:</span></span>

- <span data-ttu-id="8c0a6-107">**Foglalás generált erőforrás-követelményből:** Erőforrás-követelményt generálhat általános erőforrás létrehozása és a projekten belüli feladatok kiosztása után.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="8c0a6-108">**Foglalás az elsődleges követelményből:** Az elsődleges követelmények megjelennek az Ütemezés tábla **Projekt** lapján.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="8c0a6-109">**Foglalás új erőforrás-igénylésből:** Azonnal létrehozhat egy erőforrás-követelményt, és társíthatja azt egy projekthez.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="8c0a6-110">Az Ütemezés táblán az erőforrás-követelmény megjelenik az **Nyílt követelmények** fülön.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="8c0a6-111">Foglalás egy létrehozott erőforrás-követelményből</span><span class="sxs-lookup"><span data-stu-id="8c0a6-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="8c0a6-112">Készíthet általános erőforrást, és egy vagy több feladatot rendelhet hozzá egy projekten belül.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="8c0a6-113">Ezután generálhat egy erőforrás-követelményt az általános csapattagtól.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="8c0a6-114">Az Ütemezés táblán ez az erőforrás megjelenik az **Nyílt követelmények** lapon. Lehet, hogy oszlopszűrőket kell használnia a rácson, ha sok nyílt követelmény van.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="8c0a6-115">![A Követelmények lap megnyitása az Ütemezési táblán](media/FAQ-Project-Booking-Schedule-Board-1.png "A foglalások és hozzárendelések tábla – képernyőkép")</span><span class="sxs-lookup"><span data-stu-id="8c0a6-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="8c0a6-116">Válassza ki a követelmény.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-116">Select the requirement.</span></span> <span data-ttu-id="8c0a6-117">A **Rendelkezésre állás keresése** fül jelenik meg a kiválasztott sor tetején.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="8c0a6-118">A fül kiválasztásakor megnyílik az Ütemezés tábla Ütemezés-asszisztens módja, majd kiszűri a rendelkezésre álló erőforrásokat, amelyek megfelelnek az erőforrás-követelményeknek.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="8c0a6-119">Ezután lefoglalhat egy erőforrást.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="8c0a6-120">A kijelölt sort az Ütemezés tábla aljáról a fenti rács erőforráscellájába is húzhatja.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="8c0a6-121">Amikor ledobja, megjelenik az **Erőforrás-foglalások létrehozása** panel a jobb oldalon.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="8c0a6-122">A **Foglalás** kijelölése lefoglaja az erőforrást a projektcsoport számára.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-122">Selecting **Book** books the resource onto the project team.</span></span>

![Erőforrás-foglalási panel létrehozása](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="8c0a6-124">Foglalás az elsődleges követelményből</span><span class="sxs-lookup"><span data-stu-id="8c0a6-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="8c0a6-125">Egy projekt létrehozása a Project Service megoldásban automatikusan hoz létre egy elsődleges követelmény nevű erőforrás-követelményt.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="8c0a6-126">Ez egy olyan üres követelmény, amelyet az erőforrás gyors ütemezéséhez használnak az Ütemezés táblán követelmény generálása vagy a nulláról való létrehozása nélkül.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="8c0a6-127">Mivel a követelmény üres, meg kell adnia a dátumokat, valamint a beosztási módszert és az órákat, ha alkalmazható.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="8c0a6-128">Erőforrás foglalásához az elsődleges követelménnyel az Ütemezés táblán válassza a **Projekt** fület. Szükség lehet az oszlopszűrő használatára a **Projekt** oszlopon, ha több projekttel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="8c0a6-129">![Oszlopszűrők az Ütemezési táblán](media/FAQ-Project-Booking-Schedule-Board-2.png "A foglalások és hozzárendelések tábla – képernyőkép")</span><span class="sxs-lookup"><span data-stu-id="8c0a6-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="8c0a6-130">Válassza ki azt a követelményt, amelynek csak a projekt neve lesz a neve, és időtartama nulla (0).</span><span class="sxs-lookup"><span data-stu-id="8c0a6-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="8c0a6-131">Válassza az **Elérhetőség keresése** lapot, amely a soron jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="8c0a6-132">Ez az Ütemezés táblát Ütemezés-asszisztens módra állítja, és megmutatja a rendelkezésre álló erőforrásokat, amelyek lefoglalhatók a projektre.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="8c0a6-133">Mivel az **Elsődleges követelmény** nulla (0) időtartammal rendelkező, üres követelmény, az erőforrás kiválasztásakor és lefoglalásakor be kell állítania az időtartamot az **Erőforrás-foglalás létrehozása** panelen.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="8c0a6-134">Az Ütemezés tábla alján kiválaszthatja a **Projekt elsődleges követelményét**, és áthelyezheti az erőforrásba, hogy lefoglalja.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="8c0a6-135">Mivel a **Elsődleges követelmény** egy nulla (0) időtartamú, üres követelmény, akkor kell beállítania az időtartamot az **Erőforrás-foglalás létrehozása** panelen, amikor kiválasztja és lefoglalja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="8c0a6-136">Amikor egy erőforrást az Ütemezés táblán az **Elsődleges követelmény** lehetőségen keresztül foglal le, hozzárendelések nélkül adja hozzá azt a projektcsapathoz.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="8c0a6-137">Foglalás egy új erőforrás-követelményből</span><span class="sxs-lookup"><span data-stu-id="8c0a6-137">Book from a new resource requirement</span></span>
<span data-ttu-id="8c0a6-138">Az új erőforrás-követelményből történő foglaláshoz hajtsa végre a következő lépéseket.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="8c0a6-139">Lépjen az **Erőforráskövetelmény** elemre, majd válassza az **Új** lehetőséget új erőforráskövetelmény létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="8c0a6-140">A **Projekt** fülön válasszon ki egy projektet a követelmény társításához.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="8c0a6-141">Az Ütemezés táblán ez az új követelmény **Nyílt követelmény** formájában jelenik meg, amelyet teljesíteni tud.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="8c0a6-142">Foglalja le az erőforrást a projektcsapathoz történő hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="8c0a6-143">Miután lefoglalta az erőforrást, kézileg kell hozzárendelnie a feladatokat.</span><span class="sxs-lookup"><span data-stu-id="8c0a6-143">Now that the resource is booked, you must assign tasks manually.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]