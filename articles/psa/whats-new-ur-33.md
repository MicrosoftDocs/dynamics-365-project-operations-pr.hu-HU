---
title: Újdonságok vagy változások a Project Service Automation 33-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 33-os frissítési kiadásában.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334551"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="ccd68-103">Újdonságok vagy változások a Project Service Automation 33-es frissítési kiadásának V3 változatában</span><span class="sxs-lookup"><span data-stu-id="ccd68-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ccd68-104">Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését.</span><span class="sxs-lookup"><span data-stu-id="ccd68-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="ccd68-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="ccd68-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ccd68-106">Kompatibilis a Dynamics 365 9.x rendszerrel.</span><span class="sxs-lookup"><span data-stu-id="ccd68-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ccd68-107">A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést.</span><span class="sxs-lookup"><span data-stu-id="ccd68-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="ccd68-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ccd68-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ccd68-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 33-es frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="ccd68-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="ccd68-110">Ennek a verziónak a buldszáma V3.10.54.98, és általánosan elérhető 2021. júliusában önálló frissítésen keresztül.</span><span class="sxs-lookup"><span data-stu-id="ccd68-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="ccd68-111">33-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="ccd68-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ccd68-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="ccd68-112">Bug fixes</span></span>

<span data-ttu-id="ccd68-113">**Idő és költség**</span><span class="sxs-lookup"><span data-stu-id="ccd68-113">**Time and Expense**</span></span>

<span data-ttu-id="ccd68-114">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="ccd68-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="ccd68-115">Két zárolt mező, az **msdyn_description** és az **msdyn_externaldescription** szerkeszthető az elküldés után.</span><span class="sxs-lookup"><span data-stu-id="ccd68-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="ccd68-116">Hibaüzenet jelenik meg, ha olyan költség jön létre, amely nem kapcsolódik projekthez.</span><span class="sxs-lookup"><span data-stu-id="ccd68-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="ccd68-117">Időbejegyzés létrehozásakor az erőforrás szerepköre alapértelmezetten egy inaktív szerepkörre vált.</span><span class="sxs-lookup"><span data-stu-id="ccd68-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="ccd68-118">A rendszer nem távolítja el a visszahívott és nem törölt kiadásokhoz társított naplósorokat.</span><span class="sxs-lookup"><span data-stu-id="ccd68-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="ccd68-119">Az **Időbeviteli gyorslétrehozási űrlapon** módosítsa a **Projektfeladat-lista** nézetét, hogy az alapértelmezetten megjelenített dátumot a feladat kezdő dátumára váltsa.</span><span class="sxs-lookup"><span data-stu-id="ccd68-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="ccd68-120">Ha a foglalható erőforrás **Kapcsolódó** lapján hoz létre időbejegyzést, a fölérendelt foglalható erőforrás helyett helytelenül a bejelentkezett felhasználóhoz jön létre az időbejegyzés.</span><span class="sxs-lookup"><span data-stu-id="ccd68-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="ccd68-121">Az új mezőket a rendszer hozzáadja a **Tömeges jóváhagyású MDD** párbeszédpanelhez.</span><span class="sxs-lookup"><span data-stu-id="ccd68-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="ccd68-122">**Projekt tervezése**</span><span class="sxs-lookup"><span data-stu-id="ccd68-122">**Project planning**</span></span>

<span data-ttu-id="ccd68-123">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="ccd68-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="ccd68-124">Lassítja a projektek létrehozását, ha összetett naptárakat alkalmaz a projekt munkaóra-sablonokhoz.</span><span class="sxs-lookup"><span data-stu-id="ccd68-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="ccd68-125">Ha a kezdő dátum nagyobb a záró dátumnál, a mezők időösszetevői közötti különbség miatt hiba jelenik meg a projektsablon másolásakor.</span><span class="sxs-lookup"><span data-stu-id="ccd68-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="ccd68-126">**Erőforrás-kezelés**</span><span class="sxs-lookup"><span data-stu-id="ccd68-126">**Resource management**</span></span>

<span data-ttu-id="ccd68-127">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="ccd68-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="ccd68-128">Az erőforrás-felhasználás lekérdezésben helytelen paraméter van használva, és az XML helytelen szűrési eredményekhez vezet az **Erőforrás-felhasználás** rácsban.</span><span class="sxs-lookup"><span data-stu-id="ccd68-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="ccd68-129">A **Foglalások meghosszabbítása** jóváhagyás helytelen záró dátumot jelenít meg a foglalásokhoz.</span><span class="sxs-lookup"><span data-stu-id="ccd68-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="ccd68-130">**Értékesítés**</span><span class="sxs-lookup"><span data-stu-id="ccd68-130">**Sales**</span></span>

<span data-ttu-id="ccd68-131">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="ccd68-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="ccd68-132">Hibaüzenet jelenik meh, ha egy kategóriaárat hiányzó értékekkel hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="ccd68-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="ccd68-133">Hibaüzenet jelenik meg, ha a szerződéssor mérföldkövét megrendeléssor nélkül hozzák létre.</span><span class="sxs-lookup"><span data-stu-id="ccd68-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
