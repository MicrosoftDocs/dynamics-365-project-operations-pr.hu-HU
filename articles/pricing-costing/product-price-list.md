---
title: Termékárlista
description: Ez a témakör a projektárajánlatokhoz és szerződésekhez használatos katalógusárképzésben szereplő árlistákról nyújt információkat.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877493"
---
# <a name="product-price-lists"></a><span data-ttu-id="0fc80-103">Termékárlisták</span><span class="sxs-lookup"><span data-stu-id="0fc80-103">Product price lists</span></span>

<span data-ttu-id="0fc80-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="0fc80-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="0fc80-105">A Project Operations, a **Termékárlisták** és a kapcsolódó árlistaelem-entitások támogatják a termékalapú árajánlaton és szerződéssorokon alapuló árképzési termékek funkcióit.</span><span class="sxs-lookup"><span data-stu-id="0fc80-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="0fc80-106">A projektekben használt termékek esetében a projektárlisták árlistarekordjait használja a elem.</span><span class="sxs-lookup"><span data-stu-id="0fc80-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="0fc80-107">A termékeket úgy kell beállítani, hogy azok alapértelmezett költséggel és árlistákkal rendelkezzenek a termékkatalógusban.</span><span class="sxs-lookup"><span data-stu-id="0fc80-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="0fc80-108">Az alapértelmezett költség és a listaárak konfigurálásához használja a listaárat, illetve a szokásos és a jelenlegi költségeket.</span><span class="sxs-lookup"><span data-stu-id="0fc80-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="0fc80-109">Az alapértelmezett listaárak csak akkor használhatók az árajánlatsoron vagy a projektszerződés-soron, ha a rendszer nem találja az adott termék árlistáját az árajánlatban vagy a projektszerződésben.</span><span class="sxs-lookup"><span data-stu-id="0fc80-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="0fc80-110">A termékkatalógus-sorok bekerülési ára árajánlatok között megváltoztatható.</span><span class="sxs-lookup"><span data-stu-id="0fc80-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="0fc80-111">Ez a képesség fontos, mivel ha nem pontosan követi nyomon a költségeket, akkor nem tudja meghatározni a projekt kötelezettségvállalásaiból származó működési nyereséget.</span><span class="sxs-lookup"><span data-stu-id="0fc80-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="0fc80-112">Alapértelmezés szerint a termék standard költsége lesz a bekerülési ár.</span><span class="sxs-lookup"><span data-stu-id="0fc80-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="0fc80-113">Az alapértelmezett bekerülési ár azonban frissíthető az árajánlatsorban, ha az árajánlat eltérő.</span><span class="sxs-lookup"><span data-stu-id="0fc80-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="0fc80-114">Árlistaelemek</span><span class="sxs-lookup"><span data-stu-id="0fc80-114">Price list items</span></span>

<span data-ttu-id="0fc80-115">A termékkatalógusból felveheti termékeit a különböző árlistákra.</span><span class="sxs-lookup"><span data-stu-id="0fc80-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="0fc80-116">A termékek árlistasorai mindig egy adott egységre utalnak.</span><span class="sxs-lookup"><span data-stu-id="0fc80-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="0fc80-117">Az árlistán szereplő termékek árképzése devizaösszegként konfigurálható.</span><span class="sxs-lookup"><span data-stu-id="0fc80-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="0fc80-118">Alternatív lehetőségként a listaár, az aktuális költség vagy a standard költség függvényében is konfigurálható.</span><span class="sxs-lookup"><span data-stu-id="0fc80-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="0fc80-119">Az árképzési funkció különféle kerekítési lehetőségeket támogat, ha a termékárakat a listaár, a standard költség vagy az aktuális költség függvényében konfigurálják.</span><span class="sxs-lookup"><span data-stu-id="0fc80-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="0fc80-120">Amellett, hogy kihasználja a több árképzési módszer és a kerekítési lehetőség előnyeit, kedvezménylistákat kapcsolhat hozzá az árlisták elemeihez.</span><span class="sxs-lookup"><span data-stu-id="0fc80-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="0fc80-121">Alapértelmezett termékárlista</span><span class="sxs-lookup"><span data-stu-id="0fc80-121">Default product price list</span></span>
<span data-ttu-id="0fc80-122">Minden ügyfélrekordnak van egy **Alapértelmezett árlista** mezője, ahol megadhatja az ügyfél pénznemének megfelelő árlistát.</span><span class="sxs-lookup"><span data-stu-id="0fc80-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="0fc80-123">Az alapértelmezett értékek nem kerülnek be automatikusan ebbe a mezőbe.</span><span class="sxs-lookup"><span data-stu-id="0fc80-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="0fc80-124">Ha egyedi árképzési megállapodás létezik egy adott ügyféllel, akkor ezt a mezőt felhasználhatja az árlista az adott ügyféllel való társításához.</span><span class="sxs-lookup"><span data-stu-id="0fc80-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="0fc80-125">A Lehetőség, az Árajánlat és a Projektszerződés entitásai az alábbi sorrendet használják az alapértelmezett terméklisták megadására.</span><span class="sxs-lookup"><span data-stu-id="0fc80-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="0fc80-126">Ugyanez a sorrend használatos a projekt árlistáira is.</span><span class="sxs-lookup"><span data-stu-id="0fc80-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="0fc80-127">Ajánlat</span><span class="sxs-lookup"><span data-stu-id="0fc80-127">Quote</span></span>
2.  <span data-ttu-id="0fc80-128">Lehetőség</span><span class="sxs-lookup"><span data-stu-id="0fc80-128">Opportunity</span></span>
3.  <span data-ttu-id="0fc80-129">Ügyfél</span><span class="sxs-lookup"><span data-stu-id="0fc80-129">Customer</span></span>
4.  <span data-ttu-id="0fc80-130">Globális beállítások</span><span class="sxs-lookup"><span data-stu-id="0fc80-130">Global settings</span></span> 

<span data-ttu-id="0fc80-131">Alapértelmezés szerint az árajánlatsor **Termék** mezője felsorolja az összes aktív terméket az árajánlat terméklistáján.</span><span class="sxs-lookup"><span data-stu-id="0fc80-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="0fc80-132">Ha egy terméket inaktiváltak, vagy ha ez egy termékvázlat, akkor nem szerepel a listán még akkor sem, ha szerepel az árlistán.</span><span class="sxs-lookup"><span data-stu-id="0fc80-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="0fc80-133">A termékkatalógus-sorok számlasorokként kerülnek hozzáadásra az első számlára, amelyet egy projektszerződéshez készítenek.</span><span class="sxs-lookup"><span data-stu-id="0fc80-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="0fc80-134">A számlatervezeten törölhetők ezek a számlasorok.</span><span class="sxs-lookup"><span data-stu-id="0fc80-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="0fc80-135">Ebben az esetben a sorok egy későbbi számlán jelennek meg, amíg számlázásra nem kerülnek, vagy amíg a számlát el nem küldik az ügyfélnek.</span><span class="sxs-lookup"><span data-stu-id="0fc80-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="0fc80-136">Nem számlázható ki egy termékszámlasor részleges mennyisége.</span><span class="sxs-lookup"><span data-stu-id="0fc80-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="0fc80-137">Amikor a projektszerződés terméksorozatait kiszámlázzák, tényadatok jönnek létre.</span><span class="sxs-lookup"><span data-stu-id="0fc80-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="0fc80-138">Ezek a tényadatok azonban nem kapcsolódnak a kapcsolódó projektentitáshoz.</span><span class="sxs-lookup"><span data-stu-id="0fc80-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="0fc80-139">Más szavakkal: a termék-alapú projektszerződés-sorok függetlenek minden projektalapú felhasználástól.</span><span class="sxs-lookup"><span data-stu-id="0fc80-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
