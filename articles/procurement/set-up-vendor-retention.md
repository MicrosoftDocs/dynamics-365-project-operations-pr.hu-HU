---
title: Szállítói visszatartás beállítása
description: Ez a cikk ismerteti a szállítói visszatartás beállítását.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f30e8829d8d5d99c81fce730cb93cd7ce31913fe
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929769"
---
# <a name="set-up-vendor-retention"></a>Szállítói visszatartás beállítása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a cikk a szállítói visszatartás beállításával kapcsolatosan nyújt tájékoztatást.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>A szállítói visszatartási számla beállítása a főkönyvben

1. A Dynamics 365 Finance alkalmazásban menjen a **Főkönyv** > **Feladás beállítása** > **Számlák az automatikus tranzakciókhoz** menübe.
2. Adjon hozzá egy új sort.
3. A **Feladás típusa** mezőben válassza a **Szállítói visszatartás** elemet.
4. Válassza ki a szállító visszatartás feladásához a fő számlát.

## <a name="create-vendor-retention-terms"></a>Szállítói visszatartási feltételek létrehozása

A **Szállítói visszatartási feltétele** lap használatával állítsa be és tartsa karban a szállítói fizetésre vonatkozó visszatartási feltételeket. Adja meg a szállítói kifizetés visszatartani kívánt részének százalékos arányát, illetve a korábban visszatartott összegek felszabadítani kívánt százalékát is. Az összegek a szállítói számlákhoz automatikusan vissza lesznek tartva mindaddig, amíg a szerződés el nem éri a megadott teljesítési állapotot. Miután beállította a szállító visszatartási feltételeit, alkalmazhatja azokat minden olyan projekthez, amelyen a szállító dolgozik.

1. A Finance-ben nyissa meg a **Projektvezetés és könyvelés** > **Beállítás** > **Visszatartás** > **Szállító fizetés-visszatartás feltételei** lehetőséget.
2. Új Szállítói visszatartási feltétel hozzáadásához válassza az **Új** lehetőséget. A **Szabály azonosítója** mező értéke automatikusan megjelenik a mezőben. 
3. A **Leírás** mezőben adjon beszédes nevet az új feltétel számára.
4. A **Feltételek** lapon válassza a **Sor hozzáadása** lehetőséget a szállítói visszatartási feltétel megadásához.
5. A **Szállított cikkek százaléka** mezőben adja meg a szabályhoz tartozó teljesítési százalékot. A rendszer automatikusan visszatartja a megfelelő összegeket a szállítói számlákon egészen addig, amíg a projekt teljesítési aránya el nem éri a megadott százalékos értéket. Ha például az 50,00 értéket adja meg, akkor a program az összegeket mindaddig visszatartja amíg a projekt 50%-ban be nem fejeződött.
6. A **Visszatartandó százalék** mezőben adja meg a szállítói számla visszatartandó összegének százalékos arányát. Ha például a 10,00 értéket adja meg a mezőben, a rendszer a szállítói számlákon szereplő összeg 10 százalékát tartja vissza addig, amíg a projekt el nem éri a **Szállított cikkek százaléka** mezőben Ön által megadott teljesítési százalékot.
7. A **Felszabadítandó százalék** mezőben válassza a Sor hozzáadása lehetőséget a százalékos érték megadásához, amelyet a korábban visszatartott összegekből fel kíván szabadítani a projekt teljesítésének kiválasztott szintjén.

> [!NOTE]
> Ha több mérföldkő van meghatározva a projekt teljesítésének különböző szintjeihez, minden visszatartási szabályhoz külön szállítói visszatartási feltételsort adjon meg. Minden sorban különböző százalékos értéket adhat meg a visszatartandó és a felszabadítandó százalékokhoz a projekt teljesítésének minden egyes szintjén.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>A szállító szerződés beállítása a projekthez

Állítsa be a projektre vonatkozó szállítói visszatartási feltételeket. A szállítóhoz létrehozott beszerzési megrendeléseken a szállítói visszatartási feltételek is megjelennek.

1. A Finance-ben válassza ki a **Projektvezetés és könyvelés** > **Projektek** > **Minden projekt** lehetőséget. 
2. Jelöljön ki egy projektet, és a műveletablakban és válassza a **Projektcsoport** > **Szállítói szerződések** lehetőséget.
3. A **Szállítói szerződések** lapon vegyen fel egy új sort.
4. Az **Partnerkód** mezőben válasszon a következő lehetőségek közül:
   - **Táblázat**: A szállítói visszatartási feltételek egyetlen szállítóra vonatkoznak.
   - **Csoport** – a szállítói visszatartási feltételek a szállítói csoport minden szállítója esetében érvényesek.
   - **Összes**: A szállítói visszatartási feltételek az összes szállítóra vonatkoznak.
5. A **Szállító/szállítói csoport mezőben** mezőben válassza ki azt a szállítót vagy szállítói csoportot, amelyikre a szállítói visszatartási feltételek vonatkoznak. Ha az előző lépésben az **Összes** lehetőséget választotta, akkor ez a mező nem érhető el.
6. A **Szállító visszatartási feltételei** mezőben válassza ki a szabályazonosítót, amely az adott szállítóra vonatkozó visszatartási feltételeket alkalmazza.

