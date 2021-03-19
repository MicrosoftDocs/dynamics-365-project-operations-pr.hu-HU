---
title: Újdonságok vagy változások a Project Service Automation 15-es frissítési kiadásának V3 változatában
description: Ez a témakör információkat nyújt arról, hogy milyen újdonságok és változások vannak a Project Service Automation 15-ös frissítési kiadásának V3 verziójában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 189b99c6a4bf18b6063c7b6020dbf1ac372b41e9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280941"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="e2e78-103">Project Service Automation 15-ös frissítési kiadás, V3</span><span class="sxs-lookup"><span data-stu-id="e2e78-103">Project Service Automation Update Release 15, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e2e78-104">Örömmel jelentjük be a Dynamics 365 Project Service Automation (PSA) alkalmazás legújabb frissítését.</span><span class="sxs-lookup"><span data-stu-id="e2e78-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="e2e78-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e2e78-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e2e78-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="e2e78-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e2e78-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez nyissa meg a megoldások oldalt.</span><span class="sxs-lookup"><span data-stu-id="e2e78-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="e2e78-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e2e78-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e2e78-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a PSA V3. 15-ös frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="e2e78-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="e2e78-110">Ennek a verziónak a build száma V 3.10.5.28, és általánosan elérhető egy önálló frissítésben 2020 januárjában.</span><span class="sxs-lookup"><span data-stu-id="e2e78-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="e2e78-111">15-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="e2e78-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="e2e78-112">Fejlesztések</span><span class="sxs-lookup"><span data-stu-id="e2e78-112">Enhancements</span></span>

- <span data-ttu-id="e2e78-113">Projektmenedzsment</span><span class="sxs-lookup"><span data-stu-id="e2e78-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e2e78-114">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="e2e78-114">Bug fixes</span></span>

- <span data-ttu-id="e2e78-115">Idő és költség</span><span class="sxs-lookup"><span data-stu-id="e2e78-115">Time and Expense</span></span>

  - <span data-ttu-id="e2e78-116">Javítva: Bővítmény betöltési hibája az egyeztetési nézetben.</span><span class="sxs-lookup"><span data-stu-id="e2e78-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="e2e78-117">Javítva: Projekterőforrás-központ: **Mennyiség** átnevezése a többértelműség elkerüléséhez.</span><span class="sxs-lookup"><span data-stu-id="e2e78-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="e2e78-118">Javítva: Az **Időbejegyzés másolásához használt oszlopok** módosítása,hogy a típust is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e2e78-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="e2e78-119">Javítva: Szerkesztés ideje bejegyzés megadása a rácsnézetben decimális számokkal bizonyos számoknál ismeretlen hibát ad.</span><span class="sxs-lookup"><span data-stu-id="e2e78-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="e2e78-120">Projektmenedzsment</span><span class="sxs-lookup"><span data-stu-id="e2e78-120">Project Management</span></span>

  - <span data-ttu-id="e2e78-121">Javítva: A **Használata követési nézetben** legördülő menü kibővül a lehetőségek szélességének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="e2e78-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="e2e78-122">Javítva: A +13-as időzónában a projektek kezelésekor a feladatszámítások pontatlan eredményeket jeleníthettek meg.</span><span class="sxs-lookup"><span data-stu-id="e2e78-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="e2e78-123">Javítva: **Csoporttag befejezési idő** javítva lett 24-órás naptár használata esetén.</span><span class="sxs-lookup"><span data-stu-id="e2e78-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="e2e78-124">Javítva: A **BPF** ismét aktiválva az **msdyn_project** fő űrlapon.</span><span class="sxs-lookup"><span data-stu-id="e2e78-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="e2e78-125">Javítva: A hozzárendelések kiszámítása immár nem hagy figyelmen kívül egy napot.</span><span class="sxs-lookup"><span data-stu-id="e2e78-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="e2e78-126">Javítva: Egy új értesítési sáv lett hozzáadva a projektűrlaphoz, amikor az időzóna eltér a felhasználó és a projekt között.</span><span class="sxs-lookup"><span data-stu-id="e2e78-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="e2e78-127">Sales</span><span class="sxs-lookup"><span data-stu-id="e2e78-127">Sales</span></span>

  - <span data-ttu-id="e2e78-128">Javítva: A költségbecslés kategória keresése használható az ismétlődések szűrésére.</span><span class="sxs-lookup"><span data-stu-id="e2e78-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="e2e78-129">Javítva: A **PluginDomain.ExecuteInTryCatchBlock(..)** kódja a továbbiakban nem rejti el a kivételek eredetét.</span><span class="sxs-lookup"><span data-stu-id="e2e78-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="e2e78-130">Javítva: A továbbiakban nem kap hibaüzenetet a **Projektkeresőben** az **Ajánlati sor** űrlapon, ha több mint 1000 projekt van.</span><span class="sxs-lookup"><span data-stu-id="e2e78-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="e2e78-131">Javítva: A **Becslések** rács a munka becsléséhez és a költségbecsléséhez immár a helyes pénznemszimbólummal jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="e2e78-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="e2e78-132">Javítva: Miután egy szervezet frissítette a PSA-t 14. frissítési kiadásról a 15. frissítési kiadásra, az **Ütemezés** lap már nem üresen jelenik meg a **Projekt** űrlapon.</span><span class="sxs-lookup"><span data-stu-id="e2e78-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]