---
title: Korábban jóváhagyott bejegyzések visszahívása
description: Ez a cikk ismerteti, hogyan kérheti a projektcsoport tagja a korábban elküldött és jóváhagyott időpontok, kiadások és anyaghasználat rekordjait, valamint hogy a projektvezető hogyan hagyhatja jóvá vagy utasíthatja vissza a kéréseket.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 54fc7ac2301a4423ebf70b0b67ad489580c347b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930367"
---
# <a name="recall-previously-approved-entries"></a>Korábban jóváhagyott bejegyzések visszahívása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A projektcsoport tagja vagy más személy, aki benyújt egy idő-, költség vagy anyaghasználati bejegyzést, visszavonhatja azt a bejegyzést miután azt jóváhagyták. Az visszahívási folyamat két fő lépésből áll:

1. A benyújtó visszahívást kér.
2. A visszahívási kérelmet a jóváhagyó személy hagyja jóvá.

## <a name="request-a-recall"></a>Kérjen visszahívást

Kövesse ezeket a lépéseket egy jóváhagyott idő-, költség- vagy anyaghasználati bejegyzés visszahívásának kérésére.

1. Kövesse ezen lépések egyikét attól függően, hogy milyen típusú bejegyzést szeretne visszahívni:

    - Időbeírásokhoz válassza a **Projektek** \> **Saját munka** \> **Időbejegyzés**, és válassza ki az összes időbejegyzést a projekt és a feladat egy adott kombinációjára. Alternatív megoldásként a rácsban válassza ki az egyes cellákat az adott időpontra egy adott dátumra egy adott projekthez.
    - Költségbejegyzés esetén válassza a **Projektek** \> **Saját munka** \> **Költségek** menüpontot, és válassza ki a visszahívandó költségbejegyzés sorát.
    - Anyaghasználati bejegyzésekhez válassza a **Projektek** \> **Saját munka** \> **Anyaghasználati napló** menüpontot, és válassza ki a visszahívandó anyaghasználati napló sorát.

2. Válassza az **Előhívás** lehetőséget. Megjelenik a jóváhagyást kérő párbeszédpanel. Ha a kiválasztott idő-, költség- vagy anyaghasználati bejegyzéseket már jóváhagyták, a rendszer kéri, hogy írja be a visszahívás okát.
3. Írja be a visszahívás okát, majd a művelet megerősítéséhez válassza az **OK** lehetőséget. A rendszer kéri a bejegyzés jóváhagyóját a visszahívás jóváhagyására.

> [!IMPORTANT]
> Nem hozhat létre visszahívási kérelmet egy jóváhagyott időpont, költség és anyaghasználati tétel jóváhagyását, amely már ki lett számlázva az ügyfélnek. Ha megkísérli, üzenetet kap, amelyben jelzi, hogy az időt, költségeket vagy anyaghasználati bejegyzést nem lehet visszahívni, mert már kiszámlázásra került. Ebben az esetben a bejegyzése visszahívását csak akkor kérelmezheti, ha az eredeti számlához egy helyesbítő számlával ad jóváírást vagy teljes visszatérítést az ügyfélnek.

## <a name="approve-or-reject-a-recall-request"></a>A visszahívás jóváhagyása vagy elutasítása

A visszahívás jóváhagyásához vagy elutasításához kövesse ezeket a lépéseket.

1. Válassza a **Projektek** \> **Saját munka** \> **Jóváhagyások** lehetőséget.
2. A **Jóváhagyások** lista oldalon módosítsa a nézetet **Jogosultsági kérelmek előhívása** nézetre. Megjelenik a benyújtott visszahívási kérelmek listája.
3. Válasszon egy vagy több bejegyzést, majd válassza az **Jóváhagyás** vagy az **Elutasítás** lehetőséget.
4. Ha a **Jóváhagyást** választotta, figyelmeztető üzenetet kap, amely elmagyarázza a jóváhagyás hatását. A művelet megerősítéséhez válassza az **OK** lehetőséget. A visszahívási kérelmet jóváhagyják.

    –vagy–

    Ha az **Elutasítás** lehetőséget választotta, akkor a visszahívási kérelmet elutasítják.

> [!IMPORTANT]
> Amikor egy visszahívást jóváhagynak éppen akkor, amikor kérelmezik, a rendszer ellenőrzi az esetleges számlázási tevékenységeket az idő-költség- vagy anyaghasználati bejegyzésen. Ha egy bejegyzésre már számláztak, vagy ha számlatervezetről van szó, akkor a jóváhagyó hibaüzenetet fog kapni, amely kijelenti, hogy az időt vagy a költségeket nem lehet jóváhagyni a visszahíváshoz, mert már számláztak. Ebben az esetben a jóváhagyó a bejegyzés visszahívását csak akkor kérelmezheti, ha az eredeti számlához egy helyesbítő számlával ad jóváírást vagy teljes visszatérítést az ügyfélnek.

## <a name="impact-of-a-recall-request"></a>A visszahívás kérésének hatása

A jóváhagyás visszavonásakor mind működési, mind pénzügyi hatásokkal jár.

### <a name="operational-impact"></a>Működési hatás

Ha egy visszahívási kérelmet jóváhagynak, a jóváhagyási rekordot **Elutasítva** jelöléssel kell ellátni. A bejegyzés állapota megváltozik **Visszatérített** vagy **Elutasított** értékre , attól függően, hogy idő, költség- vagy anyaghasználati bejegyzés van-e.

A projektcsoport tagja megtekintheti a bejegyzéseket, szerkesztheti és újra benyújthatja a bejegyzéseket, vagy teljesen törölheti a bejegyzéseket.

Ha egy visszahívási kérelmet elutasítanak, akkor a bejegyzés állapota továbbra is **Jóváhagyva**, és a bejegyzés nem módosítható a projekt csapattagjának vagy a projekt jóváhagyójának.

### <a name="financial-impact"></a>Pénzügyi hatás

Ha egy visszahívási kérelmet jóváhagynak, a költség és az értékesítés vonatkozó aktuális tényezőit a következő módon frissítik:

- A **Beállítás állapota** mező frissül **Korrigált**-ra.
- A **Számlázás állapota** mező frissül **Megszakítva**-ra.

A következő lépésként létrejönnek a sztornózott bejegyzések a Tényadatok táblában. Sztornózott bejegyzések létrehozásához a rendszer átmásolja az eredeti tényadatok mezőinek értékeit. Csak a minőségi értékek nem lesznek átmásolva. Ezeket az értékeket sztornózza a rendszer. Mind a **Költség**, mind a **Számlázatlan értékesítés** tényadatai esetén létrejönnek sztornózott tényadatok. A **Beállítás állapota** mező **Nem állítható** értékre áll, és a **Számlázási állapot** mező értéke **Megszakítva** lesz. Ezeknek a változásoknak köszönhetően a projektre elszámolt kiadások és bevételmaradás már nem veszi figyelembe az aktuális tényezők által képviselt összegeket.

Ha a visszahívási kérelmet elutasítják, nincs pénzügyi hatása a projektre.

## <a name="changes-to-time-entry-records"></a>Változások az időbejegyzés rekordokban

Az alábbi ábra bemutatja a jóváhagyott időbejegyzéseknél és a kapcsolódó jóváhagyási rekordokat a visszahíváskor bekövetkező változásokat.

![Időbeviteli állapotátmenetek.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>A költség- és anyaghasználati bejegyzések nyilvántartásának változásai

Az alábbi ábra bemutatja a jóváhagyott költség és anyaghasználati bejegyzéseknél és a kapcsolódó jóváhagyási rekordokat a visszahíváskor bekövetkező változásokat.

![Költségbejegyzés állapotátmenetek.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
