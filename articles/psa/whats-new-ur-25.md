---
title: Újdonságok vagy változások a Project Service Automation 25-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 25-os frissítési kiadásában.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 92dd74378457cf877e8ec26eb85a7883dda97d51
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000214"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="3a80f-103">Újdonságok vagy változások a Project Service Automation 25-es frissítési kiadásának V3 változatában</span><span class="sxs-lookup"><span data-stu-id="3a80f-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3a80f-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="3a80f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="3a80f-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="3a80f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3a80f-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="3a80f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3a80f-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="3a80f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="3a80f-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="3a80f-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3a80f-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy módosultak a Project Service Automation V3 verzió 25-ös frissítéskiadásnál Ez a verzió a V 3.10.43.76 buildszámmal rendelkezik, és 2020 októberében általánosan elérhető egy önkiszolgáló frissítéssel.</span><span class="sxs-lookup"><span data-stu-id="3a80f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="3a80f-110">25-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="3a80f-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3a80f-111">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="3a80f-111">Bug fixes</span></span>

<span data-ttu-id="3a80f-112">**Idő és költség**</span><span class="sxs-lookup"><span data-stu-id="3a80f-112">**Time and Expense**</span></span>

<span data-ttu-id="3a80f-113">A következő probléma ki lett javítva:</span><span class="sxs-lookup"><span data-stu-id="3a80f-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="3a80f-114">Időbejegyzés-diagram további adatokat mutatott a túl nagy beolvasott intervallum esetén.</span><span class="sxs-lookup"><span data-stu-id="3a80f-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="3a80f-115">**Erőforráskezelés**</span><span class="sxs-lookup"><span data-stu-id="3a80f-115">**Resource Management**</span></span>

<span data-ttu-id="3a80f-116">A következő probléma ki lett javítva:</span><span class="sxs-lookup"><span data-stu-id="3a80f-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="3a80f-117">Hozzáadtunk egy további Package Deployer-kódot, amellyel a Universal Resource Scheduling javítás kihagyható, ha létezik magasabb verziójú javítás.</span><span class="sxs-lookup"><span data-stu-id="3a80f-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="3a80f-118">**Projektmenedzsment**</span><span class="sxs-lookup"><span data-stu-id="3a80f-118">**Project Management**</span></span>

<span data-ttu-id="3a80f-119">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="3a80f-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="3a80f-120">Javítottuk a kerekítési és árfolyam-eltéréseket, amelyek helytelen tervezett költséget eredményeztek a projektkövetési rácsban.</span><span class="sxs-lookup"><span data-stu-id="3a80f-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="3a80f-121">Támogatja a **projekt** űrlapon két vagy több reagáló rács megjelenítését.</span><span class="sxs-lookup"><span data-stu-id="3a80f-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="3a80f-122">Ellenőrzést adtunk hozzá, hogy foglalkozzunk a feladat naptári záró dátum utáni hozzáadási képességével, amely sikertelen erőforrás-hozzárendeléshez vezet.</span><span class="sxs-lookup"><span data-stu-id="3a80f-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="3a80f-123">Javított hibakezelés a következőkből előállított null hivatkozás-kivétel kezelésére:</span><span class="sxs-lookup"><span data-stu-id="3a80f-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="3a80f-124">**PreValidateProjectTeamMemberCreate** beépülő modul</span><span class="sxs-lookup"><span data-stu-id="3a80f-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="3a80f-125">**PreValidateProjectTaskCreate**, ha társított projekt nélkül jön létre a Projektfeladat</span><span class="sxs-lookup"><span data-stu-id="3a80f-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="3a80f-126">**PreProjectTeamMemberCreate** beépülő modul</span><span class="sxs-lookup"><span data-stu-id="3a80f-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="3a80f-127">**PostProjectTeamMemberDelete** beépülő modul</span><span class="sxs-lookup"><span data-stu-id="3a80f-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="3a80f-128">**PreValidateProjectTaskDelete** beépülő modul</span><span class="sxs-lookup"><span data-stu-id="3a80f-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="3a80f-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="3a80f-129">**Sales**</span></span>

<span data-ttu-id="3a80f-130">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="3a80f-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="3a80f-131">Javított hibakezelés a következőből létrehozott nulla hivatkozású kivételek kezelésére: **Projekt másolása: becslések HelperResource kezelése**.</span><span class="sxs-lookup"><span data-stu-id="3a80f-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="3a80f-132">**Nem számlázásra kész** az **idő- és anyagelszámolású számlázási lemaradás** esetén nem törli a számlázási állapotot.</span><span class="sxs-lookup"><span data-stu-id="3a80f-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="3a80f-133">Javítottuk a helytelenül címkézett **Árak** gombokat a **Szerepkörárak** és **Katalóguscikkek** lapon.</span><span class="sxs-lookup"><span data-stu-id="3a80f-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]