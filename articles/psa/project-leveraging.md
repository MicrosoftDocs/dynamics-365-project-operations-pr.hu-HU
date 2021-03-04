---
title: Értékesítési becslések és projektek
description: Ez a témakör információkat nyújt arról, hogyan lehet kihasználni az ütemezést és a becsléseket az értékesítési folyamatban.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 76e21f80e51e6f3092880dc629ba90b400805486
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148376"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="dd4b5-103">Értékesítési becslések és projektek</span><span class="sxs-lookup"><span data-stu-id="dd4b5-103">Sales estimates and projects</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="dd4b5-104">Az értékesítési folyamat során értékesítési becsléseket készíthet úgy, hogy egy projektet az értékesítési árajánlathoz kapcsol.</span><span class="sxs-lookup"><span data-stu-id="dd4b5-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="dd4b5-105">Ilyen módon determinisztikus becslés történhet az értékesítési folyamat során, a projekt ütemezésének és becslési lehetőségeinek kihasználása érdekében.</span><span class="sxs-lookup"><span data-stu-id="dd4b5-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="dd4b5-106">Ha az eladás végbe megy, akkor az eladási becslés céljából használt ütemezés szolgálhat a projektterv további finomításának alapjául.</span><span class="sxs-lookup"><span data-stu-id="dd4b5-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="dd4b5-107">Projekt összekapcsolása árajánlatsorral</span><span class="sxs-lookup"><span data-stu-id="dd4b5-107">Linking a project to a quote line</span></span>

<span data-ttu-id="dd4b5-108">Projekt alapú árajánlatsor létrehozásakor létrehozhat egy új projektet, vagy társíthat egy meglévő projektet az **Árajánlatsor** oldalon.</span><span class="sxs-lookup"><span data-stu-id="dd4b5-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Árajánlat űrlapja](media/project-8.png)
 
<span data-ttu-id="dd4b5-110">Amikor új projektet hoz létre az árajánlatsor részleteiből, felhasználhatja a projektsablonokat.</span><span class="sxs-lookup"><span data-stu-id="dd4b5-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="dd4b5-111">A projektsablonok olyan modellprojektek, amelyek a szervezetre jellemző szabványos projektterveket és pénzügyi becsléseket jelentenek.</span><span class="sxs-lookup"><span data-stu-id="dd4b5-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="dd4b5-112">Jelenthetik a projekttervek másolatait és a korábbi projektek becsléseit is.</span><span class="sxs-lookup"><span data-stu-id="dd4b5-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Árajánlatsor részletei](media/project-9.png)
  
<span data-ttu-id="dd4b5-114">Amikor létrehozza a projektet az árajánlatból, a projekt automatikusan társítva lesz az árajánlatsorhoz.</span><span class="sxs-lookup"><span data-stu-id="dd4b5-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="dd4b5-115">A becslések összetevői egy projektben</span><span class="sxs-lookup"><span data-stu-id="dd4b5-115">Components of estimates in a project</span></span>

<span data-ttu-id="dd4b5-116">Az ütemezés lehetővé teszi a munka felosztását feladatokra, a feladatok hierarchiájának fenntartását, a feladat elvégzéséhez szükséges erőforrások meghatározását és a feladat elvégzéséhez szükséges erőfeszítés megbecslését.</span><span class="sxs-lookup"><span data-stu-id="dd4b5-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="dd4b5-117">Az erőfeszítés és az ütemezés becslései a **Projekt** oldal **Ütemezés** fülén található mezők segítségével definiálhatók.</span><span class="sxs-lookup"><span data-stu-id="dd4b5-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="dd4b5-118">Mivel a projekthez árlisták vannak társítva, a pénzügyi becsléseket az árlistában meghatározott költség- és eladási árak alapján számítják ki.</span><span class="sxs-lookup"><span data-stu-id="dd4b5-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="dd4b5-119">Becslések importálása projektből árajánlatba</span><span class="sxs-lookup"><span data-stu-id="dd4b5-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="dd4b5-120">A projektbecslések meghatározása után importálhatja azokat az árajánlatsorba.</span><span class="sxs-lookup"><span data-stu-id="dd4b5-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="dd4b5-121">Az **Árajánlatsor részletei** lapon válassza a szalag **Importálás becslésekből** lehetőségét a projektbecslések összefoglalásához tranzakciós típus, szerepkör vagy feladatszint alapján.</span><span class="sxs-lookup"><span data-stu-id="dd4b5-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
