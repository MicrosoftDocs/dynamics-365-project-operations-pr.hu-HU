---
title: Projektszállítói számlák megerősítése
description: Ez a cikk bemutatja, hogyan erősítheti meg a projektszállítói számlát a Microsoftnál Dynamics 365 Project Operations, és ismerteti a projektszállítói számla megerősítésének pénzügyi hatását.
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
# <a name="confirm-project-vendor-invoices"></a>Projektszállítói számlák megerősítése

**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

Ha a **Kötelező paraméter a PM általi manuális megerősítéshez** paraméter engedélyezve van, a létrehozott Microsoft Dataverse szállítói számlák Vázlat **állapotúak**. Az így létrehozott szállítói számlákat felül kell vizsgálni és manuálisan meg kell erősíteni. Ha a **PM általi manuális megerősítés kötelező** paraméter le van tiltva, a rendszer automatikusan megerősíti a benne Dataverse létrehozott szállítói számlákat. Nincs szükség további intézkedésre. 

Miután ellenőrizte a szállítói számla Dynamics 365 Project Operations összes sorát, válassza a Megerősítés **lehetőséget** a szállítói számla megerősítéséhez.

Ha a szállítói számlán a Megerősítés **lehetőséget választja**, a következő viselkedés jelenik meg:

1. A szállítói számla állapota Visszaigazolt **állapotra** frissül.
1. A visszaigazolt szállítói számla és a kapcsolódó rekordok csak olvashatóvá válnak, és nem szerkeszthetők vagy törölhetők.
1. Ha bármely bekerülési érték a szállítói számlasorra hivatkozik az egyeztetési folyamat részeként, a hivatkozott szállítói számlasorhoz társított összes költség tényleges érték vissza lesz fordítva.
1. Az új költség tényleges adatai a szállítói számlasoron található információk felhasználásával jönnek létre.
1. A továbbiakban nem hozhat létre javítási naplókat, nem dolgozhatja fel az időbejegyzések visszahívását, és nem törölheti a visszavont eredeti idő-, költség- vagy anyag-tényleges adatok jóváhagyását.
1. A Dynamics 365 Finance a Projekt költségértéke a **Projektintegrációs napló használatával frissül, és a Beszerzési integrációs számla** a Projektintegrációs napló feladása után vissza lesz fordítva *.*

> [!NOTE]
> Ha a szállítói számla bármely sora nem **Befejezett** ellenőrzési állapotú, a szállítói számla nem erősíthető meg.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
