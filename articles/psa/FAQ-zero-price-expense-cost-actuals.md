---
title: Az ár miért alapértelmezetten nulla a tényleges kiadásköltségeknél?
description: Annak meghatározása, hogy az ár miért alapértelmezett nulla a tényleges a tényleges kiadásköltségeknél
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078113"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="313d0-103">Az ár miért alapértelmezetten nulla a tényleges kiadásköltségeknél?</span><span class="sxs-lookup"><span data-stu-id="313d0-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="313d0-104">Ez a gyakori kérdések rész azokra a tényleges költségekre vonatkozik, ahol a tranzakcióosztály Költség értékre van állítva, és tranzakció Költség.</span><span class="sxs-lookup"><span data-stu-id="313d0-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="313d0-105">Költségarányokkal kapcsolatos hibaelhárítás az aktuális kiadásköltségeknél</span><span class="sxs-lookup"><span data-stu-id="313d0-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="313d0-106">Nyissa meg a kapcsolódó költségbejegyzést, és győződjön meg arról, hogy van összeg a költség mezőben.</span><span class="sxs-lookup"><span data-stu-id="313d0-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="313d0-107">Ha az eredeti költség bejegyzésben az összeg mező nincs kitöltve, akkor azonosította a problémát.</span><span class="sxs-lookup"><span data-stu-id="313d0-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="313d0-108">A probléma megoldásához hozza létre újból a költségbejegyzést egy érvényes értékkel, és hagyja jóvá azt.</span><span class="sxs-lookup"><span data-stu-id="313d0-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
