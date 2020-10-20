---
title: Csoporttagok karbantartása
description: Ez a témakör információt nyújt a nevesített erőforrásoknak a projektcsoportokhoz való foglalásáról, és a feladatokhoz való hozzárendeléséről.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961881"
---
# <a name="maintain-team-members"></a><span data-ttu-id="62cb4-103">Csoporttagok karbantartása</span><span class="sxs-lookup"><span data-stu-id="62cb4-103">Maintain team members</span></span>

<span data-ttu-id="62cb4-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="62cb4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="62cb4-105">Nevesített erőforrást úgy adhat hozzá a projektcsoporthoz, ha közvetlenül a csoporthoz foglalja le azt.</span><span class="sxs-lookup"><span data-stu-id="62cb4-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="62cb4-106">A Dynamics 365 Project Operations programban lépjen a **Projektek**elemre, majd válassza ki azt a projektet, amelyhez a foglalást végzi.</span><span class="sxs-lookup"><span data-stu-id="62cb4-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="62cb4-107">A **Projekt** oldal **Csoport** lapján válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="62cb4-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="62cb4-108">Válassza ki a foglalható erőforrást a **Csoporttag gyors létrehozása** párbeszédablabkan.</span><span class="sxs-lookup"><span data-stu-id="62cb4-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="62cb4-109">Ha van alapértelmezett szerepkör hozzárendelve az erőforráshoz, az a **Szerepkör** mezőben látható.</span><span class="sxs-lookup"><span data-stu-id="62cb4-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="62cb4-110">A szerep megváltoztatható.</span><span class="sxs-lookup"><span data-stu-id="62cb4-110">You can change the role.</span></span> 
4. <span data-ttu-id="62cb4-111">Válassza ki, hogy az erőforrásra melyik dátumok között lesz szüksége, majd az erőforrás kapacitásának felosztási módját.</span><span class="sxs-lookup"><span data-stu-id="62cb4-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="62cb4-112">Ha szeretné, hogy egy csoporttag projektjóváhagyó legyen , válassza az **Igen** lehetőséget a **Projektjóváhagyó** mezőben.</span><span class="sxs-lookup"><span data-stu-id="62cb4-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="62cb4-113">A csoporttag jóváhagyhatja a projekt beküldött idő- és költségbejegyzéseit.</span><span class="sxs-lookup"><span data-stu-id="62cb4-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="62cb4-114">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="62cb4-114">Select **Save**.</span></span>

<span data-ttu-id="62cb4-115">Ezután a foglalt erőforrást hozzárendelheti a projekthez kapcsolódó feladatokhoz.</span><span class="sxs-lookup"><span data-stu-id="62cb4-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="62cb4-116">Az új erőforráshoz feladatokat rendelhet hozzá, ehhez a **Projekt** lapon kattintson az **Ütemezés fülre**.</span><span class="sxs-lookup"><span data-stu-id="62cb4-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="62cb4-117">A feladat rács **Erőforrás** mezőjéből indítható erőforrás-választó a kiválasztható csoporttagokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="62cb4-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="62cb4-118">A Project Operationsben, az erőforrás-foglalások és a feladatok hozzárendelései nem szorosan párosulnak.</span><span class="sxs-lookup"><span data-stu-id="62cb4-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="62cb4-119">Ha az erőforrás-választót használja az ütemezésben, akkor a munkacsoport tagjaihoz több óráig is hozzárendelheti a feladatokat, mint a projekten végzett foglalások időfedezete.</span><span class="sxs-lookup"><span data-stu-id="62cb4-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="62cb4-120">A csoporttagok foglalásai és a hozzárendelések közötti különbségek megjelennek a **Csoport** és az **Erőforrás-egyeztetés** lapjain.</span><span class="sxs-lookup"><span data-stu-id="62cb4-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="62cb4-121">A foglalások és a hozzárendelések közötti különbségeket részletesebb szinten is egyeztetheti.</span><span class="sxs-lookup"><span data-stu-id="62cb4-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="62cb4-122">Az **Ütemezés** lapról elérhető erőforrás-választóval megkeresheti és kijelölheti azokat a foglalható erőforrásokat, amelyek még nem szerepelnek a projektcsoportban.</span><span class="sxs-lookup"><span data-stu-id="62cb4-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="62cb4-123">Ezek az erőforrások az erőforrás-választóban az **Egyéb erőforrások** részen jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="62cb4-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="62cb4-124">Amikor választ, az erőforrás hozzáadódik a projektcsoporthoz, és hozzárendelésre kerül a feladathoz, de a rendszer nem hoz létre foglalást.</span><span class="sxs-lookup"><span data-stu-id="62cb4-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="62cb4-125">Az **Egyeztetés** lapon a Foglalás meghosszabbítása funkció, vagy az **Ütemezési tábla** használatával foglalhatja le az erőforrás kapacitását a projekt számára.</span><span class="sxs-lookup"><span data-stu-id="62cb4-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="62cb4-126">Miután egy csoporttag foglalásra került a projekthez, használhatja a **Foglalások karbantartása** funkciót, vagy az **Ütemezési tábla** használatával közvetlenül kezelheti annak foglalásait.</span><span class="sxs-lookup"><span data-stu-id="62cb4-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
