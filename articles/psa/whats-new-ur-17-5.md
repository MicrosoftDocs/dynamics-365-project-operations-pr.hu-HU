---
title: Újdonságok vagy változások a Project Service Automation 17.5-es gyorsjavításának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 17.5-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/13/2020
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
ms.openlocfilehash: 359eb8f8ca41d69d4f30dd44497a4deb6a6c4f8d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078047"
---
# <a name="project-service-automation-update-release-175-v3"></a><span data-ttu-id="697fc-103">Project Service Automation 17.5-ös frissítési kiadás, V3</span><span class="sxs-lookup"><span data-stu-id="697fc-103">Project Service Automation Update Release 17.5, V3</span></span>

<span data-ttu-id="697fc-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="697fc-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="697fc-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="697fc-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="697fc-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="697fc-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="697fc-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="697fc-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="697fc-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="697fc-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="697fc-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a V3. 17.5-ös frissítési kiadásban.</span><span class="sxs-lookup"><span data-stu-id="697fc-109">This topic lists the features and fixes that are new or changed for V3, Update Release 17.5.</span></span> <span data-ttu-id="697fc-110">Ennek a verziónak a build száma V 3.10.5.32, és általánosan elérhető egy önálló frissítésben 2020 márciusában.</span><span class="sxs-lookup"><span data-stu-id="697fc-110">This version has a build number of V3.10.7.32 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-175"></a><span data-ttu-id="697fc-111">17.5-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="697fc-111">Update Release 17.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="697fc-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="697fc-112">Bug fixes</span></span>


<span data-ttu-id="697fc-113">**Projektmenedzsment**</span><span class="sxs-lookup"><span data-stu-id="697fc-113">**Project Management**</span></span>

- <span data-ttu-id="697fc-114">Javítva: A hosszú ideig tartó feladatoknál tapasztalhat, kiszolgálóoldali szinkronizálási problémák megoldása.</span><span class="sxs-lookup"><span data-stu-id="697fc-114">Fixed: Addressed server-side synchronization issues that occur with long duration tasks.</span></span>
- <span data-ttu-id="697fc-115">Rögzített: A napi 24 órás munkaidő-sablonok helytelenül egy újabb napot vesznek fel a feladatokba, ez javítva lett.</span><span class="sxs-lookup"><span data-stu-id="697fc-115">Fixed: Addressed 24-hour work hour templates inaccurately adding an additional day to tasks.</span></span>
- <span data-ttu-id="697fc-116">Javítva: A + 13 GMT munkaidő-sablonjai helytelenül áthelyezik a feladatokat egy nappal előre.</span><span class="sxs-lookup"><span data-stu-id="697fc-116">Fixed: Addressed +13 GMT work hour templates inaccurately shifting tasks one day ahead.</span></span>

