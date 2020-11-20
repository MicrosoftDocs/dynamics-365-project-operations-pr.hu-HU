---
title: A projekt beállításai
description: Ez a témakör információkat nyújt a projektkezelési beállításokról.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: b2cda6bfd7f152ee948cf49fab91aed475968a09
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123111"
---
# <a name="project-settings"></a><span data-ttu-id="16bca-103">A projekt beállításai</span><span class="sxs-lookup"><span data-stu-id="16bca-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="16bca-104">A következő beállításokkal érheti el a projekttervezési funkciókat.</span><span class="sxs-lookup"><span data-stu-id="16bca-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="16bca-105">Munkasablon</span><span class="sxs-lookup"><span data-stu-id="16bca-105">Work template</span></span>

<span data-ttu-id="16bca-106">A projekt ütemezésének elkészítéséhez létre kell hoznia egy projekt naptársablont, amely meghatározza a napi munkaórák számát és az esetleges szünnapokat.</span><span class="sxs-lookup"><span data-stu-id="16bca-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="16bca-107">Projekt naptársablon létrehozásához társítson egy munkasablont a projekt **Naptársablon** mezőjéhez.</span><span class="sxs-lookup"><span data-stu-id="16bca-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="16bca-108">Kövesse az alábbi a lépéseket munkasablon létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="16bca-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="16bca-109">A PSA-ban a bal oldali navigációs panelen kattintson az **Erőforrások** elemre.</span><span class="sxs-lookup"><span data-stu-id="16bca-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="16bca-110">Az **Erőforrások** listaoldalon nyisson meg egy felhasználói rekordot, majd válassza a **Munkaórák megjelenítése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="16bca-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="16bca-111">Győződjön meg arról, hogy engedélyezte az előugró ablakokat a böngésző oldalán.</span><span class="sxs-lookup"><span data-stu-id="16bca-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="16bca-112">Ez lehetővé teszi az erőforráshoz beállított munkaórák megtekintését.</span><span class="sxs-lookup"><span data-stu-id="16bca-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="16bca-113">A **Havi nézet** lapon kattintson a **Beállítás** elemre.</span><span class="sxs-lookup"><span data-stu-id="16bca-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="16bca-114">Megjelenik egy három lehetőséget tartalmazó lista:</span><span class="sxs-lookup"><span data-stu-id="16bca-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="16bca-115">Új heti ütemezés</span><span class="sxs-lookup"><span data-stu-id="16bca-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="16bca-116">Egynapi munkaütemezés</span><span class="sxs-lookup"><span data-stu-id="16bca-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="16bca-117">Szabadidő</span><span class="sxs-lookup"><span data-stu-id="16bca-117">Time Off</span></span>

> ![Opciók beállítása](media/project-13.png)

4. <span data-ttu-id="16bca-119">Válassza az **Új heti ütemezés** elemet, majd állítsa be az erőforrás ütemezésének opcióit.</span><span class="sxs-lookup"><span data-stu-id="16bca-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="16bca-120">Beállíthat ismétlődő heti ütemezést, napi óraparamétereket, szünnapokat stb.</span><span class="sxs-lookup"><span data-stu-id="16bca-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="16bca-121">Állítsa be a dátumtartományt, válassza a **Mentés** lehetőséget, majd kattintson a **Bezár** gombra.</span><span class="sxs-lookup"><span data-stu-id="16bca-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="16bca-122">Lépjen vissza az **Erőforrások** listaoldalra, és válassza ki azt az erőforrást, amelyre beállította a munkaórákat.</span><span class="sxs-lookup"><span data-stu-id="16bca-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="16bca-123">A munkasablon beállításához válassza a **Naptár beállítása mint** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="16bca-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="16bca-124">A **Munkasablon** párbeszédpanelen adja meg a munkasablon nevét, majd válassza az **Alkalmaz** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="16bca-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="16bca-125">Most már hozzárendelheti a munkasablont egy projekt naptársablonhoz.</span><span class="sxs-lookup"><span data-stu-id="16bca-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="16bca-126">Erőforrás-szerepkörök</span><span class="sxs-lookup"><span data-stu-id="16bca-126">Resource roles</span></span>

<span data-ttu-id="16bca-127">Az *erőforrás-szerepkör* kifejezés egy sor készséget, kompetenciát és minősítést takar, amelyekre egy személynek szüksége van ahhoz, hogy egy konkrét feladatcsoportot végrehajtson egy projektben.</span><span class="sxs-lookup"><span data-stu-id="16bca-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="16bca-128">A PSA segítségével kiszámolhatja és kiszámlázhatja az erőforrás idejét az erőforráshoz társított szerepkör alapján.</span><span class="sxs-lookup"><span data-stu-id="16bca-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="16bca-129">Minden szervezetnek be kell állítania ezeket a szerepköröket a bal oldali navigációs panel segítségével a **Project Service** menüben.</span><span class="sxs-lookup"><span data-stu-id="16bca-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="16bca-130">Minden szervezetnek be kell állítania ezeket a szerepköröket az **Aktív erőforráskategóriák** oldalon.</span><span class="sxs-lookup"><span data-stu-id="16bca-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="16bca-131">Az oldal megnyitásához a bal oldali navigációs panelen válassza a **Erőforrás-szerepkörök** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="16bca-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="16bca-132">Árlisták</span><span class="sxs-lookup"><span data-stu-id="16bca-132">Price lists</span></span>

<span data-ttu-id="16bca-133">Az árlisták segítségével beállíthatja a költség- és eladási árakat az erőforrás-szerepkörökhöz, a költségkategóriákhoz, a termékekhez és a szervezet más elemeihez.</span><span class="sxs-lookup"><span data-stu-id="16bca-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="16bca-134">Mielőtt meghatározná a projekthez teljesítendő munkára vonatkozó pénzügyi becsléseket, el kell készítenie egy támogatási költség- és eladási árlistát.</span><span class="sxs-lookup"><span data-stu-id="16bca-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="16bca-135">A paraméterek szakaszban be kell állítania egy alapértelmezett költség- és eladási árlistát, amely a szervezetben létrehozott projektekre vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="16bca-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="16bca-136">Az **Aktív projektparaméterek** oldalon ellenőrizze, hogy beállított-e alapértelmezett költség- és eladási árlistát.</span><span class="sxs-lookup"><span data-stu-id="16bca-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
