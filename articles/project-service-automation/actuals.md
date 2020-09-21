---
title: Tények
description: Ez a témakör a projektek tényadataival kapcsolatban nyújt tájékoztatást.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752288"
---
# <a name="actuals"></a><span data-ttu-id="6a71f-103">Tények</span><span class="sxs-lookup"><span data-stu-id="6a71f-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6a71f-104">A tények a projektben befejezett munka mennyiségét jelentik.</span><span class="sxs-lookup"><span data-stu-id="6a71f-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="6a71f-105">A projektek tényadatai visszavezethetők a forrásdokumentumokhoz.</span><span class="sxs-lookup"><span data-stu-id="6a71f-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="6a71f-106">Ezek a forrásdokumentumok többek között idő-, költség-és naplóbejegyzések, valamint számlák.</span><span class="sxs-lookup"><span data-stu-id="6a71f-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Hogyan vezethetők vissza a projekt tényadatok a forrásdokumentumokhoz](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="6a71f-108">Időbejegyzés elküldése</span><span class="sxs-lookup"><span data-stu-id="6a71f-108">Submitting a time entry</span></span>

<span data-ttu-id="6a71f-109">A PSA-ban, amikor egy idő- és anyagelszámolású szerződéssorra leképezett projekthez küldenek be időbejegyzést, két naplósor jön létre.</span><span class="sxs-lookup"><span data-stu-id="6a71f-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="6a71f-110">Az egyik sor a költségre, míg a másik a számlázatlan értékesítésre szolgál.</span><span class="sxs-lookup"><span data-stu-id="6a71f-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="6a71f-111">Amikor egy rögzített árú szerződéssorra leképezett projekthez küldenek be időbejegyzést, csak a költségekre vonatkozó naplósor jön létre.</span><span class="sxs-lookup"><span data-stu-id="6a71f-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="6a71f-112">Az alapértelmezett árak megadásának logikája a naplósorban található.</span><span class="sxs-lookup"><span data-stu-id="6a71f-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="6a71f-113">Az időbejegyzésből származó mezőértékek mindegyike a naplósorba van másolva.</span><span class="sxs-lookup"><span data-stu-id="6a71f-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="6a71f-114">Ezekben a mezőkben szerepel a tranzakció dátuma, a projekthez leképezett szerződéssor, és a megfelelő árlistában szereplő pénznem.</span><span class="sxs-lookup"><span data-stu-id="6a71f-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="6a71f-115">Az alapértelmezett árakra hatással lévő mezők, például a **Szerepkör** és a **Szervezeti egység** mezők a naplósorban alapértelmezés szerint megfelelő áron jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="6a71f-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="6a71f-116">Ha egyéni mezőt ad hozzá az időbejegyzéshez, és azt szeretné, hogy a mező értéke a tényadatokra legyen propagálva, hozza létre a mezőt a Tények entitáson, és a mezők leképezésével másolja a mezőt az időbejegyzésből a tényekhez.</span><span class="sxs-lookup"><span data-stu-id="6a71f-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="6a71f-117">Költségbejegyzés elküldése</span><span class="sxs-lookup"><span data-stu-id="6a71f-117">Submitting an expense entry</span></span>

<span data-ttu-id="6a71f-118">A PSA-ban, amikor egy idő- és anyagelszámolású szerződéssorra leképezett projekthez küldenek be költségbejegyzést, két naplósor jön létre.</span><span class="sxs-lookup"><span data-stu-id="6a71f-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="6a71f-119">Az egyik sor a költségre, míg a másik a számlázatlan értékesítésre szolgál.</span><span class="sxs-lookup"><span data-stu-id="6a71f-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="6a71f-120">Amikor egy rögzített árú szerződéssorra leképezett projekthez küldenek be költségbejegyzést, csak a költségekre vonatkozó naplósor jön létre.</span><span class="sxs-lookup"><span data-stu-id="6a71f-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="6a71f-121">A költségekre vonatkozó alapértelmezett árak megadásának logikája a **Költségbejegyzés** lapon kiválasztott költségkategórián alapul.</span><span class="sxs-lookup"><span data-stu-id="6a71f-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="6a71f-122">A tranzakció dátuma, a projekthez leképezett szerződéssor és a pénznem mind a megfelelő árlista meghatározására szolgál.</span><span class="sxs-lookup"><span data-stu-id="6a71f-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="6a71f-123">Az ár esetében azonban a felhasználó által megadott összeg, alapértelmezés szerint közvetlenül a kapcsolódó költség-naplósorokban van beállítva a költségre és értékesítésre vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="6a71f-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="6a71f-124">A PSA jelenlegi verziójában nem áll rendelkezésre az egységenkénti alapértelmezett ár kategória alapú megadása a költségbejegyzésekre vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="6a71f-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="6a71f-125">Naplók használata a költségek rögzítésére</span><span class="sxs-lookup"><span data-stu-id="6a71f-125">Using journals to record costs</span></span>

<span data-ttu-id="6a71f-126">A PSA-ban a naplók segítségével rögzítheti a költséget vagy bevételt az anyag-, díj-, idő-, költség- vagy adózási tranzakciók osztályaiban.</span><span class="sxs-lookup"><span data-stu-id="6a71f-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="6a71f-127">A napló fejlécet, sorokat és egy **Megerősítés** műveletet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="6a71f-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="6a71f-128">Az alábbi helyzetekben érdemes naplót használni:</span><span class="sxs-lookup"><span data-stu-id="6a71f-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="6a71f-129">Amikor tényleges költségeket és értékesítéseket kell rögzíteni a projektben.</span><span class="sxs-lookup"><span data-stu-id="6a71f-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="6a71f-130">Amikor tranzakciós tényeket kell egy másik rendszerből a PSA-ba áthelyezni.</span><span class="sxs-lookup"><span data-stu-id="6a71f-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="6a71f-131">Amikor rögzítenie kell a másik rendszerben felmerült költségeket, például beszerzési vagy alvállalkozói költségeket.</span><span class="sxs-lookup"><span data-stu-id="6a71f-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="6a71f-132">Tényadatok rögzítése projektesemények alapján</span><span class="sxs-lookup"><span data-stu-id="6a71f-132">Recording actuals based on project events</span></span>

<span data-ttu-id="6a71f-133">A PSA rögzíti a projekt során bekövetkező pénzügyi tranzakciókat.</span><span class="sxs-lookup"><span data-stu-id="6a71f-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="6a71f-134">Ezeket a tranzakciókat a rendszer **tényadatokként** rögzíti.</span><span class="sxs-lookup"><span data-stu-id="6a71f-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="6a71f-135">A következő táblázatok a létrehozott tényadatok különböző típusait mutatják be attól függően, hogy a projekt idő- és anyagelszámolású vagy rögzített árú projekt, elővásárlási fázisban van-e, vagy belső projekt-e.</span><span class="sxs-lookup"><span data-stu-id="6a71f-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="6a71f-136">**Az erőforrás ugyanahhoz a szervezeti egységhez tartozik, mint a projekt szerződő részlege**</span><span class="sxs-lookup"><span data-stu-id="6a71f-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="6a71f-137">Esemény</span><span class="sxs-lookup"><span data-stu-id="6a71f-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="6a71f-138">Számlázható vagy értékesített projekt</span><span class="sxs-lookup"><span data-stu-id="6a71f-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="6a71f-139">Elővásárlási szakaszban lévő projekt</span><span class="sxs-lookup"><span data-stu-id="6a71f-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="6a71f-140">Belső projekt</span><span class="sxs-lookup"><span data-stu-id="6a71f-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="6a71f-141">Idő és anyagok</span><span class="sxs-lookup"><span data-stu-id="6a71f-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="6a71f-142">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="6a71f-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6a71f-143">Tények</span><span class="sxs-lookup"><span data-stu-id="6a71f-143">Actuals</span></span></th>
<th><span data-ttu-id="6a71f-144">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-144">Transaction currency</span></span></th>
<th><span data-ttu-id="6a71f-145">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="6a71f-145">Fixed price</span></span></th>
<th><span data-ttu-id="6a71f-146">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a71f-147">Létrejön egy időbejegyzés.</span><span class="sxs-lookup"><span data-stu-id="6a71f-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="6a71f-148">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="6a71f-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-149">A rendszer elküld egy időbejegyzést.</span><span class="sxs-lookup"><span data-stu-id="6a71f-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="6a71f-150">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="6a71f-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6a71f-151">Az időt elfogadják, és a jóváhagyáskor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="6a71f-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6a71f-152">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="6a71f-152">Cost actual</span></span></td>
<td><span data-ttu-id="6a71f-153">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6a71f-154">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="6a71f-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="6a71f-155">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="6a71f-156">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="6a71f-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="6a71f-157">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="6a71f-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-158">Tényeleges számlázatlan értékesítés – Felszámítható</span><span class="sxs-lookup"><span data-stu-id="6a71f-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="6a71f-159">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6a71f-160">Az időt elfogadják, és a jóváhagyáskor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="6a71f-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6a71f-161">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="6a71f-161">Cost actual</span></span></td>
<td><span data-ttu-id="6a71f-162">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6a71f-163">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="6a71f-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="6a71f-164">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6a71f-165">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="6a71f-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="6a71f-166">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="6a71f-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-167">Tényleges számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="6a71f-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6a71f-168">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-169">Tényleges számlázatlan értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="6a71f-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6a71f-170">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6a71f-171">Egy számla megerősítésekor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="6a71f-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6a71f-172">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="6a71f-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6a71f-173">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6a71f-174">Mérföldkőhöz tartozó számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="6a71f-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="6a71f-175">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6a71f-176">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="6a71f-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="6a71f-177">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="6a71f-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-178">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="6a71f-178">Billed sales</span></span></td>
<td><span data-ttu-id="6a71f-179">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6a71f-180">Egy számla megerősítésekor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="6a71f-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6a71f-181">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="6a71f-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6a71f-182">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6a71f-183">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="6a71f-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6a71f-184">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="6a71f-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6a71f-185">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="6a71f-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6a71f-186">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="6a71f-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-187">Számlázott értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="6a71f-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6a71f-188">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-189">Számlázott értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="6a71f-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6a71f-190">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6a71f-191">Egy számla javítva a felszámítható mennyiség növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="6a71f-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6a71f-192">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="6a71f-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6a71f-193">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="6a71f-194">Mérföldkőhöz tartozó sztornózott értékesítés</span><span class="sxs-lookup"><span data-stu-id="6a71f-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="6a71f-195">A mérföldkő <strong>Számlázott</strong> állapotból <strong>Számlázásra készen áll</strong> állapotba kerül</span><span class="sxs-lookup"><span data-stu-id="6a71f-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="6a71f-196">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6a71f-197">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="6a71f-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="6a71f-198">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="6a71f-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-199">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="6a71f-199">Billed sales</span></span></td>
<td><span data-ttu-id="6a71f-200">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6a71f-201">Egy számla javítva a felszámítható mennyiség csökkentéséhez.</span><span class="sxs-lookup"><span data-stu-id="6a71f-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6a71f-202">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="6a71f-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6a71f-203">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-204">Számlázott értékesítés az új mennyiséghez</span><span class="sxs-lookup"><span data-stu-id="6a71f-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="6a71f-205">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-206">Számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="6a71f-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="6a71f-207">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6a71f-208">**Az erőforrás egy olyan szervezeti egységhez tartozik, amely a projekt szerződő részlegétől eltérő**</span><span class="sxs-lookup"><span data-stu-id="6a71f-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="6a71f-209">Esemény</span><span class="sxs-lookup"><span data-stu-id="6a71f-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="6a71f-210">Számlázható vagy értékesített projekt</span><span class="sxs-lookup"><span data-stu-id="6a71f-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="6a71f-211">Elővásárlási szakaszban lévő projekt</span><span class="sxs-lookup"><span data-stu-id="6a71f-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="6a71f-212">Belső projekt</span><span class="sxs-lookup"><span data-stu-id="6a71f-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="6a71f-213">Idő és anyagok</span><span class="sxs-lookup"><span data-stu-id="6a71f-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="6a71f-214">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="6a71f-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6a71f-215">Tények</span><span class="sxs-lookup"><span data-stu-id="6a71f-215">Actuals</span></span></th>
<th><span data-ttu-id="6a71f-216">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-216">Transaction currency</span></span></th>
<th><span data-ttu-id="6a71f-217">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="6a71f-217">Fixed price</span></span></th>
<th><span data-ttu-id="6a71f-218">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a71f-219">Létrejön egy időbejegyzés.</span><span class="sxs-lookup"><span data-stu-id="6a71f-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="6a71f-220">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="6a71f-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-221">A rendszer elküld egy időbejegyzést.</span><span class="sxs-lookup"><span data-stu-id="6a71f-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="6a71f-222">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="6a71f-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="6a71f-223">Az időt elfogadják, és a jóváhagyáskor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="6a71f-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6a71f-224">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="6a71f-224">Cost actual</span></span></td>
<td><span data-ttu-id="6a71f-225">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="6a71f-226">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="6a71f-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="6a71f-227">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="6a71f-228">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="6a71f-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="6a71f-229">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="6a71f-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-230">Tényeleges számlázatlan értékesítés – Felszámítható</span><span class="sxs-lookup"><span data-stu-id="6a71f-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="6a71f-231">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-232">Erőforrás-kezelő részleg költsége</span><span class="sxs-lookup"><span data-stu-id="6a71f-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="6a71f-233">Erőforrás-kezelő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-234">Szervezetek közötti értékesítések</span><span class="sxs-lookup"><span data-stu-id="6a71f-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="6a71f-235">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="6a71f-236">Az időt elfogadják, és a jóváhagyáskor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="6a71f-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6a71f-237">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="6a71f-237">Cost actual</span></span></td>
<td><span data-ttu-id="6a71f-238">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6a71f-239">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="6a71f-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="6a71f-240">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6a71f-241">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="6a71f-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="6a71f-242">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="6a71f-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-243">Erőforrás-kezelő részleg költsége</span><span class="sxs-lookup"><span data-stu-id="6a71f-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="6a71f-244">Erőforrás-kezelő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-245">Szervezetek közötti értékesítések</span><span class="sxs-lookup"><span data-stu-id="6a71f-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="6a71f-246">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-247">Tényleges számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="6a71f-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6a71f-248">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-249">Tényleges számlázatlan értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="6a71f-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6a71f-250">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6a71f-251">Egy számla megerősítésekor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="6a71f-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6a71f-252">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="6a71f-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6a71f-253">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6a71f-254">Mérföldkőhöz tartozó számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="6a71f-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="6a71f-255">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6a71f-256">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="6a71f-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="6a71f-257">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="6a71f-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-258">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="6a71f-258">Billed sales</span></span></td>
<td><span data-ttu-id="6a71f-259">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6a71f-260">Egy számla megerősítésekor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="6a71f-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6a71f-261">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="6a71f-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6a71f-262">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6a71f-263">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="6a71f-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6a71f-264">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="6a71f-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6a71f-265">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="6a71f-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6a71f-266">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="6a71f-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-267">Számlázott értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="6a71f-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6a71f-268">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-269">Számlázott értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="6a71f-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6a71f-270">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6a71f-271">Egy számla javítva a felszámítható mennyiség növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="6a71f-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6a71f-272">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="6a71f-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6a71f-273">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="6a71f-274">Mérföldkőhöz tartozó sztornózott értékesítés</span><span class="sxs-lookup"><span data-stu-id="6a71f-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="6a71f-275">A mérföldkő <strong>Számlázott</strong> állapotból <strong>Számlázásra készen áll</strong> állapotba kerül</span><span class="sxs-lookup"><span data-stu-id="6a71f-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="6a71f-276">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6a71f-277">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="6a71f-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="6a71f-278">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="6a71f-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-279">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="6a71f-279">Billed sales</span></span></td>
<td><span data-ttu-id="6a71f-280">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6a71f-281">Egy számla javítva a felszámítható mennyiség csökkentéséhez.</span><span class="sxs-lookup"><span data-stu-id="6a71f-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6a71f-282">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="6a71f-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6a71f-283">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-284">Számlázott értékesítés az új mennyiséghez</span><span class="sxs-lookup"><span data-stu-id="6a71f-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="6a71f-285">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a71f-286">Számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="6a71f-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="6a71f-287">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="6a71f-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
