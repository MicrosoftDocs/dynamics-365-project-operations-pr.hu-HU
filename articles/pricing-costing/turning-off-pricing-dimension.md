---
title: Árképzési dimenzió kikapcsolása
description: Ez a témakör az árképzési dimenziók kikapcsolásáról nyújt információkat.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 7b7c1d1b3363c0d158fcf6fda532822354b852a3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004534"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="b03d8-103">Árképzési dimenzió kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="b03d8-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="b03d8-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="b03d8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b03d8-105">Előfordulhat, hogy néhány évente felül kell vizsgálnia és frissítenie kell az árképzési stratégiát.</span><span class="sxs-lookup"><span data-stu-id="b03d8-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="b03d8-106">A frissítések elvégzéséhez szükség lehet egy meglévő árazási dimenzió kikapcsolására és egy új létrehozására.</span><span class="sxs-lookup"><span data-stu-id="b03d8-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="b03d8-107">Például előfordulhat, hogy korábban a **Szerep** árát határozta meg, de most úgy döntött, hogy az **Munkakörnyezet** szerinti árat határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b03d8-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="b03d8-108">Ehhez szükség lehet a **Szerep** árképzési dimenzió kikapcsolására és a **Munkakörnyezet** új árképzési dimenzió létrehozására.</span><span class="sxs-lookup"><span data-stu-id="b03d8-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="b03d8-109">Árképzési dimenzió kikapcsolása, függetlenül attól, hogy kész vagy egyéni, lehetséges a **Költségre vonatkozó** és **Értékesítésre vonatkozó** mezők **Nem**-re állításával.</span><span class="sxs-lookup"><span data-stu-id="b03d8-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="b03d8-110">Ekkor azonban a hibaüzenet jelenhet meg: **Az árképzési dimenzió nem frissíthető és nem törölhető, ha vannak társított árképzési rekordok vannak.**</span><span class="sxs-lookup"><span data-stu-id="b03d8-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Üzleti folyamat hiba valószínűsíthető, amikor kikapcsolja az árképzési dimenziót](media/Business-Process-Error.png)

<span data-ttu-id="b03d8-112">Ez a hibaüzenet azt jelzi, hogy vannak árrekordok, amelyeket korábban beállítottak a kikapcsolt dimenzióhoz.</span><span class="sxs-lookup"><span data-stu-id="b03d8-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="b03d8-113">Az összes **Szerepár** és **Szerep felár** rekordot, amely egy dimenzióra utal, törölni kell, mielőtt a dimenzió alkalmazhatóságát **Nem** értékre lehet állítani.</span><span class="sxs-lookup"><span data-stu-id="b03d8-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="b03d8-114">Ez a szabály vonatkozik mind a beépített árképzési dimenziókra, mind az esetlegesen létrehozott egyedi árképzési dimenziókra.</span><span class="sxs-lookup"><span data-stu-id="b03d8-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="b03d8-115">Erre az ellenőrzésre azért van szükség, mert minden **Szerepár** rekordnak egyedi dimenziókombinációval kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="b03d8-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="b03d8-116">Például az **US Cost Rates 2018** nevű árlistán a következő **Szerepár** sorok vannak.</span><span class="sxs-lookup"><span data-stu-id="b03d8-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="b03d8-117">Normál cím</span><span class="sxs-lookup"><span data-stu-id="b03d8-117">Standard Title</span></span>         | <span data-ttu-id="b03d8-118">Szerv. egység</span><span class="sxs-lookup"><span data-stu-id="b03d8-118">Org Unit</span></span>    |<span data-ttu-id="b03d8-119">Kiszerelés</span><span class="sxs-lookup"><span data-stu-id="b03d8-119">Unit</span></span>   |<span data-ttu-id="b03d8-120">Ár</span><span class="sxs-lookup"><span data-stu-id="b03d8-120">Price</span></span>  |<span data-ttu-id="b03d8-121">Pénznem</span><span class="sxs-lookup"><span data-stu-id="b03d8-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="b03d8-122">Rendszermérnök</span><span class="sxs-lookup"><span data-stu-id="b03d8-122">Systems Engineer</span></span>|<span data-ttu-id="b03d8-123">Contoso US</span><span class="sxs-lookup"><span data-stu-id="b03d8-123">Contoso US</span></span>|<span data-ttu-id="b03d8-124">Óra</span><span class="sxs-lookup"><span data-stu-id="b03d8-124">Hour</span></span>| <span data-ttu-id="b03d8-125">100</span><span class="sxs-lookup"><span data-stu-id="b03d8-125">100</span></span>|<span data-ttu-id="b03d8-126">USD</span><span class="sxs-lookup"><span data-stu-id="b03d8-126">USD</span></span>|
| <span data-ttu-id="b03d8-127">Vezető rendszermérnök</span><span class="sxs-lookup"><span data-stu-id="b03d8-127">Senior Systems Engineer</span></span>|<span data-ttu-id="b03d8-128">Contoso US</span><span class="sxs-lookup"><span data-stu-id="b03d8-128">Contoso US</span></span>|<span data-ttu-id="b03d8-129">Óra</span><span class="sxs-lookup"><span data-stu-id="b03d8-129">Hour</span></span>| <span data-ttu-id="b03d8-130">150</span><span class="sxs-lookup"><span data-stu-id="b03d8-130">150</span></span>| <span data-ttu-id="b03d8-131">USD</span><span class="sxs-lookup"><span data-stu-id="b03d8-131">USD</span></span>|


<span data-ttu-id="b03d8-132">Ha kikapcsolja a **Normál cím** árképzési dimenziót, és az árképzési motor árat keres, akkor a bemeneti környezetből csak a **Szerv. egység** értéket fogja használni.</span><span class="sxs-lookup"><span data-stu-id="b03d8-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="b03d8-133">Ha a bemeneti kontextus **Szervezeti egysége** a „Contoso US”, az eredmény nem lesz meghatározó, hiszen mindkét sor egyezik.</span><span class="sxs-lookup"><span data-stu-id="b03d8-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="b03d8-134">Ennek elkerülése érdekében, amikor **Szerepár** rekordokat hoz létre, a rendszer ellenőrzi, hogy a dimenziók kombinációja egyedi-e.</span><span class="sxs-lookup"><span data-stu-id="b03d8-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="b03d8-135">Ha a dimenziót a **Szerepár** rekordok létrehozása után kikapcsolják, ez a korlátozás megsérthető.</span><span class="sxs-lookup"><span data-stu-id="b03d8-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="b03d8-136">Ezért szükséges, hogy mielőtt kikapcsolna egy dimenziót, törölje az összes **Szerepár** és **Szerep felár** sort, amelyekben a dimenzió értéke kitöltve van.</span><span class="sxs-lookup"><span data-stu-id="b03d8-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]