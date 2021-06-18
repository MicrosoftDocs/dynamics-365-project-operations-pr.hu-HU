---
title: Újdonságok vagy változások a Project Service Automation 31-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 31-os frissítési kiadásában.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999134"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="30bae-103">Újdonságok vagy változások a Project Service Automation 31-es frissítési kiadásának V3 változatában</span><span class="sxs-lookup"><span data-stu-id="30bae-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="30bae-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="30bae-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="30bae-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="30bae-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="30bae-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="30bae-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="30bae-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="30bae-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="30bae-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="30bae-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="30bae-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 31-es frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="30bae-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="30bae-110">A verzió build száma V3.10.52.77, és általánosan elérhető lesz önálló frissítésként 2021 májusában.</span><span class="sxs-lookup"><span data-stu-id="30bae-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="30bae-111">31-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="30bae-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="30bae-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="30bae-112">Bug fixes</span></span>

<span data-ttu-id="30bae-113">**Idő és költség**</span><span class="sxs-lookup"><span data-stu-id="30bae-113">**Time and Expense**</span></span>

<span data-ttu-id="30bae-114">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="30bae-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="30bae-115">Az Időbevitel vezérlő parancsgombjai a **Foglalható erőforrás** lapon érthetetlenek voltak.</span><span class="sxs-lookup"><span data-stu-id="30bae-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="30bae-116">A **Project.SetTrackingFields** null referencia kivételt generált egy időbejegyzés jóváhagyásakor.</span><span class="sxs-lookup"><span data-stu-id="30bae-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="30bae-117">**Erőforráskezelés**</span><span class="sxs-lookup"><span data-stu-id="30bae-117">**Resource Management**</span></span>

<span data-ttu-id="30bae-118">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="30bae-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="30bae-119">A **Csapattag létrehozása** nem jeleníti meg helyesen a foglalási beállítások metaadatainak beállítását a **Foglalások alapértelmezett lekötött állapota** esetében.</span><span class="sxs-lookup"><span data-stu-id="30bae-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="30bae-120">A PSA 1.X verzióról 3.X verzióra való frissítés esetén a frissítési folyamat sikertelen lesz az **UpgradeResourceRequirements** elemben.</span><span class="sxs-lookup"><span data-stu-id="30bae-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="30bae-121">**Értékesítés**</span><span class="sxs-lookup"><span data-stu-id="30bae-121">**Sales**</span></span>

<span data-ttu-id="30bae-122">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="30bae-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="30bae-123">A tényleges bevétel a nyomkövetési táblázatban a projekt pénznemére váltja át az összegeket.</span><span class="sxs-lookup"><span data-stu-id="30bae-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="30bae-124">A pénznem alapértelmezett beállítása olyan helyzetekben, amikor a szervezet alappénzneme eltér a projektpénznemtől, árajánlatsorok és szerződéssorok létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="30bae-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="30bae-125">**A függőben lévő javításra vonatkozó** érvényesítési lekérdezés nem szűri le a projekteket.</span><span class="sxs-lookup"><span data-stu-id="30bae-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="30bae-126">A hátralévő értékesítések helytelen számítása történik egy projekten.</span><span class="sxs-lookup"><span data-stu-id="30bae-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="30bae-127">A kapcsolattartón alapuló ajánlatok nem sikerülnek, ha árlista nélkül jön létre.</span><span class="sxs-lookup"><span data-stu-id="30bae-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="30bae-128">Ha a **Számla megerősítése** lehetőséget választja, akkor nem jelenik meg a feldolgozásléptető.</span><span class="sxs-lookup"><span data-stu-id="30bae-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="30bae-129">Ha a **Számla létrehozása** lehetőséget választja, akkor nem jelenik meg a feldolgozásléptető</span><span class="sxs-lookup"><span data-stu-id="30bae-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="30bae-130">Az ajánlat elvesztettként való lezárása nem törli a foglalásokat.</span><span class="sxs-lookup"><span data-stu-id="30bae-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







