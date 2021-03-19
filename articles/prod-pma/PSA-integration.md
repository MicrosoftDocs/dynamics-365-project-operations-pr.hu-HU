---
title: Project Service Automation áttekintése
description: Ez a témakör a Dynamics 365 Project Service Automation és Dynamics 365 Finance közötti integrációs megoldásra vonatkozó információkat tartalmaz.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41d2eace497f4291022da0775cca7cda7d600df7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271086"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="8ac94-103">Project Service Automation áttekintése</span><span class="sxs-lookup"><span data-stu-id="8ac94-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8ac94-104">A Project Service Automation és Finance közötti integrációs megoldás az adatintegrációs funkció segítségével szinkronizálja az adatokat a Dynamics 365 Finance és a Dynamics 365 Project Service Automation között a Common Data Service szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="8ac94-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="8ac94-105">Az adatintegrációs szolgáltatással elérhető integrációs sablonok lehetővé teszik a projektek, projektszerződések, projektszerződéssorok, projektszerződéssor mérföldkövei, projektfeladatok, költségtranzakciós kategóriák, órabecslések és költségbecslések áramlását a Project Service Automation és a Finance között.</span><span class="sxs-lookup"><span data-stu-id="8ac94-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="8ac94-106">Ha 7.3.0 verziót használ, akkor a KB 4074835 telepítésére van szükség.</span><span class="sxs-lookup"><span data-stu-id="8ac94-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="8ac94-107">Ekkor lehetőség van a rögzített árú projektek integrálására.</span><span class="sxs-lookup"><span data-stu-id="8ac94-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="8ac94-108">Ha 7.3.0 verziót használ, és a Project Service Automation alkalmazásból hozza át a díjtranzakciókat, akkor a díjaknak a projekt számláján való feltümntetéséhez szükség van a KB 4345320 telepítésére.</span><span class="sxs-lookup"><span data-stu-id="8ac94-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="8ac94-109">Ha a 8.0 verziót használja, akkor a projektfeladatok integrációja, a kiadási tranzakciók kategóriái, az órabecslések, a kiadásbecslések és a funkciók zárolása is hasaználható.</span><span class="sxs-lookup"><span data-stu-id="8ac94-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="8ac94-110">Ha a 8.0.1 vagy újabb verziót használja, szinkronizálhatja a tényleges értékeket.</span><span class="sxs-lookup"><span data-stu-id="8ac94-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="8ac94-111">Mielőtt integrálhatná a Project Service Automation alkalmazást a Finance rendszerrel, konfigurálnia kell a Project Service Automation integrációs paramétereit.</span><span class="sxs-lookup"><span data-stu-id="8ac94-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="8ac94-112">További információk: [Project Service Automation integrációs paraméterei](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8ac94-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="8ac94-113">Ez az integrációs megoldás a következő helyzetekben teszi lehetővé a közvetlen szinkronizálást:</span><span class="sxs-lookup"><span data-stu-id="8ac94-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="8ac94-114">A projektszerződések karbantartása a Project Service Automation alkalmazásban, majd közvetlenül a Project Service Automation és a Finance közötti szinkronizálása.</span><span class="sxs-lookup"><span data-stu-id="8ac94-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8ac94-115">Projektek létrehozása a Project Service Automation alkalmazásban, majd közvetlenül a Project Service Automation és a Finance közötti szinkronizálása.</span><span class="sxs-lookup"><span data-stu-id="8ac94-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8ac94-116">A projektszerződéssorok karbantartása a Project Service Automation alkalmazásban, majd közvetlenül a Project Service Automation és a Finance közötti szinkronizálása.</span><span class="sxs-lookup"><span data-stu-id="8ac94-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8ac94-117">A projektszerződéssorok mérföldköveinek karbantartása a Project Service Automation alkalmazásban, majd közvetlenül a Project Service Automation és a Finance közötti szinkronizálása.</span><span class="sxs-lookup"><span data-stu-id="8ac94-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8ac94-118">A projektfeladatok karbantartása a Project Service Automation alkalmazásban, majd közvetlenül a Project Service Automation és a Finance közötti szinkronizálása.</span><span class="sxs-lookup"><span data-stu-id="8ac94-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8ac94-119">A költségtranzakciós kategóriák karbantartása a Finance rendszerben, majd közvetlenül a Finance és a Project Service Automation közötti szinkronizálása.</span><span class="sxs-lookup"><span data-stu-id="8ac94-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="8ac94-120">Projektek órabecsléseinek létrehozása a Project Service Automation alkalmazásban, majd közvetlenül a Project Service Automation és a Finance közötti szinkronizálása.</span><span class="sxs-lookup"><span data-stu-id="8ac94-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8ac94-121">Projektek költségbecsléseinek létrehozása a Project Service Automation alkalmazásban, majd közvetlenül a Project Service Automation és a Finance közötti szinkronizálása.</span><span class="sxs-lookup"><span data-stu-id="8ac94-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8ac94-122">Projekt tényleges idő-, költség- és díjértékeinek létrehozása a Project Service Automation, és projekttranzakciók létrehozása a Project Service Automation integrációs naplóban, hogy azok feladhatók legyenek a Finance rendszerbe.</span><span class="sxs-lookup"><span data-stu-id="8ac94-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="8ac94-123">Adatszinkronizálás</span><span class="sxs-lookup"><span data-stu-id="8ac94-123">Data synchronization</span></span>

<span data-ttu-id="8ac94-124">A következő ábra azt mutatja be, hogyan történik az adatok szinkronizálása az integráció részeként a Project Service Automation és a Finance rendszer között.</span><span class="sxs-lookup"><span data-stu-id="8ac94-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="8ac94-125">Jelenleg nem minden sablon érhető el.</span><span class="sxs-lookup"><span data-stu-id="8ac94-125">Not all templates are currently available.</span></span> <span data-ttu-id="8ac94-126">A sablonok megjelennek, amikor elkészültek.</span><span class="sxs-lookup"><span data-stu-id="8ac94-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="8ac94-127">[![Project Service Automation és a Finance közötti integráció](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="8ac94-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="8ac94-128">A Finance rendszerkövetelményei</span><span class="sxs-lookup"><span data-stu-id="8ac94-128">System requirements for Finance</span></span>

<span data-ttu-id="8ac94-129">A Project Service Automation és a Finance közötti integráció használatához telepítenie kell a Enterprise Edition 7.3 programot a 12-es vagy újabb platformfrissítéssel.</span><span class="sxs-lookup"><span data-stu-id="8ac94-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="8ac94-130">Project Service Automation rendszerkövetelményei</span><span class="sxs-lookup"><span data-stu-id="8ac94-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="8ac94-131">A Project Service Automation és a Finance közötti integrációs megoldás használatához a következő összetevőket kell telepíteni:</span><span class="sxs-lookup"><span data-stu-id="8ac94-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="8ac94-132">Dynamics 365 Project Service Automation 9.0.0.0-es vagy újabb verzió</span><span class="sxs-lookup"><span data-stu-id="8ac94-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="8ac94-133">Érdeklődőből készpénz megoldás a Dynamics 365 Sales 1.14.0.0 (V14) vagy újabb verziójához</span><span class="sxs-lookup"><span data-stu-id="8ac94-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="8ac94-134">A Project Service Automation és Finance közötti megoldás a Dynamics 365 Project Service Automation 1.0.0.0 vagy újabb verziójához</span><span class="sxs-lookup"><span data-stu-id="8ac94-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="8ac94-135">Telepítse a Project Service Automation és Finance integrációs megoldását a Project Service Automation-példányba</span><span class="sxs-lookup"><span data-stu-id="8ac94-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="8ac94-136">Töltse le a Project Service Automation és Finance közötti integrációs megoldást a [Microsoft letöltőközpontból](https://www.microsoft.com/download/details.aspx?id=57016), és kövesse a megoldásban szereplő útmutatást.</span><span class="sxs-lookup"><span data-stu-id="8ac94-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]