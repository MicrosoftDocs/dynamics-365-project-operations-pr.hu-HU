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
ms.openlocfilehash: 829f0941f255aab11a37cacd90c0dca6f99bc2d2
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948737"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-276-v3"></a><span data-ttu-id="b59c5-103">Újdonságok vagy változások a Project Service Automation 27.6-es frissítési kiadásának V3 változatában</span><span class="sxs-lookup"><span data-stu-id="b59c5-103">What's new or changed in Project Service Automation Update Release 27.6, V3</span></span>

<span data-ttu-id="b59c5-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="b59c5-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b59c5-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b59c5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b59c5-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="b59c5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b59c5-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="b59c5-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b59c5-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b59c5-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b59c5-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 27.6-es frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="b59c5-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 27.6.</span></span> <span data-ttu-id="b59c5-110">Ennek a verziónak a build száma V3.10.45.120, és általánosan elérhető egy önálló frissítésben 2021. januárjában.</span><span class="sxs-lookup"><span data-stu-id="b59c5-110">This version has a build number of V3.10.45.120 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-276"></a><span data-ttu-id="b59c5-111">27.6-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="b59c5-111">Update Release 27.6</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b59c5-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="b59c5-112">Bug fixes</span></span>


<span data-ttu-id="b59c5-113">**Erőforráskezelés**</span><span class="sxs-lookup"><span data-stu-id="b59c5-113">**Resource Management**</span></span>

<span data-ttu-id="b59c5-114">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="b59c5-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="b59c5-115">Az erőforrások rendelkezésre állásának keresésekor a rendszer az **ExpandCalendar** függvényt hívja minden olyan erőforráshoz, amelyre nem vonatkoznak naptári szabályok.</span><span class="sxs-lookup"><span data-stu-id="b59c5-115">When finding resource availability, **ExpandCalendar** is called for each resource that has no calendar rules applied.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]