---
title: Termékalapú árajánlatsorok áttekintése - Lite
description: Ez a témakör információkat nyújt a termékalapú árajánlatsorok használatáról.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29d82637c6c8bb5b5cde7707d181d5b3d3b235c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272571"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="b3e54-103">Termékalapú árajánlatsorok áttekintése - Lite</span><span class="sxs-lookup"><span data-stu-id="b3e54-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="b3e54-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="b3e54-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b3e54-105">A Dynamics 365 Project Operations szolgáltatásban termékalapú árajánlatsorokat hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="b3e54-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="b3e54-106">A termékalapú árajánlatsorok lehetnek manuálisan megadott vagy a termékkatalógusban szereplő elemek.</span><span class="sxs-lookup"><span data-stu-id="b3e54-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="b3e54-107">Termékkatalógus</span><span class="sxs-lookup"><span data-stu-id="b3e54-107">Product catalog</span></span>

<span data-ttu-id="b3e54-108">A termékkatalógusban szereplő egyes termékek alapértelmezett egységgel és egységcsoporttal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="b3e54-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="b3e54-109">Ha több termék ugyanazon attribútumkészlettel rendelkezik, akkor létrehozhat egy termékcsaládot, amely szintén rendelkezik ezekkel az attribútumokkal.</span><span class="sxs-lookup"><span data-stu-id="b3e54-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="b3e54-110">Például egy vállalat előfizetési licenceket értékesít különféle szoftverekre.</span><span class="sxs-lookup"><span data-stu-id="b3e54-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="b3e54-111">Az összes előfizetési szoftver a következő két attribútummal rendelkezik:</span><span class="sxs-lookup"><span data-stu-id="b3e54-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="b3e54-112">Felhasználók száma</span><span class="sxs-lookup"><span data-stu-id="b3e54-112">Number of users</span></span>
- <span data-ttu-id="b3e54-113">Az előfizetés időtartama hónapokban van megadva</span><span class="sxs-lookup"><span data-stu-id="b3e54-113">A subscription duration measured in months</span></span>

<span data-ttu-id="b3e54-114">Az ilyen típusú katalógus fenntartásához hozzon létre egy **Előfizetési szoftver** nevű termékcsaládot, és adja hozzá a felhasználók számát és az előfizetés időtartamát attribútumként.</span><span class="sxs-lookup"><span data-stu-id="b3e54-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="b3e54-115">Következő lépésként egyéni termékeket adhat hozzá az **Előfizetési szoftver** termékcsaládhoz.</span><span class="sxs-lookup"><span data-stu-id="b3e54-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="b3e54-116">Termékkatalógus-elemek hozzáadása a projektárajánlathoz</span><span class="sxs-lookup"><span data-stu-id="b3e54-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="b3e54-117">A **projektárajánlat** és a **projektszerződés** oldalak tartalmaznak szakaszokat a projektalapú sorokhoz és termékalapú sorokhoz.</span><span class="sxs-lookup"><span data-stu-id="b3e54-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="b3e54-118">A termékalapú soroknál az árajánlatsorban vagy a projektszerződés-sorban lévő legördülő lista tartalmazza az összes terméket és egységet a termék árlistájában.</span><span class="sxs-lookup"><span data-stu-id="b3e54-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="b3e54-119">Olyan termékeket is hozzáadhat, amelyek nem képezik részét a termékárlistának.</span><span class="sxs-lookup"><span data-stu-id="b3e54-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="b3e54-120">Ezen felül kiválaszthat termékeket más árlistákból, vagy közvetlenül a termékkatalógusból.</span><span class="sxs-lookup"><span data-stu-id="b3e54-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="b3e54-121">Ha közvetlenül termékkatalógusból választja ki a termékeket, akkor az adott termék alapértelmezett árlistáját kell használnia a termék értékesítési árának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="b3e54-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="b3e54-122">Ha nincs megadva alapértelmezett árlista, akkor az ár 0 (nulla) értékre lesz állítva.</span><span class="sxs-lookup"><span data-stu-id="b3e54-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="b3e54-123">Ha az árajánlatsor egy termékkatalóguson alapul, akkor az értékesítési árat közvetlenül az árajánlatsoron bírálhatja felül.</span><span class="sxs-lookup"><span data-stu-id="b3e54-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="b3e54-124">Az árajánlat sora az **Árképzés** mezőben két használható értékkel:</span><span class="sxs-lookup"><span data-stu-id="b3e54-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="b3e54-125">**Árképzés felülbírálása**</span><span class="sxs-lookup"><span data-stu-id="b3e54-125">**Override Pricing**</span></span>
- <span data-ttu-id="b3e54-126">**Alapértelmezett használata**</span><span class="sxs-lookup"><span data-stu-id="b3e54-126">**Use Default**</span></span>

<span data-ttu-id="b3e54-127">Ha az **Árképzés felülbírálása** lehetőséget választja, akkor az alapértelmezett ár nincs beállítva.</span><span class="sxs-lookup"><span data-stu-id="b3e54-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="b3e54-128">Ehelyett az árajánlatsorba kell beírnia a termék árát.</span><span class="sxs-lookup"><span data-stu-id="b3e54-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="b3e54-129">Ha az **alapértelmezett használata** lehetőséget választja, akkor az alapértelmezett értékesítési árat használja a program, és a mező szerkesztésre zárolva van.</span><span class="sxs-lookup"><span data-stu-id="b3e54-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="b3e54-130">Az alapértelmezett eladási árak az árajánlat termékalapú soraiba kerülnek be.</span><span class="sxs-lookup"><span data-stu-id="b3e54-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="b3e54-131">Az **Árképzés** mező ezután **Árképzés felülbírálása** értékre lesz állítva, hogy az alapértelmezett árat az árajánlatsorokon szerkeszthesse.</span><span class="sxs-lookup"><span data-stu-id="b3e54-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="b3e54-132">Ez egy olyan Project Operations-specifikus felülbírálás, amely a terméken alapuló sorok viselkedését a Dynamics 365 Salesben felülbírálja.</span><span class="sxs-lookup"><span data-stu-id="b3e54-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]