---
title: Újdonságok vagy változások a Project Service Automation 26-es frissítési kiadásának V3 változatában
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643266"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="9a813-102">Project Service Automation 26-es frissítési kiadás, V3</span><span class="sxs-lookup"><span data-stu-id="9a813-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="9a813-103">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="9a813-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9a813-104">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="9a813-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9a813-105">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="9a813-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9a813-106">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="9a813-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="9a813-107">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9a813-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9a813-108">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3 26-os frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="9a813-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="9a813-109">A Build száma V 3.10.44.59, és általánosan elérhető egy önálló frissítésként 2020 decemberében.</span><span class="sxs-lookup"><span data-stu-id="9a813-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="9a813-110">26-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="9a813-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="9a813-111">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="9a813-111">Bug fixes</span></span>

<span data-ttu-id="9a813-112">**Idő és költség**</span><span class="sxs-lookup"><span data-stu-id="9a813-112">**Time and Expense**</span></span>

<span data-ttu-id="9a813-113">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="9a813-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="9a813-114">A felhasználók egy jóváhagyott/elküldött időbejegyzésen módosíthatják a feladatot.</span><span class="sxs-lookup"><span data-stu-id="9a813-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="9a813-115">Az időbejegyzés mentésekor az „Objektumhivatkozás nincs beállítva” hibaüzenet jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="9a813-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="9a813-116">Az erőforrás-hozzárendelések importálásának időrekordjainak nem megfelelő DateTime értékekkel rendelkező időbejegyzéseket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9a813-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="9a813-117">Ha a Project Service Automation és a Field Service alkalmazás egyaránt telepítve van, az **Új** gomb kétszer jelenik meg a parancssávon a Field Service alkalmazás időbejegyzéseihez.</span><span class="sxs-lookup"><span data-stu-id="9a813-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="9a813-118">Az **Egység engedélyezése** és az **Egységcsoport** cellái frissítései immár működnek **Költségbecslések** rácson.</span><span class="sxs-lookup"><span data-stu-id="9a813-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="9a813-119">**Az időtételmódosítás frissítése** űrlap tartalmaz **Idősort**.</span><span class="sxs-lookup"><span data-stu-id="9a813-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="9a813-120">A projekten kívüli időbejegyzések időjóváhagyása a projekt jóváhagyói szerepkörének keresésekor blokkolja a rendszert.</span><span class="sxs-lookup"><span data-stu-id="9a813-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="9a813-121">**Erőforráskezelés**</span><span class="sxs-lookup"><span data-stu-id="9a813-121">**Resource Management**</span></span>

<span data-ttu-id="9a813-122">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="9a813-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="9a813-123">Hozzáadott érvényesítés a **PostProjectCreate** beépülő modulban amely ellenőrzi az elsődleges követelményt, mielőtt létrehozna egyet.</span><span class="sxs-lookup"><span data-stu-id="9a813-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="9a813-124">A **Projektcsapat tagja** gyors létrehozási űrlap egy null referencia kivételt ad, ha a mezőket eltávolítja az űrlapról.</span><span class="sxs-lookup"><span data-stu-id="9a813-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="9a813-125">12 órás követelmények létrehozása egy évre vonatkozóan sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="9a813-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="9a813-126">Javított hibaüzenet null hivatkozás kivétel az erőforrásszükséglet létrehozása során.</span><span class="sxs-lookup"><span data-stu-id="9a813-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="9a813-127">**Projektmenedzsment**</span><span class="sxs-lookup"><span data-stu-id="9a813-127">**Project Management**</span></span>

<span data-ttu-id="9a813-128">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="9a813-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="9a813-129">Javított érvényesítés a **PreProjectUpdate** beépülő modulban létrejött null hivatkozásra vonatkozó kivételek kezelésére.</span><span class="sxs-lookup"><span data-stu-id="9a813-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="9a813-130">A Microsoft Project Desktop bővítmény által közzétett projektek a törlik a nem hozzárendelt megbízásokat.</span><span class="sxs-lookup"><span data-stu-id="9a813-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="9a813-131">Az új ellenőrzés hozzáadva, ha **PreValidateProjectTaskUpdate** nulla hivatkozás kivétele miatt a projekthivatkozás érvénytelen.</span><span class="sxs-lookup"><span data-stu-id="9a813-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="9a813-132">A Csapattagok rácsa nem jeleníti meg a csapattagok rekordjainak különböző hozzárendeléseit.</span><span class="sxs-lookup"><span data-stu-id="9a813-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="9a813-133">Hozzáadva egy új ellenőrzés és hibaüzenetek a **PreProjectTaskDelete** beépülő modul nullhivatkozás kivétele miatt.</span><span class="sxs-lookup"><span data-stu-id="9a813-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="9a813-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="9a813-134">**Sales**</span></span>

<span data-ttu-id="9a813-135">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="9a813-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="9a813-136">Ha egy projekten alapuló sort egy ajánlatban vagy szerződésben választ ki, akkor a **Javaslat** gomb csak akkor látható, ha egy termékalapú sort választ ki egy meglévő termékhez.</span><span class="sxs-lookup"><span data-stu-id="9a813-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="9a813-137">A **Create_Product** jogosultság le lett választva a **Create_ProjectContract** jogosultságról.</span><span class="sxs-lookup"><span data-stu-id="9a813-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="9a813-138">Egy számlasor törlése nullahivatkozás hibát okoz **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice** elemnél.</span><span class="sxs-lookup"><span data-stu-id="9a813-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
