---
title: Nevesített foglalható erőforrások foglalása projektcsoporthoz, és feladatok hozzárendelése
description: Ez a témakör információt nyújt a nevesített erőforrásoknak a projektcsoportokhoz való foglalásáról, és a feladatokhoz való hozzárendeléséről.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 0300c494a3294b26e2de6bbfa1dd50a76bb72651
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130176"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="eb88b-103">Nevesített foglalható erőforrások foglalása projektcsoporthoz, és feladatok hozzárendelése</span><span class="sxs-lookup"><span data-stu-id="eb88b-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="eb88b-104">Nevesített erőforrást úgy adhat hozzá a projektcsoporthoz, ha közvetlenül a csoporthoz foglalja le azt.</span><span class="sxs-lookup"><span data-stu-id="eb88b-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="eb88b-105">Ehhez hajtsa végre az alábbi műveleteket.</span><span class="sxs-lookup"><span data-stu-id="eb88b-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="eb88b-106">A Project Service Automation programban lépjen a **Projektek** elemre, majd válassza ki azt a projektet, amelyhez a foglalást végzi.</span><span class="sxs-lookup"><span data-stu-id="eb88b-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="eb88b-107">A **Projekt** oldal **Csoport** lapján kattinton az **Új** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="eb88b-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Csoporttag hozzáadása a csoport lapról](media/RM-how-to-1.png)

3. <span data-ttu-id="eb88b-109">Válassza ki a foglalható erőforrást a **Csoporttag gyors létrehozása** párbeszédablabkan.</span><span class="sxs-lookup"><span data-stu-id="eb88b-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="eb88b-110">Ha van alapértelmezett szerepkör hozzárendelve az erőforráshoz, az a **Szerepkör** mezőben látható.</span><span class="sxs-lookup"><span data-stu-id="eb88b-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="eb88b-111">Szükség esetén a szerepkör módosítható.</span><span class="sxs-lookup"><span data-stu-id="eb88b-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="eb88b-112">Válassza ki, hogy az erőforrásra melyik dátumok között lesz szüksége, majd az erőforrás kapacitásának felosztási módját.</span><span class="sxs-lookup"><span data-stu-id="eb88b-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="eb88b-113">Ha szeretné, hogy egy csoporttag projektjóváhagyó legyen , válassza az **Igen** lehetőséget a **Projektjóváhagyó** mezőben.</span><span class="sxs-lookup"><span data-stu-id="eb88b-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="eb88b-114">Ez azt jelenti, hogy a csoporttag jóváhagyhatja a projekt beküldött idő- és költségbejegyzéseit.</span><span class="sxs-lookup"><span data-stu-id="eb88b-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="eb88b-115">Kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="eb88b-115">Click **Save**.</span></span>

![Csoporttag hozzáadása a Gyors létrehozás űrlapon](media/RM-how-to-2.png)


<span data-ttu-id="eb88b-117">Ezután a foglalt erőforrást hozzárendelheti a projekthez kapcsolódó feladatokhoz.</span><span class="sxs-lookup"><span data-stu-id="eb88b-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="eb88b-118">Az új erőforráshoz feladatokat rendelhet hozzá, ehhez a **Projekt** lapon kattintson az **Ütemezés fülre**.</span><span class="sxs-lookup"><span data-stu-id="eb88b-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="eb88b-119">A feladat rács **Erőforrás** mezőjéből indítható erőforrás-választó a kiválasztható csoporttagokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="eb88b-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Csoporttag hozzárendelése egy feladathoz az Ütemezés lapon](media/RM-how-to-3.png)

<span data-ttu-id="eb88b-121">Project Service Automation (PSA) 3. verziójában az erőforrás-foglalás és a feladatok hozzárendelése nem párosul szorosan.</span><span class="sxs-lookup"><span data-stu-id="eb88b-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="eb88b-122">Ez azt jelenti, hogy ha az erőforrás-választót használja az ütemezésben, akkor a munkacsoport tagjaihoz több óráig is hozzárendelheti a feladatokat, mint a projekten végzett foglalások időfedezete.</span><span class="sxs-lookup"><span data-stu-id="eb88b-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="eb88b-123">A csoporttagok foglalásai és a hozzárendelések közötti különbségeket a **Csoport** vagy az **Erőforrás-egyeztetések** lapon tekintheti meg. A foglalások és az erőforrás-hozzárendelések közötti különbségeket részletesebb szinten is egyeztetheti.</span><span class="sxs-lookup"><span data-stu-id="eb88b-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Erőforrás-egyeztetés lap](media/RM-how-to-4.png)

<span data-ttu-id="eb88b-125">Az **Ütemezés** lapról elérhető erőforrás-választóval is megkeresheti és kijelölheti azokat a foglalható erőforrásokat, amelyek még nem szerepelnek a projektcsoportban.</span><span class="sxs-lookup"><span data-stu-id="eb88b-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="eb88b-126">Ezek az erőforrás-választóban az **Egyéb erőforrások** részen jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="eb88b-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Nem csoporttag erőforrás hozzárendelése egy feladathoz](media/RM-how-to-5.png)

<span data-ttu-id="eb88b-128">Ennek használatával az erőforrás hozzáadódik a projektcsoporthoz, és hozzárendelésre kerül a feladathoz, de a rendszer nem hoz létre foglalást.</span><span class="sxs-lookup"><span data-stu-id="eb88b-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Csoporttag hozzárendelésekkel, foglalások nélkül](media/RM-how-to-6.png)

<span data-ttu-id="eb88b-130">Az **Egyeztetés** lapon a Foglalás meghosszabbítása funkció, vagy az **Ütemezési tábla** használatával foglalhatja le az erőforrás kapacitását a projekt számára.</span><span class="sxs-lookup"><span data-stu-id="eb88b-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Csoporttag foglalásainak meghosszabbítása az Erőforrás-egyeztetés lapon](media/RM-how-to-7.png)

<span data-ttu-id="eb88b-132">Miután egy csoporttag foglalásra került a projekhez, használhatja a Foglalások karbantartása funkciót, vagy az Ütemezési tábla használatával közvetlenül kezelheti annak foglalásait.</span><span class="sxs-lookup"><span data-stu-id="eb88b-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
