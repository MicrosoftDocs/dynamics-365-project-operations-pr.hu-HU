---
title: Jóváhagyási készletek
description: Ez a témakör elmagyarázza, hogyan kell dolgozni a jóváhagyási halmazokkal, a kérelmekkel és e műveletek részhalmazaival.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323239"
---
# <a name="approval-sets"></a>Jóváhagyási készletek

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A jóváhagyási készletek a jóváhagyás-kérelmeket a műveletek kisebb részhalmazaiba csoportosítja. Ez a csoportosítás lehetővé teszi a jóváhagyások projektenkénti, meghatározott sorrendben történő feldolgozását, valamint az újbóli próbálkozást és a sorrendiséget. A jóváhagyási kérelmek csoportosítása javítja a jóváhagyási folyamat megbízhatóságát és nyomon követhetőségét nagy mennyiségű jóváhagyás esetén.

A jóváhagyási készletek jelzik a kapcsolódó bejegyzések teljes feldolgozási állapotát. Amikor egy jóváhagyási rekordot egy jóváhagyási készlet felhasználásával dolgoznak fel, a rekord az **Elküldve** állapotból a **Jóváhagyva** állapotba kerül, és többé nem kapcsolódik a jóváhagyási készlethez. Ha egy rekord meghiúsul, amikor el van jelölve jóváhagyásra, a bejegyzés **Beküldött** állapotú marad, és a jóváhagyási készlet sikertelenként van megjelölve. A jóváhagyási készlet naplózza a hiba hibaüzenetét.

## <a name="processing-approvals-and-approval-sets"></a>Jóváhagyások és jóváhagyási készletek feldolgozása
A feldolgozási sorban várakozó jóváhagyások a **Jóváhagyások feldolgozása** nézetben láthatók. A rendszer aszinkron módon többször is feldolgozza az összes bejegyzést, beleértve a jóváhagyás újbóli megkísérlését, ha az előző kísérletek sikertelenek voltak.

A **Jóváhagyási készlet élettartama** mező rögzíti, hogy hány kísérlet maradt a készlet feldolgozására, mielőtt sikertelenként jelölték volna meg.

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
