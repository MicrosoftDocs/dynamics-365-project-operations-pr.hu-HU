---
title: Az ár miért alapértelmezett nulla a tényleges a tényleges időköltségeknél?
description: Annak meghatározása, hogy az ár miért alapértelmezett nulla a tényleges a tényleges időköltségeknél
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: 597d75b7-fadf-4947-8d52-95425ff90324
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 448c6c0569a40e1d7cb133561435811ecedb4356
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752330"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="fa78e-103">Az ár miért alapértelmezett nulla a tényleges a tényleges időköltségeknél?</span><span class="sxs-lookup"><span data-stu-id="fa78e-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="fa78e-104">Ez a gyakori kérdések rész azokra a tényleges költségekre vonatkozik, ahol a tranzakcióosztály Idő értékre van állítva, és tranzakció típusa Költség.</span><span class="sxs-lookup"><span data-stu-id="fa78e-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="fa78e-105">A következő három ellenőrzés segít a hibaelhárításban, hogy az ár miért alapértelmezetten 0 a tényleges időköltségeknél.</span><span class="sxs-lookup"><span data-stu-id="fa78e-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="fa78e-106">1. ellenőrzés: Azonosítsa a költségárlistát a projekthez</span><span class="sxs-lookup"><span data-stu-id="fa78e-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="fa78e-107">Keresés a projektet a tényleges projektmezőjében, majd ugorjon a projektlapra.</span><span class="sxs-lookup"><span data-stu-id="fa78e-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="fa78e-108">Kattintson a mezőben a szerződő részleg hivatkozásra.</span><span class="sxs-lookup"><span data-stu-id="fa78e-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="fa78e-109">A Szerződő részleg oldalon ellenőrizze, hogy a szerződő egység rendelkezik-e árlistával a költségárlista rácson.</span><span class="sxs-lookup"><span data-stu-id="fa78e-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="fa78e-110">Ha egynél több árlista van, akkor sikerült behatárolni a probléma.</span><span class="sxs-lookup"><span data-stu-id="fa78e-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="fa78e-111">A Project Service szervezeti egységenként csak egy árlistát támogat.</span><span class="sxs-lookup"><span data-stu-id="fa78e-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="fa78e-112">Távolítson el minden árlistát ehhez az entitáshoz, amíg a szervezeti egység költségárlista rácsához már csak egy árlista van csatolva.</span><span class="sxs-lookup"><span data-stu-id="fa78e-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="fa78e-113">Ha nincsenek csatolva árlisták a szervezeti egységhez , jegyezze fel a szervezeti egységet pénznemét.</span><span class="sxs-lookup"><span data-stu-id="fa78e-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="fa78e-114">Menjen a Project Service alkalmazásba, majd a Paraméterek elemhez, és nyissa meg az Árlisták lapot, Ellenőrizze, hogy van-e árlista, amely Költségre és pénznemre hivatkozik, amely megfelel a Szervezeti egység pénznemének.</span><span class="sxs-lookup"><span data-stu-id="fa78e-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="fa78e-115">Ha nincsenek a kritériumnak megfelelő árlisták, akkor sikerült a problémát azonosítani.</span><span class="sxs-lookup"><span data-stu-id="fa78e-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="fa78e-116">Győződjön meg arról, hogy legalább egy árlista van amelynek hivatkozása Költség értékre van állítva, és amelynek pénzneme megegyezik a szervezeti egységet pénznemével.</span><span class="sxs-lookup"><span data-stu-id="fa78e-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="fa78e-117">Ha egynél több árlista van, amely megfelel a feltételeknek, olvassa tovább a dokumentumot a további ellenőrzésekhez.</span><span class="sxs-lookup"><span data-stu-id="fa78e-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="fa78e-118">2. ellenőrzés: A fentebb felsorolt árlisták bármelyike érvényese a tényleges időköltség napján?</span><span class="sxs-lookup"><span data-stu-id="fa78e-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="fa78e-119">Ahhoz, hogy a Project Service alapértelmezett árként vegye figyelembe az árlistát, az árlistának vonatkoznia kell az időköltség dátumán.</span><span class="sxs-lookup"><span data-stu-id="fa78e-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="fa78e-120">Ellenőrizze a következőket, hogy a fentebb felsorolt árlisták érvényesek-e:</span><span class="sxs-lookup"><span data-stu-id="fa78e-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="fa78e-121">Ellenőrizze, hogy a csatolt árlisták kezdő és befejező dátumai nem üresek-e az Általános lapon.</span><span class="sxs-lookup"><span data-stu-id="fa78e-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="fa78e-122">Ha a kezdő és befejező dátumok fent azonosított árlistáknál üresek, akkor azonosította a problémát.</span><span class="sxs-lookup"><span data-stu-id="fa78e-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="fa78e-123">Jegyezze fel a tényleges időköltség kezdő dátum mezőjének tartalmát és ellenőrizze, hogy az azonosított árlisták bármelyike vonatkozik-e erre a dátumra.</span><span class="sxs-lookup"><span data-stu-id="fa78e-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="fa78e-124">Például a tényleges időköltség dátuma az árlista kezdő és befejező dátuma közé kell essen.</span><span class="sxs-lookup"><span data-stu-id="fa78e-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="fa78e-125">Ha nincs olyan árlista, amely vonatkozik az aktuális időköltség dátumára, akkor a problémát azonosította.</span><span class="sxs-lookup"><span data-stu-id="fa78e-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="fa78e-126">Módosítsa az árlista kezdő és befejező dátumait annak érdekében, hogy az árlista vonatkozzon az időköltség a dátumára.</span><span class="sxs-lookup"><span data-stu-id="fa78e-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="fa78e-127">Ha több olyan árlista van, amely vonatkozik az aktuális idő költség dátumára, akkor a problémát azonosította.</span><span class="sxs-lookup"><span data-stu-id="fa78e-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="fa78e-128">Ezt úgy javíthatja, hogy az árlisták kezdő- és befejező dátumait úgy módosítja hogy csak egy árlista vonatkozzon, a tényleges időköltség dátumára.</span><span class="sxs-lookup"><span data-stu-id="fa78e-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="fa78e-129">Ha csak egy árlista vonatkozik a tényleges időköltség dátumára, ugorjon a dokumentum következő szakaszára.</span><span class="sxs-lookup"><span data-stu-id="fa78e-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="fa78e-130">Amikor kész a szükséges javításokkal, hozzon létre újra egy időbejegyzést, és győződjön meg arról, hogy az aktuális időtöltség az érvényes árat mutatja-e.</span><span class="sxs-lookup"><span data-stu-id="fa78e-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="fa78e-131">3. ellenőrzés: Van egy ár az árlistában az árazási dimenziókhoz az aktuális időköltséghez?</span><span class="sxs-lookup"><span data-stu-id="fa78e-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="fa78e-132">Ha sikeresen befejezte az 1. és 2 ellenőrzést, most már rendelkezik csak egy árlistával rendelkezik, amely érvényes a tényleges időköltség napján.</span><span class="sxs-lookup"><span data-stu-id="fa78e-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="fa78e-133">Nyissa meg a ezt az árlistát, és lépjen a Szerepkörárak lapra. Győződjön meg arról, hogy van egy sor a rácson az árazási dimenziókhoz a tényleges költségnél.</span><span class="sxs-lookup"><span data-stu-id="fa78e-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="fa78e-134">Ha nincs sor a szerepkörár rácson az árazási dimenzióhoz a tényleges költségnél, azonosította a problémát.</span><span class="sxs-lookup"><span data-stu-id="fa78e-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="fa78e-135">Hozzon létre egy sort Szerepkörárak rácson az árazási dimenziókhoz a tényleges időköltségnél.</span><span class="sxs-lookup"><span data-stu-id="fa78e-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="fa78e-136">Amikor végzett ezzel, hozzon létre újra egy időbejegyzést, és győződjön meg arról, hogy az aktuális időköltség az érvényes árat mutatja-e.</span><span class="sxs-lookup"><span data-stu-id="fa78e-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="fa78e-137">Ha még mindig nem látható érvényes ár az aktuális időköltségnél, miután elvégezte a három ellenőrzést, hozzon létre egy támogatási jegyet.</span><span class="sxs-lookup"><span data-stu-id="fa78e-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



