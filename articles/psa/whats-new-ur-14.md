---
title: Újdonságok vagy változások a Project Service Automation 14-es frissítési kiadásának V3 változatában
description: Ez a témakör információkat nyújt arról, hogy milyen újdonságok és változások vannak a Project Service Automation 14-es frissítési kiadásának V3 verziójában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: e19c8ffe7d92ab7ec9eb46aff8f944c62b0bb4bc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280986"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="b04f2-103">Project Service Automation 14-es frissítési kiadás, V3</span><span class="sxs-lookup"><span data-stu-id="b04f2-103">Project Service Automation Update Release 14, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b04f2-104">Örömmel jelentjük be a Dynamics 365 Project Service Automation (PSA) alkalmazás legújabb frissítését.</span><span class="sxs-lookup"><span data-stu-id="b04f2-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="b04f2-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b04f2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b04f2-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="b04f2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b04f2-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez nyissa meg a megoldások oldalt.</span><span class="sxs-lookup"><span data-stu-id="b04f2-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="b04f2-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b04f2-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b04f2-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a PSA V3. 14-ös frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="b04f2-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="b04f2-110">Ennek a verziónak a build száma V 3.10.4.21, és a következő ütemezés szerint érhető el:</span><span class="sxs-lookup"><span data-stu-id="b04f2-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="b04f2-111">**Általános elérhetőség (Önálló frissítés):** 2020. január</span><span class="sxs-lookup"><span data-stu-id="b04f2-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="b04f2-112">**Automatikus frissítés:** 2020. február</span><span class="sxs-lookup"><span data-stu-id="b04f2-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="b04f2-113">14-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="b04f2-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="b04f2-114">Fejlesztések</span><span class="sxs-lookup"><span data-stu-id="b04f2-114">Enhancements</span></span>

- <span data-ttu-id="b04f2-115">Sales</span><span class="sxs-lookup"><span data-stu-id="b04f2-115">Sales</span></span>

     - <span data-ttu-id="b04f2-116">Az **Ajánlati sor részletei** mezőből származó egyéni mezőértékeket a program átmásolja a **Projektszerződés sorainak részletei** elemhez, amikor az ajánlatot **Lezárva megnyertként** értékre frissíti a rendszer.</span><span class="sxs-lookup"><span data-stu-id="b04f2-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="b04f2-117">A megerősített projektek állapota lehet **Lezárva elvesztettként**.</span><span class="sxs-lookup"><span data-stu-id="b04f2-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="b04f2-118">Erőforráskezelés</span><span class="sxs-lookup"><span data-stu-id="b04f2-118">Resource Management</span></span>

     - <span data-ttu-id="b04f2-119">A foglalások kibővítésekor a rendszer egy megerősítő párbeszédpanellel kéri a felhasználókat a foglalási eredmények összesítésére, és egy hivatkozást kínál a foglalások karbantartásához.</span><span class="sxs-lookup"><span data-stu-id="b04f2-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="b04f2-120">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="b04f2-120">Bug fixes</span></span>

- <span data-ttu-id="b04f2-121">Idő és költség</span><span class="sxs-lookup"><span data-stu-id="b04f2-121">Time and Expense</span></span>

     - <span data-ttu-id="b04f2-122">Javítva: A felhasználói élmény javítása, amikor a felhasználó nem jelölt ki semmilyen helyesbítendő bejegyzést.</span><span class="sxs-lookup"><span data-stu-id="b04f2-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="b04f2-123">Erőforráskezelés</span><span class="sxs-lookup"><span data-stu-id="b04f2-123">Resource Management</span></span>

     - <span data-ttu-id="b04f2-124">Javítva: Egy erőforrás többszöri foglalása túlcsordulást okoz a foglalt erőforrás nevében.</span><span class="sxs-lookup"><span data-stu-id="b04f2-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="b04f2-125">Sales</span><span class="sxs-lookup"><span data-stu-id="b04f2-125">Sales</span></span>

     - <span data-ttu-id="b04f2-126">Javítva: A teljes értékesítési ár nincs kiszámítva addig, amíg a felhasználó nem ad meg önköltségi árat költségbecslésekhez egy projektben.</span><span class="sxs-lookup"><span data-stu-id="b04f2-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="b04f2-127">Javítva: Az ajánlat lezárása **Megnyert** állapottal sikertelen, ha a társított szerződés nem **Vázlat** állapotú.</span><span class="sxs-lookup"><span data-stu-id="b04f2-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]