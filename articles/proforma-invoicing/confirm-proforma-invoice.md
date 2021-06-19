---
title: Projektalapú proforma számla megerősítése
description: Ez témakör a proforma projektalapú számlák megerősítéséről nyújt információt.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1e4591d97e9d895dade42b2bcce57f22208cba96
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012139"
---
# <a name="confirm-a-proforma-project-based-invoice"></a><span data-ttu-id="3e953-103">Projektalapú proforma számla megerősítése</span><span class="sxs-lookup"><span data-stu-id="3e953-103">Confirm a proforma project-based invoice</span></span>

<span data-ttu-id="3e953-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="3e953-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3e953-105">A proforma számla megerősítését követően a projektszámla- frissítések állapota **Megerősítve** lesz.</span><span class="sxs-lookup"><span data-stu-id="3e953-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="3e953-106">A számla megerősítését követően csak olvasható lesz.</span><span class="sxs-lookup"><span data-stu-id="3e953-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="3e953-107">A jövőben a számla csak akkor helyesbíthető, ha vannak ügyfél által kezdeményezett helyesbítések vagy jóváírások.</span><span class="sxs-lookup"><span data-stu-id="3e953-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="3e953-108">A következő táblázat a rendszer által létrehozott tényleges adatokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="3e953-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="3e953-109">A rendszer ezeket a tényleges adatokat akkor hozza létre, amikor bizonyos műveleteket végrehajtanak a projekt vázlat állapotú számláján a jóváhagyás előtt.</span><span class="sxs-lookup"><span data-stu-id="3e953-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="3e953-110">
                    <strong>Forgatókönyv</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3e953-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="3e953-111">
                    <strong>A jóváhagyáskor létrehozott tényleges adatok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3e953-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3e953-112">Foglaló vagy előleg számlázása</span><span class="sxs-lookup"><span data-stu-id="3e953-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-113">A <strong>Foglaló</strong> típusú számlázott tényleges értékesítés az előleg vagy a foglaló összegéhez van létrehozva.</span><span class="sxs-lookup"><span data-stu-id="3e953-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-114">Azokat a nem számlázható értékesítési tényadatokat, amelyek negatív összegű foglalóval vagy előleggel rendelkeznek, egyeztetéshez kell használni.</span><span class="sxs-lookup"><span data-stu-id="3e953-114">An unbilled sales actual with a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3e953-115">Egy foglaló vagy előleg teljes körű egyeztetése után a számlán.</span><span class="sxs-lookup"><span data-stu-id="3e953-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-116">A foglaló vagy előleg nem számlázott értékesítésének sztornírozása, ami egyeztetéshez lett létrehozva.</span><span class="sxs-lookup"><span data-stu-id="3e953-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="3e953-117">Ez az összeg pozitív, mert a foglaló vagy az előleg számlázásakor létrejött negatív értéket kell kiegyenlítenie.</span><span class="sxs-lookup"><span data-stu-id="3e953-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-118">Egy számlázott tényleges értékesítés ezen számla összegéhez.</span><span class="sxs-lookup"><span data-stu-id="3e953-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="3e953-119">Egy foglaló vagy előleg részleges egyeztetése után a számlán.</span><span class="sxs-lookup"><span data-stu-id="3e953-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-120">A foglaló vagy előleg nem számlázott értékesítésének sztornírozása, ami egyeztetéshez lett létrehozva.</span><span class="sxs-lookup"><span data-stu-id="3e953-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="3e953-121">Ez az összeg pozitív, mert a foglaló vagy az előleg számlázásakor létrejött negatív értéket kell kiegyenlítenie.</span><span class="sxs-lookup"><span data-stu-id="3e953-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-122">Egy számlázott tényleges értékesítés ezen számla összegéhez.</span><span class="sxs-lookup"><span data-stu-id="3e953-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-123">A nem számlázott negatív tényleges értékesítés a fennmaradó foglaló vagy előleg összegéhez, amelyet a rendszer az egyeztetéshez fog használni a későbbi számlákon.</span><span class="sxs-lookup"><span data-stu-id="3e953-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3e953-124">Az időtranzakciók számlázása szerkesztés nélkül vázlat állapotú számlára.</span><span class="sxs-lookup"><span data-stu-id="3e953-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-125">Nem számlázott értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.</span><span class="sxs-lookup"><span data-stu-id="3e953-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-126">Számlázott tényleges értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.</span><span class="sxs-lookup"><span data-stu-id="3e953-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="3e953-127">A mennyiség csökkentéséhez módosított időtranzakció számlázása.</span><span class="sxs-lookup"><span data-stu-id="3e953-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-128">Nem számlázott értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.</span><span class="sxs-lookup"><span data-stu-id="3e953-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-129">Az új, nem számlázott tényleges értékesítés, amely felszámítható az órákhoz és összeghez a szerkesztett számlasoradatokhoz, a tényleges értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="3e953-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-130">Egy új, nem számlázott értékesítési tényadat nem számítható fel a hátralévő órákra és összegre, miután levonta a helyesbített összegeket a szerkesztett számlasor részleteiből, az értékesítés tényleges sztornírozásából és az azzal egyenértékű számlázott értékesítésből.</span><span class="sxs-lookup"><span data-stu-id="3e953-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3e953-131">A mennyiség növeléséhez módosított időtranzakció számlázása.</span><span class="sxs-lookup"><span data-stu-id="3e953-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-132">Nem számlázott értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.</span><span class="sxs-lookup"><span data-stu-id="3e953-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-133">Az új, nem számlázott tényleges értékesítés, amely felszámítható az órákhoz és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="3e953-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3e953-134">Az költségtranzakciók számlázása szerkesztés nélkül vázlat állapotú számlára.</span><span class="sxs-lookup"><span data-stu-id="3e953-134">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-135">Nem számlázott értékesítés mennyiségének és összegének sztornírozása az eredeti költségjóváhagyásra.</span><span class="sxs-lookup"><span data-stu-id="3e953-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-136">Számlázott tényleges értékesítés mennyiségéhez és összegéhez az eredeti költségjóváhagyásra.</span><span class="sxs-lookup"><span data-stu-id="3e953-136">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="3e953-137">A mennyiség csökkentéséhez módosított költségtranzakció számlázása.</span><span class="sxs-lookup"><span data-stu-id="3e953-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-138">Nem számlázott értékesítés mennyiségének és összegének sztornírozása az eredeti költségjóváhagyásra.</span><span class="sxs-lookup"><span data-stu-id="3e953-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-139">Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="3e953-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-140">Az új, nem számlázott tényleges értékesítés, amely nem felszámítható a fennmaradó mennyiséghez a javított értékek levonását követően és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="3e953-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3e953-141">A mennyiség növeléséhez módosított költségtranzakció számlázása.</span><span class="sxs-lookup"><span data-stu-id="3e953-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-142">Nem számlázott értékesítés mennyiségének és összegének sztornírozása az eredeti költségjóváhagyásra.</span><span class="sxs-lookup"><span data-stu-id="3e953-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-143">Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott tényleges értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="3e953-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3e953-144">Anyagtranzakció számlázása a számlatervezet szerkesztése nélkül.</span><span class="sxs-lookup"><span data-stu-id="3e953-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-145">A mennyiség és az összeg nem számlázott értékesítési sztornírozása az eredeti anyaghasználati jóváhagyáson.</span><span class="sxs-lookup"><span data-stu-id="3e953-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-146">A mennyiség és az összeg számlázott értékesítési tényadat az eredeti anyaghasználati jóváhagyáson.</span><span class="sxs-lookup"><span data-stu-id="3e953-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="3e953-147">A mennyiség csökkentése érdekében szerkesztett anyagtranzakció számlázása.</span><span class="sxs-lookup"><span data-stu-id="3e953-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-148">A mennyiség és az összeg nem számlázott értékesítési sztornírozása az eredeti időjóváhagyáson.</span><span class="sxs-lookup"><span data-stu-id="3e953-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-149">Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="3e953-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-150">Az új, nem számlázott tényleges értékesítés, amely nem felszámítható a fennmaradó mennyiséghez a javított értékek levonását követően és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="3e953-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3e953-151">A mennyiség növelése érdekében szerkesztett anyagtranzakció számlázása.</span><span class="sxs-lookup"><span data-stu-id="3e953-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-152">A mennyiség és az összeg nem számlázott értékesítési sztornírozása az eredeti anyaghasználati jóváhagyáson.</span><span class="sxs-lookup"><span data-stu-id="3e953-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-153">Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="3e953-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3e953-154">Díj számlázása.</span><span class="sxs-lookup"><span data-stu-id="3e953-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-155">Nem számlázott értékesítés díjösszegének sztornírozása az naplósoron.</span><span class="sxs-lookup"><span data-stu-id="3e953-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-156">Számlázott tényleges értékesítés mennyiségéhez és összegéhez az eredeti díj naplósorán.</span><span class="sxs-lookup"><span data-stu-id="3e953-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="3e953-157">Mérföldkő számlázása.</span><span class="sxs-lookup"><span data-stu-id="3e953-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3e953-158">Számlázott tényleges értesítés a projektszerződés eredeti mérföldkövén a mérföldkő mennyiségéhez.</span><span class="sxs-lookup"><span data-stu-id="3e953-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
