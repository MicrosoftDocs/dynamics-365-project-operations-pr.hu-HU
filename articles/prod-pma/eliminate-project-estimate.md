---
title: Projekt becslésének eltávolítása
description: Ez a témakör a projektbecslés eltávolításával kapcsolatosan tartalmaz információkat, miután az elkészült.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 8bda8a7357e883b948449b2a19bea476996dde3c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078145"
---
# <a name="eliminate-a-project-estimate"></a>Projekt becslésének eltávolítása

[!include [banner](../includes/banner.md)]

A projektbecslések biztosítják a becsült és a projekthez ütemezett munka pénzügyi áttekintését. A projektek becsült értékének megadásához a projektet egy becsült projekthez kell csatolnia. A becsült projektek mindig egy meglévő projekten alapulnak, de több projekt is hivatkozhat egyetlen becsült projektre. Csak a rögzített árú és a beruházási projektek csatolhatók a becsült projektekhez, és a projekteknek ugyanahhoz a csoporthoz kell tartozniuk, mint a becsült projektnek.

A becsült projekt megszüntetéséhez annak teljesnek kell lennie. A következő lépésekből megtudhatja, hogyan lehet megszüntetni a becsléseket.

1. Lépjen a **Projektvezetés és könyvelés** > **Minden projekt** elemre, és nyissa meg a projektet. 
2. A **Kezelés** lapon jelölje ki a **Becslések** elemet, majd a **Becslés** lapon válassza az **Eltávolítás** lehetőséget.
3. A **Becslés eltávolítása** lap **Általános** fülén adja meg a következő beállításokat:

   - **Időszak kódja** : Válassza ki az időszak kódját a megfelelő becsült projektek kiválasztásához. 
   - **Becslés dátuma** : Válassza ki a megfelelő becslési dátumot az eltávolításhoz.
   - **Eltávolítás folyamatban lévő munka figyelmeztetésekkel** : Engedélyezze ezt a beállítást, ha értesítést szeretne kapni, amikor egy folyamatban lévő munkához kapcsolódó becslés el lesz távolítva. Ha a beállítás nincs engedélyezve, akkor az eltávolítás nem folytatható, ha nem becsült tranzakciók léteznek. 
   > [!NOTE]
   > Ez a beállítás csak akkor érhető el, ha az eltávolítást egy becsült projektre alkalmazza a rendszer. Periodikus feladás használata esetén nem érhető el. Ez a beállítás a **Projekt paraméterei** lap **Becslés** lapjának beállításaival működik az **Eltávolítás engedélyezése, ha nem becsült tranzakciók léteznek** mezőcsoportban.
   - **Fázis beállítása befejezettre** : Engedélyezze ezt a beállítást, ha az eltávolítás futtatása után a becsült projekt fázisát **Befejezett** értékre szeretné állítani.
   - **Becslési listák nyomtatása** : Válassza ki, hogy milyen adatok szerepeljenek a becslési listák kinyomtatásakor.
   - **Információs napló megjelenítése** : Engedélyezze ezt a beállítást az információs napló megjelenítéséhez.
   - **Könyvelési dátum** : Válassza ki a becslés főkönyvi feladási dátumát.

4.  Kattintson az **OK** gombra.
5. Az eltávolítási folyamat befejeződése után a megszüntetett becsült projekt negatív értékkel jelenik meg. 

Ha nem kívánja eltávolítani a becslést, akkor kiválaszthatja az eltávolított becslést, és kiválaszthatja az **Eltávolítás visszaállítása** elemet.   
