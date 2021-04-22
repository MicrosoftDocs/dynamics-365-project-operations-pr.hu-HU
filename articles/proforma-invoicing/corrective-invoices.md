---
title: Helyesbítő projektalapú számlák
description: Ez a témakör információt nyújt arról, hogyan hozhat létre és erősíthet meg helyesbítő projektalapú számlákat a Project Operations szolgáltatásban.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fc96bb40f5207efc381986d46a3e37dfc1dc111c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867044"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="9f99c-103">Helyesbítő projektalapú számlák</span><span class="sxs-lookup"><span data-stu-id="9f99c-103">Corrective project-based invoices</span></span>

<span data-ttu-id="9f99c-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="9f99c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9f99c-105">A megerősített projekt számlát ki lehet javítani az ügyféllel és a projektmenedzserrel egyeztetett változtatások vagy jóváírások feldolgozásához.</span><span class="sxs-lookup"><span data-stu-id="9f99c-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="9f99c-106">Ha a visszaigazolt számlán szeretne módosításokat készíteni, nyissa meg a visszaigazolt számlát, és válassza a **Számla helyesbítése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9f99c-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="9f99c-107">Ez a kiválasztás csak akkor érhető el, ha a projektszámlát megerősítik, vagy ha a projektalapú számlán előlegek vagy foglalók, illetve előlegek vagy foglalók egyeztetése található.</span><span class="sxs-lookup"><span data-stu-id="9f99c-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="9f99c-108">Az új vázlat állapotú számlát a visszaigazolt számla alapján hozza létre a rendszer.</span><span class="sxs-lookup"><span data-stu-id="9f99c-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="9f99c-109">A rendszer a korábban visszaigazolt számla minden számlázási adatait átmásolja az új vázlatba.</span><span class="sxs-lookup"><span data-stu-id="9f99c-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="9f99c-110">Az alábbiakban néhány olyan alapvető szempontot talál, amelyek fontosak az új helyesbített számla soradataival kapcsolatosan.</span><span class="sxs-lookup"><span data-stu-id="9f99c-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="9f99c-111">Minden mennyiség nullára van frissítve.</span><span class="sxs-lookup"><span data-stu-id="9f99c-111">All quantities are updated to zero.</span></span> <span data-ttu-id="9f99c-112">A Dynamics 365 Project Operations azt feltételezi, hogy az összes számlázott cikk teljes mértékben jóváírandó.</span><span class="sxs-lookup"><span data-stu-id="9f99c-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="9f99c-113">Ha szükséges, manuálisan frissítheti ezeket a mennyiségeket, hogy azok a számlázott mennyiséget tükrözzék, és nem a jóváírt mennyiséget.</span><span class="sxs-lookup"><span data-stu-id="9f99c-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="9f99c-114">A megadott mennyiség alapján az alkalmazás kiszámítja a jóváírt mennyiséget.</span><span class="sxs-lookup"><span data-stu-id="9f99c-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="9f99c-115">Ez az összeg jelenik meg a helyesbített számla megerősítését követően létrehozott tényadatokban.</span><span class="sxs-lookup"><span data-stu-id="9f99c-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="9f99c-116">Ha módosítja az adó összegét, akkor meg kell adnia a helyes adót, és nem a jóváírt adó összegét.</span><span class="sxs-lookup"><span data-stu-id="9f99c-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="9f99c-117">A mérföldkő-helyesbítéseket a rendszer mindig teljes jóváírásként dolgozza fel.</span><span class="sxs-lookup"><span data-stu-id="9f99c-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="9f99c-118">Azoknál a számlasor részleteknél, amelyek már más, számlázott költségek helyesbítései, a **Helyesbítés** mező **Igen** értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="9f99c-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="9f99c-119">Azoknál a számláknál, amelyek helyesbített számlasor részletekkel rendelkeznek, a **Helyesbített** mező **Igen** értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="9f99c-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="9f99c-120">Helyesbítő számla visszaigazolásakor létrehozott tényadatok</span><span class="sxs-lookup"><span data-stu-id="9f99c-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="9f99c-121">Az alábbi tábla azokat a tényadatokat sorolja fel, amelyek a helyesbítő számla visszaigazolásakor jönnek létre.</span><span class="sxs-lookup"><span data-stu-id="9f99c-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="9f99c-122">
                    <strong>Forgatókönyv</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f99c-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="9f99c-123">
                    <strong>A jóváhagyáskor létrehozott tényleges adatok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f99c-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9f99c-124">Egy korábban számlázott időtranzakció teljes jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="9f99c-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-125">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés összegének sztornírozása az idő esetében.</span><span class="sxs-lookup"><span data-stu-id="9f99c-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-126">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés összegére vonatkozó új nem számlázott tényleges értékesítés az idő esetében.</span><span class="sxs-lookup"><span data-stu-id="9f99c-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9f99c-127">Egy részleges jóváírás számlázása egy időtranzakcióban.</span><span class="sxs-lookup"><span data-stu-id="9f99c-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-128">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés összegének sztornírozása az idő esetében.</span><span class="sxs-lookup"><span data-stu-id="9f99c-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-129">Az új, nem számlázott tényleges értékesítés, amely felszámítható az órákhoz és összeghez a szerkesztett számlasoradatokhoz, ennek helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="9f99c-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-130">Egy új, nem számlázott tényleges értékesítés, amely a hátralévő órákra és az összegre felszámolható, a helyesbített értékek levonása után a számlasor részleteiben.</span><span class="sxs-lookup"><span data-stu-id="9f99c-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9f99c-131">Egy korábban számlázott költségtranzakció teljes jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="9f99c-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-132">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének sztornírozása a kiadáshoz.</span><span class="sxs-lookup"><span data-stu-id="9f99c-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-133">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének új nem számlázott tényleges értékesítése.</span><span class="sxs-lookup"><span data-stu-id="9f99c-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9f99c-134">Egy korábban számlázott költségtranzakció részleges jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="9f99c-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-135">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének sztornírozása egy kiadáshoz.</span><span class="sxs-lookup"><span data-stu-id="9f99c-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-136">Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a helyesbített számlasoradatokhoz, ennek helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="9f99c-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-137">Egy új, nem számlázott tényleges értékesítés, amely a hátralévő mennyiségre és az összegre felszámolható, a helyesbített értékek levonása után a számlasor részleteiben.</span><span class="sxs-lookup"><span data-stu-id="9f99c-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9f99c-138">Korábban számlázott anyagtranzakció teljes jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="9f99c-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-139">A mennyiség és az összeg számlázott értékesítési sztornírozása az anyag eredeti számlasorának részletein.</span><span class="sxs-lookup"><span data-stu-id="9f99c-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-140">Az mennyiség és az összeg új számlázatlan értékesítési tényadata az anyag eredeti számlasorának részletein.</span><span class="sxs-lookup"><span data-stu-id="9f99c-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9f99c-141">Anyagtranzakció részleges jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="9f99c-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-142">A számlázott mennyiség és az összeg számlázott értékesítési sztornírozása az anyag eredeti számlasorának részletein.</span><span class="sxs-lookup"><span data-stu-id="9f99c-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-143">Egy új, nem számlázott értékesítési tényadat – amely felszámítható a szerkesztett számlasor részleteiben lévő mennyiségért és összegért – sztornírozása és ezzel egyenértékű számlázott értékesítési tényadata.</span><span class="sxs-lookup"><span data-stu-id="9f99c-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-144">Egy új, nem számlázott tényleges értékesítés, amely a hátralévő mennyiségre és az összegre felszámolható, a helyesbített értékek levonása után a számlasor részleteiben.</span><span class="sxs-lookup"><span data-stu-id="9f99c-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9f99c-145">Egy korábban számlázott díjtranzakció teljes jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="9f99c-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-146">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének sztornírozása a díjhoz.</span><span class="sxs-lookup"><span data-stu-id="9f99c-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-147">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének díjának új nem számlázott tényleges értékesítése.</span><span class="sxs-lookup"><span data-stu-id="9f99c-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9f99c-148">Egy korábban számlázott díjtranzakció részleges jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="9f99c-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-149">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének sztornírozása díjhoz.</span><span class="sxs-lookup"><span data-stu-id="9f99c-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-150">Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a javított, helyesbítő számlasoradatokhoz, ennek helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="9f99c-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9f99c-151">Egy korábban számlázott mérföldkő teljes jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="9f99c-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-152">Az eredeti számlasor részleteire vonatkozó számlázott értékesítés összegének sztornírozása a mérföldkőhöz.</span><span class="sxs-lookup"><span data-stu-id="9f99c-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="9f99c-153">A mérföldkő számlaállapota a <b>Közzétett ügyfélszámla</b> értékről <b>Számlázásra kész</b> állapotra frissül.</span><span class="sxs-lookup"><span data-stu-id="9f99c-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9f99c-154">Egy korábban számlázott mérföldkő részleges jóváírásának számlázása.</span><span class="sxs-lookup"><span data-stu-id="9f99c-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9f99c-155">Ez a forgatókönyv nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="9f99c-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
