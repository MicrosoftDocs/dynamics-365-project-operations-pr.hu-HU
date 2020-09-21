---
title: Újdonságok a Project Service Automation 15-ös frissítési kiadásának V3 változatában
description: Ez a témakör információkat nyújt arról, hogy milyen újdonságok és változások vannak a Project Service Automation 15-ös frissítési kiadásának V3 verziójában.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752223"
---
# <a name="project-service-automation-v3-update-release-15"></a><span data-ttu-id="caa25-103">Project Service Automation V3, 15-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="caa25-103">Project Service Automation V3, Update Release 15</span></span>

<span data-ttu-id="caa25-104">Örömmel jelentjük be a Dynamics 365 Project Service Automation (PSA) alkalmazás legújabb frissítését.</span><span class="sxs-lookup"><span data-stu-id="caa25-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="caa25-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="caa25-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="caa25-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="caa25-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="caa25-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez nyissa meg a megoldások oldalt.</span><span class="sxs-lookup"><span data-stu-id="caa25-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="caa25-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="caa25-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="caa25-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a PSA V3. 15-ös frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="caa25-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="caa25-110">Ennek a verziónak a build száma V 3.10.5.28, és általánosan elérhető egy önálló frissítésben 2020 januárjában.</span><span class="sxs-lookup"><span data-stu-id="caa25-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="caa25-111">15-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="caa25-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="caa25-112">Fejlesztések</span><span class="sxs-lookup"><span data-stu-id="caa25-112">Enhancements</span></span>

- <span data-ttu-id="caa25-113">Projektmenedzsment</span><span class="sxs-lookup"><span data-stu-id="caa25-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="caa25-114">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="caa25-114">Bug fixes</span></span>

- <span data-ttu-id="caa25-115">Idő és költség</span><span class="sxs-lookup"><span data-stu-id="caa25-115">Time and Expense</span></span>

  - <span data-ttu-id="caa25-116">Javítva: Bővítmény betöltési hibája az egyeztetési nézetben.</span><span class="sxs-lookup"><span data-stu-id="caa25-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="caa25-117">Javítva: Projekterőforrás-központ: **Mennyiség** átnevezése a többértelműség elkerüléséhez.</span><span class="sxs-lookup"><span data-stu-id="caa25-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="caa25-118">Javítva: Az **Időbejegyzés másolásához használt oszlopok** módosítása,hogy a típust is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="caa25-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="caa25-119">Javítva: Szerkesztés ideje bejegyzés megadása a rácsnézetben decimális számokkal bizonyos számoknál ismeretlen hibát ad.</span><span class="sxs-lookup"><span data-stu-id="caa25-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="caa25-120">Projektmenedzsment</span><span class="sxs-lookup"><span data-stu-id="caa25-120">Project Management</span></span>

  - <span data-ttu-id="caa25-121">Javítva: A **Használata követési nézetben** legördülő menü kibővül a lehetőségek szélességének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="caa25-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="caa25-122">Javítva: A +13-as időzónában a projektek kezelésekor a feladatszámítások pontatlan eredményeket jeleníthettek meg.</span><span class="sxs-lookup"><span data-stu-id="caa25-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="caa25-123">Javítva: **Csoporttag befejezési idő** javítva lett 24-órás naptár használata esetén.</span><span class="sxs-lookup"><span data-stu-id="caa25-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="caa25-124">Javítva: A **BPF** ismét aktiválva az **msdyn_project** fő űrlapon.</span><span class="sxs-lookup"><span data-stu-id="caa25-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="caa25-125">Javítva: A hozzárendelések kiszámítása immár nem hagy figyelmen kívül egy napot.</span><span class="sxs-lookup"><span data-stu-id="caa25-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="caa25-126">Javítva: Egy új értesítési sáv lett hozzáadva a projektűrlaphoz, amikor az időzóna eltér a felhasználó és a projekt között.</span><span class="sxs-lookup"><span data-stu-id="caa25-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="caa25-127">Sales</span><span class="sxs-lookup"><span data-stu-id="caa25-127">Sales</span></span>

  - <span data-ttu-id="caa25-128">Javítva: A költségbecslés kategória keresése használható az ismétlődések szűrésére.</span><span class="sxs-lookup"><span data-stu-id="caa25-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="caa25-129">Javítva: A **PluginDomain.ExecuteInTryCatchBlock(..)** kódja a továbbiakban nem rejti el a kivételek eredetét.</span><span class="sxs-lookup"><span data-stu-id="caa25-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="caa25-130">Javítva: A továbbiakban nem kap hibaüzenetet a **Projektkeresőben** az **Ajánlati sor** űrlapon, ha több mint 1000 projekt van.</span><span class="sxs-lookup"><span data-stu-id="caa25-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="caa25-131">Javítva: A **Becslések** rács a munka becsléséhez és a költségbecsléséhez immár a helyes pénznemszimbólummal jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="caa25-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="caa25-132">Javítva: Miután egy szervezet frissítette a PSA-t 14. frissítési kiadásról a 15. frissítési kiadásra, az **Ütemezés** lap már nem üresen jelenik meg a **Projekt** űrlapon.</span><span class="sxs-lookup"><span data-stu-id="caa25-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>
