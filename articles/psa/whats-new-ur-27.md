---
title: Újdonságok vagy változások a Project Service Automation 27-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 27-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 6b9da3ec54ec10408774945d26db9e702c858d05
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146666"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a><span data-ttu-id="8a642-103">Újdonságok vagy változások a Project Service Automation 27-es frissítési kiadásának V3 változatában</span><span class="sxs-lookup"><span data-stu-id="8a642-103">What's new or changed in Project Service Automation Update Release 27, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8a642-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="8a642-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8a642-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="8a642-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8a642-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="8a642-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8a642-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="8a642-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="8a642-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="8a642-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8a642-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 27-es frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="8a642-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 27.</span></span> <span data-ttu-id="8a642-110">Ennek a verziónak a build száma V3.10.45.98, és általánosan elérhető egy önálló frissítésben 2021. januárjában.</span><span class="sxs-lookup"><span data-stu-id="8a642-110">This version has a build number of V3.10.45.98 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-27"></a><span data-ttu-id="8a642-111">27-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="8a642-111">Update Release 27</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8a642-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="8a642-112">Bug fixes</span></span>

<span data-ttu-id="8a642-113">**Általános**</span><span class="sxs-lookup"><span data-stu-id="8a642-113">**General**</span></span>

<span data-ttu-id="8a642-114">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="8a642-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="8a642-115">A Project Service Automation beépülő moduljai által létrehozott naplók nincsenek automatikus törlésre állítva.</span><span class="sxs-lookup"><span data-stu-id="8a642-115">Logs generated by plug-ins in Project Service Automation haven't been set to auto-delete.</span></span>
- <span data-ttu-id="8a642-116">Az automatikus frissítés sikertelen, mert a Project Service Automation megoldás örökölt null NavBarArea és cím elemet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="8a642-116">Auto-upgrade fails because the Project Service Automation solution contains a legacy null NavBarArea and title element.</span></span>

<span data-ttu-id="8a642-117">**Idő és költség**</span><span class="sxs-lookup"><span data-stu-id="8a642-117">**Time and Expense**</span></span>

<span data-ttu-id="8a642-118">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="8a642-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="8a642-119">Az **Időbejegyzés** rács helytelen adatokat jelenít meg az **Időzónától független** dátum viselkedéséhez.</span><span class="sxs-lookup"><span data-stu-id="8a642-119">The **Time Entry** grid displays incorrect data for **TimeZone Independent** date behavior.</span></span>
- <span data-ttu-id="8a642-120">Az **Időbejegyzés** rács helytelen időt hoz létre az **Időzónától független** dátum viselkedéséhez.</span><span class="sxs-lookup"><span data-stu-id="8a642-120">The **Time Entry** grid creates incorrect time for **TimeZone Independent** date behavior.</span></span>
- <span data-ttu-id="8a642-121">A tevékenység keresése nem korlátozódik a kijelölt projektre az **Időbejegyzés szerkesztése** lapon.</span><span class="sxs-lookup"><span data-stu-id="8a642-121">Task lookup isn't limited to the selected project on the **Edit Time Entry** page.</span></span>
- <span data-ttu-id="8a642-122">A projekten kívüli időbejegyzések időjóváhagyása a projekt jóváhagyójának keresésekor blokkolja a rendszert.</span><span class="sxs-lookup"><span data-stu-id="8a642-122">Time approval for non-project time entries is blocked because the system is looking for a project approver.</span></span>
- <span data-ttu-id="8a642-123">A Tényadatok helyes bejegyzései helytelen hibaüzenetet jelenítenek meg.</span><span class="sxs-lookup"><span data-stu-id="8a642-123">Correct entries on Actuals displays an incorrect error message.</span></span>
- <span data-ttu-id="8a642-124">Ha egy feladat null értéket tartalmaz a tényleges költségnél, és a projekt összesítései frissülnek, a következő hiba történik: „Az adott kulcs nem létezik a szótárban”.</span><span class="sxs-lookup"><span data-stu-id="8a642-124">When a task contains a null value for actual cost and the project totals are refreshed, the following error occurs, "Given key not present in dictionary".</span></span>
- <span data-ttu-id="8a642-125">Bizonyos esetekben a **Projektbecslés** fülön lévő **Csoportosítás** szűrők nem jelenítik meg a költségbecsléseket.</span><span class="sxs-lookup"><span data-stu-id="8a642-125">In specific instances, **Group By** filters on the **Project Estimate** tab does not display expense estimates.</span></span>
- <span data-ttu-id="8a642-126">A **Nyári időszámítás** időintervalluma nem megfelelő az időbejegyzések esetében.</span><span class="sxs-lookup"><span data-stu-id="8a642-126">**Daylight Saving Time** interval isn't correct for time entries.</span></span>

<span data-ttu-id="8a642-127">**Projektmenedzsment**</span><span class="sxs-lookup"><span data-stu-id="8a642-127">**Project Management**</span></span>

<span data-ttu-id="8a642-128">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="8a642-128">The following issues have been fixed:</span></span>

- <span data-ttu-id="8a642-129">A gyorsítótárazási fejlesztések, amelyek növelik a **Projekt** oldal betöltésével kapcsolatos teljesítményt.</span><span class="sxs-lookup"><span data-stu-id="8a642-129">Caching improvements, which enhances performance related to loading the **Project** page.</span></span>
- <span data-ttu-id="8a642-130">Egy elavult üzleti szabály megakadályozza a projektfeladatok elvégzését.</span><span class="sxs-lookup"><span data-stu-id="8a642-130">Obsolete business rule preventing project tasks from being completed.</span></span>
- <span data-ttu-id="8a642-131">A Microsoft Project bővítménykontúrok nem tartják tiszteletben a bővítmény naptárát, ami helytelen erőforrás-követelményeket eredményez.</span><span class="sxs-lookup"><span data-stu-id="8a642-131">Microsoft Project Add-in contours aren't respecting the add-in’s calendar resulting in incorrect resource requirements.</span></span>
- <span data-ttu-id="8a642-132">A projektek sablonokból történő létrehozása helytelenül állítja be a hozzárendelési dátumokat, és megakadályozza az erőforrás-követelmények létrehozását.</span><span class="sxs-lookup"><span data-stu-id="8a642-132">Creating projects from templates incorrectly sets assignment dates and prevents the ability to generate resource requirements.</span></span>
- <span data-ttu-id="8a642-133">A felhasználó nem tudja elérni a **Kategória**, **Leírás**, **Állapot** lehetőségeket a billentyűzet használatával.</span><span class="sxs-lookup"><span data-stu-id="8a642-133">User can't access **Category**, **Description**, **Status** options using the keyboard.</span></span>
- <span data-ttu-id="8a642-134">A projekt tényleges értékesítési értékei nem tartalmaznak díj- és anyagértékesítési értékeket.</span><span class="sxs-lookup"><span data-stu-id="8a642-134">Actual sales values of the project aren't including fee and materials sales values.</span></span>
- <span data-ttu-id="8a642-135">A tényleges értékesítések és a tényleges költségek összesítése helytelenül és különböző árfolyamokkal történik.</span><span class="sxs-lookup"><span data-stu-id="8a642-135">Aggregation of actual sales and actual cost happens incorrectly with different exchange rates.</span></span>
- <span data-ttu-id="8a642-136">Az **Alapértelmezett munkaóra sablon** leírása félrevezető.</span><span class="sxs-lookup"><span data-stu-id="8a642-136">The description in the **Default Work Hour Template** is misleading.</span></span>
- <span data-ttu-id="8a642-137">A feladat behúzása addig nem távolítja el a **Kategória** parancsot a felhasználói felületen, amíg nem frissül.</span><span class="sxs-lookup"><span data-stu-id="8a642-137">Indenting a task doesn't remove **Category** in the user interface until it is refreshed.</span></span>
- <span data-ttu-id="8a642-138">Az ellenőrzés kihagyása annak biztosítása érdekében, hogy a projekt a befejezési dátumon belül teljesüljön, nem engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="8a642-138">Missing validation to ensure moving a project beyond its end date isn't permitted.</span></span>

<span data-ttu-id="8a642-139">**Sales**</span><span class="sxs-lookup"><span data-stu-id="8a642-139">**Sales**</span></span>

<span data-ttu-id="8a642-140">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="8a642-140">The following issues have been fixed:</span></span>

- <span data-ttu-id="8a642-141">A projekt ajánlatsorán null hivatkozási kivétel jön létre, mert az **Importálás projektbecslésből** akkor látható, ha a projekt nincs kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="8a642-141">A null reference exception is generated on a project quote line because **Import from Project Estimation** is visible when a project hasn't been selected.</span></span>
- <span data-ttu-id="8a642-142">Az „Objektumhivatkozás nincs objektumpéldányra állítva” hibaüzenet akkor jelenik meg, amikor egy ajánlatot **Megnyert** állapotban zárnak le.</span><span class="sxs-lookup"><span data-stu-id="8a642-142">The following error, "Object reference not set to an instance of an object" occurs when closing a quote as **Won**.</span></span>
- <span data-ttu-id="8a642-143">A korrekció állapota a tényleges sztornírozás során nincs megadva a projekt szerződéssorról történő leválasztása közben.</span><span class="sxs-lookup"><span data-stu-id="8a642-143">Adjustment status isn't set during an actual reversal while unlinking a project from a contract line.</span></span>
- <span data-ttu-id="8a642-144">Ha a Dynamics 365 Field Service és a Project Service Automation egyaránt telepítve van, a **Zárolási díjszabás** és az **Aktuális díjszabás használata** beállítás nem jelenik meg egyszerre a **Számla** lapon.</span><span class="sxs-lookup"><span data-stu-id="8a642-144">When Dynamics 365 Field Service and Project Service Automation are both installed, the **Lock pricing** and **Use Current Pricing** options are not displayed at a same time on the **Invoice** page.</span></span>
- <span data-ttu-id="8a642-145">A japán nyelv esetében nincs más naptáralapú oldalakkal konzisztens fordítás.</span><span class="sxs-lookup"><span data-stu-id="8a642-145">For the Japanese language, there is inconsistent translation with other calendar-based pages.</span></span>
- <span data-ttu-id="8a642-146">Az **Aktiválás** és **Inaktiválás** el lett távolítva a Project Service Automation **Árlistatársítás** entitásaiból.</span><span class="sxs-lookup"><span data-stu-id="8a642-146">**Activate** and **Deactivate** have been removed from **Price List Association** entities in Project Service Automation.</span></span>