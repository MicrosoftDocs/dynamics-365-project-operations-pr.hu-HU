---
title: Projektsablon létrehozása
description: Projektsablon létrehozása a Project Service szolgáltatásban
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ba15d6d5-a43b-456a-9488-db6e92023fa1
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 50e12d65d5ed957565485413490b8d9f0e2f47ab
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752185"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="e7f67-103">Projektsablon létrehozása (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e7f67-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e7f67-104">A projektsablonokkal időt takaríthat meg, ha a vállalat rendszeresen tesz ajánlatot hasonló típusú projektekre.</span><span class="sxs-lookup"><span data-stu-id="e7f67-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="e7f67-105">Egy bizonyos típusú projekthez standard szerepeket és becsült órákat nyújt.</span><span class="sxs-lookup"><span data-stu-id="e7f67-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="e7f67-106">A fiókmenedzserek és a projektmenedzsereket létrehozhatnak projekteken alapuló sablonokat, vagy másolhatnak egy sablont, és létrehozhatják a sajátjukat.</span><span class="sxs-lookup"><span data-stu-id="e7f67-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="e7f67-107">Projektsablon összetevői</span><span class="sxs-lookup"><span data-stu-id="e7f67-107">Components of project template</span></span>
 <span data-ttu-id="e7f67-108">A projektsablon három összetevőből áll:</span><span class="sxs-lookup"><span data-stu-id="e7f67-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="e7f67-109">**Munkalebontási szerkezet**: A munkalebontási szerkezet egy projektsablonban ugyanazokat az elemeket tartalmazza, mint a projekt.</span><span class="sxs-lookup"><span data-stu-id="e7f67-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="e7f67-110">Létrehozhat feladathierarchiát, kioszthat szerepeket feladatokhoz, meghatározhat ütemezési attribútumokat, beállíthat függőségeket és megtekinthet minden adatot a Gantt-diagramon.</span><span class="sxs-lookup"><span data-stu-id="e7f67-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="e7f67-111">A projektsablonok munkalebontási szerkezete támogatja az egyes feladatok feladatmódját.</span><span class="sxs-lookup"><span data-stu-id="e7f67-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="e7f67-112">Nincs különbség a projektsablon és a projekt között, amikor ütemtervet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e7f67-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="e7f67-113">**Projektbecslés**: A projektbecslések a sablonokban ugyanúgy működnek, ahogy a projektekben, kivéve, hogy a költségeket és eladási árakat meghatározó árlisták mind a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] paraméterek között megtalálható alapértelmezett költség- és eladásiár-listák.</span><span class="sxs-lookup"><span data-stu-id="e7f67-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="e7f67-114">A többi funkció ugyanaz, mint egy projektben.</span><span class="sxs-lookup"><span data-stu-id="e7f67-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="e7f67-115">**Projektcsoport létrehozása**: Amikor projektcsoportot hoz létre projektsablonból, nem foglalhat le névvel rendelkező erőforrást a sablonban.</span><span class="sxs-lookup"><span data-stu-id="e7f67-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="e7f67-116">A munkalebontási struktúrában használhatja a **Projektcsoport létrehozása** lehetőséget az általános erőforrások generálásához.</span><span class="sxs-lookup"><span data-stu-id="e7f67-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="e7f67-117">Megadhatja a szükséges készségeket és a szakmai tapasztalatokat az általános erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="e7f67-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="e7f67-118">Nem helyettesíthet általános erőforrást foglalható erőforrással a projektsablonokban.</span><span class="sxs-lookup"><span data-stu-id="e7f67-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="e7f67-119">Projekt létrehozása sablonból</span><span class="sxs-lookup"><span data-stu-id="e7f67-119">Create a project from a template</span></span>  
 <span data-ttu-id="e7f67-120">A következő módokon hozhat létre projektet sablonból:</span><span class="sxs-lookup"><span data-stu-id="e7f67-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="e7f67-121">Amikor árajánlatból hoz létre projektet, kiválaszthat projektsablont a projekt gyorslétrehozási űrlapján.</span><span class="sxs-lookup"><span data-stu-id="e7f67-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="e7f67-122">Amikor projektet hoz létre az **Új projekt** lehetőségre kattintva, megjelenik a projektűrlap a rekord mentése előtt.</span><span class="sxs-lookup"><span data-stu-id="e7f67-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="e7f67-123">Innen kattintson a **Sablon kiválasztása** mezőre, hogy válasszon a vállalkozásában előre meghatározott projektsablonok közül.</span><span class="sxs-lookup"><span data-stu-id="e7f67-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="e7f67-124">Kattintson a **Projekt létrehozása sablonból** lehetőségre a **Projektsablon** lapon, ha sablonból szeretne projektet létrehozni.</span><span class="sxs-lookup"><span data-stu-id="e7f67-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="e7f67-125">Összetevők másolása sablonból projektbe</span><span class="sxs-lookup"><span data-stu-id="e7f67-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="e7f67-126">Amikor összetevőt másol sablonból projektbe, van néhány dolog, amiről tudnia kell.</span><span class="sxs-lookup"><span data-stu-id="e7f67-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="e7f67-127">**Munkalebontási struktúra másolása**: Amikor munkalebontási struktúrát másol projektsablonba, ha a projektnek más a projektnaptára, mint a sablonnak, akkor a projektnaptár munkaórái a feladatok ütemezéséhez kerülnek.</span><span class="sxs-lookup"><span data-stu-id="e7f67-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="e7f67-128">Ez az ütemezést a projektnaptárhoz igazítja.</span><span class="sxs-lookup"><span data-stu-id="e7f67-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="e7f67-129">Ehhez hasonlóan a munkalebontási struktúrában az első feladat a projekt kezdési dátumának megadása, így a feladathierarchia ütemezésének fennmaradó része a sablon munkalebontási struktúrájában meghatározott időtartam és függőségek alapján frissül.</span><span class="sxs-lookup"><span data-stu-id="e7f67-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="e7f67-130">**Projektbecslések másolása**: Ha projektbecslési sorokat másol, az árlisták a projekt tulajdonosegységének önköltségi listája alapján frissülnek, és az ügyfél az értékesítési árlista alapján.</span><span class="sxs-lookup"><span data-stu-id="e7f67-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="e7f67-131">Az egységköltség és az eladási árak az árlista alapján kerülnek meghatározásra azoknál a projekteknél, amelyek értékesítési entitással vannak összekapcsolva.</span><span class="sxs-lookup"><span data-stu-id="e7f67-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="e7f67-132">**Projektcsapat másolása**: Amikor a projektcsapatot sablonból projektbe másolja, akkor az általános erőforrásokat is másolja a rendszer a sablonban meghatározott képességekkel és szakmai tapasztalatokkal együtt.</span><span class="sxs-lookup"><span data-stu-id="e7f67-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="e7f67-133">Az általános erőforrás-hozzárendelések is megmaradnak a projektsablon szerint.</span><span class="sxs-lookup"><span data-stu-id="e7f67-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e7f67-134">Kapcsolódó információk</span><span class="sxs-lookup"><span data-stu-id="e7f67-134">See Also</span></span>  
 [<span data-ttu-id="e7f67-135">Projektmenedzseri útmutató</span><span class="sxs-lookup"><span data-stu-id="e7f67-135">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)