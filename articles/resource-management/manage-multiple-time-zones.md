---
title: Időzónák kezelése
description: A projekt létrehozásakor az időzónája a munkaidősablonban megadott időzónán alapul.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e0cf24a9916f7ceedee0e9d6fa9399a88c3e4b91
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279546"
---
# <a name="manage-time-zones"></a><span data-ttu-id="66e68-103">Időzónák kezelése</span><span class="sxs-lookup"><span data-stu-id="66e68-103">Manage time zones</span></span>

<span data-ttu-id="66e68-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="66e68-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="66e68-105">Projektek</span><span class="sxs-lookup"><span data-stu-id="66e68-105">Projects</span></span>

<span data-ttu-id="66e68-106">A projekt létrehozásakor az időzónája az alkalmazott munkaidősablonban megadott időzónán alapul.</span><span class="sxs-lookup"><span data-stu-id="66e68-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="66e68-107">A **Projekt** esetében a dátumok mindig az egyes lapokon bejelentkezett felhasználó időzónájához viszonyítva jelennek meg, kivéve a **Feladat** lapot. Ha megtekinti a munkalebontási struktúrát, akkor a dátumok mindig a projekt időzónájában jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="66e68-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="66e68-108">Tevékenységek</span><span class="sxs-lookup"><span data-stu-id="66e68-108">Tasks</span></span>

<span data-ttu-id="66e68-109">A feladat létrehozásakor a kezdő időt, a záró időt és az órát/napot a projekt munkaideje szabályozza.</span><span class="sxs-lookup"><span data-stu-id="66e68-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="66e68-110">Ha például egy feladat egy olyan projekttel jön létre, amelynek időzónája -8 PST, és a következő munkaidővel rendelkezik: 9:00 – 17:00, hétfőtől péntekig, a hozzárendelés nélkül létrehozott bármely feladat tiszteletben tartja a projektnaptár kezdő időpontját és befejező időpontját.</span><span class="sxs-lookup"><span data-stu-id="66e68-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="66e68-111">Erőforrások kezelése időzónákkal</span><span class="sxs-lookup"><span data-stu-id="66e68-111">Manage resources with time zones</span></span>

<span data-ttu-id="66e68-112">A **Foglalás kiterjesztése** funkció használatakor a pontos és kiszámítható eredmény érdekében két alapvető követelménynek kell teljesülnie:</span><span class="sxs-lookup"><span data-stu-id="66e68-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="66e68-113">A felhasználónak konfigurálnia kell az eszköz időzónáját, hogy az megfeleljen a rendszer **Személyre szabási beállítások** részében megadott időzónának.</span><span class="sxs-lookup"><span data-stu-id="66e68-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Időzóna-beállítások a Windows 10 rendszerben](media/reconcile-assignments-03.png)

  ![Időzóna-beállítások a testreszabási beállításokban](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="66e68-116">A foglalható erőforrásnak legalább egy perc munkaidővel kell rendelkeznie, amely átfedésben van az elosztásokkal, amelyeket a kért hosszabbítás definiálásához használnak.</span><span class="sxs-lookup"><span data-stu-id="66e68-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="66e68-117">A következő erőforrások például 9:00 és 19:00 óra közötti munkaórákkal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="66e68-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Az erőforrás-eloszlások összehasonlítása](media/reconcile-assignments-05.png)

<span data-ttu-id="66e68-119">Az alábbi táblában a következők láthatók:</span><span class="sxs-lookup"><span data-stu-id="66e68-119">The following table shows:</span></span>

- <span data-ttu-id="66e68-120">Egy projektnaptársablon</span><span class="sxs-lookup"><span data-stu-id="66e68-120">A project calendar template</span></span>
- <span data-ttu-id="66e68-121">A erőforrás: Ennek az erőforrásnak ugyanaz a naptára, és ugyanabban az időzónában van, mint a projekt.</span><span class="sxs-lookup"><span data-stu-id="66e68-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="66e68-122">A foglalások kezdő időpontja 9:00 lesz.</span><span class="sxs-lookup"><span data-stu-id="66e68-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="66e68-123">B erőforrás: Ez az erőforrás a projekttől eltérő időzónában helyezkedik el, és 7:00 órakor kezdőd az időzónájában.</span><span class="sxs-lookup"><span data-stu-id="66e68-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="66e68-124">A foglalások azonban 9:00 órakor kezdődnek, mert ez a hozzárendelési felosztás legkorábbi kezdési időpontja.</span><span class="sxs-lookup"><span data-stu-id="66e68-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="66e68-125">C és D erőforrások: Az erőforrások különböző időzónákban találhatók, mindkettő eltér egymástól és a projektétől, és a foglalásuk a rendelkezésre álló kezdő időpontokhoz képest nem korábban kezdődik.</span><span class="sxs-lookup"><span data-stu-id="66e68-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="66e68-126">Entitás</span><span class="sxs-lookup"><span data-stu-id="66e68-126">Entity</span></span>  |<span data-ttu-id="66e68-127">Naptár</span><span class="sxs-lookup"><span data-stu-id="66e68-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="66e68-128">Projektnaptár-sablon</span><span class="sxs-lookup"><span data-stu-id="66e68-128">Project calendar template</span></span>   | ![projektnaptár](media/reconcile-assignments-06.png) |
|<span data-ttu-id="66e68-130">A erőforrás</span><span class="sxs-lookup"><span data-stu-id="66e68-130">Resource A</span></span>  | ![A erőforrás naptárja](media/reconcile-assignments-06.png) |
|<span data-ttu-id="66e68-132">B erőforrás</span><span class="sxs-lookup"><span data-stu-id="66e68-132">Resource B</span></span>  |  ![B erőforrás naptárja](media/reconcile-assignments-07.png) |
|<span data-ttu-id="66e68-134">C erőforrás</span><span class="sxs-lookup"><span data-stu-id="66e68-134">Resource C</span></span>  |  ![C erőforrás naptárja](media/reconcile-assignments-08.png) |
|<span data-ttu-id="66e68-136">D erőforrás</span><span class="sxs-lookup"><span data-stu-id="66e68-136">Resource D</span></span>  | ![D erőforrás naptárja](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="66e68-138">Amikor megnyitja az **Egyeztetés** nézetet, az erőforrás-hozzárendelések és a hozzájuk tartozó foglalási hiány jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="66e68-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Egyeztetési nézet a bővítés előtt](media/reconcile-assignments-10.png)

<span data-ttu-id="66e68-140">Miután minden erőforráshoz kiterjeszti a foglalási funkciót, a rendszer sikeresen kiterjeszti a foglalásokat az egyes erőforrások esetében, mivel az egyes erőforrások munkaideje átfedésben van a hiány kontúrjaival.</span><span class="sxs-lookup"><span data-stu-id="66e68-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Egyeztetési nézet a foglalás meghosszabbítása után](media/reconcile-assignments-11.png) 

<span data-ttu-id="66e68-142">Figyelje meg, hogy a foglalások részletes vizsgálata a foglalások kezdő időpontjában jelentkező különbségeket mutatja.</span><span class="sxs-lookup"><span data-stu-id="66e68-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="66e68-143">A foglalások legkorábban a hozzárendelési kontúrok kezdési időpontjában jelennek meg, és legkorábban az erőforrás rendelkezésre álló kezdési időpontjában.</span><span class="sxs-lookup"><span data-stu-id="66e68-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Erőforrások új foglalásai az ütemezési táblában](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]