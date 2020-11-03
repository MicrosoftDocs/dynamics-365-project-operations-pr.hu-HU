---
title: A vállalatközi projektek számlázásának konfigurálása
description: Ez a témakör azt mutatja be, hogyan állítható be projektszámlázás a szervezet két vállalata között.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cb53cb63ee11082146455ec9f13790501dc3d1d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078151"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="ceee1-103">A vállalatközi projektek számlázásának konfigurálása</span><span class="sxs-lookup"><span data-stu-id="ceee1-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ceee1-104">Ez a témakör azt mutatja be, hogyan állítható be projektszámlázás a szervezet két vállalata között.</span><span class="sxs-lookup"><span data-stu-id="ceee1-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="ceee1-105">Ez a feladat a USSI adatkészletet használja.</span><span class="sxs-lookup"><span data-stu-id="ceee1-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="ceee1-106">A Navigáció ablaktáblán nyissa meg a következőt: **Modulok > Kötelezettségek > Szállítók > Minden szállító**.</span><span class="sxs-lookup"><span data-stu-id="ceee1-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="ceee1-107">Keresse meg, majd jelölje ki a kívánt rekordot a **Minden szállító** listán.</span><span class="sxs-lookup"><span data-stu-id="ceee1-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="ceee1-108">A Művelet ablaktáblában válassza az **Általános** elemet.</span><span class="sxs-lookup"><span data-stu-id="ceee1-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="ceee1-109">Válassza a **Vállalatközi** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="ceee1-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="ceee1-110">A vállalatközi kereskedés engedélyezéséhez állítsa az **Aktív** paramétert **Igen** értékre.</span><span class="sxs-lookup"><span data-stu-id="ceee1-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="ceee1-111">Adjon meg vagy jelöljön ki egy értéket a **Vevő vállalat** mezőben.</span><span class="sxs-lookup"><span data-stu-id="ceee1-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="ceee1-112">Adjon meg vagy jelöljön ki egy értéket a **Saját fiók** mezőben.</span><span class="sxs-lookup"><span data-stu-id="ceee1-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="ceee1-113">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="ceee1-113">Select **Save**.</span></span>
9. <span data-ttu-id="ceee1-114">Zárja be a lapokat, és térjen vissza a kezdőlapra.</span><span class="sxs-lookup"><span data-stu-id="ceee1-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="ceee1-115">Az ablaktáblában kattintson a **Modulok > Projektvezetés és könyvelés > Beállítás > Projektvezetési és könyvelési paraméterek** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="ceee1-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="ceee1-116">Válassza a **Vállalatközi** fület.</span><span class="sxs-lookup"><span data-stu-id="ceee1-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="ceee1-117">A vállalatközi erőforrás-ütemezés és az időnyilvántartások engedélyezéséhez mozgassa a csúszkát az **Igen** értékre.</span><span class="sxs-lookup"><span data-stu-id="ceee1-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="ceee1-118">A listán jelölje meg a kiválasztott sort.</span><span class="sxs-lookup"><span data-stu-id="ceee1-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="ceee1-119">Válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="ceee1-119">Select **New**.</span></span>
15. <span data-ttu-id="ceee1-120">Adjon meg vagy jelöljön ki egy értéket a **Kölcsönbe vevő jogi személy** mezőben.</span><span class="sxs-lookup"><span data-stu-id="ceee1-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="ceee1-121">Jelölje be az **Elhatárolt bevételhez** tartozó jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="ceee1-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="ceee1-122">Adjon meg vagy jelöljön ki egy értéket az **Alapértelmezett időnyilvántartási kategória** mezőben.</span><span class="sxs-lookup"><span data-stu-id="ceee1-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="ceee1-123">Adjon meg vagy jelöljön ki egy értéket az **Alapértelmezett költségkategória** mezőben.</span><span class="sxs-lookup"><span data-stu-id="ceee1-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="ceee1-124">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="ceee1-124">Select **Save**.</span></span>
20. <span data-ttu-id="ceee1-125">Zárja be a lapot.</span><span class="sxs-lookup"><span data-stu-id="ceee1-125">Close the page.</span></span>
21. <span data-ttu-id="ceee1-126">Az ablaktáblán kattintson a **Modulok > Projektvezetés és könyvelés > Beállítás > Feladás > Főkönyvi feladás beállítása** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="ceee1-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="ceee1-127">A **Főkönyvi számlatípusok** mezőben válasszon a lehetőségek közül.</span><span class="sxs-lookup"><span data-stu-id="ceee1-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="ceee1-128">Válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="ceee1-128">Select **New**.</span></span>
24. <span data-ttu-id="ceee1-129">Az új sor **Fő számla** mezőjében határozza meg a kívánt értékeket.</span><span class="sxs-lookup"><span data-stu-id="ceee1-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="ceee1-130">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="ceee1-130">Select **Save**.</span></span>
26. <span data-ttu-id="ceee1-131">Zárja be a lapot.</span><span class="sxs-lookup"><span data-stu-id="ceee1-131">Close the page.</span></span>
27. <span data-ttu-id="ceee1-132">Az ablaktáblában kattintson a **Modulok > Projektvezetés és könyvelés > Beállítás > Árak > Transzferár** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="ceee1-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="ceee1-133">Válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="ceee1-133">Select **New**.</span></span>
29. <span data-ttu-id="ceee1-134">Írjon be egy dátumot az **Érvényesség dátuma** mezőbe.</span><span class="sxs-lookup"><span data-stu-id="ceee1-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="ceee1-135">Adjon meg vagy jelöljön ki egy értéket a **Kölcsönbe vevő jogi személy** mezőben.</span><span class="sxs-lookup"><span data-stu-id="ceee1-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="ceee1-136">Válasszon a lehetőségek közül a **Transzferármodell** mezőben.</span><span class="sxs-lookup"><span data-stu-id="ceee1-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="ceee1-137">Írjon be egy számot az **Árképzés** mezőbe.</span><span class="sxs-lookup"><span data-stu-id="ceee1-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="ceee1-138">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="ceee1-138">Select **Save**.</span></span>

