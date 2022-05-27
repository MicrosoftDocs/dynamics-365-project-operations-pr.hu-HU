---
title: Jóváhagyási készletek
description: Ez a témakör elmagyarázza, hogyan kell dolgozni a jóváhagyási halmazokkal, a kérelmekkel és e műveletek részhalmazaival.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6809e01d8c3c93841125d0100d898dc208577019
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576227"
---
# <a name="approval-sets"></a>Jóváhagyási készletek

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A jóváhagyási készletek a jóváhagyás-kérelmeket a műveletek kisebb részhalmazaiba csoportosítja. Ez a csoportosítás lehetővé teszi a jóváhagyások projektenkénti, meghatározott sorrendben történő feldolgozását, valamint az újbóli próbálkozást és a sorrendiséget. A jóváhagyási kérelmek csoportosítása javítja a jóváhagyási folyamat megbízhatóságát és nyomon követhetőségét nagy mennyiségű jóváhagyás esetén.

A jóváhagyási készletek jelzik a kapcsolódó bejegyzések teljes feldolgozási állapotát. Amikor egy jóváhagyási rekordot egy jóváhagyási készlet felhasználásával dolgoznak fel, a rekord az **Elküldve** állapotból a **Jóváhagyva** állapotba kerül, és többé nem kapcsolódik a jóváhagyási készlethez. Ha egy rekord meghiúsul, amikor el van jelölve jóváhagyásra, a bejegyzés **Beküldött** állapotú marad, és a jóváhagyási készlet sikertelenként van megjelölve. A jóváhagyási készlet naplózza a hiba hibaüzenetét.

## <a name="processing-approvals-and-approval-sets"></a>Jóváhagyások és jóváhagyási készletek feldolgozása
A feldolgozási sorban várakozó jóváhagyások a **Jóváhagyások feldolgozása** nézetben láthatók. A rendszer aszinkron módon többször is feldolgozza az összes bejegyzést, beleértve a jóváhagyás újbóli megkísérlését, ha az előző kísérletek sikertelenek voltak.

A **Jóváhagyási készlet élettartama** mező rögzíti, hogy hány kísérlet maradt a készlet feldolgozására, mielőtt sikertelenként jelölték volna meg.

A jóváhagyási készleteket a program a Project Service nevű **felhőfolyamaton** alapuló időszakos aktiválással **dolgozza fel – Ismétlődően ütemezi a projektjóváhagyási készleteket**. Ez a **Project Operations nevű** megoldásban **található**. 

Győződjön meg arról, hogy a folyamat aktiválva van az alábbi lépések végrehajtásával.

1. Rendszergazdaként jelentkezzen be a [flow.microsoft.com](https://powerautomate.microsoft.com).
2. A jobb felső sarokban váltson a használt környezetre Dynamics 365 Project Operations.
3. Válassza a Megoldások **lehetőséget** a környezetben telepített megoldások felsorolásához.
4. A megoldáslistában válassza a Projektműveletek **lehetőséget**.
5. Módosítsa a szűrőt a Mindenről **a** **Felhőfolyamatokra**.
6. Ellenőrizze, hogy a **Projektszolgáltatás – Ismétlődően ütemezett projekt-jóváhagyási készletek** folyamatának be van-e **kapcsolva**. Ha nem, jelölje ki a folyamatot, majd válassza a Bekapcsolás **lehetőséget**.
7. Ellenőrizze, hogy a feldolgozás ötpercenként történik-e, ha áttekinti a **Rendszerfeladatok** listát a **Project Operations** környezet Beállítások Dataverse területén.

## <a name="failed-approvals-and-approval-sets"></a>Meghiúsult jóváhagyások és jóváhagyási készletek
A **Sikertelen jóváhagyások** nézet felsorolja az összes olyan jóváhagyást, amely felhasználói beavatkozást igényel. Nyissa meg a társított jóváhagyási készlet naplóit, hogy azonosítsa a hiba okát.
Ha kiválasztja az **Újrapróbálkozás** hozzáadja a a jóváhagyási készlet életciklusszámát, és visszahelyezi a jóváhagyási készletet **Feldolgozás** állapotba, és megpróbálja feldolgozni a fennmaradó rekordokat.

## <a name="configure-approval-sets"></a>Jóváhagyási készletek konfigurálása

### <a name="enable-the-approval-sets-feature"></a>A Jóváhagyási készletek funkció engedélyezése
A Jóváhagyáskészletek funkció engedélyezése előtt ellenőrizze, hogy nincsenek-e jóváhagyások feldolgozás alatt.

- Menjen a **Projektparaméterek** oldalra, és válassza a **Funkcióvezérlés** > **Modern jóváhagyások engedélyezése** lehetőséget.

### <a name="turn-off-the-approval-sets-feature"></a>Kapcsolja ki a Jóváhagyási készletek funkciót
A Jóváhagyáskészletek funkció kikapcsolása előtt ellenőrizze, hogy nincsenek-e jóváhagyások feldolgozás alatt.

- Menjen a **Projektparaméterek** oldalra, és válassza a **Funkcióvezérlés** > **Modern jóváhagyások letiltása** lehetőséget.

### <a name="configuring-the-asynchronous-threshold"></a>Az aszinkron küszöbérték konfigurálása 
A jóváhagyási készletek létrehozásakor a feldolgozás a háttérbe kerül, ha a jóváhagyásra kijelölt bejegyzések száma meghaladja a jelzett küszöbértéket. Az **Aszinkron küszöbérték** mező segítségével konfigurálhatja, hogy a jóváhagyás feldolgozása mikor fusson szinkronizált vagy aszinkron módon. Válassza ki a következő értékek egyikét:

  - Nulla: Minden kérést aszinkron módon kell feldolgozni. 
  - Nullánál nagyobb számok: A jóváhagyások feldolgozása csak akkor történik meg aszinkron módon, ha a beküldött jóváhagyások száma meghaladja ezt az értéket.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
