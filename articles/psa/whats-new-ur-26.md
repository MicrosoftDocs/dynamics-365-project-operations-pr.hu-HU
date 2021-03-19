---
title: Újdonságok vagy változások a Project Service Automation 26-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 26-os frissítési kiadásában.
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
ms.openlocfilehash: 135f017533705e165230ac994d217ad7c58bab10
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280401"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="0cefe-103">Project Service Automation 26-es frissítési kiadás, V3</span><span class="sxs-lookup"><span data-stu-id="0cefe-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0cefe-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="0cefe-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="0cefe-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="0cefe-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="0cefe-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="0cefe-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0cefe-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="0cefe-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="0cefe-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="0cefe-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="0cefe-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3 26-os frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="0cefe-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="0cefe-110">A Build száma V 3.10.44.59, és általánosan elérhető egy önálló frissítésként 2020 decemberében.</span><span class="sxs-lookup"><span data-stu-id="0cefe-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="0cefe-111">26-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="0cefe-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="0cefe-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="0cefe-112">Bug fixes</span></span>

<span data-ttu-id="0cefe-113">**Idő és költség**</span><span class="sxs-lookup"><span data-stu-id="0cefe-113">**Time and Expense**</span></span>

<span data-ttu-id="0cefe-114">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="0cefe-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="0cefe-115">A felhasználók egy jóváhagyott/elküldött időbejegyzésen módosíthatják a feladatot.</span><span class="sxs-lookup"><span data-stu-id="0cefe-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="0cefe-116">Az időbejegyzés mentésekor az „Objektumhivatkozás nincs beállítva” hibaüzenet jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="0cefe-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="0cefe-117">Az erőforrás-hozzárendelések importálásának időrekordjainak nem megfelelő DateTime értékekkel rendelkező időbejegyzéseket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0cefe-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="0cefe-118">Ha a Project Service Automation és a Field Service alkalmazás egyaránt telepítve van, az **Új** gomb kétszer jelenik meg a parancssávon a Field Service alkalmazás időbejegyzéseihez.</span><span class="sxs-lookup"><span data-stu-id="0cefe-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="0cefe-119">Az **Egység engedélyezése** és az **Egységcsoport** cellái frissítései immár működnek **Költségbecslések** rácson.</span><span class="sxs-lookup"><span data-stu-id="0cefe-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="0cefe-120">**Az időtételmódosítás frissítése** űrlap tartalmaz **Idősort**.</span><span class="sxs-lookup"><span data-stu-id="0cefe-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="0cefe-121">A projekten kívüli időbejegyzések időjóváhagyása a projekt jóváhagyói szerepkörének keresésekor blokkolja a rendszert.</span><span class="sxs-lookup"><span data-stu-id="0cefe-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="0cefe-122">**Erőforráskezelés**</span><span class="sxs-lookup"><span data-stu-id="0cefe-122">**Resource Management**</span></span>

<span data-ttu-id="0cefe-123">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="0cefe-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="0cefe-124">Hozzáadott érvényesítés a **PostProjectCreate** beépülő modulban amely ellenőrzi az elsődleges követelményt, mielőtt létrehozna egyet.</span><span class="sxs-lookup"><span data-stu-id="0cefe-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="0cefe-125">A **Projektcsapat tagja** gyors létrehozási űrlap egy null referencia kivételt ad, ha a mezőket eltávolítja az űrlapról.</span><span class="sxs-lookup"><span data-stu-id="0cefe-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="0cefe-126">12 órás követelmények létrehozása egy évre vonatkozóan sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="0cefe-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="0cefe-127">Javított hibaüzenet null hivatkozás kivétel az erőforrásszükséglet létrehozása során.</span><span class="sxs-lookup"><span data-stu-id="0cefe-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="0cefe-128">**Projektmenedzsment**</span><span class="sxs-lookup"><span data-stu-id="0cefe-128">**Project Management**</span></span>

<span data-ttu-id="0cefe-129">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="0cefe-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="0cefe-130">Javított érvényesítés a **PreProjectUpdate** beépülő modulban létrejött null hivatkozásra vonatkozó kivételek kezelésére.</span><span class="sxs-lookup"><span data-stu-id="0cefe-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="0cefe-131">A Microsoft Project Desktop bővítmény által közzétett projektek a törlik a nem hozzárendelt megbízásokat.</span><span class="sxs-lookup"><span data-stu-id="0cefe-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="0cefe-132">Az új ellenőrzés hozzáadva, ha **PreValidateProjectTaskUpdate** nulla hivatkozás kivétele miatt a projekthivatkozás érvénytelen.</span><span class="sxs-lookup"><span data-stu-id="0cefe-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="0cefe-133">A Csapattagok rácsa nem jeleníti meg a csapattagok rekordjainak különböző hozzárendeléseit.</span><span class="sxs-lookup"><span data-stu-id="0cefe-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="0cefe-134">Hozzáadva egy új ellenőrzés és hibaüzenetek a **PreProjectTaskDelete** beépülő modul nullhivatkozás kivétele miatt.</span><span class="sxs-lookup"><span data-stu-id="0cefe-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="0cefe-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="0cefe-135">**Sales**</span></span>

<span data-ttu-id="0cefe-136">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="0cefe-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="0cefe-137">Ha egy projekten alapuló sort egy ajánlatban vagy szerződésben választ ki, akkor a **Javaslat** gomb csak akkor látható, ha egy termékalapú sort választ ki egy meglévő termékhez.</span><span class="sxs-lookup"><span data-stu-id="0cefe-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="0cefe-138">A **Create_Product** jogosultság le lett választva a **Create_ProjectContract** jogosultságról.</span><span class="sxs-lookup"><span data-stu-id="0cefe-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="0cefe-139">Egy számlasor törlése nullahivatkozás hibát okoz **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice** elemnél.</span><span class="sxs-lookup"><span data-stu-id="0cefe-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]