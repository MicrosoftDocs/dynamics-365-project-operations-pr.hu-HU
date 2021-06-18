---
title: Miért nem tudok rekordokat törölni a tényadatok entitásból?
description: Ez a témakör arról tájékoztat, hogy miért nem lehet bejegyzéseket törölni a tényleges entitásból.
author: JPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 434be93cedb4772616b1e6d5cbe15fc715eed19a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993104"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="6d7db-103">Miért nem tudok rekordokat törölni a Tényadatok entitásból?</span><span class="sxs-lookup"><span data-stu-id="6d7db-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6d7db-104">A Project Service Automation (PSA) nem teszi lehetővé a tényadatok törlését, mivel ezek az igazság forrásaként szolgálnak olyan tranzakciók esetében, amelyek pénzügyi következményekkel járnak a lefelé irányuló rendszerekre, például a főkönyvre.</span><span class="sxs-lookup"><span data-stu-id="6d7db-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="6d7db-105">Ha a tényleges adatok törölhetőek lennének, a pénzügyi jelentési tranzakciók integritása megkérdőjelezhetővé válna.</span><span class="sxs-lookup"><span data-stu-id="6d7db-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="6d7db-106">Az auditnapló megállapításához az ügyfeleknek a naplók segítségével kell létrehozniuk a kompenzációs tranzakciókat.</span><span class="sxs-lookup"><span data-stu-id="6d7db-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]