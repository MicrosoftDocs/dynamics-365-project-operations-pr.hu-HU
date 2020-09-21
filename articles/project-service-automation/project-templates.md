---
title: Projektsablonok
description: Ez a témakör ismerteti, hogyan lehet a projektsablonokat használni a gyors projektbeállításhoz.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f0161bf9-af4c-4a21-b767-ac20a8e30688
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5a3112c2eef9525946314bdb587c44904557fa52
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752199"
---
# <a name="project-templates"></a><span data-ttu-id="96532-103">Projektsablonok</span><span class="sxs-lookup"><span data-stu-id="96532-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="96532-104">A projekt sablon egy előre meghatározott keret, amely segít a projekt gyors és egyszerű elindításában.</span><span class="sxs-lookup"><span data-stu-id="96532-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="96532-105">Használhat egy előre definiált sablont egy új kattintással új projekt létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="96532-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="96532-106">Ami a projektet illeti, meg kell határoznia a projektsablonok előfeltételeit.</span><span class="sxs-lookup"><span data-stu-id="96532-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="96532-107">Minden egyes projektsablonhoz meg kell határoznia egy projektnaptárt, a szerepeket és az árlistákat előre meg kell határozni a szervezetben, hogy a sablon összetevői hasznos adatokkal rendelkezzenek.</span><span class="sxs-lookup"><span data-stu-id="96532-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="96532-108">A projekt sablonja három összetevőből áll: ütemterv, projektbecslések és a projektcsoport tagjai.</span><span class="sxs-lookup"><span data-stu-id="96532-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="96532-109">Ütemezés</span><span class="sxs-lookup"><span data-stu-id="96532-109">Schedule</span></span>

<span data-ttu-id="96532-110">A ütemterv a projekt sablonjában ugyanazokat az elemeket tartalmazza, mint a projekt ütemezése.</span><span class="sxs-lookup"><span data-stu-id="96532-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="96532-111">Létrehozhat egy feladathierarchiát, társíthat szerepeket a feladatokhoz, meghatározhat ütemezési attribútumokat és beállíthat függőségeket.</span><span class="sxs-lookup"><span data-stu-id="96532-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="96532-112">Az ütemterv egy projektsablonban támogatja az egyes feladatok feladatmódjait is.</span><span class="sxs-lookup"><span data-stu-id="96532-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="96532-113">Ezért támogatja az ütemezési motort.</span><span class="sxs-lookup"><span data-stu-id="96532-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="96532-114">A projekt naptárát társítania kell a projekthez.</span><span class="sxs-lookup"><span data-stu-id="96532-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="96532-115">A munkaterv létrehozásakor nincs különbség a projekt sablonja és a projekt között.</span><span class="sxs-lookup"><span data-stu-id="96532-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="96532-116">Projektbecslések</span><span class="sxs-lookup"><span data-stu-id="96532-116">Project estimates</span></span>

<span data-ttu-id="96532-117">A projektminta egy projektsablonban ugyanúgy működik, mint a projektben szereplő projektbecslés.</span><span class="sxs-lookup"><span data-stu-id="96532-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="96532-118">A költségeket és az eladási árakat azonban a paraméterekben meghatározott alapértelmezett költség- és eladási árlistákból vonják le.</span><span class="sxs-lookup"><span data-stu-id="96532-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="96532-119">Projekt létrehozása sablonból</span><span class="sxs-lookup"><span data-stu-id="96532-119">Creating a project from a template</span></span>
 
<span data-ttu-id="96532-120">A projekt sablonból történő létrehozásához többféle módszer létezik:</span><span class="sxs-lookup"><span data-stu-id="96532-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="96532-121">Amikor egy projektet árajánlatból hoz létre, kiválaszthatja a projekt sablonját a **Gyors létrehozás: Projekt** párbeszédpanelen.</span><span class="sxs-lookup"><span data-stu-id="96532-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Gyors létrehozás: Projekt párbeszédpanel](media/project-11.png)

- <span data-ttu-id="96532-123">Amikor egy projektet az **Új projekt** kiválasztásával hoz létre, a **Projekt** oldal jelenik meg, mielőtt a rekord mentésre kerül.</span><span class="sxs-lookup"><span data-stu-id="96532-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="96532-124">A **Sablon kiválasztása** mezőben válassza ki a szervezet előre meghatározott projektsablonjait.</span><span class="sxs-lookup"><span data-stu-id="96532-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="96532-125">Használja a **Projekt létrehozása sablonból** elemet a **Sablon entitás** oldalon.</span><span class="sxs-lookup"><span data-stu-id="96532-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="96532-126">A sablon összetevőinek másolása a projektbe</span><span class="sxs-lookup"><span data-stu-id="96532-126">Copying components of template to project</span></span>

<span data-ttu-id="96532-127">A projekt sablonjának összetevőinek a projektbe másolásakor a projekt beállításaitól függően néhány felülbírálás fordulhat elő.</span><span class="sxs-lookup"><span data-stu-id="96532-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="96532-128">Az ütemterv másolása</span><span class="sxs-lookup"><span data-stu-id="96532-128">Copying the schedule</span></span>

<span data-ttu-id="96532-129">Az ütemezés másolásakor a projekt sablonból, ha a projektnek eltér a projekt naptára, mint a sablonon, a projekt naptárában szereplő munkaidő alkalmazandó a feladat ütemezésére.</span><span class="sxs-lookup"><span data-stu-id="96532-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="96532-130">Ilyen módon az ütemtervet hozzáigazítják a projekt hátteréhez.</span><span class="sxs-lookup"><span data-stu-id="96532-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="96532-131">Hasonlóképpen, az ütemterv első feladata a projekt kezdő dátumát veszi, és a hierarchia többi részének ütemterve frissül a sablonban megadott időtartam és függőségek alapján.</span><span class="sxs-lookup"><span data-stu-id="96532-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="96532-132">Projektbecslések másolása</span><span class="sxs-lookup"><span data-stu-id="96532-132">Copying project estimates</span></span> 

<span data-ttu-id="96532-133">Ha a projektbecslési sorok között másol, az árlisták frissülnek.</span><span class="sxs-lookup"><span data-stu-id="96532-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="96532-134">A költségjegyzéknél ezek a frissítések a projekt tulajdonos egységén alapulnak.</span><span class="sxs-lookup"><span data-stu-id="96532-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="96532-135">Az eladási árlista alapján a vevőn alapulnak.</span><span class="sxs-lookup"><span data-stu-id="96532-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="96532-136">Az értékesítési egységhez kapcsolódó projektek esetében az egységköltséget és az eladási árat ezen árlisták alapján határozzák meg.</span><span class="sxs-lookup"><span data-stu-id="96532-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="96532-137">Projektcsoport másolása</span><span class="sxs-lookup"><span data-stu-id="96532-137">Copying a project team</span></span>

<span data-ttu-id="96532-138">Amikor egy projektcsoportot átmásolnak egy projekt sablonból egy projektbe, akkor az általános erőforrások másolódnak, a sablonban meghatározott készségekkel és jártasságokkal együtt.</span><span class="sxs-lookup"><span data-stu-id="96532-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="96532-139">Az általános erőforrás-hozzárendeléseket szintén fenntartják, ahogy a projekt sablonjában is voltak.</span><span class="sxs-lookup"><span data-stu-id="96532-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="96532-140">A megnevezett erőforrásokat a projektsablonok nem támogatják.</span><span class="sxs-lookup"><span data-stu-id="96532-140">Named resources aren't supported in project templates.</span></span>