---
title: Helyesbített számlák - Lite
description: Ez a témakör a helyesbített számlák a Project Operations alkalmazásban való használatáról nyújt tájékoztatást
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb949ff3a53bcba19d44e1c3d6fe08a6b368108d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274236"
---
# <a name="corrected-invoices---lite"></a><span data-ttu-id="0f452-103">Helyesbített számlák - Lite</span><span class="sxs-lookup"><span data-stu-id="0f452-103">Corrected invoices - lite</span></span>

<span data-ttu-id="0f452-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="0f452-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0f452-105">A megerősített projekt számlát ki lehet javítani az ügyféllel és a projektmenedzserrel egyeztetett változtatások vagy jóváírások feldolgozásához.</span><span class="sxs-lookup"><span data-stu-id="0f452-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="0f452-106">Ha a visszaigazolt számlán szeretne módosításokat készíteni, nyissa meg a visszaigazolt számlát, és válassza a **Számla helyesbítése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="0f452-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="0f452-107">Ez a beállítás csak akkor érhető el, ha a projektszámlát megerősítik.</span><span class="sxs-lookup"><span data-stu-id="0f452-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="0f452-108">Az új vázlat állapotú számlát a visszaigazolt számla alapján hozza létre a rendszer.</span><span class="sxs-lookup"><span data-stu-id="0f452-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="0f452-109">A rendszer a korábban visszaigazolt számla minden számlázási adatait átmásolja az új vázlatba.</span><span class="sxs-lookup"><span data-stu-id="0f452-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="0f452-110">Az alábbiakban néhány olyan alapvető szempontot talál, amelyek fontosak az új helyesbített számla soradataival kapcsolatosan.</span><span class="sxs-lookup"><span data-stu-id="0f452-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="0f452-111">Minden mennyiség nullára van frissítve.</span><span class="sxs-lookup"><span data-stu-id="0f452-111">All quantities are updated to zero.</span></span> <span data-ttu-id="0f452-112">Az alkalmazás feltételezi, hogy a számlázott elemek teljes mértékben jóváírásra kerülnek.</span><span class="sxs-lookup"><span data-stu-id="0f452-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="0f452-113">Ha szükséges, manuálisan frissítheti ezeket a mennyiségeket, hogy azok a számlázott mennyiséget tükrözzék, és nem a jóváírt mennyiséget.</span><span class="sxs-lookup"><span data-stu-id="0f452-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="0f452-114">A megadott mennyiség alapján az alkalmazás kiszámítja a jóváírt mennyiséget.</span><span class="sxs-lookup"><span data-stu-id="0f452-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="0f452-115">Ez az összeg jelenik meg a helyesbített számla megerősítését követően létrehozott tényadatokban.</span><span class="sxs-lookup"><span data-stu-id="0f452-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="0f452-116">Ha módosítja az adó összegét, akkor meg kell adnia a helyes adót, és nem a jóváírt adó összegét.</span><span class="sxs-lookup"><span data-stu-id="0f452-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="0f452-117">A korábban megerősített termékalapú szerződéssorok nem lesznek átmásolva.</span><span class="sxs-lookup"><span data-stu-id="0f452-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="0f452-118">A terméken alapuló projektszámlán végzett helyesbítések feldolgozása nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="0f452-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="0f452-119">A mérföldkő-helyesbítéseket a rendszer mindig teljes jóváírásként dolgozza fel.</span><span class="sxs-lookup"><span data-stu-id="0f452-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="0f452-120">A foglaló vagy az előleg összegét korrigálni lehet, ha az ügyfél nem megfelelő összeget számlázott.</span><span class="sxs-lookup"><span data-stu-id="0f452-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="0f452-121">A foglalók és az előlegek egyeztetése korrigálható, ha nem megfelelő összeget használtak a díjak egyeztetésére egy előzőleg visszaigazolt számlán.</span><span class="sxs-lookup"><span data-stu-id="0f452-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f452-122">A számlasor részletei esetében, amelyek az egyéb már számlázott díjakra vonatkozóan korrekciók a **Helyesbítés** mező **Igen** értékre van beállítva.</span><span class="sxs-lookup"><span data-stu-id="0f452-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="0f452-123">A helyesbített számlasor adatait tartalmazó számlákhoz egy **Helyesbítésekkel rendelkezik** mező is tartozik, amelynek értéke szintén **Igen**.</span><span class="sxs-lookup"><span data-stu-id="0f452-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="0f452-124">A helyesbítő számla megerősítésével létrehozott tényadatok:</span><span class="sxs-lookup"><span data-stu-id="0f452-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="0f452-125">Az alábbiakban láthatók az alkalmazás által létrehozott tényleges adatok a helyesbítő számla tervezetének a jóváhagyást megelőzően elvégzett műveletei alapján.</span><span class="sxs-lookup"><span data-stu-id="0f452-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="0f452-126">
                    <strong>Forgatókönyv</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0f452-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="0f452-127">
                    <strong>A jóváhagyáskor létrehozott tényleges adatok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0f452-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="0f452-128">A számlázott előleg vagy a foglaló korrekciójának megerősítése.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="0f452-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-129">A foglaló vagy előleg nem számlázott értékesítésének sztornírozása, ami egyeztetéshez lett létrehozva.</span><span class="sxs-lookup"><span data-stu-id="0f452-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="0f452-130">Ez az összeg pozitív, mert a foglaló vagy az előleg számlázásakor létrejött negatív értéket kell visszavonni.</span><span class="sxs-lookup"><span data-stu-id="0f452-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-131">A kiszámlázott értékesítési sztornírozás tényleges adata jön létre a foglaló vagy előleg összegéhez az eredeti számlázott értékesítés sztornírozásához.</span><span class="sxs-lookup"><span data-stu-id="0f452-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-132">A rendszer egy új számlázott értékesítési tényadatot hoz létre a foglaló vagy előleg helyesbített összegéhez a javított számlasoron.</span><span class="sxs-lookup"><span data-stu-id="0f452-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-133">A nem számlázott negatív mennyiségű tényleges értékesítés a foglalón vagy előlegen alapuló helyesbített számlasor, amelyet a rendszer az egyeztetéshez használni fog.</span><span class="sxs-lookup"><span data-stu-id="0f452-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="0f452-134">A korábban egyeztetett foglaló vagy előleg helyesbítésének megerősítése.</span><span class="sxs-lookup"><span data-stu-id="0f452-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-135">A foglaló vagy előleg nem számlázott értékesítésének sztornírozása, ami egyeztetéshez lett létrehozva.</span><span class="sxs-lookup"><span data-stu-id="0f452-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="0f452-136">Ez az összeg pozitív, és a foglaló vagy az előleg egyeztetésekor létrejött negatív értéket kell visszavonni.</span><span class="sxs-lookup"><span data-stu-id="0f452-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-137">A számlázott értékesítés tényleges sztornírozása az előző számla összegéhez.</span><span class="sxs-lookup"><span data-stu-id="0f452-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-138">A rendszer egy új számlázott tényleges értékesítést létre a foglaló helyesbített összegéhez, ami alkalmazva van a javított számlán.</span><span class="sxs-lookup"><span data-stu-id="0f452-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-139">A nem számlázott negatív mennyiségű tényleges értékesítés a foglaló vagy előleg javított maradékából, amelyet a rendszer az egyeztetéshez használni fog.</span><span class="sxs-lookup"><span data-stu-id="0f452-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0f452-140">Egy korábban számlázott időtranzakció teljes jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="0f452-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-141">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés összegének sztornírozása az idő esetében.</span><span class="sxs-lookup"><span data-stu-id="0f452-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-142">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés összegére vonatkozó új nem számlázott tényleges értékesítés az idő esetében.</span><span class="sxs-lookup"><span data-stu-id="0f452-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0f452-143">Egy részleges jóváírás számlázása egy időtranzakcióban.</span><span class="sxs-lookup"><span data-stu-id="0f452-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-144">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés összegének sztornírozása az idő esetében.</span><span class="sxs-lookup"><span data-stu-id="0f452-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-145">Az új, nem számlázott tényleges értékesítés, amely felszámítható az órákhoz és összeghez a szerkesztett számlasoradatokhoz, ennek helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="0f452-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-146">Egy új, nem számlázott tényleges értékesítés, amely a hátralévő órákra és az összegre felszámolható, a helyesbített értékek levonása után a számlasor részleteiben.</span><span class="sxs-lookup"><span data-stu-id="0f452-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0f452-147">Egy korábban számlázott költségtranzakció teljes jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="0f452-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-148">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének sztornírozása a kiadáshoz.</span><span class="sxs-lookup"><span data-stu-id="0f452-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-149">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének új nem számlázott tényleges értékesítése.</span><span class="sxs-lookup"><span data-stu-id="0f452-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0f452-150">Egy korábban számlázott költségtranzakció részleges jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="0f452-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-151">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének sztornírozása egy kiadáshoz.</span><span class="sxs-lookup"><span data-stu-id="0f452-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-152">Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a helyesbített számlasoradatokhoz, ennek helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="0f452-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-153">Egy új, nem számlázott tényleges értékesítés, amely a hátralévő mennyiségre és az összegre felszámolható, a helyesbített értékek levonása után a számlasor részleteiben.</span><span class="sxs-lookup"><span data-stu-id="0f452-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0f452-154">Egy korábban számlázott díjtranzakció teljes jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="0f452-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-155">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének sztornírozása a díjhoz.</span><span class="sxs-lookup"><span data-stu-id="0f452-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-156">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének díjának új nem számlázott tényleges értékesítése.</span><span class="sxs-lookup"><span data-stu-id="0f452-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0f452-157">Egy korábban számlázott díjtranzakció részleges jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="0f452-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-158">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének sztornírozása díjhoz.</span><span class="sxs-lookup"><span data-stu-id="0f452-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-159">Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a javított, helyesbítő számlasoradatokhoz, ennek helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="0f452-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="0f452-160">Egy korábban számlázott mérföldkő teljes jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="0f452-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-161">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés összegének sztornírozása a mérföldkőhöz.</span><span class="sxs-lookup"><span data-stu-id="0f452-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="0f452-162">A projekt szerződéssor mezőjében a mérföldkőnek számla vagy számlázási állapot **Számlázásra kész** értékre frissül.</span><span class="sxs-lookup"><span data-stu-id="0f452-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="0f452-163">Egy korábban számlázott mérföldkő részleges jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="0f452-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-164">Nem támogatott</span><span class="sxs-lookup"><span data-stu-id="0f452-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="0f452-165">A korábban számlázott termék alapú szerződéssor jóváírásai és helyesbítései.</span><span class="sxs-lookup"><span data-stu-id="0f452-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0f452-166">Nem támogatott</span><span class="sxs-lookup"><span data-stu-id="0f452-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]