---
title: Újdonságok vagy változások a Project Service Automation 32-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 32-os frissítési kiadásában.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129669"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="a07ef-103">Újdonságok vagy változások a Project Service Automation 32-es frissítési kiadásának V3 változatában</span><span class="sxs-lookup"><span data-stu-id="a07ef-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a07ef-104">Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését.</span><span class="sxs-lookup"><span data-stu-id="a07ef-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="a07ef-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="a07ef-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a07ef-106">Kompatibilis a Dynamics 365 9.x rendszerrel.</span><span class="sxs-lookup"><span data-stu-id="a07ef-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a07ef-107">A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést.</span><span class="sxs-lookup"><span data-stu-id="a07ef-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="a07ef-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a07ef-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a07ef-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 32-es frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="a07ef-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="a07ef-110">A verzió build száma V3.10.53.108, és általánosan elérhető lesz önálló frissítésként 2021 júniusában.</span><span class="sxs-lookup"><span data-stu-id="a07ef-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="a07ef-111">32-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="a07ef-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a07ef-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="a07ef-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="a07ef-113">Általános</span><span class="sxs-lookup"><span data-stu-id="a07ef-113">General</span></span>

- <span data-ttu-id="a07ef-114">Ha egy nagyobb frissítés sikertelen, csak az alkalmazás fő belépési pontjait kell zárolni annak érdekében, hogy a megosztott entitások továbbra is elérhetők legyenek.</span><span class="sxs-lookup"><span data-stu-id="a07ef-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="a07ef-115">Idő és költség</span><span class="sxs-lookup"><span data-stu-id="a07ef-115">Time and Expense</span></span>

<span data-ttu-id="a07ef-116">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="a07ef-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="a07ef-117">A **TimeEntalbumImportResourceAsignment** nem tartja karban az erőforrás-hozzárendelési szelet kezdő és a záró időpontját.</span><span class="sxs-lookup"><span data-stu-id="a07ef-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="a07ef-118">Ha kiválasztja a **Bejegyzés megnyitása** az **Időbejegyzés** lehetőséget az Időbevitel rácson, előfordulhat, hogy más űrlapokat nem lehet kijelölni.</span><span class="sxs-lookup"><span data-stu-id="a07ef-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="a07ef-119">Amikor időbejegyzések hozzárendelését importálja, az ügyfélkód lekérdezése hosszú URL-címet generálhat, amely meghiúsul a lekérdezésben.</span><span class="sxs-lookup"><span data-stu-id="a07ef-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="a07ef-120">Az **Időbevitel** rácsban, miután egy értéket törölnek a cellából, a fókusz nem marad a rácsban.</span><span class="sxs-lookup"><span data-stu-id="a07ef-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="a07ef-121">Az **Elutasítás** gomb el lett távolítva a modern jóváhagyások **Jóváhagyások feldolgozása** nézetéből.</span><span class="sxs-lookup"><span data-stu-id="a07ef-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="a07ef-122">Az időbevitel tömeges jóváhagyásának stabilitását és teljesítményét befolyásolják a holtpontok és az, hogy nem elehet megefelelően kezelni a testreszabásokat, amelyek az **Időbevitel** bejegyzéshez kapcsolódnak.</span><span class="sxs-lookup"><span data-stu-id="a07ef-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="a07ef-123">Projekttervezés</span><span class="sxs-lookup"><span data-stu-id="a07ef-123">Project Planning</span></span>

- <span data-ttu-id="a07ef-124">Null referencia kivétel jön létre olyan projekt frissítésekkor, amelyek értéke null értéket tartalmaz a **Szerződésszerződéses egység** mezőben.</span><span class="sxs-lookup"><span data-stu-id="a07ef-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="a07ef-125">A **Projekt végösszegeinek frissítése** nem megfelelően számítja ki a fennmaradó költséget és a projekt hátralévő értékesítését.</span><span class="sxs-lookup"><span data-stu-id="a07ef-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="a07ef-126">A redundáns árképzési számítások hatással vannak az erőforrás-hozzárendelések frissítéséhez kapcsolódó teljesítményre.</span><span class="sxs-lookup"><span data-stu-id="a07ef-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="a07ef-127">Erőforráskezelés</span><span class="sxs-lookup"><span data-stu-id="a07ef-127">Resource Management</span></span>

<span data-ttu-id="a07ef-128">A következő probléma ki lett javítva:</span><span class="sxs-lookup"><span data-stu-id="a07ef-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="a07ef-129">Ha egy lefoglalható erőforrás naptárkapacitása 1-nél több, a Project Service Automation helytelenül 0 (nulla) értékként ismeri fel a kapacitást.</span><span class="sxs-lookup"><span data-stu-id="a07ef-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="a07ef-130">Éppen ezért végtelen ciklus fordul elő az ütemezési nézetben.</span><span class="sxs-lookup"><span data-stu-id="a07ef-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="a07ef-131">Értékesítés</span><span class="sxs-lookup"><span data-stu-id="a07ef-131">Sales</span></span>

<span data-ttu-id="a07ef-132">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="a07ef-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="a07ef-133">Egyéni tranzakciótípusú naplósor létrehozásakor a következő null hivatkozási kivétel jön létre: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="a07ef-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="a07ef-134">Az olyan szerepkörök és kategóriák, amelyek inaktiválva vannak az árajánlat másolása előtt, ne adja hozzá a számlázható szerepkörökhöz és kategóriákhoz az újonnan másolt árajánlatban.</span><span class="sxs-lookup"><span data-stu-id="a07ef-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="a07ef-135">A dokumentum dátuma és a könyvelési dátum nem igazodik a számlasor olyan részleteihez tartozó kezdő dátumhoz, amely közvetlenül a számlatervezeten jön létre.</span><span class="sxs-lookup"><span data-stu-id="a07ef-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="a07ef-136">A null hivatkozási kivételek olyan helyzetekben jönnek létre, amelyek a szerepkörök és kategóriák inaktiválásával kapcsolatosak az árajánlat másolása előtt.</span><span class="sxs-lookup"><span data-stu-id="a07ef-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="a07ef-137">A **Projektek** lapon az **Árak frissítése** művelet nem frissíti a költségbecsléseket és az anyagbecsléseket.</span><span class="sxs-lookup"><span data-stu-id="a07ef-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
