---
title: Helyesbítő naplók létrehozása és megerősítése
description: Ez a témakör a helyesbítő napló létrehozásáról és megerősítéséről tartalmaz további információt.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6cc22168cdfefc4ae7b833bea75f68ba37c1ee67
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127757"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="d67b9-103">Helyesbítő naplók létrehozása és megerősítése</span><span class="sxs-lookup"><span data-stu-id="d67b9-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="d67b9-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="d67b9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d67b9-105">Időnként előfordulhat, hogy egy idő-vagy költségbejegyzés helytelenül van megadva.</span><span class="sxs-lookup"><span data-stu-id="d67b9-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="d67b9-106">Előfordulhat például, hogy egy tanácsadó helytelen időpontot választki időbejegyzés létrehozásakor, vagy egy költség bevitelekor felcserél számokat.</span><span class="sxs-lookup"><span data-stu-id="d67b9-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="d67b9-107">Ha egy tanácsadó nem tudja frissíteni a beküldött bejegyzéseket, az adminisztrátor közvetlenül kijavíthatja a projekthez tartozó bejegyzést.</span><span class="sxs-lookup"><span data-stu-id="d67b9-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="d67b9-108">A jelen témakör eljárásainak végrehajtásához rendszergazdai jogosultságokra van szükség.</span><span class="sxs-lookup"><span data-stu-id="d67b9-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="d67b9-109">Jóváhagyott időbejegyzések kijavítása</span><span class="sxs-lookup"><span data-stu-id="d67b9-109">Correct approved time entries</span></span>     

<span data-ttu-id="d67b9-110">A következő lépések végrehajtásával helyesbítheti a projekt egy vagy több időbejegyzését.</span><span class="sxs-lookup"><span data-stu-id="d67b9-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="d67b9-111">Az **Értékesítés** területen jelölje ki a **Tranzakciók** elemet, majd válassza a **Jóváhagyott idő** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d67b9-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="d67b9-112">A **Jóváhagyott idő** listájában keressen meg és jelöljön ki egy vagy több jóváhagyott időbejegyzést a helyesbítéshez.</span><span class="sxs-lookup"><span data-stu-id="d67b9-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="d67b9-113">A szűrő segítségével megkeresheti a kapcsolódó bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="d67b9-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="d67b9-114">Szűrheti például a projekt azonosítójára, és kijelölheti a projekt az adott Projektazonosítóval rendelkező összes jóváhagyott időbejegyzést.</span><span class="sxs-lookup"><span data-stu-id="d67b9-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="d67b9-115">Válassza a **Bejegyzések helyesbítése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d67b9-115">Select **Correct entries**.</span></span> <span data-ttu-id="d67b9-116">A rendszer automatikusan létrehoz egy új helyesbítő naplót az **Idő helyesbítése** hozzárendelt típussal.</span><span class="sxs-lookup"><span data-stu-id="d67b9-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="d67b9-117">A kijelölt bejegyzéseket a rendszer hozzáadja a naplóhoz.</span><span class="sxs-lookup"><span data-stu-id="d67b9-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="d67b9-118">Az **Új napló** lapon adja meg a helyesbítő napló **Leírását**, majd válassza ki az **Időbejegyzések helyesbítései** lapot.</span><span class="sxs-lookup"><span data-stu-id="d67b9-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="d67b9-119">Az **Időbejegyzések új értékei** részben igény szerint frissítse a mezőket a megfelelő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="d67b9-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="d67b9-120">Megváltoztathatja például a hozzárendelt projektet vagy a lefoglalható erőforrást.</span><span class="sxs-lookup"><span data-stu-id="d67b9-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="d67b9-121">Válassza a **Előnézet** elemet.</span><span class="sxs-lookup"><span data-stu-id="d67b9-121">Select **Preview**.</span></span> <span data-ttu-id="d67b9-122">A párbeszédpanelen válassza az **OK** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d67b9-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="d67b9-123">A **Naplósorok** lapon megtekintheti a sztornírozott kijelölt időpontokhoz kapcsolódó eredeti tényadatok listáját, valamint a hozzájuk tartozó helyesbített sorokat, amelyek létre lettek hozva.</span><span class="sxs-lookup"><span data-stu-id="d67b9-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="d67b9-124">Ha további helyesbítésekre van szükség, ismételje meg az 5. és a 6. lépéseket.</span><span class="sxs-lookup"><span data-stu-id="d67b9-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="d67b9-125">Minden helyesbített tényadatnak ugyanazok az értékei lesznek, mint amelyeket kiválasztott **Időbejegyzések új értékei** szakaszban.</span><span class="sxs-lookup"><span data-stu-id="d67b9-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="d67b9-126">Ha a javítások a várt módon jelennek meg ,válassza a **Jóváhagyás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d67b9-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="d67b9-127">A párbeszédpanelen válassza az **OK** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d67b9-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="d67b9-128">Térjen vissza az **Értékesítés** területre, válassza a **Projektek** lehetőséget, majd nyissa meg azt a projektet, amelyhez az imént az időbejegyzéseket frissítette.</span><span class="sxs-lookup"><span data-stu-id="d67b9-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="d67b9-129">A **Projektek** oldalon, a **Tényadatok** lapon tekintse meg a végrehajtott módosításokat.</span><span class="sxs-lookup"><span data-stu-id="d67b9-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="d67b9-130">Ha a **Tényadatok** lap nem látható, válassza a **Kapcsolódó** > **Tényadatok** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d67b9-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="d67b9-131">A **Tényleges adatok társított nézete** listában látható, hogy a sztornírozott eredeti időbejegyzések továbbra is ott vannak, ahogy a hozzájuk tartozó helyesbített időpontok is.</span><span class="sxs-lookup"><span data-stu-id="d67b9-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="d67b9-132">A következő ábrán például két olyan sor tétel szerepel, amelyek mennyisége 8,00 és terhelések tartoznak hozzájuk a Mennyiség oszlopban.</span><span class="sxs-lookup"><span data-stu-id="d67b9-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="d67b9-133">Emellett két olyan sor tétel szerepel, amelynek mennyisége -8,00, és ezekhez az Összeg oszlopban jóváírás látható.</span><span class="sxs-lookup"><span data-stu-id="d67b9-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="d67b9-134">Ezek a javítások nullára módosítják a mennyiséget.</span><span class="sxs-lookup"><span data-stu-id="d67b9-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="d67b9-135">Jóváhagyott költségbejegyzések kijavítása</span><span class="sxs-lookup"><span data-stu-id="d67b9-135">Correct approved expense entries</span></span>

<span data-ttu-id="d67b9-136">Hajtsa végre az alábbi lépéseket egy vagy több költségbejegyzés kijavításához.</span><span class="sxs-lookup"><span data-stu-id="d67b9-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="d67b9-137">Az **Értékesítés** terület bal oldali navigációs ablaktáblájának **Tranzakciók** területén a **Jóváhagyott kiadások** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d67b9-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="d67b9-138">A **Jóváhagyott kiadások** listájában jelölje ki a helyesbíteni kívánt projektet, majd válassza a **Bejegyzések helyesbítése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d67b9-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="d67b9-139">A rendszer automatikusan létrehoz majd egy új helyesbítő naplót a **Költség helyesbítése** hozzárendelt típussal.</span><span class="sxs-lookup"><span data-stu-id="d67b9-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="d67b9-140">Az **Új napló** lapon adja meg a helyesbítés **Leírását**, és a **Költség javítása** lapon, a **Költségek új értékei** szakaszban jelölje ki a kiválasztott költségsorhoz helyesbíteni kívánt adatmezőket.</span><span class="sxs-lookup"><span data-stu-id="d67b9-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="d67b9-141">Például hozzárendelheti a költséget egy másik **Projekthez**, vagy helyesbítheti a **Költségkategóriát**, a **Költség dátumát** vagy a **Lefoglalható erőforrást**.</span><span class="sxs-lookup"><span data-stu-id="d67b9-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="d67b9-142">Válassza a **Előnézet** elemet.</span><span class="sxs-lookup"><span data-stu-id="d67b9-142">Select **Preview**.</span></span> <span data-ttu-id="d67b9-143">A párbeszédpanelen válassza az **OK** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d67b9-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="d67b9-144">A **Naplósorok** lapon ellenőrizze a javításokat. Megtekintheti a kijelölt költségbejegyzésekhez kapcsolódó eredeti tényadatok listáját, valamint a hozzájuk tartozó helyesbített sorokat, amelyek létre lettek hozva.</span><span class="sxs-lookup"><span data-stu-id="d67b9-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="d67b9-145">Ha a javított értékek a várt módon jelennek meg ,válassza a **Jóváhagyás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d67b9-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="d67b9-146">A párbeszédpanelen válassza az **OK** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d67b9-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="d67b9-147">Ha az értékek nem a várt módon jelennek meg , válassza a **Mégse** lehetőséget a **Jóváhagyott kiadások** listájához való visszatéréshez.</span><span class="sxs-lookup"><span data-stu-id="d67b9-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="d67b9-148">Ismételje meg a 2 – 5. lépéseket.</span><span class="sxs-lookup"><span data-stu-id="d67b9-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="d67b9-149">Minden helyesbített tényadatnak ugyanazok az értékei lesznek, mint amelyeket kiválasztott **Költségek új értékei** szakaszban.</span><span class="sxs-lookup"><span data-stu-id="d67b9-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="d67b9-150">A helyesbítő napló megerősítése után lépjen vissza a frissített projekthez vagy projektekhez, és tekintse meg a változtatásokat.</span><span class="sxs-lookup"><span data-stu-id="d67b9-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="d67b9-151">A projekt oldalán a **Tényadatok** lapon tekintse át a **Tényleges adatok társított nézete** elemet.</span><span class="sxs-lookup"><span data-stu-id="d67b9-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="d67b9-152">Az eredeti bejegyzések és a helyesbített bejegyzések vannak felsorolva.</span><span class="sxs-lookup"><span data-stu-id="d67b9-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="d67b9-153">A következő ábra az eredeti költségbejegyzés összegeket, illetve az azokhoz tartozó helyesbített költségbejegyzés-mennyiségeket.</span><span class="sxs-lookup"><span data-stu-id="d67b9-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 


