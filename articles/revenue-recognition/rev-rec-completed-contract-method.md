---
title: Bevételi becslések kezelése
description: Ez a témakör információt nyújt a bevételi becslések használatához a projektekhez.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b63346f56db8b906e5aa45940465bdb18e3df480
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279006"
---
# <a name="manage-revenue-estimates"></a><span data-ttu-id="bc8b3-103">Bevételi becslések kezelése</span><span class="sxs-lookup"><span data-stu-id="bc8b3-103">Manage revenue estimates</span></span>

<span data-ttu-id="bc8b3-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="bc8b3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="bc8b3-105">Bevételi becsléseket hozhat létre, számíthat ki, könyvelhet, sztornírozhat vagy szűntethet meg.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-105">You can create, calculate, post, reverse, or eliminate revenue estimates.</span></span> <span data-ttu-id="bc8b3-106">Ezt manuálisan vagy egy időszakos folyamattal teheti meg.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-106">You can do this either manually or by using a periodic process.</span></span> <span data-ttu-id="bc8b3-107">Ez a témakör információt nyújt a bevételi becslések használatához a projektekhez.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-107">This topic provides information about how to work with revenue estimates for projects.</span></span>

### <a name="manage-revenue-estimates-manually"></a><span data-ttu-id="bc8b3-108">Bevételi becslések kezelése manuálisan</span><span class="sxs-lookup"><span data-stu-id="bc8b3-108">Manage revenue estimates manually</span></span>

<span data-ttu-id="bc8b3-109">A rögzített bevételbecslési projektben vagy a **Becslés lekérdezés** oldalon (**Projektvezetés és könyvelés** > **Jelentések és lekérdezések** > **Becslések lekérdezése és jelentések**) válassza a **Becslések** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-109">On the fixed price revenue estimate project or the **Estimate inquiry** page (**Project management and accounting** > **Reports and inquiries** > **Estimates inquiries and reports**), select **Estimates**.</span></span>

### <a name="manage-revenue-estimates-using-a-periodic-process"></a><span data-ttu-id="bc8b3-110">Bevételbecslések kezelése időszakos folyamattal</span><span class="sxs-lookup"><span data-stu-id="bc8b3-110">Manage revenue estimates using a periodic process</span></span>

<span data-ttu-id="bc8b3-111">Nyissa meg a **Projektvezetés és -könyvelés** > **Időszakos** > **Becslések** lehetőséget, és válassza ki a kapcsolódó folyamatot.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-111">Go to **Project management and accounting** > **Periodic** > **Estimates** and select the corresponding process.</span></span>

## <a name="create-a-revenue-estimate"></a><span data-ttu-id="bc8b3-112">Bevételi becslés létrehozása</span><span class="sxs-lookup"><span data-stu-id="bc8b3-112">Create a revenue estimate</span></span>

<span data-ttu-id="bc8b3-113">Bevételi becslések létrehozásához hajtsa végre az alábbi lépéseket.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-113">Complete the following steps to create a revenue estimate.</span></span> 

1. <span data-ttu-id="bc8b3-114">Nyissa meg a **Projektvezetés és könyvelés** > **Időszakos** > **Becslések** menüpontot.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-114">Go to **Project management and accounting** > **Periodic** > **Estimates**.</span></span>
2. <span data-ttu-id="bc8b3-115">Válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-115">Select **New**.</span></span> <span data-ttu-id="bc8b3-116">A **Becslés létrehozása** lapon adja meg az alábbi paramétereket:</span><span class="sxs-lookup"><span data-stu-id="bc8b3-116">On the **Estimate creation** page, select the following parameters:</span></span>

   - <span data-ttu-id="bc8b3-117">**Időszakkód**: Ez a kód határozza meg, hogy milyen gyakran adják fel a becsléseket.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-117">**Period code**: This code determines how frequently estimates are posted.</span></span>
   - <span data-ttu-id="bc8b3-118">**Becslés dátuma**: A becslés feldolgozásának dátuma.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-118">**Estimate date**: The date the estimate is processed.</span></span>
   - <span data-ttu-id="bc8b3-119">**Folyamatos**: Jelölje be ezt a jelölőnégyzetet, ha csak akkor szeretne becsléseket létrehozni, ha becsléseket adtak fel az előző időszakban, vagy ha a becslés az első létrehozott becslés.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-119">**Continuous**: Select this check box to create estimates only if estimates were posted in the previous period, or if the estimate is the first estimate that has been created.</span></span> <span data-ttu-id="bc8b3-120">Ha ez nincs bejelölve, akkor is becslések jönnek létre, még akkor is, ha becsléseket nem adtak fel az előző időszakban.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-120">If this is not selected, estimates are created even if estimates were not posted in the previous period.</span></span>
   - <span data-ttu-id="bc8b3-121">**Teljesítési költség módszere**: Adja meg, hogyan kell megbecsülni a fennmaradó projektmunkát.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-121">**Cost to complete method**: Define how to estimate the remaining project work.</span></span> <span data-ttu-id="bc8b3-122">További információ: [Teljesítési költség módszerei](cost-complete-methods.md).</span><span class="sxs-lookup"><span data-stu-id="bc8b3-122">For more information, see [Cost to complete methods](cost-complete-methods.md).</span></span>
   - <span data-ttu-id="bc8b3-123">**Teljesítési módszer**: Válasszon ki egy teljesítési módszert a következő lehetőségek közül:</span><span class="sxs-lookup"><span data-stu-id="bc8b3-123">**Completion method**: Select a completion method from the following options:</span></span>
     - <span data-ttu-id="bc8b3-124">**Automatikus** : A készültségi százalék számítása automatikusan, és a számításban szereplő költségsorok alapján történik.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-124">**Automatic**: The completion percentage is calculated automatically and based on the cost lines included in the calculation.</span></span> <span data-ttu-id="bc8b3-125">A költségsablon határozza meg a benne foglalt költségsorokat.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-125">The cost template defines the cost lines that are included.</span></span>
     - <span data-ttu-id="bc8b3-126">**Manuális**: A készültségi százalék megegyezik az utolsó becslés készültségi százalékával.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-126">**Manual**: The completion percentage equals the completion percentage of the last estimate.</span></span> <span data-ttu-id="bc8b3-127">A becslés létrehozása után módosíthatja a **Manuális számítást** a **Becslések** lapon.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-127">After the estimate is created, you can change the **Manual calculation** on the **Estimates** page.</span></span>
     - <span data-ttu-id="bc8b3-128">**Költségsablonból**: Az automatikus és a manuális módszerek kombinációja.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-128">**From cost template**: A combination of the automatic and manual methods.</span></span> <span data-ttu-id="bc8b3-129">Ez a lehetőség automatikus vagy manuális értékre van beállítva, a költségsablon alapértelmezett értékétől függően.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-129">This option is set automatically or manually, depending on the default value in the cost template.</span></span>
   - <span data-ttu-id="bc8b3-130">**Előrejelzési modell**: Válasszon előrejelzési modellt a becsléshez.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-130">**Forecast model**: Select a forecast model for the estimate.</span></span>
   - <span data-ttu-id="bc8b3-131">**Becslési listanyomtatása**: Becslési lista létrehozása és megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-131">**Print estimate list**: Create and show an estimate list.</span></span> <span data-ttu-id="bc8b3-132">A lista az aktuális függvény állapotát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-132">The list contains the status of the current function.</span></span> <span data-ttu-id="bc8b3-133">A becsléssel kapcsolatos figyelmeztetéseket a jelentésben kinyomtathatja.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-133">You can print any warnings about the estimate on the report.</span></span> <span data-ttu-id="bc8b3-134">A következő feltételek hatására figyelmeztetések jelennek meg a becslési listában:</span><span class="sxs-lookup"><span data-stu-id="bc8b3-134">The following conditions cause warnings to appear in the estimate list:</span></span>
     - <span data-ttu-id="bc8b3-135">A készültségi százalék több mint 100 százalék.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-135">A completion percentage of more than 100 percent.</span></span>
     - <span data-ttu-id="bc8b3-136">A készültségi százalék kevesebb mint nulla százalék.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-136">A completion percentage less than zero percent.</span></span>
     - <span data-ttu-id="bc8b3-137">Negatív összeg a **Befejezéshez** oszlopban.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-137">A negative amount in the **To complete** column.</span></span>
     - <span data-ttu-id="bc8b3-138">Kapcsolódó szerződésösszeg nélküli becslés.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-138">An estimate with no corresponding contract amount.</span></span>
     - <span data-ttu-id="bc8b3-139">Csatolt költségbecslés nélküli becslés.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-139">An estimate with no attached cost estimate.</span></span>
   - <span data-ttu-id="bc8b3-140">**Információs napló megjelenítése**: Akkor válassza ezt a lehetőséget, ha egy olyan üzenetet szeretne kapni, amely a feladat futtatásakor feldolgozott becsült projektekre vonatkozó információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-140">**Show Infolog**: Select this option to receive a message that contains information about the estimate projects that were processed when the job was run.</span></span>


## <a name="post-wip-or-accruals"></a><span data-ttu-id="bc8b3-141">Folyamatban lévő munka vagy elhatárolások feladása</span><span class="sxs-lookup"><span data-stu-id="bc8b3-141">Post WIP or accruals</span></span>

<span data-ttu-id="bc8b3-142">A becslések értékelése után azok fenntartva, csökkentve vagy növelve lesznek.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-142">After the estimates are evaluated, they are maintained, decreased, or increased.</span></span> <span data-ttu-id="bc8b3-143">Ezután feladhatja a folyamatban lévő munkát a **Befejezett szerződés** felmérési elvvel, vagy feladhatja az elhatárolásokat az **Elkészült százalék** elv használatával.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-143">You can then post the WIP when you work with the **Completed contract** assessment principle, or post the accruals when you work with the **Completed percentage** assessment principle.</span></span>
  
<span data-ttu-id="bc8b3-144">A becsült időszak állapota **Létrehozva** állapotról **Feladottra** változik.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-144">The estimate period status changes from **Created** to **Posted**.</span></span>

## <a name="reverse-wip-or-accruals"></a><span data-ttu-id="bc8b3-145">Folyamatban lévő munka vagy elhatárolás sztornírozása</span><span class="sxs-lookup"><span data-stu-id="bc8b3-145">Reverse WIP or accruals</span></span>

<span data-ttu-id="bc8b3-146">A sztornírozás lehetőség használatával jóváírhatja a már feladott folyamatban lévő munkát vagy elhatárolást, majd az időszakra vonatkozóan becsléseket hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-146">Use the reverse option to credit already posted WIP or accruals, and then create estimates for the period.</span></span>

> [!NOTE]
> <span data-ttu-id="bc8b3-147">Az egyéb időszakok közötti időszak sztornózásához szotronózza a szükséges becslési időszakokat, majd adja fel ezeket újra.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-147">To reverse a period that is in between other periods, reverse the necessary estimate periods and then repost them.</span></span> <span data-ttu-id="bc8b3-148">Mivel a későbbi időszakok az előző időszak becsléseitől függnek, nem hagyjon ki semmilyen időszakot.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-148">Because all subsequent periods depend on the estimates from the previous period, don't skip any periods.</span></span>

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a><span data-ttu-id="bc8b3-149">A becsülési projekt megszüntetése és a projekt befejezése</span><span class="sxs-lookup"><span data-stu-id="bc8b3-149">Eliminate the estimate project and finish the project</span></span>

<span data-ttu-id="bc8b3-150">A becslési folyamat utolsó lépése a becsült projekt megszüntetése és a fix áras projekt lezárása, amikor a készültségi szint eléri a 100 százalékos értéket.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-150">The final step in the estimate process is to eliminate the estimate project and end the fixed price project when the percentage of completion reaches 100 percent.</span></span>

<span data-ttu-id="bc8b3-151">A következő akkor fordul elő, ha futtatja a megszüntetést:</span><span class="sxs-lookup"><span data-stu-id="bc8b3-151">The following occurs when you run the elimination:</span></span>

- <span data-ttu-id="bc8b3-152">Befejezett szerződéssel rendelkező rögzített áras projekt esetén a folyamatban lévő munka értékét a rendszer az egyenlegszámlákból törli, az eredménykimutatást pedig könyveli.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-152">For a fixed price project with a completed contract, the WIP values clear from the balance accounts and post to the profit and loss accounts.</span></span>
- <span data-ttu-id="bc8b3-153">Befejezett százalékértékű rögzített árú projekt esetén az elhatárolások az eredménykimutatásból törlődnek.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-153">For a fixed-price project with a completed percentage, the accruals are removed from the profit and loss accounts.</span></span>

<span data-ttu-id="bc8b3-154">A becslés az állapota **Megszüntetve** értékre változik.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-154">The estimate changes the status to **Eliminated**.</span></span>

> [!NOTE]
> <span data-ttu-id="bc8b3-155">Különleges esetekben a százalékos arány 100 százaléknál több is lehet.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-155">In special cases, the percentage can extend beyond 100 percent.</span></span> <span data-ttu-id="bc8b3-156">Amikor ez megtörténik, csökkentse a készültségi fokot a **Teljesítési költség módszere beállítása** funkcióval, amíg el nem éri a 100 százalékos értéket.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-156">When this happens, reduce the percentage of completion by using the **Set cost to complete to zero method** to reach 100 percent.</span></span>

## <a name="reverse-elimination"></a><span data-ttu-id="bc8b3-157">Sztornírozás megszüntetése</span><span class="sxs-lookup"><span data-stu-id="bc8b3-157">Reverse elimination</span></span>

1. <span data-ttu-id="bc8b3-158">Nyissa meg a **Projektvezetés és könyvelés** > **Időszakos** > **Becslések** > **Eltávolítás sztornírozása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-158">Go to **Project management and accounting** > **Periodic** > **Estimates** > **Reverse elimination**.</span></span> 
2. <span data-ttu-id="bc8b3-159">A művelet ablaktábla **Folyamat** lapjának **Karbantartás** csoportjában válassza a **Becslés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-159">On the Action Pane, on the **Process** tab, in the **Maintain** group, select **Estimate**.</span></span> 
3. <span data-ttu-id="bc8b3-160">Válassza az **Eltávolítás sztornírozása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-160">Select **Reverse elimination**.</span></span>

<span data-ttu-id="bc8b3-161">Ezen az oldalon a megadott becslési dátummal rendelkező összes eltávolítást sztornírozhatja, és megszüntetheti a **Becsült** állapotot.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-161">Use this page to reverse all eliminations with a specified estimate date and with an estimate status of **Eliminated**.</span></span> <span data-ttu-id="bc8b3-162">A tranzakció állapota a megfelelő mezők kiválasztása után módosul.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-162">The transaction status changes after you select the appropriate fields.</span></span>

<span data-ttu-id="bc8b3-163">Ezzel automatikusan a projekt állapotát **Folyamatban** állapotra változtatja, ha a projekt fázisa befejezett értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-163">This also automatically changes the project status to **In process** if the project stage is set to finished.</span></span> <span data-ttu-id="bc8b3-164">A projekt időszakának becsült állapota a **Feladott** értékre változik vissza.</span><span class="sxs-lookup"><span data-stu-id="bc8b3-164">The estimate status of the project period changes back to **Posted**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]