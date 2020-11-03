---
title: Termékalapú szerződéssorok áttekintése
description: Ez a témakör információkat nyújt a termékalapú szerződéssorokról.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 794a80b0dd6b8717b43e712b96b9ac077517c226
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078019"
---
# <a name="product-based-contract-lines-overview"></a><span data-ttu-id="105d6-103">Termékalapú szerződéssorok áttekintése</span><span class="sxs-lookup"><span data-stu-id="105d6-103">Product-based contract lines overview</span></span>

<span data-ttu-id="105d6-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="105d6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="105d6-105">A Dynamics 365 Project Operations alkalmazásban a termékalapú szerződéssorokat hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="105d6-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="105d6-106">A termékalapú szerződéssorok lehetnek manuálisan létrehozott sorok vagy a termékkatalógusban szereplő elemek.</span><span class="sxs-lookup"><span data-stu-id="105d6-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="105d6-107">Termékkatalógus</span><span class="sxs-lookup"><span data-stu-id="105d6-107">Product catalog</span></span>

<span data-ttu-id="105d6-108">A termékkatalógusban szereplő termékek alapértelmezett egységgel és egységcsoporttal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="105d6-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="105d6-109">Ha több termék ugyanazon attribútumkészlettel rendelkezik, akkor létrehozhat egy termékcsaládot, amely szintén rendelkezik ezekkel az attribútumokkal.</span><span class="sxs-lookup"><span data-stu-id="105d6-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="105d6-110">Egy termékcsalád összes terméke ugyanazt az attribútumkészletet örökli.</span><span class="sxs-lookup"><span data-stu-id="105d6-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="105d6-111">Például egy vállalat előfizetési licenceket értékesít különféle szoftverekre.</span><span class="sxs-lookup"><span data-stu-id="105d6-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="105d6-112">Az összes előfizetési szoftver a következő két attribútummal rendelkezik:</span><span class="sxs-lookup"><span data-stu-id="105d6-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="105d6-113">Felhasználók száma</span><span class="sxs-lookup"><span data-stu-id="105d6-113">Number of users</span></span>
- <span data-ttu-id="105d6-114">Előfizetés időtartama (hónapokban)</span><span class="sxs-lookup"><span data-stu-id="105d6-114">Subscription duration (in months)</span></span>

<span data-ttu-id="105d6-115">Az ilyen típusú katalógus karbantartásához hozzon létre egy **előfizetési szoftver** nevű termékcsaládot.</span><span class="sxs-lookup"><span data-stu-id="105d6-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="105d6-116">Adja hozzá az attribútumokat, a **felhasználók számát** és az **előfizetési időtartamot** a termékcsalád számára.</span><span class="sxs-lookup"><span data-stu-id="105d6-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="105d6-117">Ezután vegye fel az egyes termékeket az **előfizetői szoftver** termékcsaládba.</span><span class="sxs-lookup"><span data-stu-id="105d6-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="105d6-118">Termékkatalógus-elemek hozzáadása a projektszerződéshez</span><span class="sxs-lookup"><span data-stu-id="105d6-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="105d6-119">A projektszerződések kétféle sort tartalmaznak: projektalapú sorok és termékalapú sorok.</span><span class="sxs-lookup"><span data-stu-id="105d6-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="105d6-120">A terméken alapuló sorok tartalmazzák az összes terméket és egységet a szerződéshez tartozó termékárlistán.</span><span class="sxs-lookup"><span data-stu-id="105d6-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="105d6-121">Olyan termékeket is hozzáadhat, amelyek nem képezik részét a szerződés termékárlistájának.</span><span class="sxs-lookup"><span data-stu-id="105d6-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="105d6-122">A termékeket más árlistákből, vagy közvetlenül a termékkatalógusból is kijelölheti.</span><span class="sxs-lookup"><span data-stu-id="105d6-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="105d6-123">Ha közvetlenül termékkatalógusból választja ki a termékeket, akkor az adott termék alapértelmezett árlistáját kell használnia a termék értékesítési árának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="105d6-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="105d6-124">Ha nincs megadva alapértelmezett árlista, akkor az ár 0 (nulla) értékre lesz állítva.</span><span class="sxs-lookup"><span data-stu-id="105d6-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="105d6-125">Ha a szerződéssor egy termékkatalóguson alapul, akkor az értékesítési árat közvetlenül a soron bírálhatja felül.</span><span class="sxs-lookup"><span data-stu-id="105d6-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="105d6-126">A szerződéssoron szerepel az **Árképzés** mező két értékkel:</span><span class="sxs-lookup"><span data-stu-id="105d6-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="105d6-127">**Árképzés felülbírálása**</span><span class="sxs-lookup"><span data-stu-id="105d6-127">**Override pricing**</span></span>
- <span data-ttu-id="105d6-128">**Alapértelmezett használata**</span><span class="sxs-lookup"><span data-stu-id="105d6-128">**Use default**</span></span>

<span data-ttu-id="105d6-129">Ha az **Árképzés** mezőt az **Árképzés felülbírálása** értékre állítja, nem állít be alapértelmezett árat.</span><span class="sxs-lookup"><span data-stu-id="105d6-129">If you set the **Pricing** field to **Override pricing** , the default price isn't set.</span></span> <span data-ttu-id="105d6-130">Adja meg a szerződéssor termékének árát.</span><span class="sxs-lookup"><span data-stu-id="105d6-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="105d6-131">Ha a mezőt **Alapértelmezett érték használata** értékre állítja, akkor a rendszer az alapértelmezett értékesítési árat használja, és a mező nem szerkeszthető.</span><span class="sxs-lookup"><span data-stu-id="105d6-131">If you set the field to **Use default** , the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="105d6-132">A Project Operations telepítése után az alapértelmezett eladási árak a szerződés termékalapú soraiba kerülnek be.</span><span class="sxs-lookup"><span data-stu-id="105d6-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="105d6-133">Az **Árképzés** mező **Árképzés felülbírálása** értékre lesz állítva, hogy az alapértelmezett árat a szerződéssorokon szerkeszthesse.</span><span class="sxs-lookup"><span data-stu-id="105d6-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="105d6-134">Ez a Project Operations-specifikus felülbírálás a termék alapú sorok működésénál a Dynamics 365 Sales alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="105d6-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>
