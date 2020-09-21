---
title: Projekt ütemezése
description: Ez a témakör információt nyújt az ütemezés létrehozásáról.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 10e8f8aa-ddfb-4626-b936-86f054808dc2
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: e6c259677fbc43e2e6087e013955f156ae2dac4e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752205"
---
# <a name="project-schedules"></a><span data-ttu-id="9acc7-103">Projekt ütemezése</span><span class="sxs-lookup"><span data-stu-id="9acc7-103">Project schedules</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9acc7-104">A projekt ütemezése ismerteti, hogy milyen munkát kell elvégezni, mely erőforrások fogják elvégezni a munkát, és azt az időkeretet, amelyen belül a munkát be kell fejezni.</span><span class="sxs-lookup"><span data-stu-id="9acc7-104">A project schedule communicates what work must be completed, which resources will do the work, and the timeframe that the work must be finished in.</span></span> <span data-ttu-id="9acc7-105">Ez az összes olyan munkát tükrözi, amely a projekt időben történő végrehajtásával jár.</span><span class="sxs-lookup"><span data-stu-id="9acc7-105">It reflects all the work that is associated with delivering the project on time.</span></span> <span data-ttu-id="9acc7-106">A Dynamics 365 Project Service Automation szolgáltatásban úgy hozható létre a projekt ütemezése, hogy a munkát kezelhető feladatokra bontja, megbecsüli az egyes feladatok elvégzéséhez szükséges időt, beállítja a feladat függőségeit, a feladat időtartamát, és megbecsüli a feladatokat végrehajtó általános erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="9acc7-106">In Dynamics 365 Project Service Automation, you create a project schedule by breaking the work down into manageable tasks, estimating the time that is required to do each task, setting task dependencies, setting task durations, and estimating the generic resources that will do the tasks.</span></span> <span data-ttu-id="9acc7-107">A projekt ütemezése a projektoldal **Ütemezés** lapján jön létre.</span><span class="sxs-lookup"><span data-stu-id="9acc7-107">The project schedule is created on the **Schedule** tab of the project page.</span></span>
 
## <a name="tasks"></a><span data-ttu-id="9acc7-108">Feladatok</span><span class="sxs-lookup"><span data-stu-id="9acc7-108">Tasks</span></span>

<span data-ttu-id="9acc7-109">A projekt ütemezésének létrehozásakor az első lépés a munka kezelhető részekre bontása.</span><span class="sxs-lookup"><span data-stu-id="9acc7-109">The first step in creating a project schedule is to break the work down into manageable portions.</span></span> <span data-ttu-id="9acc7-110">A PSA ütemezése a következő szolgáltatásokat támogatja:</span><span class="sxs-lookup"><span data-stu-id="9acc7-110">The schedule in PSA supports the following features:</span></span>

- <span data-ttu-id="9acc7-111">Projekt gyökércsomópontja</span><span class="sxs-lookup"><span data-stu-id="9acc7-111">Project root node</span></span>
- <span data-ttu-id="9acc7-112">Összefoglaló vagy tárolófeladatok</span><span class="sxs-lookup"><span data-stu-id="9acc7-112">Summary or container tasks</span></span>
- <span data-ttu-id="9acc7-113">Levélcsomópont-feladatok</span><span class="sxs-lookup"><span data-stu-id="9acc7-113">Leaf node tasks</span></span>

### <a name="project-root-node"></a><span data-ttu-id="9acc7-114">Projekt gyökércsomópontja</span><span class="sxs-lookup"><span data-stu-id="9acc7-114">Project root node</span></span>

<span data-ttu-id="9acc7-115">A projekt gyökércsomópontja a projekt legfelső szintű összefoglaló feladata.</span><span class="sxs-lookup"><span data-stu-id="9acc7-115">The project root node is the top-level summary task for the project.</span></span> <span data-ttu-id="9acc7-116">Minden más projekttevékenység ez alapján jönnek létre.</span><span class="sxs-lookup"><span data-stu-id="9acc7-116">All other project tasks are created under it.</span></span> <span data-ttu-id="9acc7-117">A gyökércsomópont nevét mindig a projekt nevére állítják be.</span><span class="sxs-lookup"><span data-stu-id="9acc7-117">The name of the root node is always set to the project name.</span></span> <span data-ttu-id="9acc7-118">A gyökércsomópont erőfeszítéseit, dátumait és időtartamát az alatta lévő hierarchia értékei alapján összegzik.</span><span class="sxs-lookup"><span data-stu-id="9acc7-118">The effort, dates, and duration of the root node are summarized based on the values in the hierarchy below it.</span></span> <span data-ttu-id="9acc7-119">A gyökércsomópont tulajdonságait nem szerkesztheti.</span><span class="sxs-lookup"><span data-stu-id="9acc7-119">You can't edit the properties of the root node.</span></span> <span data-ttu-id="9acc7-120">A gyökércsomópontot nem is törölheti.</span><span class="sxs-lookup"><span data-stu-id="9acc7-120">You also can't delete the root node.</span></span>

### <a name="summary-or-container-tasks"></a><span data-ttu-id="9acc7-121">Összefoglaló vagy tárolófeladatok</span><span class="sxs-lookup"><span data-stu-id="9acc7-121">Summary or container tasks</span></span> 

<span data-ttu-id="9acc7-122">Az összefoglaló feladatok alfeladatokkal vagy tároló feladatokkal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="9acc7-122">Summary tasks have sub-tasks or container tasks under them.</span></span> <span data-ttu-id="9acc7-123">Nem rendelkeznek erőfeszítéssel vagy költségekkel.</span><span class="sxs-lookup"><span data-stu-id="9acc7-123">They have no work effort or cost of their own.</span></span> <span data-ttu-id="9acc7-124">Ehelyett erőfeszítéseik és költségeik a tároló feladatok erőfeszítéseinek és költségeinek összegét jelentik.</span><span class="sxs-lookup"><span data-stu-id="9acc7-124">Instead, their work effort and cost are a rollup of the work effort and cost of their container tasks.</span></span> <span data-ttu-id="9acc7-125">Az összefoglaló feladat kezdő dátuma a tároló feladatok kezdő dátuma, a befejező dátum pedig a tároló feladatok befejező dátuma.</span><span class="sxs-lookup"><span data-stu-id="9acc7-125">The start date of the summary task is the start date of the container tasks, and the end date is the end date of the container tasks.</span></span> <span data-ttu-id="9acc7-126">Az összefoglaló feladat neve szerkeszthető, de az ütemezési tulajdonságok (erőfeszítés, dátumok és időtartam) nem szerkeszthetők.</span><span class="sxs-lookup"><span data-stu-id="9acc7-126">The name of a summary task can be edited, but scheduling properties (effort, dates, and duration) can't be edited.</span></span> <span data-ttu-id="9acc7-127">Ha töröl egy összefoglaló feladatot, akkor törli az összes tároló feladatot.</span><span class="sxs-lookup"><span data-stu-id="9acc7-127">If you delete a summary task, you also delete all its container tasks.</span></span>

### <a name="leaf-node-tasks"></a><span data-ttu-id="9acc7-128">Levélcsomópont-feladatok</span><span class="sxs-lookup"><span data-stu-id="9acc7-128">Leaf node tasks</span></span>

<span data-ttu-id="9acc7-129">A levélcsomópont-feladatok képviselik a projekt legrészletesebb munkáját.</span><span class="sxs-lookup"><span data-stu-id="9acc7-129">Leaf node tasks represent the most granular work on the project.</span></span> <span data-ttu-id="9acc7-130">Becsült erőfeszítéssel, erőforrásokkal, tervezett kezdési és befejezési dátummal, valamint időtartammal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="9acc7-130">They have an estimated effort, resources, planned start and end dates, and a duration.</span></span>
 
## <a name="creating-a-task-hierarchy"></a><span data-ttu-id="9acc7-131">Feladathierarchia létrehozása</span><span class="sxs-lookup"><span data-stu-id="9acc7-131">Creating a task hierarchy</span></span>

<span data-ttu-id="9acc7-132">A következő lehetőségekkel hozhat létre feladathierarchiát:</span><span class="sxs-lookup"><span data-stu-id="9acc7-132">You can create a task hierarchy by using the following options:</span></span>

- <span data-ttu-id="9acc7-133">**Feladat hozzáadása** gomb</span><span class="sxs-lookup"><span data-stu-id="9acc7-133">**Add task** button</span></span>
- <span data-ttu-id="9acc7-134">**Feladat behúzása** gomb</span><span class="sxs-lookup"><span data-stu-id="9acc7-134">**Indent task** button</span></span>
- <span data-ttu-id="9acc7-135">**Feladat kihúzása** gomb</span><span class="sxs-lookup"><span data-stu-id="9acc7-135">**Outdent task** button</span></span>
- <span data-ttu-id="9acc7-136">**Mozgatás felfelé** és **Mozgatás lefelé** gombok</span><span class="sxs-lookup"><span data-stu-id="9acc7-136">**Move up** and **Move down** buttons</span></span>
- <span data-ttu-id="9acc7-137">Kisegítő lehetőségek és billentyűparancsok</span><span class="sxs-lookup"><span data-stu-id="9acc7-137">Accessibility and keyboard shortcuts</span></span>

### <a name="add-task"></a><span data-ttu-id="9acc7-138">Feladat hozzáadása</span><span class="sxs-lookup"><span data-stu-id="9acc7-138">Add task</span></span>

<span data-ttu-id="9acc7-139">A **Feladat hozzáadása** gomb segítségével új feladatot hozhat létre a hierarchiában.</span><span class="sxs-lookup"><span data-stu-id="9acc7-139">The **Add task** button lets you create a new task in the hierarchy.</span></span> <span data-ttu-id="9acc7-140">Ha nem választja ki a pozíciót, akkor a feladat a végén kerül beillesztésre.</span><span class="sxs-lookup"><span data-stu-id="9acc7-140">If you don't select a position, the task is inserted at the end.</span></span> 

<span data-ttu-id="9acc7-141">Minden feladathoz tartozik ütemezésazonosító.</span><span class="sxs-lookup"><span data-stu-id="9acc7-141">A schedule ID is assigned to every task.</span></span> <span data-ttu-id="9acc7-142">Az ütemezésazonosító azonosítja a feladat mélységét és helyét a hierarchiában.</span><span class="sxs-lookup"><span data-stu-id="9acc7-142">The schedule ID represents the task's depth and position in the hierarchy.</span></span> <span data-ttu-id="9acc7-143">Vázlatos számozást használ.</span><span class="sxs-lookup"><span data-stu-id="9acc7-143">It uses outline numbering.</span></span> <span data-ttu-id="9acc7-144">Az első szintű feladatokhoz a projekt gyökércsomópontja alatt az 1, 2, 3 stb. számozási séma kerül felhasználásra.</span><span class="sxs-lookup"><span data-stu-id="9acc7-144">For tasks in the first level under the project root node, a numbering scheme of 1, 2, 3, and so on, is used.</span></span> <span data-ttu-id="9acc7-145">Az első szint alatti feladatokhoz az 1.1, 1.2, 1.3 stb. számozási séma kerül felhasználásra.</span><span class="sxs-lookup"><span data-stu-id="9acc7-145">For tasks under the first level, a numbering scheme of 1.1, 1.2, 1.3, and so on, is used.</span></span>

### <a name="indent-task"></a><span data-ttu-id="9acc7-146">Feladat behúzása</span><span class="sxs-lookup"><span data-stu-id="9acc7-146">Indent task</span></span>

<span data-ttu-id="9acc7-147">Amikor egy feladatot behúznak, az a közvetlenül felette található feladat gyereke lesz.</span><span class="sxs-lookup"><span data-stu-id="9acc7-147">When a task is indented, it becomes a child of the task that is directly above it.</span></span> <span data-ttu-id="9acc7-148">Ezután a feladat ütemezésazonosítóját újra kiszámítják úgy, hogy az új szülő ütemezésazonosítóján alapuljon, és kövesse a vázlatos számozási sémát.</span><span class="sxs-lookup"><span data-stu-id="9acc7-148">The schedule ID of the task is then recalculated so that it's based on the schedule ID of its new parent and follows the outline numbering scheme.</span></span> <span data-ttu-id="9acc7-149">A szülőfeladat most már összefoglaló vagy tároló feladat.</span><span class="sxs-lookup"><span data-stu-id="9acc7-149">The parent task is now a summary task or a container task.</span></span> <span data-ttu-id="9acc7-150">Így lesz a saját gyermekfeladatainak összegzése.</span><span class="sxs-lookup"><span data-stu-id="9acc7-150">Therefore, it becomes a rollup of its child tasks.</span></span>

### <a name="outdent-task"></a><span data-ttu-id="9acc7-151">Feladat kihúzása</span><span class="sxs-lookup"><span data-stu-id="9acc7-151">Outdent task</span></span> 

<span data-ttu-id="9acc7-152">Ha egy feladatot kihúztak, akkor már nem annak a feladatnak a gyermeke, amelyik a szülője volt.</span><span class="sxs-lookup"><span data-stu-id="9acc7-152">When a task is outdented, it's no longer a child of the task that was its parent.</span></span> <span data-ttu-id="9acc7-153">Az ütemezés azonosítóját ezután újra kiszámítja a rendszer, hogy tükrözze a feladat frissített mélységét és helyzetét a hierarchiában.</span><span class="sxs-lookup"><span data-stu-id="9acc7-153">The schedule ID is then recalculated so that it reflects the task's updated depth and position in the hierarchy.</span></span> <span data-ttu-id="9acc7-154">Az előző szülőfeladat erőfeszítéseit, költségeit és dátumait újra kiszámítja a rendszer, így azok nem tartalmazzák ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="9acc7-154">The effort, cost, and dates of the previous parent task are recalculated so that they don't include this task.</span></span>

### <a name="move-up-and-move-down"></a><span data-ttu-id="9acc7-155">Mozgatás felfelé és lefelé</span><span class="sxs-lookup"><span data-stu-id="9acc7-155">Move up and Move down</span></span> 

<span data-ttu-id="9acc7-156">A **Mozgatás felfelé** és a **Mozgatás lefelé** gombokkal változtatható meg a feladat helyzete a szülőhierarchiában.</span><span class="sxs-lookup"><span data-stu-id="9acc7-156">The **Move up** and **Move down** buttons change the position of a task within its parent hierarchy.</span></span> <span data-ttu-id="9acc7-157">Az ilyen típusú változások nem befolyásolják a feladat erőfeszítését, költségét, dátumait vagy időtartamát.</span><span class="sxs-lookup"><span data-stu-id="9acc7-157">Changes of this type don't affect the task's effort, cost, dates, or duration.</span></span> <span data-ttu-id="9acc7-158">Csak a feladat ütemezésazonosítóját érintik.</span><span class="sxs-lookup"><span data-stu-id="9acc7-158">Only the task's schedule ID is affected.</span></span> <span data-ttu-id="9acc7-159">Az ütemezésazonosítót újraszámítják úgy, hogy az tükrözze a feladat új helyzetét a szülő gyermekfeladat-listáján.</span><span class="sxs-lookup"><span data-stu-id="9acc7-159">The schedule ID is recalculated so that it reflects the task's new position in the parent's list of child tasks.</span></span>

### <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="9acc7-160">Kisegítő lehetőségek és billentyűparancsok</span><span class="sxs-lookup"><span data-stu-id="9acc7-160">Accessibility and keyboard shortcuts</span></span>

<span data-ttu-id="9acc7-161">Az **Ütemezés** rács teljesen elérhető és képernyőolvasókkal, például a Narrátorral, JAWS vagy NVDA programokkal használható.</span><span class="sxs-lookup"><span data-stu-id="9acc7-161">The **Schedule** grid is fully accessible and can be used with screen readers such as Narrator, JAWS, or NVDA.</span></span> <span data-ttu-id="9acc7-162">A rácsterületen nyílbillentyűkkel mozoghat (a Microsoft Excel programhoz hasonlóan ), a Tab billentyű segítségével léphet tovább az interaktív felhasználói felület elemein, a lefelé mutató nyíl, az Enter vagy a szóköz segítségével választhat és hívhatja be a legördülő menüket.</span><span class="sxs-lookup"><span data-stu-id="9acc7-162">You can move through the grid area by using arrow keys (as in Microsoft Excel), you can use the Tab key to advance through the interactive UI elements, and you can use the Down arrow key, the Enter key, or the Spacebar to select and invoke the drop-down menus.</span></span> <span data-ttu-id="9acc7-163">Az oszlopfejlécek szintén interaktívak.</span><span class="sxs-lookup"><span data-stu-id="9acc7-163">The column headers are also interactive.</span></span> <span data-ttu-id="9acc7-164">Az oszlopokat elrejtheti és megjelenítheti, a Tab billentyűvel és a nyílbillentyűkkel mozgathatja az oszlopfejléceket, és az eszköztár műveleti gombjait is használhatja.</span><span class="sxs-lookup"><span data-stu-id="9acc7-164">You can hide and show columns, use the Tab key and arrow keys to move through the column headers, and use the action buttons on the toolbar.</span></span> <span data-ttu-id="9acc7-165">Ezenkívül a következő billentyűparancsokat használhatja:</span><span class="sxs-lookup"><span data-stu-id="9acc7-165">In addition, you can use the following keyboard shortcuts:</span></span>

- <span data-ttu-id="9acc7-166">**Frissítés**: ALT+SHIFT+F5</span><span class="sxs-lookup"><span data-stu-id="9acc7-166">**Refresh**: ALT+SHIFT+F5</span></span>
- <span data-ttu-id="9acc7-167">**Hozzáadás**: ALT+SHIFT+Insert</span><span class="sxs-lookup"><span data-stu-id="9acc7-167">**Add**: ALT+SHIFT+Insert</span></span>
- <span data-ttu-id="9acc7-168">**Törlés**: ALT+SHIFT+Delete</span><span class="sxs-lookup"><span data-stu-id="9acc7-168">**Delete**: ALT+SHIFT+Delete</span></span>
- <span data-ttu-id="9acc7-169">**Mozgatás fel/le**: ALT+SHIFT+Fel/le nyilak</span><span class="sxs-lookup"><span data-stu-id="9acc7-169">**Move up/down**: ALT+SHIFT+Up/Down arrows</span></span>
- <span data-ttu-id="9acc7-170">**Behúzás/kihúzás**: ALT_SHIFT+Balra/jobbra nyilak</span><span class="sxs-lookup"><span data-stu-id="9acc7-170">**Indent/Outdent**: ALT_SHIFT+Left/Right arrows</span></span>
- <span data-ttu-id="9acc7-171">**Hierarchiák kibontása/összecsukása**: ALT+SHIFT+Plusz/mínusz gombok</span><span class="sxs-lookup"><span data-stu-id="9acc7-171">**Expand/Collapse Hierarchies**: ALT+SHIFT+Plus/Minus keys</span></span>

## <a name="task-attributes"></a><span data-ttu-id="9acc7-172">Feladat attribútumok</span><span class="sxs-lookup"><span data-stu-id="9acc7-172">Task attributes</span></span>

<span data-ttu-id="9acc7-173">A feladat neve leírja az elvégzendő munkát.</span><span class="sxs-lookup"><span data-stu-id="9acc7-173">A task's name describes the work that must be completed.</span></span> <span data-ttu-id="9acc7-174">A PSA-ban a feladattal kapcsolatos attribútumok leírják a feladat ütemezését és a személyzeti követelményeket.</span><span class="sxs-lookup"><span data-stu-id="9acc7-174">In PSA, the attributes that are associated with a task describe the schedule of the task and its staffing requirements.</span></span>

> ![Feladat attribútumok](media/project-2.png)
 
### <a name="schedule-attributes"></a><span data-ttu-id="9acc7-176">Attribútumok ütemezése</span><span class="sxs-lookup"><span data-stu-id="9acc7-176">Schedule attributes</span></span>

<span data-ttu-id="9acc7-177">Az **Erőfeszítés**, a **Kezdő dátum**, a **Befejező dátum** és az **Időtartam** attribútumok határozzák meg a feladat ütemezését.</span><span class="sxs-lookup"><span data-stu-id="9acc7-177">The **Effort**, **Start date**, **End date**, and **Duration** attributes define the schedule for the task.</span></span>

<span data-ttu-id="9acc7-178">További ütemezési attribútumok a következők:</span><span class="sxs-lookup"><span data-stu-id="9acc7-178">Additional schedule attributes include:</span></span>

- <span data-ttu-id="9acc7-179">**Erőfeszítés órái**: Adja meg a feladat elvégzéséhez szükséges órák becsült számát.</span><span class="sxs-lookup"><span data-stu-id="9acc7-179">**Effort hours**: Enter an estimate of the hours that are required to complete the task.</span></span> 
- <span data-ttu-id="9acc7-180">**Időtartam**: Adja meg a feladat elvégzéséhez szükséges munkanapok számát.</span><span class="sxs-lookup"><span data-stu-id="9acc7-180">**Duration**: Specify the number of workdays that are required to complete the task.</span></span>
- <span data-ttu-id="9acc7-181">**Ütemezésazonosító**: Ezzel az automatikusan generált azonosítóval rendelik meg a feladatokat a hierarchiában.</span><span class="sxs-lookup"><span data-stu-id="9acc7-181">**Schedule ID**: This automatically generated ID is used to order tasks in the hierarchy.</span></span> <span data-ttu-id="9acc7-182">A feladatok közötti függőségek kezelik a feladatok tényleges sorrendjét.</span><span class="sxs-lookup"><span data-stu-id="9acc7-182">Dependencies between the tasks manage the actual order in which the tasks are worked on.</span></span>
 
### <a name="staffing-attributes"></a><span data-ttu-id="9acc7-183">Munkaerő-attribútumok</span><span class="sxs-lookup"><span data-stu-id="9acc7-183">Staffing attributes</span></span>

<span data-ttu-id="9acc7-184">A személyzet attribútumai az ütemterv **Erőforrások** mezőjével érhetők el.</span><span class="sxs-lookup"><span data-stu-id="9acc7-184">Staffing attributes are accessed through the **Resources** field in the schedule.</span></span> <span data-ttu-id="9acc7-185">Vagy keressen meglévő erőforrást, vagy kattintson a **Létrehozás** elemre, és a **Gyors létrehozás** ablaktáblában új erőforrásként adja hozzá a projekt egyik csapattagját.</span><span class="sxs-lookup"><span data-stu-id="9acc7-185">You can either search for an existing resource, or click **Create** and in the **Quick Create** pane, add a project team member as a new resource.</span></span>

<span data-ttu-id="9acc7-186">A **Szerepkör**, az **Erőforrásbiztosító egység** és a **Pozíció neve** mezők a feladat személyzeti követelményeinek leírására szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="9acc7-186">The **Role**, **Resourcing Unit**, and **Position Name** fields are used to describe the staffing requirements for the task.</span></span> <span data-ttu-id="9acc7-187">A személyzeti attribútumokat és a feladatütemezést a rendelkezésre álló erőforrások megkeresésére használják az adott feladat végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="9acc7-187">These staffing attributes together with the task schedule are used to find available resources to do this task.</span></span>

<span data-ttu-id="9acc7-188">**Szerepkör** – Adja meg a feladat elvégzéséhez szükséges erőforrás típusát.</span><span class="sxs-lookup"><span data-stu-id="9acc7-188">**Role** - Specify the type of resource that is required to do the task.</span></span>

<span data-ttu-id="9acc7-189">**Erőforrásbiztosító egység** – Adja meg azt az egységet, ahonnan megtörténik az erőforrások hozzárendelése a feladathoz.</span><span class="sxs-lookup"><span data-stu-id="9acc7-189">**Resourcing unit** - Specify the unit that resources for the task should be assigned from.</span></span> <span data-ttu-id="9acc7-190">Ez az attribútum befolyásolja a feladat költség- és értékesítési becslését, ha az erőforrás költségét és számlamértékét erőforrásbiztosító egységek alapján állítják be.</span><span class="sxs-lookup"><span data-stu-id="9acc7-190">This attribute affects the cost and sales estimate for the task if the cost and bill rate for the resource are set based on resourcing units.</span></span>

<span data-ttu-id="9acc7-191">**Pozíció neve** – Adjon meg egy barátságos nevet az általános erőforrás számára, hogy a név helyőrzőjeként szolgáljon azon erőforrás számára, amely végül elvégzi majd a munkát.</span><span class="sxs-lookup"><span data-stu-id="9acc7-191">**Position name** – Enter a friendly name for the generic resource that serves as a placeholder for the resource that will ultimately do the work.</span></span>

<span data-ttu-id="9acc7-192">Az **Erőforrások** mező az általános erőforrás vagy a megnevezett erőforrás pozíciónevét tartalmazza, ha megtalálható valamelyik.</span><span class="sxs-lookup"><span data-stu-id="9acc7-192">The **Resources** field holds the position name of the generic resource or named resource when one is found.</span></span>

<span data-ttu-id="9acc7-193">A **Kategória** mező azokat az értékeket tartalmazza, amelyek egy olyan szélesebb körű munkát jelölnek, amelybe a feladat csoportosítható.</span><span class="sxs-lookup"><span data-stu-id="9acc7-193">The **Category** field holds the values that indicate a broader type of work that the task can be grouped into.</span></span> <span data-ttu-id="9acc7-194">Ez a mező nem érinti az ütemezést vagy a személyzetet.</span><span class="sxs-lookup"><span data-stu-id="9acc7-194">This field doesn't affect scheduling or staffing.</span></span> <span data-ttu-id="9acc7-195">Csak jelentéskészítéshez használják.</span><span class="sxs-lookup"><span data-stu-id="9acc7-195">It's used only for reporting.</span></span>

### <a name="task-dependencies"></a><span data-ttu-id="9acc7-196">Tevékenység függőségek</span><span class="sxs-lookup"><span data-stu-id="9acc7-196">Task dependencies</span></span> 

<span data-ttu-id="9acc7-197">A PSA-ban az ütemezést a feladatok közötti korábbi kapcsolatok létrehozására használhatja.</span><span class="sxs-lookup"><span data-stu-id="9acc7-197">You can use the schedule in PSA to create predecessor relationships between tasks.</span></span> <span data-ttu-id="9acc7-198">A **Korábbi** mezőben a **Feladatok** alatt egy vagy több értéket vesz fel, hogy jelezze azokat a feladatokat, amelyektől a feladat függ.</span><span class="sxs-lookup"><span data-stu-id="9acc7-198">The **Predecessor** field under **Tasks** takes one or more values to indicate the tasks that a task depends on.</span></span> <span data-ttu-id="9acc7-199">Ha egy feladathoz korábbi értékek vannak hozzárendelve, akkor a feladat csak a korábbi feladatok elvégzése után indulhat el.</span><span class="sxs-lookup"><span data-stu-id="9acc7-199">When predecessor values are assigned to a task, the task can start only after all the predecessor tasks have been completed.</span></span> <span data-ttu-id="9acc7-200">A függőség miatt a feladat tervezett kezdő dátumát visszaállítják a korábbi feladatok befejezésének napjára.</span><span class="sxs-lookup"><span data-stu-id="9acc7-200">Because of the dependency, the planned start date of the task is reset to the date when the predecessor tasks are completed.</span></span>

<span data-ttu-id="9acc7-201">A feladat mód nincs hatással a korábbi/függő feladatok kezdő és befejező dátumának frissítéseire.</span><span class="sxs-lookup"><span data-stu-id="9acc7-201">The task mode has no effect on updates that are made to the start and end dates of predecessor/dependent tasks.</span></span>

## <a name="task-mode"></a><span data-ttu-id="9acc7-202">Tevékenység mód</span><span class="sxs-lookup"><span data-stu-id="9acc7-202">Task mode</span></span> 

<span data-ttu-id="9acc7-203">A feladat mód határozza meg a levélcsomópont-feladatok ütemezését.</span><span class="sxs-lookup"><span data-stu-id="9acc7-203">The task mode determines the scheduling of leaf node tasks.</span></span> <span data-ttu-id="9acc7-204">A PSA minden feladathoz két feladatmódot támogat: automatikus ütemezés és kézi ütemezés.</span><span class="sxs-lookup"><span data-stu-id="9acc7-204">PSA supports two task modes for every task: automatic scheduling and manual scheduling.</span></span>

### <a name="auto-scheduling"></a><span data-ttu-id="9acc7-205">Automatikus ütemezés</span><span class="sxs-lookup"><span data-stu-id="9acc7-205">Auto-scheduling</span></span> 
 
<span data-ttu-id="9acc7-206">Amikor a feladatmód beállítása **Automatikusan ütemezett** egy feladatnál, a feladatütemező motor ütemezési szabályokat használ a feladatattribútumokon a feladat ütemezésének meghatározására.</span><span class="sxs-lookup"><span data-stu-id="9acc7-206">When task mode is set to **Automatically Scheduled** for a task, the task scheduling engine uses the scheduling rules on task attributes to determine the schedule for the task.</span></span>

#### <a name="scheduling-rules"></a><span data-ttu-id="9acc7-207">Ütemezési szabályok</span><span class="sxs-lookup"><span data-stu-id="9acc7-207">Scheduling rules</span></span>

<span data-ttu-id="9acc7-208">Alapértelmezés szerint, ha a levélcsomópont-feladatnak nincsenek elődei, akkor a kezdési dátum a projekt ütemezett kezdési dátumára lesz állítva.</span><span class="sxs-lookup"><span data-stu-id="9acc7-208">By default, if a leaf node task doesn't have predecessors, its start date is set to the project's scheduled start date.</span></span> <span data-ttu-id="9acc7-209">Egy levélcsomópont tevékenység időtartamot mindig a kezdő és befejezési dátumok közötti napok száma szerint számítják ki.</span><span class="sxs-lookup"><span data-stu-id="9acc7-209">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="9acc7-210">Amikor egy feladat automatikusan ütemezett, az ütemező motor a következő szabályokat követi:</span><span class="sxs-lookup"><span data-stu-id="9acc7-210">When a task is automatically scheduled, the scheduling engine follows these rules:</span></span>

- <span data-ttu-id="9acc7-211">A feladat kezdési és befejezési dátumának munkanapon kell lennie a projekt ütemezési naptárának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="9acc7-211">The start and end dates of the task must be working days, according to the project's scheduling calendar.</span></span> 
- <span data-ttu-id="9acc7-212">Bármely olyan feladat esetében, amely korábbi feladatokkal rendelkezik, a kezdő dátum automatikusan az elődei legújabb befejezési dátumára lesz állítva.</span><span class="sxs-lookup"><span data-stu-id="9acc7-212">For any task that has predecessor tasks, the start date is automatically set to the latest end date of its predecessors.</span></span>
- <span data-ttu-id="9acc7-213">Az erőfeszítést a következő képlet alapján számítják ki: Személyek száma × Időtartam × Órák a projekt naptárában standard munkanapon.</span><span class="sxs-lookup"><span data-stu-id="9acc7-213">Effort is calculated by using this formula: Number of people × Duration × Hours in a standard workday in the project calendar.</span></span>

### <a name="manual-scheduling"></a><span data-ttu-id="9acc7-214">Kézi ütemezés</span><span class="sxs-lookup"><span data-stu-id="9acc7-214">Manual scheduling</span></span>

<span data-ttu-id="9acc7-215">Ha az automatikus ütemezés szabályai nem felelnek meg az Ön igényeinek, beállíthatja a feladatmódot **Kézi ütemezés** értékre.</span><span class="sxs-lookup"><span data-stu-id="9acc7-215">If the rules of automatic scheduling don't meet your requirements, you can set the task mode for the task to **Manually Scheduled**.</span></span> <span data-ttu-id="9acc7-216">Ez a beállítás megakadályozza, hogy az ütemezőmotor kiszámolja a többi ütemezési attribútum értékét.</span><span class="sxs-lookup"><span data-stu-id="9acc7-216">This setting stops the scheduling engine from calculating the values of other scheduling attributes.</span></span> <span data-ttu-id="9acc7-217">A feladatmódtól függetlenül, ha elődöket állít be a feladatokra, akkor mindig befolyásolni fogja a függő feladat kezdő dátumát.</span><span class="sxs-lookup"><span data-stu-id="9acc7-217">Regardless of the task mode, if you set predecessors on tasks, you always affect the dependent task's start date.</span></span>