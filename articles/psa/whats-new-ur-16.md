---
title: Újdonságok vagy változások a Project Service Automation 16-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 16-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 2c93d34b61001b7755d426539ac384641a7bc9da
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121581"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="db7b1-103">Project Service Automation 16-os frissítési kiadás, V3</span><span class="sxs-lookup"><span data-stu-id="db7b1-103">Project Service Automation Update Release 16, V3</span></span>

<span data-ttu-id="db7b1-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="db7b1-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="db7b1-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="db7b1-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="db7b1-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="db7b1-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="db7b1-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="db7b1-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="db7b1-108">További információ: [Előnyben részesített telepítése, frissítése](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="db7b1-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="db7b1-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a PSA V3. 16-ös frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="db7b1-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="db7b1-110">Ennek a verziónak a build száma V3.10.6.34, és általánosan elérhető egy önálló frissítésben 2020. januárjában.</span><span class="sxs-lookup"><span data-stu-id="db7b1-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="db7b1-111">16-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="db7b1-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="db7b1-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="db7b1-112">Bug fixes</span></span>

-   <span data-ttu-id="db7b1-113">Idő és költség</span><span class="sxs-lookup"><span data-stu-id="db7b1-113">Time and Expense</span></span>

    -   <span data-ttu-id="db7b1-114">Javítva: A felhasználók, akik törölt idő- vagy költségbejegyzéseket küldenek be jóváhagyásra mostantól ehhez kapcsolódó hibaüzenetet kapnak.</span><span class="sxs-lookup"><span data-stu-id="db7b1-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="db7b1-115">Projektmenedzsment</span><span class="sxs-lookup"><span data-stu-id="db7b1-115">Project Management</span></span>

    -   <span data-ttu-id="db7b1-116">Javítva: A sablonokban a csapattagokhoz definiált erőforrásegységek figyelembe lesznek véve a sablonokban, és alkalmazva lesznek az új projektre.</span><span class="sxs-lookup"><span data-stu-id="db7b1-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="db7b1-117">Javítva: Bejegyzések tulajdonjogának újbóli hozzárendelésének továbbfejlesztett kezelése.</span><span class="sxs-lookup"><span data-stu-id="db7b1-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="db7b1-118">Javítva A másolás alatt álló projektek másolása az összes másolási művelet befejezéséig nem engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="db7b1-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="db7b1-119">Erőforráskezelés</span><span class="sxs-lookup"><span data-stu-id="db7b1-119">Resource Management</span></span>

    -   <span data-ttu-id="db7b1-120">Javítva: A foglalások meghosszabbítása mostantól helyesen kezeli a rövid időtartamokat, és a továbbiakban nem hoz létre nulla órákat a meghosszabbított foglalásokhoz.</span><span class="sxs-lookup"><span data-stu-id="db7b1-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="db7b1-121">Javítva: Az egyeztetési nézet immár megjelenítésre kerül, ha a projekt időzónája +5:30 GMT és a felhasználó időzónája eltérő.</span><span class="sxs-lookup"><span data-stu-id="db7b1-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="db7b1-122">Sales</span><span class="sxs-lookup"><span data-stu-id="db7b1-122">Sales</span></span>

    -   <span data-ttu-id="db7b1-123">Javítva: Egy szerződéssorhoz társított projekt eltávolítása és egy új projekt társítása esetén az új projektben szereplő tényadat-bejegyzések nem lettek újra kiértékelve a szerződéssorhoz definiált számlázási és árképzési szabályok alapján.</span><span class="sxs-lookup"><span data-stu-id="db7b1-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="db7b1-124">Ez ebben a kiadásban ez javítva lett.</span><span class="sxs-lookup"><span data-stu-id="db7b1-124">This has been fixed in this release.</span></span> <span data-ttu-id="db7b1-125">A projekthez újonnan társított árképzési és tényadat-bejegyzések a szerződéssor árazási és számlázási szabályai alapján vissza lesznek állítva, és helyesen lesznek létrehozva.</span><span class="sxs-lookup"><span data-stu-id="db7b1-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="db7b1-126">A megszüntetett hozzárendelésű projekt tényadat-bejegyzései ennek megfelelően újra lesznek értékelve, és újra létre lesznek hozva.</span><span class="sxs-lookup"><span data-stu-id="db7b1-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="db7b1-127">Javítva: A rendszer további ellenőrzést kapott a becslési sor **Összeg** mezőjéhez így biztosítva, hogy a nulla értékek ne maradjanak meg.</span><span class="sxs-lookup"><span data-stu-id="db7b1-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="db7b1-128">Javítva: Ha a tényadatokat frissítették egy projekten, akkor a program a projekt fő űrlapjára megjelenik egy frissítés gomb, hogy a felhasználók újra szinkronizálhassák a tényadatokat.</span><span class="sxs-lookup"><span data-stu-id="db7b1-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="db7b1-129">Javítva: Amikor a felhasználók 2.X verzióról a 3.X verzóra a NULL projektnévértű projektek megengedettek.</span><span class="sxs-lookup"><span data-stu-id="db7b1-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>

