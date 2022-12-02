---
title: Újdonságok vagy változások a Project Service Automation 12-es frissítési kiadásának V3 változatában
description: Ez a cikk információkat nyújt arról, hogy milyen újdonságok és változások vannak a Project Service Automation 12-es frissítési kiadásának V3 verziójában.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 28539b2e1331c8509e40aaf771f4d88d6f54e022
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922639"
---
# <a name="project-service-automation-update-release-12-v3"></a>Project Service Automation 12-es frissítési kiadás, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Örömmel jelentjük be a Dynamics 365 Project Service Automation (PSA) alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez nyissa meg a megoldások oldalt. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a cikk felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 12-es frissítési kiadásában. Ennek a verziónak a build száma V3.10.2.34, és általánosan elérhető egy önálló frissítésben 2019 októberében.

## <a name="update-release-12"></a>12-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

- Idő és költség

    - Javítva: Az időbevitel hibaüzenetei további releváns környezettel frissültek.
    - Javítva: Az időbeviteli rács és az ütemezés helyesen jeleníti meg a függőleges görgetősávot, ha szükséges.
    - Javítva: Az elküldött és a jóváhagyott költség- időbejegyzések jóváhagyhatók.
    - Javítva: A jóváhagyás megerősítésének visszavonása párbeszédpanel üzenete ki lett javítva, hogy tükrözze a jóváhagyás állapotát a **Jóváhagyott** értékről **Beküldött** értékre való váltáskor.
    - Javítva: Az **Ár**, **Egység** és **Mennyiség** mezők zárolva vannak a Ráfordítás bejegyzésen, miután annak jóváhagyása megtörtént.

- Projektmenedzsment

    - Javítva: Az **Új** művelet a **Csapattag** fő űrlapon el lett távolítva.
    - Javítva: Az erőforrás-hozzárendelések frissítése javítva lett, hogy számoljon a pontatlan kerekítési hibákkal, amelyek egy feladat záró dátumának eltolódását okozzák.
    - Javítva: A feladatrácsban a releváns kiszolgálóoldali hibák a felhasználó számára is láthatók lesznek.
    - Javítva A csapattag neve a feladat személyválasztójában jelenik meg a pozíciónév helyett.

- Erőforráskezelés

    - Jaívítva: Az erőforrás-követelmények részletei a sablonból létrehozott projektek esetén a projektnaptárt használják.
    - Javítva: A szakértelmek és a kompetenciák alapértelmezetten a szerepkör mesteradataiból kerülnek a szerepkörhöz létrehozott erőforráskövetelményeibe.

- Sales

    - Javítva: A **Szerződés fő** űrlapján található duplikált objektumazonosítók.
    - Javítva: a logika frissítve lett, így láthatóvá válik az **Ajánlat elemzése** lap, hogy megjelenítse a lap metaadat-beállításait.
    - Javítva: A tényleges bejegyzésen a számlázási dátum immár az idő/költség dátumából származik és nem a jóváhagyás dátumából.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
