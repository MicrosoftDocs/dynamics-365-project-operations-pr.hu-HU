---
title: A projektfeladatok szinkronizálása közvetlenül a Project Service Automation alkalmazásból a Finance and Operations rendszerbe
description: Ez a témakör ismerteti azt a sablont és azt az alapul szolgáló feladatot, amelyek a projektfeladatok közvetlenül a Microsoft Dynamics 365 Project Service Automation alkalmazásból a Dynamics 365 Finance rendszerbe történő szinkronizálására szolgálnak.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7cc9ee9de576549c132e14c333a1000c22a55236
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288922"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="b8379-103">A projektfeladatok szinkronizálása közvetlenül a Project Service Automation alkalmazásból a Finance and Operations rendszerbe</span><span class="sxs-lookup"><span data-stu-id="b8379-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b8379-104">Ez a témakör ismerteti azt a sablont és azt az alapul szolgáló feladatot, amelyek a projektfeladatok közvetlenül a Dynamics 365 Project Service Automation alkalmazásból a Dynamics 365 Finance rendszerbe történő szinkronizálására szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="b8379-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="b8379-105">A projektfeladatok integrációja, a kiadási tranzakciók kategóriái, az órabecslések, a kiadásbecslések és a funkciók zárolása a 8.0 verzióban érhető el.</span><span class="sxs-lookup"><span data-stu-id="b8379-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="b8379-106">Ha az Enterprise Edition 7.3.0 verzióját használja, a KB 4132657 és a KB 4132660 telepítése után használhatja a sablonokat a projektfeladatok, a költségtranzakció-kategóriák, az órabecslések, a kiadásbecslések és a tényadatok integrálására, valamint a funkciók zárolásának konfigurálására.</span><span class="sxs-lookup"><span data-stu-id="b8379-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="b8379-107">Ha vissza kell állítania a könyvelési feloszlásokat, ajánlott a KB 4131710 telepítése is.</span><span class="sxs-lookup"><span data-stu-id="b8379-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="b8379-108">A tényadatok integrációja a 8.0.1 vagy újabb verziókban érhető el.</span><span class="sxs-lookup"><span data-stu-id="b8379-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="b8379-109">Adatfolyam a Project Service Automation és a Finance között</span><span class="sxs-lookup"><span data-stu-id="b8379-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="b8379-110">A Project Service Automation és Finance közötti integrációs megoldás az adatintegrációs funkció segítségével szinkronizálja az adatokat a Project Service Automation és a Finance példányai között.</span><span class="sxs-lookup"><span data-stu-id="b8379-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="b8379-111">Az adatintegrációs szolgáltatással elérhető integrációs sablon lehetővé teszi a projektfeladatok áramlását a Project Service Automation és a Finance között.</span><span class="sxs-lookup"><span data-stu-id="b8379-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="b8379-112">A következő ábra azt mutatja be, hogyan történik az adatok szinkronizálása a Project Service Automation és a Finance rendszer között.</span><span class="sxs-lookup"><span data-stu-id="b8379-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="b8379-113">[![Adatfolyam a Project Service Automation és a Finance közötti integrációhoz](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="b8379-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="b8379-114">Sablon és feladat</span><span class="sxs-lookup"><span data-stu-id="b8379-114">Template and task</span></span>

<span data-ttu-id="b8379-115">A sablon eléréséhez a Microsoft Power Apps felügyeleti központban válassza a **Projektek** lehetőséget, majd a jobb felső sarokban válassza az **Új projekt** lehetőséget a nyilvános sablonok kiválasztásához.</span><span class="sxs-lookup"><span data-stu-id="b8379-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b8379-116">A következő sablon és a mögöttes feladat segítségével szinkronizálhatja a projektfeladatokat a Project Service Automation alkalmazásból a Finance rendszerbe:</span><span class="sxs-lookup"><span data-stu-id="b8379-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="b8379-117">**A sablon neve az adatintegrációban:** Projektfeladatok (PSA – Fin és Ops)</span><span class="sxs-lookup"><span data-stu-id="b8379-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="b8379-118">**A feladat neve a projektben:** Projektfeladatok</span><span class="sxs-lookup"><span data-stu-id="b8379-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="b8379-119">A projektfeladatok szinkronizálása előtt szinkronizálnia kell a projektszerződéseket és projekteket.</span><span class="sxs-lookup"><span data-stu-id="b8379-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="b8379-120">Entitáskészlet</span><span class="sxs-lookup"><span data-stu-id="b8379-120">Entity set</span></span>

| <span data-ttu-id="b8379-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b8379-121">Project Service Automation</span></span> | <span data-ttu-id="b8379-122">Pénzügy</span><span class="sxs-lookup"><span data-stu-id="b8379-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="b8379-123">Projektfeladatok</span><span class="sxs-lookup"><span data-stu-id="b8379-123">Project Tasks</span></span>              | <span data-ttu-id="b8379-124">A projektfeladat integrációs entitása</span><span class="sxs-lookup"><span data-stu-id="b8379-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="b8379-125">Entitásfolyam</span><span class="sxs-lookup"><span data-stu-id="b8379-125">Entity flow</span></span>

<span data-ttu-id="b8379-126">A projektfeladatok a Project Service Automation alkalmazásban kezelhetők, és a program projekttevékenységekként szinkronizálja őket a Finance rendszerbe.</span><span class="sxs-lookup"><span data-stu-id="b8379-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="b8379-127">Előfeltételek és leképezési beállítások</span><span class="sxs-lookup"><span data-stu-id="b8379-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="b8379-128">A projektfeladatok szinkronizálása előtt szinkronizálnia kell a projektszerződéseket és projekteket.</span><span class="sxs-lookup"><span data-stu-id="b8379-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="b8379-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="b8379-129">Power Query</span></span>

<span data-ttu-id="b8379-130">Ha a következő feltétel teljesül, az Excelhez készült Microsoft Power Query alkalmazást kell használnia az adatok szűréséhez:</span><span class="sxs-lookup"><span data-stu-id="b8379-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="b8379-131">A projektfeladatban erőforrás-specifikus rekordok vannak.</span><span class="sxs-lookup"><span data-stu-id="b8379-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="b8379-132">Ha Power Query alkalmazást kell használnia, kövesse az alábbi irányelvet:</span><span class="sxs-lookup"><span data-stu-id="b8379-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="b8379-133">A Projektfeladatok (PSA – Fin és Ops) sablonja egy alapértelmezett szűrővel rendelkezik, amely kizárja a projektfeladat erőforrás-specifikus bejegyzéseit az **IsLineTask** szűrőjét **Hemis** értékre állítva.</span><span class="sxs-lookup"><span data-stu-id="b8379-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="b8379-134">Ha saját sablont hoz létre, akkor ezt a szűrőt kell hozzáadnia.</span><span class="sxs-lookup"><span data-stu-id="b8379-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b8379-135">Sablonok leképezése az adatintegrációban</span><span class="sxs-lookup"><span data-stu-id="b8379-135">Template mapping in Data integration</span></span>

<span data-ttu-id="b8379-136">A következő ábra egy példát mutat be az adatintegrációban az sablonfeladatok leképezésére.</span><span class="sxs-lookup"><span data-stu-id="b8379-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="b8379-137">A leképezés azokat a mezőinformációkat mutatja, amelyek a Project Service Automation alkalmazásból a Finance rendszerbe lesznek szinkronizálva.</span><span class="sxs-lookup"><span data-stu-id="b8379-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="b8379-138">[![Sablonok leképezése](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="b8379-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]