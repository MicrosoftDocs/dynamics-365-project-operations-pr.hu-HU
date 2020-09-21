---
title: Nevesített erőforrások foglalása erőforrás-követelményekből
description: Ez a témakör a nevesített erőforrásoknak egy általános erőforrás-követelmény részére történő foglalásáról nyújt tájékoztatást.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 83ac2056-313e-4f90-8297-238fd4d25ef9
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: eab280cd1a670cc2a6ed0ae02cde7ba9bf7d601d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752187"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="11aeb-103">Nevesített erőforrások foglalása erőforrás-követelményekből</span><span class="sxs-lookup"><span data-stu-id="11aeb-103">Book named resources from resource requirements</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="11aeb-104">Egy elnevezett erőforrás foglalható az erőforrás-követelménnyel rendelkező általános erőforrás lecserélése céljából.</span><span class="sxs-lookup"><span data-stu-id="11aeb-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="11aeb-105">A Project Service Automation (PSA) program **Projektek** lapján kattintson a **Csoport** fülre.</span><span class="sxs-lookup"><span data-stu-id="11aeb-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="11aeb-106">Válassza ki a listából azt az általános erőforrást, amelyhez erőforrás-követelmény tartozik, majd kattintson a **Foglalás** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="11aeb-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="11aeb-107">Másik lehetőségként nyissa meg az erőforrás-követelményt, majd kattintson a **Foglalás** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="11aeb-107">Or, open the resource requirement and then click **Book**.</span></span>


![Általános csoporttag foglalása](media/RM-how-to-14.png)


3. <span data-ttu-id="11aeb-109">Az **Ütemezési segéd** lapon jelöljön ki egy elnevezett erőforrást a projektcsoport számára történő foglaláshoz, majd kattintson a **Foglalás**lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="11aeb-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Általános csoporttag foglalása az Ütemezési segéd használatával](media/RM-how-to-15.png)

<span data-ttu-id="11aeb-111">Amikor a foglalás befejeződött, és azt egy elnevezett erőforrás teljesíti, az általános erőforrást az elnevezett erőforrás váltja fel.</span><span class="sxs-lookup"><span data-stu-id="11aeb-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Az általános csoporttagot leváltó elnevezett csoporttag](media/RM-how-to-16.png)

<span data-ttu-id="11aeb-113">Továbbá az ütemezésben szereplő hozzárendelések frissülnek az elnevezett erőforrással.</span><span class="sxs-lookup"><span data-stu-id="11aeb-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![A projektfeladatokhoz hozzárendelt elnevezett csoporttag](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="11aeb-115">Általános erőforrás követelményeinek teljesítése több elnevezett erőforrással</span><span class="sxs-lookup"><span data-stu-id="11aeb-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="11aeb-116">Egy általános erőforrás követelménye több elnevezett erőforrással is teljesíthető, hasonlóan, mint egy elnevezett erőforrás hozzárendelése esetén.</span><span class="sxs-lookup"><span data-stu-id="11aeb-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="11aeb-117">Például, adott egy feladat, amely öt nap és 120 óra ráfordítást igényel.</span><span class="sxs-lookup"><span data-stu-id="11aeb-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="11aeb-118">Ezt a feladatot nem lehet egy olyan erőforrással befejezni, amely egy ötnapos héten átlagosan napi nyolc órát dolgozik.</span><span class="sxs-lookup"><span data-stu-id="11aeb-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Öt nap alatt 120 órányi erőfeszítést igénylő feladat](media/RM-how-to-21.png)

<span data-ttu-id="11aeb-120">A követelmény 120 órányi robotikai mérnöki tevékenység öt nap alatt, tehát napi 24 óra.</span><span class="sxs-lookup"><span data-stu-id="11aeb-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Napi követelmény](media/RM-how-to-22.png)

<span data-ttu-id="11aeb-122">Ez egy példa arra az esetre, amikor egy általános erőforrás-kérelem teljesítéséhez több elnevezett erőforrásra van szükség.</span><span class="sxs-lookup"><span data-stu-id="11aeb-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="11aeb-123">A követelmény teljesítéséhez több erőforrást is le kell foglalnia.</span><span class="sxs-lookup"><span data-stu-id="11aeb-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Több erőforrás foglalása a követelmény teljesítéséhez](media/RM-how-to-23.png)

<span data-ttu-id="11aeb-125">A fő különbség ezen forgatókönyv esetén, hogy az általános erőforrás a feladathoz rendelt csoportban marad, és a foglalt elnevezett erőforráscsoport-tagok nem lesznek hozzárendelve a pozíció részeként.</span><span class="sxs-lookup"><span data-stu-id="11aeb-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="11aeb-126">A projektvezető a munkát megfelelő módon hozzárendelheti az elnevezett erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="11aeb-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="11aeb-127">Az **Egyeztetés** segíthet a projektkezelőnek a foglalás több erőforrás közötti lebontásában a feladat-hozzárendelésekhez.</span><span class="sxs-lookup"><span data-stu-id="11aeb-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="11aeb-128">Ez nem történik meg automatikusan, mert a fenti egyszerű példánál bonyolultabb forgatókönyv esetén (például, ha a követelményt számos feladat teszi ki) a szándékkal, a rendszernek feltételeznie kell a projektkezelő által igényelt hozzárendelési módot.</span><span class="sxs-lookup"><span data-stu-id="11aeb-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="11aeb-129">Mivel a rendszer nem érti a szándékot, előfordulhat, hogy a feltételezések eltérnek a szándékolt módszertől, és az nem megfelelő vagy kiszámíthatatlan eredményt okoz.</span><span class="sxs-lookup"><span data-stu-id="11aeb-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="11aeb-130">A kiszámítható eredmény az, hogy az általános erőforrás mindaddig hozzá lesz rendelve, amíg a projetkezelő szándékosan hozza létre a hozzárendeléseket az **Egyeztetés** nézet segítségével.</span><span class="sxs-lookup"><span data-stu-id="11aeb-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>

