---
title: Újdonságok vagy változások a Project Service Automation 13-es frissítési kiadásának V3 változatában
description: Ez a témakör információkat nyújt arról, hogy milyen újdonságok és változások vannak a Project Service Automation 13-ös frissítési kiadásának V3 verziójában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 7287054c470a44ed1fdc243018ec935fe21a6c4f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147251"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="194f3-103">Project Service Automation 13-es frissítési kiadás, V3</span><span class="sxs-lookup"><span data-stu-id="194f3-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="194f3-104">Örömmel jelentjük be a Dynamics 365 Project Service Automation (PSA) alkalmazás legújabb frissítését.</span><span class="sxs-lookup"><span data-stu-id="194f3-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="194f3-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="194f3-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="194f3-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="194f3-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="194f3-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez nyissa meg a megoldások oldalt.</span><span class="sxs-lookup"><span data-stu-id="194f3-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="194f3-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="194f3-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="194f3-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 13-es frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="194f3-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="194f3-110">Ennek a verziónak a build száma V 3.10.3.18, és a következő ütemezés szerint érhető el:</span><span class="sxs-lookup"><span data-stu-id="194f3-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="194f3-111">**Általános elérhetőség (Önálló frissítés):** 2019. november</span><span class="sxs-lookup"><span data-stu-id="194f3-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="194f3-112">**Automatikus frissítés:** 2019. december</span><span class="sxs-lookup"><span data-stu-id="194f3-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="194f3-113">13-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="194f3-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="194f3-114">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="194f3-114">Bug fixes</span></span>

- <span data-ttu-id="194f3-115">Idő és költség</span><span class="sxs-lookup"><span data-stu-id="194f3-115">Time and Expense</span></span>

     - <span data-ttu-id="194f3-116">Javítva: A **Költség-jóváhagyás** lapon a keresési funkció nem működik, ha költség célja alapján keres.</span><span class="sxs-lookup"><span data-stu-id="194f3-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="194f3-117">Erőforráskezelés</span><span class="sxs-lookup"><span data-stu-id="194f3-117">Resource Management</span></span>

     - <span data-ttu-id="194f3-118">Javítva: Az egyeztetésben szereplő frissítve lettek, hogy jobbra igazítottak legyenek.</span><span class="sxs-lookup"><span data-stu-id="194f3-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="194f3-119">Javítva: A megnevezett erőforrások nem rendelhetők hozzá a feladatokhoz az **Ütemezés** lapon.</span><span class="sxs-lookup"><span data-stu-id="194f3-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="194f3-120">Projektmenedzsment</span><span class="sxs-lookup"><span data-stu-id="194f3-120">Project Management</span></span>

     - <span data-ttu-id="194f3-121">Javítva: Null hivatkozás kivétel csoporttag hozzárendelésekor, amikor a **TransactionType** esetében hiányzik a beállítási információ az **Egység** és **DefaultGroup** esetében.</span><span class="sxs-lookup"><span data-stu-id="194f3-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="194f3-122">Sales</span><span class="sxs-lookup"><span data-stu-id="194f3-122">Sales</span></span>

     - <span data-ttu-id="194f3-123">Javítva: A duplikált tranzakciótípus-rekordok hibát adnak vissza a szerepkör árrekordjai létrehozása során.</span><span class="sxs-lookup"><span data-stu-id="194f3-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="194f3-124">Rögzített: Extra gombok az **Új lehetőség**, **Árajánlat**, **Rendelési sor** és **Termék hozzáadása** elemekhez láthatóvá válnak a Lehetőségek, Árajánlatok és Rendeléshez tartozó termékek parancsaiban, és a projektalapú Sorok részrácson.</span><span class="sxs-lookup"><span data-stu-id="194f3-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>


