---
title: Projekt létrehozása
description: Projektárajánlat létrehozása a Project Service szolgáltatásban
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/13/2020
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
ms.openlocfilehash: 93958f8e7654ebc4cb038ba7ca0c5e4e02f39937
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148871"
---
# <a name="create-a-project-project-service"></a><span data-ttu-id="250fc-103">Projekt létrehozása (Project Service)</span><span class="sxs-lookup"><span data-stu-id="250fc-103">Create a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="250fc-104">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] segít a projekt létrehozásában a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] rendszerben, amikor projektalapú szolgáltatásokhoz szeretne lehetőséget, árajánlatot vagy szerződést létrehozni.</span><span class="sxs-lookup"><span data-stu-id="250fc-104">Create a project using the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] when you want to create an opportunity, quote, or contract for project-based services.</span></span> <span data-ttu-id="250fc-105">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] segít a projektek kezelésében a lehetőségtől a befejezésig.</span><span class="sxs-lookup"><span data-stu-id="250fc-105">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities help you manage your project from opportunity through completion.</span></span> <span data-ttu-id="250fc-106">Amikor létrehoz egy projektet, akkor létrehoz egy munkalebontási struktúrát is, amely hatással van az árajánlatokra, a költségbecslésekre és az erőforrás-kezelésre.</span><span class="sxs-lookup"><span data-stu-id="250fc-106">When you create a project, you’ll also create a work breakdown structure, which affects your quotes, cost estimates, and resource management.</span></span>  
  
1.  <span data-ttu-id="250fc-107">Lépjen a **Project Service > Projektek** pontba.</span><span class="sxs-lookup"><span data-stu-id="250fc-107">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="250fc-108">Kattintson az **Új projekt** pontra.</span><span class="sxs-lookup"><span data-stu-id="250fc-108">Click **New Project**.</span></span>  
  
3.  <span data-ttu-id="250fc-109">Az **Összefoglaló** területen adja meg a projekt nevét, és töltsön ki annyi részletet, amennyit csak lehet.</span><span class="sxs-lookup"><span data-stu-id="250fc-109">In the **Summary** area, enter a name for your project, and then fill in as many of the details as you can.</span></span> <span data-ttu-id="250fc-110">A kötelezően kitöltendő mezőket piros színű csillag (\*) jelzi.</span><span class="sxs-lookup"><span data-stu-id="250fc-110">Items marked with a red asterisk (\*) are required.</span></span>  
  
4.  <span data-ttu-id="250fc-111">Kattintson a **Mentés** gombra a projekt létrehozásához, hogy folytathassa a szerkesztést.</span><span class="sxs-lookup"><span data-stu-id="250fc-111">Click **Save** to create your project so you can continue editing it.</span></span>  
  
<span data-ttu-id="250fc-112">Ezután egy munkalebontási struktúrát fog létrehozni a projekthez, hogy definiálja a projekthez szükséges feladatokat, időzítést és erőforrás-szerepköröket.</span><span class="sxs-lookup"><span data-stu-id="250fc-112">Next, you’ll create a work breakdown structure for your project to define the tasks, timing, and resource roles needed for the project.</span></span>  

> [!NOTE]
> <span data-ttu-id="250fc-113">Az ütemezés során a Project Service Automation tiszteletben tartja az alkalmazott **Munkaidő** sablon időzónáját.</span><span class="sxs-lookup"><span data-stu-id="250fc-113">When scheduling, Project Service Automation respects the time zone of the applied **Work Hour** template.</span></span> <span data-ttu-id="250fc-114">Az ütemezési feladatok megtekintésekor azonban a program a felhasználó időzónájában jeleníti meg a feladat kezdő és befejező dátumát.</span><span class="sxs-lookup"><span data-stu-id="250fc-114">However, when viewing the schedule tasks, the start and end dates of a task will be displayed in the user's time zone.</span></span> <span data-ttu-id="250fc-115">Ez a **Projekt** űrlap egyéb időszakos nézeteire is vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="250fc-115">This applies to other time-phased views in the **Project** form.</span></span> <span data-ttu-id="250fc-116">Ha a felhasználó időzónája nem egyezik meg a projektre alkalmazott munkaidő-sablon időzónájával, akkor egy figyelmeztetés jelenik meg, amely ismerteti az eltéréseket.</span><span class="sxs-lookup"><span data-stu-id="250fc-116">If the user's time zone does not match the time zone of the work hour template applied to the project, a warning which explains the difference will occur.</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="250fc-117">Kapcsolódó információk</span><span class="sxs-lookup"><span data-stu-id="250fc-117">See Also</span></span>  
 [<span data-ttu-id="250fc-118">Projektmenedzseri útmutató</span><span class="sxs-lookup"><span data-stu-id="250fc-118">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
