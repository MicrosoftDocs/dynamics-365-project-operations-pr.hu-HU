---
title: Erőforrás szerepkörök konfigurálása
description: Erőforrás-szerepek testreszabása a Project Service szolgáltatásban
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 5f899d17980df16602c964bab4bbab1e976b3ebf
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078090"
---
# <a name="configure-resource-roles-project-service"></a><span data-ttu-id="aadc1-103">Erőforrás-szerepek testreszabása (Project Service)</span><span class="sxs-lookup"><span data-stu-id="aadc1-103">Configure resource roles (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="aadc1-104">A szerepkörök az erőforrás-követelmények és a projektköltségek meghatározásával kapcsolatban fontosak a projekttervezés szempontjából.</span><span class="sxs-lookup"><span data-stu-id="aadc1-104">Roles play an important part in project planning, when determining resource requirements or costs of a project.</span></span> <span data-ttu-id="aadc1-105">A projektekhez szükséges minden szerepkörhöz létre kell hozni egy erőforrás-szerepkört, amelyhez képzettségeket és jártasságokat kell társítani.</span><span class="sxs-lookup"><span data-stu-id="aadc1-105">For each role your projects require, you need to create a resource role and associate skills and proficiencies to that role.</span></span> <span data-ttu-id="aadc1-106">Például érdemes lehet létrehozni szerepköröket fejlesztők, projektmenedzserek vagy játéktesztelők számára.</span><span class="sxs-lookup"><span data-stu-id="aadc1-106">For example, you might want to create roles for developer, project manager, or game tester.</span></span> <span data-ttu-id="aadc1-107">Ezen kívül be kell állítania a képzettségeket és a jártassági szinteket is a szerepkörhöz.</span><span class="sxs-lookup"><span data-stu-id="aadc1-107">You’ll also set the skills and proficiency levels required for the role.</span></span>  
  
 <span data-ttu-id="aadc1-108">Az erőforrás-szerepkörök konfigurálásával biztosíthatja szervezete számára a hatékony projektbecslést.</span><span class="sxs-lookup"><span data-stu-id="aadc1-108">Configure resource roles to ensure effective project estimation for your organization.</span></span>  <span data-ttu-id="aadc1-109">Arra is ügyeljen, hogy pontosan állítsa be számlázás típusát.</span><span class="sxs-lookup"><span data-stu-id="aadc1-109">Also make sure you accurately set the billing type.</span></span> <span data-ttu-id="aadc1-110">A nem számlázható számlázási típussal rendelkező elemek nem jelennek meg a szerződés- és árajánlatsorokban.</span><span class="sxs-lookup"><span data-stu-id="aadc1-110">An item set with a non-chargeable billing type doesn’t show up on contract or quote lines.</span></span>  
  
 <span data-ttu-id="aadc1-111">Amikor beállította az erőforrás-szerepköröket, beállíthatja az önköltségi és az értékesítési árakat.</span><span class="sxs-lookup"><span data-stu-id="aadc1-111">Once you’ve set up resource roles, you can set up cost and sales prices with a price list.</span></span>  
  
 <span data-ttu-id="aadc1-112">Minden hozzáadni kívánt szerepkör esetében végezze el a következőket:</span><span class="sxs-lookup"><span data-stu-id="aadc1-112">For each role you want to add, do the following:</span></span>  
  
1.  <span data-ttu-id="aadc1-113">Lépjen a **Project Service > Erőforrás-szerepkörök** pontba.</span><span class="sxs-lookup"><span data-stu-id="aadc1-113">Go to **Project Service > Resource Roles**.</span></span>  
  
2.  <span data-ttu-id="aadc1-114">Kattintson az **Új** elemre.</span><span class="sxs-lookup"><span data-stu-id="aadc1-114">Click **New**.</span></span>  
  
3.  <span data-ttu-id="aadc1-115">Az **Általános** területen adja meg a szerepkör nevét a **Név** mezőben, majd szükség szerint töltse ki a többi mezőt.</span><span class="sxs-lookup"><span data-stu-id="aadc1-115">In the **General** area, enter a name for the role in **Name** , and then fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="aadc1-116">Kattintson a **Mentés** gombra a bejegyzés létrehozásához, hogy folytathassa a szerkesztést.</span><span class="sxs-lookup"><span data-stu-id="aadc1-116">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="aadc1-117">Képzettség hozzáadásához a **Képzettségek** területen kattintson a **+** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="aadc1-117">In the **Skills** area, click **+** to add a skill.</span></span>  
  
6.  <span data-ttu-id="aadc1-118">A **Szerepkör kompetenciakövetelménye** ablaktáblán kattintson a **Képzettség** mezőbe, majd kattintson a **Keresés** gombra, és válasszon ki egy képzettséget.</span><span class="sxs-lookup"><span data-stu-id="aadc1-118">In the **Role competency requirement** pane, click in the **Skill** field, click the **Search** button, and then select a skill.</span></span>  
  
7.  <span data-ttu-id="aadc1-119">Válasszon egy jártasságot a képzettséghez, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="aadc1-119">Select a proficiency for that skill, and then click **Save**.</span></span>  
  
8.  <span data-ttu-id="aadc1-120">Folytassa a képzettségek hozzáadását, ameddig szükséges.</span><span class="sxs-lookup"><span data-stu-id="aadc1-120">Continue adding skills as necessary.</span></span> <span data-ttu-id="aadc1-121">Amikor végzett kattintson a **Mentés** gombra a képernyő jobb alsó sarkában.</span><span class="sxs-lookup"><span data-stu-id="aadc1-121">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
9. <span data-ttu-id="aadc1-122">Ha szeretné elérhetővé tenni ezt az erőforrás-szerepkört projektek számára, kattintson az **Aktiválás** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="aadc1-122">To make this resource role available for projects to use, click **Activate**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="aadc1-123">Kapcsolódó információk</span><span class="sxs-lookup"><span data-stu-id="aadc1-123">See Also</span></span>  
 [<span data-ttu-id="aadc1-124">Erőforrások beállítása</span><span class="sxs-lookup"><span data-stu-id="aadc1-124">Set up resources</span></span>](../psa/set-up-resources.md)
