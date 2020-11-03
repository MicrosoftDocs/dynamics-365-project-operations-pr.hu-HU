---
title: Frissítse a munka lebontási struktúrájával kapcsolatos szempontokat
description: Ez a témakör a munka bontási struktúrájának a Project Service Automation 2.x-ről a 3.x-re történő frissítéséről nyújt információkat.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 169dc24f0d1ae151ea5927123fb738221de88250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078174"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="05303-103">Frissítse a munka lebontási struktúrájával kapcsolatos szempontokat</span><span class="sxs-lookup"><span data-stu-id="05303-103">Upgrade considerations for the work breakdown structure</span></span>
<span data-ttu-id="05303-104">Ez a témakör a munka bontási struktúrájának a Project Service Automation 2.x-ről a 3.x-re történő frissítéséről nyújt információkat.</span><span class="sxs-lookup"><span data-stu-id="05303-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="05303-105">Ez a témakör a sikeres frissítéshez szükséges Project Service Automation (PSA) projekt egészségi állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="05303-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="05303-106">Információ van a közös blokkolási körülményekről is, amelyek miatt a frissítés meghiúsul.</span><span class="sxs-lookup"><span data-stu-id="05303-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="05303-107">A projektfeladatok és azok funkcióinak a projektütemezésen belüli meghatározásáról lásd: [Projektütemezések](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="05303-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="05303-108">Kulcsfontosságú entitások</span><span class="sxs-lookup"><span data-stu-id="05303-108">Key entities</span></span>
<span data-ttu-id="05303-109">A pontos, az erőforrásokkal már megterhelt munka bontási struktúrához a következő entitások szükségesek:</span><span class="sxs-lookup"><span data-stu-id="05303-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="05303-110">Projekt</span><span class="sxs-lookup"><span data-stu-id="05303-110">Project</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="05303-111">Projektcsoport</span><span class="sxs-lookup"><span data-stu-id="05303-111">Project Team</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="05303-112">Projektfeladat</span><span class="sxs-lookup"><span data-stu-id="05303-112">Project Task</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="05303-113">Erőforrás-hozzárendelések</span><span class="sxs-lookup"><span data-stu-id="05303-113">Resource Assignments</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="05303-114">Projektfeladat függősége</span><span class="sxs-lookup"><span data-stu-id="05303-114">Project Task Dependency</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="05303-115">Lefoglalható erőforrások</span><span class="sxs-lookup"><span data-stu-id="05303-115">Bookable Resources</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="05303-116">Az erőforrások által betöltött munka bontási struktúrájának meghatározásához a következő lépéseket kell végrehajtania:</span><span class="sxs-lookup"><span data-stu-id="05303-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="05303-117">Hozzon létre egy új projektet.</span><span class="sxs-lookup"><span data-stu-id="05303-117">Create a new project.</span></span> <span data-ttu-id="05303-118">További információ az új projekt létrehozásáról: [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="05303-118">For more information about how to create a new project, see [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="05303-119">Hozzon létre egy vagy több feladatot.</span><span class="sxs-lookup"><span data-stu-id="05303-119">Create one or more tasks.</span></span> <span data-ttu-id="05303-120">A feladat létrehozásával kapcsolatos további információkért lásd: [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="05303-120">For more information about how to create a task, see [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="05303-121">Határozza meg a feladat függőségeit.</span><span class="sxs-lookup"><span data-stu-id="05303-121">Define the task dependencies.</span></span> <span data-ttu-id="05303-122">További információ a [Projektfeladat függősége](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency) című témakörben olvasható.</span><span class="sxs-lookup"><span data-stu-id="05303-122">For more information, see [Project Task Dependency](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="05303-123">Jelölje ki a projekt csapattagjait.</span><span class="sxs-lookup"><span data-stu-id="05303-123">Assign project team members to the project.</span></span> <span data-ttu-id="05303-124">További információ: [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="05303-124">For more information, see [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="05303-125">Jelölje ki a projektcsoport tagjait a feladatokhoz.</span><span class="sxs-lookup"><span data-stu-id="05303-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="05303-126">További információ: [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="05303-126">For more information, see [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="05303-127">Projektcsapat-kapcsolatok</span><span class="sxs-lookup"><span data-stu-id="05303-127">Project team relationships</span></span>

<span data-ttu-id="05303-128">A sikeres frissítés biztosításához a következő kapcsolatokat kell megfelelően fenntartani:</span><span class="sxs-lookup"><span data-stu-id="05303-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="05303-129">A projektcsoport összes tagját hozzárendelni kell foglalható forráshoz.</span><span class="sxs-lookup"><span data-stu-id="05303-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="05303-130">A projektcsoport összes tagját azonos projekthez kell társítani.</span><span class="sxs-lookup"><span data-stu-id="05303-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="05303-131">Projekt feladat kapcsolatok</span><span class="sxs-lookup"><span data-stu-id="05303-131">Project task relationships</span></span>
<span data-ttu-id="05303-132">A sikeres frissítés biztosításához a következő kapcsolatokat kell megfelelően fenntartani:</span><span class="sxs-lookup"><span data-stu-id="05303-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="05303-133">Minden kapcsolódó feladatot ugyanahhoz a projekthez kell társítani.</span><span class="sxs-lookup"><span data-stu-id="05303-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="05303-134">Minden sorfeladatnak szülői feladattal kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="05303-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="05303-135">Minden feladatnak tartalmaznia kell egy szülői projektet.</span><span class="sxs-lookup"><span data-stu-id="05303-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="05303-136">Érvényes feltételek</span><span class="sxs-lookup"><span data-stu-id="05303-136">Valid conditions</span></span>

- <span data-ttu-id="05303-137">Az összes feladat időtartamának legalább egy óránnak (>=) vagy azzal egyenlőnek kell lennie, és kevesebbnek kell lennie 1 800 000 percnél (1250 nap).\*</span><span class="sxs-lookup"><span data-stu-id="05303-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="05303-138">Minden feladatnak legkorábban 2000/01/01 kezdő dátummal kell rendelkeznie.\*</span><span class="sxs-lookup"><span data-stu-id="05303-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="05303-139">Minden feladatnak legkésőbb a mai naptól számított 17 éven belüli kezdő dátummal kell rendelkeznie.\*</span><span class="sxs-lookup"><span data-stu-id="05303-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="05303-140">Minden feladatnak a kezdési dátummal korábban vagy azzal egyenlőnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="05303-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="05303-141">Az osztályozásban szereplő összes tranzakciótípusnak (költség, anyag, adó és idő) a következőknek kell lennie: **Alapértelmezett egység** és **Egységcsoport**.</span><span class="sxs-lookup"><span data-stu-id="05303-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="05303-142">Kerülni kell a betűkkel ellátott dátumformátumot.</span><span class="sxs-lookup"><span data-stu-id="05303-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="05303-143">Potenciális kockázatcsökkentési lépések</span><span class="sxs-lookup"><span data-stu-id="05303-143">Potential mitigation steps</span></span>
- <span data-ttu-id="05303-144">Az Irányított keresés segítségével azonosíthatja projektazonosítót nem tartalmazó projekttevékenységeket.</span><span class="sxs-lookup"><span data-stu-id="05303-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="05303-145">Az Irányított keresés segítségével azonosíthatók azok a projekttevékenységek, amelyeknél az ütemezett időtartam nagyobb, mint 1 800 000.</span><span class="sxs-lookup"><span data-stu-id="05303-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="05303-146">Az adatok módosítása előtt meg kell vizsgálnia az entitáshoz kapcsolódó testreszabásokat, amelyek ahhoz vezethettek, hogy az adatok hibás állapotba kerültek.</span><span class="sxs-lookup"><span data-stu-id="05303-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="05303-147">Ezeket a testreszabásokat kezelni kell az adatokkal kapcsolatos bármilyen frissítések végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="05303-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="05303-148">Az azonosított árva feladatok esetében érdemes lehet törölni ezeket a feladatokat, ha nem szükségesek, vagy a megfelelő fölérendelt projekthez kell azokat társítani.</span><span class="sxs-lookup"><span data-stu-id="05303-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="05303-149">Minden olyan feladat esetében, ahol az időtartam nagyobb, mint 1250 nap, érdemes több feladatot is felvenni, amelyek kitöltik a teljes időtartamot, ha ez megoldható.</span><span class="sxs-lookup"><span data-stu-id="05303-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="05303-150">A csillaggal (\*) megjelölt elemeknek vannak olyan korlátai, amelyek annak a ténynek a következményei, hogy az ügyfélkapcsolat-kezelés (CRM) csak 7320 ismétlődési kiterjesztést támogat.</span><span class="sxs-lookup"><span data-stu-id="05303-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="05303-151">Ezen határ alatt kell maradnia.</span><span class="sxs-lookup"><span data-stu-id="05303-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="05303-152">Erőforrás-hozzárendelési kapcsolatok</span><span class="sxs-lookup"><span data-stu-id="05303-152">Resource Assignment relationships</span></span>
<span data-ttu-id="05303-153">A sikeres frissítés biztosításához a következő kapcsolatokat kell megfelelően fenntartani:</span><span class="sxs-lookup"><span data-stu-id="05303-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="05303-154">A munkabontási struktúrában szereplő összes erőforrás-hozzárendelésnek ugyanabba a projekthez kell kapcsolódnia.</span><span class="sxs-lookup"><span data-stu-id="05303-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="05303-155">A munkabontási struktúrában szereplő összes erőforrás-hozzárendelést társítani kell a projektcsoport tagjaihoz ugyanabban a projektben.</span><span class="sxs-lookup"><span data-stu-id="05303-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="05303-156">Potenciális kockázatcsökkentési lépések</span><span class="sxs-lookup"><span data-stu-id="05303-156">Potential mitigation steps</span></span>
- <span data-ttu-id="05303-157">Azonosítsa az összes olyan feladatot, amely kívül esik a fent leírt feltételeken.</span><span class="sxs-lookup"><span data-stu-id="05303-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="05303-158">A már nem érvényes erőforrás-hozzárendeléseket törölni kell.</span><span class="sxs-lookup"><span data-stu-id="05303-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="05303-159">Projektfeladat-függőségi viszonyok</span><span class="sxs-lookup"><span data-stu-id="05303-159">Project task dependency relationships</span></span>
<span data-ttu-id="05303-160">A sikeres frissítés biztosításához a következő kapcsolatokat kell megfelelően fenntartani:</span><span class="sxs-lookup"><span data-stu-id="05303-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="05303-161">Az összes projektfeladat-függőségnek ugyanahhoz a projekthez kell kapcsolódnia.</span><span class="sxs-lookup"><span data-stu-id="05303-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="05303-162">Egy feladatnak nem lehet ugyanaz a függősége, többször hivatkozva.</span><span class="sxs-lookup"><span data-stu-id="05303-162">A task can't have the same dependency referenced more than once.</span></span>
