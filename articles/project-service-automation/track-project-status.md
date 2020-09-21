---
title: Projektállapot nyomon követése
description: Projekt állapotának nyomkövetése a Project Service szolgáltatásban
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7610aecb-318c-422b-b626-9106b0736b5f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: e4d53b6235c3b941bce525dca09ee3d647c3d242
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752297"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="44d40-103">Projekt állapotának nyomkövetése (Project Service)</span><span class="sxs-lookup"><span data-stu-id="44d40-103">Track a project’s status (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="44d40-104">A [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] használatával nyomon követhető egy ügyfél projektjének fejlődése.</span><span class="sxs-lookup"><span data-stu-id="44d40-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="44d40-105">Az ügylet előrehaladásával a projekt fázisai frissülnek, hogy tükrözzék az ügylet fázisát:</span><span class="sxs-lookup"><span data-stu-id="44d40-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="44d40-106">**Új**</span><span class="sxs-lookup"><span data-stu-id="44d40-106">**New**</span></span>    | <span data-ttu-id="44d40-107">A projekt létrehozásakor a fázis értéke az **Új**.</span><span class="sxs-lookup"><span data-stu-id="44d40-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="44d40-108">Ha a projektet egy sablonból hozta létre, akkor a projekt ebben a fázisban rendelkezhet ütemezéssel, becslésekkel és a csoportadatokkal.</span><span class="sxs-lookup"><span data-stu-id="44d40-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="44d40-109">Ellenkező esetben a projekt vázlata lesz, és manuálisan kell megadni a többi projekt-összetevőt.</span><span class="sxs-lookup"><span data-stu-id="44d40-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="44d40-110">**Ajánlat**</span><span class="sxs-lookup"><span data-stu-id="44d40-110">**Quote**</span></span>   |      <span data-ttu-id="44d40-111">Amikor egy árajánlathoz társít egy projektet, vagy egy árajánlatból hozza azt létre, a projekt fázisa **Árajánlat** lesz, és frissülnek a becsült kezdési és befejezési dátumok is.</span><span class="sxs-lookup"><span data-stu-id="44d40-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="44d40-112">Amikor a projekt az árajánlati fázisban tart, az árajánlat részletei a **Sales** lapon jelennek meg, a **Projekt** oldalon.</span><span class="sxs-lookup"><span data-stu-id="44d40-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="44d40-113">**Terv**</span><span class="sxs-lookup"><span data-stu-id="44d40-113">**Plan**</span></span>   |                                     <span data-ttu-id="44d40-114">Amikor nyer egy projekthez társított árajánlattal, és az ügylet eléri a szerződés fázist, a projekt fázis a **Terv** fázisra frissül.</span><span class="sxs-lookup"><span data-stu-id="44d40-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="44d40-115">A szerződés részletei a **Sales** lapon jelennek meg, a **Projekt** oldalon.</span><span class="sxs-lookup"><span data-stu-id="44d40-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="44d40-116">**Teljes**</span><span class="sxs-lookup"><span data-stu-id="44d40-116">**Complete**</span></span> |                    <span data-ttu-id="44d40-117">Amikor a projekten végzett munka véget ért, módosíthatja a fázist **Befejezettre**.</span><span class="sxs-lookup"><span data-stu-id="44d40-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="44d40-118">Ha a projektfázis értéke befejezett, az azt jelenti, hogy a munka 100%-át sikerült elvégezni, de a projekt még nyitott, hogy meg lehessen adni az esetlegesen még függő idő- és kiadásbejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="44d40-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="44d40-119">**Bezárás**</span><span class="sxs-lookup"><span data-stu-id="44d40-119">**Close**</span></span>   |           <span data-ttu-id="44d40-120">Amikor a projekthez tartozó minden tranzakció rögzítésre került, és nem várja továbbiak naplózását, akkor manuálisan beállíthatja a fázist **Lezártra**.</span><span class="sxs-lookup"><span data-stu-id="44d40-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="44d40-121">Ha a projekt fázisa **Lezárt**, nem rögzíthet további tranzakciókat a projekthez, és a projekt csak olvasható lesz.</span><span class="sxs-lookup"><span data-stu-id="44d40-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="44d40-122">Projektállapot követése</span><span class="sxs-lookup"><span data-stu-id="44d40-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="44d40-123">Lépjen a **Project Service > Projektek** pontba.</span><span class="sxs-lookup"><span data-stu-id="44d40-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="44d40-124">Kattintson arra a projektre, amellyel dolgozni szeretne.</span><span class="sxs-lookup"><span data-stu-id="44d40-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="44d40-125">A képernyő felső részén található sávon válassza ki a projekt neve melletti lefelé mutató nyilat, majd kattintson a **Projektkövetés** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="44d40-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="44d40-126">Válassza a **Ráfordításkövetés** vagy a **Költségkövetés** lehetőséget a legördülő listában a feladatlista felett.</span><span class="sxs-lookup"><span data-stu-id="44d40-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="44d40-127">Kattintson duplán a szerkeszteni kívánt feladatra.</span><span class="sxs-lookup"><span data-stu-id="44d40-127">Double-click any task to edit it.</span></span> <span data-ttu-id="44d40-128">Áthelyezheti vagy átméretezheti az Gantt-diagram oszlopait, ha módosítani akarja egy feladat idejét és előrehaladását.</span><span class="sxs-lookup"><span data-stu-id="44d40-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="44d40-129">Kapcsolódó információk</span><span class="sxs-lookup"><span data-stu-id="44d40-129">See Also</span></span>  
 [<span data-ttu-id="44d40-130">Projektmenedzseri útmutató</span><span class="sxs-lookup"><span data-stu-id="44d40-130">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
