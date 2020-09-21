---
title: Erőforrások kezelése
description: Ez a témakör információkat nyújt az erőforrások kezeléséről.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 39893019-123b-4bc6-8a2b-a37bc517dc97
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 6c199cbadd1c78e7e29c0cda0febde4236a13d96
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752313"
---
# <a name="manage-resources"></a><span data-ttu-id="8cd3f-103">Erőforrások kezelése</span><span class="sxs-lookup"><span data-stu-id="8cd3f-103">Manage resources</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8cd3f-104">A Dynamics 365 Project Service Automation tartalmaz egy erőforrás-kezelő irányítópultot, amely vizuális áttekintést nyújt az erőforrásigényről és -felhasználásról a szervezet egészében.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="8cd3f-105">Az irányítópult diagramjait felhasználhatja a következő információk megjelenítésére:</span><span class="sxs-lookup"><span data-stu-id="8cd3f-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="8cd3f-106">**Erőforrásigény** - Az **Aktív erőforrásigény** azokat a erőforrásokat mutatja, amelyeket benyújtottak.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="8cd3f-107">Az erőforrásokat szerepkör vagy projekt szerint összesíti.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="8cd3f-108">**Nem benyújtott erőforrásigény** - A **Hozzá nem rendelt erőforrásigény** ábra az összes, még nem benyújtott erőforrásigényt mutatja.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="8cd3f-109">Segít az erőforrás-kezelőknek megtekinteni a nem biztos igényeket, amelyeket erőforrás-kéréssel nyújthatnak be.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="8cd3f-110">**Számlázható felhasználás az elmúlt héten** - A **Használat szerep szerint** táblázat mutatja a szervezet tényleges számlázható felhasználásának százalékos arányát a szerepenkénti számlázandó felhasználás százalékában.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8cd3f-111">A **Használat szerep szerint** diagram elérhetővé tételéhez hozzon létre egy munkát, amely futtatja az UpdateRoleUtilization munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="8cd3f-112">Ez az ismétlődő munka hét naponként fut, hogy kiszámítsa a számlázható felhasználást az előző hét napra.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="8cd3f-113">Az eredményeket szerep szerint csoportosítják.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="8cd3f-114">Kezelje a projektcsoport tagjait</span><span class="sxs-lookup"><span data-stu-id="8cd3f-114">Manage project team members</span></span>

<span data-ttu-id="8cd3f-115">A projektmenedzserek az erőforrás-kezelő irányítópultját használhatják a projektek erőforrásainak kezelésére.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="8cd3f-116">Például felvehetnek egy csapattagot közvetlenül egy projektbe, és lefoglalhatják a csapattagot egy általános erőforrás által elfoglalt erőforrás-követelmények teljesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="8cd3f-117">Csapattag hozzáadása közvetlenül egy projekthez</span><span class="sxs-lookup"><span data-stu-id="8cd3f-117">Add a team member directly to a project</span></span>

<span data-ttu-id="8cd3f-118">Csapattag közvetlen hozzáadásához a projekthez a **Projektek** oldalon, a **Csapat** lapon válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="8cd3f-119">Megjelenik a **Gyors létrehozás: Projektcsapattag** párbeszédpanel.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="8cd3f-120">Ezen a párbeszédpanelen a következő feladatokat hajthatja végre:</span><span class="sxs-lookup"><span data-stu-id="8cd3f-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="8cd3f-121">**Megnevezett erőforrás foglalása** - A **Foglalható erőforrás** mezőben válassza ki az erőforrás nevét.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="8cd3f-122">Ezután válassza ki a szerepet, állítsa be az időszakot, és válassza ki az allokációs módszert.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="8cd3f-123">A kiválasztott megnevezett erőforrás hozzáadódik a projekthez a kiválasztott elosztási módszer és az erőforrásnaptár használatával.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="8cd3f-124">**Általános erőforrás hozzáadása** - Hagyja üresen a **Foglalható erőforrás** mezőt, majd válassza ki a szerepet, állítsa be az időszakot, és válassza ki a preferált allokációs módszert.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="8cd3f-125">Általános erőforrást adunk a csoporthoz helyőrzőként, hogy megőrizzük a csoportban megnevezett erőforrások könyvelésére szolgáló igénymintát.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="8cd3f-126">A követelményt a projekt naptárának megfelelően kell megtenni.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="8cd3f-127">**Adjon meg egy elnevezett erőforrást a csapatnak erőforrás-kapacitás felhasználása nélkül** - A **Foglalható erőforrás** mezőben válassza ki az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="8cd3f-128">Ezután válassza ki az időszakot, és válassza a **Nincs** lehetőséget allokációs módszerként.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="8cd3f-129">Az erőforrás hozzáadódik a csapathoz, de az erőforrás kapacitása nem merül fel a foglalás során.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="8cd3f-130">Csapattag lefoglalása az általános erőforrás erőforrásigényének teljesítéséhez</span><span class="sxs-lookup"><span data-stu-id="8cd3f-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="8cd3f-131">A PSA-ban egy általános erőforrást lefoglalhat egy projektcsoportra, és meghatározhatja a szerepet, a szükséges kapacitást és a kapacitás elosztását.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="8cd3f-132">Az erőforrás-igénynél meghatározhatja az általános erőforráshoz társított attribútumokat.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="8cd3f-133">Ezek a tulajdonságok tartalmazzák a szükséges készségeket, az előnyben részesített szervezeti egységet és az előnyben részesített erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="8cd3f-134">Kövesse ezeket a lépéseket a fejlesztői általános erőforráshoz szükséges készségek meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="8cd3f-135">A **Projektek** oldalon, a **Csapat** lapon válassza az **Új** lehetőséget egy általános forrás lefoglalásához.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Általános erőforrás lefoglalva a csapatra](media/Resource-Management-image9.png)

2. <span data-ttu-id="8cd3f-137">A **Minden csapattag** nézetben, az **Erőforrásigény** oszlopban válassza ki a hivatkozást a szükséges készségek hozzáadásához az általános erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Követelmény hivatkozás](media/Resource-Management-image10.png)

3. <span data-ttu-id="8cd3f-139">A megjelenő **Erőforrásigény** oldalon a **Tudás** rácsban válassza ki a három pontot (**...**), majd válassza az **Új igényjellemző hozzáadása** lehetőséget a szükséges képességek fejlesztőhöz való hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Új igényjellemző parancs hozzáadása](media/Resource-Management-image11.png)

4. <span data-ttu-id="8cd3f-141">A megjelenő **Gyors létrehozás: Követelményjellemző** párbeszédpanelen a **Jellemző** mezőben válassza ki a szükséges képességeket.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="8cd3f-142">Ezután az **Értékelés** mezőben válassza ki az adott készséghez szükséges jártassági szintet.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="8cd3f-143">Végül, az **Erőforrásigény** mezőben állítsa be az erőforrások forrásának követelményét a szervezeti egységektől, vagy akár a megnevezett erőforrásokat is.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="8cd3f-144">Ha kész, válassza a **Mentés**lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-144">When you've finished, select **Save**.</span></span>

    ![Gyors létrehozás: Követelményjellemző párbeszédpanel](media/Resource-Management-image12.png)

5. <span data-ttu-id="8cd3f-146">A **Forrásigény** oldalon válassza a **Foglalás** elemet az erőforrásigény teljesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Foglalás gomb az erőforrásigény oldalon](media/Resource-Management-image13.png)

    <span data-ttu-id="8cd3f-148">Kiválaszthatja az általános erőforrást a **Minden csapat tagja** rácsból, majd a **Foglalás** lehetőséget választhatja.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![A Minden csoport tagja rács felett található Foglalás gomb](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="8cd3f-150">Ebben a példában 40 szükséges óra van, de nincs ténylegesen lekötött óra, mivel az általános forrásoknak nincs foglalása.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="8cd3f-151">Ezenkívül nincsenek kijelölt órák, mivel az általános erőforrást közvetlenül a csapathoz adták hozzá.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="8cd3f-152">Nem a feladat-hozzárendeléssel adták hozzá.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="8cd3f-153">Az **Ütemezési asszisztens** oldalon a rendelkezésre álló erőforrásokat az erőforrásigényben megadott követelmények szerint szűrheti.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="8cd3f-154">Az erőforrásokat az Ütemezési táblán megadott rendezési paraméterek szerint rendezzük.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Ütemezési asszisztens oldal](media/Resource-Management-image15.png)

    <span data-ttu-id="8cd3f-156">Itt található néhány gyakran használt szűrő:</span><span class="sxs-lookup"><span data-stu-id="8cd3f-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="8cd3f-157">**Jellemzők és minősítés** - Szűrés készségek, igazolások és egyéb erőforrás-tulajdonságok alapján, a jártassági besoroláson felül.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="8cd3f-158">**Szerepek** - Szűrés az alapértelmezett szerepek szerint, amelyek a foglalható forrásokhoz vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="8cd3f-159">**Szervezeti egységek** - Foglalható erőforrások szűrése szervezeti egységek szerint, amelyekhez hozzá vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="8cd3f-160">Ha nem elégedett a kezdeti keresési eredményekkel, megváltoztathatja a szűrési kritériumokat.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="8cd3f-161">Bontsa ki a bal oldalon a **Szűrő nézet** ablakot, majd válassza a **Keresés** lehetőséget további források kereséséhez.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Nézet szűrése ablaktábla](media/Resource-Management-image16.png)

7. <span data-ttu-id="8cd3f-163">Az eredmények rendezésének megváltoztatásához válassza a **Rendezés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Rendezés parancs](media/Resource-Management-image17.png)

8. <span data-ttu-id="8cd3f-165">Válassza ki az erőforrásokat a követelményben megadott igénynek megfelelően, a rács tetején feltüntetett módon.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="8cd3f-166">Törölheti a cellák kiválasztását a rácsban, és nyitva hagyhatja az erőforrás-kapacitást.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="8cd3f-167">Egyszerre csak egy erőforrás választható lefoglaltként.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="8cd3f-168">Válassza a **Foglalás** lehetőséget a kiválasztott erőforrás lefoglalásához, és hagyja nyitva az Ütemezési táblát, hogy további erőforrásokat válasszon ki.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="8cd3f-169">Alternatív megoldásként válassza a **Foglalás és kilépés** lehetőséget a kiválasztott erőforrás lefoglalásához és az Ütemezési tábla bezárásához.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Foglalni kívánt erőforrás](media/Resource-Management-image19.png)

    <span data-ttu-id="8cd3f-171">Értesítést kap a lefoglalt órákról.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="8cd3f-172">Az igény mutatói megmutatják, hogy a foglalási követelmény mennyire teljesül, és mennyi marad.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="8cd3f-173">Láthatja azt is, hogy mekkora a kiválasztott erőforrás kapacitása.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="8cd3f-174">Válassza a **Kibontás** lehetőséget az erőforrás-foglalás részletesebb megjelenítéséhez.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="8cd3f-175">Térjen vissza a **Minden csapattag** nézethez.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="8cd3f-176">A rácsban vegye észre, hogy az általános erőforrást felváltotta a megnevezett erőforrás, és a 40 órát az erőforrás lekötöttként sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Frissített Összes csapattag rács](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="8cd3f-178">A hozzárendelt órák nem kerülnek megjelenítésre, mert közvetlenül a csapatra voltak foglalva.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="8cd3f-179">Nem feladat-hozzárendeléssel foglaltak őket.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="8cd3f-180">Általános erőforrások rendelése a feladatokhoz és az erőforrás-követelmények generálása</span><span class="sxs-lookup"><span data-stu-id="8cd3f-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="8cd3f-181">A PSA-ban létrehozhat feladatokat, majd általános erőforrásokat rendelhet hozzájuk.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="8cd3f-182">Ily módon az erőforrásigényt helyőrzők képviselhetik, miközben becsülheti az ütemtervet és a pénzügyi számokat.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="8cd3f-183">Ezután generálhat erőforrásigényeket az általános erőforrásokhoz, és teljesítheti azokat.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="8cd3f-184">A **Projektek** oldalon, az **Ütemezés** lapon válassza a **Hozzáadás** lehetőséget a feladat létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Új feladat létrehozva](media/Resource-Management-image21.png)

2. <span data-ttu-id="8cd3f-186">Az **Erőforrások** mezőben válassza az **Erőforrás-választó** szimbólumot.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="8cd3f-187">Megjelenik az Erőforrás-választó, amely megmutatja a projekt meglévő csapattagjait.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Erőforrás-választó](media/Resource-Management-image22.png)

3. <span data-ttu-id="8cd3f-189">Írja be az új általános erőforrás nevét, majd válassza a **Létrehozás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![A beírt új általános erőforrás neve](media/Resource-Management-image23.png)

4. <span data-ttu-id="8cd3f-191">A megjelenő **Gyors létrehozás: Projektcsapattag** párbeszédpanelen a **Szerep** mezőben válassza ki az általános erőforrás szerepét.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="8cd3f-192">Az **Erőforrásegység** mezőben válassza ki az általános erőforrás szervezeti egységét.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="8cd3f-193">Azután válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-193">Then select **Save**.</span></span>

    ![Gyors létrehozás: Projektcsoporttag párbeszédpanel](media/Resource-Management-image24.png)

    <span data-ttu-id="8cd3f-195">Az általános csoporttagot most kiosztották a feladathoz.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-195">The generic team member is now assigned to the task.</span></span>

    ![A feladathoz kijelölt általános csapattag](media/Resource-Management-image25.png)

    <span data-ttu-id="8cd3f-197">A **Csapat** lapon láthatja az új általános csapattagot.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="8cd3f-198">Vegye észre, hogy csak órákat adott meg.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="8cd3f-199">Ezek az órák az összes feladat összegét adják, amelyeket az általános csapattagnak kiosztottak.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="8cd3f-200">Az általános csapattagnak még nincs szüksége órára vagy erőforrás-igényre.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Általános csapattag a Csapat lapon](media/Resource-Management-image26.png)

5. <span data-ttu-id="8cd3f-202">Most az Erőforrás-választó segítségével hozzárendelheti az általános csapattagot más feladatokhoz.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Általános csapattag az Erőforrás-választóban](media/Resource-Management-image27.png)

    <span data-ttu-id="8cd3f-204">Ha befejezte az általános erőforrás hozzárendelését a feladatokhoz, generálhat egy erőforrás-követelményt az általános erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="8cd3f-205">A **Csapat** lapon válassza ki az általános erőforrást, majd válassza a **Követelmény generálása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Követelmény generálása parancs](media/Resource-Management-image28.png)

    <span data-ttu-id="8cd3f-207">A követelmény előállításakor az általános csapattagnak rendelkeznie kell a szükséges órákkal és egy linkkel az erőforrás-igényhez.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Erőforrás-igény hivatkozás](media/Resource-Management-image29.png)

    <span data-ttu-id="8cd3f-209">Miután egy megnevezett erőforrást lekötött, az általános erőforrás eltávolításra kerül a csapatból, és helyébe a megnevezett erőforrás kerül.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Az általános erőforrás helyébe a megnevezett erőforrás lép](media/Resource-Management-image30.png)

    <span data-ttu-id="8cd3f-211">Az **Ütemezés** lapon az általános erőforrás-hozzárendelések eltávolításra kerülnek, és helyébe a megnevezett erőforrás lép.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Általános erőforrás-hozzárendelések az Ütemezés lapon megnevezett erőforrásokkal helyettesítve](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="8cd3f-213">Ez a viselkedés csak akkor fordul elő, ha a megnevezett erőforrást teljes mértékben lefoglalják az általános erőforrás-igényre.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="8cd3f-214">Ha egy megnevezett erőforrás részben helyettesíti az általános erőforrás-igényt, vagy több megnevezett erőforrás helyettesíti az általános erőforrás-követelményt, akkor az általános erőforrás továbbra is hozzá van rendelve a feladathoz.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="8cd3f-215">A következő ábrán egy 80 órás feladatot terveztek ötnapos időtartamra (napi 16 óra öt nap alatt), és hozzárendelték a **Funkcionális** nevű általános erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![Nyolcvan órás, ötnapos feladat a Funkcionális általános erőforráshoz rendelve](media/Resource-Management-image32.png)

    <span data-ttu-id="8cd3f-217">Amikor előállítja a követelményt, akkor az 80 órára szól öt napon keresztül.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![80 órára, öt napra generált követelmény](media/Resource-Management-image33.png)

    <span data-ttu-id="8cd3f-219">Mivel a rendelkezésre álló erőforrások napi nyolc órán keresztül működnek, két erőforrásra van szükség a követelmény teljesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Második erőforrás](media/Resource-Management-image35.png)

    <span data-ttu-id="8cd3f-221">A **Csapat** lapon most láthatja, hogy az általános erőforrásnak nincs kötelező órája, de a hozzárendelt órák továbbra is megjelennek a teljesítést alkotó két megnevezett erőforrással együtt.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Két megnevezett erőforrás a Csapat lapon](media/Resource-Management-image36.png)

    <span data-ttu-id="8cd3f-223">Az **Ütemezés** lapon az általános erőforrás továbbra is hozzá van rendelve a feladathoz.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Általános erőforrások az Ütemezés lapon](media/Resource-Management-image37.png)

<span data-ttu-id="8cd3f-225">A PSA nem rendeli hozzá mindkét erőforrást a feladathoz, mert ez a viselkedés kevésbé kiszámítható ütemezést eredményezne.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="8cd3f-226">Ebben az egyszerű példában könnyű elosztani az órákat két erőforrás között.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="8cd3f-227">Az összetettebb forgatókönyvekben, amelyek több feladatot és több erőforrást foglalnak magukban, a PSA-nak feltételezéseket kell tennie arra vonatkozóan, hogy hogyan kell elosztani a több erőforráshoz kapott foglalásokat több feladat között.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="8cd3f-228">Ezért ezekben a forgatókönyvekben a projektmenedzser felel a többszörös foglalás elemzéséért és a szükséges hozzárendeléséért.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="8cd3f-229">A foglalások kiosztásához a projektmenedzser az általános erőforrásokból a megnevezett erőforrásokhoz rendeli a feladatokat, majd az **Összehangolás** nézetet használja annak ellenőrzésére, hogy az allokáció a foglalásokkal együtt működik-e.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="8cd3f-230">Erőforrásigény szerkesztése</span><span class="sxs-lookup"><span data-stu-id="8cd3f-230">Edit a resource requirement</span></span>

<span data-ttu-id="8cd3f-231">Az erőforrásigény létrehozása után a projektmenedzser vagy az erőforrás-kezelő módosíthatja a részleteket, hogy finomítsa a keresési feltételeket az Ütemezési tábla használatakor.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="8cd3f-232">Az erőforrásigény szerkesztéséhez kövesse ezeket a lépéseket.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="8cd3f-233">A **Projektek** oldalon, a **Csapat** lapon válassza ki az általános erőforrás követelményeinek hivatkozását.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="8cd3f-234">A megjelenő **Erőforrásigény** oldalon frissíthet több attribútumot.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="8cd3f-235">Íme néhány példa:</span><span class="sxs-lookup"><span data-stu-id="8cd3f-235">Here are some examples:</span></span>

    - <span data-ttu-id="8cd3f-236">Név</span><span class="sxs-lookup"><span data-stu-id="8cd3f-236">Name</span></span>
    - <span data-ttu-id="8cd3f-237">Kezdő dátum</span><span class="sxs-lookup"><span data-stu-id="8cd3f-237">From Date</span></span>
    - <span data-ttu-id="8cd3f-238">Befejezési dátum</span><span class="sxs-lookup"><span data-stu-id="8cd3f-238">To Date</span></span>
    - <span data-ttu-id="8cd3f-239">Időtartam</span><span class="sxs-lookup"><span data-stu-id="8cd3f-239">Duration</span></span>
    - <span data-ttu-id="8cd3f-240">Erőforrás típusa</span><span class="sxs-lookup"><span data-stu-id="8cd3f-240">Resource Type</span></span>

<span data-ttu-id="8cd3f-241">Az **Erőforrásigény** oldalon a projektmenedzser vagy az erőforrás-kezelő a következő információkat is meghatározhatja:</span><span class="sxs-lookup"><span data-stu-id="8cd3f-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="8cd3f-242">Képességek</span><span class="sxs-lookup"><span data-stu-id="8cd3f-242">Skills</span></span>
- <span data-ttu-id="8cd3f-243">Szerepkörök</span><span class="sxs-lookup"><span data-stu-id="8cd3f-243">Roles</span></span>
- <span data-ttu-id="8cd3f-244">Erőforrás-preferenciák</span><span class="sxs-lookup"><span data-stu-id="8cd3f-244">Resource preferences</span></span>
- <span data-ttu-id="8cd3f-245">Előnyben részesített szervezeti egység</span><span class="sxs-lookup"><span data-stu-id="8cd3f-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="8cd3f-246">Frissítse az erőforrás-foglalásokat, miután azokat egy projektre lefoglalták</span><span class="sxs-lookup"><span data-stu-id="8cd3f-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="8cd3f-247">Miután hozzáadott egy általános vagy megnevezett erőforrást egy projektcsoporthoz, megváltoztathatja az erőforrás foglalásait.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="8cd3f-248">A **Projektek** oldalon, a **Csapat** lapon válassza ki a csapattagot, majd válassza a **Foglalás fenntartása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Ütemezési tábla nyitva a kiválasztott csapattag számára](media/Resource-Management-image40.png)

    <span data-ttu-id="8cd3f-250">Megjelenik az Ütemezési tábla, amely megmutatja a projektcsoport tagjainak foglalásait.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="8cd3f-251">Bővítse a csapattag rekordját, hogy megnézhesse az órákat, amelyeket ez a projekt és más projektek foglaltak le, felhasználva a csapattag kapacitását.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="8cd3f-252">Válassza ki és húzza el a foglalást annak meghosszabbításához vagy rövidítéséhez.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="8cd3f-253">Megjelenik egy **Erőforrás-foglalás létrehozása** párbeszédpanel, amely lehetővé teszi a foglalás módosítását.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Erőforrás-foglalás létrehozása párbeszédpanel](media/Resource-Management-image41.png)

3. <span data-ttu-id="8cd3f-255">Kattintson a jobb gombbal a foglalásra.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-255">Right-click the booking.</span></span> <span data-ttu-id="8cd3f-256">Ezután a helyi menü segítségével elvégezheti a következő műveleteket:</span><span class="sxs-lookup"><span data-stu-id="8cd3f-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="8cd3f-257">A foglalás állapotának módosítása.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-257">Change the booking status.</span></span>
    - <span data-ttu-id="8cd3f-258">A foglalás szerkesztése.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-258">Edit the booking.</span></span>
    - <span data-ttu-id="8cd3f-259">Egy erőforrás helyettesítése a projektcsoportban.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="8cd3f-260">A foglalás állapotának módosítása</span><span class="sxs-lookup"><span data-stu-id="8cd3f-260">Change the booking status</span></span>

<span data-ttu-id="8cd3f-261">Az alapértelmezett vagy az egyéni foglalás állapotának módosítása.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-261">You can change any default or custom booking status.</span></span>

![Állapot módosítása parancs](media/Resource-Management-image42.png)

<span data-ttu-id="8cd3f-263">A PSA a következő állapotokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="8cd3f-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="8cd3f-264">**Törölve** - Ez az állapot visszavonja egy erőforrás foglalását, és felszabadítja az erőforrás kapacitását.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="8cd3f-265">**Nehéz foglalás** - Ez az állapot felhasználja az erőforrás kapacitását.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="8cd3f-266">A foglalás jellemzően akkor veszi fel ezt az állapotot, amikor megnyitja a **Foglalás fenntartása** panelt a **Minden csapattag** rácsból a **Projektek** oldalon.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="8cd3f-267">**Puha foglalás** - Ez az állapot hozzáad egy erőforrást a csapathoz, de nem használja fel az erőforrás kapacitását.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="8cd3f-268">Ez azt jelzi, hogy az erőforrást fenntartották a lehetséges munkavégzéshez, de még mindig rendelkezik kapacitással, ha más munkákhoz szükséges.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="8cd3f-269">Az általános erőforrás-rendelkezésre állás szempontjából a puha foglalások eltérő státusszal rendelkeznek, mint a kemény foglalások.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="8cd3f-270">**Javasolt** - Ez az állapot egy erőforrás-menedzser vagy projektmenedzser erőforrásra tett javaslatát reprezentálja.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="8cd3f-271">A javaslatok nem használják fel egy erőforrás kapacitását, és az erőforrás nem kerül hozzáadásra a projekt csapatához.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="8cd3f-272">Annak érdekében, hogy az erőforrást a csapatba foglalhassák, a projektmenedzsernek el kell fogadnia a javaslatot.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="8cd3f-273">Erőforrás-kérelmek elküldése</span><span class="sxs-lookup"><span data-stu-id="8cd3f-273">Submit resource requests</span></span>

<span data-ttu-id="8cd3f-274">Az erőforrás-kérelmek a kereslet (erőforrás-igény) teljesítésére szolgálnak, amelyet az erőforrás-kezelőnek teljesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="8cd3f-275">Ha egy általános erőforrás már létezik a csapatban, akkor közvetlenül küldhet erőforrás-kérelmet.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-275">For a generic resource thta is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="8cd3f-276">Az erőforrás-igényt kétféle módon lehet teljesíteni:</span><span class="sxs-lookup"><span data-stu-id="8cd3f-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="8cd3f-277">Az erőforrás-kezelő közvetlenül teljesíti a kérést.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="8cd3f-278">Ebben az esetben az általános erőforrást egy kemény foglalás váltja fel, amelynek megnevezett erőforrása van.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="8cd3f-279">Az erőforrás-kezelő erőforrást javasol a projektmenedzser számára, a projektvezető pedig jóváhagyja vagy elutasítja a javasolt erőforrást.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="8cd3f-280">Az erőforrás-kérelmek közvetlen teljesítése</span><span class="sxs-lookup"><span data-stu-id="8cd3f-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="8cd3f-281">Amikor egy erőforrásigény keletkezik, a projekt vezetője benyújthat egy erőforrásigényt egy általános erőforrásra az erőforrás kiválasztásával, majd az **Igény benyújtása** ponttal.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Igény benyújtása gomb](media/Resource-Management-image45.png)

<span data-ttu-id="8cd3f-283">Az erőforrással kapcsolatos megjegyzéseket meg lehet adni az erőforrás-kezelőnek, aki teljesíti a kérést.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="8cd3f-284">Az igény benyújtása után a csapattag **Állapot** mezője **Beküldve** lesz.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Opcionális megjegyzések beírása](media/Resource-Management-image46.png)

<span data-ttu-id="8cd3f-286">Amikor az erőforrás-kezelő teljesíti a kérést, az általános csapattagot a **Minden csapattag** rácsban a megnevezett erőforrás váltja fel.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Az általános csapattagot a Minden csapattag rácsban a megnevezett erőforrás váltja fel](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="8cd3f-288">Erőforrás-javaslat használata erőforrás-kérelmekhez</span><span class="sxs-lookup"><span data-stu-id="8cd3f-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="8cd3f-289">Ahelyett, hogy egy erőforrást közvetlenül egy erőforráskérésre foglalna, az erőforrás-kezelő erőforrást javasolhat a projektmenedzser számára.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="8cd3f-290">Az erőforrás-kezelő akkor használhatja ezt a lehetőséget, ha a követelményekhez nem áll rendelkezésre pontos egyezés.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="8cd3f-291">Amikor egy erőforrás-kezelő erőforrást javasol, a projektmenedzser látja, hogy az általános csapattag **Állapot** mezője **Áttekintés szükséges** lesz.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Az általános csapattag állapota Áttekintés szükségesre váltva](media/Resource-Management-image48.png)

<span data-ttu-id="8cd3f-293">A javasolt erőforrás megtekintéséhez és a javaslat foglalásának hatásának megjelenítéséhez kattintson duplán arra a csapattagra, amelynek **Áttekintés szükséges** státusza van.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="8cd3f-294">Ezután válassza a **Javasolt erőforrások** fület.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-294">Then select the **Proposed Resources** tab.</span></span>

![Javasolt erőforrások fül](media/Resource-Management-image49.png)

<span data-ttu-id="8cd3f-296">Válassza **Az összes javaslat elfogadása** elemet az összes javasolt erőforrás elfogadásához, vagy az **Összes javaslat elutasítása** opciót az elutasításhoz.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="8cd3f-297">Ha elfogadja a javasolt erőforrásokat, akkor ezeket a projektre csapattagokként foglalják, és felváltják az általános erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="8cd3f-298">Valamennyi elfogadott erőforrást el kell fogadnia vagy el kell utasítania.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="8cd3f-299">Részben nem fogadhatja el vagy utasíthatja el őket.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="8cd3f-300">Egy erőforrás felváltása a projektcsapatban</span><span class="sxs-lookup"><span data-stu-id="8cd3f-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="8cd3f-301">Időnként a projektmenedzsernek helyettesítenie kell egy lefoglalt csapattagot egy projektnél.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="8cd3f-302">A **Projektek** lapon, a **Csapat** fülön válassza ki a helyettesítő erőforrást, majd válassza a **Foglalások fenntartása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="8cd3f-303">Bontsa ki az erőforrást a hozzárendelt projektek megtekintéséhez.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Az erőforrás kibontva a hozzárendelt projektek megjelenítéséhez](media/Resource-Management-image50.png)

3. <span data-ttu-id="8cd3f-305">Kattintson a jobb gombbal a projektre, majd válassza a **Helyettesítő erőforrás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="8cd3f-306">Ha ismeri az erőforrást, amelyet helyettesíteni szeretne az aktuális erőforrással, jelölje ki vagy írja be a nevet, majd válassza az **Újbóli hozzárendelés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Helyettesítő erőforrás meghatározása](media/Resource-Management-image51.png)

    <span data-ttu-id="8cd3f-308">Alternatív megoldásként, kövesse az alábbi lépéseket egy erőforrás kereséséhez:</span><span class="sxs-lookup"><span data-stu-id="8cd3f-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="8cd3f-309">Válassza a **Helyettesítő keresése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-309">Select **Find Substitution**.</span></span>

        ![Helyettesítő erőforrás keresése](media/Resource-Management-image52.png)

        <span data-ttu-id="8cd3f-311">Az Ütemezési segéd visszaadja az elérhető helyettesítők listáját.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="8cd3f-312">Az Ütemezési segédben tovább szűrheti a rendelkezésre álló erőforrásokat a megfelelő helyettesítő megtalálásához.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![A rendelkezésre álló helyettesítők listája](media/Resource-Management-image53.png)

    2. <span data-ttu-id="8cd3f-314">Az erőforrás helyettesítéséhez válassza ki a kívánt erőforrást, majd válassza a **Helyettesítő** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Kiválasztott helyettesítő erőforrás](media/Resource-Management-image54.png)

    <span data-ttu-id="8cd3f-316">A foglalásokat és a feladatokat az új erőforrás váltja fel.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![A foglalásokat és a feladatokat az új erőforrás váltja fel](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="8cd3f-318">A csapattagok foglalásainak és feladatainak egyeztetése</span><span class="sxs-lookup"><span data-stu-id="8cd3f-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="8cd3f-319">A csapat tagjai számára a foglalások és a megbízások lazán kapcsolódnak egymáshoz.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="8cd3f-320">Más szavakkal: az erőforrásoknak lehetnek hozzárendelései, de foglalásai nem, vagy lehetnek foglalásaik, de nem lehet hozzárendeléseik.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="8cd3f-321">Ideális esetben a foglalásokat és a feladatokat össze kell hangolni, hogy az erőforrások képesek legyenek a feladat-hozzárendelések végrehajtására.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="8cd3f-322">Előfordulhat azonban, hogy a foglalások rendelkezésre álláson alapulnak, és a projekt folytatásakor a feladatok ütemezése változhat.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="8cd3f-323">Ezért a foglalások és feladatok laza csatolása rugalmasságot biztosít.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="8cd3f-324">A PSA rendelkezik egy **Egyeztetés** lappal, amely lehetővé teszi a projektmenedzserek számára, hogy összehangolják a csapattagok foglalásait és a projektcsoportokhoz rendelt megbízásaikat.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Egyeztetés fül](media/Resource-Management-image56.png)

<span data-ttu-id="8cd3f-326">Az **Egyeztetés** lap a foglalásokat és a hozzárendeléseket az egyes csoporttagok egyedi feladat-hozzárendelésének szintjéig mutatja.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="8cd3f-327">A cellákban órákat jelenít meg, amelyek hónapoktól napokig terjedő időszakokat jelent.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="8cd3f-328">A fül a projekt teljes nettó összértékét, valamint az Összesen oszlopot is mutatja.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="8cd3f-329">Az egyes erőforrások esetében a fül kiszámítja a különbséget a csapattag foglalása és a csoporttag feladatainak összeállítása között.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="8cd3f-330">Ideális esetben ennek a különbségnek 0-nak (nulla) kell lennie.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="8cd3f-331">Más szavakkal, nem lehet különbség a foglalások és a megbízások között.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="8cd3f-332">A különbségek színesek és árnyaltak, hogy felhívják a figyelmet két körülményre:</span><span class="sxs-lookup"><span data-stu-id="8cd3f-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="8cd3f-333">**Foglalási hiány** - Foglalási hiány akkor fordul elő, ha az erőforrás több hozzárendeléssel rendelkezik, mint a foglalások.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="8cd3f-334">Mivel ez a kapacitás nem volt fenntartva, a projektmenedzser javíthatja ezt a feltételt azáltal, hogy az erőforrás foglalásait kiterjeszti a hiány fedezésére.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="8cd3f-335">**Többletfoglalások** - Többletfoglalások akkor fordulnak elő, amikor egy erőforrást lefoglaltak a projekthez, de nem rendeltek hozzá feladatokhoz.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="8cd3f-336">Ez a feltétel elfogadható lehet azokban az esetekben, amikor az erőforrást a projekthez a feladat-hozzárendelés megtörténte előtt lefoglalták.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="8cd3f-337">Más esetekben azonban az erőforrást nem tervezik feladatokhoz rendelni.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="8cd3f-338">Ezekben az esetekben a projektmenedzsernek fontolóra kell vennie az erőforrás foglalásainak visszavonását, hogy a kapacitás felhasználható legyen egy másik projekthez.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="8cd3f-339">Bizonyos esetekben, ha az időt a napi szintnél magasabb szinten nézi (például a hónap szintjén), akkor az erőforrás nettó különbsége nulla lehet (más szóval, foglalások = megbízások).</span><span class="sxs-lookup"><span data-stu-id="8cd3f-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="8cd3f-340">Ha azonban az időt heti szinten tekinti, akkor láthatja, hogy az első héten nulla órás megbízások és 40 órás foglalások vannak, a második héten pedig 40 órás megbízások és nulla órás foglalások vannak.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="8cd3f-341">Összességében a foglalások és a feladatok összeegyeztethetők, de hetente különböznek.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="8cd3f-342">Ha az időt magasabb szinteken tekinti meg, akkor az **Egyeztetés** lapon lévő cellák jelzik, hogy az alacsonyabb szinteken eltérések vannak.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="8cd3f-343">Ha egy cellába duplán kattint, nagyíthat, hogy megnézze a különbséget.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="8cd3f-344">Ezután jobb egérgombbal kattinthat a kicsinyítéshez. Ha kiválaszt egy erőforrást, majd használja a rács eszköztár **Következő különbség** vezérlőjét, a következő különbséghez ugorhat az adott erőforrás foglalása és hozzárendelése között.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="8cd3f-345">Ezután az **Előző különbség** vezérlővel visszatérhet.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="8cd3f-346">A különbségjelzőt és a navigációs viselkedést a **Beállítások** alatt is kikapcsolhatja.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Különbségmutató](media/Resource-Management-image57.png)

<span data-ttu-id="8cd3f-348">Ha az erőforráshoz feladatok vannak hozzárendelve, de nincs foglalása, akkor a **Projektek** oldalon, az **Egyeztetés** lapon válassza ki a foglalási hiányt, majd válassza a **Foglalás kiterjesztése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="8cd3f-349">Megjelenik a **Foglalás kiterjesztése** párbeszédpanel, amely megmutatja az erőforrás hiányának kezeléséhez szükséges foglalást.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="8cd3f-350">Ezenkívül megmutatja az erőforrás meglévő foglalásait az összes projektben vagy más ütemezhető entitásban.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="8cd3f-351">Ha az **OK** lehetőséget választja az erőforrás foglalásának elkészítéséhez, az erőforrás elérhetőségétől függetlenül túlfoglalást okozhat.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![A Foglalás kiterjesztése párbeszédpanel](media/Resource-Management-image58.png)

<span data-ttu-id="8cd3f-353">A projektmenedzser vagy az erőforrás-kezelő ezután felhasználhatja az Ütemezési táblát olyan helyzetek kezelésére, amikor egy erőforrás túlfoglalása meghaladja a kapacitást.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
