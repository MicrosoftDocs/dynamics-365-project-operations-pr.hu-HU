---
title: Projektállapot nyomon követése
description: Projekt állapotának nyomkövetése a Project Service szolgáltatásban
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
ms.openlocfilehash: d57f33cdf240db4cae1f33fe962173790fe0fe7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281931"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="82fd1-103">Projekt állapotának nyomkövetése (Project Service)</span><span class="sxs-lookup"><span data-stu-id="82fd1-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="82fd1-104">A [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] használatával nyomon követhető egy ügyfél projektjének fejlődése.</span><span class="sxs-lookup"><span data-stu-id="82fd1-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="82fd1-105">Az ügylet előrehaladásával a projekt fázisai frissülnek, hogy tükrözzék az ügylet fázisát:</span><span class="sxs-lookup"><span data-stu-id="82fd1-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="82fd1-106">**Új**</span><span class="sxs-lookup"><span data-stu-id="82fd1-106">**New**</span></span>    | <span data-ttu-id="82fd1-107">A projekt létrehozásakor a fázis értéke az **Új**.</span><span class="sxs-lookup"><span data-stu-id="82fd1-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="82fd1-108">Ha a projektet egy sablonból hozta létre, akkor a projekt ebben a fázisban rendelkezhet ütemezéssel, becslésekkel és a csoportadatokkal.</span><span class="sxs-lookup"><span data-stu-id="82fd1-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="82fd1-109">Ellenkező esetben a projekt vázlata lesz, és manuálisan kell megadni a többi projekt-összetevőt.</span><span class="sxs-lookup"><span data-stu-id="82fd1-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="82fd1-110">**Ajánlat**</span><span class="sxs-lookup"><span data-stu-id="82fd1-110">**Quote**</span></span>   |      <span data-ttu-id="82fd1-111">Amikor egy árajánlathoz társít egy projektet, vagy egy árajánlatból hozza azt létre, a projekt fázisa **Árajánlat** lesz, és frissülnek a becsült kezdési és befejezési dátumok is.</span><span class="sxs-lookup"><span data-stu-id="82fd1-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="82fd1-112">Amikor a projekt az árajánlati fázisban tart, az árajánlat részletei a **Sales** lapon jelennek meg, a **Projekt** oldalon.</span><span class="sxs-lookup"><span data-stu-id="82fd1-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="82fd1-113">**Terv**</span><span class="sxs-lookup"><span data-stu-id="82fd1-113">**Plan**</span></span>   |                                     <span data-ttu-id="82fd1-114">Amikor nyer egy projekthez társított árajánlattal, és az ügylet eléri a szerződés fázist, a projekt fázis a **Terv** fázisra frissül.</span><span class="sxs-lookup"><span data-stu-id="82fd1-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="82fd1-115">A szerződés részletei a **Sales** lapon jelennek meg, a **Projekt** oldalon.</span><span class="sxs-lookup"><span data-stu-id="82fd1-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="82fd1-116">**Teljes**</span><span class="sxs-lookup"><span data-stu-id="82fd1-116">**Complete**</span></span> |                    <span data-ttu-id="82fd1-117">Amikor a projekten végzett munka véget ért, módosíthatja a fázist **Befejezettre**.</span><span class="sxs-lookup"><span data-stu-id="82fd1-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="82fd1-118">Ha a projektfázis értéke befejezett, az azt jelenti, hogy a munka 100%-át sikerült elvégezni, de a projekt még nyitott, hogy meg lehessen adni az esetlegesen még függő idő- és kiadásbejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="82fd1-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="82fd1-119">**Bezárás**</span><span class="sxs-lookup"><span data-stu-id="82fd1-119">**Close**</span></span>   |           <span data-ttu-id="82fd1-120">Amikor a projekthez tartozó minden tranzakció rögzítésre került, és nem várja továbbiak naplózását, akkor manuálisan beállíthatja a fázist **Lezártra**.</span><span class="sxs-lookup"><span data-stu-id="82fd1-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="82fd1-121">Ha a projekt fázisa **Lezárt**, nem rögzíthet további tranzakciókat a projekthez, és a projekt csak olvasható lesz.</span><span class="sxs-lookup"><span data-stu-id="82fd1-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="82fd1-122">Projektállapot követése</span><span class="sxs-lookup"><span data-stu-id="82fd1-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="82fd1-123">Lépjen a **Project Service > Projektek** pontba.</span><span class="sxs-lookup"><span data-stu-id="82fd1-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="82fd1-124">Kattintson arra a projektre, amellyel dolgozni szeretne.</span><span class="sxs-lookup"><span data-stu-id="82fd1-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="82fd1-125">A képernyő felső részén található sávon válassza ki a projekt neve melletti lefelé mutató nyilat, majd kattintson a **Projektkövetés** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="82fd1-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="82fd1-126">Válassza a **Ráfordításkövetés** vagy a **Költségkövetés** lehetőséget a legördülő listában a feladatlista felett.</span><span class="sxs-lookup"><span data-stu-id="82fd1-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="82fd1-127">Kattintson duplán a szerkeszteni kívánt feladatra.</span><span class="sxs-lookup"><span data-stu-id="82fd1-127">Double-click any task to edit it.</span></span> <span data-ttu-id="82fd1-128">Áthelyezheti vagy átméretezheti az Gantt-diagram oszlopait, ha módosítani akarja egy feladat idejét és előrehaladását.</span><span class="sxs-lookup"><span data-stu-id="82fd1-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="82fd1-129">Kapcsolódó információk</span><span class="sxs-lookup"><span data-stu-id="82fd1-129">See Also</span></span>  
 [<span data-ttu-id="82fd1-130">Projektmenedzseri útmutató</span><span class="sxs-lookup"><span data-stu-id="82fd1-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]