---
title: Erőforrás-kérés benyújtása
description: Ez a témakör információkat nyújt a projekt erőforrás iránti kérelem benyújtásáról.
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: acdd228a9eb9d6c6c56f126ccca416613332a838
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013174"
---
# <a name="submitting-a-resource-request"></a>Erőforrás-kérés benyújtása

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A létrehozott erőforrás-igényt erőforrás-kérésként is beadhatja. Ezután a kérést teljesítés céljából elküldik egy erőforrás-kezelőnek.

1. A Project Service Automation (PSA) rendszerben a **Projektek** oldalon kattintson a **Csapat** fülre, hogy megtekintse a foglalható erőforrások listáját. 
2. Válassza ki a listából az általános erőforrást, amely rendelkezik erőforrás-követelménnyel, majd kattintson a **Kérés benyújtása** elemre.

![Erőforrás-kérés benyújtása](media/RM-how-to-18.png)

Az általános csapattag kérésének státusza **Benyújtott** lesz.

Miután a kérést az erőforrás-kezelő teljesítette, az általános erőforrást egy megnevezett erőforrás váltja fel, ha az erőforrás-kezelő egy megnevezett erőforrás lefoglalásával teljesíti a kérést. Ellenkező esetben az általános erőforrás a csapaton marad, és a kérés állapota **Áttekintés szükséges** értékre változik , ha az erőforrás-kezelő egy megnevezett erőforrást javasolt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]