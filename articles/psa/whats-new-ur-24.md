---
title: Újdonságok vagy változások a Project Service Automation 24-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 24-os frissítési kiadásában.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c95a9dcada4fbf6c462df29d450aaafab4e73aa5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000259"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="bbe88-103">Project Service Automation 24-es frissítési kiadás, V3</span><span class="sxs-lookup"><span data-stu-id="bbe88-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="bbe88-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="bbe88-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="bbe88-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="bbe88-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="bbe88-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="bbe88-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="bbe88-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="bbe88-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="bbe88-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="bbe88-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="bbe88-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 24-es frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="bbe88-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="bbe88-110">Ennek a verziónak a buildszáma V3.10.42.43, és általánosan elérhető egy önálló frissítésben 2020 októberében.</span><span class="sxs-lookup"><span data-stu-id="bbe88-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="bbe88-111">24-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="bbe88-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="bbe88-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="bbe88-112">Bug fixes</span></span>

<span data-ttu-id="bbe88-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="bbe88-113">**Sales**</span></span>

<span data-ttu-id="bbe88-114">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="bbe88-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="bbe88-115">Probléma a termékek alapértelmezett árlistájának beállításakor.</span><span class="sxs-lookup"><span data-stu-id="bbe88-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="bbe88-116">Az árajánlat elnyerésének teljesítménye lassú a beágyazott árlista és a szerepkörár bejegyzések másolása miatt.</span><span class="sxs-lookup"><span data-stu-id="bbe88-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="bbe88-117">A **Projektszerződés/Értékesítési központ** > **Terméksorelem/Rendelési sor mennyisége** automatikusan a legközelebbi egész számra kerekítődik.</span><span class="sxs-lookup"><span data-stu-id="bbe88-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="bbe88-118">A rendszerjogosultság bővítése az árlisták olvasásakor.</span><span class="sxs-lookup"><span data-stu-id="bbe88-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="bbe88-119">A(z) **address1_freighttermscode** és a(z) **address1_shippingmethodcode** ügyfélcím mezőinek másolása az Árajánlat/Megrendelés mezőkbe.</span><span class="sxs-lookup"><span data-stu-id="bbe88-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="bbe88-120">**Idő és költség**</span><span class="sxs-lookup"><span data-stu-id="bbe88-120">**Time and Expense**</span></span>

<span data-ttu-id="bbe88-121">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="bbe88-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="bbe88-122">Az **Időbeviteli rács** nem támogatja a **Csak dátum** időműködést.</span><span class="sxs-lookup"><span data-stu-id="bbe88-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="bbe88-123">Az **Időbejegyzés** nem frissül automatikusan.</span><span class="sxs-lookup"><span data-stu-id="bbe88-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="bbe88-124">Manuális frissítés szükséges.</span><span class="sxs-lookup"><span data-stu-id="bbe88-124">A manual refresh is required.</span></span>
- <span data-ttu-id="bbe88-125">Nem lehet importálni az időpontokat egy hozzárendelésből, ha az erőforrás hozzárendeléseiben szünet (0 óra) van.</span><span class="sxs-lookup"><span data-stu-id="bbe88-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="bbe88-126">Az időbejegyzés létrehozásakor állítsa a kezdést ugyanarra, mint a következő: **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="bbe88-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="bbe88-127">Ismételten engedélyezheti az időbejegyzés csoportos szerkesztését.</span><span class="sxs-lookup"><span data-stu-id="bbe88-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="bbe88-128">**Erőforráskezelés**</span><span class="sxs-lookup"><span data-stu-id="bbe88-128">**Resource Management**</span></span>

<span data-ttu-id="bbe88-129">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="bbe88-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="bbe88-130">A napközbeni foglalás állapotának frissítése követelmény nélkül egy null értékű referenciakivételt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bbe88-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="bbe88-131">Hiba történt az **Egyeztetés nézet** betöltésekor.</span><span class="sxs-lookup"><span data-stu-id="bbe88-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="bbe88-132">**Projektmenedzsment**</span><span class="sxs-lookup"><span data-stu-id="bbe88-132">**Project Management**</span></span>

<span data-ttu-id="bbe88-133">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="bbe88-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="bbe88-134">A **Projekt ütemezése** menüben **Manuális** értékről **Automatikus** értékre történő váltáskor az automatikus mentés nem fejeződik be.</span><span class="sxs-lookup"><span data-stu-id="bbe88-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="bbe88-135">A költségeket nem szabad beleszámolni a **Projekt nyomonkövetési rács** pontban szereplő szórásokba.</span><span class="sxs-lookup"><span data-stu-id="bbe88-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="bbe88-136">Következetlen viselkedés a **Becslések címke** oszlopok betöltésekor, szemben az **Időfázis** típusának módosításával.</span><span class="sxs-lookup"><span data-stu-id="bbe88-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="bbe88-137">Előfordulhat, hogy a projekt tényleges költsége nem tükrözi **Tényadatok** pontban szereplő összegeket.</span><span class="sxs-lookup"><span data-stu-id="bbe88-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="bbe88-138">Az **Összegzés** lapon szereplő **Becsült befejezési dátum** nem egyezik meg a **WBS-ütemezéssel**.</span><span class="sxs-lookup"><span data-stu-id="bbe88-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="bbe88-139">A **Tényleges órák frissítése** a kihúzáson nem működik megfelelően.</span><span class="sxs-lookup"><span data-stu-id="bbe88-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="bbe88-140">A gyökér **üzleti egységen** kívüli projektmenedzserek nem tudnak projekteket létrehozni.</span><span class="sxs-lookup"><span data-stu-id="bbe88-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="bbe88-141">A feladat vagy a kategória változtatásai nem maradnak meg a **Költségbecslések** pontban.</span><span class="sxs-lookup"><span data-stu-id="bbe88-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="bbe88-142">A **Szerződés másolata** átmásolja a számlák ütemezéseit, valamint a futtatási állapotot.</span><span class="sxs-lookup"><span data-stu-id="bbe88-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="bbe88-143">A **Tényadatok frissítése** gomb hibásan számítja ki az összefoglaló feladatokat.</span><span class="sxs-lookup"><span data-stu-id="bbe88-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="bbe88-144">Microsoft Project-bővítmény: javítja a null referenciahibát, ha bármelyik csapattaghoz egy üres erőforrásbiztosító egység tartozik.</span><span class="sxs-lookup"><span data-stu-id="bbe88-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]