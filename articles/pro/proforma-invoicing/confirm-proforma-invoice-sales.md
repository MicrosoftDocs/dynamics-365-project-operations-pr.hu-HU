---
title: Proforma számla megerősítése – Lite
description: Ez a témakör a proforma számlák a Project Operations alkalmazásban való megerősítéséről nyújt tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3b1818f20a0d54848939b689f87986154943c57a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274281"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="33bb6-103">Proforma számla megerősítése – Lite</span><span class="sxs-lookup"><span data-stu-id="33bb6-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="33bb6-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="33bb6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="33bb6-105">A proforma számla megerősítését követően a projektszámla- frissítések állapota **Megerősítve** lesz.</span><span class="sxs-lookup"><span data-stu-id="33bb6-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="33bb6-106">A számla megerősítését követően csak olvasható lesz.</span><span class="sxs-lookup"><span data-stu-id="33bb6-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="33bb6-107">Ezután a számla csak akkor helyesbíthető, ha ügyfél által kezdeményezett helyesbítések vagy jóváírások vannak, vagy ha a számla kifizetettként van megjelölve.</span><span class="sxs-lookup"><span data-stu-id="33bb6-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="33bb6-108">A következő táblázat a rendszer által létrehozott tényleges adatokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="33bb6-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="33bb6-109">A rendszer ezeket a tényleges adatokat akkor hozza létre, amikor bizonyos műveleteket végrehajtanak a projekt vázlat állapotú számláján a jóváhagyás előtt.</span><span class="sxs-lookup"><span data-stu-id="33bb6-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="33bb6-110">
                    <strong>Forgatókönyv</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33bb6-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="33bb6-111">
                    <strong>A jóváhagyáskor létrehozott tényleges adatok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33bb6-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="33bb6-112">Foglaló vagy előleg számlázása</span><span class="sxs-lookup"><span data-stu-id="33bb6-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-113">A <strong>Foglaló</strong> típusú számlázott tényleges értékesítés az előleg vagy a foglaló összegéhez van létrehozva.</span><span class="sxs-lookup"><span data-stu-id="33bb6-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-114">A nem számlázott negatív mennyiségű tényleges értékesítés a foglaló, amelyet a rendszer az egyeztetéshez használni fog.</span><span class="sxs-lookup"><span data-stu-id="33bb6-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="33bb6-115">Egy foglaló vagy előleg teljes körű egyeztetése után a számlán.</span><span class="sxs-lookup"><span data-stu-id="33bb6-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-116">A foglaló vagy előleg nem számlázott értékesítésének sztornírozása, ami egyeztetéshez lett létrehozva.</span><span class="sxs-lookup"><span data-stu-id="33bb6-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="33bb6-117">Ez az összeg pozitív, mert a foglaló vagy az előleg számlázásakor létrejött negatív értéket kell kiegyenlítenie.</span><span class="sxs-lookup"><span data-stu-id="33bb6-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-118">Egy számlázott tényleges értékesítés ezen számla összegéhez.</span><span class="sxs-lookup"><span data-stu-id="33bb6-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="33bb6-119">Egy foglaló vagy előleg részleges egyeztetése után a számlán.</span><span class="sxs-lookup"><span data-stu-id="33bb6-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-120">A foglaló vagy előleg nem számlázott értékesítésének sztornírozása, ami egyeztetéshez lett létrehozva.</span><span class="sxs-lookup"><span data-stu-id="33bb6-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="33bb6-121">Ez az összeg pozitív, mert a foglaló vagy az előleg számlázásakor létrejött negatív értéket kell kiegyenlítenie.</span><span class="sxs-lookup"><span data-stu-id="33bb6-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-122">Egy számlázott tényleges értékesítés ezen számla összegéhez.</span><span class="sxs-lookup"><span data-stu-id="33bb6-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-123">A nem számlázott negatív tényleges értékesítés a fennmaradó foglaló vagy előleg összegéhez, amelyet a rendszer az egyeztetéshez fog használni a későbbi számlákon.</span><span class="sxs-lookup"><span data-stu-id="33bb6-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="33bb6-124">Az időtranzakciók számlázása szerkesztés nélkül vázlat állapotú számlára.</span><span class="sxs-lookup"><span data-stu-id="33bb6-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-125">Nem számlázott értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.</span><span class="sxs-lookup"><span data-stu-id="33bb6-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-126">Számlázott tényleges értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.</span><span class="sxs-lookup"><span data-stu-id="33bb6-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="33bb6-127">A mennyiség csökkentéséhez módosított időtranzakció számlázása.</span><span class="sxs-lookup"><span data-stu-id="33bb6-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-128">Nem számlázott értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.</span><span class="sxs-lookup"><span data-stu-id="33bb6-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-129">Az új, nem számlázott tényleges értékesítés, amely felszámítható az órákhoz és összeghez a szerkesztett számlasoradatokhoz, a tényleges értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="33bb6-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-130">Az új, nem számlázott tényleges értékesítés, amely nem felszámítható a fennmaradó órákhoz a javított értékek levonását követően és összeghez a szerkesztett számlasoradatokhoz, a tényleges értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="33bb6-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="33bb6-131">A mennyiség növeléséhez módosított időtranzakció számlázása.</span><span class="sxs-lookup"><span data-stu-id="33bb6-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-132">Nem számlázott értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.</span><span class="sxs-lookup"><span data-stu-id="33bb6-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-133">Az új, nem számlázott tényleges értékesítés, amely felszámítható az órákhoz és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="33bb6-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="33bb6-134">Az költségtranzakciók számlázása szerkesztés nélkül vázlat állapotú számlára.</span><span class="sxs-lookup"><span data-stu-id="33bb6-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-135">Nem számlázott értékesítés mennyiségének és összegének sztornírozása az eredeti költségjóváhagyásra.</span><span class="sxs-lookup"><span data-stu-id="33bb6-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-136">Számlázott tényleges értékesítés mennyiségéhez és összegéhez az eredeti költségjóváhagyásra</span><span class="sxs-lookup"><span data-stu-id="33bb6-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="33bb6-137">A mennyiség csökkentéséhez módosított költségtranzakció számlázása.</span><span class="sxs-lookup"><span data-stu-id="33bb6-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-138">Nem számlázott értékesítés mennyiségének és összegének sztornírozása az eredeti költségjóváhagyásra.</span><span class="sxs-lookup"><span data-stu-id="33bb6-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-139">Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="33bb6-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-140">Az új, nem számlázott tényleges értékesítés, amely nem felszámítható a fennmaradó mennyiséghez a javított értékek levonását követően és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="33bb6-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="33bb6-141">A mennyiség növeléséhez módosított költségtranzakció számlázása.</span><span class="sxs-lookup"><span data-stu-id="33bb6-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-142">Nem számlázott értékesítés mennyiségének és összegének sztornírozása az eredeti költségjóváhagyásra.</span><span class="sxs-lookup"><span data-stu-id="33bb6-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-143">Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott tényleges értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="33bb6-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="33bb6-144">Díj számlázása.</span><span class="sxs-lookup"><span data-stu-id="33bb6-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-145">Nem számlázott értékesítés díjösszegének sztornírozása az naplósoron.</span><span class="sxs-lookup"><span data-stu-id="33bb6-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-146">Számlázott tényleges értékesítés mennyiségéhez és összegéhez az eredeti díj naplósorán.</span><span class="sxs-lookup"><span data-stu-id="33bb6-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="33bb6-147">Mérföldkő számlázása.</span><span class="sxs-lookup"><span data-stu-id="33bb6-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-148">Számlázott tényleges értesítés a projektszerződés eredeti mérföldkövén a mérföldkő mennyiségéhez.</span><span class="sxs-lookup"><span data-stu-id="33bb6-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="33bb6-149">Termékalapú szerződéssor számlázása.</span><span class="sxs-lookup"><span data-stu-id="33bb6-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="33bb6-150">A terméksorhoz tartozó számlázott értékesítés, a termék alapú szerződéssorból származó mennyiséggel és összeggel.</span><span class="sxs-lookup"><span data-stu-id="33bb6-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]