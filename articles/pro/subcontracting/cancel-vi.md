---
title: Projekt szállítói számlájának érvénytelenítése
description: Ez a cikk ismerteti, hogyan lehet visszavonni a projekt beszállítója számláját a Microsoft Dynamics 365 Project Operations alkalmazásban, valamint a projekt beszállítók számlái visszavonásának pénzügyi hatásait.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261093"
---
# <a name="cancel-a-project-vendor-invoice"></a>Projekt szállítói számlájának érvénytelenítése

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A szállítói számla a megerősítést követően nem módosítható vagy törölhető. Ha egy szállító számláján hiba történt, és azt megerősítették akkor a Mégse művelet használható a szállítói számla hatásának visszafordítására, és egy új szállítói számla létrehozására.

Ha egy szállító számláján a **Visszavonás** lehetőséget választja, a következő viselkedés történik:

1. A rendszer **Visszavonva** állapotra frissíti a szállítói számla állapotát.
2. A visszavont szállítói számla és a kapcsolódó rekordok írásvédetté válnak, és nem szerkeszthetők vagy törölhetők.
3. A rendszer a szállítói számla megerősítésének részeként a szállítói számlasorok alapján létrehozott költség-tényadatokat visszavonja.
4. Ha a költség tényadatai az egyeztetési folyamat során a szállító számlasorához lettek társítva, az eredeti szállítói számla jóváhagyása visszavonta azokat. A szállítói számlák visszavonása során a költség tényszámai újra létrejönnek. Az eredet az idő-, költség- vagy anyaghasználati bejegyzésekre mutat.
5. A szállítói számla visszavonása után ismét létrehozhat korrekciós naplókat, feldolgozhatja az időbejegyzések visszavonását, és visszavonhatja az eredeti idő, költség vagy anyag tényadatainak jóváhagyását.

> [!NOTE]
> Csak a megerősített projektbeszállítói számlákat lehet visszavonni. A más állapotba tartozó szállítói számlák nem visszavonhatóak.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
