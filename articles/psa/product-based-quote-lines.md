---
title: Termékalapú árajánlatsorok
description: Ez a témakör információkat nyújt a termékalapú árajánlatsorokról.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8bde88f5f2d00c09129c6a9363c09f6f6ad1dd90
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284091"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="11d4e-103">Termékalapú árajánlatsorok</span><span class="sxs-lookup"><span data-stu-id="11d4e-103">Product-based quote lines</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="11d4e-104">A Dynamics 365 Project Service Automation szolgáltatásban termékalapú árajánlatsorokat hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="11d4e-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="11d4e-105">A termékalapú árajánlatsorok lehetnek „beírási” sorok vagy a termékkatalógusban szereplő elemek.</span><span class="sxs-lookup"><span data-stu-id="11d4e-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="11d4e-106">Termékkatalógus</span><span class="sxs-lookup"><span data-stu-id="11d4e-106">Product catalog</span></span>

<span data-ttu-id="11d4e-107">A Dynamics 365 termékkatalógusban szereplő termékek alapértelmezett egységgel és egységcsoporttal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="11d4e-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="11d4e-108">Ha több termék ugyanazon attribútumkészlettel rendelkezik, akkor létrehozhat egy termékcsaládot, amely szintén rendelkezik ezekkel az attribútumokkal.</span><span class="sxs-lookup"><span data-stu-id="11d4e-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="11d4e-109">Egy termékcsalád összes terméke ugyanazt az attribútumkészletet örökli.</span><span class="sxs-lookup"><span data-stu-id="11d4e-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="11d4e-110">Például egy vállalat előfizetési licenceket értékesít különféle szoftverekre.</span><span class="sxs-lookup"><span data-stu-id="11d4e-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="11d4e-111">Az összes előfizetési szoftver a következő két attribútummal rendelkezik:</span><span class="sxs-lookup"><span data-stu-id="11d4e-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="11d4e-112">Felhasználók száma</span><span class="sxs-lookup"><span data-stu-id="11d4e-112">Number of users</span></span> 
- <span data-ttu-id="11d4e-113">Előfizetés időtartama (hónapokban)</span><span class="sxs-lookup"><span data-stu-id="11d4e-113">Subscription duration (in months)</span></span>

<span data-ttu-id="11d4e-114">Az ilyen típusú katalógus fenntartásának megfelelő módja egy termékcsalád létrehozása, amelynek neve **Előfizetési szoftver**, és amely rendelkezik **Felhasználók száma** és **Előfizetés időtartama** attribútumokkal.</span><span class="sxs-lookup"><span data-stu-id="11d4e-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="11d4e-115">Ezután különálló termékeket, például a **Dynamics 365 Sales** szolgáltatást vagy a **Dynamics 365 Field Service** szolgáltatást hozzáadhatja az **Előfizetési szoftver** termékcsaládhoz.</span><span class="sxs-lookup"><span data-stu-id="11d4e-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="11d4e-116">Termékkatalógus-elemek hozzáadása a projektárajánlathoz</span><span class="sxs-lookup"><span data-stu-id="11d4e-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="11d4e-117">A projektárajánlat és a projektszerződés oldalak kétféle sort tartalmaznak: projektalapú sorok és termékalapú sorok.</span><span class="sxs-lookup"><span data-stu-id="11d4e-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="11d4e-118">Termékalapú sorok esetén a Dynamics 365 használatával elemeket adhat hozzá termékkatalógusból egy árajánlathoz.</span><span class="sxs-lookup"><span data-stu-id="11d4e-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="11d4e-119">Az árajánlatsorban vagy a projektszerződés-sorban lévő legördülő lista tartalmazza az összes terméket és egységet a termék árlistájában, amelyet csatolt az árajánlathoz vagy a projektszerződéshez.</span><span class="sxs-lookup"><span data-stu-id="11d4e-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="11d4e-120">Olyan termékeket is hozzáadhat, amelyek nem képezik részét az árajánlat termékárlistájának.</span><span class="sxs-lookup"><span data-stu-id="11d4e-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="11d4e-121">Ezen felül kiválaszthat termékeket más árlistákból, vagy közvetlenül a termékkatalógusból is kiválaszthatja a termékeket.</span><span class="sxs-lookup"><span data-stu-id="11d4e-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="11d4e-122">Ha közvetlenül termékkatalógusból választja ki a termékeket, akkor az adott termék alapértelmezett árlistáját kell használnia a termék értékesítési árának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="11d4e-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="11d4e-123">Ha nincs megadva alapértelmezett árlista, akkor az ár 0 (nulla) értékre lesz állítva.</span><span class="sxs-lookup"><span data-stu-id="11d4e-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="11d4e-124">Ha az árajánlatsor egy termékkatalóguson alapul, akkor az értékesítési árat közvetlenül az árajánlatsoron bírálhatja felül.</span><span class="sxs-lookup"><span data-stu-id="11d4e-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="11d4e-125">Vegye figyelembe, hogy a Dynamics 365 árajánlatsora rendelkezik **Árképzés** mezővel.</span><span class="sxs-lookup"><span data-stu-id="11d4e-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="11d4e-126">Két érték áll rendelkezésre:</span><span class="sxs-lookup"><span data-stu-id="11d4e-126">Two values are available:</span></span>

- <span data-ttu-id="11d4e-127">Árképzés felülbírálása</span><span class="sxs-lookup"><span data-stu-id="11d4e-127">Override pricing</span></span>  
- <span data-ttu-id="11d4e-128">Alapértelmezett használata</span><span class="sxs-lookup"><span data-stu-id="11d4e-128">Use default</span></span>

<span data-ttu-id="11d4e-129">Ha ezt a mezőt **Árképzés felülbírálása** értékre állítja, a Dynamics 365 nem állít be alapértelmezett árat.</span><span class="sxs-lookup"><span data-stu-id="11d4e-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="11d4e-130">Az árajánlatsorba kell beírnia a termék árát.</span><span class="sxs-lookup"><span data-stu-id="11d4e-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="11d4e-131">Ha ezt a mezőt **Alapértelmezett használata** értékre állítja, akkor a Dynamics 365 az alapértelmezett értékesítési árat használja, és bezárja a mezőt a szerkesztés megakadályozása érdekében.</span><span class="sxs-lookup"><span data-stu-id="11d4e-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="11d4e-132">A PSA telepítése után az alapértelmezett eladási árak az árajánlat termékalapú soraiba kerülnek be.</span><span class="sxs-lookup"><span data-stu-id="11d4e-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="11d4e-133">Az **Árképzés** mező ezután **Árképzés felülbírálása** értékre lesz állítva, hogy az alapértelmezett árat az árajánlatsorokon szerkeszthesse.</span><span class="sxs-lookup"><span data-stu-id="11d4e-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Árképzés felülbírálásának beállítása](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="11d4e-135">A termékek mennyiségi tényezői</span><span class="sxs-lookup"><span data-stu-id="11d4e-135">Quantity factors for products</span></span>

<span data-ttu-id="11d4e-136">A PSA mennyiségi tényezőket alkalmaz az előfizetésen alapuló termékek értékesítésének támogatására.</span><span class="sxs-lookup"><span data-stu-id="11d4e-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="11d4e-137">Az előfizetésen alapuló termékek esetében az árajánlat vagy a projektszerződés sorában szereplő mennyiséget a felhasználói/hónap számában fejezik ki.</span><span class="sxs-lookup"><span data-stu-id="11d4e-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="11d4e-138">Az előfizetési szoftver ára általában a katalógusban kerül tárolásra havi felhasználónkénti árként.</span><span class="sxs-lookup"><span data-stu-id="11d4e-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="11d4e-139">Ehelyett más időleírásokat is használhat.</span><span class="sxs-lookup"><span data-stu-id="11d4e-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="11d4e-140">Az értékesítési folyamat során az árajánlatsorban a felhasználónkénti havi ár általában az IT-értékesítési ügynökkel való egyeztetés után és az általa megadott árengedménnyel születik meg.</span><span class="sxs-lookup"><span data-stu-id="11d4e-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="11d4e-141">Minden egyes ügyletnek eltérő felhasználói száma és előfizetési hónapjai vannak.</span><span class="sxs-lookup"><span data-stu-id="11d4e-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="11d4e-142">Az árajánlatsor összegének kiszámításához használt mennyiség a felhasználók számának és az előfizetési hónapoknak a szorzata.</span><span class="sxs-lookup"><span data-stu-id="11d4e-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="11d4e-143">Az ilyen típusú értékesítés támogatása érdekében a PSA bevezette a mennyiségi tényezők fogalmát.</span><span class="sxs-lookup"><span data-stu-id="11d4e-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="11d4e-144">A mennyiségi tényezők a Dynamics 365 termékattribútumaira támaszkodnak.</span><span class="sxs-lookup"><span data-stu-id="11d4e-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="11d4e-145">Amikor egy adott termék tulajdonságait konfigurálja, a PSA lehetővé teszi, hogy mennyiségi tényezőként jelölje meg ezen tulajdonságok egy részhalmazát vagy az összes tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="11d4e-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="11d4e-146">A PSA ügyel rá, hogy csak a numerikus vagy a numerikus adattípusú termékjellemzők kerülhessenek megjelölésre mennyiségi tényezőként.</span><span class="sxs-lookup"><span data-stu-id="11d4e-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="11d4e-147">Ha egy termék, amelynek mennyiségi tényezőit konfigurálják, hozzáadásra kerül egy árajánlatsorhoz, az árajánlatsor **Mennyiség** mezője „csak olvasható” mező lesz.</span><span class="sxs-lookup"><span data-stu-id="11d4e-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="11d4e-148">Miután megadta a terméktulajdonságok értékeit, amelyek mennyiségi tényezők, a PSA kiszámítja az árajánlatsor mennyiségét.</span><span class="sxs-lookup"><span data-stu-id="11d4e-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="11d4e-149">Például a Dynamics 365 a következő tulajdonságokkal rendelkezik:</span><span class="sxs-lookup"><span data-stu-id="11d4e-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="11d4e-150">**Felhasználók száma** – a felhasználók száma</span><span class="sxs-lookup"><span data-stu-id="11d4e-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="11d4e-151">**Hónapok száma** – az előfizetési hónapok száma</span><span class="sxs-lookup"><span data-stu-id="11d4e-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="11d4e-152">**Termék cikkszáma**</span><span class="sxs-lookup"><span data-stu-id="11d4e-152">**Product SKU**</span></span> 

<span data-ttu-id="11d4e-153">A **Felhasználók száma** és a **Hónapok száma** tulajdonságok megjelölhetők mennyiségi tényezőként a terméksor tulajdonságainak szerkesztésével.</span><span class="sxs-lookup"><span data-stu-id="11d4e-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![A felhasználók számának és a hónapok számának megjelölése minőségi tényezőként](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]