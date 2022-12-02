---
title: Jóváhagyási készletek
description: Ez a cikk elmagyarázza, hogyan kell dolgozni a jóváhagyási halmazokkal, a kérelmekkel és e műveletek részhalmazaival.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: ca205073edbce2b399aab3ae273d635c8af96765
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524919"
---
# <a name="approval-sets"></a>Jóváhagyási készletek

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A jóváhagyási készletek a jóváhagyás-kérelmeket a műveletek kisebb részhalmazaiba csoportosítja. Ez a csoportosítás lehetővé teszi a jóváhagyások projektenkénti, meghatározott sorrendben történő feldolgozását, valamint az újbóli próbálkozást és a sorrendiséget. A jóváhagyási kérelmek csoportosítása javítja a jóváhagyási folyamat megbízhatóságát és nyomon követhetőségét nagy mennyiségű jóváhagyás esetén.

A jóváhagyási készletek jelzik a kapcsolódó bejegyzések teljes feldolgozási állapotát. Amikor egy jóváhagyási rekordot egy jóváhagyási készlet felhasználásával dolgoznak fel, a rekord az **Elküldve** állapotból a **Jóváhagyva** állapotba kerül, és többé nem kapcsolódik a jóváhagyási készlethez. Ha egy rekord meghiúsul, amikor el van jelölve jóváhagyásra, a bejegyzés **Beküldött** állapotú marad, és a jóváhagyási készlet sikertelenként van megjelölve. A jóváhagyási készlet naplózza a hiba hibaüzenetét.

## <a name="processing-approvals-and-approval-sets"></a>Jóváhagyások és jóváhagyási készletek feldolgozása
A feldolgozási sorban várakozó jóváhagyások a **Jóváhagyások feldolgozása** nézetben láthatók. A rendszer aszinkron módon többször is feldolgozza az összes bejegyzést, beleértve a jóváhagyás újbóli megkísérlését, ha az előző kísérletek sikertelenek voltak.

A **Jóváhagyási készlet élettartama** mező rögzíti, hogy hány kísérlet maradt a készlet feldolgozására, mielőtt sikertelenként jelölték volna meg.

A jóváhagyási készleteket a rendszer egy időszakos aktiválással dolgozza fel egy **Felhőfolyamat** alapján, amelynek neve **Project Service – Projektjóváhagyási készletek ismétlődő ütemezése**. Ez megtalálható a **Project Operations** nevű **Megoldásban**. 

A következő lépések elvégzésével győződjön meg arról, hogy a folyamat aktiválva van.

1. Rendszergazdaként jelentkezzen be a [flow.microsoft.com](https://powerautomate.microsoft.com) weboldalra.
2. A jobb felső sarokban váltson arra a környezetre, amelyet a Dynamics 365 Project Operations alkalmazásban használ.
3. Válassza a **Megoldások** lehetőséget a környezetbe telepített megoldások felsorolásához.
4. Válassza a megoldáslistában a **Project Operations** lehetőséget.
5. A szűrőt módosítsa **Minden** helyett **Felhőfolyamatok** értékre.
6. Ellenőrizze, hogy a **Project Service – Projektjóváhagyási készletek ismétlődő ütemezése** folyamat **Be** van-e kapcsolva. Ha nem, válassza ki a folyamatot, majd válassza a **Bekapcsolás** lehetőséget.
7. Ellenőrizze, hogy a feldolgozás öt percenként történik-e meg, ehhez tekintse át a **Rendszerfeladatok** listát a **Beállítások** területen a Project Operations Dataverse-környezetében.

## <a name="failed-approvals-and-approval-sets"></a>Meghiúsult jóváhagyások és jóváhagyási készletek
A **Sikertelen jóváhagyások** nézet felsorolja az összes olyan jóváhagyást, amely felhasználói beavatkozást igényel. Nyissa meg a társított jóváhagyási készlet naplóit, hogy azonosítsa a hiba okát.
Ha kiválasztja az **Újrapróbálkozás** hozzáadja a a jóváhagyási készlet életciklusszámát, és visszahelyezi a jóváhagyási készletet **Feldolgozás** állapotba, és megpróbálja feldolgozni a fennmaradó rekordokat.

## <a name="configure-approval-sets"></a>Jóváhagyási készletek konfigurálása

### <a name="enable-the-approval-sets-feature"></a>A Jóváhagyási készletek funkció engedélyezése
A Jóváhagyáskészletek funkció engedélyezése előtt ellenőrizze, hogy nincsenek-e jóváhagyások feldolgozás alatt. A szolgáltatás engedélyezése után az nem tiltható le.

- Menjen a **Projektparaméterek** oldalra, és válassza a **Funkcióvezérlés** > **Modern jóváhagyások engedélyezése** lehetőséget.

### <a name="configuring-the-asynchronous-threshold"></a>Az aszinkron küszöbérték konfigurálása 
A jóváhagyási készletek létrehozásakor a feldolgozás a háttérbe kerül, ha a jóváhagyásra kijelölt bejegyzések száma meghaladja a jelzett küszöbértéket. Az **Aszinkron küszöbérték** mező segítségével konfigurálhatja, hogy a jóváhagyás feldolgozása mikor fusson szinkronizált vagy aszinkron módon. Válassza ki a következő értékek egyikét:

  - Nulla: Minden kérést aszinkron módon kell feldolgozni. 
  - Nullánál nagyobb számok: A jóváhagyások feldolgozása csak akkor történik meg aszinkron módon, ha a beküldött jóváhagyások száma meghaladja ezt az értéket.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
