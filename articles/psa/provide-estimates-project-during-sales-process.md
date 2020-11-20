---
title: Munkabecslések biztosítása egy projekthez az értékesítési folyamat során
description: Munkabecslések biztosítása egy projekthez az értékesítési folyamat során a Project Service szolgáltatásban
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
ms.openlocfilehash: 7bd83b6872d437f1d074d6ea2336c751bdfdd9e6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120591"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="c26c2-103">Munkabecslések biztosítása egy projekthez az értékesítési folyamat során (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c26c2-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c26c2-104">Az értékesítési folyamat során teljesen új értékesítési becsléseket dolgozhat ki árajánlatsorokkal.</span><span class="sxs-lookup"><span data-stu-id="c26c2-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="c26c2-105">képességeinek a(z) [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] tudományosabb és determinisztikusabb módon készíthetők értékesítési becslések a munkatételek lebontásával és a projektbecslések szempontjából lényeges attribútumok társításával a munkalebontási struktúrában.</span><span class="sxs-lookup"><span data-stu-id="c26c2-105">capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="c26c2-106">Az értékesítés elnyerését követően használhatja a társított munkalebontási struktúrát a projekttervben, hogy szükség szerint finomítsa azt a projekt sikeres kivitelezése érdekében.</span><span class="sxs-lookup"><span data-stu-id="c26c2-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="c26c2-107">Egy projekt árajánlatsorhoz kapcsolása</span><span class="sxs-lookup"><span data-stu-id="c26c2-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="c26c2-108">Egy projektalapú árajánlatsor létrehozásakor létrehozhat új projektet az árajánlatsorból.</span><span class="sxs-lookup"><span data-stu-id="c26c2-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="c26c2-109">Ekkor használhat projektsablonokat, amelyek vagy előre konfigurált, a szervezetében gyakori, szabványos projektterv és a pénzügyi becslések vagy egy korábbi projektből származó projektterv és becslések másolata.</span><span class="sxs-lookup"><span data-stu-id="c26c2-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="c26c2-110">Egy projekt létrehozásakor a projektsablon kiválasztása biztosít alapot a projektterv, a becslések és a szerepkör-követelmények finomításához.</span><span class="sxs-lookup"><span data-stu-id="c26c2-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="c26c2-111">Ha árajánlatból hoz létre projektet, akkor a rendszer automatikusan társítja a projektet az árajánlatsorhoz.</span><span class="sxs-lookup"><span data-stu-id="c26c2-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="c26c2-112">Projektbecslések összetevői</span><span class="sxs-lookup"><span data-stu-id="c26c2-112">Project estimate components</span></span>  
 <span data-ttu-id="c26c2-113">A projekt munkalebontási struktúrája segítségével bontható a munka feladatokra, tartható fent a feladatok hierarchiája, és társítható egy becslés az egyes feladatokhoz az elvégzésükhöz szükséges ráfordításról.</span><span class="sxs-lookup"><span data-stu-id="c26c2-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="c26c2-114">Továbbá társíthat szerepköröket is egy feladathoz, így megadva egy becslést az erőforrás-típusra vonatkozóan, amelyre szükség van a feladat és az ütemterv befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="c26c2-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="c26c2-115">A munkalebontási struktúra segít meghatározni a munkaráfordítást és ütemezni a becsléseket.</span><span class="sxs-lookup"><span data-stu-id="c26c2-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="c26c2-116">Alapértelmezés szerint a projekt korábban meghatározott alapértelmezett árlistákat használja.</span><span class="sxs-lookup"><span data-stu-id="c26c2-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="c26c2-117">Az árlistákban meghatározott önköltségi és értékesítési árak segítenek meghatározni a pénzügyi becsléseket a projekt munkalebontásához.</span><span class="sxs-lookup"><span data-stu-id="c26c2-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="c26c2-118">Ha a projekthez egy árajánlat társul, és az árajánlat az alapértelmezettől eltérő árlistával rendelkezik, akkor az árajánlat árlistáját használja a rendszer a pénzügyi becslésekhez.</span><span class="sxs-lookup"><span data-stu-id="c26c2-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="c26c2-119">Becslések importálása egy projektből egy árajánlatba</span><span class="sxs-lookup"><span data-stu-id="c26c2-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="c26c2-120">Ha rendelkezik projektbecslésekkel a projektben, akkor importálhatja ezeket a becsléseket az árajánlatsorba:</span><span class="sxs-lookup"><span data-stu-id="c26c2-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="c26c2-121">Az **Árajánlatsor részletei** részben kattintson az **Importálás becslésekből** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="c26c2-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="c26c2-122">Válassza ki, hogy a projektbecslések importálásakor az összegzés a tranzakciótípus, a szerepkör vagy a munkalebontási struktúra csomópontszintje alapján történjen.</span><span class="sxs-lookup"><span data-stu-id="c26c2-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c26c2-123">Kapcsolódó információk</span><span class="sxs-lookup"><span data-stu-id="c26c2-123">See Also</span></span>  
 [<span data-ttu-id="c26c2-124">Projektmenedzseri útmutató</span><span class="sxs-lookup"><span data-stu-id="c26c2-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
