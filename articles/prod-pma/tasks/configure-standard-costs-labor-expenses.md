---
title: A munkaerő és a kiadások elszámolóárainak konfigurálása
description: Ez a témakör azt mutatja be, hogyan állíthatók be a munkaerő és a kiadások elszámolóárai egy projekten belül.
author: Yowelle
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 517e5ae776cff18aec81e5446a7aaedfba61ac0c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011014"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="2ff0a-103">A munkaerő és a kiadások elszámolóárainak konfigurálása</span><span class="sxs-lookup"><span data-stu-id="2ff0a-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ff0a-104">Ez a témakör azt mutatja be, hogyan állíthatók be a munkaerő és a kiadások elszámolóárai egy projekten belül.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="2ff0a-105">Ez a feladat a USSI adatkészletet használja.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="2ff0a-106">Az ablaktáblán kattintson a **Modulok > Projektvezetés és könyvelés > Beállítás > Árak > Önköltségi ár (óra)** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="2ff0a-107">Válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-107">Select **New**.</span></span>
3. <span data-ttu-id="2ff0a-108">Írjon be egy dátumot az **Érvényesség dátuma** mezőbe.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="2ff0a-109">Írjon be egy számot az **Önköltségi ár** mezőbe.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="2ff0a-110">Itt beállíthat egy elszámolóárat az adott projektkategóriához, illetve beállíthat önköltségi árat a munkavállalók száma, a projektszám, a kategória, a dátum vagy ezek tetszőleges kombinációja alapján.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="2ff0a-111">Az alkalmazott önköltségi ár a legrészletesebb szintű önköltségi ár.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="2ff0a-112">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-112">Select **Save**.</span></span>
6. <span data-ttu-id="2ff0a-113">Az ablaktáblán kattintson a **Modulok > Projektvezetés és könyvelés > Beállítás > Árak > Eladási ár (óra)** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="2ff0a-114">Válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-114">Select **New**.</span></span>
8. <span data-ttu-id="2ff0a-115">Írjon be egy dátumot az **Érvényesség dátuma** mezőbe.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="2ff0a-116">Válasszon az **Érvényes** mezőben lévő lehetőségek közül.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="2ff0a-117">Írjon be egy számot az **Árképzés** mezőbe.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="2ff0a-118">Itt beállíthat egy szabványos eladási árat az óratranzakciókhoz vagy a projektkategóriákhoz.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="2ff0a-119">Emellett az eladási árakat a munkavállalók száma, a projektszám, a kategória, a tranzakció dátuma vagy ezek bármilyen kombinációja szerint is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="2ff0a-120">A tényleges eladási ár, amelyet a rendszer akkor alkalmaz, amikor egy munkavállaló tranzakciót ad meg az óranaplóban, a legrészletesebb szintű eladási ár.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="2ff0a-121">Ha például egy általános eladási ár és egy munkavállaló-specifikus értékesítési ár is be van állítva, akkor a rendszer a munkavállaló-specifikus értékesítési árat használja.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="2ff0a-122">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-122">Select **Save**.</span></span>
12. <span data-ttu-id="2ff0a-123">Zárja be a lapot.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-123">Close the page.</span></span>
13. <span data-ttu-id="2ff0a-124">Az ablaktáblán kattintson a **Modulok > Projektvezetés és könyvelés > Beállítás > Árak > Önköltségi ár (kiadás)** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="2ff0a-125">Válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-125">Select **New**.</span></span>
15. <span data-ttu-id="2ff0a-126">Írjon be egy dátumot az **Érvényesség dátuma** mezőbe.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="2ff0a-127">Írjon be egy számot az **Önköltségi ár** mezőbe.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="2ff0a-128">Több mező is kitölthető, de legalább ennyi szükséges a rekord mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="2ff0a-129">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-129">Select **Save**.</span></span>
18. <span data-ttu-id="2ff0a-130">Az ablaktáblán kattintson a **Modulok > Projektvezetés és könyvelés > Beállítás > Árak > Eladási ár (kiadás)** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="2ff0a-131">Válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-131">Select **New**.</span></span>
20. <span data-ttu-id="2ff0a-132">Írjon be egy dátumot az **Érvényesség dátuma** mezőbe.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="2ff0a-133">Válasszon az **Érvényes** mezőben lévő lehetőségek közül.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="2ff0a-134">Írjon be egy számot az **Árképzés** mezőbe.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="2ff0a-135">A tényleges eladási ár, amelyet akkor alkalmaz a rendszer, amikor egy munkavállaló tranzakciókat ad meg egy Költségnaplóban, a legrészletesebb szintű eladási ár.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="2ff0a-136">Ha például egy általános és egy munkavállaló-specifikus értékesítési ár is be van állítva, akkor a rendszer a munkavállaló-specifikus értékesítési árat használja.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="2ff0a-137">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-137">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]