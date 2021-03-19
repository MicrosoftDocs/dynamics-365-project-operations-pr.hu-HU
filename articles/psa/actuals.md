---
title: Tényadatok áttekintése
description: Ez a témakör a projektek tényadataival kapcsolatban nyújt tájékoztatást.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c4a3424bed704243dfb5524fa541c3fcc0899e57
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285621"
---
# <a name="actuals-overview"></a><span data-ttu-id="d87bf-103">Tényadatok áttekintése</span><span class="sxs-lookup"><span data-stu-id="d87bf-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d87bf-104">A tények a projektben befejezett munka mennyiségét jelentik.</span><span class="sxs-lookup"><span data-stu-id="d87bf-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="d87bf-105">A projektek tényadatai visszavezethetők a forrásdokumentumokhoz.</span><span class="sxs-lookup"><span data-stu-id="d87bf-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="d87bf-106">Ezek a forrásdokumentumok többek között idő-, költség-és naplóbejegyzések, valamint számlák.</span><span class="sxs-lookup"><span data-stu-id="d87bf-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Hogyan vezethetők vissza a projekt tényadatok a forrásdokumentumokhoz](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="d87bf-108">Időbejegyzés elküldése</span><span class="sxs-lookup"><span data-stu-id="d87bf-108">Submitting a time entry</span></span>

<span data-ttu-id="d87bf-109">A PSA-ban, amikor egy idő- és anyagelszámolású szerződéssorra leképezett projekthez küldenek be időbejegyzést, két naplósor jön létre.</span><span class="sxs-lookup"><span data-stu-id="d87bf-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="d87bf-110">Az egyik sor a költségre, míg a másik a számlázatlan értékesítésre szolgál.</span><span class="sxs-lookup"><span data-stu-id="d87bf-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="d87bf-111">Amikor egy rögzített árú szerződéssorra leképezett projekthez küldenek be időbejegyzést, csak a költségekre vonatkozó naplósor jön létre.</span><span class="sxs-lookup"><span data-stu-id="d87bf-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="d87bf-112">Az alapértelmezett árak megadásának logikája a naplósorban található.</span><span class="sxs-lookup"><span data-stu-id="d87bf-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="d87bf-113">Az időbejegyzésből származó mezőértékek mindegyike a naplósorba van másolva.</span><span class="sxs-lookup"><span data-stu-id="d87bf-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="d87bf-114">Ezekben a mezőkben szerepel a tranzakció dátuma, a projekthez leképezett szerződéssor, és a megfelelő árlistában szereplő pénznem.</span><span class="sxs-lookup"><span data-stu-id="d87bf-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="d87bf-115">Az alapértelmezett árakra hatással lévő mezők, például a **Szerepkör** és a **Szervezeti egység** mezők a naplósorban alapértelmezés szerint megfelelő áron jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="d87bf-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="d87bf-116">Ha egyéni mezőt ad hozzá az időbejegyzéshez, és azt szeretné, hogy a mező értéke a tényadatokra legyen propagálva, hozza létre a mezőt a Tények entitáson, és a mezők leképezésével másolja a mezőt az időbejegyzésből a tényekhez.</span><span class="sxs-lookup"><span data-stu-id="d87bf-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="d87bf-117">Költségbejegyzés elküldése</span><span class="sxs-lookup"><span data-stu-id="d87bf-117">Submitting an expense entry</span></span>

<span data-ttu-id="d87bf-118">A PSA-ban, amikor egy idő- és anyagelszámolású szerződéssorra leképezett projekthez küldenek be költségbejegyzést, két naplósor jön létre.</span><span class="sxs-lookup"><span data-stu-id="d87bf-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="d87bf-119">Az egyik sor a költségre, míg a másik a számlázatlan értékesítésre szolgál.</span><span class="sxs-lookup"><span data-stu-id="d87bf-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="d87bf-120">Amikor egy rögzített árú szerződéssorra leképezett projekthez küldenek be költségbejegyzést, csak a költségekre vonatkozó naplósor jön létre.</span><span class="sxs-lookup"><span data-stu-id="d87bf-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="d87bf-121">A költségekre vonatkozó alapértelmezett árak megadásának logikája a **Költségbejegyzés** lapon kiválasztott költségkategórián alapul.</span><span class="sxs-lookup"><span data-stu-id="d87bf-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="d87bf-122">A tranzakció dátuma, a projekthez leképezett szerződéssor és a pénznem mind a megfelelő árlista meghatározására szolgál.</span><span class="sxs-lookup"><span data-stu-id="d87bf-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="d87bf-123">Az ár esetében azonban a felhasználó által megadott összeg, alapértelmezés szerint közvetlenül a kapcsolódó költség-naplósorokban van beállítva a költségre és értékesítésre vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="d87bf-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="d87bf-124">A PSA jelenlegi verziójában nem áll rendelkezésre az egységenkénti alapértelmezett ár kategória alapú megadása a költségbejegyzésekre vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="d87bf-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="d87bf-125">Rekordaplók használata a költségek rögzítésére</span><span class="sxs-lookup"><span data-stu-id="d87bf-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="d87bf-126">A PSA-ban a rekordnaplók segítségével rögzítheti a költséget vagy bevételt az anyag-, díj-, idő-, költség- vagy adózási tranzakciók osztályaiban.</span><span class="sxs-lookup"><span data-stu-id="d87bf-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="d87bf-127">A napló fejlécet, sorokat és egy **Megerősítés** műveletet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="d87bf-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="d87bf-128">Az alábbi helyzetekben érdemes naplót használni:</span><span class="sxs-lookup"><span data-stu-id="d87bf-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="d87bf-129">Amikor tényleges költségeket és értékesítéseket kell rögzíteni a projektben.</span><span class="sxs-lookup"><span data-stu-id="d87bf-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="d87bf-130">Amikor tranzakciós tényeket kell egy másik rendszerből a PSA-ba áthelyezni.</span><span class="sxs-lookup"><span data-stu-id="d87bf-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="d87bf-131">Amikor rögzítenie kell a másik rendszerben felmerült költségeket, például beszerzési vagy alvállalkozói költségeket.</span><span class="sxs-lookup"><span data-stu-id="d87bf-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d87bf-132">A Rekordnaplók létrehozásakor a tényleges adatokat csak olyan felhasználó hozhatja létre, aki teljes mértékben tisztában van azzal, hogy milyen hatással vannak azok a tényleges adatokra a projekten.</span><span class="sxs-lookup"><span data-stu-id="d87bf-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="d87bf-133">Ennek oka az, hogy az alkalmazás nem ellenőrzi a naplósor típusát, vagy a kapcsolódó árazást, amelyeket a naplósorban adtak meg.</span><span class="sxs-lookup"><span data-stu-id="d87bf-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="d87bf-134">A naplótípus hatása miatt kellő óvatossággal kell eljárnia, hogy ki kapja meg a belépési naplók létrehozásához szükséges hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="d87bf-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="d87bf-135">Tényadatok rögzítése projektesemények alapján</span><span class="sxs-lookup"><span data-stu-id="d87bf-135">Recording actuals based on project events</span></span>

<span data-ttu-id="d87bf-136">A PSA rögzíti a projekt során bekövetkező pénzügyi tranzakciókat.</span><span class="sxs-lookup"><span data-stu-id="d87bf-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="d87bf-137">Ezeket a tranzakciókat a rendszer **tényadatokként** rögzíti.</span><span class="sxs-lookup"><span data-stu-id="d87bf-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="d87bf-138">A következő táblázatok a létrehozott tényadatok különböző típusait mutatják be attól függően, hogy a projekt idő- és anyagelszámolású vagy rögzített árú projekt, elővásárlási fázisban van-e, vagy belső projekt-e.</span><span class="sxs-lookup"><span data-stu-id="d87bf-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="d87bf-139">**Az erőforrás ugyanahhoz a szervezeti egységhez tartozik, mint a projekt szerződő részlege**</span><span class="sxs-lookup"><span data-stu-id="d87bf-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="d87bf-140">Esemény</span><span class="sxs-lookup"><span data-stu-id="d87bf-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="d87bf-141">Számlázható vagy értékesített projekt</span><span class="sxs-lookup"><span data-stu-id="d87bf-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="d87bf-142">Elővásárlási szakaszban lévő projekt</span><span class="sxs-lookup"><span data-stu-id="d87bf-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="d87bf-143">Belső projekt</span><span class="sxs-lookup"><span data-stu-id="d87bf-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="d87bf-144">Idő és anyagok</span><span class="sxs-lookup"><span data-stu-id="d87bf-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="d87bf-145">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="d87bf-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d87bf-146">Tények</span><span class="sxs-lookup"><span data-stu-id="d87bf-146">Actuals</span></span></th>
<th><span data-ttu-id="d87bf-147">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-147">Transaction currency</span></span></th>
<th><span data-ttu-id="d87bf-148">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="d87bf-148">Fixed price</span></span></th>
<th><span data-ttu-id="d87bf-149">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d87bf-150">Létrejön egy időbejegyzés.</span><span class="sxs-lookup"><span data-stu-id="d87bf-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="d87bf-151">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="d87bf-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-152">A rendszer elküld egy időbejegyzést.</span><span class="sxs-lookup"><span data-stu-id="d87bf-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="d87bf-153">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="d87bf-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d87bf-154">Az időt elfogadják, és a jóváhagyáskor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="d87bf-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d87bf-155">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="d87bf-155">Cost actual</span></span></td>
<td><span data-ttu-id="d87bf-156">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d87bf-157">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="d87bf-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="d87bf-158">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="d87bf-159">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="d87bf-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="d87bf-160">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="d87bf-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-161">Tényeleges számlázatlan értékesítés – Felszámítható</span><span class="sxs-lookup"><span data-stu-id="d87bf-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="d87bf-162">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d87bf-163">Az időt elfogadják, és a jóváhagyáskor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="d87bf-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d87bf-164">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="d87bf-164">Cost actual</span></span></td>
<td><span data-ttu-id="d87bf-165">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d87bf-166">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="d87bf-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="d87bf-167">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d87bf-168">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="d87bf-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="d87bf-169">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="d87bf-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-170">Tényleges számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="d87bf-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d87bf-171">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-172">Tényleges számlázatlan értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="d87bf-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d87bf-173">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d87bf-174">Egy számla megerősítésekor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="d87bf-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d87bf-175">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="d87bf-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d87bf-176">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d87bf-177">Mérföldkőhöz tartozó számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="d87bf-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="d87bf-178">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d87bf-179">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="d87bf-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="d87bf-180">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="d87bf-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-181">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="d87bf-181">Billed sales</span></span></td>
<td><span data-ttu-id="d87bf-182">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d87bf-183">Egy számla megerősítésekor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="d87bf-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d87bf-184">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="d87bf-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d87bf-185">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d87bf-186">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="d87bf-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d87bf-187">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="d87bf-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d87bf-188">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="d87bf-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d87bf-189">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="d87bf-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-190">Számlázott értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="d87bf-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d87bf-191">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-192">Számlázott értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="d87bf-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d87bf-193">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d87bf-194">Egy számla javítva a felszámítható mennyiség növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="d87bf-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d87bf-195">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="d87bf-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d87bf-196">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="d87bf-197">Mérföldkőhöz tartozó sztornózott értékesítés</span><span class="sxs-lookup"><span data-stu-id="d87bf-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="d87bf-198">A mérföldkő <strong>Számlázott</strong> állapotból <strong>Számlázásra készen áll</strong> állapotba kerül</span><span class="sxs-lookup"><span data-stu-id="d87bf-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="d87bf-199">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d87bf-200">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="d87bf-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="d87bf-201">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="d87bf-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-202">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="d87bf-202">Billed sales</span></span></td>
<td><span data-ttu-id="d87bf-203">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d87bf-204">Egy számla javítva a felszámítható mennyiség csökkentéséhez.</span><span class="sxs-lookup"><span data-stu-id="d87bf-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d87bf-205">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="d87bf-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d87bf-206">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-207">Számlázott értékesítés az új mennyiséghez</span><span class="sxs-lookup"><span data-stu-id="d87bf-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="d87bf-208">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-209">Számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="d87bf-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="d87bf-210">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d87bf-211">**Az erőforrás egy olyan szervezeti egységhez tartozik, amely a projekt szerződő részlegétől eltérő**</span><span class="sxs-lookup"><span data-stu-id="d87bf-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="d87bf-212">Esemény</span><span class="sxs-lookup"><span data-stu-id="d87bf-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="d87bf-213">Számlázható vagy értékesített projekt</span><span class="sxs-lookup"><span data-stu-id="d87bf-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="d87bf-214">Elővásárlási szakaszban lévő projekt</span><span class="sxs-lookup"><span data-stu-id="d87bf-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="d87bf-215">Belső projekt</span><span class="sxs-lookup"><span data-stu-id="d87bf-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="d87bf-216">Idő és anyagok</span><span class="sxs-lookup"><span data-stu-id="d87bf-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="d87bf-217">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="d87bf-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d87bf-218">Tények</span><span class="sxs-lookup"><span data-stu-id="d87bf-218">Actuals</span></span></th>
<th><span data-ttu-id="d87bf-219">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-219">Transaction currency</span></span></th>
<th><span data-ttu-id="d87bf-220">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="d87bf-220">Fixed price</span></span></th>
<th><span data-ttu-id="d87bf-221">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d87bf-222">Létrejön egy időbejegyzés.</span><span class="sxs-lookup"><span data-stu-id="d87bf-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="d87bf-223">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="d87bf-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-224">A rendszer elküld egy időbejegyzést.</span><span class="sxs-lookup"><span data-stu-id="d87bf-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="d87bf-225">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="d87bf-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="d87bf-226">Az időt elfogadják, és a jóváhagyáskor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="d87bf-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d87bf-227">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="d87bf-227">Cost actual</span></span></td>
<td><span data-ttu-id="d87bf-228">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="d87bf-229">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="d87bf-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="d87bf-230">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="d87bf-231">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="d87bf-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="d87bf-232">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="d87bf-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-233">Tényeleges számlázatlan értékesítés – Felszámítható</span><span class="sxs-lookup"><span data-stu-id="d87bf-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="d87bf-234">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-235">Erőforrás-kezelő részleg költsége</span><span class="sxs-lookup"><span data-stu-id="d87bf-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="d87bf-236">Erőforrás-kezelő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-237">Szervezetek közötti értékesítések</span><span class="sxs-lookup"><span data-stu-id="d87bf-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="d87bf-238">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="d87bf-239">Az időt elfogadják, és a jóváhagyáskor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="d87bf-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d87bf-240">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="d87bf-240">Cost actual</span></span></td>
<td><span data-ttu-id="d87bf-241">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d87bf-242">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="d87bf-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="d87bf-243">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d87bf-244">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="d87bf-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="d87bf-245">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="d87bf-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-246">Erőforrás-kezelő részleg költsége</span><span class="sxs-lookup"><span data-stu-id="d87bf-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="d87bf-247">Erőforrás-kezelő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-248">Szervezetek közötti értékesítések</span><span class="sxs-lookup"><span data-stu-id="d87bf-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="d87bf-249">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-250">Tényleges számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="d87bf-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d87bf-251">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-252">Tényleges számlázatlan értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="d87bf-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d87bf-253">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d87bf-254">Egy számla megerősítésekor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="d87bf-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d87bf-255">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="d87bf-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d87bf-256">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d87bf-257">Mérföldkőhöz tartozó számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="d87bf-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="d87bf-258">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d87bf-259">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="d87bf-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="d87bf-260">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="d87bf-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-261">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="d87bf-261">Billed sales</span></span></td>
<td><span data-ttu-id="d87bf-262">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d87bf-263">Egy számla megerősítésekor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="d87bf-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d87bf-264">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="d87bf-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d87bf-265">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d87bf-266">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="d87bf-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d87bf-267">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="d87bf-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d87bf-268">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="d87bf-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d87bf-269">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="d87bf-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-270">Számlázott értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="d87bf-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d87bf-271">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-272">Számlázott értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="d87bf-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d87bf-273">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d87bf-274">Egy számla javítva a felszámítható mennyiség növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="d87bf-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d87bf-275">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="d87bf-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d87bf-276">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="d87bf-277">Mérföldkőhöz tartozó sztornózott értékesítés</span><span class="sxs-lookup"><span data-stu-id="d87bf-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="d87bf-278">A mérföldkő <strong>Számlázott</strong> állapotból <strong>Számlázásra készen áll</strong> állapotba kerül</span><span class="sxs-lookup"><span data-stu-id="d87bf-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="d87bf-279">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d87bf-280">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="d87bf-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="d87bf-281">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="d87bf-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-282">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="d87bf-282">Billed sales</span></span></td>
<td><span data-ttu-id="d87bf-283">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d87bf-284">Egy számla javítva a felszámítható mennyiség csökkentéséhez.</span><span class="sxs-lookup"><span data-stu-id="d87bf-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d87bf-285">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="d87bf-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d87bf-286">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-287">Számlázott értékesítés az új mennyiséghez</span><span class="sxs-lookup"><span data-stu-id="d87bf-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="d87bf-288">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d87bf-289">Számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="d87bf-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="d87bf-290">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="d87bf-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]