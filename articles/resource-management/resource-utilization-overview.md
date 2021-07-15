---
title: Erőforrás-kihasználtság áttekintése
description: Ez a témakör információkat nyújt az erőforrás-kihasználtságról a Project Operations alkalmazásban.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: c9464b1de87211f8317a39a1d749e619769309ae
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367939"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="6ecba-103">Erőforrás-kihasználtság áttekintése</span><span class="sxs-lookup"><span data-stu-id="6ecba-103">Resource utilization overview</span></span>

<span data-ttu-id="6ecba-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="6ecba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6ecba-105">Az erőforrások megcélozhatók számlázható felhasználással.</span><span class="sxs-lookup"><span data-stu-id="6ecba-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="6ecba-106">Ezt a célfelhasználást a rendszer egy erőforrás alapértelmezett szerepének attribútumaként határozza meg, vagy beállítja az egyes foglalható erőforrások rekordjában.</span><span class="sxs-lookup"><span data-stu-id="6ecba-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="6ecba-107">A hasznosítási számítások azon tényleges órákon alapulnak, amelyeket az erőforrások jóváhagyott időbejegyzésekkel jelentettek.</span><span class="sxs-lookup"><span data-stu-id="6ecba-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="6ecba-108">A felhasználás kiszámításához a következő képleteket kell használni:</span><span class="sxs-lookup"><span data-stu-id="6ecba-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="6ecba-109">Számlázható felhasználás = Számlázható tényleges óra ÷ Erőforrás-kapacitás</span><span class="sxs-lookup"><span data-stu-id="6ecba-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="6ecba-110">Nem számlázható felhasználás = Tényleges idő számlaszám-azonosítóval = Nem terhelhető, kiegészítő vagy nem elérhető ÷ Erőforrás-kapacitás</span><span class="sxs-lookup"><span data-stu-id="6ecba-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="6ecba-111">Belső = Valós idő eladási szerződés nélkül ÷ Erőforrás-kapacitás</span><span class="sxs-lookup"><span data-stu-id="6ecba-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="6ecba-112">Erőforrás-kapacitás = Erőforrás-munkaidő - Irodán kívüli - Nem munkanapok</span><span class="sxs-lookup"><span data-stu-id="6ecba-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="6ecba-113">Az **Erőforrás-hasznosítás** nézetet az **Erőforrások** ablaktáblában találhatja meg.</span><span class="sxs-lookup"><span data-stu-id="6ecba-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="6ecba-114">A rács minden cellája képviseli az erőforrás számlázható felhasználási százalékát egy időszakban, például egy nap, hét vagy hónap.</span><span class="sxs-lookup"><span data-stu-id="6ecba-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="6ecba-115">A cellák színezésére a következő képleteket használják:</span><span class="sxs-lookup"><span data-stu-id="6ecba-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="6ecba-116">**Zöld**: Számlázható kihasználtság >= Erőforrás cél kihasználtsága</span><span class="sxs-lookup"><span data-stu-id="6ecba-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="6ecba-117">**Sárga**: Cél kihasználtság – 20 <= Számlázható kihasználtság < Célkihasználtság</span><span class="sxs-lookup"><span data-stu-id="6ecba-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="6ecba-118">**Piros**: Számlázható kihasználtság < Célkihasználtság – 20</span><span class="sxs-lookup"><span data-stu-id="6ecba-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="6ecba-119">Mivel az **Erőforrás-hasznosítás** nézet az Ütemezési táblán alapul, az Ütemezési tábla szűrési képességeit használhatja az eredmények szűrésére.</span><span class="sxs-lookup"><span data-stu-id="6ecba-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="6ecba-120">A rács megköveteli, hogy állítson be egy célfelhasználást a szerepre vagy az egyes erőforrásokra.</span><span class="sxs-lookup"><span data-stu-id="6ecba-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="6ecba-121">A beállítás elvégzéséhez ugorjon az **Erőforrások** > **Erőforrásszerepek** elemre.</span><span class="sxs-lookup"><span data-stu-id="6ecba-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="6ecba-122">Ezenkívül minden foglalható erőforráshoz alapértelmezett szerepet kell hozzárendelni.</span><span class="sxs-lookup"><span data-stu-id="6ecba-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="6ecba-123">Lépjen az **Erőforrások** > **Erőforrások** oldalra.</span><span class="sxs-lookup"><span data-stu-id="6ecba-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="6ecba-124">A **Project Service** lapon ellenőrizze, hogy az erőforrás szerepe van meghatározva, és hogy a **Alapértelmezett** mező **Igen** értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="6ecba-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="6ecba-125">További szerepeket adhat hozzá, ahol **Alapértelmezett** = **Nem**.</span><span class="sxs-lookup"><span data-stu-id="6ecba-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="6ecba-126">A szerep, ahol az **Alapértelmezett** = **Igen**, az erőforrás felhasználásának értékelésére szolgál annak a célnak a függvényében.</span><span class="sxs-lookup"><span data-stu-id="6ecba-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="6ecba-127">A **Project Service** lapon az erőforrás egyedi célhasználatát is beállíthatja.</span><span class="sxs-lookup"><span data-stu-id="6ecba-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="6ecba-128">A hasznosítási számítás ezt követően a célfelhasználást használja az erőforrás céljának értékelésére, az erőforrás alapértelmezett szerepének célpontja helyett.</span><span class="sxs-lookup"><span data-stu-id="6ecba-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="6ecba-129">Az erőforrás felhasználása csak akkor jelenik meg, ha az erőforrás jóváhagyott, díjköteles időt mutat a rácson megjelenített időszakban.</span><span class="sxs-lookup"><span data-stu-id="6ecba-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]