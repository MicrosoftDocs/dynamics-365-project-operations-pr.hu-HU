---
title: Projekt szállítói számlájának visszavonása
description: Ez a témakör bemutatja, hogyan lehet törölni egy projekt szállítói számláját a Microsoftban Dynamics 365 Project Operations, valamint a projekt szállítói számlájának visszavonásának pénzügyi hatását.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 87f6bdca30c5779e3d70922e75609ff4cdfca167
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580643"
---
# <a name="cancel-a-project-vendor-invoice"></a>Projekt szállítói számlájának visszavonása

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A szállítói számla megerősítése után nem lehet szerkeszteni vagy törölni. Ha egy megerősített szállítói számlán hiba történt, a Mégse művelettel sztornírozhatja a szállítói számla hatását, és új szállítói számlát hozhat létre.

Ha szállítói számlán a Mégse lehetőséget **választja**, a következő jelenség jelenik meg:

1. A szállítói számla állapota Visszavonva értékre **frissül**.
2. A visszavont szállítói számla és a hozzá kapcsolódó bejegyzések írásvédetté válnak, és nem szerkeszthetők vagy törölhetők.
3. A szállítói számlasorok alapján a szállítói számla megerősítése részeként létrehozott költségalapokat a rendszer sztornírozza.
4. Ha az egyeztetési folyamat részeként bármilyen költség-tényleges érték a szállítói számlasorokhoz volt csatolva, az eredeti szállítói számla visszaigazolása sztornírozta azokat. A szállítói számla törlése során ezek a költségalapokat a program újra létrehozza. A származás az idő-, költség- vagy anyagfelhasználási bejegyzésekre mutat.
5. A szállítói számla visszavonása után ismét létrehozhat korrekciós naplókat, feldolgozhatja az időbejegyzések visszahívását, és visszavonhatja az eredeti idő-, költség- vagy anyagatikai adatok jóváhagyását.

> [!NOTE]
> Csak a visszaigazolt projekt szállítói számlák törölhetők. Más államokban a szállítói számlák nem vonhatók vissza.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
