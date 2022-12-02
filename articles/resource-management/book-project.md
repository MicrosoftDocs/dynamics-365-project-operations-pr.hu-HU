---
title: Projekt foglalása
description: Ez a cikk információt nyújt az erőforrások lefoglalásáról egy projekthez.
author: ruhercul
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dca9d722eae595af7a81c2b4684729d7658ed012
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928527"
---
# <a name="book-to-a-project"></a>Projekt foglalása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Vannak olyan időpontok, amikor egy projektmenedzsernek vagy erőforrás-kezelőnek egy erőforrást kell lefoglalnia a projekthez meghatározott követelmény nélkül egy általános csoporttagtól. Ez három módon valósítható meg.

- Foglalás a csoporttagrácsból
- Foglalás az ütemezési tábláról
- Foglalás a **Projekt** űrlapról

## <a name="book-from-the-team-member-grid"></a>Foglalás a csoporttagrácsból

Ha a szervezet hibrid erőforrás-elosztási módban működik, akkor a projektmenedzser az alábbi lépések végrehajtásával közvetlenül a projekthez tudja lefoglalni az erőforrásokat.

1. A projektből nyissa meg a csoporttagrácsot, és válassza az **Új** lehetőséget.
2. Adja meg az erőforrás pozíciójának nevét és szerepét.
3. Válassza ki a lefoglalható erőforrást a rendelkezésre álló keresésből.
4. Az erőforrás kiválasztását követően adja meg a következő mezők adatait az erőforrás lefoglalásához:

    - Kezdődátum
    - Befejezési dátum
    - Felosztási mód
    - Órák száma, ha alkalmazható
    - Projekt jóváhagyója

6. Válassza a **Mentés és bezárás** lehetőséget.

## <a name="book-from-the-schedule-board"></a>Foglalás az ütemezési tábláról

Amikor egy erőforrás-kezelőnek közvetlenül egy projekthez kell lefoglalnia az erőforrást, az ütemezési táblát és a projektkövetelményt is használhatja. A projektkövetelmény olyan erőforrás-követelmény, amely minden esetben elérhető a foglaláshoz. A közvetlenük egy projektűrlapra történő foglaláshoz hajtsa végre b következő lépéseket.

1. Lépjen az ütemezési táblához, és a bal oldalon szűrje a szükségletre szánt szükséges erőforrásokat.
2. Az alsó ablaktáblában válassza a **Projekt** lapot a projektkövetelmények listájának megjelenítéséhez.
3. Húzza a követelményt egy erőforrásra, és adja meg a következő adatokat:

    - Kezdési dátum
    - Befejezési dátum
    - Foglalás állapota
    - Foglalási módszer
    - Duration
   
   > [!NOTE]
   > Jelenleg a Dynamics 365 Project Operations nem támogatja az ütemezési táblát.   

## <a name="book-from-the-project-form"></a>Foglalás a Projekt űrlapról

Projektmenedzserként előfordulhat, hogy erőforrást kell lefoglalnia egy projekthez, de csak a feltételeket tudja megismerni, nem az erőforrás nevét. Hajtsa végre a következő lépéseket, hogy az ütemezési segéd segítségével megkeresse az erőforrást az erőforrás bármely rendelkezésre álló attribútuma alapján. 

1. Lépjen a projekthez, és válassza a **Foglalás** lehetőséget az ütemezési segéd megnyitásához.
2. Az ütemezési segéd bal oldalán található szűrők használatával szűkítse a feltételeket, és válassza a **Keresés** lehetőséget.
3. Az eredményekben visszaadott erőforrások alapján lefoglalhatja az erőforrásokat.

> [!NOTE]
> Ez a módszer nem hoz létre az erőforráshoz tartozó foglalásokat. Ehelyett az erőforrást hozzáadja a projektcsoporthoz. Miután a csapattagot hozzáadta a projekthez, a projektmenedzser használhatja a foglalások fenntartását vagy a foglalások kiterjesztését, és felveheti a szükséges foglalásokat az erőforráshoz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
