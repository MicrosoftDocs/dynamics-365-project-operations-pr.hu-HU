---
title: Árképzési dimenzió kikapcsolása
description: Ez a témakör az árképzési dimenziók kikapcsolásáról nyújt információkat.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 54e02726138f7306481ca50d5204ee29a3b68549
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896509"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="e85d1-103">Árképzési dimenzió kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="e85d1-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="e85d1-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="e85d1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e85d1-105">Előfordulhat, hogy néhány évente felül kell vizsgálnia és frissítenie kell az árképzési stratégiát.</span><span class="sxs-lookup"><span data-stu-id="e85d1-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="e85d1-106">A frissítések elvégzéséhez szükség lehet egy meglévő árazási dimenzió kikapcsolására és egy új létrehozására.</span><span class="sxs-lookup"><span data-stu-id="e85d1-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="e85d1-107">Például előfordulhat, hogy korábban a **Szerep** árát határozta meg, de most úgy döntött, hogy az **Munkakörnyezet** szerinti árat határozza meg.</span><span class="sxs-lookup"><span data-stu-id="e85d1-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="e85d1-108">Ehhez szükség lehet a **Szerep** árképzési dimenzió kikapcsolására és a **Munkakörnyezet** új árképzési dimenzió létrehozására.</span><span class="sxs-lookup"><span data-stu-id="e85d1-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="e85d1-109">Árképzési dimenzió kikapcsolása, függetlenül attól, hogy kész vagy egyéni, lehetséges a **Költségre vonatkozó** és **Értékesítésre vonatkozó** mezők **Nem**-re állításával.</span><span class="sxs-lookup"><span data-stu-id="e85d1-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="e85d1-110">Ekkor azonban a hibaüzenet jelenhet meg: **Az árképzési dimenzió nem frissíthető és nem törölhető, ha vannak társított árképzési rekordok vannak.**</span><span class="sxs-lookup"><span data-stu-id="e85d1-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

<span data-ttu-id="e85d1-111">Ez a hibaüzenet azt jelzi, hogy vannak árrekordok, amelyeket korábban beállítottak a kikapcsolt dimenzióhoz.</span><span class="sxs-lookup"><span data-stu-id="e85d1-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="e85d1-112">Az összes **Szerepár** és **Szerep felár** rekordot, amely egy dimenzióra utal, törölni kell, mielőtt a dimenzió alkalmazhatóságát **Nem** értékre lehet állítani.</span><span class="sxs-lookup"><span data-stu-id="e85d1-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="e85d1-113">Ez a szabály vonatkozik mind a beépített árképzési dimenziókra, mind az esetlegesen létrehozott egyedi árképzési dimenziókra.</span><span class="sxs-lookup"><span data-stu-id="e85d1-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="e85d1-114">Erre az ellenőrzésre azért van szükség, mert minden **Szerepár** rekordnak egyedi dimenziókombinációval kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="e85d1-114">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="e85d1-115">Például az **US Cost Rates 2018** nevű árlistán a következő **Szerepár** sorok vannak.</span><span class="sxs-lookup"><span data-stu-id="e85d1-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="e85d1-116">Normál cím</span><span class="sxs-lookup"><span data-stu-id="e85d1-116">Standard Title</span></span>         | <span data-ttu-id="e85d1-117">Szerv. egység</span><span class="sxs-lookup"><span data-stu-id="e85d1-117">Org Unit</span></span>    |<span data-ttu-id="e85d1-118">Egység</span><span class="sxs-lookup"><span data-stu-id="e85d1-118">Unit</span></span>   |<span data-ttu-id="e85d1-119">Ár</span><span class="sxs-lookup"><span data-stu-id="e85d1-119">Price</span></span>  |<span data-ttu-id="e85d1-120">Pénznem</span><span class="sxs-lookup"><span data-stu-id="e85d1-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="e85d1-121">Rendszermérnök</span><span class="sxs-lookup"><span data-stu-id="e85d1-121">Systems Engineer</span></span>|<span data-ttu-id="e85d1-122">Contoso USA</span><span class="sxs-lookup"><span data-stu-id="e85d1-122">Contoso US</span></span>|<span data-ttu-id="e85d1-123">Hour</span><span class="sxs-lookup"><span data-stu-id="e85d1-123">Hour</span></span>| <span data-ttu-id="e85d1-124">100</span><span class="sxs-lookup"><span data-stu-id="e85d1-124">100</span></span>|<span data-ttu-id="e85d1-125">USD</span><span class="sxs-lookup"><span data-stu-id="e85d1-125">USD</span></span>|
| <span data-ttu-id="e85d1-126">Vezető rendszermérnök</span><span class="sxs-lookup"><span data-stu-id="e85d1-126">Senior Systems Engineer</span></span>|<span data-ttu-id="e85d1-127">Contoso USA</span><span class="sxs-lookup"><span data-stu-id="e85d1-127">Contoso US</span></span>|<span data-ttu-id="e85d1-128">Hour</span><span class="sxs-lookup"><span data-stu-id="e85d1-128">Hour</span></span>| <span data-ttu-id="e85d1-129">150</span><span class="sxs-lookup"><span data-stu-id="e85d1-129">150</span></span>| <span data-ttu-id="e85d1-130">USD</span><span class="sxs-lookup"><span data-stu-id="e85d1-130">USD</span></span>|


<span data-ttu-id="e85d1-131">Ha kikapcsolja a **Normál cím** árképzési dimenziót, és az árképzési motor árat keres, akkor a bemeneti környezetből csak a **Szerv. egység** értéket fogja használni.</span><span class="sxs-lookup"><span data-stu-id="e85d1-131">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="e85d1-132">Ha a bemeneti kontextus **szervezeti egysége** a „Contoso US”, az eredmény nem lesz determinisztikus, hiszen mindkét sor egyezik.</span><span class="sxs-lookup"><span data-stu-id="e85d1-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="e85d1-133">Ennek elkerülése érdekében, amikor **Szerepár** rekordokat hoz létre, a rendszer ellenőrzi, hogy a dimenziók kombinációja egyedi-e.</span><span class="sxs-lookup"><span data-stu-id="e85d1-133">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="e85d1-134">Ha a dimenziót a **Szerepár** rekordok létrehozása után kikapcsolják, ez a korlátozás megsérthető.</span><span class="sxs-lookup"><span data-stu-id="e85d1-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="e85d1-135">Ezért szükséges, hogy mielőtt kikapcsolna egy dimenziót, törölje az összes **Szerepár** és **Szerep felár** sort, amelyekben a dimenzió értéke kitöltve van.</span><span class="sxs-lookup"><span data-stu-id="e85d1-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>
