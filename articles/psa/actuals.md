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
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146126"
---
# <a name="actuals-overview"></a><span data-ttu-id="04ecc-103">Tényadatok áttekintése</span><span class="sxs-lookup"><span data-stu-id="04ecc-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="04ecc-104">A tények a projektben befejezett munka mennyiségét jelentik.</span><span class="sxs-lookup"><span data-stu-id="04ecc-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="04ecc-105">A projektek tényadatai visszavezethetők a forrásdokumentumokhoz.</span><span class="sxs-lookup"><span data-stu-id="04ecc-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="04ecc-106">Ezek a forrásdokumentumok többek között idő-, költség-és naplóbejegyzések, valamint számlák.</span><span class="sxs-lookup"><span data-stu-id="04ecc-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Hogyan vezethetők vissza a projekt tényadatok a forrásdokumentumokhoz](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="04ecc-108">Időbejegyzés elküldése</span><span class="sxs-lookup"><span data-stu-id="04ecc-108">Submitting a time entry</span></span>

<span data-ttu-id="04ecc-109">A PSA-ban, amikor egy idő- és anyagelszámolású szerződéssorra leképezett projekthez küldenek be időbejegyzést, két naplósor jön létre.</span><span class="sxs-lookup"><span data-stu-id="04ecc-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="04ecc-110">Az egyik sor a költségre, míg a másik a számlázatlan értékesítésre szolgál.</span><span class="sxs-lookup"><span data-stu-id="04ecc-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="04ecc-111">Amikor egy rögzített árú szerződéssorra leképezett projekthez küldenek be időbejegyzést, csak a költségekre vonatkozó naplósor jön létre.</span><span class="sxs-lookup"><span data-stu-id="04ecc-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="04ecc-112">Az alapértelmezett árak megadásának logikája a naplósorban található.</span><span class="sxs-lookup"><span data-stu-id="04ecc-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="04ecc-113">Az időbejegyzésből származó mezőértékek mindegyike a naplósorba van másolva.</span><span class="sxs-lookup"><span data-stu-id="04ecc-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="04ecc-114">Ezekben a mezőkben szerepel a tranzakció dátuma, a projekthez leképezett szerződéssor, és a megfelelő árlistában szereplő pénznem.</span><span class="sxs-lookup"><span data-stu-id="04ecc-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="04ecc-115">Az alapértelmezett árakra hatással lévő mezők, például a **Szerepkör** és a **Szervezeti egység** mezők a naplósorban alapértelmezés szerint megfelelő áron jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="04ecc-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="04ecc-116">Ha egyéni mezőt ad hozzá az időbejegyzéshez, és azt szeretné, hogy a mező értéke a tényadatokra legyen propagálva, hozza létre a mezőt a Tények entitáson, és a mezők leképezésével másolja a mezőt az időbejegyzésből a tényekhez.</span><span class="sxs-lookup"><span data-stu-id="04ecc-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="04ecc-117">Költségbejegyzés elküldése</span><span class="sxs-lookup"><span data-stu-id="04ecc-117">Submitting an expense entry</span></span>

<span data-ttu-id="04ecc-118">A PSA-ban, amikor egy idő- és anyagelszámolású szerződéssorra leképezett projekthez küldenek be költségbejegyzést, két naplósor jön létre.</span><span class="sxs-lookup"><span data-stu-id="04ecc-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="04ecc-119">Az egyik sor a költségre, míg a másik a számlázatlan értékesítésre szolgál.</span><span class="sxs-lookup"><span data-stu-id="04ecc-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="04ecc-120">Amikor egy rögzített árú szerződéssorra leképezett projekthez küldenek be költségbejegyzést, csak a költségekre vonatkozó naplósor jön létre.</span><span class="sxs-lookup"><span data-stu-id="04ecc-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="04ecc-121">A költségekre vonatkozó alapértelmezett árak megadásának logikája a **Költségbejegyzés** lapon kiválasztott költségkategórián alapul.</span><span class="sxs-lookup"><span data-stu-id="04ecc-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="04ecc-122">A tranzakció dátuma, a projekthez leképezett szerződéssor és a pénznem mind a megfelelő árlista meghatározására szolgál.</span><span class="sxs-lookup"><span data-stu-id="04ecc-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="04ecc-123">Az ár esetében azonban a felhasználó által megadott összeg, alapértelmezés szerint közvetlenül a kapcsolódó költség-naplósorokban van beállítva a költségre és értékesítésre vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="04ecc-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="04ecc-124">A PSA jelenlegi verziójában nem áll rendelkezésre az egységenkénti alapértelmezett ár kategória alapú megadása a költségbejegyzésekre vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="04ecc-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="04ecc-125">Rekordaplók használata a költségek rögzítésére</span><span class="sxs-lookup"><span data-stu-id="04ecc-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="04ecc-126">A PSA-ban a rekordnaplók segítségével rögzítheti a költséget vagy bevételt az anyag-, díj-, idő-, költség- vagy adózási tranzakciók osztályaiban.</span><span class="sxs-lookup"><span data-stu-id="04ecc-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="04ecc-127">A napló fejlécet, sorokat és egy **Megerősítés** műveletet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="04ecc-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="04ecc-128">Az alábbi helyzetekben érdemes naplót használni:</span><span class="sxs-lookup"><span data-stu-id="04ecc-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="04ecc-129">Amikor tényleges költségeket és értékesítéseket kell rögzíteni a projektben.</span><span class="sxs-lookup"><span data-stu-id="04ecc-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="04ecc-130">Amikor tranzakciós tényeket kell egy másik rendszerből a PSA-ba áthelyezni.</span><span class="sxs-lookup"><span data-stu-id="04ecc-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="04ecc-131">Amikor rögzítenie kell a másik rendszerben felmerült költségeket, például beszerzési vagy alvállalkozói költségeket.</span><span class="sxs-lookup"><span data-stu-id="04ecc-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04ecc-132">A Rekordnaplók létrehozásakor a tényleges adatokat csak olyan felhasználó hozhatja létre, aki teljes mértékben tisztában van azzal, hogy milyen hatással vannak azok a tényleges adatokra a projekten.</span><span class="sxs-lookup"><span data-stu-id="04ecc-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="04ecc-133">Ennek oka az, hogy az alkalmazás nem ellenőrzi a naplósor típusát, vagy a kapcsolódó árazást, amelyeket a naplósorban adtak meg.</span><span class="sxs-lookup"><span data-stu-id="04ecc-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="04ecc-134">A naplótípus hatása miatt kellő óvatossággal kell eljárnia, hogy ki kapja meg a belépési naplók létrehozásához szükséges hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="04ecc-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="04ecc-135">Tényadatok rögzítése projektesemények alapján</span><span class="sxs-lookup"><span data-stu-id="04ecc-135">Recording actuals based on project events</span></span>

<span data-ttu-id="04ecc-136">A PSA rögzíti a projekt során bekövetkező pénzügyi tranzakciókat.</span><span class="sxs-lookup"><span data-stu-id="04ecc-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="04ecc-137">Ezeket a tranzakciókat a rendszer **tényadatokként** rögzíti.</span><span class="sxs-lookup"><span data-stu-id="04ecc-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="04ecc-138">A következő táblázatok a létrehozott tényadatok különböző típusait mutatják be attól függően, hogy a projekt idő- és anyagelszámolású vagy rögzített árú projekt, elővásárlási fázisban van-e, vagy belső projekt-e.</span><span class="sxs-lookup"><span data-stu-id="04ecc-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="04ecc-139">**Az erőforrás ugyanahhoz a szervezeti egységhez tartozik, mint a projekt szerződő részlege**</span><span class="sxs-lookup"><span data-stu-id="04ecc-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="04ecc-140">Esemény</span><span class="sxs-lookup"><span data-stu-id="04ecc-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="04ecc-141">Számlázható vagy értékesített projekt</span><span class="sxs-lookup"><span data-stu-id="04ecc-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="04ecc-142">Elővásárlási szakaszban lévő projekt</span><span class="sxs-lookup"><span data-stu-id="04ecc-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="04ecc-143">Belső projekt</span><span class="sxs-lookup"><span data-stu-id="04ecc-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="04ecc-144">Idő és anyagok</span><span class="sxs-lookup"><span data-stu-id="04ecc-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="04ecc-145">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="04ecc-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="04ecc-146">Tények</span><span class="sxs-lookup"><span data-stu-id="04ecc-146">Actuals</span></span></th>
<th><span data-ttu-id="04ecc-147">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-147">Transaction currency</span></span></th>
<th><span data-ttu-id="04ecc-148">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="04ecc-148">Fixed price</span></span></th>
<th><span data-ttu-id="04ecc-149">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04ecc-150">Létrejön egy időbejegyzés.</span><span class="sxs-lookup"><span data-stu-id="04ecc-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="04ecc-151">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="04ecc-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-152">A rendszer elküld egy időbejegyzést.</span><span class="sxs-lookup"><span data-stu-id="04ecc-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="04ecc-153">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="04ecc-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="04ecc-154">Az időt elfogadják, és a jóváhagyáskor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="04ecc-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="04ecc-155">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="04ecc-155">Cost actual</span></span></td>
<td><span data-ttu-id="04ecc-156">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="04ecc-157">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="04ecc-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="04ecc-158">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="04ecc-159">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="04ecc-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="04ecc-160">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="04ecc-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-161">Tényeleges számlázatlan értékesítés – Felszámítható</span><span class="sxs-lookup"><span data-stu-id="04ecc-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="04ecc-162">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="04ecc-163">Az időt elfogadják, és a jóváhagyáskor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="04ecc-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="04ecc-164">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="04ecc-164">Cost actual</span></span></td>
<td><span data-ttu-id="04ecc-165">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="04ecc-166">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="04ecc-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="04ecc-167">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="04ecc-168">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="04ecc-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="04ecc-169">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="04ecc-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-170">Tényleges számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="04ecc-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="04ecc-171">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-172">Tényleges számlázatlan értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="04ecc-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="04ecc-173">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="04ecc-174">Egy számla megerősítésekor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="04ecc-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="04ecc-175">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="04ecc-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="04ecc-176">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="04ecc-177">Mérföldkőhöz tartozó számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="04ecc-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="04ecc-178">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="04ecc-179">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="04ecc-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="04ecc-180">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="04ecc-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-181">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="04ecc-181">Billed sales</span></span></td>
<td><span data-ttu-id="04ecc-182">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="04ecc-183">Egy számla megerősítésekor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="04ecc-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="04ecc-184">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="04ecc-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="04ecc-185">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="04ecc-186">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="04ecc-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="04ecc-187">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="04ecc-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="04ecc-188">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="04ecc-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="04ecc-189">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="04ecc-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-190">Számlázott értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="04ecc-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="04ecc-191">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-192">Számlázott értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="04ecc-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="04ecc-193">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="04ecc-194">Egy számla javítva a felszámítható mennyiség növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="04ecc-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="04ecc-195">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="04ecc-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="04ecc-196">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="04ecc-197">Mérföldkőhöz tartozó sztornózott értékesítés</span><span class="sxs-lookup"><span data-stu-id="04ecc-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="04ecc-198">A mérföldkő <strong>Számlázott</strong> állapotból <strong>Számlázásra készen áll</strong> állapotba kerül</span><span class="sxs-lookup"><span data-stu-id="04ecc-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="04ecc-199">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="04ecc-200">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="04ecc-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="04ecc-201">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="04ecc-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-202">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="04ecc-202">Billed sales</span></span></td>
<td><span data-ttu-id="04ecc-203">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="04ecc-204">Egy számla javítva a felszámítható mennyiség csökkentéséhez.</span><span class="sxs-lookup"><span data-stu-id="04ecc-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="04ecc-205">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="04ecc-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="04ecc-206">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-207">Számlázott értékesítés az új mennyiséghez</span><span class="sxs-lookup"><span data-stu-id="04ecc-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="04ecc-208">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-209">Számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="04ecc-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="04ecc-210">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04ecc-211">**Az erőforrás egy olyan szervezeti egységhez tartozik, amely a projekt szerződő részlegétől eltérő**</span><span class="sxs-lookup"><span data-stu-id="04ecc-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="04ecc-212">Esemény</span><span class="sxs-lookup"><span data-stu-id="04ecc-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="04ecc-213">Számlázható vagy értékesített projekt</span><span class="sxs-lookup"><span data-stu-id="04ecc-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="04ecc-214">Elővásárlási szakaszban lévő projekt</span><span class="sxs-lookup"><span data-stu-id="04ecc-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="04ecc-215">Belső projekt</span><span class="sxs-lookup"><span data-stu-id="04ecc-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="04ecc-216">Idő és anyagok</span><span class="sxs-lookup"><span data-stu-id="04ecc-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="04ecc-217">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="04ecc-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="04ecc-218">Tények</span><span class="sxs-lookup"><span data-stu-id="04ecc-218">Actuals</span></span></th>
<th><span data-ttu-id="04ecc-219">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-219">Transaction currency</span></span></th>
<th><span data-ttu-id="04ecc-220">Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="04ecc-220">Fixed price</span></span></th>
<th><span data-ttu-id="04ecc-221">Tranzakció pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04ecc-222">Létrejön egy időbejegyzés.</span><span class="sxs-lookup"><span data-stu-id="04ecc-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="04ecc-223">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="04ecc-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-224">A rendszer elküld egy időbejegyzést.</span><span class="sxs-lookup"><span data-stu-id="04ecc-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="04ecc-225">Nincs aktivitás a Tényadatok entitásban</span><span class="sxs-lookup"><span data-stu-id="04ecc-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="04ecc-226">Az időt elfogadják, és a jóváhagyáskor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="04ecc-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="04ecc-227">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="04ecc-227">Cost actual</span></span></td>
<td><span data-ttu-id="04ecc-228">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="04ecc-229">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="04ecc-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="04ecc-230">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="04ecc-231">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="04ecc-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="04ecc-232">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="04ecc-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-233">Tényeleges számlázatlan értékesítés – Felszámítható</span><span class="sxs-lookup"><span data-stu-id="04ecc-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="04ecc-234">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-235">Erőforrás-kezelő részleg költsége</span><span class="sxs-lookup"><span data-stu-id="04ecc-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="04ecc-236">Erőforrás-kezelő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-237">Szervezetek közötti értékesítések</span><span class="sxs-lookup"><span data-stu-id="04ecc-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="04ecc-238">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="04ecc-239">Az időt elfogadják, és a jóváhagyáskor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="04ecc-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="04ecc-240">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="04ecc-240">Cost actual</span></span></td>
<td><span data-ttu-id="04ecc-241">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="04ecc-242">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="04ecc-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="04ecc-243">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="04ecc-244">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="04ecc-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="04ecc-245">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="04ecc-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-246">Erőforrás-kezelő részleg költsége</span><span class="sxs-lookup"><span data-stu-id="04ecc-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="04ecc-247">Erőforrás-kezelő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-248">Szervezetek közötti értékesítések</span><span class="sxs-lookup"><span data-stu-id="04ecc-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="04ecc-249">Szerződő részleg pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-250">Tényleges számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="04ecc-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="04ecc-251">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-252">Tényleges számlázatlan értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="04ecc-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="04ecc-253">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="04ecc-254">Egy számla megerősítésekor nem történik módosítás vagy növekedés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="04ecc-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="04ecc-255">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="04ecc-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="04ecc-256">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="04ecc-257">Mérföldkőhöz tartozó számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="04ecc-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="04ecc-258">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="04ecc-259">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="04ecc-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="04ecc-260">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="04ecc-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-261">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="04ecc-261">Billed sales</span></span></td>
<td><span data-ttu-id="04ecc-262">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="04ecc-263">Egy számla megerősítésekor nem történik csökkenés a számlázható órák értékében.</span><span class="sxs-lookup"><span data-stu-id="04ecc-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="04ecc-264">Sztornózott számlázatlan értékesítés</span><span class="sxs-lookup"><span data-stu-id="04ecc-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="04ecc-265">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="04ecc-266">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="04ecc-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="04ecc-267">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="04ecc-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="04ecc-268">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="04ecc-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="04ecc-269">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="04ecc-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-270">Számlázott értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="04ecc-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="04ecc-271">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-272">Számlázott értékesítés – Az új mennyiségnél nem számítható fel</span><span class="sxs-lookup"><span data-stu-id="04ecc-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="04ecc-273">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="04ecc-274">Egy számla javítva a felszámítható mennyiség növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="04ecc-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="04ecc-275">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="04ecc-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="04ecc-276">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="04ecc-277">Mérföldkőhöz tartozó sztornózott értékesítés</span><span class="sxs-lookup"><span data-stu-id="04ecc-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="04ecc-278">A mérföldkő <strong>Számlázott</strong> állapotból <strong>Számlázásra készen áll</strong> állapotba kerül</span><span class="sxs-lookup"><span data-stu-id="04ecc-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="04ecc-279">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="04ecc-280">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="04ecc-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="04ecc-281">Nem alkalmazható</span><span class="sxs-lookup"><span data-stu-id="04ecc-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-282">Számlázott értékesítés</span><span class="sxs-lookup"><span data-stu-id="04ecc-282">Billed sales</span></span></td>
<td><span data-ttu-id="04ecc-283">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="04ecc-284">Egy számla javítva a felszámítható mennyiség csökkentéséhez.</span><span class="sxs-lookup"><span data-stu-id="04ecc-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="04ecc-285">Számlázott értékesítés – Sztornó</span><span class="sxs-lookup"><span data-stu-id="04ecc-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="04ecc-286">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-287">Számlázott értékesítés az új mennyiséghez</span><span class="sxs-lookup"><span data-stu-id="04ecc-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="04ecc-288">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ecc-289">Számlázatlan értékesítés – Az új mennyiségnél felszámítható</span><span class="sxs-lookup"><span data-stu-id="04ecc-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="04ecc-290">Projektszerződés pénzneme</span><span class="sxs-lookup"><span data-stu-id="04ecc-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
