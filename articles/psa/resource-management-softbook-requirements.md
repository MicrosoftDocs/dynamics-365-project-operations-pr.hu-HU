---
title: Szoftverkövetelmények
description: Ez a témakör információkat nyújt arról, hogyan kell foglalni a követelményeket.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 736d59976ad0f456a694cedbb28b516c90632fe6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282921"
---
# <a name="soft-book-requirements"></a>Szoftverkövetelmények

[!include [banner](../includes/psa-now-project-operations.md)]

Az erőforrás-igény keményen foglalható. A kemény foglalás olyan javaslatot hoz létre, amely felhasználja az erőforrás kapacitását. A javaslatot ezután visszatérés céljából megküldik a kérelmezőnek jóváhagyás céljából. A puha foglalás egy ideiglenesen hozzáad egy erőforrást a projektcsoporthoz, és más státusszal rendelkezik az Ütemezési táblán, de nem használja fel az erőforrás kapacitását. Az erőforrás ütemezéséhez az Ütemezési táblán állítsa be a **Foglalási állapot** mezőt **Lágy** értékre.

![A foglalás státusa lágyra van állítva](media/Resource-Management-image77.png)

Amikor a **Csapat** fül a **Megnevezett csapattagok** nézetben található, ott jelenik meg az erőforrás. A puhán foglalt órákat a **Puhán foglalt órák** oszlopban kell feltüntetni.

![Kedvezményesen lefoglalva tartott órák a Megnevezett csapattagok nézetében](media/Resource-Management-image78.png)

A puha foglalású csapattagokat feladatokhoz lehet rendelni.

![A feladathoz kiosztott, puha foglalású csapattag](media/Resource-Management-image79.png)

Az **Összehangolás** lapon nem jelennek meg a puhán foglalt erőforrások foglalása, mivel az **Összehangolás** lapon csak a nehéz foglalásokat veszi figyelembe.

![Szoftverkönyvvel ellátott erőforrás foglalások nélkül az Egyeztetés lapon](media/Resource-Management-image80.png)

> [!NOTE]
> Az erőforrást nem lehet könyvelni egy általános csapattag által generált követelmény alapján.

Az Ütemezési táblán az erőforrás puha foglalásainak eltérő színezése történik.

![Puha foglalás a menetrend táblán](media/Resource-Management-image81.png)

A puha foglalás átalakításához egy kemény foglalássá az Ütemező táblán kattintson a jobb gombbal a puha foglalásra, majd válassza az **Állapot megváltoztatása** \> **Kemény foglalás** \> **Nehéz** lehetőséget.

![A foglalás státuszának keményre változtatása](media/Resource-Management-image82.png)

A foglalás megváltozik, és az állapot megváltozik az Ütemezési táblán. Mivel a foglalási státus most **Kemény**, az erőforrás foglaltként jelenik meg, kapacitása és rendelkezésre állása módosítva.

Ugyanezt a módszert használhatja a kemény foglalás vagy az engedményes foglalás törlésére az Ütemezési táblán.

A projekt **Csapat** lapján a foglalt erőforrás nehezen foglalttá történő konvertálásához válassza ki az erőforrást, majd válassza a **Megerősítés** lehetőséget.

![Megerősítés parancs](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]