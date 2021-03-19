---
title: Összetett egységek kezelése, például felhasználónként vagy havonta, termékalapú árajánlatsoroknál - Lite
description: Ez a témakör az összetett egységek kezeléséről tartalmaz tájékoztatást a termékalapú árajánlatsorok esetében.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b4a075ae5a7329f241cc31afceab0e085c771f72
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272886"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a><span data-ttu-id="4db73-103">Összetett egységek kezelése, például felhasználónként vagy havonta, termékalapú árajánlatsoroknál - Lite</span><span class="sxs-lookup"><span data-stu-id="4db73-103">Managing complex units such as per-user, per-month for product-based quote lines - lite</span></span>

<span data-ttu-id="4db73-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="4db73-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4db73-105">A Dynamics 365 Project Operations mennyiségi tényezőket alkalmaz az előfizetésen alapuló termékek értékesítésének támogatására.</span><span class="sxs-lookup"><span data-stu-id="4db73-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="4db73-106">Az előfizetésen alapuló termékek esetében az árajánlat vagy a projektszerződés sorában szereplő mennyiséget a felhasználói/hónap számában fejezik ki.</span><span class="sxs-lookup"><span data-stu-id="4db73-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="4db73-107">Az előfizetési szoftver ára általában a katalógusban kerül tárolásra havi felhasználónkénti árként.</span><span class="sxs-lookup"><span data-stu-id="4db73-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="4db73-108">Az értékesítési folyamat során az árajánlatsorban a felhasználónkénti havi ár általában az IT-értékesítési ügynökkel való egyeztetés után és az általa megadott árengedménnyel születik meg.</span><span class="sxs-lookup"><span data-stu-id="4db73-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="4db73-109">Minden egyes ügyletnek eltérő felhasználói száma és előfizetési hónapjai vannak.</span><span class="sxs-lookup"><span data-stu-id="4db73-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="4db73-110">Az árajánlatsor kiszámításához használt mennyiség a felhasználók számának és az előfizetési hónapoknak a szorzata.</span><span class="sxs-lookup"><span data-stu-id="4db73-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="4db73-111">Az ilyen típusú értékesítés támogatása érdekében a Project Operations bevezette a mennyiségi tényezők fogalmát.</span><span class="sxs-lookup"><span data-stu-id="4db73-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="4db73-112">A mennyiségi tényezők a Dynamics 365 termékattribútumaira támaszkodnak.</span><span class="sxs-lookup"><span data-stu-id="4db73-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="4db73-113">Amikor egy adott termék tulajdonságait konfigurálja, a Project Operations lehetővé teszi, hogy mennyiségi tényezőként jelölje meg ezen tulajdonságok egy részhalmazát vagy az összes tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="4db73-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="4db73-114">A Project Operations ellenőrzi, hogy csak a numerikus vagy a numerikus adattípusú termékjellemzőket jelölte-e meg mennyiségi tényezőként.</span><span class="sxs-lookup"><span data-stu-id="4db73-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="4db73-115">Ha mennyiségi tényezőket tartalmazó terméket ad hozzá egy árajánlatsorhoz, a **Mennyiség** mező írásvédett lesz.</span><span class="sxs-lookup"><span data-stu-id="4db73-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="4db73-116">Miután megadta azon terméktulajdonságok értékeit, amelyek mennyiségi tényezők, a Project Operations kiszámítja az árajánlatsor mennyiségét.</span><span class="sxs-lookup"><span data-stu-id="4db73-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="4db73-117">Például a Dynamics 365 Sales a következő tulajdonságokkal rendelkezik:</span><span class="sxs-lookup"><span data-stu-id="4db73-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="4db73-118">**Felhasználók száma**: A felhasználók száma</span><span class="sxs-lookup"><span data-stu-id="4db73-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="4db73-119">**Hónapok száma**: Az előfizetési hónapok száma</span><span class="sxs-lookup"><span data-stu-id="4db73-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="4db73-120">**Termék cikkszáma**</span><span class="sxs-lookup"><span data-stu-id="4db73-120">**Product SKU**</span></span>

<span data-ttu-id="4db73-121">A **Felhasználók száma** és a **Hónapok száma** tulajdonságok megjelölhetők mennyiségi tényezőként a terméksor tulajdonságainak szerkesztésével.</span><span class="sxs-lookup"><span data-stu-id="4db73-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="4db73-122">Ha mennyiségi tényezőket szeretne létrehozni a termék tulajdonságaiból, hajtsa végre a következő lépéseket:</span><span class="sxs-lookup"><span data-stu-id="4db73-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="4db73-123">A Project Operations bal oldali ablaktáblájában nyissa meg az **Értékesítés** > **Termékek** menüpontot.</span><span class="sxs-lookup"><span data-stu-id="4db73-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="4db73-124">Nyissa meg azt a terméket, amelyre vonatkozóan mennyiségi tényezőket kell konfigurálnia.</span><span class="sxs-lookup"><span data-stu-id="4db73-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="4db73-125">Győződjön meg róla, hogy a termékhez már konfigurálva vannak tulajdonságok.</span><span class="sxs-lookup"><span data-stu-id="4db73-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="4db73-126">A termékre vonatkozó **Projektinformációk** oldalon jelölje ki a **Mennyiségi tényezők** lapot.</span><span class="sxs-lookup"><span data-stu-id="4db73-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="4db73-127">Az alrácsban válassza az **+ Új mezőszámítás** elemet.</span><span class="sxs-lookup"><span data-stu-id="4db73-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="4db73-128">Adja meg a mennyiségi tényező nevét, és jelölje ki a mezőszámításra leképezhető megfelelő tulajdonságértéket.</span><span class="sxs-lookup"><span data-stu-id="4db73-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="4db73-129">Az űrlap mentése és bezárása.</span><span class="sxs-lookup"><span data-stu-id="4db73-129">Save and close the form.</span></span> <span data-ttu-id="4db73-130">Ismételje meg ezeket a lépéseket minden olyan tulajdonságra vonatkozóan, amelyet a termékalapú árajánlatsor mennyiségének a kiszámításához használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="4db73-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="4db73-131">Ha egy termékhez termékalapú árajánlatsort hoz létre, az árajánlatsor mennyisége zárolva lesz.</span><span class="sxs-lookup"><span data-stu-id="4db73-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="4db73-132">A mennyiséget az adott árajánlatsorhoz tartozó tulajdonságértékek szorzatával számítja ki a program.</span><span class="sxs-lookup"><span data-stu-id="4db73-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]