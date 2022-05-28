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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7de9f660bf38629bb2af4e0fb1ebf815f5e525e2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595593"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Az ár miért nulla alapértelmezésben az önköltség tényadataiban

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ez a gyakori kérdések rész azokra a tényleges költségekre vonatkozik, ahol a tranzakcióosztály Költség értékre van állítva, és tranzakció Költség.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Költségarányokkal kapcsolatos hibaelhárítás az aktuális kiadásköltségeknél

Nyissa meg a kapcsolódó költségbejegyzést, és győződjön meg arról, hogy van összeg a költség mezőben. Ha az eredeti költség bejegyzésben az összeg mező nincs kitöltve, akkor azonosította a problémát.
 
A probléma megoldásához hozza létre újból a költségbejegyzést egy érvényes értékkel, és hagyja jóvá azt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
