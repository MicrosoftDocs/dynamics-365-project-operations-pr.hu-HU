---
title: Általános erőforrás-követelmények teljesítése
description: Ez a témakör a nevesített erőforrásoknak egy általános erőforrás-követelmény részére történő foglalásáról nyújt tájékoztatást.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fef896ae12c196d5566ad54f3e15373020e4e28a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279591"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="8952c-103">Általános erőforrás-követelmények teljesítése</span><span class="sxs-lookup"><span data-stu-id="8952c-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="8952c-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="8952c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8952c-105">Egy elnevezett erőforrás foglalható az erőforrás-követelménnyel rendelkező általános erőforrás lecserélése céljából.</span><span class="sxs-lookup"><span data-stu-id="8952c-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="8952c-106">A **Projektek** oldalon lépjen a **Csoport** lapra.</span><span class="sxs-lookup"><span data-stu-id="8952c-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="8952c-107">Válassza ki a listából azt az általános erőforrást, amelyhez erőforrás-követelmény tartozik, majd válassza a **Foglalás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8952c-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="8952c-108">Egy másik lehetőség, hogy megnyitja az erőforrás-követelményt, majd a **Foglalás** lehetőséget választja.</span><span class="sxs-lookup"><span data-stu-id="8952c-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="8952c-109">Az **Ütemezési segéd** lapon jelöljön ki egy elnevezett erőforrást a projektcsoport számára történő foglaláshoz, majd válassza a **Foglalás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8952c-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="8952c-110">Amikor a foglalás befejeződött, és azt egy elnevezett erőforrás teljesíti, az általános erőforrást az elnevezett erőforrás váltja fel.</span><span class="sxs-lookup"><span data-stu-id="8952c-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="8952c-111">Továbbá az ütemezésben szereplő hozzárendelések frissülnek az elnevezett erőforrással.</span><span class="sxs-lookup"><span data-stu-id="8952c-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="8952c-112">Általános erőforrás követelményeinek teljesítése több elnevezett erőforrással</span><span class="sxs-lookup"><span data-stu-id="8952c-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="8952c-113">Egy általános erőforrás követelménye több elnevezett erőforrással is teljesíthető, hasonlóan, mint egy elnevezett erőforrás hozzárendelése esetén.</span><span class="sxs-lookup"><span data-stu-id="8952c-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="8952c-114">Például, adott egy feladat, amely öt nap és 120 óra ráfordítást igényel.</span><span class="sxs-lookup"><span data-stu-id="8952c-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="8952c-115">Ezt a feladatot nem lehet olyan erőforrással befejezni, amely egy ötnapos héten átlagosan napi nyolc órát dolgozik.</span><span class="sxs-lookup"><span data-stu-id="8952c-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="8952c-116">A követelmény 120 órányi robotikai mérnöki tevékenység öt nap alatt, tehát napi 24 óra.</span><span class="sxs-lookup"><span data-stu-id="8952c-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="8952c-117">Ez egy példa arra az esetre, amikor egy általános erőforrás-kérelem teljesítéséhez több elnevezett erőforrásra van szükség.</span><span class="sxs-lookup"><span data-stu-id="8952c-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="8952c-118">A követelmény teljesítéséhez több erőforrást is le kell foglalnia.</span><span class="sxs-lookup"><span data-stu-id="8952c-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="8952c-119">A fő különbség ezen forgatókönyv esetén, hogy az általános erőforrás a feladathoz rendelt csoportban marad, és a foglalt elnevezett erőforráscsoport-tagok nem lesznek hozzárendelve a pozíció részeként.</span><span class="sxs-lookup"><span data-stu-id="8952c-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="8952c-120">A projektvezető a munkát megfelelő módon hozzárendelheti az elnevezett erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="8952c-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="8952c-121">Az **Egyeztetés** segíthet a projektkezelőnek a foglalás több erőforrás közötti lebontásában a feladat-hozzárendelésekhez.</span><span class="sxs-lookup"><span data-stu-id="8952c-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="8952c-122">Ez nem történik meg automatikusan, mert a fenti egyszerű példánál bonyolultabb forgatókönyv esetén (ha a követelményt például számos feladat teszi ki) a rendszernek feltételeznie kell a projektkezelő által igényelt hozzárendelési módot.</span><span class="sxs-lookup"><span data-stu-id="8952c-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="8952c-123">Mivel a rendszer nem érti a szándékot, a feltételezések valószínűleg eltérnek a tervezettől, és helytelen vagy kiszámíthatatlan eredmény fordul elő.</span><span class="sxs-lookup"><span data-stu-id="8952c-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="8952c-124">A kiszámítható eredmény az, hogy az általános erőforrás mindaddig hozzá lesz rendelve, amíg a projetkezelő szándékosan hozza létre a hozzárendeléseket az **Egyeztetés** nézet segítségével.</span><span class="sxs-lookup"><span data-stu-id="8952c-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]