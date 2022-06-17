---
title: Korábban jóváhagyott bejegyzések visszahívása
description: Ez a cikk azt ismerteti, hogy a projektcsapat tagjai hogyan kérhetik a korábban beküldött és jóváhagyott idő-, költség- és anyaghasználati rekordok visszahívását, és hogyan hagyhatják jóvá vagy utasíthatják el a projektmenedzser a visszahívási kérelmeket.
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

A projektcsapat azon tagja, aki idő-, költség- vagy anyaghasználati bejegyzést küld be, a jóváhagyás után visszahívhatja a bejegyzést. A visszahívási folyamatnak két fő lépése van:

1. A benyújtó visszahívást kér.
2. A jóváhagyó jóváhagyja a visszahívási kérelmet.

## <a name="request-a-recall"></a>Kérjen visszahívást

Kövesse az alábbi lépéseket a jóváhagyott idő-, költség- vagy anyaghasználati bejegyzések visszahívásának kéréséhez.

1. Kövesse az alábbi lépések egyikét attól függően, hogy milyen típusú bejegyzést szeretne visszahívni:

    - Időbejegyzések esetén lépjen a **Projektek**\> saját munkaidő-bejegyzése **·** \> **lapra**, és válassza ki a projekt és a tevékenység adott kombinációjának összes időbejegyzését. Alternatív megoldásként a rácsban válassza ki az egyes cellákat az adott időpontra egy adott dátumra egy adott projekthez.
    - Költségbejegyzések esetén lépjen a **Projektek**\> saját **munkaköltségei** \> **lapra**, és válassza ki a visszahívni kívánt költségbejegyzés sorát.
    - Az anyaghasználati bejegyzésekhez lépjen a **Projektek**\> saját munkaanyag-használati **·**\> naplója **oldalra**, és válassza ki a visszahívni kívánt anyaghasználati bejegyzés sorát.

2. Válassza az **Előhívás** lehetőséget. Megjelenik a jóváhagyást kérő párbeszédpanel. Ha a kiválasztott idő-, költség- vagy anyaghasználati bejegyzéseket már jóváhagyták, a rendszer kéri, hogy adja meg a visszahívás okát.
3. Írja be a visszahívás okát, majd a művelet megerősítéséhez válassza az **OK** lehetőséget. A rendszer kéri a bejegyzés jóváhagyóját a visszahívás jóváhagyására.

> [!IMPORTANT]
> Nem hozhat létre visszahívási kérelmet olyan jóváhagyott idő-, költség- vagy anyaghasználati bejegyzéshez, amelyet már kiszámláztak a vevőnek. Ha megpróbálja, olyan üzenetet kap, amely szerint az idő-, költség- vagy anyaghasználati bejegyzés nem hívható vissza, mert már számlázták. Ebben az esetben csak akkor kérheti a bejegyzés visszahívását, ha helyesbítő számlát használnak a teljes jóváírás vagy visszatérítés kiadására az eredeti számlán szereplő vevőnek.

## <a name="approve-or-reject-a-recall-request"></a>A visszahívás jóváhagyása vagy elutasítása

A visszahívás jóváhagyásához vagy elutasításához kövesse ezeket a lépéseket.

1. Válassza a **Projektek** \> **Saját munka** \> **Jóváhagyások** lehetőséget.
2. A **Jóváhagyások** lista oldalon módosítsa a nézetet **Jogosultsági kérelmek előhívása** nézetre. Megjelenik a benyújtott visszahívási kérelmek listája.
3. Válasszon egy vagy több bejegyzést, majd válassza az **Jóváhagyás** vagy az **Elutasítás** lehetőséget.
4. Ha a **Jóváhagyást** választotta, figyelmeztető üzenetet kap, amely elmagyarázza a jóváhagyás hatását. A művelet megerősítéséhez válassza az **OK** lehetőséget. A visszahívási kérelmet jóváhagyják.

    –vagy–

    Ha az **Elutasítás** lehetőséget választotta, akkor a visszahívási kérelmet elutasítják.

> [!IMPORTANT]
> A visszahívás jóváhagyásakor, csakúgy, mint amikor azt kérik, a rendszer ellenőrzi, hogy vannak-e számlázási tevékenységek az idő-, költség- vagy anyaghasználati bejegyzéseken. Ha egy bejegyzés már ki lett számlázva, vagy ha az szerepel egy számlavázlaton, a jóváhagyó hibaüzenetet kap, amely szerint az idő vagy a költség nem hagyható jóvá visszahívásra, mert már kiszámlázták. Ebben az esetben a jóváhagyó csak akkor hagyhatja jóvá a visszahívást, ha helyesbítő számlát használ a teljes jóváírás vagy visszatérítés kiadására az eredeti számlán szereplő vevőnek.

## <a name="impact-of-a-recall-request"></a>A visszahívás kérésének hatása

A jóváhagyás visszavonásakor mind működési, mind pénzügyi hatásokkal jár.

### <a name="operational-impact"></a>Működési hatás

Ha egy visszahívási kérelmet jóváhagynak, a jóváhagyási rekordot **Elutasítva** jelöléssel kell ellátni. A bejegyzés állapota Visszaadva **vagy** Elutasítva **állapotra** változik, attól függően, hogy időbemenetről, költség- vagy anyaghasználati bejegyzésről van-e szó.

A projektcsapat tagja megtekintheti a bejegyzéseket, szerkesztheti, majd újra elküldheti a bejegyzéseket, vagy teljesen törölheti a bejegyzéseket.

Ha egy visszahívási kérelmet elutasítanak, akkor a bejegyzés állapota továbbra is **Jóváhagyva**, és a bejegyzés nem módosítható a projekt csapattagjának vagy a projekt jóváhagyójának.

### <a name="financial-impact"></a>Pénzügyi hatás

Ha egy visszahívási kérelmet jóváhagynak, a költség és az értékesítés vonatkozó aktuális tényezőit a következő módon frissítik:

- A **Beállítás állapota** mező frissül **Korrigált**-ra.
- A **Számlázás állapota** mező frissül **Megszakítva**-ra.

A következő lépésként létrejönnek a sztornózott bejegyzések a Tényadatok táblában. Sztornózott bejegyzések létrehozásához a rendszer átmásolja az eredeti tényadatok mezőinek értékeit. Csak a minőségi értékek nem lesznek átmásolva. Ezeket az értékeket sztornózza a rendszer. Mind a **Költség**, mind a **Számlázatlan értékesítés** tényadatai esetén létrejönnek sztornózott tényadatok. A **Beállítás állapota** mező **Nem állítható** értékre áll, és a **Számlázási állapot** mező értéke **Megszakítva** lesz. Ezeknek a változásoknak köszönhetően a projektre elszámolt kiadások és bevételmaradás már nem veszi figyelembe az aktuális tényezők által képviselt összegeket.

Ha a visszahívási kérelmet elutasítják, nincs pénzügyi hatása a projektre.

## <a name="changes-to-time-entry-records"></a>Változások az időbejegyzés rekordokban

A következő ábra a jóváhagyott időbejegyzések és a visszahívásukkor a megfelelő jóváhagyási rekordok esetében bekövetkező változásokat mutatja be.

![Időbeviteli állapotátalakulások.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>A költség- és anyaghasználati bejegyzési rekordok változásai

Az alábbi ábra a jóváhagyott költség- és anyaghasználati bejegyzések, valamint a visszahíváskor a megfelelő jóváhagyási rekordokkal kapcsolatos változásokat mutatja be.

![Költségbeviteli állapotátalakulások.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
