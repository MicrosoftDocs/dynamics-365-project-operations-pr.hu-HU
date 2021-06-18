---
title: Speciális szerződések létrehozása folyamatalapú számlázáshoz
description: Ez a témakör elmagyarázza, hogyan hozhatók létre a projektszerződések, hogy a befejezett munkák aránya alapján számlákat lehessen létrehozni az ügyfelek számára.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3b445488100e0a8335a05505405953b173ff836c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999674"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="4d970-103">Speciális szerződések létrehozása folyamatalapú számlázáshoz</span><span class="sxs-lookup"><span data-stu-id="4d970-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d970-104">Ez a témakör elmagyarázza, hogyan hozhatók létre a projektszerződések, hogy a befejezett munkák aránya alapján számlákat lehessen létrehozni az ügyfelek számára.</span><span class="sxs-lookup"><span data-stu-id="4d970-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="4d970-105">A számlaösszegeket a program automatikusan kiszámítja a projekthez beállított, meghatározott költségvetési kategóriákhoz.</span><span class="sxs-lookup"><span data-stu-id="4d970-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="4d970-106">A számla időzítését akkor adja meg a program, amikor egyezteti a projektszerződést az ügyféllel.</span><span class="sxs-lookup"><span data-stu-id="4d970-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="4d970-107">Az ebben a témakör található eljárások segítségével beállíthat egy szerződést, egy társított projektet és a számlázási szabályokat, amelyek kiszámítják a projekthez beállított munkavégzési kategóriákhoz tartozó számlaösszegeket.</span><span class="sxs-lookup"><span data-stu-id="4d970-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="4d970-108">A szerződés és a projekt létrehozása után beállíthatja a projekt részleteit.</span><span class="sxs-lookup"><span data-stu-id="4d970-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="4d970-109">Megadhatja például a tevékenységeket, és a projekthez rendelheti a dolgozókat.</span><span class="sxs-lookup"><span data-stu-id="4d970-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="4d970-110">Példa</span><span class="sxs-lookup"><span data-stu-id="4d970-110">Example</span></span>

<span data-ttu-id="4d970-111">Szervezete egy szoftverfejlesztő cég.</span><span class="sxs-lookup"><span data-stu-id="4d970-111">Your organization is a software development firm.</span></span> <span data-ttu-id="4d970-112">Ön vállalja, hogy kidolgozza a bérszámfejtési csomagot az ügyfél számára a teljes 20 000 USA dolláros (USD) díjért.</span><span class="sxs-lookup"><span data-stu-id="4d970-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="4d970-113">A szervezete vállalja, hogy a projekt adott százalékának végrehajtásakor számláz az ügyfélnek.</span><span class="sxs-lookup"><span data-stu-id="4d970-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="4d970-114">A következő projektkategóriákat állíthatja be a munkához, hogy a számlázási folyamatban használhatók legyenek:</span><span class="sxs-lookup"><span data-stu-id="4d970-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="4d970-115">Konzultáció</span><span class="sxs-lookup"><span data-stu-id="4d970-115">Consulting</span></span>
- <span data-ttu-id="4d970-116">Tervezés</span><span class="sxs-lookup"><span data-stu-id="4d970-116">Design</span></span>
- <span data-ttu-id="4d970-117">Telepítés</span><span class="sxs-lookup"><span data-stu-id="4d970-117">Installation</span></span>

<span data-ttu-id="4d970-118">Olyan számlázási szabályokat is kell beállítani, amelyek automatikusan kiszámítják a számlaösszegeket az egyes kategóriákhoz tartozó befejezett projektmunka-mennyiségek százalékos arányai alapján.</span><span class="sxs-lookup"><span data-stu-id="4d970-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="4d970-119">A költségvetés-kezelő a projektkategóriák költségvetését hozza létre.</span><span class="sxs-lookup"><span data-stu-id="4d970-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="4d970-120">A befejezett munkák összegét a rendszer automatikusan kiszámítja a tényleges munkamennyiség százalékában, a tervezett költségvetési összegekkel összehasonlítva.</span><span class="sxs-lookup"><span data-stu-id="4d970-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4d970-121">Előfeltételek</span><span class="sxs-lookup"><span data-stu-id="4d970-121">Prerequisites</span></span>

<span data-ttu-id="4d970-122">A számlázási szabályokat használó projekt létrehozása előtt be kell állítania a számlázási szabályok számsorozatait és a folyamatszámlák elszámlálásához használt díjnaplót.</span><span class="sxs-lookup"><span data-stu-id="4d970-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="4d970-123">Lépjen a **Projektmenedzsment és könyvelés** \> **Beállítás** \> **Projektmenedzsment és könyvelési paraméterek** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="4d970-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="4d970-124">A **Projektmenedzsment és könyvelési paraméterek** oldalon a **Számsorozatok** lapon állítsa be a számlázási szabályok létrehozásakor használni kívánt számsorozatot.</span><span class="sxs-lookup"><span data-stu-id="4d970-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="4d970-125">Lépjen a **Projektvezetés és könyvelés** \> **Naplók** \> **Díj** elemre.</span><span class="sxs-lookup"><span data-stu-id="4d970-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="4d970-126">A **Díjnapló** lapon válassza az **Új** lehetőséget, majd írja be a napló nevét.</span><span class="sxs-lookup"><span data-stu-id="4d970-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="4d970-127">Szerződés létrehozása folyamatban lévő számlázásokhoz</span><span class="sxs-lookup"><span data-stu-id="4d970-127">Create a contract for progress billings</span></span>

<span data-ttu-id="4d970-128">Ezzel az eljárással hozhat létre projektszerződést egy rögzített árú projekthez.</span><span class="sxs-lookup"><span data-stu-id="4d970-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="4d970-129">A projektszámlát akkor hozza létre, amikor a projekten végrehajtott munkavégzés eléri a megadott százalékértéket.</span><span class="sxs-lookup"><span data-stu-id="4d970-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="4d970-130">Lépjen a **Projektvezetés és könyvelés** \> **Projektek** \> **Projektszerződések** elemre.</span><span class="sxs-lookup"><span data-stu-id="4d970-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="4d970-131">A **Projektszerződések** oldalon válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="4d970-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="4d970-132">Az **Új projektszerződés** párbeszédablakon állítsa be a következő mezőket:</span><span class="sxs-lookup"><span data-stu-id="4d970-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="4d970-133">**Név**</span><span class="sxs-lookup"><span data-stu-id="4d970-133">**Name**</span></span>
    - <span data-ttu-id="4d970-134">**Finanszírozás típusa**</span><span class="sxs-lookup"><span data-stu-id="4d970-134">**Funding type**</span></span>
    - <span data-ttu-id="4d970-135">**Finanszírozási forrás**</span><span class="sxs-lookup"><span data-stu-id="4d970-135">**Funding source**</span></span>
    - <span data-ttu-id="4d970-136">**Értékesítési pénznem** – Ez a pénznem alapértelmezés szerint a projekt szerződéshez társított vevői számlákhoz használható.</span><span class="sxs-lookup"><span data-stu-id="4d970-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="4d970-137">Egy adott vevői számlán azonban megváltoztathatja az értékesítési pénznemet.</span><span class="sxs-lookup"><span data-stu-id="4d970-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="4d970-138">Kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="4d970-138">Select **OK**.</span></span> <span data-ttu-id="4d970-139">A rendszer átmásolja az információkat a **projektszerződések** oldal fejlécébe.</span><span class="sxs-lookup"><span data-stu-id="4d970-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="4d970-140">A **projektszerződések** lapon töltse ki a projekthez szükséges összes információt.</span><span class="sxs-lookup"><span data-stu-id="4d970-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="4d970-141">Projekt létrehozása folyamatban lévő számlázásokhoz</span><span class="sxs-lookup"><span data-stu-id="4d970-141">Create a project for progress billings</span></span>

<span data-ttu-id="4d970-142">A következő lépések végrehajtásával hozhat létre projekteket és a projekt szerződéshez kapcsolódó alprojekteket.</span><span class="sxs-lookup"><span data-stu-id="4d970-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="4d970-143">Lépjen a **Projektvezetés és könyvelés** \> **Projektek** \> **Minden projekt** elemre.</span><span class="sxs-lookup"><span data-stu-id="4d970-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="4d970-144">Az **Összes projekt** lapon válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="4d970-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="4d970-145">Az **új projekt** párbeszédpanel **projekttípus** mezőjében válassza az **idő és az anyag** elemet.</span><span class="sxs-lookup"><span data-stu-id="4d970-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="4d970-146">Válasszon ki egy projektcsoportot.</span><span class="sxs-lookup"><span data-stu-id="4d970-146">Select a project group.</span></span> <span data-ttu-id="4d970-147">A projektcsoport határozza meg a csoporthoz rendelt projektek feladási információit.</span><span class="sxs-lookup"><span data-stu-id="4d970-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="4d970-148">Válassza a **Projekt létrehozása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="4d970-148">Select **Create project**.</span></span>
6. <span data-ttu-id="4d970-149">A projekt létrehozása után állítsa be a projekt fázisát **folyamatban** értékre.</span><span class="sxs-lookup"><span data-stu-id="4d970-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="4d970-150">Költségvetés létrehozása projekthez</span><span class="sxs-lookup"><span data-stu-id="4d970-150">Create a budget for a project</span></span>

<span data-ttu-id="4d970-151">A költségvetési kategóriák segítségével a rendszer automatikusan kiszámítja a számlaösszegeket az egyes kategóriákhoz tartozó befejezett munkamennyiségek százalékos arányai alapján.</span><span class="sxs-lookup"><span data-stu-id="4d970-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="4d970-152">A következő lépések végrehajtásával költségvetési kategóriákat hozhat létre a becsült költségekhez.</span><span class="sxs-lookup"><span data-stu-id="4d970-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="4d970-153">Lépjen a **Projektvezetés és könyvelés** \> **Projektek** \> **Minden projekt** elemre.</span><span class="sxs-lookup"><span data-stu-id="4d970-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="4d970-154">Az **Összes projekt** lapon jelölje ki a kívánt projektet, és nyissa meg azt.</span><span class="sxs-lookup"><span data-stu-id="4d970-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="4d970-155">A **projektek** lap művelet ablaktáblájának **tervezés** lapján, a **költségvetés** csoportjában válassza a **projektköltségvetés** elemet.</span><span class="sxs-lookup"><span data-stu-id="4d970-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="4d970-156">A **projektköltségvetés** lapon adjon meg egy becsült költséget a projekt egyes kategóriáira vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="4d970-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="4d970-157">Számlázási szabályok létrehozása a folyamatban lévő számlázáshoz</span><span class="sxs-lookup"><span data-stu-id="4d970-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="4d970-158">Lépjen a **Projektvezetés és könyvelés** \> **Projektek** \> **Projektszerződések** elemre.</span><span class="sxs-lookup"><span data-stu-id="4d970-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="4d970-159">A **Projektszerződések** oldalon válassza ki és nyissa meg a projektszerződést.</span><span class="sxs-lookup"><span data-stu-id="4d970-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="4d970-160">A projektszerződés oldalon **Számlázási szabályok** gyorslapján válassza a **Hozzáadás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="4d970-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="4d970-161">A **Számlázási szabály** lap **sortípusa** mezőjében válassza a **folyamatjelző** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="4d970-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="4d970-162">Adja meg a szerződés teljes értékét a **Számlázási szabály sorának részletei** gyorslapon, a **Szerződés értéke** mezőben.</span><span class="sxs-lookup"><span data-stu-id="4d970-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="4d970-163">A **Kategória** mezőben válassza ki, hogy milyen kategóriába szeretné könyvelni a díjtranzakciót.</span><span class="sxs-lookup"><span data-stu-id="4d970-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="4d970-164">A **Projekt** mezőben jelölje ki a számlázási szabályt használó projektet.</span><span class="sxs-lookup"><span data-stu-id="4d970-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="4d970-165">Nem kötelező: a számlázási szabályt további projektekhez rendelje hozzá.</span><span class="sxs-lookup"><span data-stu-id="4d970-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="4d970-166">A **Projekt** gyorslapon, a **rendelkezésre álló projektek** szakaszban jelöljön ki egy projektet, majd a jobb nyílra kattintva adja hozzá a projektet a **kijelölt projektek** szakaszhoz.</span><span class="sxs-lookup"><span data-stu-id="4d970-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="4d970-167">Nem kötelező: a százalékos összeg kiszámítása, amelyet az ügyfél visszatart a számla kifizetéséről.</span><span class="sxs-lookup"><span data-stu-id="4d970-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="4d970-168">A **fizetési adatok megőrzési feltételei** gyorslapon válassza ki a finanszírozási forrást, majd az **Adatmegőrzési százalék** mezőben adja meg a megőrzési százalékot.</span><span class="sxs-lookup"><span data-stu-id="4d970-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="4d970-169">Ismételje meg ezeket a lépéseket, ha további számlázási szabályokat szeretne létrehozni a projektszerződéshez.</span><span class="sxs-lookup"><span data-stu-id="4d970-169">Repeat these steps to create additional billing rules for the project contract.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]