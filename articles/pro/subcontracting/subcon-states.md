---
title: Állapotátváltások az alvállalkozói szerződésben
description: Ez a cikk az alvállalkozói szerződés állapotátalakulásait ismerteti a Microsoftban Dynamics 365 Project Operations az alvállalkozói szerződés létrehozásakor, végrehajtásakor és lezárásakor.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 02553099a6728c19c219659dff431ff9a5cf10fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261203"
---
# <a name="state-transitions-on-a-subcontract"></a>Állapotátváltások az alvállalkozói szerződésben 

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a cikk az alvállalkozói szerződés állapotátlépéseit ismerteti a Microsoftban Dynamics 365 Project Operations. Minden állam tervezetként, megerősítettként, lezártként vagy töröltként jelenik meg. Az alábbi képen az állapotátmenetek láthatók.

![Alvállalkozói állapotmodell](../media/SubconStates.png)  

Az alábbi táblázat leírja, hogy az egyes állapotok mit képviselnek a Project Operations alvállalkozói szerződésének életciklusában.

| State | Description | Engedélyezett átmenetek |
| --- | --- | --- |
| Piszkozat | Ez az alvállalkozói szerződés kezdeti állapotát jelenti. A szállítóval folytatott tárgyalások folyamatban vannak. A sorok és az árak változhatnak. Az ebben az állapotban lévő alvállalkozói szerződés felhasználható az erőforrásokra és anyagokra vonatkozó projektkövetelmények becslésére és személyzetének növelésére. A projekt időben, költség- és anyaghasználatán is hivatkozhat rá. Az ebben az állapotban lévő alvállalkozói szerződések szerkeszthetők és törölhetők. | Megerősített |
| Megerősített | Ez az alvállalkozói szerződés azon szakaszát jelenti, hogy a szállítóval az árképzésről és a megvásárolt sorokról folytatott tárgyalások befejeződtek. Az anyagok és/vagy az alvállalkozói erőforrások által végzett munka tényleges szállítása azonban még folyamatban van. Az ebben az állapotban lévő alvállalkozói szerződés felhasználható az erőforrásokra és anyagokra vonatkozó projektkövetelmények becslésére és személyzetének növelésére. A projekt időben, költség- és anyaghasználatán is hivatkozhat rá. Az ebben az állapotban lévő alvállalkozói szerződés nem szerkeszthető vagy törölhető. A **Mégse** gomb lehetővé teszi a megerősített alvállalkozói szerződés visszavonását. Az **Újranyitás** gomb lehetővé teszi az alvállalkozói szerződés újbóli megnyitását, hogy visszaállítsa Piszkozat **státuszba**. **A Bezárás** gombbal lezárhat egy megerősített alvállalkozói szerződést. | Bezárva <br> Megszakított <br> Piszkozat |
| Bezárva | Ez az alvállalkozói szerződés azon szakaszát jelenti, amikor az anyagok és/vagy az alvállalkozásba adott erőforrások által végzett munka tényleges szállítása befejeződik. Az ebben az állapotban lévő alvállalkozói szerződés már nem használható fel az erőforrásokra és anyagokra vonatkozó projektkövetelmények becslésére és személyzetére. Ezenkívül már nem lehet hivatkozni rá a projekt időben, költségén és anyaghasználatán. Az ebben az állapotban lévő alvállalkozói szerződés nem szerkeszthető vagy törölhető. | None |
| Megszakított | Ez az alvállalkozói szerződés azon szakaszát jelenti, amikor már nincs szükség az anyagok és/vagy az alvállalkozásba adott erőforrások által végzett munka tényleges szállítására. Ebben az állapotban az alvállalkozói szerződés nem használható az erőforrásokra és anyagokra vonatkozó projektkövetelmények becslésére és személyzetének növelésére, és nem is lehet hivatkozni rá a projekt időbeli, kiadási és anyagfelhasználási adataira vonatkozóan. Az ebben az állapotban lévő alvállalkozói szerződés nem szerkeszthető vagy törölhető. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
