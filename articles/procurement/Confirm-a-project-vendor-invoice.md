---
title: Projekt szállítói számláinak megerősítése
description: Ez a cikk ismerteti, hogyan lehet megerősíteni a projekt beszállítója számláját a Microsoft Dynamics 365 Project Operations alkalmazásban, valamint a projekt beszállítók számlái megerősítésének pénzügyi hatásait írja le.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475480"
---
# <a name="confirm-project-vendor-invoices"></a>Projekt szállítói számláinak megerősítése

**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

Ha engedélyezi a **Projektvezető manuális jóváhagyása szükséges** paramétert, a Microsoft Dataverse-ben létrehozott beszállítói számlák **Vázlat** állapotúak lesznek. Az ily módon létrehozott szállítói számlákat ellenőrizni kell, és manuálisan meg kell erősíteni. Ha a **Projektvezető manuális jóváhagyása szükséges paramétert** le van tiltva, a Dataverse-ben létrehozott beszállítói számlák automatikusan meg lesznek erősítve. További művelet nem szükséges. 

Miután ellenőrizte a szállítói számla minden sorát a Dynamics 365 Project Operations alkalmazásban , válassza a **Megerősítés** lehetőséget a szállítói számla megerősítéséhez.

Ha egy szállító számláján a **Megerősítés** lehetőséget választja, a következő viselkedés történik:

1. A rendszer **Megerősítve** állapotra frissíti a szállítói számla állapotát.
1. A megerősített szállítói számla és a kapcsolódó rekordok írásvédetté válnak, és nem szerkeszthetők vagy törölhetők.
1. Ha a költség tényszámai a szállítói számla sorára hivatkoznak az egyeztetési folyamat részeként, akkor a hivatkozott szállítói számlasorhoz társított összes költség-tényadatot a rendszer sztornózza.
1. Az új költség-tényadatokat hoz létre a szállítói számlasor információi alapján.
1. Már nem hozhat létre korrekciós naplókat, nem dolgozhatja fel az időbejegyzések visszavonását, és vonhatja vissza az eredeti idő, költség vagy anyag tényadatainak jóváhagyását, amelyek sztornózva lettek.
1. A Dynamics 365 Finance alkalmazásban a **Projektköltség** értéke a Projekt integrációs napló használatával frissül, a Beszerzési integrációs fiók pedig a Projektintegrációs napló feladását követően *sztornózva* lesz.

> [!NOTE]
> Ha egy szállítói számla bármelyik sorának ellenőrzési állapota nem **Kész**, a szállítói számlát nem lehet megerősíteni.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
