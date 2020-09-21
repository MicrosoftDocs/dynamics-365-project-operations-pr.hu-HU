---
title: Újdonságok a Project Service Automation 12-es frissítési kiadásának V3 változatában
description: Ez a témakör információkat nyújt arról, hogy milyen újdonságok és változások vannak a Project Service Automation 12-ös frissítési kiadásának V3 verziójában.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752226"
---
# <a name="project-service-automation-v3-update-release-12"></a><span data-ttu-id="3c324-103">Project Service Automation V3, 12-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="3c324-103">Project Service Automation V3, Update Release 12</span></span>
<span data-ttu-id="3c324-104">Örömmel jelentjük be a Dynamics 365 Project Service Automation (PSA) alkalmazás legújabb frissítését.</span><span class="sxs-lookup"><span data-stu-id="3c324-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="3c324-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="3c324-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3c324-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="3c324-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3c324-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez nyissa meg a megoldások oldalt.</span><span class="sxs-lookup"><span data-stu-id="3c324-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="3c324-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="3c324-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3c324-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 12-es frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="3c324-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="3c324-110">Ennek a verziónak a build száma V3.10.2.34, és általánosan elérhető egy önálló frissítésben 2019 októberében.</span><span class="sxs-lookup"><span data-stu-id="3c324-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="3c324-111">12-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="3c324-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3c324-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="3c324-112">Bug fixes</span></span>

- <span data-ttu-id="3c324-113">Idő és költség</span><span class="sxs-lookup"><span data-stu-id="3c324-113">Time and Expense</span></span>

    - <span data-ttu-id="3c324-114">Javítva: Az időbevitel hibaüzenetei további releváns környezettel frissültek.</span><span class="sxs-lookup"><span data-stu-id="3c324-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="3c324-115">Javítva: Az időbeviteli rács és az ütemezés helyesen jeleníti meg a függőleges görgetősávot, ha szükséges.</span><span class="sxs-lookup"><span data-stu-id="3c324-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="3c324-116">Javítva: Az elküldött és a jóváhagyott költség- időbejegyzések jóváhagyhatók.</span><span class="sxs-lookup"><span data-stu-id="3c324-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="3c324-117">Javítva: A jóváhagyás megerősítésének visszavonása párbeszédpanel üzenete ki lett javítva, hogy tükrözze a jóváhagyás állapotát a **Jóváhagyott** értékről **Beküldött** értékre való váltáskor.</span><span class="sxs-lookup"><span data-stu-id="3c324-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="3c324-118">Javítva: Az **Ár**, **Egység** és **Mennyiség** mezők zárolva vannak a Ráfordítás bejegyzésen, miután annak jóváhagyása megtörtént.</span><span class="sxs-lookup"><span data-stu-id="3c324-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="3c324-119">Projektmenedzsment</span><span class="sxs-lookup"><span data-stu-id="3c324-119">Project Management</span></span>

    - <span data-ttu-id="3c324-120">Javítva: Az **Új** művelet a **Csapattag** fő űrlapon el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="3c324-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="3c324-121">Javítva: Az erőforrás-hozzárendelések frissítése javítva lett, hogy számoljon a pontatlan kerekítési hibákkal, amelyek egy feladat záró dátumának eltolódását okozzák.</span><span class="sxs-lookup"><span data-stu-id="3c324-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="3c324-122">Javítva: A feladatrácsban a releváns kiszolgálóoldali hibák a felhasználó számára is láthatók lesznek.</span><span class="sxs-lookup"><span data-stu-id="3c324-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="3c324-123">Javítva A csapattag neve a feladat személyválasztójában jelenik meg a pozíciónév helyett.</span><span class="sxs-lookup"><span data-stu-id="3c324-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="3c324-124">Erőforráskezelés</span><span class="sxs-lookup"><span data-stu-id="3c324-124">Resource Management</span></span>

    - <span data-ttu-id="3c324-125">Jaívítva: Az erőforrás-követelmények részletei a sablonból létrehozott projektek esetén a projektnaptárt használják.</span><span class="sxs-lookup"><span data-stu-id="3c324-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="3c324-126">Javítva: A szakértelmek és a kompetenciák alapértelmezetten a szerepkör mesteradataiból kerülnek a szerepkörhöz létrehozott erőforráskövetelményeibe.</span><span class="sxs-lookup"><span data-stu-id="3c324-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="3c324-127">Sales</span><span class="sxs-lookup"><span data-stu-id="3c324-127">Sales</span></span>

    - <span data-ttu-id="3c324-128">Javítva: A **Szerződés fő** űrlapján található duplikált objektumazonosítók.</span><span class="sxs-lookup"><span data-stu-id="3c324-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="3c324-129">Javítva: a logika frissítve lett, így láthatóvá válik az **Ajánlat elemzése** lap, hogy megjelenítse a lap metaadat-beállításait.</span><span class="sxs-lookup"><span data-stu-id="3c324-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="3c324-130">Javítva: A tényleges bejegyzésen a számlázási dátum immár az idő/költség dátumából származik és nem a jóváhagyás dátumából.</span><span class="sxs-lookup"><span data-stu-id="3c324-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
