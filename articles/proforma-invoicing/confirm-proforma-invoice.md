---
title: Proforma számla megerősítése
description: Ez a témakör a proforma számlák jóváhagyását ismerteti.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128106"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="0adaa-103">Proforma számla megerősítése</span><span class="sxs-lookup"><span data-stu-id="0adaa-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="0adaa-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="0adaa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0adaa-105">A proforma számla megerősítését követően a projektszámla- frissítések állapota **Megerősítve** lesz.</span><span class="sxs-lookup"><span data-stu-id="0adaa-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="0adaa-106">A számla megerősítését követően csak olvasható lesz.</span><span class="sxs-lookup"><span data-stu-id="0adaa-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="0adaa-107">Ezután a számla csak akkor helyesbíthető, ha ügyfél által kezdeményezett helyesbítések vagy jóváírások vannak, vagy ha kifizetettként van megjelölve.</span><span class="sxs-lookup"><span data-stu-id="0adaa-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="0adaa-108">A következő táblázat a rendszer által létrehozott tényleges adatokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="0adaa-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="0adaa-109">A rendszer ezeket a tényleges adatokat akkor hozza létre, amikor bizonyos műveleteket végrehajtanak a projekt vázlat állapotú számláján a jóváhagyás előtt.</span><span class="sxs-lookup"><span data-stu-id="0adaa-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="0adaa-110">
                    <strong>Forgatókönyv</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0adaa-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="0adaa-111">
                    <strong>A jóváhagyáskor létrehozott tényleges adatok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0adaa-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0adaa-112">Az időtranzakciók számlázása szerkesztés nélkül vázlat állapotú számlára.</span><span class="sxs-lookup"><span data-stu-id="0adaa-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0adaa-113">Nem számlázott értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.</span><span class="sxs-lookup"><span data-stu-id="0adaa-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0adaa-114">Számlázott tényleges értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.</span><span class="sxs-lookup"><span data-stu-id="0adaa-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0adaa-115">A mennyiség csökkentéséhez módosított időtranzakció számlázása.</span><span class="sxs-lookup"><span data-stu-id="0adaa-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0adaa-116">Nem számlázott értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.</span><span class="sxs-lookup"><span data-stu-id="0adaa-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0adaa-117">Az új, nem számlázott tényleges értékesítés, amely felszámítható az órákhoz és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="0adaa-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0adaa-118">Az új, nem számlázott tényleges értékesítés, amely nem felszámítható a fennmaradó órákhoz a javított értékek levonását követően és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="0adaa-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0adaa-119">A mennyiség növeléséhez módosított időtranzakció számlázása.</span><span class="sxs-lookup"><span data-stu-id="0adaa-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0adaa-120">Nem számlázott értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.</span><span class="sxs-lookup"><span data-stu-id="0adaa-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0adaa-121">Az új, nem számlázott tényleges értékesítés, amely felszámítható az órákhoz és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="0adaa-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0adaa-122">Az költségtranzakciók számlázása szerkesztés nélkül vázlat állapotú számlára.</span><span class="sxs-lookup"><span data-stu-id="0adaa-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0adaa-123">Nem számlázott értékesítés mennyiségének és összegének sztornírozása az eredeti költségjóváhagyásra.</span><span class="sxs-lookup"><span data-stu-id="0adaa-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0adaa-124">Számlázott tényleges értékesítés mennyiségéhez és összegéhez az eredeti költségjóváhagyásra.</span><span class="sxs-lookup"><span data-stu-id="0adaa-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0adaa-125">A mennyiség csökkentéséhez módosított költségtranzakció számlázása.</span><span class="sxs-lookup"><span data-stu-id="0adaa-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0adaa-126">Nem számlázott értékesítés mennyiségének és összegének sztornírozása az eredeti költségjóváhagyásra.</span><span class="sxs-lookup"><span data-stu-id="0adaa-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0adaa-127">Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="0adaa-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0adaa-128">Az új, nem számlázott tényleges értékesítés, amely nem felszámítható a fennmaradó mennyiséghez a javított értékek levonását követően és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="0adaa-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0adaa-129">A mennyiség növeléséhez módosított költségtranzakció számlázása.</span><span class="sxs-lookup"><span data-stu-id="0adaa-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0adaa-130">Nem számlázott értékesítés mennyiségének és összegének sztornírozása az eredeti költségjóváhagyásra.</span><span class="sxs-lookup"><span data-stu-id="0adaa-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0adaa-131">Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="0adaa-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0adaa-132">Díj számlázása.</span><span class="sxs-lookup"><span data-stu-id="0adaa-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0adaa-133">Nem számlázott értékesítés díjösszegének sztornírozása az naplósoron.</span><span class="sxs-lookup"><span data-stu-id="0adaa-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0adaa-134">Számlázott tényleges értékesítés mennyiségéhez és összegéhez az eredeti díj naplósorán.</span><span class="sxs-lookup"><span data-stu-id="0adaa-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="0adaa-135">Mérföldkő számlázása.</span><span class="sxs-lookup"><span data-stu-id="0adaa-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0adaa-136">Számlázott tényleges értesítés a projektszerződés eredeti mérföldkövén a mérföldkő mennyiségéhez.</span><span class="sxs-lookup"><span data-stu-id="0adaa-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
