---
title: Javasolt erőforrások áttekintése
description: Ez a témakör információt nyújt a projekt erőforrásainak javaslatáról.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078059"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="1e91a-103">Javasolt erőforrások áttekintése</span><span class="sxs-lookup"><span data-stu-id="1e91a-103">Review proposed resources</span></span>

<span data-ttu-id="1e91a-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="1e91a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1e91a-105">Az erőforrás-kezelők erőforrás-igénylés felhasználásával erőforrást javasolhatnak a projektmenedzser számára.</span><span class="sxs-lookup"><span data-stu-id="1e91a-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="1e91a-106">A kérési rácsból vagy maga a kérelemből válassza a **Források keresése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1e91a-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="1e91a-107">Az **Ütemezési asszisztens** oldalon válassza ki az erőforrást, majd az **Erőforrás foglalás létrehozása** ablaktáblában a **Foglalási állapot** mezőben válassza a **Foglalás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1e91a-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="1e91a-108">A következő állapotfrissítések történnek:</span><span class="sxs-lookup"><span data-stu-id="1e91a-108">The following status updates occur:</span></span>

- <span data-ttu-id="1e91a-109">Az **Ütemezési asszisztens** oldalon az állapotjelzők frissülnek, jelezve, hogy a foglalást javasolják, nem pedig keményen lefoglalják.</span><span class="sxs-lookup"><span data-stu-id="1e91a-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="1e91a-110">Az erőforrás-kérésnél az állapot megváltozik: **Áttekintést igényel**.</span><span class="sxs-lookup"><span data-stu-id="1e91a-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="1e91a-111">A projekt **Csapat** lapján az általános csapattag **Állapotkérés** értéke megváltozik **Áttekintést igényel** értékre.</span><span class="sxs-lookup"><span data-stu-id="1e91a-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="1e91a-112">A projektvezető elfogadhatja vagy elutasíthatja a javaslatot.</span><span class="sxs-lookup"><span data-stu-id="1e91a-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="1e91a-113">Amikor az erőforrás-kezelők feldolgozzák az erőforrás-kérelmeket, a következő megközelítések bármelyikét használhatják:</span><span class="sxs-lookup"><span data-stu-id="1e91a-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="1e91a-114">Javasoljon több erőforrást a kereslet kielégítésére, ha egyetlen erőforrás sem áll rendelkezésre a szükséges órák teljesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="1e91a-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="1e91a-115">A javasolt órákat ezután több forrásra osztják, amelyek kielégítik a szükséges órákat.</span><span class="sxs-lookup"><span data-stu-id="1e91a-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="1e91a-116">Ebben a forgatókönyvben az órák nem fedhetik át egymást.</span><span class="sxs-lookup"><span data-stu-id="1e91a-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="1e91a-117">Javasoljon kevesebb erőforrást a szükségesnél.</span><span class="sxs-lookup"><span data-stu-id="1e91a-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="1e91a-118">Ebben a forgatókönyvben a javasolt erőforrás-kapacitás kevesebb, mint a kérelmező által megadott szükséges óra.</span><span class="sxs-lookup"><span data-stu-id="1e91a-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="1e91a-119">Ezért, amikor a kérelmező elfogadja a javasolt erőforrásokat, nem teljesült erőforrás-követelmény jön létre a fennmaradó kereslet rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="1e91a-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="1e91a-120">Foglaljon több erőforrást a kereslet kielégítésére, ha egyetlen erőforrás sem áll rendelkezésre a munka befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="1e91a-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="1e91a-121">Foglaljon kevesebb erőforrást, mint amennyire szükség van.</span><span class="sxs-lookup"><span data-stu-id="1e91a-121">Book fewer resources than are required.</span></span> <span data-ttu-id="1e91a-122">Ebben a forgatókönyvben a foglalt órák kevesebbek, mint a szükséges órák.</span><span class="sxs-lookup"><span data-stu-id="1e91a-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="1e91a-123">A rendszer arra irányul, hogy erőforrásokat javasoljon a foglalás helyett, hogy a kérelmező ellenőrizhesse és nyomon tudja követni a fennmaradó igényeket.</span><span class="sxs-lookup"><span data-stu-id="1e91a-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="1e91a-124">Számlázható felhasználás</span><span class="sxs-lookup"><span data-stu-id="1e91a-124">Billable utilization</span></span>

<span data-ttu-id="1e91a-125">Az erőforrások megcélozhatók számlázható felhasználással.</span><span class="sxs-lookup"><span data-stu-id="1e91a-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="1e91a-126">Ezt a célfelhasználást vagy határozza meg egy erőforrás alapértelmezett szerepének attribútumaként, vagy beállítja az egyes foglalható erőforrások rekordjában.</span><span class="sxs-lookup"><span data-stu-id="1e91a-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="1e91a-127">A hasznosítási számítások azon tényleges órákon alapulnak, amelyeket az erőforrások jóváhagyott időbejegyzésekkel jelentettek.</span><span class="sxs-lookup"><span data-stu-id="1e91a-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="1e91a-128">A felhasználás kiszámításához a következő képleteket kell használni:</span><span class="sxs-lookup"><span data-stu-id="1e91a-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="1e91a-129">Számlázható felhasználás = Számlázható tényleges óra ÷ Erőforrás-kapacitás</span><span class="sxs-lookup"><span data-stu-id="1e91a-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="1e91a-130">Nem számlázható felhasználás = Tényleges idő számlaszám-azonosítóval = Nem terhelhető, kiegészítő vagy nem elérhető ÷ Erőforrás-kapacitás</span><span class="sxs-lookup"><span data-stu-id="1e91a-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="1e91a-131">Belső = Valós idő eladási szerződés nélkül ÷ Erőforrás-kapacitás</span><span class="sxs-lookup"><span data-stu-id="1e91a-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="1e91a-132">Erőforrás-kapacitás = Erőforrás-munkaidő - Irodán kívüli - Nem munkanapok</span><span class="sxs-lookup"><span data-stu-id="1e91a-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="1e91a-133">Az **Erőforrás-hasznosítás** nézetet az **Erőforrások** ablaktáblában találhatja meg.</span><span class="sxs-lookup"><span data-stu-id="1e91a-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="1e91a-134">A rács minden cellája képviseli az erőforrás számlázható felhasználási százalékát egy időszakban, például egy nap, hét vagy hónap.</span><span class="sxs-lookup"><span data-stu-id="1e91a-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="1e91a-135">A cellák színezésére a következő képleteket használják:</span><span class="sxs-lookup"><span data-stu-id="1e91a-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="1e91a-136">**Zöld:** Számlázható felhasználás \>= Erőforrás célfelhasználás</span><span class="sxs-lookup"><span data-stu-id="1e91a-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="1e91a-137">**Sárga:** Célfelhasználás - 20 \<= Számlázható felhasználás \< Célfelhasználás</span><span class="sxs-lookup"><span data-stu-id="1e91a-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="1e91a-138">**Piros:** Számlázható felhasználás \< Célfelhasználás - 20</span><span class="sxs-lookup"><span data-stu-id="1e91a-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="1e91a-139">Mivel az **Erőforrás-hasznosítás** nézet az Ütemezési táblán alapul, az Ütemezési tábla szűrési képességeit használhatja az eredmények szűrésére.</span><span class="sxs-lookup"><span data-stu-id="1e91a-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="1e91a-140">A rács megköveteli, hogy állítson be egy célfelhasználást a szerepre vagy az egyes erőforrásokra.</span><span class="sxs-lookup"><span data-stu-id="1e91a-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="1e91a-141">A beállítás elvégzéséhez ugorjon a **Erőforrások** \> **Erőforrás szerepek** elemre.</span><span class="sxs-lookup"><span data-stu-id="1e91a-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="1e91a-142">Ezenkívül minden foglalható erőforráshoz alapértelmezett szerepet kell hozzárendelni.</span><span class="sxs-lookup"><span data-stu-id="1e91a-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="1e91a-143">Lépjen a **Források** \> **Források** oldalra.</span><span class="sxs-lookup"><span data-stu-id="1e91a-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="1e91a-144">A **Project Service** lapon ellenőrizze, hogy az erőforrás szerepe van meghatározva, és hogy a **Alapértelmezett** mező **Igen** értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="1e91a-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="1e91a-145">További szerepeket adhat hozzá, ahol **Alapértelmezett = Nem**.</span><span class="sxs-lookup"><span data-stu-id="1e91a-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="1e91a-146">A szerep, ahol az **Alapértelmezett = Igen** , az erőforrás felhasználásának értékelésére szolgál annak a célnak a függvényében.</span><span class="sxs-lookup"><span data-stu-id="1e91a-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="1e91a-147">A **Project Service** lapon az erőforrás egyedi célhasználatát is beállíthatja.</span><span class="sxs-lookup"><span data-stu-id="1e91a-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="1e91a-148">A hasznosítási számítás ezt követően a célfelhasználást használja az erőforrás céljának értékelésére, az erőforrás alapértelmezett szerepének célpontja helyett.</span><span class="sxs-lookup"><span data-stu-id="1e91a-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="1e91a-149">Az erőforrás felhasználása csak akkor jelenik meg, ha az erőforrás jóváhagyott, díjköteles időt mutat a rácson megjelenített időszakban.</span><span class="sxs-lookup"><span data-stu-id="1e91a-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="1e91a-150">Erőforrás elérhetősége</span><span class="sxs-lookup"><span data-stu-id="1e91a-150">Resource availability</span></span>

<span data-ttu-id="1e91a-151">Fontos, hogy az erőforrás-kezelők képesek legyenek megtekinteni az erőforrások rendelkezésre állását és frissíteni a foglalásokat.</span><span class="sxs-lookup"><span data-stu-id="1e91a-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="1e91a-152">Bizonyos esetekben nincs hivatalos igény (erőforrás-igény), de az erőforrás-kezelőnek válaszolnia kell egy nem tervezett igényre, amely csatornákon, például e-mailben, telefonhívásban vagy azonnali üzenetben érkezik.</span><span class="sxs-lookup"><span data-stu-id="1e91a-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="1e91a-153">Az erőforrás-kezelők az Ütemezési táblát használják az erőforrások és a foglalások frissítésére.</span><span class="sxs-lookup"><span data-stu-id="1e91a-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="1e91a-154">Az erőforrás rendelkezésre állásának kiszámításához az erőforrás munkaidőjét vesszük alapul.</span><span class="sxs-lookup"><span data-stu-id="1e91a-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="1e91a-155">Az erőforrás-foglalások felhasználják az erőforrások kapacitását.</span><span class="sxs-lookup"><span data-stu-id="1e91a-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="1e91a-156">Az Ütemezési tábla színeket és árnyalatokat használ a foglalások, a rendelkezésre állás és a túlfoglalások, valamint a foglalások állapotának megjelenítésére.</span><span class="sxs-lookup"><span data-stu-id="1e91a-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="1e91a-157">Az Ütemezési tábla beállításai lehetővé teszik a jelmagyarázat megjelenítését.</span><span class="sxs-lookup"><span data-stu-id="1e91a-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="1e91a-158">Ha egy jobbra mutató nyíl jelenik meg az ütemező táblán az egyes foglalható források mellett, az erőforrás kibővíthető, hogy megjelenjen az erőforrás által lefoglalt munka részletei.</span><span class="sxs-lookup"><span data-stu-id="1e91a-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="1e91a-159">Mivel a Dynamics 365 Project Operations a Universal Resource Scheduling-motort használja, ha telepítette a Dynamics 365 Field Service rendszert is, akkor megtekintheti a projektek erőforrás-foglalási és munkarendelési részleteit, illetve minden olyan más entitás részleteit, amelyekre kiterjesztette az ütemezést.</span><span class="sxs-lookup"><span data-stu-id="1e91a-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="1e91a-160">Az egyes erőforrásokkal kapcsolatos további részletek megtekintéséhez kattintson a jobb gombbal az erőforráskártya megnyitásához.</span><span class="sxs-lookup"><span data-stu-id="1e91a-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

