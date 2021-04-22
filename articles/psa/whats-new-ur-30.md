---
title: Újdonságok vagy változások a Project Service Automation 30-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 30-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852861"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="c819a-103">Újdonságok vagy változások a Project Service Automation 30-es frissítési kiadásának V3 változatában</span><span class="sxs-lookup"><span data-stu-id="c819a-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c819a-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="c819a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="c819a-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="c819a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c819a-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="c819a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c819a-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="c819a-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="c819a-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="c819a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c819a-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 30-es frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="c819a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="c819a-110">A verzió build száma V3.10.51.61, és általánosan elérhető lesz önálló frissítésként 2021 áprilisában.</span><span class="sxs-lookup"><span data-stu-id="c819a-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="c819a-111">30-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="c819a-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c819a-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="c819a-112">Bug fixes</span></span>

<span data-ttu-id="c819a-113">**Idő és költség**</span><span class="sxs-lookup"><span data-stu-id="c819a-113">**Time and Expense**</span></span>

<span data-ttu-id="c819a-114">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="c819a-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="c819a-115">Hiba történik, ha időbejegyzést hoz létre és ment el a **Gyorslétrehozási** lapon, miközben a **Szerepkör** mező el van távolítva.</span><span class="sxs-lookup"><span data-stu-id="c819a-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="c819a-116">Az Időbejegyzési szűrő nem a megfelelő szűrőoperátort alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="c819a-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="c819a-117">A másolt munkaidő-nyilvántartások nem jelennek meg automatikusan, amikor az időbejegyzés vezérlőjén a **Hét másolása** lehetőséget választja ki.</span><span class="sxs-lookup"><span data-stu-id="c819a-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="c819a-118">**Erőforráskezelés**</span><span class="sxs-lookup"><span data-stu-id="c819a-118">**Resource Management**</span></span>

<span data-ttu-id="c819a-119">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="c819a-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="c819a-120">Ha meghosszabbít egy foglalást, akkor a kemény foglaláshoz rendelt foglalási állapot helytelen.</span><span class="sxs-lookup"><span data-stu-id="c819a-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="c819a-121">A foglalás kiterjesztése tiszteletben tartja a foglalási beállítás metaadataiban **Lekötöttként** meghatározott foglalási állapotot.</span><span class="sxs-lookup"><span data-stu-id="c819a-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="c819a-122">Ha nincs megadva érvényes foglalási állapot, a hibaüzenet nem lesz megfelelően lokalizálva.</span><span class="sxs-lookup"><span data-stu-id="c819a-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="c819a-123">**Projektmenedzsment**</span><span class="sxs-lookup"><span data-stu-id="c819a-123">**Project Management**</span></span>

<span data-ttu-id="c819a-124">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="c819a-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="c819a-125">A projektek nem hozhatók létre az egyik pénznemben, és nem tartalmazzák a kapcsolódó tevékenységeket egy másik pénznemben.</span><span class="sxs-lookup"><span data-stu-id="c819a-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="c819a-126">**Értékesítés**</span><span class="sxs-lookup"><span data-stu-id="c819a-126">**Sales**</span></span>

<span data-ttu-id="c819a-127">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="c819a-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="c819a-128">Árlista másolásakor az árak nem frissülnek.</span><span class="sxs-lookup"><span data-stu-id="c819a-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="c819a-129">Az árajánlat megnyertként való lezárása nem sikerül, ha a költségrészletnek van egy eredeti értéke.</span><span class="sxs-lookup"><span data-stu-id="c819a-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="c819a-130">A **Projektfeladat** entitáson a **Becsült költség** át lett nevezve **Tervezett költség (Alap)** értékre.</span><span class="sxs-lookup"><span data-stu-id="c819a-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="c819a-131">A számlák létrehozásakor vagy törlésekor null értékű hivatkozáskivétel jön létre.</span><span class="sxs-lookup"><span data-stu-id="c819a-131">A null reference exception is generated when invoices are created or deleted.</span></span>
