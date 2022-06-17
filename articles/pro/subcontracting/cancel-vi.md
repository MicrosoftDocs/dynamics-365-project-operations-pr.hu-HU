---
title: Projekt szállítói számlájának érvénytelenítése
description: Ez a cikk azt ismerteti, hogyan törölhet egy projektszállítói számlát a Microsoftnál Dynamics 365 Project Operations, és milyen pénzügyi hatása van a projekt szállítói számla törlésének.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7ddaadc0f6e336a8ba67bb4ad8000f7e894f3eb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911553"
---
# <a name="cancel-a-project-vendor-invoice"></a>Projekt szállítói számlájának érvénytelenítése

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A szállítói számla megerősítése után az nem szerkeszthető vagy törölhető. Ha hiba történt egy visszaigazolt szállítói számlán, a Mégse művelettel visszafordíthatja a szállítói számla hatását, és létrehozhat egy új szállítói számlát.

Ha a Szállítói számlán a Mégse lehetőséget **választja**, a következő viselkedés jelenik meg:

1. A szállítói számla állapota Törölve állapotra **frissül**.
2. A törölt szállítói számla és a kapcsolódó rekordok írásvédetté válnak, és nem szerkeszthetők vagy törölhetők.
3. A szállítói számlasorok alapján a szállítói számla visszaigazolásának részeként létrehozott költség-tényleges értékeket a rendszer visszavonja.
4. Ha az egyeztetési folyamat részeként bekerülési értékeket kapcsoltak a szállítói számlasorokhoz, az eredeti szállítói számla megerősítése visszavonta azokat. A szállítói számla törlése során a rendszer újra létrehozza ezeket a költség-tényleges költségeket. Az eredet az idő, a költség vagy az anyaghasználat bejegyzéseire mutat.
5. A szállítói számla törlése után ismét létrehozhat javítási naplókat, feldolgozhatja az időbeviteli visszahívásokat, és visszavonhatja az eredeti idő, költség vagy anyag tényleges adatainak jóváhagyását.

> [!NOTE]
> Csak a visszaigazolt projektszállítói számlák törölhetők. A más államokban lévő szállítói számlákat nem lehet visszavonni.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
