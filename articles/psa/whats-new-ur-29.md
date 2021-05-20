---
title: Újdonságok vagy változások a Project Service Automation 29-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 29-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 2ac47974b9cc8386c7446136faf48724de73efce
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948640"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="9abd8-103">Újdonságok vagy változások a Project Service Automation 29-es frissítési kiadásának V3 változatában</span><span class="sxs-lookup"><span data-stu-id="9abd8-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9abd8-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="9abd8-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9abd8-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="9abd8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9abd8-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="9abd8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9abd8-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="9abd8-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="9abd8-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9abd8-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9abd8-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 29-es frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="9abd8-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="9abd8-110">Ennek a verziónak a build száma V3.10.47.7, és általánosan elérhető egy önálló frissítésben 2021 februárjában.</span><span class="sxs-lookup"><span data-stu-id="9abd8-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="9abd8-111">29-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="9abd8-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9abd8-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="9abd8-112">Bug fixes</span></span>

<span data-ttu-id="9abd8-113">**Idő és költség**</span><span class="sxs-lookup"><span data-stu-id="9abd8-113">**Time and Expense**</span></span>

<span data-ttu-id="9abd8-114">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="9abd8-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="9abd8-115">A felhasználók nem látják a naplózott munkaórákat, amelyek nem munkanapokon vannak rögzítve az időbeviteli táblázatban.</span><span class="sxs-lookup"><span data-stu-id="9abd8-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="9abd8-116">A jóváhagyott költségbejegyzések a rácson szerkeszthetők.</span><span class="sxs-lookup"><span data-stu-id="9abd8-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="9abd8-117">**Projektmenedzsment**</span><span class="sxs-lookup"><span data-stu-id="9abd8-117">**Project Management**</span></span>

<span data-ttu-id="9abd8-118">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="9abd8-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="9abd8-119">Hiányzik az ellenőrzési logika, amely biztosítja, hogy az erőforrás-hozzárendelési munkaórák nem lehetnek negatívak.</span><span class="sxs-lookup"><span data-stu-id="9abd8-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="9abd8-120">Az **AssignResourcesForTask** egyéni művelet a csak a módosított mezők helyett az összes mezőt frissíti.</span><span class="sxs-lookup"><span data-stu-id="9abd8-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="9abd8-121">Ha olyan környezetben másol projektet, amely **CreateProject** eseményen regisztrált beépülő modulokkal vagy munkafolyamatokkal rendelkezik, a **msdyn_bulkgenerationstatus** attribútum nem frissül, ha a **CopyWBSToProject** nem sikerül.</span><span class="sxs-lookup"><span data-stu-id="9abd8-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="9abd8-122">A projektnaptár kibontásakor a munkanapok nem növekvő sorrendben vannak rendezve, így egyes projektfeladatok frissítése sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="9abd8-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="9abd8-123">Ha egy meglévő projekten módosítja a Projektkezelőt, akkor a szervezeti egység alapértelmezett logikája megváltozik.</span><span class="sxs-lookup"><span data-stu-id="9abd8-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="9abd8-124">**Értékesítés**</span><span class="sxs-lookup"><span data-stu-id="9abd8-124">**Sales**</span></span>

<span data-ttu-id="9abd8-125">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="9abd8-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="9abd8-126">Ha nincsenek szerződéssorok, akkor a **Szerződés** oldal **Szerződés teljesítése** lapja az inicializáció során a háttérben meghiúsul.</span><span class="sxs-lookup"><span data-stu-id="9abd8-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>