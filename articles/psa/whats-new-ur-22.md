---
title: Újdonságok vagy változások a Project Service Automation 22-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 22-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 8863d321ad88d761d0fcbd82ca26562a69468f2f
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949007"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="174eb-103">Project Service Automation 22-es frissítési kiadás, V3</span><span class="sxs-lookup"><span data-stu-id="174eb-103">Project Service Automation Update Release 22, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="174eb-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="174eb-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="174eb-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="174eb-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="174eb-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="174eb-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="174eb-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="174eb-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="174eb-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="174eb-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="174eb-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 22-es frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="174eb-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="174eb-110">A verzió build száma V 3.10.33.48, és általánosan elérhető lesz önálló frissítésként 2020 júniusában.</span><span class="sxs-lookup"><span data-stu-id="174eb-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="174eb-111">22-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="174eb-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="174eb-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="174eb-112">Bug fixes</span></span>



<span data-ttu-id="174eb-113">**Idő és költség**</span><span class="sxs-lookup"><span data-stu-id="174eb-113">**Time and Expense**</span></span>

<span data-ttu-id="174eb-114">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="174eb-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="174eb-115">Az **Időbejegyzések** az importálás után nem lesznek automatikusan hozzáadva időbejegyzések ütemezéséhez.</span><span class="sxs-lookup"><span data-stu-id="174eb-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="174eb-116">Az **Időbeviteli** rács dátumválasztója nem ismeri fel a felhasználó területi beállításait.</span><span class="sxs-lookup"><span data-stu-id="174eb-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="174eb-117">**Erőforráskezelés**</span><span class="sxs-lookup"><span data-stu-id="174eb-117">**Resource Management**</span></span>

<span data-ttu-id="174eb-118">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="174eb-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="174eb-119">Manuális módban az **Erőforrás-hozzárendelési** körvonalak módosításait a rendszer nem ismeri fel az **Erőforráskövetelmények** létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="174eb-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="174eb-120">Az **Erőforrás-kérelmek** nem támogatják az egyéni kérelemállapokat.</span><span class="sxs-lookup"><span data-stu-id="174eb-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="174eb-121">**Projektmenedzsment**</span><span class="sxs-lookup"><span data-stu-id="174eb-121">**Project Management**</span></span>

<span data-ttu-id="174eb-122">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="174eb-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="174eb-123">Dupla kattintással az EstimateGridControl nem megfelelően elemzi a holland formátumú számokat.</span><span class="sxs-lookup"><span data-stu-id="174eb-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="174eb-124">A hozzárendelt órák nem frissülnek megfelelően, ha a hozzárendelések a Microsoft Project Desktop kliensbővítmény használatával módosulnak.</span><span class="sxs-lookup"><span data-stu-id="174eb-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="174eb-125">A Projektek nyomon követése és a Becslések rácsa helytelen értékesítési pénznemkódot jelenít meg, ha a szerződés pénzneme eltér az ügyfél pénznemtől és a szervezet úgy lett konfigurálva hogy pénznem jele helyett pénznemkódokat jelenítsen meg.</span><span class="sxs-lookup"><span data-stu-id="174eb-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="174eb-126">A csoporttagok befejezési dátuma egy napot hozzáad, ha a munkaórák ütemezése napi 24 órában történik.</span><span class="sxs-lookup"><span data-stu-id="174eb-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="174eb-127">A Projekt ütemezésekor a tevékenységhez tartozó Tranzakciós kategória hozzáadása nem indítja el az automatikus mentést.</span><span class="sxs-lookup"><span data-stu-id="174eb-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="174eb-128">A következő hibaüzenet jelenik meg, amikor egy csapattagot vesz fel a Projekt sablonba: „Az erőforrás-követelmények nem társíthatók projektsablonokkal”.</span><span class="sxs-lookup"><span data-stu-id="174eb-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="174eb-129">A menüszalag szabályának „msdyn.Approval.CanApproveOrReject” parancsfájlja időtúllépési hibát jelenít meg.</span><span class="sxs-lookup"><span data-stu-id="174eb-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="174eb-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="174eb-130">**Sales**</span></span>

<span data-ttu-id="174eb-131">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="174eb-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="174eb-132">Az érvényesítési hibaüzenet nem jelenik meg, ha egy Önköltségi árlista van kiválasztva az „Új ajánlati projektárlista” űrlapon/entitáson.</span><span class="sxs-lookup"><span data-stu-id="174eb-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="174eb-133">Ha az ajánlathoz tartozó üzleti folyamat az utolsó fázisban van, akkor a megnyertként lezárt ajánlat nem navigálja a felhasználót a létrehozott szerződésre.</span><span class="sxs-lookup"><span data-stu-id="174eb-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="174eb-134">A **Ki nem számlázott értékesítések** sztornírozása az eredeti költséghez kapcsolódik az időbejegyzés visszahívásakor.</span><span class="sxs-lookup"><span data-stu-id="174eb-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="174eb-135">A **Jóváhagyás** gomb kiválasztását követően a számla állapota nem módosul **Megerősített** értékre hacsak a számlát nem frissítik.</span><span class="sxs-lookup"><span data-stu-id="174eb-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]