---
title: A Modern jóváhagyások frissítési szempontjai
description: A cikk azokat a pontokat tartalmazza, amelyek a rendszergazdáknak a Modern Approvals funkcionalitás engedélyezésekor figyelembe kell venniük.
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
# <a name="upgrade-considerations-for-modern-approvals"></a>A Modern jóváhagyások frissítési szempontjai 

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A 2022. áprilisi 1. hullám kiadás részeként a Modern jóváhagyások funkció alapértelmezés szerint engedélyezve lesz. Ez a funkció javítja a jóváhagyási logika megbízhatóságát, és biztosítja, hogy Ön megállapíthassa a jóváhagyási logika sikertelenségének okát.

A módosítás részeként a projekt jóváhagyások állapotváltozásai is frissülnek. Az állapot mostantól **Beküldött** helyett közvetlenül **Jóváhagyott** lesz. A **Függőben** a továbbiakban nem jóváhagyás-állapot. Annak megállapításához, hogy egy jóváhagyás függőben van-e, ellenőrizze, hogy a jóváhagyás egy jóváhagyási készlet része-e, valamint tekintse át a csatolt jóváhagyási készlet állapotát.

## <a name="before-you-upgrade"></a>A frissítés előtt

A Modern Approvals verzióra való frissítés előtt ellenőrizze, hogy nincsenek-e függőben lévő jóváhagyások. A modern jóváhagyások nem használja a **Függőben** állapotot. Ezért a frissítés után **Függőben** lévőként megjelölt jóváhagyások nem lesznek feldolgozva.

## <a name="after-you-upgrade"></a>A frissítés után

A Modern jóváhagyásokra való frissítés után a rendszergazdának ellenőriznie kell, hogy engedélyezve van-e a jóváhagyásokat feldolgozó felhőfolyamat.

1. Jelentkezzen be a [flow.microsoft.com](https://flow.microsoft.com) webhelyre
2. A lap jobb felső sarkában váltsa át a környezetet a frissített környezetre.
3. Válassza a **Megoldások** lehetőséget a környezetbe telepített megoldások felsorolásához.
4. Válassza a megoldáslistában a **Project Operations** vagy a **Project Service** lehetőséget.
5. A szűrőt módosítsa **Minden** helyett **Felhőfolyamatok** értékre.
6. Ellenőrizze, hogy a **Project Service – Projektjóváhagyási készletek ismétlődő ütemezése** beállítás **Be** van-e kapcsolva. Ha nem, válassza ki a folyamatot, majd válassza a **Bekapcsolás** lehetőséget.
7. Ellenőrizze, hogy a feldolgozás öt percenként megtörténik-e, ha áttekinti a **Beállítások** területen található **Rendszer feladatok** listát.

## <a name="short-term-rollback"></a>Rövidtávú visszaállítás

Ha a módosítások problémát okoznak, vagy ha a funkcióval kapcsolatban komoly probléma lép fel, a következő lépések elvégzésével ideiglenesen visszaállhat az eredeti jóváhagyási folyamatra:
1. Jelentkezzen be a környezetbe, és ellenőrizze, hogy nincsenek függőben lévő jóváhagyások.
2. Lépjen a **Beállítások** > **Projektparaméterek** pontra.
3. Válassza a **Funkcióvezérlés** lehetőséget, majd a **Modern Jóváhagyások** lehetőséget a funkció kikapcsolásához.

## <a name="removing-the-feature-flag"></a>A szolgáltatásjelző eltávolítása

A 2022. októberi, 2. hullámú frissítésben a szolgáltatás kikapcsolási lehetősége el lesz távolítva.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
