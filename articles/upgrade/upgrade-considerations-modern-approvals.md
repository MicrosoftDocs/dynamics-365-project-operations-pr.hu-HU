---
title: Frissítési szempontok a modern jóváhagyásokhoz
description: A témakör azokat a pontokat fedi le, amelyeket a rendszergazdáknak figyelembe kell venniük a Modern jóváhagyások funkció engedélyezésekor.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a3757f057a801318feccde9be3e49c7b40fa8fcb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578389"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Frissítési szempontok a modern jóváhagyásokhoz 

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A 2022. áprilisi Wave 1 kiadás részeként a Modern jóváhagyások funkció alapértelmezés szerint engedélyezve lesz. Ez a funkció javítja a jóváhagyási logika megbízhatóságát, és biztosítja, hogy meg tudja határozni az okot, ha a jóváhagyási logika sikertelen.

A módosítás részeként frissülnek a projektjóváhagyások állapotváltozásai. Az állapot most közvetlenül a Beküldve **állapotból** a Jóváhagyottba **megy**. **A függőben** lévő állapot már nem a jóváhagyások állapota. Annak megállapításához, hogy a jóváhagyás függőben van-e, ellenőrizze, hogy a jóváhagyás egy jóváhagyási készlet része-e, és tekintse át a csatolt jóváhagyási készlet állapotát.

## <a name="before-you-upgrade"></a>Frissítés előtt

Mielőtt modern jóváhagyásokra váltana, győződjön meg arról, hogy nincsenek függőben lévő jóváhagyások. A modern jóváhagyások nem használják a **Függő állapot** státuszt. Ezért a frissítés után még függőben lévőként **megjelölt** jóváhagyások feldolgozása nem történik meg.

## <a name="after-you-upgrade"></a>A frissítés után

A Modern jóváhagyásokra való frissítés után a rendszergazdának ellenőriznie kell, hogy a jóváhagyásokat feldolgozó felhőfolyamat engedélyezve van-e.

1. Bejelentkezés a [flow.microsoft.com](https://flow.microsoft.com)
2. A lap jobb felső sarkában váltson a környezetére a frissített környezetre.
3. Válassza a Megoldások **lehetőséget** a környezetben telepített megoldások felsorolásához.
4. A megoldáslistában válassza a Projektműveletek **vagy** a Projektszolgáltatás **lehetőséget**.
5. Módosítsa a szűrőt a Mindenről **a** **Felhőfolyamatokra**.
6. Ellenőrizze, hogy a **Projektszolgáltatás – Ismétlődően ütemezi a projektjóváhagyási készletek** ütemezése beállítást Be **értékre** állítva. Ha nem, jelölje ki a folyamatot, majd válassza a Bekapcsolás **lehetőséget**.
7. Ellenőrizze, hogy a feldolgozás ötpercenként történik-e a **Beállítások** területen található **Rendszerfeladatok** lista áttekintésével.

## <a name="short-term-rollback"></a>Rövid távú visszagörgetés

Ha nem tudja felvenni a módosításokat, vagy ha súlyos problémát tapasztal ezzel a funkcióval kapcsolatban, a következő lépésekkel ideiglenesen visszatérhet az eredeti jóváhagyási folyamathoz:
1. Jelentkezzen be a környezetébe, és ellenőrizze, hogy nincsenek-e függőben lévő jóváhagyások.
2. Nyissa meg a **Projektparaméterek beállításai** > **lehetőséget**.
3. Válassza **a Funkcióvezérlés lehetőséget,** majd válassza a Modern jóváhagyások **lehetőséget** a funkció kikapcsolásához.

## <a name="removing-the-feature-flag"></a>A funkció jelzőjének eltávolítása

A 2022. októberi Wave 2 frissítésben a funkció kikapcsolásának lehetősége megszűnik.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
