---
title: Projekt ütemezése munkalebontási szerkezettel
description: Projekt ütemezése munkalebontási struktúrával a Project Service szolgáltatásban
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ca9b899c-7791-4990-b02e-cdff7f652621
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 003a1c543163b7ef1df1221d0b633a078e6619cf
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752274"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="bcbec-103">Projekt ütemezése munkalebontási struktúrával (Project Service)</span><span class="sxs-lookup"><span data-stu-id="bcbec-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="bcbec-104">A projektütemterv adja meg, hogy milyen munkát kell végezni, milyen erőforrások végzik a munkát és az időkeretet, amelyben a munkát el kell végezni.</span><span class="sxs-lookup"><span data-stu-id="bcbec-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="bcbec-105">A projekt ütemterv tükrözi az összes projekt elküldésével időben társított munkát.</span><span class="sxs-lookup"><span data-stu-id="bcbec-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="bcbec-106">A projekt kezdeményezési szakaszában az első lépések egyike egy projekt ütemezéssel kell együtt megjelennie.</span><span class="sxs-lookup"><span data-stu-id="bcbec-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="bcbec-107">Egy projektütemezés létrehozásásához, egy munkalebontási szerkezetet kell létrehoznia.</span><span class="sxs-lookup"><span data-stu-id="bcbec-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="bcbec-108">Hozzon létre munkalebontási szerkezettel rendelkező projekt ütemezést, amely segít :</span><span class="sxs-lookup"><span data-stu-id="bcbec-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="bcbec-109">Bontsa le a munkát kezelhető feladatokra</span><span class="sxs-lookup"><span data-stu-id="bcbec-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="bcbec-110">Végezze el a feladat befejezéséhez szükséges idő becslését</span><span class="sxs-lookup"><span data-stu-id="bcbec-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="bcbec-111">Állítsa be függőségeket és feladat időtartamát</span><span class="sxs-lookup"><span data-stu-id="bcbec-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="bcbec-112">Határozza meg az egyes feladatok elvégzéséhez szükséges szerepeket</span><span class="sxs-lookup"><span data-stu-id="bcbec-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="bcbec-113">A projekt ütemtervét a munkalebontási szerkezetben a projekt ütemezésnek ismert megjelenése és működése van, egy interaktív Gantt-diagrammal végezze el a befejezését.</span><span class="sxs-lookup"><span data-stu-id="bcbec-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="bcbec-114">Hozzon létre a projekt számára munkalebontási struktúrát</span><span class="sxs-lookup"><span data-stu-id="bcbec-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="bcbec-115">Hozzon létre munkalebontási szerkezetet a projektben a feladatok sorozatának jelképezéséhez.</span><span class="sxs-lookup"><span data-stu-id="bcbec-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="bcbec-116">A munkalebontási szerkezet tartalmazza a tevékenységeket, követelményeket minden egyes tevékenység számára, és a bevétel-és költségadatokat.</span><span class="sxs-lookup"><span data-stu-id="bcbec-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="bcbec-117">A munkalebontási szerkezetben megadhatja:</span><span class="sxs-lookup"><span data-stu-id="bcbec-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="bcbec-118">A hierarchiában a tevékenységek sorozata</span><span class="sxs-lookup"><span data-stu-id="bcbec-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="bcbec-119">Az egyéb tevékenységeket – ha, van ilyen – el kell végezni egy feladat elindítása előtt.</span><span class="sxs-lookup"><span data-stu-id="bcbec-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="bcbec-120">A kezdő dátum, záró dátum, és a tevékenység időtartama</span><span class="sxs-lookup"><span data-stu-id="bcbec-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="bcbec-121">A feladathoz szükséges órák száma</span><span class="sxs-lookup"><span data-stu-id="bcbec-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="bcbec-122">Bármely szükséges munkavállalói képesség és oktatás</span><span class="sxs-lookup"><span data-stu-id="bcbec-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="bcbec-123">A munkavállalók, akik hozzá vannak rendelve a tevékenységhez</span><span class="sxs-lookup"><span data-stu-id="bcbec-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="bcbec-124">Becsült árbevétel és költségek</span><span class="sxs-lookup"><span data-stu-id="bcbec-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="bcbec-125">Feladattípusok</span><span class="sxs-lookup"><span data-stu-id="bcbec-125">Task types</span></span>  
<span data-ttu-id="bcbec-126">A következő típusú feladatokat fogja használni, a munkalebontási szerkezet létrehozásakor:</span><span class="sxs-lookup"><span data-stu-id="bcbec-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="bcbec-127">**Projekt gyökércsomópontja**</span><span class="sxs-lookup"><span data-stu-id="bcbec-127">**Project root node**</span></span> | <span data-ttu-id="bcbec-128">A felső szintű összefoglaló tevékenység a projekt számára.</span><span class="sxs-lookup"><span data-stu-id="bcbec-128">The top-level summary task for the project.</span></span> <span data-ttu-id="bcbec-129">Minden más projekttevékenység ez alapján jönnek létre.</span><span class="sxs-lookup"><span data-stu-id="bcbec-129">All other project tasks are created under it.</span></span> <span data-ttu-id="bcbec-130">A legfelső szintű gyökér tevékenység neve a projekt neve.</span><span class="sxs-lookup"><span data-stu-id="bcbec-130">The name of the root task is the project name.</span></span> <span data-ttu-id="bcbec-131">Az erőkifejtés, a dátumok és a gyökércsomópont időtartama a hierarchiában lenn található értékeken alapulnak.</span><span class="sxs-lookup"><span data-stu-id="bcbec-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="bcbec-132">Nem módosíthatja a gyökér csomópont tulajdonságait vagy törölheti a gyökér csomópontot.</span><span class="sxs-lookup"><span data-stu-id="bcbec-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="bcbec-133">**Összefoglaló vagy tárolófeladatok**</span><span class="sxs-lookup"><span data-stu-id="bcbec-133">**Summary or container tasks**</span></span> | <span data-ttu-id="bcbec-134">Összefoglaló tevékenység az a tevékenység, amely alatta altevékenységekkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="bcbec-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="bcbec-135">Az összefoglaló tevékenység nem rendelkezik semmilyen munka erőkifejtéssel vagy saját költséggel.</span><span class="sxs-lookup"><span data-stu-id="bcbec-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="bcbec-136">A munka erőfeszítés és költség az altevékenységeinek összesítése.</span><span class="sxs-lookup"><span data-stu-id="bcbec-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="bcbec-137">Módosíthatja az összefoglaló tevékenység nevét, de nem módosíthatja az erőkifejtést, a dátumokat, vagy az időtartamot, mert azokat automatikusan számítják ki.</span><span class="sxs-lookup"><span data-stu-id="bcbec-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="bcbec-138">Az összegző tevékenység törlésével törlődik a feladat és az összes altevékenysége.</span><span class="sxs-lookup"><span data-stu-id="bcbec-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="bcbec-139">**Levélcsomópont-feladatok**</span><span class="sxs-lookup"><span data-stu-id="bcbec-139">**Leaf node tasks**</span></span> | <span data-ttu-id="bcbec-140">A levél csomópont feladat jelöli a legrészletesebb munkát a projekten.</span><span class="sxs-lookup"><span data-stu-id="bcbec-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="bcbec-141">Becsült erőkifejtéssel, az erőforrások tervezett számával, tervezett kezdési és befejezési dátummal és időtartammal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="bcbec-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="bcbec-142">Feladat hierarchia</span><span class="sxs-lookup"><span data-stu-id="bcbec-142">Task hierarchy</span></span>  
 <span data-ttu-id="bcbec-143">Feladat hierarchia létrehozásakor a következő lehetőségei vannak:</span><span class="sxs-lookup"><span data-stu-id="bcbec-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="bcbec-144">**Feladat hozzáadása**.</span><span class="sxs-lookup"><span data-stu-id="bcbec-144">**Add task**.</span></span>   <span data-ttu-id="bcbec-145">Egy pozícióban hozzáadhat egy feladatot, amelyet a feladat hierarchiában választ ki.</span><span class="sxs-lookup"><span data-stu-id="bcbec-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="bcbec-146">Ha nem ad meg egy helyet, az új tevékenység végén jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="bcbec-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="bcbec-147">**Tevékenység behúzása**.</span><span class="sxs-lookup"><span data-stu-id="bcbec-147">**Indent task**.</span></span>   <span data-ttu-id="bcbec-148">Tervezzen meg egy feladatot a feladat utóda létrehozásához közvetlenül felette.</span><span class="sxs-lookup"><span data-stu-id="bcbec-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="bcbec-149">**Tevékenység kihúzása**.</span><span class="sxs-lookup"><span data-stu-id="bcbec-149">**Outdent task**.</span></span>   <span data-ttu-id="bcbec-150">Húzza ki egy tevékenységet ahhoz, hogy az eredeti szülő feladata altevékenységek ne legyen tovább érvényes.</span><span class="sxs-lookup"><span data-stu-id="bcbec-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="bcbec-151">**Mozgatás fel és Mozgatás le**.</span><span class="sxs-lookup"><span data-stu-id="bcbec-151">**Move up and Move down**.</span></span>   <span data-ttu-id="bcbec-152">Mozgassa fel és le a tevékenységeket a szülő feladata hierarchiájában.</span><span class="sxs-lookup"><span data-stu-id="bcbec-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="bcbec-153">Tevékenység felfelé vagy lefelé helyezéséhez nem befolyásolja az erőforrást, a költséget, a dátumokat vagy az időtartamot.</span><span class="sxs-lookup"><span data-stu-id="bcbec-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="bcbec-154">Feladat attribútumok</span><span class="sxs-lookup"><span data-stu-id="bcbec-154">Task attributes</span></span>  
 <span data-ttu-id="bcbec-155">A tevékenység neve leírja az elvégzendő munkát.</span><span class="sxs-lookup"><span data-stu-id="bcbec-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="bcbec-156">Különböző feladat attribútumok segítségével leírhatja a feladathoz az ütemezést és a munkaerő-szükségletet.</span><span class="sxs-lookup"><span data-stu-id="bcbec-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="bcbec-157">Attribútumok ütemezése</span><span class="sxs-lookup"><span data-stu-id="bcbec-157">Schedule attributes</span></span>

 - <span data-ttu-id="bcbec-158">Értékek hozzárendelése **Munkaórákhoz**, **Erőforrások számához**, **Kezdő dátumhoz**, **Befejezési dátumhoz**, és **időtartamhoz** a feladat ütemezésének meghatározása érdekében.</span><span class="sxs-lookup"><span data-stu-id="bcbec-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="bcbec-159">**Erőfeszítés** a feladat elvégzéséhez szükséges órák becsült értéke.</span><span class="sxs-lookup"><span data-stu-id="bcbec-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="bcbec-160">**Erőforrások száma** egy becslés, amit a projekt menedzser a feladatba juttat annak érdekében, hogy a lehető legjobb ütemezést eredményezze.</span><span class="sxs-lookup"><span data-stu-id="bcbec-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="bcbec-161">**Időtartam** (napokban) jelzi azon munka napok számát, amely a feladat végrehajtásához szükséges.</span><span class="sxs-lookup"><span data-stu-id="bcbec-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="bcbec-162">Munkaerő-attribútumok</span><span class="sxs-lookup"><span data-stu-id="bcbec-162">Staffing attributes</span></span>

 - <span data-ttu-id="bcbec-163">**Szerepkör**, **Erőforrás szervezeti egység**, **Erőforrások száma**, és **Erőforrások** leírják a munkaerő-szükségleteit a feladat számára.</span><span class="sxs-lookup"><span data-stu-id="bcbec-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="bcbec-164">**Szerepkör** leírja a feladat elvégzéséhez szükséges erőforrások típusát.</span><span class="sxs-lookup"><span data-stu-id="bcbec-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="bcbec-165">**Erőforrás szervezeti egység** jelzi, hogy a szervezeti egységet, amelyből az erőforrásokat személyzettel kell ellátni a tevékenység számára, ami hatással van a feladat költségi- és az értékesítési becslésére, mivel az erőforráshoz tartozó egység költségi árának meghatározását igazolja.</span><span class="sxs-lookup"><span data-stu-id="bcbec-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="bcbec-166">**Erőforrások** tartalmazza az általános erőforrást vagy elnevezett erőforrást, amikor talál egyet.</span><span class="sxs-lookup"><span data-stu-id="bcbec-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="bcbec-167">Tevékenység függőségek</span><span class="sxs-lookup"><span data-stu-id="bcbec-167">Task dependencies</span></span>  
 <span data-ttu-id="bcbec-168">A munkalebontási szerkezetben lévő egy vagy több tevékenységei között megelőző kapcsolatokat hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="bcbec-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="bcbec-169">A feladathoz tartozó megelőző mező számára egy vagy több értéket állíthat be annak érdekében, hogy jelezze a tevékenységeket, amelyek rá vannak utalva.</span><span class="sxs-lookup"><span data-stu-id="bcbec-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="bcbec-170">Amikor hozzárendel a tevékenységhez egy megelőző értéket, a feladat csak akkor indulhat el, amikor az összes megelőző tevékenység befejeződött.</span><span class="sxs-lookup"><span data-stu-id="bcbec-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="bcbec-171">A feladaton a függőség beállítása a feladat tervezett kezdeti dátum újraszámítást az összes előzmény legutolsó végeként eredményezi.</span><span class="sxs-lookup"><span data-stu-id="bcbec-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="bcbec-172">Az ütemezés megelőző jellegű hatásai nincsenek korlátozva a feladaton meghatározott feladat mód által.</span><span class="sxs-lookup"><span data-stu-id="bcbec-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="bcbec-173">Tevékenység mód</span><span class="sxs-lookup"><span data-stu-id="bcbec-173">Task mode</span></span>  
 <span data-ttu-id="bcbec-174">Tevékenység ütemezése azon fontos tényezők egyik, amelyek meghatározzák a levél csomópont feladatok ütemezése.</span><span class="sxs-lookup"><span data-stu-id="bcbec-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="bcbec-175">Kétféle feladat mód tartozik minden egyes feladathoz: automatikus és kézi ütemezési mód..</span><span class="sxs-lookup"><span data-stu-id="bcbec-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="bcbec-176">**Automatikus ütemezés**.</span><span class="sxs-lookup"><span data-stu-id="bcbec-176">**Auto scheduling**.</span></span>   <span data-ttu-id="bcbec-177">Amikor Automatikusan ütemezett módra állítja a feladatot, a feladatütemezési eszköz a következő feladatattribútumokra alkalmazza az ütemezési szabályokat, annak érdekében, hogy meghatározza az ütemezést a feladat számára:</span><span class="sxs-lookup"><span data-stu-id="bcbec-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="bcbec-178">Megelőző tevékenységek</span><span class="sxs-lookup"><span data-stu-id="bcbec-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="bcbec-179">Erőfeszítés</span><span class="sxs-lookup"><span data-stu-id="bcbec-179">Effort</span></span>  
  
    -   <span data-ttu-id="bcbec-180">Erőforrások száma</span><span class="sxs-lookup"><span data-stu-id="bcbec-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="bcbec-181">Kezdő és befejező dátumok</span><span class="sxs-lookup"><span data-stu-id="bcbec-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="bcbec-182">**Ütemezési szabályok**.</span><span class="sxs-lookup"><span data-stu-id="bcbec-182">**Scheduling rules**.</span></span>   <span data-ttu-id="bcbec-183">Egy olyan levélcsomópont-feladat kezdő dátuma, amely nem rendelkezik előzményekkel, alapértelmezés szerint a projekt ütemezett kezdő dátuma lesz.</span><span class="sxs-lookup"><span data-stu-id="bcbec-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="bcbec-184">Egy levélcsomópont tevékenység időtartamot mindig a kezdő és befejezési dátumok közötti napok száma szerint számítják ki.</span><span class="sxs-lookup"><span data-stu-id="bcbec-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="bcbec-185">Amikor a rendszer automatikusan beütemez egy feladatot, az ütemezési motor az alábbi szabályokat követi:</span><span class="sxs-lookup"><span data-stu-id="bcbec-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="bcbec-186">A feladat kezdő és záró dátumainak mindig munkanapoknak kell lennie a projektütemezési naptár szerint</span><span class="sxs-lookup"><span data-stu-id="bcbec-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="bcbec-187">Az előzményekkel rendelkező feladat kezdő dátuma alapértelmezés szerint az előzmény legutóbbi záró dátuma.</span><span class="sxs-lookup"><span data-stu-id="bcbec-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="bcbec-188">Tevékenység = Személyek száma *Időtartam* a projektnaptárban megjelenő szokásos munkanapok órái</span><span class="sxs-lookup"><span data-stu-id="bcbec-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="bcbec-189">**Kézi ütemezés**.</span><span class="sxs-lookup"><span data-stu-id="bcbec-189">**Manual scheduling**.</span></span>   <span data-ttu-id="bcbec-190">Bizonyos esetekben érdemes lehet eltérni ezektől a szabályoktól.</span><span class="sxs-lookup"><span data-stu-id="bcbec-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="bcbec-191">Ezekben az esetekben beállíthatja a tevékenységi módot a manuálisan ütemezendő feladat számára.</span><span class="sxs-lookup"><span data-stu-id="bcbec-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="bcbec-192">Ez leállítja az ütemezési motort a többi ütemezési attribútum értékeinek kiszámításából.</span><span class="sxs-lookup"><span data-stu-id="bcbec-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="bcbec-193">A tevékenység megelőző tevékenységek mindig befolyásolják a függő tevékenység kezdési dátumát.</span><span class="sxs-lookup"><span data-stu-id="bcbec-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="bcbec-194">Hozzon létre a projekt számára munkalebontási struktúrát</span><span class="sxs-lookup"><span data-stu-id="bcbec-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="bcbec-195">Lépjen a **Project Service > Projektek** pontba.</span><span class="sxs-lookup"><span data-stu-id="bcbec-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="bcbec-196">Kattintson arra a projektre, amellyel dolgozni szeretne.</span><span class="sxs-lookup"><span data-stu-id="bcbec-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="bcbec-197">A képernyő felső részén található sávon válassza ki a projekt neve melletti, lefelé mutató nyilat, majd kattintson a Munkalebontási struktúra lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="bcbec-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="bcbec-198">Feladat hozzáadásához kattintson a **Feladat hozzáadása**.</span><span class="sxs-lookup"><span data-stu-id="bcbec-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="bcbec-199">Töltse ki a kötelező mezőket a feladathoz, és kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="bcbec-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="bcbec-200">Folytassa a tevékenységek hozzáadásával, amíg befejeződik a munkalebontási szerkezet.</span><span class="sxs-lookup"><span data-stu-id="bcbec-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="bcbec-201">A munkalebontási szerkezet létrehozásakor a következőket teheti a feladatok rendszerezése érdekében:</span><span class="sxs-lookup"><span data-stu-id="bcbec-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="bcbec-202">Jelöljön ki egy tevékenységet, és kattintson a **Behúzás** lehetőségre annak érdekében, hogy egy másik tevékenység alá helyezze, vagy kattintson a Kihúzás elemre a szintből történő kihúzás érdekében.</span><span class="sxs-lookup"><span data-stu-id="bcbec-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="bcbec-203">Jelöljön ki egy feladatot, és kattintson a **Mozgatás fel** vagy **Mozgatás Le** lehetőségre a listában történő fel- és lemozgatáshoz.</span><span class="sxs-lookup"><span data-stu-id="bcbec-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="bcbec-204">Kattintson a **Gantt elrejtése** elemre a Gantt diagram elrejtéséhez, majd kattintson a **Gantt megjelenítése** elemre az újbóli megjelenítéshez.</span><span class="sxs-lookup"><span data-stu-id="bcbec-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="bcbec-205">Jelöljön ki a Gantt-diagram számára egy másik időszakot az **Időskála**mezőben.</span><span class="sxs-lookup"><span data-stu-id="bcbec-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="bcbec-206">A munkalebontási struktúrában megadott szerepek projekt csapattagokhoz való hozzáadásához kattintson a **Projektcsoport létrehozása**lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="bcbec-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="bcbec-207">Ha elkészült a módosításokkal, kattintson a **Mentés** lehetőségre a képernyő jobb alsó sarkában.</span><span class="sxs-lookup"><span data-stu-id="bcbec-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="bcbec-208">Kapcsolódó információk</span><span class="sxs-lookup"><span data-stu-id="bcbec-208">See Also</span></span>  
 [<span data-ttu-id="bcbec-209">Projektmenedzseri útmutató</span><span class="sxs-lookup"><span data-stu-id="bcbec-209">Project manager guide</span></span>](../project-service/project-manager-guide.md)
