---
title: Árazási dimenzió kikapcsolása
description: Ez a témakör bemutatja, hogyan állíthatja be az árazási dimenziókat a Project Service megoldásban.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da8615fa147838d9088c639039d5a2534e662e82
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014299"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="3c6ac-103">Árazási dimenzió kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="3c6ac-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3c6ac-104">Előfordulhat, hogy néhány évente felül kell vizsgálnia és frissítenie kell az árképzési stratégiát.</span><span class="sxs-lookup"><span data-stu-id="3c6ac-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="3c6ac-105">A frissítések elvégzéséhez szükség lehet egy meglévő árazási dimenzió kikapcsolására és egy új létrehozására.</span><span class="sxs-lookup"><span data-stu-id="3c6ac-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="3c6ac-106">Például előfordulhat, hogy korábban a **Szerep** árát határozta meg, de most úgy döntött, hogy az **Munkakörnyezet** szerinti árat határozza meg.</span><span class="sxs-lookup"><span data-stu-id="3c6ac-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="3c6ac-107">Ehhez szükség lehet a **Szerep** árképzési dimenzió kikapcsolására, és a **Munkakörnyezet** új árképzési dimenzió létrehozására.</span><span class="sxs-lookup"><span data-stu-id="3c6ac-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="3c6ac-108">Árképzési dimenzió kikapcsolása, függetlenül attól, hogy kész vagy egyéni, lehetséges a **Költségre vonatkozó** és **Értékesítésre vonatkozó** mezők **Nem**-re állításával.</span><span class="sxs-lookup"><span data-stu-id="3c6ac-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="3c6ac-109">Ennek végrehajtásakor azonban a következő hibaüzenet jelenhet meg.</span><span class="sxs-lookup"><span data-stu-id="3c6ac-109">However, when you do this, you might receive the following error message.</span></span>

![Üzleti folyamat hiba valószínűsíthető, amikor kikapcsolja az árképzési dimenziót](media/Business-Process-Error.png)


<span data-ttu-id="3c6ac-111">Ez a hibaüzenet azt jelzi, hogy vannak árrekordok, amelyeket korábban beállítottak a kikapcsolt dimenzióhoz.</span><span class="sxs-lookup"><span data-stu-id="3c6ac-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="3c6ac-112">Az összes **Szerepár** és **Szerep felár** rekordot, amely egy dimenzióra utal, törölni kell, mielőtt a dimenzió alkalmazhatóságát **Nem** értékre lehet állítani.</span><span class="sxs-lookup"><span data-stu-id="3c6ac-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="3c6ac-113">Ez a szabály vonatkozik mind a beépített árképzési dimenziókra, mind az esetlegesen létrehozott egyedi árképzési dimenziókra.</span><span class="sxs-lookup"><span data-stu-id="3c6ac-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="3c6ac-114">Ennek az érvényesítésnek az az oka, hogy a Project Service korlátozza, hogy minden **Szerepár** rekordnak egyedi dimenziókombinációval kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="3c6ac-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="3c6ac-115">Például az **US Cost Rates 2018** nevű árlistán a következő **Szerepár** sorok vannak.</span><span class="sxs-lookup"><span data-stu-id="3c6ac-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="3c6ac-116">Normál cím</span><span class="sxs-lookup"><span data-stu-id="3c6ac-116">Standard Title</span></span>         | <span data-ttu-id="3c6ac-117">Szerv. egység</span><span class="sxs-lookup"><span data-stu-id="3c6ac-117">Org Unit</span></span>    |<span data-ttu-id="3c6ac-118">Kiszerelés</span><span class="sxs-lookup"><span data-stu-id="3c6ac-118">Unit</span></span>   |<span data-ttu-id="3c6ac-119">Ár</span><span class="sxs-lookup"><span data-stu-id="3c6ac-119">Price</span></span>  |<span data-ttu-id="3c6ac-120">Pénznem</span><span class="sxs-lookup"><span data-stu-id="3c6ac-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="3c6ac-121">Rendszermérnök</span><span class="sxs-lookup"><span data-stu-id="3c6ac-121">Systems Engineer</span></span>|<span data-ttu-id="3c6ac-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="3c6ac-122">Contoso US</span></span>|<span data-ttu-id="3c6ac-123">Óra</span><span class="sxs-lookup"><span data-stu-id="3c6ac-123">Hour</span></span>| <span data-ttu-id="3c6ac-124">100</span><span class="sxs-lookup"><span data-stu-id="3c6ac-124">100</span></span>|<span data-ttu-id="3c6ac-125">USD</span><span class="sxs-lookup"><span data-stu-id="3c6ac-125">USD</span></span>|
| <span data-ttu-id="3c6ac-126">Vezető rendszermérnök</span><span class="sxs-lookup"><span data-stu-id="3c6ac-126">Senior Systems Engineer</span></span>|<span data-ttu-id="3c6ac-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="3c6ac-127">Contoso US</span></span>|<span data-ttu-id="3c6ac-128">Óra</span><span class="sxs-lookup"><span data-stu-id="3c6ac-128">Hour</span></span>| <span data-ttu-id="3c6ac-129">150</span><span class="sxs-lookup"><span data-stu-id="3c6ac-129">150</span></span>| <span data-ttu-id="3c6ac-130">USD</span><span class="sxs-lookup"><span data-stu-id="3c6ac-130">USD</span></span>|


<span data-ttu-id="3c6ac-131">Ha kikapcsolja a **Normál cím**-et árképzési dimenzióként, és a Project Service árazási motorja árat keres, akkor csak a **Szerv. egység** értéket a bemeneti környezetből fogja használni.</span><span class="sxs-lookup"><span data-stu-id="3c6ac-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="3c6ac-132">Ha a bemeneti kontextus **Szervezeti egysége** a „Contoso US”, az eredmény nem lesz meghatározó, hiszen mindkét sor egyezik.</span><span class="sxs-lookup"><span data-stu-id="3c6ac-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="3c6ac-133">E forgatókönyv elkerülése érdekében, amikor **Szerepár** rekordokat hoz létre, a Project Service ellenőrzi, hogy a dimenziók kombinációja egyedi-e.</span><span class="sxs-lookup"><span data-stu-id="3c6ac-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="3c6ac-134">Ha a dimenziót a **Szerepár** rekordok létrehozása után kikapcsolják, ez a korlátozás megsérthető.</span><span class="sxs-lookup"><span data-stu-id="3c6ac-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="3c6ac-135">Ezért szükséges, hogy mielőtt kikapcsolna egy dimenziót, törölje az összes **Szerepár** és **Szerep felár** sort, amelyekben a dimenzió értéke kitöltve van.</span><span class="sxs-lookup"><span data-stu-id="3c6ac-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]