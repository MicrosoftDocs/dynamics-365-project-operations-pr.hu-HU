---
title: Munkaidősablon létrehozása
description: Munkaidősablon létrehozása a Project Service szolgáltatásban
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 5e859a58f86d8cd98fa429beeeb99cf397a207cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285036"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="b3aa5-103">Munkaidősablon létrehozása (Project Service)</span><span class="sxs-lookup"><span data-stu-id="b3aa5-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="b3aa5-104">Mielőtt projektütemezéseket hozhatna létre, állítson be egy projektnaptárat, amely meghatározza a napi munkaórák számát és a szünnapokat.</span><span class="sxs-lookup"><span data-stu-id="b3aa5-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="b3aa5-105">Ezt egy munkaidősablonnal teheti meg, amely tartalmazza a napi munkaidőre, szabadnapokra és egyéb szünnapokra vonatkozó részleteket.</span><span class="sxs-lookup"><span data-stu-id="b3aa5-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="b3aa5-106">Egy projekt létrehozásakor egy munkasablont társít a projektnaptárhoz, hogy alkalmazza az ütemezést a projektre.</span><span class="sxs-lookup"><span data-stu-id="b3aa5-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="b3aa5-107">Két módon hozhat létre egy munkaidő sablont:</span><span class="sxs-lookup"><span data-stu-id="b3aa5-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="b3aa5-108">Munkaidősablon létrehozása egy erőforrás naptára alapján.</span><span class="sxs-lookup"><span data-stu-id="b3aa5-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="b3aa5-109">Új munkaidősablon létrehozása.</span><span class="sxs-lookup"><span data-stu-id="b3aa5-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="b3aa5-110">Munkaidősablon létrehozása egy erőforrás naptára alapján</span><span class="sxs-lookup"><span data-stu-id="b3aa5-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="b3aa5-111">Lépjen a **Project Service > Erőforrások** pontba.</span><span class="sxs-lookup"><span data-stu-id="b3aa5-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="b3aa5-112">Erőforrás kiválasztása, amelyre a munkaidőt akarja alapozni.</span><span class="sxs-lookup"><span data-stu-id="b3aa5-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="b3aa5-113">Kattintson a **Naptár mentése másként** lehetőségre, adja meg a munkaidősablon nevét, és kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="b3aa5-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="b3aa5-114">Ha végzett a beállítások módosításával kattintson a **Mentés és bezárás** gombra.</span><span class="sxs-lookup"><span data-stu-id="b3aa5-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="b3aa5-115">Kattintson a **Mentés** gombra a képernyő jobb alsó sarkában.</span><span class="sxs-lookup"><span data-stu-id="b3aa5-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="b3aa5-116">Új munkaidősablon létrehozása</span><span class="sxs-lookup"><span data-stu-id="b3aa5-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="b3aa5-117">Lépjen a **Project Service > Munkaidősablonok** pontba.</span><span class="sxs-lookup"><span data-stu-id="b3aa5-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="b3aa5-118">Kattintson az **Új** elemre.</span><span class="sxs-lookup"><span data-stu-id="b3aa5-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="b3aa5-119">Adja meg a munkaidősablon nevét.</span><span class="sxs-lookup"><span data-stu-id="b3aa5-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="b3aa5-120">Válasszon ki egy erőforrást, amelyre a munkaidőt akarja alapozni, és kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="b3aa5-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="b3aa5-121">Kapcsolódó információk</span><span class="sxs-lookup"><span data-stu-id="b3aa5-121">See Also</span></span>  
 [<span data-ttu-id="b3aa5-122">Erőforrások beállítása</span><span class="sxs-lookup"><span data-stu-id="b3aa5-122">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]