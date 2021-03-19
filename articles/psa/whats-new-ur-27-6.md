---
title: Újdonságok vagy változások a Project Service Automation 27.6-es gyorsjavításának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetőek a Project Service Automation 27.6-es gyorsjavításának V3 változatában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/17/2021
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
ms.openlocfilehash: f6576c6c5660ff6e8e53286ae226c8278a33f2be
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "5481269"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-276-v3"></a><span data-ttu-id="7b476-103">Újdonságok vagy változások a Project Service Automation 27.6-es frissítési kiadásának V3 változatában</span><span class="sxs-lookup"><span data-stu-id="7b476-103">What's new or changed in Project Service Automation Update Release 27.6, V3</span></span>

<span data-ttu-id="7b476-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="7b476-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="7b476-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="7b476-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="7b476-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="7b476-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="7b476-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="7b476-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="7b476-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="7b476-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="7b476-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 27.6-es frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="7b476-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 27.6.</span></span> <span data-ttu-id="7b476-110">Ennek a verziónak a build száma V3.10.45.120, és általánosan elérhető egy önálló frissítésben 2021. januárjában.</span><span class="sxs-lookup"><span data-stu-id="7b476-110">This version has a build number of V3.10.45.120 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-276"></a><span data-ttu-id="7b476-111">27.6-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="7b476-111">Update Release 27.6</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="7b476-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="7b476-112">Bug fixes</span></span>


<span data-ttu-id="7b476-113">**Erőforráskezelés**</span><span class="sxs-lookup"><span data-stu-id="7b476-113">**Resource Management**</span></span>

<span data-ttu-id="7b476-114">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="7b476-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="7b476-115">Az erőforrások rendelkezésre állásának keresésekor a rendszer az **ExpandCalendar** függvényt hívja minden olyan erőforráshoz, amelyre nem vonatkoznak naptári szabályok.</span><span class="sxs-lookup"><span data-stu-id="7b476-115">When finding resource availability, **ExpandCalendar** is called for each resource that has no calendar rules applied.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
