---
title: Miért nem tudok rekordokat törölni a tényadatok entitásból?
description: Ez a cikk arról tájékoztat, hogy miért nem lehet bejegyzéseket törölni a tényleges entitásból.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: bd446961432a8f18895db45699d7a731d55235b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925583"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Miért nem tudok rekordokat törölni a Tényadatok entitásból?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A Project Service Automation (PSA) nem teszi lehetővé a tényadatok törlését, mivel ezek az igazság forrásaként szolgálnak olyan tranzakciók esetében, amelyek pénzügyi következményekkel járnak a lefelé irányuló rendszerekre, például a főkönyvre. Ha a tényleges adatok törölhetőek lennének, a pénzügyi jelentési tranzakciók integritása megkérdőjelezhetővé válna. Az auditnapló megállapításához az ügyfeleknek a naplók segítségével kell létrehozniuk a kompenzációs tranzakciókat.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
