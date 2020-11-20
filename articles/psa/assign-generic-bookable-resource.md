---
title: Általános foglalható erőforrások hozzárendelése egy feladathoz és projektcsoporthoz
description: Ez a témakör információt nyújt az általános erőforrásoknak a feladatokhoz és a projektcsoportokhoz való foglalásáról.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 19761b3e570ad664522e832069a8ac50fffead64
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127071"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="2b33d-103">Általános foglalható erőforrások hozzárendelése egy feladathoz és erőforrás-követelmények generálása</span><span class="sxs-lookup"><span data-stu-id="2b33d-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2b33d-104">A lefoglalások és a nevesített vagy valós erőforrások projekthez rendelése mellett általános erőforrásokat is hozzárendelhet a projekt feladataihoz.</span><span class="sxs-lookup"><span data-stu-id="2b33d-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="2b33d-105">Ezek az erőforrások a nevesített erőforrások számára helyőrzőként szolgálhatnak, amíg készen nem áll a projekt nevesített erőforrásokkal való ellátására.</span><span class="sxs-lookup"><span data-stu-id="2b33d-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="2b33d-106">Nyissa meg a **Projekt** oldalt a Project Service Automation (PSA) programban, majd az **Ütemezés** lapon adja meg az általános erőforrás pozíciójának nevét az ütemezés **Erőforrás** cellájában.</span><span class="sxs-lookup"><span data-stu-id="2b33d-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="2b33d-107">Másik lehetőségként kattintson a cellában az **Erőforrás** ikonra, és nyissa meg az Erőforrás-választót, majd adja meg a létrehozni kívánt általános erőforrás nevét.</span><span class="sxs-lookup"><span data-stu-id="2b33d-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Általános csoporttag létrehozása és hozzárendelése](media/RM-how-to-9.png)

<span data-ttu-id="2b33d-109">Ekkor megnyílik a **Projektcsoport tag gyors létrehozása** panel.</span><span class="sxs-lookup"><span data-stu-id="2b33d-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="2b33d-110">Adja meg az általános erőforráscsoport tagjának szerepkörét és szervezeti egységét, majd kattintson **Mentés** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="2b33d-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Általános csoporttag gyors létrehozása](media/RM-how-to-10.png)

3. <span data-ttu-id="2b33d-112">Miután létrehozta az új általános erőforráscsoport-tagot, az hozzárendelésre kerül a feladathoz.</span><span class="sxs-lookup"><span data-stu-id="2b33d-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="2b33d-113">Az adott általános erőforrást továbbra is hozzárendelheti a feladatütemezésben szereplő egyéb feladatokhoz.</span><span class="sxs-lookup"><span data-stu-id="2b33d-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Meglévő általános csoporttag hozzárendelése feladatokhoz](media/RM-how-to-11.png)

4. <span data-ttu-id="2b33d-115">Miután hozzárendelte az általános erőforrást, létrehozhat egy erőforrás-követelményt, és teljesítheti azt közvetlen foglalással, vagy egy erőforrás-kérelemnek az erőforrás-kezelőnek való elküldésével.</span><span class="sxs-lookup"><span data-stu-id="2b33d-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Általános csoporttagra vonatkozó követelmény létrehozása](media/RM-how-to-12.png)

<span data-ttu-id="2b33d-117">A csoporttag rácson a fentiek szerint használhatja az erőforrás-választót, de általános erőforrásokat közvetlenül is hozzáadhat itt.</span><span class="sxs-lookup"><span data-stu-id="2b33d-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="2b33d-118">Az erőforrások egy olyan erőforrás-követelménnyel kerülnek hozzáadásra, amely a **Gyors létrehozás: projekt csoporttag** panelen megadott kezdő/végdátumokon és felosztási módszereken alapul.</span><span class="sxs-lookup"><span data-stu-id="2b33d-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="2b33d-119">A különbség akkor jelenik meg, ha közvetlenül hozzáadja az általános csoporttagot, majd több feladatot rendel hozzá az általános erőforráshoz, mint ahány óra rendelkezésre áll azok lefedéséhez.</span><span class="sxs-lookup"><span data-stu-id="2b33d-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="2b33d-120">Kattintson a **Követelmény létrehozása** lehetőségre a követelmény újbóli létrehozásához, a szükséges órák és a hozzárendelések kiegyensúlyozása érdekében.</span><span class="sxs-lookup"><span data-stu-id="2b33d-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="2b33d-121">Az **Erőforrás-követelmény** hivatkozásra kattintva a csoport rácson is megnyithatja a követelményt, és készségeket, előnyben részesített erőforrásokat stb. adhat hozzá.</span><span class="sxs-lookup"><span data-stu-id="2b33d-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Erőforrás-követelmény](media/RM-how-to-13.png)

