---
title: Az ár miért alapértelmezetten nulla a tényleges kiadásköltségeknél?
description: Annak meghatározása, hogy az ár miért alapértelmezett nulla a tényleges a tényleges kiadásköltségeknél
author: rumant
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
ms.openlocfilehash: 03c958635dec66b0f243872dfb929eba6a20119b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992789"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="721cb-103">Az ár miért nulla alapértelmezésben az önköltség tényadataiban</span><span class="sxs-lookup"><span data-stu-id="721cb-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="721cb-104">Ez a gyakori kérdések rész azokra a tényleges költségekre vonatkozik, ahol a tranzakcióosztály Költség értékre van állítva, és tranzakció Költség.</span><span class="sxs-lookup"><span data-stu-id="721cb-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="721cb-105">Költségarányokkal kapcsolatos hibaelhárítás az aktuális kiadásköltségeknél</span><span class="sxs-lookup"><span data-stu-id="721cb-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="721cb-106">Nyissa meg a kapcsolódó költségbejegyzést, és győződjön meg arról, hogy van összeg a költség mezőben.</span><span class="sxs-lookup"><span data-stu-id="721cb-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="721cb-107">Ha az eredeti költség bejegyzésben az összeg mező nincs kitöltve, akkor azonosította a problémát.</span><span class="sxs-lookup"><span data-stu-id="721cb-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="721cb-108">A probléma megoldásához hozza létre újból a költségbejegyzést egy érvényes értékkel, és hagyja jóvá azt.</span><span class="sxs-lookup"><span data-stu-id="721cb-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]