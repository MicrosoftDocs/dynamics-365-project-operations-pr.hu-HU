---
title: Proforma számla jóváhagyása
description: Ez a témakör a proforma számlák a Project Operations alkalmazásban való megerősítéséről nyújt tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4b67ee6848efdcb85cf732c1eaa3e40cdc51a2e2
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078000"
---
# <a name="confirming-a-proforma-invoice"></a><span data-ttu-id="8e0e0-103">Proforma számla jóváhagyása</span><span class="sxs-lookup"><span data-stu-id="8e0e0-103">Confirming a proforma invoice</span></span>

<span data-ttu-id="8e0e0-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="8e0e0-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="8e0e0-105">A proforma számla megerősítését követően a projektszámla- frissítések állapota **Megerősítve** lesz.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="8e0e0-106">A számla megerősítését követően csak olvasható lesz.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="8e0e0-107">Ezután a számla csak akkor helyesbíthető, ha ügyfél által kezdeményezett helyesbítések vagy jóváírások vannak, vagy ha a számla kifizetettként van megjelölve.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="8e0e0-108">A következő táblázat a rendszer által létrehozott tényleges adatokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="8e0e0-109">A rendszer ezeket a tényleges adatokat akkor hozza létre, amikor bizonyos műveleteket végrehajtanak a projekt vázlat állapotú számláján a jóváhagyás előtt.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="8e0e0-110">
                    <strong>Forgatókönyv</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e0e0-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="8e0e0-111">
                    <strong>A jóváhagyáskor létrehozott tényleges adatok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e0e0-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8e0e0-112">Foglaló vagy előleg számlázása</span><span class="sxs-lookup"><span data-stu-id="8e0e0-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-113">A <strong>Foglaló</strong> típusú számlázott tényleges értékesítés az előleg vagy a foglaló összegéhez van létrehozva.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-114">A nem számlázott negatív mennyiségű tényleges értékesítés a foglaló, amelyet a rendszer az egyeztetéshez használni fog.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8e0e0-115">Egy foglaló vagy előleg teljes körű egyeztetése után a számlán.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-116">A foglaló vagy előleg nem számlázott értékesítésének sztornírozása, ami egyeztetéshez lett létrehozva.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="8e0e0-117">Ez az összeg pozitív, mert a foglaló vagy az előleg számlázásakor létrejött negatív értéket kell kiegyenlítenie.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-118">Egy számlázott tényleges értékesítés ezen számla összegéhez.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="8e0e0-119">Egy foglaló vagy előleg részleges egyeztetése után a számlán.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-120">A foglaló vagy előleg nem számlázott értékesítésének sztornírozása, ami egyeztetéshez lett létrehozva.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="8e0e0-121">Ez az összeg pozitív, mert a foglaló vagy az előleg számlázásakor létrejött negatív értéket kell kiegyenlítenie.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-122">Egy számlázott tényleges értékesítés ezen számla összegéhez.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-123">A nem számlázott negatív tényleges értékesítés a fennmaradó foglaló vagy előleg összegéhez, amelyet a rendszer az egyeztetéshez fog használni a későbbi számlákon.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8e0e0-124">Az időtranzakciók számlázása szerkesztés nélkül vázlat állapotú számlára.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-125">Nem számlázott értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-126">Számlázott tényleges értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="8e0e0-127">A mennyiség csökkentéséhez módosított időtranzakció számlázása.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-128">Nem számlázott értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-129">Az új, nem számlázott tényleges értékesítés, amely felszámítható az órákhoz és összeghez a szerkesztett számlasoradatokhoz, a tényleges értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-130">Az új, nem számlázott tényleges értékesítés, amely nem felszámítható a fennmaradó órákhoz a javított értékek levonását követően és összeghez a szerkesztett számlasoradatokhoz, a tényleges értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8e0e0-131">A mennyiség növeléséhez módosított időtranzakció számlázása.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-132">Nem számlázott értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-133">Az új, nem számlázott tényleges értékesítés, amely felszámítható az órákhoz és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8e0e0-134">Az költségtranzakciók számlázása szerkesztés nélkül vázlat állapotú számlára.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-135">Nem számlázott értékesítés mennyiségének és összegének sztornírozása az eredeti költségjóváhagyásra.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-136">Számlázott tényleges értékesítés mennyiségéhez és összegéhez az eredeti költségjóváhagyásra</span><span class="sxs-lookup"><span data-stu-id="8e0e0-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="8e0e0-137">A mennyiség csökkentéséhez módosított költségtranzakció számlázása.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-138">Nem számlázott értékesítés mennyiségének és összegének sztornírozása az eredeti költségjóváhagyásra.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-139">Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-140">Az új, nem számlázott tényleges értékesítés, amely nem felszámítható a fennmaradó mennyiséghez a javított értékek levonását követően és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8e0e0-141">A mennyiség növeléséhez módosított költségtranzakció számlázása.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-142">Nem számlázott értékesítés mennyiségének és összegének sztornírozása az eredeti költségjóváhagyásra.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-143">Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott tényleges értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8e0e0-144">Díj számlázása.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-145">Nem számlázott értékesítés díjösszegének sztornírozása az naplósoron.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-146">Számlázott tényleges értékesítés mennyiségéhez és összegéhez az eredeti díj naplósorán.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="8e0e0-147">Mérföldkő számlázása.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-148">Számlázott tényleges értesítés a projektszerződés eredeti mérföldkövén a mérföldkő mennyiségéhez.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="8e0e0-149">Termékalapú szerződéssor számlázása.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8e0e0-150">A terméksorhoz tartozó számlázott értékesítés, a termék alapú szerződéssorból származó mennyiséggel és összeggel.</span><span class="sxs-lookup"><span data-stu-id="8e0e0-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
