---
title: Jóváhagyási készletek a Project Service Automation-ben
description: Ez témakör információkat tartalmaz a jóváhagyási készletről, a kérelmekről, valamint ezen műveletek részhalmazairól.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0783441d3bf7ed80192a3890a2e297fea05fe425
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583311"
---
# <a name="approval-sets-in-project-service-automation"></a>Jóváhagyási készletek a Project Service Automation-ben

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A jóváhagyási készletek a jóváhagyás-kérelmeket a műveletek kisebb részhalmazaiba csoportosítja. Ez a csoportosítás lehetővé teszi a jóváhagyások sorrendben való feldolgozását a Projekt által, és lehetővé teszi az újrapróbálkozást és a sorrendezést. A csoportosítás javítja a jóváhagyás-feldolgozás megbízhatóságát és nyomon követhetőségét nagy mennyiségű jóváhagyás esetén.

A jóváhagyási készletek jelzik a kapcsolódó bejegyzések teljes feldolgozási állapotát. Amikor egy jóváhagyási rekord feldolgozása egy jóváhagyási készlet használatával történik, a bejegyzés átlép a **Beküldött** állapotból **Jóváhagyott** állapotba, és nem lesz csatolva a jóváhagyási készlethez. Ha egy rekord meghiúsul, amikor el van jelölve jóváhagyásra, a bejegyzés **Beküldött** állapotú marad, és a jóváhagyási készlet sikertelenként van megjelölve. A jóváhagyási készlet naplózza a hiba hibaüzenetét.

## <a name="processing-approvals-and-approval-sets"></a>Jóváhagyások és jóváhagyási készletek feldolgozása
A feldolgozási sorban várakozó jóváhagyások a **Jóváhagyások feldolgozása** nézetben láthatók. A rendszer megpróbálja az összes bejegyzést aszinkron módon feldolgozni, beleértve a jóváhagyás újrapróbálkozási kísérletét is, ha a korábbi próbálkozások sikertelenek voltak.

A **Jóváhagyási készlet élettartama** mező rögzíti, hogy hány kísérlet maradt a készlet feldolgozására, mielőtt sikertelenként jelölték volna meg.

## <a name="failed-approvals-and-approval-sets"></a>Meghiúsult jóváhagyások és jóváhagyási készletek
A **Sikertelen jóváhagyások** nézet felsorolja a felhasználói beavatkozást igénylő összes jóváhagyást. Nyissa meg a társított jóváhagyási készlet naplóit, hogy azonosítsa a hiba okát.
Ha kiválasztja az **Újrapróbálkozás** hozzáadja a a jóváhagyási készlet életciklusszámát, és visszahelyezi a jóváhagyási készletet **Feldolgozás** állapotba, és megpróbálja feldolgozni a fennmaradó rekordokat.

## <a name="configure-approval-sets"></a>Jóváhagyási készletek konfigurálása

###  <a name="enable-the-approval-sets-feature"></a>A Jóváhagyási készletek funkció engedélyezése
A Jóváhagyáskészletek funkció engedélyezése előtt ellenőrizze, hogy nincsenek-e jóváhagyások feldolgozás alatt.

- Menjen a **Projektparaméterek** oldalra, és válassza a **Funkcióvezérlés** > **Modern jóváhagyások engedélyezése** lehetőséget.

### <a name="turn-off-the-approval-sets-feature"></a>Kapcsolja ki a Jóváhagyási készletek funkciót
A Jóváhagyáskészletek funkció kikapcsolása előtt ellenőrizze, hogy nincsenek-e jóváhagyások feldolgozás alatt.

- Menjen a **Projektparaméterek** oldalra, és válassza a **Funkcióvezérlés** > **Modern jóváhagyások letiltása** lehetőséget.

### <a name="configuring-the-asynchronous-threshold"></a>Az aszinkron küszöbérték konfigurálása 
A jóváhagyási készletek létrehozásakor a feldolgozás a háttérbe kerül, ha a jóváhagyásra kijelölt bejegyzések száma meghaladja a jelzett küszöbértéket. Az **Aszinkron küszöbérték** mező segítségével konfigurálhatja, hogy a jóváhagyás feldolgozása mikor fusson szinkronizált vagy aszinkron módon.
Az érvényes értékek a következők:

  - Nulla: Minden kérést aszinkron módon kell feldolgozni. 
  - Nullánál nagyobb számok: A jóváhagyások feldolgozása csak akkor történik meg aszinkron módon, ha a beküldött jóváhagyások száma meghaladja ezt az értéket.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
