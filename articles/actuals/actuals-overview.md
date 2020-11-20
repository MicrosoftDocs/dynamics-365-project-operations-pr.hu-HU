---
title: Tényadatok
description: Ez a témakör a tényadatok Microsoft Dynamics 365 Project Operationsben való használatáról nyújt tájékoztatást.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
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
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126307"
---
# <a name="actuals"></a><span data-ttu-id="9c847-103">Tényadatok</span><span class="sxs-lookup"><span data-stu-id="9c847-103">Actuals</span></span> 

<span data-ttu-id="9c847-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="9c847-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9c847-105">A tények a projektben befejezett munka mennyiségét jelentik.</span><span class="sxs-lookup"><span data-stu-id="9c847-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="9c847-106">Ezek idő- és költségbejegyzésekként, valamint naplóbejegyzésekként és számlákként kerülnek létrehozásra.</span><span class="sxs-lookup"><span data-stu-id="9c847-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="9c847-107">Naplósorok és idő beküldése</span><span class="sxs-lookup"><span data-stu-id="9c847-107">Journal lines and time submission</span></span>

<span data-ttu-id="9c847-108">Az időbejegyzéssel kapcsolatos további tudnivalókért lásd: [Időbejegyzés áttekintése](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9c847-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="9c847-109">Idő és anyagok</span><span class="sxs-lookup"><span data-stu-id="9c847-109">Time and materials</span></span>

<span data-ttu-id="9c847-110">Amikor egy elküldött időbejegyzés egy idő- és anyag szerződéssorra leképezett projekthez van csatolva, a rendszer két naplósort hoz létre, egyet a költség, egy pedig a nem számlázott értékesítés számára.</span><span class="sxs-lookup"><span data-stu-id="9c847-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="9c847-111">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="9c847-111">Fixed price</span></span>

<span data-ttu-id="9c847-112">Amikor egy rögzített árú szerződéssorra leképezett projekthez kapcsolt időbejegyzést küldenek be, csak a költségekre vonatkozó naplósort hoz létre a rendszer.</span><span class="sxs-lookup"><span data-stu-id="9c847-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="9c847-113">Alapértelmezett árképzés</span><span class="sxs-lookup"><span data-stu-id="9c847-113">Default pricing</span></span>

<span data-ttu-id="9c847-114">Az alapértelmezett árak létrehozásának logikája a naplósorban található.</span><span class="sxs-lookup"><span data-stu-id="9c847-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="9c847-115">Az időbejegyzésből származó mezőértékek a naplósorba vannak másolva.</span><span class="sxs-lookup"><span data-stu-id="9c847-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="9c847-116">Ezekben az értékekben szerepel a tranzakció dátuma, a projekthez leképezett szerződéssor, és a megfelelő árlistában szereplő pénznem.</span><span class="sxs-lookup"><span data-stu-id="9c847-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="9c847-117">Az alapértelmezett árazásra hatással lévő mezők, például a **Szerepkör** és a **Szervezeti egység** mezők a naplósorban a megfelelő ár meghatározására szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="9c847-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="9c847-118">Lehetőség van egyéni mező hozzáadására az időbejegyzésen.</span><span class="sxs-lookup"><span data-stu-id="9c847-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="9c847-119">Ha azt szeretné, hogy a mező értéke a tényadatokra legyen propagálva, hozza létre a mezőt a Tények entitáson, és a mezők leképezésével másolja a mezőt az időbejegyzésből a tényekhez.</span><span class="sxs-lookup"><span data-stu-id="9c847-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="9c847-120">Naplósorok és az alapvető költség benyújtása</span><span class="sxs-lookup"><span data-stu-id="9c847-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="9c847-121">A költségbejegyzéssel kapcsolatos további tudnivalókért lásd: [Költség áttekintése](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9c847-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="9c847-122">Idő és anyagok</span><span class="sxs-lookup"><span data-stu-id="9c847-122">Time and materials</span></span>

<span data-ttu-id="9c847-123">Amikor egy elküldött alapvető költségbejegyzés egy idő- és anyag szerződéssorra leképezett projekthez van csatolva, a rendszer két naplósort hoz létre, egyet a költség, egy pedig a nem számlázott értékesítés számára.</span><span class="sxs-lookup"><span data-stu-id="9c847-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="9c847-124">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="9c847-124">Fixed price</span></span>

<span data-ttu-id="9c847-125">Amikor egy rögzített árú szerződéssorra leképezett projekthez kapcsolt alapvető költségbejegyzést küldenek be, csak a költségekre vonatkozó naplósort hoz létre a rendszer.</span><span class="sxs-lookup"><span data-stu-id="9c847-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="9c847-126">Alapértelmezett árképzés</span><span class="sxs-lookup"><span data-stu-id="9c847-126">Default pricing</span></span>

<span data-ttu-id="9c847-127">A költségek alapértelmezett árának megadására vonatkozó logika a költségkategórián alapul.</span><span class="sxs-lookup"><span data-stu-id="9c847-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="9c847-128">A tranzakció dátuma, a projekthez leképezett szerződéssor és a pénznem mind a megfelelő árlista meghatározására szolgál.</span><span class="sxs-lookup"><span data-stu-id="9c847-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="9c847-129">Alapértelmezésben azonban az árként megadott össze közvetlenül a kapcsolódó költségnaplósorokban van beállítva a költségre és értékesítésre vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="9c847-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="9c847-130">Nem áll rendelkezésre az egységenkénti alapértelmezett ár kategóriaalapú megadása a költségbejegyzésekre vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="9c847-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="9c847-131">Bejegyzésnaplók használata a költségek rögzítésére</span><span class="sxs-lookup"><span data-stu-id="9c847-131">Use entry journals to record costs</span></span>

<span data-ttu-id="9c847-132">A bejegyzésnaplók segítségével rögzítheti a költséget vagy bevételt az anyag-, díj-, idő-, költség- vagy adózási tranzakciók osztályaiban.</span><span class="sxs-lookup"><span data-stu-id="9c847-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="9c847-133">A naplók a következő célokra használhatók:</span><span class="sxs-lookup"><span data-stu-id="9c847-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="9c847-134">A tényleges anyagok és értékesítés költségének rögzítésére a projektben.</span><span class="sxs-lookup"><span data-stu-id="9c847-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="9c847-135">Amikor tranzakciós tényeket kell egy másik rendszerből a Microsoft Dynamics 365 Project Operationsbe áthelyezni.</span><span class="sxs-lookup"><span data-stu-id="9c847-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="9c847-136">Egy másik rendszerben felmerült költségek rögzítésére.</span><span class="sxs-lookup"><span data-stu-id="9c847-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="9c847-137">Ezek a költségek beszerzési vagy alvállalkozói költségeket is tartalmazhatnak.</span><span class="sxs-lookup"><span data-stu-id="9c847-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9c847-138">Az alkalmazás nem ellenőrzi a naplósor típusát vagy a kapcsolódó árazást, amelyet a naplósorban adtak meg.</span><span class="sxs-lookup"><span data-stu-id="9c847-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="9c847-139">Ezért csak azoknak a felhasználóknak érdemes a bejegyzésnaplókat tényleges adatok létrehozására használniuk, akik teljes mértékben ismeretében vannak annak a számviteli hatásnak, amelyet a tényleges adatok gyakorolnak a projektre.</span><span class="sxs-lookup"><span data-stu-id="9c847-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="9c847-140">A naplótípus hatása miatt gondosan válassza ki, hogy ki férhet hozzá a bejegyzésnaplók létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="9c847-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="9c847-141">Tényadatok rögzítése projektesemények alapján</span><span class="sxs-lookup"><span data-stu-id="9c847-141">Record actuals based on project events</span></span>

<span data-ttu-id="9c847-142">A Project Operations rögzíti a projekt során bekövetkező pénzügyi tranzakciókat.</span><span class="sxs-lookup"><span data-stu-id="9c847-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="9c847-143">Ezeket a tranzakciókat a rendszer tényadatokként rögzíti.</span><span class="sxs-lookup"><span data-stu-id="9c847-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="9c847-144">A következő táblázatok a létrehozott tényadatok különböző típusait mutatják be attól függően, hogy a projekt idő- és anyagelszámolású vagy rögzített árú projekt, elővásárlási fázisban van-e, vagy belső projekt-e.</span><span class="sxs-lookup"><span data-stu-id="9c847-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="9c847-145">Az erőforrás ugyanahhoz a szervezeti egységhez tartozik, mint a projekt szerződő részlege</span><span class="sxs-lookup"><span data-stu-id="9c847-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="9c847-146">Esemény</span><span class="sxs-lookup"><span data-stu-id="9c847-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="9c847-147">Számlázható vagy értékesített projekt</span><span class="sxs-lookup"><span data-stu-id="9c847-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="9c847-148">Elővásárlási szakaszban lévő projekt</span><span class="sxs-lookup"><span data-stu-id="9c847-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="9c847-149">Belső projekt</span><span class="sxs-lookup"><span data-stu-id="9c847-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="9c847-150">Idő és anyagok</span><span class="sxs-lookup"><span data-stu-id="9c847-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="9c847-151">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="9c847-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="9c847-152">Tények</span><span class="sxs-lookup"><span data-stu-id="9c847-152">Actuals</span></span></th>
<th><span data-ttu-id="9c847-153">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-153">Transaction currency</span></span></th>
<th><span data-ttu-id="9c847-154">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="9c847-154">Fixed price</span></span></th>
<th><span data-ttu-id="9c847-155">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9c847-156">Létrejön egy időbejegyzés.</span><span class="sxs-lookup"><span data-stu-id="9c847-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="9c847-157">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="9c847-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-158">A rendszer elküld egy időbejegyzést.</span><span class="sxs-lookup"><span data-stu-id="9c847-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="9c847-159">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="9c847-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9c847-160">Az időt elfogadják, és a jóváhagyáskor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="9c847-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9c847-161">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="9c847-161">Cost actual</span></span></td>
<td><span data-ttu-id="9c847-162">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9c847-163">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="9c847-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="9c847-164">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="9c847-165">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="9c847-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="9c847-166">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="9c847-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-167">Tényeleges számlázatlan értékesítés – Felszámítható</span><span class="sxs-lookup"><span data-stu-id="9c847-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="9c847-168">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9c847-169">Az időt elfogadják, és a jóváhagyáskor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="9c847-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9c847-170">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="9c847-170">Cost actual</span></span></td>
<td><span data-ttu-id="9c847-171">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9c847-172">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="9c847-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="9c847-173">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9c847-174">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="9c847-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="9c847-175">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="9c847-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-176">Tényleges számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="9c847-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9c847-177">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-178">Tényleges számlázatlan értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="9c847-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9c847-179">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9c847-180">Egy számla megerősítésekor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="9c847-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9c847-181">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="9c847-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9c847-182">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9c847-183">Mérföldkőhöz tartozó számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="9c847-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="9c847-184">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9c847-185">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="9c847-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="9c847-186">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="9c847-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-187">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="9c847-187">Billed sales</span></span></td>
<td><span data-ttu-id="9c847-188">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9c847-189">Egy számla megerősítésekor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="9c847-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9c847-190">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="9c847-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9c847-191">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9c847-192">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="9c847-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9c847-193">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="9c847-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9c847-194">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="9c847-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9c847-195">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="9c847-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-196">Számlázott értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="9c847-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9c847-197">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-198">Számlázott értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="9c847-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9c847-199">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9c847-200">Egy számla javítva a felszámítható mennyiség növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="9c847-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9c847-201">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="9c847-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9c847-202">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="9c847-203">Mérföldkőhöz tartozó sztornózott értékesítés</span><span class="sxs-lookup"><span data-stu-id="9c847-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="9c847-204">A mérföldkő <strong>Számlázott</strong> állapotból <strong>Számlázásra készen áll</strong> állapotba kerül</span><span class="sxs-lookup"><span data-stu-id="9c847-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="9c847-205">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9c847-206">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="9c847-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="9c847-207">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="9c847-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-208">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="9c847-208">Billed sales</span></span></td>
<td><span data-ttu-id="9c847-209">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9c847-210">Egy számla javítva a felszámítható mennyiség csökkentéséhez.</span><span class="sxs-lookup"><span data-stu-id="9c847-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9c847-211">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="9c847-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9c847-212">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-213">Számlázott értékesítés az új mennyiséghez</span><span class="sxs-lookup"><span data-stu-id="9c847-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="9c847-214">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-215">Számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="9c847-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="9c847-216">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="9c847-217">Az erőforrás egy olyan szervezeti egységhez tartozik, amely a projekt szerződő részlegétől eltérő</span><span class="sxs-lookup"><span data-stu-id="9c847-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="9c847-218">Esemény</span><span class="sxs-lookup"><span data-stu-id="9c847-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="9c847-219">Számlázható vagy értékesített projekt</span><span class="sxs-lookup"><span data-stu-id="9c847-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="9c847-220">Elővásárlási szakaszban lévő projekt</span><span class="sxs-lookup"><span data-stu-id="9c847-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="9c847-221">Belső projekt</span><span class="sxs-lookup"><span data-stu-id="9c847-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="9c847-222">Idő és anyagok</span><span class="sxs-lookup"><span data-stu-id="9c847-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="9c847-223">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="9c847-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="9c847-224">Tények</span><span class="sxs-lookup"><span data-stu-id="9c847-224">Actuals</span></span></th>
<th><span data-ttu-id="9c847-225">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-225">Transaction currency</span></span></th>
<th><span data-ttu-id="9c847-226">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="9c847-226">Fixed price</span></span></th>
<th><span data-ttu-id="9c847-227">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9c847-228">Létrejön egy időbejegyzés.</span><span class="sxs-lookup"><span data-stu-id="9c847-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="9c847-229">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="9c847-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-230">A rendszer elküld egy időbejegyzést.</span><span class="sxs-lookup"><span data-stu-id="9c847-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="9c847-231">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="9c847-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="9c847-232">Az időt elfogadják, és a jóváhagyáskor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="9c847-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9c847-233">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="9c847-233">Cost actual</span></span></td>
<td><span data-ttu-id="9c847-234">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="9c847-235">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="9c847-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="9c847-236">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="9c847-237">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="9c847-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="9c847-238">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="9c847-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-239">Tényeleges számlázatlan értékesítés – Felszámítható</span><span class="sxs-lookup"><span data-stu-id="9c847-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="9c847-240">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-241">Erőforrás-kezelő részleg költsége</span><span class="sxs-lookup"><span data-stu-id="9c847-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="9c847-242">Erőforrás-kezelő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-243">Szervezetek közötti értékesítések</span><span class="sxs-lookup"><span data-stu-id="9c847-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="9c847-244">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="9c847-245">Az időt elfogadják, és a jóváhagyáskor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="9c847-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9c847-246">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="9c847-246">Cost actual</span></span></td>
<td><span data-ttu-id="9c847-247">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9c847-248">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="9c847-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="9c847-249">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9c847-250">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="9c847-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="9c847-251">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="9c847-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-252">Erőforrás-kezelő részleg költsége</span><span class="sxs-lookup"><span data-stu-id="9c847-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="9c847-253">Erőforrás-kezelő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-254">Szervezetek közötti értékesítések</span><span class="sxs-lookup"><span data-stu-id="9c847-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="9c847-255">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-256">Tényleges számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="9c847-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9c847-257">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-258">Tényleges számlázatlan értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="9c847-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9c847-259">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9c847-260">Egy számla megerősítésekor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="9c847-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9c847-261">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="9c847-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9c847-262">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9c847-263">Mérföldkőhöz tartozó számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="9c847-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="9c847-264">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9c847-265">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="9c847-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="9c847-266">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="9c847-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-267">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="9c847-267">Billed sales</span></span></td>
<td><span data-ttu-id="9c847-268">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9c847-269">Egy számla megerősítésekor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="9c847-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9c847-270">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="9c847-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9c847-271">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9c847-272">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="9c847-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9c847-273">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="9c847-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9c847-274">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="9c847-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9c847-275">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="9c847-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-276">Számlázott értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="9c847-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9c847-277">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-278">Számlázott értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="9c847-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9c847-279">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9c847-280">Egy számla javítva a felszámítható mennyiség növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="9c847-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9c847-281">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="9c847-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9c847-282">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="9c847-283">Mérföldkőhöz tartozó sztornózott értékesítés</span><span class="sxs-lookup"><span data-stu-id="9c847-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="9c847-284">A mérföldkő <strong>Számlázott</strong> állapotból <strong>Számlázásra készen áll</strong> állapotba kerül</span><span class="sxs-lookup"><span data-stu-id="9c847-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="9c847-285">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9c847-286">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="9c847-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="9c847-287">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="9c847-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-288">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="9c847-288">Billed sales</span></span></td>
<td><span data-ttu-id="9c847-289">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9c847-290">Egy számla javítva a felszámítható mennyiség csökkentéséhez.</span><span class="sxs-lookup"><span data-stu-id="9c847-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9c847-291">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="9c847-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9c847-292">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-293">Számlázott értékesítés az új mennyiséghez</span><span class="sxs-lookup"><span data-stu-id="9c847-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="9c847-294">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c847-295">Számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="9c847-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="9c847-296">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="9c847-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
