---
title: Az ár miért alapértelmezetten nulla a tényleges kiadásköltségeknél?
description: Annak meghatározása, hogy az ár miért alapértelmezett nulla a tényleges a tényleges kiadásköltségeknél
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: bc1ebc58-c733-4310-8435-572ed9a9fef9
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3fb678822877a61d141de75aea29b7d5cdf292c4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752218"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="286b7-103">Az ár miért alapértelmezetten nulla a tényleges kiadásköltségeknél?</span><span class="sxs-lookup"><span data-stu-id="286b7-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="286b7-104">Ez a gyakori kérdések rész azokra a tényleges költségekre vonatkozik, ahol a tranzakcióosztály Költség értékre van állítva, és tranzakció Költség.</span><span class="sxs-lookup"><span data-stu-id="286b7-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="286b7-105">Költségarányokkal kapcsolatos hibaelhárítás az aktuális kiadásköltségeknél</span><span class="sxs-lookup"><span data-stu-id="286b7-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="286b7-106">Nyissa meg a kapcsolódó költségbejegyzést, és győződjön meg arról, hogy van összeg a költség mezőben.</span><span class="sxs-lookup"><span data-stu-id="286b7-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="286b7-107">Ha az eredeti költség bejegyzésben az összeg mező nincs kitöltve, akkor azonosította a problémát.</span><span class="sxs-lookup"><span data-stu-id="286b7-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="286b7-108">A probléma megoldásához hozza létre újból a költségbejegyzést egy érvényes értékkel, és hagyja jóvá azt.</span><span class="sxs-lookup"><span data-stu-id="286b7-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
