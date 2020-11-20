---
title: Projektnaptárak meghatározása
description: Ez a témakör a projektütemezés nyomon követésére szolgáló projektnaptár használatáról tartalmaz információt.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 442a901af8754fa0335bbf43f4ac8c73b11f9499
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131661"
---
# <a name="define-project-calendars"></a><span data-ttu-id="d8aab-103">Projektnaptárak meghatározása</span><span class="sxs-lookup"><span data-stu-id="d8aab-103">Define project calendars</span></span>

<span data-ttu-id="d8aab-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="d8aab-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d8aab-105">A projekt ütemezésének elkészítéséhez létre kell hoznia egy projekt naptársablont, amely meghatározza a napi munkaórák számát és az esetleges szünnapokat.</span><span class="sxs-lookup"><span data-stu-id="d8aab-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="d8aab-106">Projekt naptársablon létrehozásához társítson egy munkasablont a projekt **Naptársablon** mezőjéhez.</span><span class="sxs-lookup"><span data-stu-id="d8aab-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="d8aab-107">Kövesse az alábbi a lépéseket munkasablon létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="d8aab-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="d8aab-108">A bal navigációs ablaktáblán válassza az **Erőforrások** elemet.</span><span class="sxs-lookup"><span data-stu-id="d8aab-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="d8aab-109">Az **Erőforrások** listaoldalon nyisson meg egy felhasználói rekordot, majd válassza a **Munkaórák megjelenítése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d8aab-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="d8aab-110">Győződjön meg arról, hogy engedélyezte az előugró ablakokat a böngésző oldalán.</span><span class="sxs-lookup"><span data-stu-id="d8aab-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="d8aab-111">Ez lehetővé teszi az erőforráshoz beállított munkaórák megtekintését.</span><span class="sxs-lookup"><span data-stu-id="d8aab-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="d8aab-112">A **Havi nézet** lapon válassza a **Beállítás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d8aab-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="d8aab-113">Megjelenik egy három lehetőséget tartalmazó lista:</span><span class="sxs-lookup"><span data-stu-id="d8aab-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="d8aab-114">Új heti ütemezés</span><span class="sxs-lookup"><span data-stu-id="d8aab-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="d8aab-115">Egynapi munkaütemezés</span><span class="sxs-lookup"><span data-stu-id="d8aab-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="d8aab-116">Szabadidő</span><span class="sxs-lookup"><span data-stu-id="d8aab-116">Time Off</span></span>

4. <span data-ttu-id="d8aab-117">Válassza az **Új heti ütemezés** elemet, majd állítsa be az erőforrás ütemezésének opcióit.</span><span class="sxs-lookup"><span data-stu-id="d8aab-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="d8aab-118">Beállíthat ismétlődő heti ütemezést, napi óraparamétereket, szünnapokat stb.</span><span class="sxs-lookup"><span data-stu-id="d8aab-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="d8aab-119">Állítsa be a dátumtartományt, válassza a **Mentés**, majd a **Bezárás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d8aab-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="d8aab-120">Lépjen vissza az **Erőforrások** listaoldalra, és válassza ki azt az erőforrást, amelyre beállította a munkaórákat.</span><span class="sxs-lookup"><span data-stu-id="d8aab-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="d8aab-121">A munkasablon beállításához válassza a **Naptár beállítása mint** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d8aab-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="d8aab-122">A **Munkasablon** párbeszédpanelen adja meg a munkasablon nevét, majd válassza az **Alkalmaz** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d8aab-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="d8aab-123">Most már hozzárendelheti a munkasablont egy projekt naptársablonhoz.</span><span class="sxs-lookup"><span data-stu-id="d8aab-123">You can now associate the work template with a project calendar template.</span></span>
