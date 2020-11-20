---
title: Újdonságok vagy változások a Project Service Automation 18-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 18-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 3a6d3ee21ecf742b2253132f3d3cc1cb2b57af75
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119871"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="72b0e-103">Project Service Automation 18-as frissítési kiadás, V3</span><span class="sxs-lookup"><span data-stu-id="72b0e-103">Project Service Automation Update Release 18, V3</span></span>

<span data-ttu-id="72b0e-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="72b0e-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="72b0e-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="72b0e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="72b0e-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="72b0e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="72b0e-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="72b0e-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="72b0e-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="72b0e-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="72b0e-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 18-es frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="72b0e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="72b0e-110">A verzió build száma V 3.10.8.12, és általánosan elérhető lesz önálló frissítésként 2020 áprilisában.</span><span class="sxs-lookup"><span data-stu-id="72b0e-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="72b0e-111">18-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="72b0e-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="72b0e-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="72b0e-112">Bug fixes</span></span>

<span data-ttu-id="72b0e-113">**Idő és költség**</span><span class="sxs-lookup"><span data-stu-id="72b0e-113">**Time and Expense**</span></span>

- <span data-ttu-id="72b0e-114">Javítva: A **Visszavonás**, **Kérelem** és **Jóváhagyás visszavonása** folyamatai kivételeket küldenek nem egyértelmű hibaüzenetekkel.</span><span class="sxs-lookup"><span data-stu-id="72b0e-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="72b0e-115">Javítva: Amikor a **Jóváhagyás visszavonása** sikertelen egy költség esetében, a rendszer nem jeleníti meg a megfelelő kivétellel kapcsolatos hibát.</span><span class="sxs-lookup"><span data-stu-id="72b0e-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="72b0e-116">Javítva: Az Időbejegyzés rács hibásan kezeli a munkaszüneti napokat Ausztráliában a nyári időszámítás (DST) októberi váltása után.</span><span class="sxs-lookup"><span data-stu-id="72b0e-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="72b0e-117">Javítva: a helytelen alapértelmezési logika megakadályozza a kiadások beküldését.</span><span class="sxs-lookup"><span data-stu-id="72b0e-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="72b0e-118">Javítva: Az időbejegyzés jóváhagyásának sikertelensége esetén a jóváhagyás **Függőben** állapotban marad.</span><span class="sxs-lookup"><span data-stu-id="72b0e-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="72b0e-119">Javítva: SQL-hibák tömeges jóváhagyáskor (kettős zárolás / időtúllépés).</span><span class="sxs-lookup"><span data-stu-id="72b0e-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="72b0e-120">Javítva: Az időbejegyzések jóváhagyása során a csoporttagok frissítése jelentős teljesítményproblémákat okoz a felhasználói élményben.</span><span class="sxs-lookup"><span data-stu-id="72b0e-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="72b0e-121">**Projektmenedzsment**</span><span class="sxs-lookup"><span data-stu-id="72b0e-121">**Project Management**</span></span>

- <span data-ttu-id="72b0e-122">Javítva: Az időzóna-értesítés áthelyezve az **Egyeztetés** nézetből a **Projekt** fő űrlapjára.</span><span class="sxs-lookup"><span data-stu-id="72b0e-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="72b0e-123">Javítva: A naptár sablonjának alapértelmezése nem megfelelő egy új projektűrlap megnyitásakor.</span><span class="sxs-lookup"><span data-stu-id="72b0e-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="72b0e-124">Javítva: A chromium alapú böngészőknél, a felhasználók nem tudják egyszerűen kiválaszthatja a megelőző tevékenységeket törlésre.</span><span class="sxs-lookup"><span data-stu-id="72b0e-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="72b0e-125">Javítva: A **Projekt üres sablonból** létrehozása vagy másolása nem kapcsolódó feladatokat olvas be.</span><span class="sxs-lookup"><span data-stu-id="72b0e-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="72b0e-126">Rögzített: Bizonyos szélsőséges esetekben új megbízás létrehozása a feladatrácsból duplikált bejegyzéseket eredményez.</span><span class="sxs-lookup"><span data-stu-id="72b0e-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="72b0e-127">Javítva: Manuális módban a felhasználók nem tudják frissíteni a feladat kezdési dátumát az aktuálisan mentett dátumnál későbbire.</span><span class="sxs-lookup"><span data-stu-id="72b0e-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="72b0e-128">**Erőforráskezelés**</span><span class="sxs-lookup"><span data-stu-id="72b0e-128">**Resource Management**</span></span>

- <span data-ttu-id="72b0e-129">Javítva: Az **Egyeztetés** nézet részösszeg sora helytelenül számítja ki a foglalások eltérését a foglalások meghosszabbítását követően.</span><span class="sxs-lookup"><span data-stu-id="72b0e-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="72b0e-130">Javítva: Az **Egyeztetés** nézet helytelenül jeleníti meg az erőforrás-hozzárendeléseket, ha a foglalt erőforráshoz olyan naptár tartozik, amely egyezik meg a projektnaptárral.</span><span class="sxs-lookup"><span data-stu-id="72b0e-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="72b0e-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="72b0e-131">**Sales**</span></span>

- <span data-ttu-id="72b0e-132">Rögzített: Az időbejegyzések újbóli jóváhagyása esetén (**Jóváhagyás > Visszavonás** ismételt jóváhagyás) egy duplikált, nem számlázható tényadat is létrehozásra kerül.</span><span class="sxs-lookup"><span data-stu-id="72b0e-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>
