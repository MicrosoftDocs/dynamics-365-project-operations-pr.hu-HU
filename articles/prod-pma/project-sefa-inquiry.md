---
title: A szövetségi díjak kiadásaira vonatkozó lekérdezés ütemezése
description: Ez a témakör a szövetségi díjak kiadásával kapcsolatos lekérdezés ütemezésére vonatkozó információkat tartalmaz.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078076"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="08cce-103">A szövetségi díjak kiadásaira vonatkozó lekérdezés ütemezése</span><span class="sxs-lookup"><span data-stu-id="08cce-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08cce-104">Az Igazgatási és Költségvetési Hivatal A-133 körlevele szerint, a szövetségi pénzösszegeket fogadó ügynökségek a könyvvizsgálati követelmények alá tartoznak, amelyeket egyedi auditnak is neveznek.</span><span class="sxs-lookup"><span data-stu-id="08cce-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="08cce-105">A könyvvizsgálati folyamat rendszeresen beszámol a szövetségi támogatások bevételeinek és kiadásainak jelentéséről.</span><span class="sxs-lookup"><span data-stu-id="08cce-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="08cce-106">Az egységes könyvvizsgálati jelentés egy része tartalmazza a szövetségi díjakra (SEFA) vonatkozó kiadások ütemezését.</span><span class="sxs-lookup"><span data-stu-id="08cce-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="08cce-107">A szövetségi díjak kiadásainak ütemezésével kapcsolatos lekérdezés a katalógus a szövetségi hazai támogatás (CFDA) címét és számát, a támogatás számát, a támogatás évét, a szövetségi ügynökség nevét, amely biztosítja az alapokat, valamint az átadó entitás nevét.</span><span class="sxs-lookup"><span data-stu-id="08cce-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="08cce-108">A lekérdezés adott időre szól.</span><span class="sxs-lookup"><span data-stu-id="08cce-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="08cce-109">Ez az időszak általában megegyezik a pénzügyi kimutatás időszakával, amely pénzügyi év.</span><span class="sxs-lookup"><span data-stu-id="08cce-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="08cce-110">A lekérdezés olyan támogatásokat is tartalmaz, amelyek leképezési dátumai a kijelölt időtartományban vannak.</span><span class="sxs-lookup"><span data-stu-id="08cce-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="08cce-111">A **Támogató ügynökség** oszlopa mutatja a támogatási ügyfelet, vagy a továbbadott támogatás esetén a támogató ügynökséget.</span><span class="sxs-lookup"><span data-stu-id="08cce-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="08cce-112">Továbbadott támogatás esetén az **Átadó ügynökség** oszlop mutatja a támogatott ügyfelet.</span><span class="sxs-lookup"><span data-stu-id="08cce-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="08cce-113">Ha a támogatás nem továbbadott támogatás, az **Átadó ügynökség** oszlop üres.</span><span class="sxs-lookup"><span data-stu-id="08cce-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="08cce-114">Az CFDA-klaszter beállítása</span><span class="sxs-lookup"><span data-stu-id="08cce-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="08cce-115">Be kell állítania azokat a CFDA-klasztereket, amelyek a szövetségi díjak kiadásaival kapcsolatos ütemezés során CFDA-számokhoz társíthatók.</span><span class="sxs-lookup"><span data-stu-id="08cce-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="08cce-116">Lépjen a **Projektmenedzsment és könyvelés \> Beállítás \> Támogatások \> Szövetségi belföldi támogatás katalógusa** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="08cce-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="08cce-117">CDFA-klaszter létrehozásához kattintson az **Új** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="08cce-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="08cce-118">Adja meg a klaszter nevét.</span><span class="sxs-lookup"><span data-stu-id="08cce-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="08cce-119">Válassza a **Mentés** lehetőséget a módosítások mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="08cce-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="08cce-120">CFDA-számok beállítása</span><span class="sxs-lookup"><span data-stu-id="08cce-120">Set up CFDA numbers</span></span>

<span data-ttu-id="08cce-121">Be kell állítania azokat a CFDA-számokat, amelyek támogatásokhoz adhatók és a szövetségi díjak kiadásaival kapcsolatos ütemezés lekérdezésében szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="08cce-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="08cce-122">Lépjen a **Projektmenedzsment és könyvelés \> Beállítás \> Támogatások \> Szövetségi belföldi támogatás katalógusának számai** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="08cce-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="08cce-123">CDFA-szám létrehozásához kattintson az **Új** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="08cce-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="08cce-124">A **Szám** oszlopba írja be a CFDA-számot.</span><span class="sxs-lookup"><span data-stu-id="08cce-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="08cce-125">Nyomja le a **Tab** billentyűt.</span><span class="sxs-lookup"><span data-stu-id="08cce-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="08cce-126">A **Leírás** oszlopba írja be a CFDA-címet.</span><span class="sxs-lookup"><span data-stu-id="08cce-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="08cce-127">Nyomja le a **Tab** billentyűt.</span><span class="sxs-lookup"><span data-stu-id="08cce-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="08cce-128">Nem kötelező: a **programklaszter** mezőben adja hozzá a megfelelő CFDA-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="08cce-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="08cce-129">Válassza a **Mentés** lehetőséget a módosítások mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="08cce-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="08cce-130">A szövetségi díjak kiadásának ütemezésére vonatkozó lekérdezés ütemezéséhez a jelentésekre vonatkozó támogatások beállítása</span><span class="sxs-lookup"><span data-stu-id="08cce-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="08cce-131">Lépjen a **Projektmenedzsment és könyvelés \> Támogatások \> Támogatások** részre és válasszon egy meglévő támogatást.</span><span class="sxs-lookup"><span data-stu-id="08cce-131">Go to **Project management and accounting \> Grants \> Grants** , and select an existing grant.</span></span>
2. <span data-ttu-id="08cce-132">A **telepítés** gyorslapon, a **szövetségi belföldi támogatási katalógus** mezőben a CFDA-számot rendelje hozzá.</span><span class="sxs-lookup"><span data-stu-id="08cce-132">On the **Setup** FastTab, in the  **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="08cce-133">A támogatás CFDA száma határozza meg a jelentéskészítéshez szükséges CFDA-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="08cce-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="08cce-134">A **kapcsolatfelvételi adatok** gyorslapon adja meg a támogatóra vonatkozó információkat a következő lépések végrehajtásával:</span><span class="sxs-lookup"><span data-stu-id="08cce-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="08cce-135">A **támogatott ügyfél** mezőben adja meg a támogatásért felelős ügyfelet.</span><span class="sxs-lookup"><span data-stu-id="08cce-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="08cce-136">Meglévő támogatás esetén előfordulhat, hogy a rendszer ezeket az adatokat már megadta.</span><span class="sxs-lookup"><span data-stu-id="08cce-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="08cce-137">Adja meg, hogy a támogatási ügyfél a finanszírozó-e.</span><span class="sxs-lookup"><span data-stu-id="08cce-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="08cce-138">Ha a támogatási ügyfél a finanszírozó, akkor hagyja üresen az **átadó** jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="08cce-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="08cce-139">Ha egy másik ügyfél a finanszírozó, és a támogatási ügyfél felelős a pénz kiadásáért és nyomon követéséért, jelölje be az **átadó** jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="08cce-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="08cce-140">Ha az előző lépésben bejelölte az **átadó** jelölőnégyzetet, akkor a **támogatási Ügynökség** mezőben adja meg azt az ügyfelet, aki a támogatást nyújtotta.</span><span class="sxs-lookup"><span data-stu-id="08cce-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="08cce-141">A támogatási ügynökség és a támogatási ügyfél nem lehet azonos ügyfél.</span><span class="sxs-lookup"><span data-stu-id="08cce-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="08cce-142">Példa az átadói támogatásra:</span><span class="sxs-lookup"><span data-stu-id="08cce-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="08cce-143">A szövetségi kormány egy állam számára infrastrukturális projektet finanszírozott.</span><span class="sxs-lookup"><span data-stu-id="08cce-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="08cce-144">A szövetségi kormány adta a pénzt, amit az állam elkölthet.</span><span class="sxs-lookup"><span data-stu-id="08cce-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="08cce-145">Ebben az esetben a szövetségi kormány a támogató ügynökség, és az állam a támogatási ügyfél.</span><span class="sxs-lookup"><span data-stu-id="08cce-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="08cce-146">Amikor először bekapcsolja a szolgáltatást, a rendszer a kezdeti CFDA számokat a támogatásban szereplő meglévő számok használatával adja meg.</span><span class="sxs-lookup"><span data-stu-id="08cce-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="08cce-147">Támogatások kizárása a SEFA-jelentésből a támogatás típusa alapján</span><span class="sxs-lookup"><span data-stu-id="08cce-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="08cce-148">Válassza a **Projektmenedzsment és könyvelés \> Beállítás \> Támogatás \> Támogatási típus** elemet.</span><span class="sxs-lookup"><span data-stu-id="08cce-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="08cce-149">Az **Alapértelmezett információ** gyorslapon jelölje be a **Szövetségi díjak kiadásainak ütemezéséből való kizárás** jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="08cce-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="08cce-150">Válassza a **Mentés** lehetőséget a módosítások mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="08cce-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="08cce-151">A szövetségi díjak kiadásainak ütemezésére vonatkozó lekérdezés futtatása</span><span class="sxs-lookup"><span data-stu-id="08cce-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="08cce-152">Nyissa meg a **Projektkezelés és könyvelés \> Lekérdezések és jelentések \> Támogatás lekérdezése \> Szövetségi díjak kiadásainak ütemezése** pontot.</span><span class="sxs-lookup"><span data-stu-id="08cce-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="08cce-153">A **Paraméterek** szakaszban kövesse az alábbi lépéseket:</span><span class="sxs-lookup"><span data-stu-id="08cce-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="08cce-154">A **dátumtartomány** mezőben jelölje ki a dátumtartomány kódját.</span><span class="sxs-lookup"><span data-stu-id="08cce-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="08cce-155">Másik lehetőségként a **kezdő dátum** és a **záró dátum** mezőkben adhatja meg a dátumtartomány értékét.</span><span class="sxs-lookup"><span data-stu-id="08cce-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="08cce-156">Nem kötelező: Ha csak a számlázott tranzakciókat kívánja bevételként szerepeltetni a lekérdezésben, akkor állítsa az **csak a számlázott bevétel felvétele** lehetőséget **Igen** értékre.</span><span class="sxs-lookup"><span data-stu-id="08cce-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="08cce-157">Oszlopok</span><span class="sxs-lookup"><span data-stu-id="08cce-157">Columns</span></span>

<span data-ttu-id="08cce-158">A szövetségi díjak kiadásainak ütemezésére vonatkozó lekérdezés a következő oszlopokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="08cce-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="08cce-159">A Szövetségi belföldi támogatás katalógusának klaszterneve</span><span class="sxs-lookup"><span data-stu-id="08cce-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="08cce-160">Ttámogatási ügynökség</span><span class="sxs-lookup"><span data-stu-id="08cce-160">Grantor agency</span></span>
- <span data-ttu-id="08cce-161">Átadó ügynökség</span><span class="sxs-lookup"><span data-stu-id="08cce-161">Pass-through agency</span></span>
- <span data-ttu-id="08cce-162">Támogatás neve</span><span class="sxs-lookup"><span data-stu-id="08cce-162">Grant name</span></span>
- <span data-ttu-id="08cce-163">Támogatási azonosító</span><span class="sxs-lookup"><span data-stu-id="08cce-163">Grant ID</span></span>
- <span data-ttu-id="08cce-164">Támogatási pályázat azonosítója</span><span class="sxs-lookup"><span data-stu-id="08cce-164">Grant application ID</span></span>
- <span data-ttu-id="08cce-165">A Szövetségi belföldi támogatás katalógusa</span><span class="sxs-lookup"><span data-stu-id="08cce-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="08cce-166">Nyugták</span><span class="sxs-lookup"><span data-stu-id="08cce-166">Receipts</span></span>
- <span data-ttu-id="08cce-167">Kiadások</span><span class="sxs-lookup"><span data-stu-id="08cce-167">Expenditures</span></span>
