---
title: Újdonságok vagy változások a Project Service Automation 29.5-es gyorsjavításának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetőek a Project Service Automation 29.5-es gyorsjavításának V3 változatában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/26/2021
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
ms.openlocfilehash: 99ba353236ad88b8bdff2c1b25e1247fa4bf3455
ms.sourcegitcommit: 9ebf7dd501898053bfa824f732adabf3f273613b
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/26/2021
ms.locfileid: "5715675"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-295-v3"></a><span data-ttu-id="9d655-103">Újdonságok vagy változások a Project Service Automation 29.5-es frissítési kiadásának V3 változatában</span><span class="sxs-lookup"><span data-stu-id="9d655-103">What's new or changed in Project Service Automation Update Release 29.5, V3</span></span>

<span data-ttu-id="9d655-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="9d655-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9d655-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="9d655-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9d655-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="9d655-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9d655-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="9d655-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="9d655-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9d655-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9d655-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 29.5-es frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="9d655-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.5.</span></span> <span data-ttu-id="9d655-110">Ennek a verziónak a build száma V3.10.47.150, és általánosan elérhető egy önálló frissítésben 2021. januárjában.</span><span class="sxs-lookup"><span data-stu-id="9d655-110">This version has a build number of V3.10.47.150 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-295"></a><span data-ttu-id="9d655-111">29.5-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="9d655-111">Update Release 29.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9d655-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="9d655-112">Bug fixes</span></span>


<span data-ttu-id="9d655-113">**Értékesítés**</span><span class="sxs-lookup"><span data-stu-id="9d655-113">**Sales**</span></span>

<span data-ttu-id="9d655-114">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="9d655-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="9d655-115">A **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** fájlban null értékű hivatkozáskivétel történik, amikor megnyertként zár le egy árajánlatot, és az ajánlatnak nincs árlistája.</span><span class="sxs-lookup"><span data-stu-id="9d655-115">A possible null reference exception occurs in **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** when you close a quote as won and the quote has no price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
