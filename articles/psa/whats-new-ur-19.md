---
title: Újdonságok vagy változások a Project Service Automation 19-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 19-os frissítési kiadásában.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 7812bc41f32f9d4116c63990059f7dbc0351cf9e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006604"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="da373-103">Project Service Automation 19-es frissítési kiadás, V3</span><span class="sxs-lookup"><span data-stu-id="da373-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="da373-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="da373-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="da373-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="da373-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="da373-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="da373-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="da373-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="da373-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="da373-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="da373-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="da373-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a PSA V3. 19-ös frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="da373-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="da373-110">A verzió build száma V3.10.30.41, és általánosan elérhető lesz önálló frissítésként 2020 májusában.</span><span class="sxs-lookup"><span data-stu-id="da373-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="da373-111">19-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="da373-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="da373-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="da373-112">Bug fixes</span></span>

<span data-ttu-id="da373-113">**Idő és költség**</span><span class="sxs-lookup"><span data-stu-id="da373-113">**Time and Expense**</span></span>

<span data-ttu-id="da373-114">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="da373-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="da373-115">Az időbejegyzés-importálásokból származtatott hibák nem megfelelően jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="da373-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="da373-116">Az időbeviteli rács nem támogatja a **csak dátum** típusú mezők működését.</span><span class="sxs-lookup"><span data-stu-id="da373-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="da373-117">A Projekterőforrások nem tudnak költséget létrehozni egy projekttel.</span><span class="sxs-lookup"><span data-stu-id="da373-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="da373-118">**Projektmenedzsment**</span><span class="sxs-lookup"><span data-stu-id="da373-118">**Project Management**</span></span>

<span data-ttu-id="da373-119">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="da373-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="da373-120">Az unokafeladat a Befejezés (BefKB) kiszámítása során nem megfelelő erőfeszítés-becslést okoz.</span><span class="sxs-lookup"><span data-stu-id="da373-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="da373-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="da373-121">**Sales**</span></span>

<span data-ttu-id="da373-122">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="da373-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="da373-123">Az **Újraszámítás** művelet nem működik a költségszerződéssor részleteivel vagy az ajánlati sor részleteivel.</span><span class="sxs-lookup"><span data-stu-id="da373-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="da373-124">Az **Árak frissítése** hiányzik a költségbecsléseknél.</span><span class="sxs-lookup"><span data-stu-id="da373-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="da373-125">Az ügyfelek nem tudják kiválasztani az egyéni szerződésállapot-okot a **Projektszerződés** oldalon.</span><span class="sxs-lookup"><span data-stu-id="da373-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="da373-126">Az ügyfelek az árajánlatokból történő egyéni árlista létrehozásakor csökkentett teljesítményt tapasztalhatnak.</span><span class="sxs-lookup"><span data-stu-id="da373-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="da373-127">Az ügyfelek inkonzisztenciát észlelhetnek a **kiszerelés** alapértelmezett értékeiben az **Árajánlatsor részletei** és **Szerződéssor részletei** oldalakon.</span><span class="sxs-lookup"><span data-stu-id="da373-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="da373-128">Ha nem számlázható tranzakciókategóriájú cikkeket szeretne hozzáadni egy számlázható szerződéssorhoz, akkor a rendszer nem veszi figyelembe a tranzakciós kategória **Nem számlázható** számlázási típusát.</span><span class="sxs-lookup"><span data-stu-id="da373-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="da373-129">Az ügyfelek nem használhatják az újonnan hozzáadott szerepköröket és kategóriát a korábban létrehozott szerződésekben.</span><span class="sxs-lookup"><span data-stu-id="da373-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="da373-130">Az ügyfelek leromlott teljesítményt tapasztalhatnak a Szükségtelen beolvasásnál a PreValidateProjectTeamMemberUpdate.cs esetén</span><span class="sxs-lookup"><span data-stu-id="da373-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="da373-131">A nem számlázhatóként beállított szerepköröket az **Erőforrás-kategóriák** listában a rendszernek hozzá kellene adnia a **Számlázható szerepkörök** laphoz **Nem számlázható** értékkel a projekt szerződéssorában.</span><span class="sxs-lookup"><span data-stu-id="da373-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="da373-132">A projektek létrehozásakor az ügyfelek leromlott teljesítményt tapasztalhatnak, mivel a **GetBookableResourceIdFromUser** a foglalható erőforrások összes oszlopát beolvassa csak az elsődleges azonosító helyett.</span><span class="sxs-lookup"><span data-stu-id="da373-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="da373-133">**TransactionType** entitásból hiányzik az ellenőrzés előtti frissítés beépülő modul, amellyel megakadályozható, hogy a felhasználók tranzakciótípusokhoz nem érvényes **Kiszerelések** és **UnitGroups** értékeket adjanak meg.</span><span class="sxs-lookup"><span data-stu-id="da373-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="da373-134">Az **eltávolítás** lépés nem működik az időbejegyzés importálásához.</span><span class="sxs-lookup"><span data-stu-id="da373-134">The **Remove** step does not work for time entry import.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]