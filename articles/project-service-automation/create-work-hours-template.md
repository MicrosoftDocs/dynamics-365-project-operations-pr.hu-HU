---
title: Munkaidősablon létrehozása
description: Munkaidősablon létrehozása a Project Service szolgáltatásban
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 1a519487-25f1-4e9d-b739-1c1becf1d649
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5e7ef4af5f22419cccd8f29ea2a0a0a21a75875a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752253"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="1e3ad-103">Munkaidősablon létrehozása (Project Service)</span><span class="sxs-lookup"><span data-stu-id="1e3ad-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="1e3ad-104">Mielőtt projektütemezéseket hozhatna létre, állítson be egy projektnaptárat, amely meghatározza a napi munkaórák számát és a szünnapokat.</span><span class="sxs-lookup"><span data-stu-id="1e3ad-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="1e3ad-105">Ezt egy munkaidősablonnal teheti meg, amely tartalmazza a napi munkaidőre, szabadnapokra és egyéb szünnapokra vonatkozó részleteket.</span><span class="sxs-lookup"><span data-stu-id="1e3ad-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="1e3ad-106">Egy projekt létrehozásakor egy munkasablont társít a projektnaptárhoz, hogy alkalmazza az ütemezést a projektre.</span><span class="sxs-lookup"><span data-stu-id="1e3ad-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="1e3ad-107">Két módon hozhat létre egy munkaidő sablont:</span><span class="sxs-lookup"><span data-stu-id="1e3ad-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="1e3ad-108">Munkaidősablon létrehozása egy erőforrás naptára alapján.</span><span class="sxs-lookup"><span data-stu-id="1e3ad-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="1e3ad-109">Új munkaidősablon létrehozása.</span><span class="sxs-lookup"><span data-stu-id="1e3ad-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="1e3ad-110">Munkaidősablon létrehozása egy erőforrás naptára alapján</span><span class="sxs-lookup"><span data-stu-id="1e3ad-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="1e3ad-111">Lépjen a **Project Service > Erőforrások** pontba.</span><span class="sxs-lookup"><span data-stu-id="1e3ad-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="1e3ad-112">Erőforrás kiválasztása, amelyre a munkaidőt akarja alapozni.</span><span class="sxs-lookup"><span data-stu-id="1e3ad-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="1e3ad-113">Kattintson a **Naptár mentése másként** lehetőségre, adja meg a munkaidősablon nevét, és kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="1e3ad-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="1e3ad-114">Ha végzett a beállítások módosításával kattintson a **Mentés és bezárás** gombra.</span><span class="sxs-lookup"><span data-stu-id="1e3ad-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="1e3ad-115">Kattintson a **Mentés** gombra a képernyő jobb alsó sarkában.</span><span class="sxs-lookup"><span data-stu-id="1e3ad-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="1e3ad-116">Új munkaidősablon létrehozása</span><span class="sxs-lookup"><span data-stu-id="1e3ad-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="1e3ad-117">Lépjen a **Project Service > Munkaidősablonok** pontba.</span><span class="sxs-lookup"><span data-stu-id="1e3ad-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="1e3ad-118">Kattintson az **Új** elemre.</span><span class="sxs-lookup"><span data-stu-id="1e3ad-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="1e3ad-119">Adja meg a munkaidősablon nevét.</span><span class="sxs-lookup"><span data-stu-id="1e3ad-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="1e3ad-120">Válasszon ki egy erőforrást, amelyre a munkaidőt akarja alapozni, és kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="1e3ad-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="1e3ad-121">Kapcsolódó információk</span><span class="sxs-lookup"><span data-stu-id="1e3ad-121">See Also</span></span>  
 [<span data-ttu-id="1e3ad-122">Erőforrások beállítása</span><span class="sxs-lookup"><span data-stu-id="1e3ad-122">Set up resources</span></span>](../project-service/set-up-resources.md)
