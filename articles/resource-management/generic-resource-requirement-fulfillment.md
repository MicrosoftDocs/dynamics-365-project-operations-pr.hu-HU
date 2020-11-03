---
title: Általános erőforrás-követelmények teljesítése
description: Ez a témakör a nevesített erőforrásoknak egy általános erőforrás-követelmény részére történő foglalásáról nyújt tájékoztatást.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6bb7c185656ff87bb3ca24209594c07d25862d70
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078037"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="e6fc7-103">Általános erőforrás-követelmények teljesítése</span><span class="sxs-lookup"><span data-stu-id="e6fc7-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="e6fc7-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="e6fc7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e6fc7-105">Egy elnevezett erőforrás foglalható az erőforrás-követelménnyel rendelkező általános erőforrás lecserélése céljából.</span><span class="sxs-lookup"><span data-stu-id="e6fc7-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="e6fc7-106">A **Projektek** oldalon lépjen a **Csoport** lapra.</span><span class="sxs-lookup"><span data-stu-id="e6fc7-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="e6fc7-107">Válassza ki a listából azt az általános erőforrást, amelyhez erőforrás-követelmény tartozik, majd válassza a **Foglalás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="e6fc7-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="e6fc7-108">Egy másik lehetőség, hogy megnyitja az erőforrás-követelményt, majd a **Foglalás** lehetőséget választja.</span><span class="sxs-lookup"><span data-stu-id="e6fc7-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="e6fc7-109">Az **Ütemezési segéd** lapon jelöljön ki egy elnevezett erőforrást a projektcsoport számára történő foglaláshoz, majd válassza a **Foglalás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="e6fc7-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="e6fc7-110">Amikor a foglalás befejeződött, és azt egy elnevezett erőforrás teljesíti, az általános erőforrást az elnevezett erőforrás váltja fel.</span><span class="sxs-lookup"><span data-stu-id="e6fc7-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="e6fc7-111">Továbbá az ütemezésben szereplő hozzárendelések frissülnek az elnevezett erőforrással.</span><span class="sxs-lookup"><span data-stu-id="e6fc7-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="e6fc7-112">Általános erőforrás követelményeinek teljesítése több elnevezett erőforrással</span><span class="sxs-lookup"><span data-stu-id="e6fc7-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="e6fc7-113">Egy általános erőforrás követelménye több elnevezett erőforrással is teljesíthető, hasonlóan, mint egy elnevezett erőforrás hozzárendelése esetén.</span><span class="sxs-lookup"><span data-stu-id="e6fc7-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="e6fc7-114">Például, adott egy feladat, amely öt nap és 120 óra ráfordítást igényel.</span><span class="sxs-lookup"><span data-stu-id="e6fc7-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="e6fc7-115">Ezt a feladatot nem lehet olyan erőforrással befejezni, amely egy ötnapos héten átlagosan napi nyolc órát dolgozik.</span><span class="sxs-lookup"><span data-stu-id="e6fc7-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="e6fc7-116">A követelmény 120 órányi robotikai mérnöki tevékenység öt nap alatt, tehát napi 24 óra.</span><span class="sxs-lookup"><span data-stu-id="e6fc7-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="e6fc7-117">Ez egy példa arra az esetre, amikor egy általános erőforrás-kérelem teljesítéséhez több elnevezett erőforrásra van szükség.</span><span class="sxs-lookup"><span data-stu-id="e6fc7-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="e6fc7-118">A követelmény teljesítéséhez több erőforrást is le kell foglalnia.</span><span class="sxs-lookup"><span data-stu-id="e6fc7-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="e6fc7-119">A fő különbség ezen forgatókönyv esetén, hogy az általános erőforrás a feladathoz rendelt csoportban marad, és a foglalt elnevezett erőforráscsoport-tagok nem lesznek hozzárendelve a pozíció részeként.</span><span class="sxs-lookup"><span data-stu-id="e6fc7-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="e6fc7-120">A projektvezető a munkát megfelelő módon hozzárendelheti az elnevezett erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="e6fc7-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="e6fc7-121">Az **Egyeztetés** segíthet a projektkezelőnek a foglalás több erőforrás közötti lebontásában a feladat-hozzárendelésekhez.</span><span class="sxs-lookup"><span data-stu-id="e6fc7-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="e6fc7-122">Ez nem történik meg automatikusan, mert a fenti egyszerű példánál bonyolultabb forgatókönyv esetén (ha a követelményt például számos feladat teszi ki) a rendszernek feltételeznie kell a projektkezelő által igényelt hozzárendelési módot.</span><span class="sxs-lookup"><span data-stu-id="e6fc7-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="e6fc7-123">Mivel a rendszer nem érti a szándékot, a feltételezések valószínűleg eltérnek a tervezettől, és helytelen vagy kiszámíthatatlan eredmény fordul elő.</span><span class="sxs-lookup"><span data-stu-id="e6fc7-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="e6fc7-124">A kiszámítható eredmény az, hogy az általános erőforrás mindaddig hozzá lesz rendelve, amíg a projetkezelő szándékosan hozza létre a hozzárendeléseket az **Egyeztetés** nézet segítségével.</span><span class="sxs-lookup"><span data-stu-id="e6fc7-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


