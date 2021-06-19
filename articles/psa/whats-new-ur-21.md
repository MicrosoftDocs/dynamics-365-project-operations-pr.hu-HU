---
title: Újdonságok vagy változások a Project Service Automation 21-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 21-os frissítési kiadásában.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: dd894f27baac70238d0bd9e9b1a21a9a499e1ea7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002330"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="9abbe-103">Project Service Automation 21-es frissítési kiadás, V3</span><span class="sxs-lookup"><span data-stu-id="9abbe-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9abbe-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="9abbe-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9abbe-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="9abbe-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9abbe-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="9abbe-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9abbe-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="9abbe-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="9abbe-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9abbe-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9abbe-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 21-es frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="9abbe-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="9abbe-110">A verzió build száma V 3.10.32.50, és általánosan elérhető lesz önálló frissítésként 2020 júniusában.</span><span class="sxs-lookup"><span data-stu-id="9abbe-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="9abbe-111">21-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="9abbe-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9abbe-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="9abbe-112">Bug fixes</span></span>

<span data-ttu-id="9abbe-113">**Idő és költség**</span><span class="sxs-lookup"><span data-stu-id="9abbe-113">**Time and Expense**</span></span>

<span data-ttu-id="9abbe-114">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="9abbe-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="9abbe-115">Amikor az irányítópulton található az **Időbeviteli rács vezérlő**, a rács nem használja az irányítópult rácsához tartozó tároló teljes szélességét.</span><span class="sxs-lookup"><span data-stu-id="9abbe-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="9abbe-116">Bizonyos időzónák esetén az **Időbejegyzés** rácsvezérlő nem jeleníti meg a bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="9abbe-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="9abbe-117">A 21:00 óra utáni időpontok nem megfelelő napon jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="9abbe-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="9abbe-118">A felhasználók nem küldhetnek be költséget, ha a **Költségnyugta szükséges** költségkategória nem tartalmaz értéket.</span><span class="sxs-lookup"><span data-stu-id="9abbe-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="9abbe-119">**Erőforráskezelés**</span><span class="sxs-lookup"><span data-stu-id="9abbe-119">**Resource Management**</span></span>

<span data-ttu-id="9abbe-120">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="9abbe-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="9abbe-121">Az inaktív foglalások az **Egyeztetés** nézetben jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="9abbe-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="9abbe-122">Az általános erőforrás-teljesítés esetében hiányzik az ellenőrzés az érvényes foglalási állapot meglétének biztosításához.</span><span class="sxs-lookup"><span data-stu-id="9abbe-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="9abbe-123">**Projektmenedzsment**</span><span class="sxs-lookup"><span data-stu-id="9abbe-123">**Project Management**</span></span>

<span data-ttu-id="9abbe-124">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="9abbe-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="9abbe-125">A **Projekt** űrlap rácsai (**Erőforrás-hozzárendelés**, **Feladat**, **Egyeztetés** nézet, **Kiadások becslése**) akkor is szerkeszthető maradnak, ha a projekt nem aktív.</span><span class="sxs-lookup"><span data-stu-id="9abbe-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="9abbe-126">A duplikált ügyfelek nem egyesíthetők a megerősített projekt-szerződésekhez kapcsolt ügyfelekkel.</span><span class="sxs-lookup"><span data-stu-id="9abbe-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="9abbe-127">Ha érvényes naptárral nem rendelkező erőforrást ad hozzá, akkor a rendszer nem küld vissza felhasználóbarát hibaüzenetet.</span><span class="sxs-lookup"><span data-stu-id="9abbe-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="9abbe-128">A **Feladat hozzáadása** gomb a feladatrácson engedélyezve van, amikor a projekt társítva a van a **Microsoft Project bővítményhez**.</span><span class="sxs-lookup"><span data-stu-id="9abbe-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="9abbe-129">Az erőfeszítés nem kontrollálhatóan nő, ha egy adott kategóriához tartozó feladatot egy erőforráshoz rendelnek, amelyhez olyan szerepkör tartozik, amelyhez önköltségi ár van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="9abbe-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="9abbe-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="9abbe-130">**Sales**</span></span>

<span data-ttu-id="9abbe-131">A következőket fejlesztettük:</span><span class="sxs-lookup"><span data-stu-id="9abbe-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="9abbe-132">A **Számlázás gyakorisága** és a **Számlázás kezdete** át lett helyezve a **Számla ütemezése** lapra.</span><span class="sxs-lookup"><span data-stu-id="9abbe-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="9abbe-133">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="9abbe-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="9abbe-134">A **Teljes eladási ár** nulla (0) a **Kategóriához** annak ellenére, hogy a **Szerepkörhöz** nem nulla teljes értékesítési ár tartozik.</span><span class="sxs-lookup"><span data-stu-id="9abbe-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="9abbe-135">Az ügyfelek nem módosíthatják a **Számlaállapot** mező értékét, **Számlázásra kész** értékre, amikor egy másik testreszabott folyamat egy további mezőt frissít.</span><span class="sxs-lookup"><span data-stu-id="9abbe-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="9abbe-136">A **Számlasorok frissítése** gomb több duplikált sort is létrehozhat, ha az ismételten ki van választva.</span><span class="sxs-lookup"><span data-stu-id="9abbe-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="9abbe-137">Az **Árak frissítése** gomb nem működik a **Szerepkörárak** alrácson a **Betekintő nézet** képernyőn.</span><span class="sxs-lookup"><span data-stu-id="9abbe-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="9abbe-138">Az **Értékesítési árlisták feloldási** logikája nem megfelelően kezeli az időzónákat, így az árlisták helytelenül lesznek kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="9abbe-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="9abbe-139">A projekt **Összes tényleges költsége** egyetlen időbevitel jóváhagyása után tört összeggel is elvégezhető.</span><span class="sxs-lookup"><span data-stu-id="9abbe-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="9abbe-140">Az **Árfeloldás** logikája nem biztosít felhasználóbarát hibaüzenetet, ha a **Beolvasott szerepkörár** nem rendelkezik az **„Elsődleges kiszerelés”** és az **„Ár az elsődleges kiszerelésben”** mezőkben értékkel.</span><span class="sxs-lookup"><span data-stu-id="9abbe-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]