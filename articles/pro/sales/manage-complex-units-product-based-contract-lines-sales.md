---
title: Bonyolult egységek kezelése termékalapú szerződéssorokhoz - lite
description: Ez az témakör az előfizetéses termékek értékesítésének támogatásával kapcsolatos információkat tartalmaz.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177379"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="02ec3-103">Bonyolult egységek kezelése termékalapú szerződéssorokhoz - lite</span><span class="sxs-lookup"><span data-stu-id="02ec3-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="02ec3-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="02ec3-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="02ec3-105">A Dynamics 365 Project Operations mennyiségi tényezőket alkalmaz az előfizetésen alapuló termékek értékesítésének támogatására.</span><span class="sxs-lookup"><span data-stu-id="02ec3-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="02ec3-106">Az előfizetésen alapuló termékek esetében a szerződés vagy a projektszerződés sorában szereplő mennyiséget a felhasználói-hónap számában fejezik ki.</span><span class="sxs-lookup"><span data-stu-id="02ec3-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="02ec3-107">Általában az előfizetési szoftver ára általában a katalógusban kerül tárolásra havi felhasználónkénti árként.</span><span class="sxs-lookup"><span data-stu-id="02ec3-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="02ec3-108">Az értékesítési folyamat során a szerződéssorban a felhasználónkénti havi ár általában az értékesítési ügynökkel való egyeztetés után és az általa megadott árengedménnyel születik meg.</span><span class="sxs-lookup"><span data-stu-id="02ec3-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="02ec3-109">Minden egyes ügyletnek eltérő felhasználói száma és előfizetési hónapjai vannak.</span><span class="sxs-lookup"><span data-stu-id="02ec3-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="02ec3-110">A szerződéssor összegének kiszámításához használt mennyiség a felhasználók számának és az előfizetési hónapoknak a szorzata.</span><span class="sxs-lookup"><span data-stu-id="02ec3-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="02ec3-111">Az ilyen típusú értékesítés támogatása érdekében a Project Operations támogatja a *mennyiségi tényezők* fogalmát.</span><span class="sxs-lookup"><span data-stu-id="02ec3-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="02ec3-112">A mennyiségi tényezők a termékattribútumokra támaszkodnak.</span><span class="sxs-lookup"><span data-stu-id="02ec3-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="02ec3-113">Amikor egy adott termék tulajdonságait konfigurálja, mennyiségi tényezőként jelölheti meg ezen tulajdonságok egy részhalmazát vagy az összes tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="02ec3-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="02ec3-114">A Project Operations ellenőrzi, hogy csak a numerikus vagy a numerikus adattípusú termékjellemzőket jelölte-e meg mennyiségi tényezőként.</span><span class="sxs-lookup"><span data-stu-id="02ec3-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="02ec3-115">Amikor beállított mennyiség tényezőkkel rendelkező terméket vesz fel egy szerződéssorba, a **Mennyiség** mező írásvédett lesz.</span><span class="sxs-lookup"><span data-stu-id="02ec3-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="02ec3-116">Miután megadta a terméktulajdonságok értékeit, amelyek mennyiségi tényezők, a Project Operations kiszámítja az szerződéssor mennyiségét.</span><span class="sxs-lookup"><span data-stu-id="02ec3-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="02ec3-117">Például a Dynamics 365 Sales a következő tulajdonságokkal rendelkezik:</span><span class="sxs-lookup"><span data-stu-id="02ec3-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="02ec3-118">**Felhasználók száma**: A felhasználók száma.</span><span class="sxs-lookup"><span data-stu-id="02ec3-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="02ec3-119">**Hónapok száma**: Az előfizetési hónapok száma.</span><span class="sxs-lookup"><span data-stu-id="02ec3-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="02ec3-120">**Termék termékváltozata**: A raktározási egység (SKU) a termékhez.</span><span class="sxs-lookup"><span data-stu-id="02ec3-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="02ec3-121">A **Felhasználók száma** és a **Hónapok száma** tulajdonságok megjelölhetők mennyiségi tényezőként a terméksor tulajdonságainak szerkesztésével.</span><span class="sxs-lookup"><span data-stu-id="02ec3-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="02ec3-122">Ha mennyiségi tényezőket szeretne létrehozni a termék tulajdonságaiból, hajtsa végre az alábbi lépéseket.</span><span class="sxs-lookup"><span data-stu-id="02ec3-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="02ec3-123">A **Project Operations** alkalmazásban válassza az **Értékesítés-termékek** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="02ec3-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="02ec3-124">Nyissa meg azt a terméket, amelyre vonatkozóan meg kell adnia a mennyiségi tényezőket.</span><span class="sxs-lookup"><span data-stu-id="02ec3-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="02ec3-125">Ügyeljen arra, hogy a termékhez a tulajdonságok már be legyenek beállítva..</span><span class="sxs-lookup"><span data-stu-id="02ec3-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="02ec3-126">A **Projektinformációk** lapon válassza a **Mennyiségi tényezők** lapot.</span><span class="sxs-lookup"><span data-stu-id="02ec3-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="02ec3-127">Az alrácsban válassza az **+ Új mezőszámítás** elemet.</span><span class="sxs-lookup"><span data-stu-id="02ec3-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="02ec3-128">Adja meg a **Mennyiségi tényező** nevét, és jelölje ki a mezőszámításra leképezhető megfelelő tulajdonságértéket.</span><span class="sxs-lookup"><span data-stu-id="02ec3-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="02ec3-129">Az űrlap mentése és bezárása.</span><span class="sxs-lookup"><span data-stu-id="02ec3-129">Save and close the form.</span></span>
7. <span data-ttu-id="02ec3-130">Ismételje meg a 2–6 lépéseket az összes olyan tulajdonságra vonatkozóan, amelyek együttesen alkotják a termék alapú szerződéssor mennyiségét.</span><span class="sxs-lookup"><span data-stu-id="02ec3-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="02ec3-131">A beállított mennyiségi tényezőkkel, amikor a felhasználó létrehoz egy szerződéssor ehhez a termékhez, a szerződéssor mennyisége zárolva van.</span><span class="sxs-lookup"><span data-stu-id="02ec3-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="02ec3-132">A mennyiséget a program az adott szerződéssor tulajdonságértékeinek szorzataként számítja ki.</span><span class="sxs-lookup"><span data-stu-id="02ec3-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>
