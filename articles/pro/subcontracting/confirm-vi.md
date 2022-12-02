---
title: Projekt szállítói számlájának megerősítése
description: Ez a cikk ismerteti, hogyan lehet megerősíteni a projekt beszállítója számláját a Microsoft Dynamics 365 Project Operations alkalmazásban, valamint a projekt beszállítók számlái megerősítésének pénzügyi hatásait.
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

Miután ellenőrizte a szállítói számla minden sorát a Microsoft Dynamics 365 Project Operations alkalmazásban, használhatja a Megerősítés lehetőséget a szállítói számla megerősítéséhez.

Ha egy szállító számláján a **Megerősítés** lehetőséget választja, a következő viselkedés történik:

1. A rendszer **Megerősítve** állapotra frissíti a szállítói számla állapotát.
2. A megerősített szállítói számla és a kapcsolódó rekordok írásvédetté válnak, és nem szerkeszthetők vagy törölhetők.
3. Ha a költség tényszámai a szállítói számla sorára hivatkoznak az egyeztetési folyamat részeként, akkor a hivatkozott szállítói számlasorhoz társított összes költség-tényadatot a rendszer sztornózza.
4. Az új költség-tényadatokat hoz létre a szállítói számlasor információi alapján.
5. A szállítói számla megerősítése már nem hozhat létre korrekciós naplókat, dolgozhatja fel az időbejegyzések visszavonását, vagy vonhatja vissza az eredeti idő, költség vagy anyag tényadatainak jóváhagyását, amelyek sztornózva lettek.

> [!NOTE]
> Ha egy szállítói számla bármelyik sorának ellenőrzési állapota nem **Kész**, a szállítói számlát nem lehet megerősíteni.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
