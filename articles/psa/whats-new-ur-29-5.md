---
title: Újdonságok vagy változások a Project Service Automation 29.5-es gyorsjavításának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetőek a Project Service Automation 29.5-es gyorsjavításának V3 változatában.
author: ruhercul
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
ms.openlocfilehash: d5050945c4ab7c1da61b07ec08bed20f32e166b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999179"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-295-v3"></a><span data-ttu-id="63870-103">Újdonságok vagy változások a Project Service Automation 29.5-es frissítési kiadásának V3 változatában</span><span class="sxs-lookup"><span data-stu-id="63870-103">What's new or changed in Project Service Automation Update Release 29.5, V3</span></span>

<span data-ttu-id="63870-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="63870-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="63870-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="63870-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="63870-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="63870-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="63870-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="63870-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="63870-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="63870-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="63870-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 29.5-es frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="63870-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.5.</span></span> <span data-ttu-id="63870-110">Ennek a verziónak a build száma V3.10.47.150, és általánosan elérhető egy önálló frissítésben 2021. januárjában.</span><span class="sxs-lookup"><span data-stu-id="63870-110">This version has a build number of V3.10.47.150 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-295"></a><span data-ttu-id="63870-111">29.5-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="63870-111">Update Release 29.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="63870-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="63870-112">Bug fixes</span></span>


<span data-ttu-id="63870-113">**Értékesítés**</span><span class="sxs-lookup"><span data-stu-id="63870-113">**Sales**</span></span>

<span data-ttu-id="63870-114">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="63870-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="63870-115">A **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** fájlban null értékű hivatkozáskivétel történik, amikor megnyertként zár le egy árajánlatot, és az ajánlatnak nincs árlistája.</span><span class="sxs-lookup"><span data-stu-id="63870-115">A possible null reference exception occurs in **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** when you close a quote as won and the quote has no price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
