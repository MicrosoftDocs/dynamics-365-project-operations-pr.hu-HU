---
title: Projekt szállítói számlájának megerősítése
description: Ez a témakör bemutatja, hogyan lehet megerősíteni a projekt szállítói számláját a Microsoftban Dynamics 365 Project Operations, valamint a projekt szállítói számlájának megerősítésének pénzügyi hatását.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595731"
---
# <a name="confirm-a-project-vendor-invoice"></a>Projekt szállítói számlájának megerősítése

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Miután ellenőrizte a Microsoft Dynamics 365 Project Operations szállítói számláján szereplő összes sort, a Megerősítés művelettel megerősítheti a szállítói számlát.

Ha a Szállítói számlán a Megerősítés **lehetőséget választja**, a következő viselkedés lép fel:

1. A szállítói számla állapota megerősítve **lesz**.
2. A visszaigazolt szállítói számla és a hozzá kapcsolódó bejegyzések írásvédetté válnak, és nem szerkeszthetők vagy törölhetők.
3. Ha bármely költségalapot tartalmazó tényleges költség a szállítói számlasorra hivatkozik az egyeztetési folyamat részeként, a hivatkozott szállítói számlasorhoz társított összes költségalapot a rendszer sztornírozza.
4. Az új költségalapokat a szállítói számlasorban szereplő információk alapján hozzák létre.
5. A szállítói számla megerősítése után a továbbiakban nem hozhat létre korrekciós naplókat, nem dolgozhatja fel az időbevitel visszahívását, és nem szakíthatja meg a sztornírozott eredeti idő-, költség- vagy anyagaték jóváhagyását.

> [!NOTE]
> Ha a szállítói számla bármely sorának ellenőrzési állapota nem **Teljes**, a szállítói számla nem erősíthető meg.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
