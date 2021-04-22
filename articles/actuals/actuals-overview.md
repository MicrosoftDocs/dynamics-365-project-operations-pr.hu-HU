---
title: Tényadatok
description: A témakör a Microsoft Dynamics 365 Project Operations tényadatokkal való munkára vonatkozó információit mutatja be.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852547"
---
# <a name="actuals"></a><span data-ttu-id="bb3a3-103">Tények</span><span class="sxs-lookup"><span data-stu-id="bb3a3-103">Actuals</span></span> 

<span data-ttu-id="bb3a3-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű központi telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="bb3a3-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bb3a3-105">A tényleges adatok a projekt felülvizsgált és jóváhagyott pénzügyi és ütemezési előrehaladását jelentik.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="bb3a3-106">Az idő-, költség-, anyagfelhasználási tételek, valamint a naplótételek és számlák jóváhagyásának eredményeként jönnek létre.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="bb3a3-107">Naplósorok és idő beküldése</span><span class="sxs-lookup"><span data-stu-id="bb3a3-107">Journal lines and time submission</span></span>

<span data-ttu-id="bb3a3-108">Az időbejegyzéssel kapcsolatos további tudnivalókért lásd: [Időbejegyzés áttekintése](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bb3a3-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="bb3a3-109">Idő és anyagok</span><span class="sxs-lookup"><span data-stu-id="bb3a3-109">Time and materials</span></span>

<span data-ttu-id="bb3a3-110">Amikor egy elküldött időbejegyzés egy idő- és anyag szerződéssorra leképezett projekthez van csatolva, a rendszer két naplósort hoz létre, egyet a költség, egy pedig a nem számlázott értékesítés számára.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="bb3a3-111">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="bb3a3-111">Fixed price</span></span>

<span data-ttu-id="bb3a3-112">Amikor egy rögzített árú szerződéssorra leképezett projekthez kapcsolt időbejegyzést küldenek be, csak a költségekre vonatkozó naplósort hoz létre a rendszer.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="bb3a3-113">Alapértelmezett árképzés</span><span class="sxs-lookup"><span data-stu-id="bb3a3-113">Default pricing</span></span>

<span data-ttu-id="bb3a3-114">Az alapértelmezett árak létrehozásának logikája a naplósorban található.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="bb3a3-115">Az időbejegyzésből származó mezőértékek a naplósorba vannak másolva.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="bb3a3-116">Ezekben az értékekben szerepel a tranzakció dátuma, a projekthez leképezett szerződéssor, és a megfelelő árlistában szereplő pénznem.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="bb3a3-117">Az alapértelmezett árképzésre hatással lévő mezők, például a **Szerepkör** és a **Erőforrás-kezelő részleg** mezők a naplósorban alapértelmezés szerint megfelelő ár meghatározására szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="bb3a3-118">Lehetőség van egyéni mező hozzáadására az időbejegyzésen.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="bb3a3-119">Ha azt szeretné, hogy a mezőérték tényleges értékre legyen propagálva, hozza létre a mezőt a **Tényleges** és a **Naplósor** táblákban.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="bb3a3-120">Egyéni kód használatával propagálhatja a kijelölt mezőértéket az Időbejegyzéstől a Tényleges adatokig a naplósoron keresztül tranzakcióeredeteket használva.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="bb3a3-121">A tranzakcióeredetekről és -kapcsolatokról további információt a [Tényleges adatok hozzákapcsolása az eredeti rekordokhoz](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection) részben talál.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="bb3a3-122">Naplósorok és az alapvető költség benyújtása</span><span class="sxs-lookup"><span data-stu-id="bb3a3-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="bb3a3-123">A költségbejegyzéssel kapcsolatos további tudnivalókért lásd: [Költség áttekintése](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bb3a3-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="bb3a3-124">Idő és anyagok</span><span class="sxs-lookup"><span data-stu-id="bb3a3-124">Time and materials</span></span>

<span data-ttu-id="bb3a3-125">Amikor egy elküldött alapvető költségbejegyzés egy idő- és anyag szerződéssorra leképezett projekthez van csatolva, a rendszer két naplósort hoz létre, egyet a költség, egy pedig a nem számlázott értékesítés számára.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="bb3a3-126">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="bb3a3-126">Fixed price</span></span>

<span data-ttu-id="bb3a3-127">Amikor egy rögzített árú szerződéssorra leképezett projekthez küldenek be alapköltség-bejegyzést, a rendszer egy naplósort hoz létre költséghez.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="bb3a3-128">Alapértelmezett árképzés</span><span class="sxs-lookup"><span data-stu-id="bb3a3-128">Default pricing</span></span>

<span data-ttu-id="bb3a3-129">A költségek alapértelmezett árának megadására vonatkozó logika a költségkategórián alapul.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="bb3a3-130">A tranzakció dátuma, a projekthez leképezett szerződéssor és a pénznem mind a megfelelő árlista meghatározására szolgál.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="bb3a3-131">Az alapértelmezett árképzésre hatással lévő mezők, például a **Tranzakció kategóriája** és az **Egység** mezők a naplósorban alapértelmezés szerint megfelelő ár meghatározására szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="bb3a3-132">Ez azonban csak akkor működik, ha az árlistában szereplő árképzési módszer az **Egységár**.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="bb3a3-133">Ha az árképzési módszer **Költségen** vagy **Árrés a költség felett** érték, a program a költségbevitel létrehozásakor megadott árat használja költségként, és az értékesítési naplósorban megadott árat az árképzési módszer alapján számítja ki.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="bb3a3-134">A költségbevitelhez hozzáadhat egyéni mezőt.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="bb3a3-135">Ha azt szeretné, hogy a mezőérték tényleges értékre legyen propagálva, hozza létre a mezőt a **Tényleges** és a **Naplósor** táblákban.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="bb3a3-136">Egyéni kód használatával propagálhatja a kijelölt mezőértéket az Időbejegyzéstől a Tényleges adatokig a naplósoron keresztül tranzakcióeredeteket használva.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="bb3a3-137">A tranzakcióeredetekről és -kapcsolatokról további információt a [Tényleges adatok hozzákapcsolása az eredeti rekordokhoz](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection) részben talál.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="bb3a3-138">Naplósorok és anyaghasználati napló benyújtása</span><span class="sxs-lookup"><span data-stu-id="bb3a3-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="bb3a3-139">A költségbevitelről további információt az [Anyagfelhasználási naplóban](../material/material-usage-log.md) talál.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="bb3a3-140">Idő és anyagok</span><span class="sxs-lookup"><span data-stu-id="bb3a3-140">Time and materials</span></span>

<span data-ttu-id="bb3a3-141">Ha egy beküldött anyaghasználatinapló-tétel egy idő- és anyagszerződési sorhoz leképezett projekthez kapcsolódik, a rendszer két naplósort hoz létre, egyet a költséghez, egyet pedig a számlázatlan értékesítésekhez.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="bb3a3-142">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="bb3a3-142">Fixed price</span></span>

<span data-ttu-id="bb3a3-143">Amikor egy rögzített árú szerződéssorra leképezett projekthez küldenek be anyagfelhasználásinapló-bejegyzést, a rendszer egy naplósort hoz létre a költséghez.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="bb3a3-144">Alapértelmezett árképzés</span><span class="sxs-lookup"><span data-stu-id="bb3a3-144">Default pricing</span></span>

<span data-ttu-id="bb3a3-145">Az anyaghoz tartozó alapértelmezett árak megadásának logikája a termék- és egységkombináción alapul.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="bb3a3-146">A tranzakció dátuma, a projekthez leképezett szerződéssor és a pénznem mind a megfelelő árlista meghatározására szolgál.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="bb3a3-147">Az alapértelmezett árképzésre hatással lévő mezők, például a **Termékazonosító** és az **Egység** mezők a naplósorban alapértelmezés szerint megfelelő ár meghatározására szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="bb3a3-148">Ez azonban csak katalogizált termékek esetében működik.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-148">However, this only works for catalog products.</span></span> <span data-ttu-id="bb3a3-149">Nem katalogizált termékek esetében az anyagfelhasználásinapló-tétel létrehozásakor megadott ár kerül felhasználásra a naplósorok költség- és eladási ára tekintetében.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="bb3a3-150">Az **Anyagfelhasználási napló** bejegyzéshez hozzáadhat egyéni mezőt.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="bb3a3-151">Ha azt szeretné, hogy a mezőérték tényleges értékre legyen propagálva, hozza létre a mezőt a **Tényleges** és a **Naplósor** táblákban.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="bb3a3-152">Egyéni kód használatával propagálhatja a kijelölt mezőértéket az Időbejegyzéstől a Tényleges adatokig a naplósoron keresztül tranzakcióeredeteket használva.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="bb3a3-153">A tranzakcióeredetekről és -kapcsolatokról további információt a [Tényleges adatok hozzákapcsolása az eredeti rekordokhoz](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection) részben talál.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="bb3a3-154">Bejegyzésnaplók használata a költségek rögzítésére</span><span class="sxs-lookup"><span data-stu-id="bb3a3-154">Use entry journals to record costs</span></span>

<span data-ttu-id="bb3a3-155">A bejegyzésnaplók segítségével rögzítheti a költséget vagy bevételt az anyag-, díj-, idő-, költség- vagy adózási tranzakciók osztályaiban.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="bb3a3-156">A naplók a következő célokra használhatók:</span><span class="sxs-lookup"><span data-stu-id="bb3a3-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="bb3a3-157">Tranzakciós tényeket helyezhet egy másik rendszerből a Microsoft Dynamics 365 Project Operations rendszerbe.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="bb3a3-158">Egy másik rendszerben felmerült költségek rögzítésére.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="bb3a3-159">Ezek a költségek beszerzési vagy alvállalkozói költségeket is tartalmazhatnak.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bb3a3-160">Az alkalmazás nem ellenőrzi a naplósor típusát vagy a kapcsolódó árazást, amelyet a naplósorban adtak meg.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="bb3a3-161">Ezért csak azoknak a felhasználóknak érdemes a bejegyzésnaplókat tényleges adatok létrehozására használniuk, akik teljes mértékben ismeretében vannak annak a számviteli hatásnak, amelyet a tényleges adatok gyakorolnak a projektre.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="bb3a3-162">A naplótípus hatása miatt gondosan válassza ki, hogy ki férhet hozzá a bejegyzésnaplók létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="bb3a3-163">Tényadatok rögzítése projektesemények alapján</span><span class="sxs-lookup"><span data-stu-id="bb3a3-163">Record actuals based on project events</span></span>

<span data-ttu-id="bb3a3-164">A Project Operations rögzíti a projekt során bekövetkező pénzügyi tranzakciókat.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="bb3a3-165">Ezeket a tranzakciókat a rendszer tényadatokként rögzíti.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="bb3a3-166">A következő táblázatok a létrehozott tényadatok különböző típusait mutatják be attól függően, hogy a projekt idő- és anyagelszámolású vagy rögzített árú projekt, elővásárlási fázisban van-e, vagy belső projekt-e.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="bb3a3-167">Az erőforrás ugyanahhoz a szervezeti egységhez tartozik, mint a projekt szerződő részlege</span><span class="sxs-lookup"><span data-stu-id="bb3a3-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="bb3a3-168">Esemény</span><span class="sxs-lookup"><span data-stu-id="bb3a3-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="bb3a3-169">Számlázható vagy értékesített projekt</span><span class="sxs-lookup"><span data-stu-id="bb3a3-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="bb3a3-170">Elővásárlási szakaszban lévő projekt</span><span class="sxs-lookup"><span data-stu-id="bb3a3-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="bb3a3-171">Belső projekt</span><span class="sxs-lookup"><span data-stu-id="bb3a3-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="bb3a3-172">Idő és anyagok</span><span class="sxs-lookup"><span data-stu-id="bb3a3-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="bb3a3-173">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="bb3a3-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="bb3a3-174">Tények</span><span class="sxs-lookup"><span data-stu-id="bb3a3-174">Actuals</span></span></th>
<th><span data-ttu-id="bb3a3-175">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-175">Transaction currency</span></span></th>
<th><span data-ttu-id="bb3a3-176">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="bb3a3-176">Fixed price</span></span></th>
<th><span data-ttu-id="bb3a3-177">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bb3a3-178">Létrejön egy időbejegyzés.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="bb3a3-179">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="bb3a3-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-180">A rendszer elküld egy időbejegyzést.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="bb3a3-181">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="bb3a3-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bb3a3-182">Az időt elfogadják, és a jóváhagyáskor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="bb3a3-183">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="bb3a3-183">Cost actual</span></span></td>
<td><span data-ttu-id="bb3a3-184">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bb3a3-185">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="bb3a3-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="bb3a3-186">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="bb3a3-187">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="bb3a3-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="bb3a3-188">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="bb3a3-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-189">Tényeleges számlázatlan értékesítés – Felszámítható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="bb3a3-190">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bb3a3-191">Az időt elfogadják, és a jóváhagyáskor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="bb3a3-192">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="bb3a3-192">Cost actual</span></span></td>
<td><span data-ttu-id="bb3a3-193">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="bb3a3-194">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="bb3a3-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="bb3a3-195">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="bb3a3-196">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="bb3a3-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="bb3a3-197">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="bb3a3-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-198">Tényleges számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="bb3a3-199">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-200">Tényleges számlázatlan értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="bb3a3-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="bb3a3-201">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bb3a3-202">Egy számla megerősítésekor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="bb3a3-203">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="bb3a3-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="bb3a3-204">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bb3a3-205">Mérföldkőhöz tartozó számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="bb3a3-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="bb3a3-206">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bb3a3-207">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="bb3a3-208">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-209">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="bb3a3-209">Billed sales</span></span></td>
<td><span data-ttu-id="bb3a3-210">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bb3a3-211">Egy számla megerősítésekor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="bb3a3-212">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="bb3a3-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="bb3a3-213">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="bb3a3-214">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bb3a3-215">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bb3a3-216">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bb3a3-217">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-218">Számlázott értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="bb3a3-219">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-220">Számlázott értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="bb3a3-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="bb3a3-221">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bb3a3-222">Egy számla javítva a felszámítható mennyiség növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="bb3a3-223">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="bb3a3-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="bb3a3-224">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="bb3a3-225">Mérföldkőhöz tartozó sztornózott értékesítés</span><span class="sxs-lookup"><span data-stu-id="bb3a3-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="bb3a3-226">A mérföldkő <strong>Számlázott</strong> állapotból <strong>Számlázásra készen áll</strong> állapotba kerül</span><span class="sxs-lookup"><span data-stu-id="bb3a3-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="bb3a3-227">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="bb3a3-228">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="bb3a3-229">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-230">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="bb3a3-230">Billed sales</span></span></td>
<td><span data-ttu-id="bb3a3-231">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bb3a3-232">Egy számla javítva a felszámítható mennyiség csökkentéséhez.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="bb3a3-233">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="bb3a3-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="bb3a3-234">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-235">Számlázott értékesítés az új mennyiséghez</span><span class="sxs-lookup"><span data-stu-id="bb3a3-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="bb3a3-236">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-237">Számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="bb3a3-238">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="bb3a3-239">Az erőforrás egy olyan szervezeti egységhez tartozik, amely a projekt szerződő részlegétől eltérő</span><span class="sxs-lookup"><span data-stu-id="bb3a3-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="bb3a3-240">Esemény</span><span class="sxs-lookup"><span data-stu-id="bb3a3-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="bb3a3-241">Számlázható vagy értékesített projekt</span><span class="sxs-lookup"><span data-stu-id="bb3a3-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="bb3a3-242">Elővásárlási szakaszban lévő projekt</span><span class="sxs-lookup"><span data-stu-id="bb3a3-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="bb3a3-243">Belső projekt</span><span class="sxs-lookup"><span data-stu-id="bb3a3-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="bb3a3-244">Idő és anyagok</span><span class="sxs-lookup"><span data-stu-id="bb3a3-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="bb3a3-245">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="bb3a3-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="bb3a3-246">Tények</span><span class="sxs-lookup"><span data-stu-id="bb3a3-246">Actuals</span></span></th>
<th><span data-ttu-id="bb3a3-247">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-247">Transaction currency</span></span></th>
<th><span data-ttu-id="bb3a3-248">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="bb3a3-248">Fixed price</span></span></th>
<th><span data-ttu-id="bb3a3-249">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bb3a3-250">Létrejön egy időbejegyzés.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="bb3a3-251">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="bb3a3-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-252">A rendszer elküld egy időbejegyzést.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="bb3a3-253">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="bb3a3-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="bb3a3-254">Az időt elfogadják, és a jóváhagyáskor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="bb3a3-255">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="bb3a3-255">Cost actual</span></span></td>
<td><span data-ttu-id="bb3a3-256">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="bb3a3-257">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="bb3a3-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="bb3a3-258">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="bb3a3-259">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="bb3a3-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="bb3a3-260">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="bb3a3-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-261">Tényeleges számlázatlan értékesítés – Felszámítható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="bb3a3-262">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-263">Erőforrás-kezelő részleg költsége</span><span class="sxs-lookup"><span data-stu-id="bb3a3-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="bb3a3-264">Erőforrás-kezelő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-265">Szervezetek közötti értékesítések</span><span class="sxs-lookup"><span data-stu-id="bb3a3-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="bb3a3-266">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="bb3a3-267">Az időt elfogadják, és a jóváhagyáskor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="bb3a3-268">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="bb3a3-268">Cost actual</span></span></td>
<td><span data-ttu-id="bb3a3-269">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="bb3a3-270">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="bb3a3-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="bb3a3-271">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="bb3a3-272">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="bb3a3-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="bb3a3-273">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="bb3a3-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-274">Erőforrás-kezelő részleg költsége</span><span class="sxs-lookup"><span data-stu-id="bb3a3-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="bb3a3-275">Erőforrás-kezelő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-276">Szervezetek közötti értékesítések</span><span class="sxs-lookup"><span data-stu-id="bb3a3-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="bb3a3-277">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-278">Tényleges számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="bb3a3-279">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-280">Tényleges számlázatlan értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="bb3a3-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="bb3a3-281">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bb3a3-282">Egy számla megerősítésekor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="bb3a3-283">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="bb3a3-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="bb3a3-284">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bb3a3-285">Mérföldkőhöz tartozó számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="bb3a3-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="bb3a3-286">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bb3a3-287">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="bb3a3-288">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-289">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="bb3a3-289">Billed sales</span></span></td>
<td><span data-ttu-id="bb3a3-290">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bb3a3-291">Egy számla megerősítésekor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="bb3a3-292">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="bb3a3-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="bb3a3-293">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="bb3a3-294">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bb3a3-295">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bb3a3-296">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bb3a3-297">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-298">Számlázott értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="bb3a3-299">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-300">Számlázott értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="bb3a3-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="bb3a3-301">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bb3a3-302">Egy számla javítva a felszámítható mennyiség növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="bb3a3-303">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="bb3a3-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="bb3a3-304">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="bb3a3-305">Mérföldkőhöz tartozó sztornózott értékesítés</span><span class="sxs-lookup"><span data-stu-id="bb3a3-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="bb3a3-306">A mérföldkő <strong>Számlázott</strong> állapotból <strong>Számlázásra készen áll</strong> állapotba kerül</span><span class="sxs-lookup"><span data-stu-id="bb3a3-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="bb3a3-307">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="bb3a3-308">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="bb3a3-309">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-310">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="bb3a3-310">Billed sales</span></span></td>
<td><span data-ttu-id="bb3a3-311">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bb3a3-312">Egy számla javítva a felszámítható mennyiség csökkentéséhez.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="bb3a3-313">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="bb3a3-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="bb3a3-314">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-315">Számlázott értékesítés az új mennyiséghez</span><span class="sxs-lookup"><span data-stu-id="bb3a3-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="bb3a3-316">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb3a3-317">Számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="bb3a3-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="bb3a3-318">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="bb3a3-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
