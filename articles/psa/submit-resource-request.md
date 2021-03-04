---
title: Erőforrás-kérés benyújtása
description: Ez a témakör információkat nyújt a projekt erőforrás iránti kérelem benyújtásáról.
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 173572be43149aea253bf7beddb993f8c50ab337
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149726"
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