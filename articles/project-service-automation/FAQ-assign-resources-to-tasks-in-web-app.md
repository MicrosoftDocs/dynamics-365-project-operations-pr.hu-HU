---
title: Hogyan rendelhető hozzá foglalható erőforrás egy feladathoz a webes alkalmazásban
description: A foglalható erőforrások hozzárendelési módjainak áttekintése.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x on platform version 9.x
ms.assetid: 9db35b39-8dfc-4989-9160-fd841fe0ae5a
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 521ea73c948619816d3cd06d72140fcc85366397
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752322"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="d9de6-103">Hogyan rendelhető hozzá foglalható erőforrás egy feladathoz a webes alkalmazásban (Project Service 2.x alkalmazás)?</span><span class="sxs-lookup"><span data-stu-id="d9de6-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d9de6-104">Két módon lehet hozzárendelni egy erőforrást egy feladathoz a Project Service esetében.</span><span class="sxs-lookup"><span data-stu-id="d9de6-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="d9de6-105">Csoporttagként foglahatja le az erőforrást, és hozzárendelheti egy feladathoz.</span><span class="sxs-lookup"><span data-stu-id="d9de6-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="d9de6-106">Vagy hozzon létre egy általános csoporttagot a feladatok szerepkör-hozzárendelésén keresztül, hozzon létre egy csoportot, majd teljesítse a mögöttes követelményt egy elnevezett erőforrással.</span><span class="sxs-lookup"><span data-stu-id="d9de6-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="d9de6-107">Megjegyzés: ha szeretne egy lefoglalható erőforrást hozzárendelni egy feladathoz, a foglalható erőforrás-csoport tagjának elegendő foglalással kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="d9de6-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="d9de6-108">A foglalás állapotának a következőnek kell lennie: Véglegesítés típusa –Végleges lefoglalás és Állapot – Véglegesített.</span><span class="sxs-lookup"><span data-stu-id="d9de6-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="d9de6-109">Nem nincs elegendő foglalás az erőforráshoz, a Project Service eltávolítja a hozzárendelést, és megjeleníti a következő hibaüzenetet:</span><span class="sxs-lookup"><span data-stu-id="d9de6-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="d9de6-110">*Erőforrás hozzárendelése feladathoz sikertelen – A következő erőforrások nem rendelkeznek elegendő lefoglalt órával a projekthez*</span><span class="sxs-lookup"><span data-stu-id="d9de6-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="d9de6-111">Az erőforrás lefoglalása csoporttagként, és az erőforrás hozzárendelése egy feladathoz</span><span class="sxs-lookup"><span data-stu-id="d9de6-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="d9de6-112">Ennél a módszernél a projektcsoporthoz ad egy erőforrást, és feladatokat rendel hozzá az erőforráshoz a projektütemezésben.</span><span class="sxs-lookup"><span data-stu-id="d9de6-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="d9de6-113">Ennek módja itt található:</span><span class="sxs-lookup"><span data-stu-id="d9de6-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="d9de6-114">A csoport tagja rácson adjon hozzá egy új csoporttagot a következő kiválasztásával: **Új**.</span><span class="sxs-lookup"><span data-stu-id="d9de6-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="d9de6-115">A csoport tagja gyorslétrehozás képernyőn jelölje ki a foglalható erőforrás nevét, majd állítsa be a szerepkört.</span><span class="sxs-lookup"><span data-stu-id="d9de6-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="d9de6-116">Jelölje ki a **Kezdő** és **Befejező** dátumokat.</span><span class="sxs-lookup"><span data-stu-id="d9de6-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="d9de6-117">![Egy csapattag hozzáadásának képernyőképe](media/FAQ-Resources-to-Tasks2-1.png "Egy csapattag hozzáadásának képernyőképe")</span><span class="sxs-lookup"><span data-stu-id="d9de6-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="d9de6-118">A következő hozzárendelési módok közül választhat az erőforrás foglalásához:</span><span class="sxs-lookup"><span data-stu-id="d9de6-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="d9de6-119">**Teljes kapacitás** – legfoglalja az erőforrás teljes kapacitását a megadott kezdő és záró dátum között.</span><span class="sxs-lookup"><span data-stu-id="d9de6-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="d9de6-120">**Százalékos kapacitás** – legfoglalja az erőforrást az erőforrás kapacitásának bizonyos százalékára a megadott kezdő és záró dátum között.</span><span class="sxs-lookup"><span data-stu-id="d9de6-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="d9de6-121">**Órák egyenletes elosztásával** – legfoglalja az erőforrást bizonyos mennyiségű órára, amelyeket egyenletesen oszt el naponta a megadott kezdő és záró dátum között.</span><span class="sxs-lookup"><span data-stu-id="d9de6-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="d9de6-122">**Órák lefoglalása minél hamarabb** – legfoglalja az erőforrást bizonyos mennyiségű órára, minél gyorsabban felhasználva a napi órákat a megadott kezdő és záró dátum között.</span><span class="sxs-lookup"><span data-stu-id="d9de6-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="d9de6-123">Ne válassza a **Nincs** lehetőséget, mert az erőforrást hozzáadja a csoporthoz, de nem hoz létre a foglalásokat, amelyek felveszik az erőforrás kapacitását.</span><span class="sxs-lookup"><span data-stu-id="d9de6-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="d9de6-124">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="d9de6-124">Select **Save**.</span></span>

    <span data-ttu-id="d9de6-125">Vegye figyelembe, hogy a lefoglalás óráinak elégnek kell lenniük arra, hogy lefedjék a munkaórákat és a dátumtartományokat a feladatokhoz, amelyekhez hozzárendeli az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="d9de6-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="d9de6-126">Ha nincsenek összhangban, az erőforrást nem rendelhett a feladathoz.</span><span class="sxs-lookup"><span data-stu-id="d9de6-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="d9de6-127">A feladat munkalebontási struktúráján (WBS) kattintson az erőforrás cella legördülő listájára.</span><span class="sxs-lookup"><span data-stu-id="d9de6-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="d9de6-128">Ekkor:</span><span class="sxs-lookup"><span data-stu-id="d9de6-128">Then:</span></span> 

    1. <span data-ttu-id="d9de6-129">Válassza a **Hozzáadás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d9de6-129">Select **Add**.</span></span>
    2. <span data-ttu-id="d9de6-130">Válassza a legördülő listát az **Erőforrások** alatt, és jelölje ki a fenti hozzáadott csoporttagot.</span><span class="sxs-lookup"><span data-stu-id="d9de6-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="d9de6-131">Kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="d9de6-131">Select **OK**.</span></span> <span data-ttu-id="d9de6-132">A csoport tagja most már hozzá van rendelve a feladathoz.</span><span class="sxs-lookup"><span data-stu-id="d9de6-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="d9de6-133">![Erőforrások WBS-sel hozzáadásának képernyőképe](media/FAQ-Resources-to-Tasks2-2.png "Erőforrások WBS-sel hozzáadásának képernyőképe")</span><span class="sxs-lookup"><span data-stu-id="d9de6-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="d9de6-134">A csoport tagja rácson megjelenik az erőforrás összesített hozzárendelt óraszáma a Hozzárendelt órák alatt.</span><span class="sxs-lookup"><span data-stu-id="d9de6-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="d9de6-135">Az óraszám kisebb vagy egyelnő lesz, mint az erőforrás a lefoglalt óráinak száma.</span><span class="sxs-lookup"><span data-stu-id="d9de6-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="d9de6-136">![Erőforráshoz rendelt munkaórák képernyőképe](media/FAQ-Resources-to-Tasks2-3.png "Erőforráshoz rendelt munkaórák képernyőképe")</span><span class="sxs-lookup"><span data-stu-id="d9de6-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="d9de6-137">Ha az erőforráshoz hozzárendelni kívánt feladat az erőforrás-foglalások záró dátuma után kezdődik, az erőforrás nem jelenik meg a legördülő listában.</span><span class="sxs-lookup"><span data-stu-id="d9de6-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="d9de6-138">Megjegyzés: hozzárendelhet egy erőforrást a lefoglalt óráknál több órához, ha az erőforrás némi fennmaradó nem hozzárendelt kapacitással rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="d9de6-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="d9de6-139">Ebben az esetben az erőforrás csak részben lesz hozzárendelve a foglalások maximumáig.</span><span class="sxs-lookup"><span data-stu-id="d9de6-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="d9de6-140">Megtekintheti a fennmaradó nem hozzárendelt feladatórákat a Személyzet nélküli órák oszlopot hozzáad a munkalebontási struktúrához.</span><span class="sxs-lookup"><span data-stu-id="d9de6-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="d9de6-141">Ha az erőforrások hozzá vannak rendelve a lefoglalt órák maximumáig (a lefoglat órák száma egyenlő a hozzárendelt órákkal), a következő hibaüzenetet fogja látni, amikor megkísérel további feladatok hozzájuk rendelni:</span><span class="sxs-lookup"><span data-stu-id="d9de6-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="d9de6-142">*Erőforrás hozzárendelése feladathoz sikertelen – A következő erőforrások nem rendelkeznek elegendő lefoglalt órával a projekthez.*</span><span class="sxs-lookup"><span data-stu-id="d9de6-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="d9de6-143">Ezenkívül az alapértelmezett projektvezető csoporttag, aki a a projekt létrehozásakor van hozzáadva a csoporthoz, bármely lefoglalás nélkül van hozzáadva, és nem rendelhető hozzá semmilyen feladathoz.</span><span class="sxs-lookup"><span data-stu-id="d9de6-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="d9de6-144">Nem jelenik meg az erőforrás legördülő menüjében a feladatokhoz.</span><span class="sxs-lookup"><span data-stu-id="d9de6-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="d9de6-145">Ha hozzá szeretné rendelni ezt az erőforrást, el kell távolítani a csoportból, és ezután adja hozzá újra egy hozzárendelés módszerrel, amely eltérő a „Nincs”-től.</span><span class="sxs-lookup"><span data-stu-id="d9de6-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="d9de6-146">A projekt létrehozásakor azért van hozzáadva a csoporthoz, hogy a projekt legalább egy projektjóváhagyóval rendelkezzen alapértelmezés szerint.</span><span class="sxs-lookup"><span data-stu-id="d9de6-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="d9de6-147">Egy általános csoporttag létrehozása szerepkör-hozzárendeléssel a feladatokon</span><span class="sxs-lookup"><span data-stu-id="d9de6-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="d9de6-148">Ez a módszer biztosítja, hogy az erőforrásoknak elég foglalásuk legyen a feladatokhoz.</span><span class="sxs-lookup"><span data-stu-id="d9de6-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="d9de6-149">Első lépésként hozzon létre egy helyőrző vagy általános erőforrást, amely leírja annak az elnevezett erőforrásnak a jellemzőit, akit végső soron a feladaton végzett munkával akar megbízni, egy csoport létrehozásával szerepkörök hozzárendelése után a feladatokhoz.</span><span class="sxs-lookup"><span data-stu-id="d9de6-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="d9de6-150">Ennek módja itt található:</span><span class="sxs-lookup"><span data-stu-id="d9de6-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="d9de6-151">Jelöljön be egy feladatot a munkalebontási struktúrában.</span><span class="sxs-lookup"><span data-stu-id="d9de6-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="d9de6-152">Jelölje ki a **Hozzárendelt szerepkör** legördülő ikont az erőforráscellában.</span><span class="sxs-lookup"><span data-stu-id="d9de6-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="d9de6-153">Válassza a **Szerepkör** legördülő listát, és jelölje ki a szerepkört az általános erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="d9de6-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="d9de6-154">Kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="d9de6-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="d9de6-155">![Képernyőfotó: WBS használata erőforrás hozzáadásához](media/FAQ-Resources-to-Tasks2-4.png "Képernyőfotó: WBS használata erőforrás hozzáadásához")</span><span class="sxs-lookup"><span data-stu-id="d9de6-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="d9de6-156">Miután befejezte a WBS segítségével a szerepkörök hozzárendelését a feladatokhoz, válassza ezt: **Projektcsoport létrehozása**.</span><span class="sxs-lookup"><span data-stu-id="d9de6-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="d9de6-157">A Project Service létrehozza a minimális számú általános csoporttagot a szerepkörök alapján, erőforrás-szervezeti egységek és a projektnaptár alapján, a feladat-hozzárendelések összesítésével.</span><span class="sxs-lookup"><span data-stu-id="d9de6-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="d9de6-158">![Képernyőfotó: projektcsoport generálása](media/FAQ-Resources-to-Tasks2-5.png "Képernyőfotó: projektcsoport generálása")</span><span class="sxs-lookup"><span data-stu-id="d9de6-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="d9de6-159">A Csoporttag rácsban látni fogja az általános erőforrástípusú erőforrásokat a szerepkör és a pozíció nevével.</span><span class="sxs-lookup"><span data-stu-id="d9de6-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="d9de6-160">Ha a munka elvégzéséhez két erőforrás szükséges egy szerepkörhoz, a Csoport létrehozása funkció két csoporttagot hoz létre, és a pozíció neve segítségével különbözteti meg őket.</span><span class="sxs-lookup"><span data-stu-id="d9de6-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="d9de6-161">![Képernyőkép: két általános erőforrás hozzáadása](media/FAQ-Resources-to-Tasks2-6.png "Képernyőkép: két általános erőforrás hozzáadása")</span><span class="sxs-lookup"><span data-stu-id="d9de6-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="d9de6-162">Az Erőforrás-követelmény alatt található hivatkozás kiválasztásával megnyithatja az általános csoporttag mögöttes erőforrás-követelményeit.</span><span class="sxs-lookup"><span data-stu-id="d9de6-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="d9de6-163">![Képernyőkép: támogató erőforráskövetelmény megnyitása](media/FAQ-Resources-to-Tasks2-7.png "Képernyőkép: támogató erőforráskövetelmény megnyitása")</span><span class="sxs-lookup"><span data-stu-id="d9de6-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="d9de6-164">Jelölje be a **Foglalás** elemet az általános erőforráshoz, és aztán az ütemezési tábla használatával kereshet és foglalhat le egy tényleges erőforrást.</span><span class="sxs-lookup"><span data-stu-id="d9de6-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="d9de6-165">A **Kérelem küldése** kiválasztásával el is küldheti a követelményt egy erőforrás-menedzser általi teljesítésre.</span><span class="sxs-lookup"><span data-stu-id="d9de6-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="d9de6-166">Ha az általános erőforrás teljesítése elnevezett erőforrással történik, az általános erőforrás törlődik a csoportból, és az általános erőforrás feladat-hozzárendelései az elnevezett erőforráshoz lesznek rendelve, aki végrehajtotta az általán erőforrás erőforrás-követelményét.</span><span class="sxs-lookup"><span data-stu-id="d9de6-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

