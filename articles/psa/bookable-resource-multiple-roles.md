---
title: A projektek értékesítésének és költségeinek becslése, ha egy foglalt erőforrás több szerepkört tölt be egy projekthez
description: Ez a témakör információkat tartalmaz arról, hogyan használhatók árképzési dimenziók a több szerepkörrel rendelkező erőforrásra vonatkozó árképzés és költségszámítás támogatására.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 67e24156e960b9b09cf92f7f0cd77f6c74a982b8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145046"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a><span data-ttu-id="fa5b6-103">A projektek értékesítésének és költségeinek becslése, ha egy foglalt erőforrás több szerepkört tölt be egy projekthez</span><span class="sxs-lookup"><span data-stu-id="fa5b6-103">Estimate project sales and costs when a bookable resource fills multiple roles for a project</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fa5b6-104">A projektalapú vállalatoknak gyakran szükségük van arra, hogy egy erőforrásra több szerepkört hajtson végre egy projekten.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-104">Project-based companies often have the need for one resource to perform multiple roles on a project.</span></span> <span data-ttu-id="fa5b6-105">Az egyes szerepkörök árazása és elszámolása eltérhet, ami azt jelenti, hogy ugyanazon erőforrás ideje a projektre vonatkozóan eltérő pénzügyi becslést kaphat az egyes szerepkörök számla- és költségmértékének függvényében.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-105">Each of these roles could be priced and costed differently, which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="fa5b6-106">A Project Service Automation lehetővé teszi, hogy a csoporttagrekordban szereplő értékek a megadott erőforráshoz legyenek beállítva, valamint különböző felülbírálásokat tesz lehetővé a csoporttaghoz rendelt minden egyes feladat esetében.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="fa5b6-107">A következő példa azt mutatja be, hogyan teszi lehetővé az érték egyszerű felülírása, hogy egy erőforrás több szerepkörrel rendelkezzen a projektben, ahol különböző költség- és számlázási mértékek szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="fa5b6-108">Feladatok létrehozása</span><span class="sxs-lookup"><span data-stu-id="fa5b6-108">Create tasks</span></span>
<span data-ttu-id="fa5b6-109">Hozzon létre két, egyenként 40 órára vonatkozó projektfeladatot, a „A” és a „B” feladatot. Válassza ki az „A” feladatot a „B” feladat elődjeként.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="fa5b6-110">Szerepkör és Szervezeti egység beállítása általános projektcsoporttag számára</span><span class="sxs-lookup"><span data-stu-id="fa5b6-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="fa5b6-111">Az **Ütemezés** lapon jelölje ki a **Feladat** sort az „A” Feladathoz.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="fa5b6-112">Az **Erőforrások** mezőben válassza ki a **Létrehozás** elemet a legördülő listából.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="fa5b6-113">A **Csapattagok gyors létrehozása** lapon adja meg a feladatot végrehajtó általános csoporttag attribútumait.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="fa5b6-114">Jelölje ki a megfelelő szerepkört és szervezeti egységet, majd kattintson a **Mentés és bezárás** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="fa5b6-115">A rendszer létrehoz egy általános csoporttagot, és hozzárendeli ehhez a feladathoz.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="fa5b6-116">Ismételje meg ezeket a lépéseket a „B” feladat esetében is, és győződjön meg arról, hogy a „B” feladathoz létrehozott általános csoporttagon létrehozott szerepkör és szervezeti egység nem egyezik meg az „A” feladatban megadottakkal.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="fa5b6-117">Szerepkör és szervezeti egység beállítása egy projektfeladathoz</span><span class="sxs-lookup"><span data-stu-id="fa5b6-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="fa5b6-118">Miután létrehozta az „A” feladatot, jelölje ki a feladatot, majd válassza a **Feladat szerkesztése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="fa5b6-119">A **Feladat részletei** lapon keresse meg a **Szerepkör** és a **Szervezeti egység** mezőket, és adja hozzá a feladatot végrehajtó erőforráshoz szükséges értékeket.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="fa5b6-120">Ha a Project Service Automation demóadatainak használatával hajtja végre ezt a műveletet, jelölje be a **Vezető tanácsadó** lehetőséget a szerepkörhöz, és a **Fabrikam US** lehetőséget a szervezeti egységhez.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="fa5b6-121">Jelölje ki a „B” feladatot, és válassza ki a **Feladat szerkesztése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="fa5b6-122">A **Feladat részletei** lapon keresse meg a **Szerepkör** és a **Szervezeti egység** mezőket, és adja hozzá a feladatot végrehajtó erőforráshoz szükséges értékeket.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="fa5b6-123">Győződjön meg arról, hogy a **Szerepkör** és **Szervezeti egység** mezők értékei eltérnek a B feladat és az A feladat esetében.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from the values for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="fa5b6-124">Ha a Project Service Automation demóadatainak használatával hajtja végre ezt a műveletet, jelölje be a **Hálózati technikus** lehetőséget a szerepkörhöz, és a **Fabrikam US** lehetőséget a szervezeti egységhez.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="fa5b6-125">Mentse és zárja be a **Feladat részletei** lapot.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="fa5b6-126">Csoporttag és a becslések működése</span><span class="sxs-lookup"><span data-stu-id="fa5b6-126">Team member and estimates behavior</span></span> 

1. <span data-ttu-id="fa5b6-127">A **Feladat részletei** lapon a **Csoporttag** lehetőségnél jelölje ki a két általános csoporttagot, majd válassza a **Követelmények létrehozása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-127">On the **Task Details** page, on the **Team Member**, select the two generic team Members and then select **Generate Requirements**.</span></span> 
2. <span data-ttu-id="fa5b6-128">Válassza ki a csoporttag sort a **Vezető tanácsadó** lehetőségnél, majd válassza a **Foglalás** opciót.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-128">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="fa5b6-129">Megnyílik az ütemezési tábla, és lefoglalja az adott követelménynek megfelelő erőforrást.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-129">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="fa5b6-130">Válassza ki a csoporttag sort a **Hálózati technikus** lehetőségnél, majd válassza a **Foglalás** opciót.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-130">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="fa5b6-131">Megnyílik az ütemezési tábla, és lefoglalja ugyanazt az erőforrást az adott követelménynek.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-131">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="fa5b6-132">Csoporttag rács</span><span class="sxs-lookup"><span data-stu-id="fa5b6-132">Team Member grid</span></span> 
<span data-ttu-id="fa5b6-133">A **Csoporttag** rácson figyelje meg, hogy a két általános csoporttag bejegyzése törlődik, és lecserélődik egy erőforrásra.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-133">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="fa5b6-134">Az adott erőforráshoz egy értékkészlet van megadva, amely a **Szerepkör** és a **Szervezeti egység** alapértelmezett értékeit jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-134">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="fa5b6-135">Ha kibontja a csoporttagrekord sorát, akkor mindkét feladathoz külön hozzárendelések jelennek meg a csoporttagrekordban.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-135">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="fa5b6-136">Minden hozzárendelési sornak a **Szerepkörhöz** és a **Szervezeti egységhez** kapcsolódó feladatspecifikus értékei vannak.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-136">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="fa5b6-137">Becslések rács</span><span class="sxs-lookup"><span data-stu-id="fa5b6-137">Estimates grid</span></span> 
<span data-ttu-id="fa5b6-138">Amikor megnyitja a **Becslések** rácsot, megfigyelheti, hogy az ugyanahhoz az erőforráshoz tartozó hozzárendelések eltérően vannak árazva.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-138">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="fa5b6-139">Az „A” feladatnál az erőforráshoz rendelt hozzárendelés árazása a **Vezető tanácsadó** opció **Szerepkör** attribútumának értéke szerint történik.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-139">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="fa5b6-140">A „B” feladatnál az ugyanazon erőforráshoz rendelt hozzárendelés árazása a **Hálózati technikus** opció **Szerepkör** attribútumának értéke szerint történik.</span><span class="sxs-lookup"><span data-stu-id="fa5b6-140">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>

