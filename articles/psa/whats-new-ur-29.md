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
ms.openlocfilehash: 0e1ff0db42adb8b991b26dca1585bd603b2e2276
ms.sourcegitcommit: f57408d6637f670b920d7ce95f8ace8eb1963093
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/17/2021
ms.locfileid: "5664646"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="19b94-103">Újdonságok vagy változások a Project Service Automation 29-es frissítési kiadásának V3 változatában</span><span class="sxs-lookup"><span data-stu-id="19b94-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="19b94-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="19b94-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="19b94-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="19b94-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="19b94-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="19b94-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="19b94-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="19b94-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="19b94-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="19b94-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="19b94-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 29-es frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="19b94-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="19b94-110">Ennek a verziónak a build száma V3.10.47.7, és általánosan elérhető egy önálló frissítésben 2021 februárjában.</span><span class="sxs-lookup"><span data-stu-id="19b94-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="19b94-111">29-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="19b94-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="19b94-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="19b94-112">Bug fixes</span></span>

<span data-ttu-id="19b94-113">**Idő és költség**</span><span class="sxs-lookup"><span data-stu-id="19b94-113">**Time and Expense**</span></span>

<span data-ttu-id="19b94-114">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="19b94-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="19b94-115">A felhasználók nem látják a naplózott munkaórákat, amelyek nem munkanapokon vannak rögzítve az időbeviteli táblázatban.</span><span class="sxs-lookup"><span data-stu-id="19b94-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="19b94-116">A jóváhagyott költségbejegyzések a rácson szerkeszthetők.</span><span class="sxs-lookup"><span data-stu-id="19b94-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="19b94-117">**Projektmenedzsment**</span><span class="sxs-lookup"><span data-stu-id="19b94-117">**Project Management**</span></span>

<span data-ttu-id="19b94-118">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="19b94-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="19b94-119">Hiányzik az ellenőrzési logika, amely biztosítja, hogy az erőforrás-hozzárendelési munkaórák nem lehetnek negatívak.</span><span class="sxs-lookup"><span data-stu-id="19b94-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="19b94-120">Az **AssignResourcesForTask** egyéni művelet a csak a módosított mezők helyett az összes mezőt frissíti.</span><span class="sxs-lookup"><span data-stu-id="19b94-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="19b94-121">Ha olyan környezetben másol projektet, amely **CreateProject** eseményen regisztrált beépülő modulokkal vagy munkafolyamatokkal rendelkezik, a **msdyn_bulkgenerationstatus** attribútum nem frissül, ha a **CopyWBSToProject** nem sikerül.</span><span class="sxs-lookup"><span data-stu-id="19b94-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="19b94-122">A projektnaptár kibontásakor a munkanapok nem növekvő sorrendben vannak rendezve, így egyes projektfeladatok frissítése sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="19b94-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="19b94-123">Ha egy meglévő projekten módosítja a Projektkezelőt, akkor a szervezeti egység alapértelmezett logikája megváltozik.</span><span class="sxs-lookup"><span data-stu-id="19b94-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="19b94-124">**Értékesítés**</span><span class="sxs-lookup"><span data-stu-id="19b94-124">**Sales**</span></span>

<span data-ttu-id="19b94-125">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="19b94-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="19b94-126">Ha nincsenek szerződéssorok, akkor a **Szerződés** oldal **Szerződés teljesítése** lapja az inicializáció során a háttérben meghiúsul.</span><span class="sxs-lookup"><span data-stu-id="19b94-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>
