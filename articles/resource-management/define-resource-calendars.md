---
title: Erőforrásnaptárak meghatározása
description: Ez a témakör a Project Operations erőforrásaihoz tartozó munkaidőnaptárak definiálásával kapcsolatban tartalmaz tájékoztatást.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5ac834e16afc2f559bee6e10434f7015e8a8e51f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012184"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="e63ab-103">Erőforrásnaptárak meghatározása</span><span class="sxs-lookup"><span data-stu-id="e63ab-103">Define resource calendars</span></span>

<span data-ttu-id="e63ab-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="e63ab-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e63ab-105">A projekten dolgozó minden egyes lefoglalható erőforrásnak munkaidőnaptárral kell rendelkeznie a rendelkezésre állás meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="e63ab-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="e63ab-106">Az erőforrás munkaidejét kétféleképpen lehet definiálni:</span><span class="sxs-lookup"><span data-stu-id="e63ab-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="e63ab-107">Egyéni naptári szabályok definiálása erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="e63ab-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="e63ab-108">Meglévő naptársablon alkalmazása az erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="e63ab-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="e63ab-109">Erőforrás munkaóráinak megadása</span><span class="sxs-lookup"><span data-stu-id="e63ab-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="e63ab-110">Válassza az **Erőforrások** menü **Erőforrások** pontját.</span><span class="sxs-lookup"><span data-stu-id="e63ab-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="e63ab-111">A rács nézetben válassza ki a megfelelő **Lefoglalható erőforrás** elemet.</span><span class="sxs-lookup"><span data-stu-id="e63ab-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="e63ab-112">Az **Erőforrás részletei** oldalon válassza a **Munkaidő** lapot. Alapértelmezés szerint a foglalt erőforrások naptára alapértelmezés szerint a szervezet számára definiált alapértelmezett munkaidősablon munkaidejét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e63ab-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="e63ab-113">A munkaidő frissítéséhez kattintson a jobb gombbal a meghatározandó javasolt naptári szabály kezdő dátumára.</span><span class="sxs-lookup"><span data-stu-id="e63ab-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="e63ab-114">A naptári szabály menü segítségével definiálhat egy adott napra vonatkozó naptári szabályt, a sorozat többi részét vagy a teljes naptárat.</span><span class="sxs-lookup"><span data-stu-id="e63ab-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="e63ab-115">Miután a lehetőség be van jelölve, megadhatja a következőket:</span><span class="sxs-lookup"><span data-stu-id="e63ab-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="e63ab-116">A hét napja, ahol a munkaidő érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="e63ab-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="e63ab-117">Az egyes napokon belüli munkaidők.</span><span class="sxs-lookup"><span data-stu-id="e63ab-117">The working times within each day.</span></span>
    - <span data-ttu-id="e63ab-118">A naptári szabály időzónája</span><span class="sxs-lookup"><span data-stu-id="e63ab-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="e63ab-119">Adott esetben a munkaszüneti idő is megadható a szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="e63ab-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="e63ab-120">Naptársablon alkalmazása egy erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="e63ab-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="e63ab-121">Válassza az **Erőforrások** menü **Erőforrások** pontját.</span><span class="sxs-lookup"><span data-stu-id="e63ab-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="e63ab-122">A rács nézetben akár 25 **Lefoglalható erőforrás** is kiválasztható frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="e63ab-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="e63ab-123">Válassza a **Naptár beállítása** lehetőséget, és egy párbeszéd jelenik meg a rendelkezésre álló munkaidősablonok listájával.</span><span class="sxs-lookup"><span data-stu-id="e63ab-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="e63ab-124">Válassza ki a használni kívánt sablont, majd nyomja meg az **Alkalmaz** gombot.</span><span class="sxs-lookup"><span data-stu-id="e63ab-124">Select the template you want to use, and then select **Apply**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]