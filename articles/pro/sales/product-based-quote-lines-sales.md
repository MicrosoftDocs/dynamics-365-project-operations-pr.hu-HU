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
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178191"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="0cd16-103">Termékalapú árajánlatsorok áttekintése - Lite</span><span class="sxs-lookup"><span data-stu-id="0cd16-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="0cd16-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="0cd16-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0cd16-105">A Dynamics 365 Project Operations szolgáltatásban termékalapú árajánlatsorokat hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="0cd16-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="0cd16-106">A termékalapú árajánlatsorok lehetnek manuálisan megadott vagy a termékkatalógusban szereplő elemek.</span><span class="sxs-lookup"><span data-stu-id="0cd16-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="0cd16-107">Termékkatalógus</span><span class="sxs-lookup"><span data-stu-id="0cd16-107">Product catalog</span></span>

<span data-ttu-id="0cd16-108">A termékkatalógusban szereplő egyes termékek alapértelmezett egységgel és egységcsoporttal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="0cd16-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="0cd16-109">Ha több termék ugyanazon attribútumkészlettel rendelkezik, akkor létrehozhat egy termékcsaládot, amely szintén rendelkezik ezekkel az attribútumokkal.</span><span class="sxs-lookup"><span data-stu-id="0cd16-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="0cd16-110">Például egy vállalat előfizetési licenceket értékesít különféle szoftverekre.</span><span class="sxs-lookup"><span data-stu-id="0cd16-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="0cd16-111">Az összes előfizetési szoftver a következő két attribútummal rendelkezik:</span><span class="sxs-lookup"><span data-stu-id="0cd16-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="0cd16-112">Felhasználók száma</span><span class="sxs-lookup"><span data-stu-id="0cd16-112">Number of users</span></span>
- <span data-ttu-id="0cd16-113">Az előfizetés időtartama hónapokban van megadva</span><span class="sxs-lookup"><span data-stu-id="0cd16-113">A subscription duration measured in months</span></span>

<span data-ttu-id="0cd16-114">Az ilyen típusú katalógus fenntartásához hozzon létre egy **Előfizetési szoftver** nevű termékcsaládot, és adja hozzá a felhasználók számát és az előfizetés időtartamát attribútumként.</span><span class="sxs-lookup"><span data-stu-id="0cd16-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="0cd16-115">Következő lépésként egyéni termékeket adhat hozzá az **Előfizetési szoftver** termékcsaládhoz.</span><span class="sxs-lookup"><span data-stu-id="0cd16-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="0cd16-116">Termékkatalógus-elemek hozzáadása a projektárajánlathoz</span><span class="sxs-lookup"><span data-stu-id="0cd16-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="0cd16-117">A **projektárajánlat** és a **projektszerződés** oldalak tartalmaznak szakaszokat a projektalapú sorokhoz és termékalapú sorokhoz.</span><span class="sxs-lookup"><span data-stu-id="0cd16-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="0cd16-118">A termékalapú soroknál az árajánlatsorban vagy a projektszerződés-sorban lévő legördülő lista tartalmazza az összes terméket és egységet a termék árlistájában.</span><span class="sxs-lookup"><span data-stu-id="0cd16-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="0cd16-119">Olyan termékeket is hozzáadhat, amelyek nem képezik részét a termékárlistának.</span><span class="sxs-lookup"><span data-stu-id="0cd16-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="0cd16-120">Ezen felül kiválaszthat termékeket más árlistákból, vagy közvetlenül a termékkatalógusból.</span><span class="sxs-lookup"><span data-stu-id="0cd16-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="0cd16-121">Ha közvetlenül termékkatalógusból választja ki a termékeket, akkor az adott termék alapértelmezett árlistáját kell használnia a termék értékesítési árának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="0cd16-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="0cd16-122">Ha nincs megadva alapértelmezett árlista, akkor az ár 0 (nulla) értékre lesz állítva.</span><span class="sxs-lookup"><span data-stu-id="0cd16-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="0cd16-123">Ha az árajánlatsor egy termékkatalóguson alapul, akkor az értékesítési árat közvetlenül az árajánlatsoron bírálhatja felül.</span><span class="sxs-lookup"><span data-stu-id="0cd16-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="0cd16-124">Az árajánlat sora az **Árképzés** mezőben két használható értékkel:</span><span class="sxs-lookup"><span data-stu-id="0cd16-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="0cd16-125">**Árképzés felülbírálása**</span><span class="sxs-lookup"><span data-stu-id="0cd16-125">**Override Pricing**</span></span>
- <span data-ttu-id="0cd16-126">**Alapértelmezett használata**</span><span class="sxs-lookup"><span data-stu-id="0cd16-126">**Use Default**</span></span>

<span data-ttu-id="0cd16-127">Ha az **Árképzés felülbírálása** lehetőséget választja, akkor az alapértelmezett ár nincs beállítva.</span><span class="sxs-lookup"><span data-stu-id="0cd16-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="0cd16-128">Ehelyett az árajánlatsorba kell beírnia a termék árát.</span><span class="sxs-lookup"><span data-stu-id="0cd16-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="0cd16-129">Ha az **alapértelmezett használata** lehetőséget választja, akkor az alapértelmezett értékesítési árat használja a program, és a mező szerkesztésre zárolva van.</span><span class="sxs-lookup"><span data-stu-id="0cd16-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="0cd16-130">Az alapértelmezett eladási árak az árajánlat termékalapú soraiba kerülnek be.</span><span class="sxs-lookup"><span data-stu-id="0cd16-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="0cd16-131">Az **Árképzés** mező ezután **Árképzés felülbírálása** értékre lesz állítva, hogy az alapértelmezett árat az árajánlatsorokon szerkeszthesse.</span><span class="sxs-lookup"><span data-stu-id="0cd16-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="0cd16-132">Ez egy olyan Project Operations-specifikus felülbírálás, amely a terméken alapuló sorok viselkedését a Dynamics 365 Salesben felülbírálja.</span><span class="sxs-lookup"><span data-stu-id="0cd16-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>
