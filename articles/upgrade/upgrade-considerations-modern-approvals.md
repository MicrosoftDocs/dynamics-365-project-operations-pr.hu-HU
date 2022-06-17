---
title: Modern jóváhagyások frissítési szempontjai
description: A cikk azokat a pontokat ismerteti, amelyeket a rendszergazdáknak figyelembe kell venniük, amikor engedélyezik a Modern jóváhagyások funkciót.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931747"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Modern jóváhagyások frissítési szempontjai 

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A 2022. áprilisi 1. hullám kiadásának részeként a Modern jóváhagyások funkció alapértelmezés szerint engedélyezve lesz. Ez a funkció javítja a jóváhagyási logika megbízhatóságát, és biztosítja, hogy meg tudja határozni az okot, ha a jóváhagyási logika sikertelen.

A módosítás részeként a projektjóváhagyások állapotváltozásai frissülnek. Az állapot mostantól közvetlenül a Beküldött **állapotból** a Jóváhagyva állapotba **kerül**. **A Függőben már** nem szerepel a jóváhagyások állapota. Annak megállapításához, hogy egy jóváhagyás függőben van-e, ellenőrizze, hogy a jóváhagyás egy jóváhagyási készlet része-e, és tekintse át a csatolt jóváhagyási készlet állapotát.

## <a name="before-you-upgrade"></a>A frissítés előtt

Mielőtt modern jóváhagyásokra frissítene, győződjön meg arról, hogy nincsenek függőben lévő jóváhagyások. A Modern jóváhagyások nem használja a **Függőben állapotot**. Ezért a frissítés után is Függőben állapotúként **megjelölt** jóváhagyások nem lesznek feldolgozva.

## <a name="after-you-upgrade"></a>A frissítés után

A modern jóváhagyásokra való frissítés után a rendszergazdának ellenőriznie kell, hogy a jóváhagyásokat feldolgozó felhőfolyamat engedélyezve van-e.

1. Jelentkezzen be flow.microsoft.com [...](https://flow.microsoft.com)
2. Az oldal jobb felső sarkában váltsa át a környezetet a frissített környezetre.
3. Válassza a Megoldások **lehetőséget** a környezetben telepített megoldások listához.
4. A megoldáslistában válassza a Project Operations vagy a Project Service **lehetőséget**.**·**
5. Módosítsa a szűrőt Az összesről **a** **Felhőfolyamatokra**.
6. Ellenőrizze, hogy a **Project Service – Ismétlődően ütemezze a projekt-jóváhagyási készleteket** beállítás Be értékre van-e **állítva**. Ha nem, válassza ki a folyamatot, majd válassza a Bekapcsolás **lehetőséget**.
7. Ellenőrizze, hogy a feldolgozás ötpercenként történik-e, ha áttekinti a **Rendszerfeladatok** listát a **Beállítások** területen.

## <a name="short-term-rollback"></a>Rövid távú visszagörgetés

Ha nem tudja felvenni a módosításokat, vagy ha súlyos problémába ütközik ezzel a funkcióval kapcsolatban, ideiglenesen visszatérhet az eredeti jóváhagyási folyamathoz a következő lépések végrehajtásával:
1. Jelentkezzen be a környezetbe, és ellenőrizze, hogy nincsenek-e függőben lévő jóváhagyások.
2. Lépjen a **Beállítások** > **projektparaméterek elemre**.
3. Válassza a **Funkcióvezérlés**, majd a Modern jóváhagyások **lehetőséget** a funkció kikapcsolásához.

## <a name="removing-the-feature-flag"></a>A funkciójelölő eltávolítása

A 2022. októberi 2. hullám frissítésében megszűnik a funkció kikapcsolásának lehetősége.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
