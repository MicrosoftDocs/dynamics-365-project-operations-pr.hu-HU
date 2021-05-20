---
title: Újdonságok vagy változások a Project Service Automation 28-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 28-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2d5e8c629f8108ed039948ca70842c9d8afebfa6
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948689"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="14ed9-103">Újdonságok vagy változások a Project Service Automation 28-es frissítési kiadásának V3 változatában</span><span class="sxs-lookup"><span data-stu-id="14ed9-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="14ed9-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="14ed9-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="14ed9-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="14ed9-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="14ed9-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="14ed9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="14ed9-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="14ed9-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="14ed9-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="14ed9-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="14ed9-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy módosultak a Project Service Automation V3 verzió 28-es frissítéskiadásnál. Ez a verzió a V3.10.46.32 buildszámmal rendelkezik, és 2021 januárjában általánosan elérhető egy önkiszolgáló frissítéssel.</span><span class="sxs-lookup"><span data-stu-id="14ed9-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="14ed9-110">28-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="14ed9-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="14ed9-111">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="14ed9-111">Bug fixes</span></span>

<span data-ttu-id="14ed9-112">**Idő és költség**</span><span class="sxs-lookup"><span data-stu-id="14ed9-112">**Time and Expense**</span></span>

<span data-ttu-id="14ed9-113">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="14ed9-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="14ed9-114">A felhasználók a **Tömeges szerkesztés** segítségével frissíthetik a jóváhagyott és elküldött időbejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="14ed9-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="14ed9-115">**Projektmenedzsment**</span><span class="sxs-lookup"><span data-stu-id="14ed9-115">**Project Management**</span></span>

<span data-ttu-id="14ed9-116">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="14ed9-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="14ed9-117">Azokban az esetekben, amikor a tevékenység GUID-azonosítóját számként értelmezi, a tevékenységek nem nyithatók meg szerkesztésre **Munkalebontási struktúra** lap menüszalagján található **Tevékenység szerkesztése** használatával.</span><span class="sxs-lookup"><span data-stu-id="14ed9-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="14ed9-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="14ed9-118">**Sales**</span></span>

<span data-ttu-id="14ed9-119">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="14ed9-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="14ed9-120">Egy nulla hivatkozási kivétel jön létre a **GetEstimatesForProject** beépülő modul meghívásakor.</span><span class="sxs-lookup"><span data-stu-id="14ed9-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="14ed9-121">A mérföldkő rácson **Számlakészként megjelölés** csak részben frissíti az attribútumokat, kivéve a frissített **InvoiceStatus** attribútumot.</span><span class="sxs-lookup"><span data-stu-id="14ed9-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]