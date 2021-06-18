---
title: Projektalapú helyesbítő számlák létrehozása
description: Ez témakör a Project Operations szolgáltatásban lévő helyesbítő számlákról nyújt információt.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0423fe9895b91431b2a83a8fff81118205b0736
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001620"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="f1716-103">Projektalapú helyesbítő számlák létrehozása</span><span class="sxs-lookup"><span data-stu-id="f1716-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="f1716-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="f1716-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f1716-105">A megerősített projekt számlát ki lehet javítani az ügyféllel és a projektmenedzserrel egyeztetett változtatások vagy jóváírások feldolgozásához.</span><span class="sxs-lookup"><span data-stu-id="f1716-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="f1716-106">Ha a visszaigazolt számlán szeretne módosításokat készíteni, nyissa meg a visszaigazolt számlát, és válassza a **Számla helyesbítése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f1716-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="f1716-107">Ez a beállítás csak akkor érhető el, ha a projektszámlát megerősítik.</span><span class="sxs-lookup"><span data-stu-id="f1716-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="f1716-108">Az új vázlat állapotú számlát a visszaigazolt számla alapján hozza létre a rendszer.</span><span class="sxs-lookup"><span data-stu-id="f1716-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="f1716-109">A rendszer a korábban visszaigazolt számla minden számlázási adatait átmásolja az új vázlatba.</span><span class="sxs-lookup"><span data-stu-id="f1716-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="f1716-110">Az alábbiakban néhány fontos szempontot talál, amelyek segítenek jobban megérteni az új helyesbített számla sorrészleteit:</span><span class="sxs-lookup"><span data-stu-id="f1716-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="f1716-111">Minden mennyiség nullára van frissítve.</span><span class="sxs-lookup"><span data-stu-id="f1716-111">All quantities are updated to zero.</span></span> <span data-ttu-id="f1716-112">Ez azt feltételezi, hogy az összes számlázott cikk teljes mértékben jóváírandó.</span><span class="sxs-lookup"><span data-stu-id="f1716-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="f1716-113">Ha szükséges, manuálisan frissítheti ezeket a mennyiségeket, hogy azok a számlázott mennyiséget tükrözzék, és nem a jóváírt mennyiséget.</span><span class="sxs-lookup"><span data-stu-id="f1716-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="f1716-114">A megadott mennyiség alapján az alkalmazás kiszámítja a jóváírt mennyiséget.</span><span class="sxs-lookup"><span data-stu-id="f1716-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="f1716-115">Ez az összeg jelenik meg a helyesbített számla megerősítését követően létrehozott tényadatokban.</span><span class="sxs-lookup"><span data-stu-id="f1716-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="f1716-116">Ha módosítja az adó összegét, akkor meg kell adnia a helyes adót, és nem a jóváírt adó összegét.</span><span class="sxs-lookup"><span data-stu-id="f1716-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="f1716-117">A mérföldkő-helyesbítéseket a rendszer mindig teljes jóváírásként dolgozza fel.</span><span class="sxs-lookup"><span data-stu-id="f1716-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="f1716-118">A foglaló vagy az előleg összegét korrigálni lehet, ha az ügyfél nem megfelelő összeget számlázott.</span><span class="sxs-lookup"><span data-stu-id="f1716-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="f1716-119">A foglalók és az előlegek egyeztetése korrigálható, ha nem megfelelő összeget használtak a díjak egyeztetésére egy előzőleg visszaigazolt számlán.</span><span class="sxs-lookup"><span data-stu-id="f1716-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f1716-120">Azon számlasor részleteknél, amelyek más, számlázott költségek helyesbítései, a **Helyesbítés** mező **Igen** értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="f1716-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="f1716-121">A helyesbített számlasor adatait tartalmazó számlákhoz egy **Helyesbítésekkel rendelkezik** mező is tartozik, amelynek értéke szintén **Igen**.</span><span class="sxs-lookup"><span data-stu-id="f1716-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="f1716-122">A helyesbítő számla megerősítésével létrehozott tényadatok</span><span class="sxs-lookup"><span data-stu-id="f1716-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="f1716-123">Az alábbi tábla azokat a tényadatokat sorolja fel, amelyek a helyesbítő számla visszaigazolásakor jönnek létre.</span><span class="sxs-lookup"><span data-stu-id="f1716-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="f1716-124">
                    <strong>Forgatókönyv</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f1716-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="f1716-125">
                    <strong>A jóváhagyáskor létrehozott tényleges adatok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f1716-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="f1716-126">A számlázott előleg vagy a foglaló korrekciójának megerősítése.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="f1716-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-127">A foglaló vagy előleg nem számlázott értékesítésének sztornírozása, ami egyeztetéshez lett létrehozva.</span><span class="sxs-lookup"><span data-stu-id="f1716-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="f1716-128">Ez az összeg pozitív, mert a foglaló vagy az előleg számlázásakor létrejött negatív értéket kell visszavonni.</span><span class="sxs-lookup"><span data-stu-id="f1716-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-129">A kiszámlázott értékesítési sztornírozás tényleges adata jön létre a foglaló vagy előleg összegéhez az eredeti számlázott értékesítés sztornírozásához.</span><span class="sxs-lookup"><span data-stu-id="f1716-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-130">A rendszer egy új számlázott értékesítési tényadatot hoz létre a foglaló vagy előleg helyesbített összegéhez a javított számlasoron.</span><span class="sxs-lookup"><span data-stu-id="f1716-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-131">A nem számlázott negatív mennyiségű tényleges értékesítés a foglalón vagy előlegen alapuló helyesbített számlasor, amelyet a rendszer az egyeztetéshez használni fog.</span><span class="sxs-lookup"><span data-stu-id="f1716-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="f1716-132">A korábban egyeztetett foglaló vagy előleg helyesbítésének megerősítése.</span><span class="sxs-lookup"><span data-stu-id="f1716-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-133">A foglaló vagy előleg nem számlázott értékesítésének sztornírozása, ami egyeztetéshez lett létrehozva.</span><span class="sxs-lookup"><span data-stu-id="f1716-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="f1716-134">Ez az összeg pozitív, és a foglaló vagy az előleg egyeztetésekor létrejött negatív értéket kell visszavonni.</span><span class="sxs-lookup"><span data-stu-id="f1716-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-135">A számlázott értékesítés tényleges sztornírozása az előző számla összegéhez.</span><span class="sxs-lookup"><span data-stu-id="f1716-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-136">A rendszer egy új számlázott tényleges értékesítést létre a foglaló helyesbített összegéhez, ami alkalmazva van a javított számlán.</span><span class="sxs-lookup"><span data-stu-id="f1716-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-137">A nem számlázott negatív mennyiségű tényleges értékesítés a foglaló vagy előleg javított maradékából, amelyet a rendszer az egyeztetéshez használni fog.</span><span class="sxs-lookup"><span data-stu-id="f1716-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f1716-138">Egy korábban számlázott időtranzakció teljes jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="f1716-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-139">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés összegének sztornírozása az idő esetében.</span><span class="sxs-lookup"><span data-stu-id="f1716-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-140">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés összegére vonatkozó új nem számlázott tényleges értékesítés az idő esetében.</span><span class="sxs-lookup"><span data-stu-id="f1716-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f1716-141">Egy részleges jóváírás számlázása egy időtranzakcióban.</span><span class="sxs-lookup"><span data-stu-id="f1716-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-142">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés összegének sztornírozása az idő esetében.</span><span class="sxs-lookup"><span data-stu-id="f1716-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-143">Az új, nem számlázott tényleges értékesítés, amely felszámítható az órákhoz és összeghez a szerkesztett számlasoradatokhoz, ennek helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="f1716-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-144">Egy új, nem számlázott tényleges értékesítés, amely a hátralévő órákra és az összegre felszámolható, a helyesbített értékek levonása után a számlasor részleteiben.</span><span class="sxs-lookup"><span data-stu-id="f1716-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f1716-145">Egy korábban számlázott költségtranzakció teljes jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="f1716-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-146">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének sztornírozása a kiadáshoz.</span><span class="sxs-lookup"><span data-stu-id="f1716-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-147">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének új nem számlázott tényleges értékesítése.</span><span class="sxs-lookup"><span data-stu-id="f1716-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f1716-148">Egy korábban számlázott költségtranzakció részleges jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="f1716-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-149">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének sztornírozása egy kiadáshoz.</span><span class="sxs-lookup"><span data-stu-id="f1716-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-150">Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a helyesbített számlasoradatokhoz, ennek helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="f1716-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-151">Egy új, nem számlázott tényleges értékesítés, amely a hátralévő mennyiségre és az összegre felszámolható, a helyesbített értékek levonása után a számlasor részleteiben.</span><span class="sxs-lookup"><span data-stu-id="f1716-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f1716-152">Egy korábban számlázott díjtranzakció teljes jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="f1716-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-153">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének sztornírozása a díjhoz.</span><span class="sxs-lookup"><span data-stu-id="f1716-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-154">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének díjának új nem számlázott tényleges értékesítése.</span><span class="sxs-lookup"><span data-stu-id="f1716-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f1716-155">Egy korábban számlázott díjtranzakció részleges jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="f1716-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-156">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének sztornírozása díjhoz.</span><span class="sxs-lookup"><span data-stu-id="f1716-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-157">Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a javított, helyesbítő számlasoradatokhoz, ennek helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="f1716-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f1716-158">Egy korábban számlázott mérföldkő teljes jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="f1716-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-159">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés összegének sztornírozása a mérföldkőhöz.</span><span class="sxs-lookup"><span data-stu-id="f1716-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="f1716-160">A mérföldkő számlaállapota a <b>Közzétett ügyfélszámla</b> értékről <b>Számlázásra kész</b> állapotra frissül.</span><span class="sxs-lookup"><span data-stu-id="f1716-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f1716-161">Egy korábban számlázott mérföldkő részleges jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="f1716-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f1716-162">Nem támogatott</span><span class="sxs-lookup"><span data-stu-id="f1716-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
