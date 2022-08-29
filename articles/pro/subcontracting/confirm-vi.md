---
title: Projekt szállítói számlájának megerősítése
description: Ez a cikk bemutatja, hogyan erősítheti meg a projektszállítói számlát a Microsoftnál Dynamics 365 Project Operations, és milyen pénzügyi hatása van a projekt szállítói számla megerősítésének.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261514"
---
# <a name="confirm-a-project-vendor-invoice"></a>Projekt szállítói számlájának megerősítése

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Miután ellenőrizte a szállítói számla összes sorát a Microsoftban Dynamics 365 Project Operations, a Megerősítés művelettel megerősítheti a szállítói számlát.

Ha a szállítói számlán a Megerősítés **lehetőséget választja**, a következő viselkedés jelenik meg:

1. A szállítói számla állapota Visszaigazolt állapotra **frissül**.
2. A visszaigazolt szállítói számla és a kapcsolódó rekordok csak olvashatóvá válnak, és nem szerkeszthetők vagy törölhetők.
3. Ha bármely bekerülési érték a szállítói számlasorra hivatkozik az egyeztetési folyamat részeként, a hivatkozott szállítói számlasorhoz társított összes költség tényleges érték vissza lesz fordítva.
4. Az új költség tényleges adatai a szállítói számlasoron található információk felhasználásával jönnek létre.
5. A szállítói számla megerősítése után már nem hozhat létre javítási naplókat, nem dolgozhatja fel az időbeviteli visszahívásokat, és nem vonhatja vissza a visszavont eredeti idő, költség vagy anyag tényleges adatok jóváhagyását.

> [!NOTE]
> Ha a szállítói számla bármely sora nem **Befejezett** ellenőrzési állapotú, a szállítói számla nem erősíthető meg.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
