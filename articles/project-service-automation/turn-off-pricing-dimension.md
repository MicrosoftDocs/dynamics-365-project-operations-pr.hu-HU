---
title: Árazási dimenzió kikapcsolása
description: Ez a témakör bemutatja, hogyan állíthatja be az árazási dimenziókat a Project Service megoldásban.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 689e5a8d-e39a-471d-a6c4-7e2fc3bb5590
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5cf2cd86fb1eba50c8e08b2bd624669ab0b1deb3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752264"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="3cc62-103">Árazási dimenzió kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="3cc62-103">Turn off a pricing dimension</span></span>

<span data-ttu-id="3cc62-104">Előfordulhat, hogy néhány évente felül kell vizsgálnia és frissítenie kell az árképzési stratégiát.</span><span class="sxs-lookup"><span data-stu-id="3cc62-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="3cc62-105">A frissítések elvégzéséhez szükség lehet egy meglévő árazási dimenzió kikapcsolására és egy új létrehozására.</span><span class="sxs-lookup"><span data-stu-id="3cc62-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="3cc62-106">Például előfordulhat, hogy korábban a **Szerep** árát határozta meg, de most úgy döntött, hogy az **Munkakörnyezet** szerinti árat határozza meg.</span><span class="sxs-lookup"><span data-stu-id="3cc62-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="3cc62-107">Ehhez szükség lehet a **Szerep** árképzési dimenzió kikapcsolására, és a **Munkakörnyezet** új árképzési dimenzió létrehozására.</span><span class="sxs-lookup"><span data-stu-id="3cc62-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="3cc62-108">Árképzési dimenzió kikapcsolása, függetlenül attól, hogy kész vagy egyéni, lehetséges a **Költségre vonatkozó** és **Értékesítésre vonatkozó** mezők **Nem**-re állításával.</span><span class="sxs-lookup"><span data-stu-id="3cc62-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="3cc62-109">Ennek végrehajtásakor azonban a következő hibaüzenet jelenhet meg.</span><span class="sxs-lookup"><span data-stu-id="3cc62-109">However, when you do this, you might receive the following error message.</span></span>

![Üzleti folyamat hiba valószínűsíthető, amikor kikapcsolja az árképzési dimenziót](media/Business-Process-Error.png)


<span data-ttu-id="3cc62-111">Ez a hibaüzenet azt jelzi, hogy vannak árrekordok, amelyeket korábban beállítottak a kikapcsolt dimenzióhoz.</span><span class="sxs-lookup"><span data-stu-id="3cc62-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="3cc62-112">Az összes **Szerepár** és **Szerep felár** rekordot, amely egy dimenzióra utal, törölni kell, mielőtt a dimenzió alkalmazhatóságát **Nem** értékre lehet állítani.</span><span class="sxs-lookup"><span data-stu-id="3cc62-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="3cc62-113">Ez a szabály vonatkozik mind a beépített árképzési dimenziókra, mind az esetlegesen létrehozott egyedi árképzési dimenziókra.</span><span class="sxs-lookup"><span data-stu-id="3cc62-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="3cc62-114">Ennek az érvényesítésnek az az oka, hogy a Project Service korlátozza, hogy minden **Szerepár** rekordnak egyedi dimenziókombinációval kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="3cc62-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="3cc62-115">Például az **US Cost Rates 2018** nevű árlistán a következő **Szerepár** sorok vannak.</span><span class="sxs-lookup"><span data-stu-id="3cc62-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="3cc62-116">Normál cím</span><span class="sxs-lookup"><span data-stu-id="3cc62-116">Standard Title</span></span>         | <span data-ttu-id="3cc62-117">Szerv. egység</span><span class="sxs-lookup"><span data-stu-id="3cc62-117">Org Unit</span></span>    |<span data-ttu-id="3cc62-118">Egység</span><span class="sxs-lookup"><span data-stu-id="3cc62-118">Unit</span></span>   |<span data-ttu-id="3cc62-119">Ár</span><span class="sxs-lookup"><span data-stu-id="3cc62-119">Price</span></span>  |<span data-ttu-id="3cc62-120">Pénznem</span><span class="sxs-lookup"><span data-stu-id="3cc62-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="3cc62-121">Rendszermérnök</span><span class="sxs-lookup"><span data-stu-id="3cc62-121">Systems Engineer</span></span>|<span data-ttu-id="3cc62-122">Contoso USA</span><span class="sxs-lookup"><span data-stu-id="3cc62-122">Contoso US</span></span>|<span data-ttu-id="3cc62-123">Hour</span><span class="sxs-lookup"><span data-stu-id="3cc62-123">Hour</span></span>| <span data-ttu-id="3cc62-124">100</span><span class="sxs-lookup"><span data-stu-id="3cc62-124">100</span></span>|<span data-ttu-id="3cc62-125">USD</span><span class="sxs-lookup"><span data-stu-id="3cc62-125">USD</span></span>|
| <span data-ttu-id="3cc62-126">Vezető rendszermérnök</span><span class="sxs-lookup"><span data-stu-id="3cc62-126">Senior Systems Engineer</span></span>|<span data-ttu-id="3cc62-127">Contoso USA</span><span class="sxs-lookup"><span data-stu-id="3cc62-127">Contoso US</span></span>|<span data-ttu-id="3cc62-128">Hour</span><span class="sxs-lookup"><span data-stu-id="3cc62-128">Hour</span></span>| <span data-ttu-id="3cc62-129">150</span><span class="sxs-lookup"><span data-stu-id="3cc62-129">150</span></span>| <span data-ttu-id="3cc62-130">USD</span><span class="sxs-lookup"><span data-stu-id="3cc62-130">USD</span></span>|


<span data-ttu-id="3cc62-131">Ha kikapcsolja a **Normál cím**-et árképzési dimenzióként, és a Project Service árazási motorja árat keres, akkor csak a **Szerv. egység** értéket a bemeneti környezetből fogja használni.</span><span class="sxs-lookup"><span data-stu-id="3cc62-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="3cc62-132">Ha a bemeneti kontextus **szervezeti egysége** a „Contoso US”, az eredmény nem lesz determinisztikus, hiszen mindkét sor egyezik.</span><span class="sxs-lookup"><span data-stu-id="3cc62-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="3cc62-133">E forgatókönyv elkerülése érdekében, amikor **Szerepár** rekordokat hoz létre, a Project Service ellenőrzi, hogy a dimenziók kombinációja egyedi-e.</span><span class="sxs-lookup"><span data-stu-id="3cc62-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="3cc62-134">Ha a dimenziót a **Szerepár** rekordok létrehozása után kikapcsolják, ez a korlátozás megsérthető.</span><span class="sxs-lookup"><span data-stu-id="3cc62-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="3cc62-135">Ezért szükséges, hogy mielőtt kikapcsolna egy dimenziót, törölje az összes **Szerepár** és **Szerep felár** sort, amelyekben a dimenzió értéke kitöltve van.</span><span class="sxs-lookup"><span data-stu-id="3cc62-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>
