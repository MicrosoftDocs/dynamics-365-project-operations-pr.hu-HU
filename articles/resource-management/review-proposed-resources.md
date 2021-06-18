---
title: Javasolt erőforrások áttekintése
description: Ez a témakör információt nyújt a projekt erőforrásainak javaslatáról.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 987ea08c77c1824182856c0d52ee0cd15e7029b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000754"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="e75d1-103">Javasolt erőforrások áttekintése</span><span class="sxs-lookup"><span data-stu-id="e75d1-103">Review proposed resources</span></span>

<span data-ttu-id="e75d1-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="e75d1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e75d1-105">Az erőforrás-kezelők erőforrás-igénylés felhasználásával erőforrást javasolhatnak a projektmenedzser számára.</span><span class="sxs-lookup"><span data-stu-id="e75d1-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="e75d1-106">A kérési rácsból vagy maga a kérelemből válassza a **Források keresése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="e75d1-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="e75d1-107">Az **Ütemezési asszisztens** oldalon válassza ki az erőforrást, majd az **Erőforrás foglalás létrehozása** ablaktáblában a **Foglalási állapot** mezőben válassza a **Foglalás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="e75d1-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="e75d1-108">A következő állapotfrissítések történnek:</span><span class="sxs-lookup"><span data-stu-id="e75d1-108">The following status updates occur:</span></span>

- <span data-ttu-id="e75d1-109">Az **Ütemezési asszisztens** oldalon az állapotjelzők frissülnek, jelezve, hogy a foglalást javasolják, nem pedig keményen lefoglalják.</span><span class="sxs-lookup"><span data-stu-id="e75d1-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="e75d1-110">Az erőforrás-kérésnél az állapot megváltozik: **Áttekintést igényel**.</span><span class="sxs-lookup"><span data-stu-id="e75d1-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="e75d1-111">A projekt **Csapat** lapján az általános csapattag **Állapotkérés** értéke megváltozik **Áttekintést igényel** értékre.</span><span class="sxs-lookup"><span data-stu-id="e75d1-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="e75d1-112">A projektvezető elfogadhatja vagy elutasíthatja a javaslatot.</span><span class="sxs-lookup"><span data-stu-id="e75d1-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="e75d1-113">Amikor az erőforrás-kezelők feldolgozzák az erőforrás-kérelmeket, a következő megközelítések bármelyikét használhatják:</span><span class="sxs-lookup"><span data-stu-id="e75d1-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="e75d1-114">Javasoljon több erőforrást a kereslet kielégítésére, ha egyetlen erőforrás sem áll rendelkezésre a szükséges órák teljesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="e75d1-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="e75d1-115">A javasolt órákat ezután több forrásra osztják, amelyek kielégítik a szükséges órákat.</span><span class="sxs-lookup"><span data-stu-id="e75d1-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="e75d1-116">Ebben a forgatókönyvben az órák nem fedhetik át egymást.</span><span class="sxs-lookup"><span data-stu-id="e75d1-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="e75d1-117">Javasoljon kevesebb erőforrást a szükségesnél.</span><span class="sxs-lookup"><span data-stu-id="e75d1-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="e75d1-118">Ebben a forgatókönyvben a javasolt erőforrás-kapacitás kevesebb, mint a kérelmező által megadott szükséges óra.</span><span class="sxs-lookup"><span data-stu-id="e75d1-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="e75d1-119">Ezért, amikor a kérelmező elfogadja a javasolt erőforrásokat, nem teljesült erőforrás-követelmény jön létre a fennmaradó kereslet rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="e75d1-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="e75d1-120">Foglaljon több erőforrást a kereslet kielégítésére, ha egyetlen erőforrás sem áll rendelkezésre a munka befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="e75d1-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="e75d1-121">Foglaljon kevesebb erőforrást, mint amennyire szükség van.</span><span class="sxs-lookup"><span data-stu-id="e75d1-121">Book fewer resources than are required.</span></span> <span data-ttu-id="e75d1-122">Ebben a forgatókönyvben a foglalt órák kevesebbek, mint a szükséges órák.</span><span class="sxs-lookup"><span data-stu-id="e75d1-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="e75d1-123">A rendszer arra irányul, hogy erőforrásokat javasoljon a foglalás helyett, hogy a kérelmező ellenőrizhesse és nyomon tudja követni a fennmaradó igényeket.</span><span class="sxs-lookup"><span data-stu-id="e75d1-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="e75d1-124">Erőforrás elérhetősége</span><span class="sxs-lookup"><span data-stu-id="e75d1-124">Resource availability</span></span>

<span data-ttu-id="e75d1-125">Fontos, hogy az erőforrás-kezelők képesek legyenek megtekinteni az erőforrások rendelkezésre állását és frissíteni a foglalásokat.</span><span class="sxs-lookup"><span data-stu-id="e75d1-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="e75d1-126">Bizonyos esetekben nincs hivatalos igény (erőforrás-igény), de az erőforrás-kezelőnek válaszolnia kell egy nem tervezett igényre, amely csatornákon, például e-mailben, telefonhívásban vagy azonnali üzenetben érkezik.</span><span class="sxs-lookup"><span data-stu-id="e75d1-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="e75d1-127">Az erőforrás-kezelők az Ütemezési táblát használják az erőforrások és a foglalások frissítésére.</span><span class="sxs-lookup"><span data-stu-id="e75d1-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="e75d1-128">Az erőforrás rendelkezésre állásának kiszámításához az erőforrás munkaidőjét vesszük alapul.</span><span class="sxs-lookup"><span data-stu-id="e75d1-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="e75d1-129">Az erőforrás-foglalások felhasználják az erőforrások kapacitását.</span><span class="sxs-lookup"><span data-stu-id="e75d1-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="e75d1-130">Az Ütemezési tábla színeket és árnyalatokat használ a foglalások, a rendelkezésre állás és a túlfoglalások, valamint a foglalások állapotának megjelenítésére.</span><span class="sxs-lookup"><span data-stu-id="e75d1-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="e75d1-131">Az Ütemezési tábla beállításai lehetővé teszik a jelmagyarázat megjelenítését.</span><span class="sxs-lookup"><span data-stu-id="e75d1-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="e75d1-132">Ha egy jobbra mutató nyíl jelenik meg az ütemező táblán az egyes foglalható források mellett, az erőforrás kibővíthető, hogy megjelenjen az erőforrás által lefoglalt munka részletei.</span><span class="sxs-lookup"><span data-stu-id="e75d1-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="e75d1-133">Mivel a Dynamics 365 Project Operations a Universal Resource Scheduling motort használja, ha telepítette a Dynamics 365 Field Service rendszert is, akkor megtekintheti a projektek erőforrás-foglalási, munkamegrendelési és minden más entitás részleteit, amelyekre az ütemezést kiterjesztette.</span><span class="sxs-lookup"><span data-stu-id="e75d1-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="e75d1-134">Az egyes erőforrásokkal kapcsolatos további részletek megtekintéséhez kattintson a jobb gombbal az erőforráskártya megnyitásához.</span><span class="sxs-lookup"><span data-stu-id="e75d1-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]