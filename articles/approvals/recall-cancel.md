---
title: A korábban jóváhagyott bejegyzések visszahívása
description: Ez a témakör bemutatja, hogy a projektcsapat tagjai hogyan kérhetik a korábban benyújtott és jóváhagyott idő-, költség- és anyaghasználati rekordok visszahívását, valamint azt, hogy a projektmenedzser hogyan hagyhatja jóvá vagy utasíthatja el a visszahívási kérelmeket.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 18796e803ff73806aaa60b453048ee3160406b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586577"
---
# <a name="recall-previously-approved-entries"></a>A korábban jóváhagyott bejegyzések visszahívása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az idő-, költség- vagy anyaghasználati bejegyzést beküldő projektcsapat-tag a jóváhagyás után visszahívhatja ezt a bejegyzést. A visszahívási folyamatnak két fő lépése van:

1. A benyújtó visszahívást kér.
2. A jóváhagyó jóváhagyja a visszahívási kérelmet.

## <a name="request-a-recall"></a>Kérjen visszahívást

Az alábbi lépéseket követve kérheti a jóváhagyott idő-, költség- vagy anyaghasználati bejegyzések visszahívását.

1. A visszahívni kívánt bejegyzés típusától függően hajtsa végre az alábbi lépések egyikét:

    - Időbejegyzések esetén nyissa meg a **Projektek** \> **saját munkaidő** \> **tétel című témakört**, és válassza ki a projekt és a tevékenység adott kombinációjának összes időbejegyzését. Alternatív megoldásként a rácsban válassza ki az egyes cellákat az adott időpontra egy adott dátumra egy adott projekthez.
    - Költségtételek esetén nyissa meg a **Projekt** \> **saját munkaköltsége** \> **lehetőséget**, és válassza ki a visszahívandó költségtétel sorát.
    - Anyaghasználati bejegyzések esetén nyissa meg a **Projektek** \> **saját munkaanyag-használati** \> **naplója című témakört**, és válassza ki a visszahívandó anyaghasználati bejegyzés sorát.

2. Válassza az **Előhívás** lehetőséget. Megjelenik a jóváhagyást kérő párbeszédpanel. Ha a kiválasztott idő-, költség- vagy anyagfelhasználási tételeket már jóváhagyták, a rendszer kéri, hogy adja meg a visszahívás okát.
3. Írja be a visszahívás okát, majd a művelet megerősítéséhez válassza az **OK** lehetőséget. A rendszer kéri a bejegyzés jóváhagyóját a visszahívás jóváhagyására.

> [!IMPORTANT]
> Nem hozhat létre visszahívási kérelmet olyan jóváhagyott időpont-, költség- vagy anyaghasználati tételhez, amelyet már kiszámláztak a vevőnek. Ha megpróbálja, megjelenik egy üzenet, amely szerint az idő-, költség- vagy anyaghasználati bejegyzés nem hívható vissza, mert már kiszámlázták. Ebben az esetben csak akkor kérheti a tétel visszahívását, ha helyesbítő számlát használnak az eredeti számlán szereplő vevő teljes jóváírásának vagy visszatérítésének kibocsátására.

## <a name="approve-or-reject-a-recall-request"></a>A visszahívás jóváhagyása vagy elutasítása

A visszahívás jóváhagyásához vagy elutasításához kövesse ezeket a lépéseket.

1. Válassza a **Projektek** \> **Saját munka** \> **Jóváhagyások** lehetőséget.
2. A **Jóváhagyások** lista oldalon módosítsa a nézetet **Jogosultsági kérelmek előhívása** nézetre. Megjelenik a benyújtott visszahívási kérelmek listája.
3. Válasszon egy vagy több bejegyzést, majd válassza az **Jóváhagyás** vagy az **Elutasítás** lehetőséget.
4. Ha a **Jóváhagyást** választotta, figyelmeztető üzenetet kap, amely elmagyarázza a jóváhagyás hatását. A művelet megerősítéséhez válassza az **OK** lehetőséget. A visszahívási kérelmet jóváhagyják.

    –vagy–

    Ha az **Elutasítás** lehetőséget választotta, akkor a visszahívási kérelmet elutasítják.

> [!IMPORTANT]
> A visszahívás jóváhagyásakor a rendszer ellenőrzi az idő-, költség- vagy anyaghasználati tételek számlázási tevékenységeit. Ha egy tételt már kiszámláztak, vagy ha számlatervezeten van, a jóváhagyó hibaüzenetet kap, amely szerint az idő vagy a költség nem hagyható jóvá visszahívásra, mert már kiszámlázták. Ebben az esetben a jóváhagyó csak akkor hagyhatja jóvá a visszahívást, ha helyesbítő számlát használnak az eredeti számlán szereplő vevő teljes jóváírásának vagy visszatérítésének kibocsátására.

## <a name="impact-of-a-recall-request"></a>A visszahívás kérésének hatása

A jóváhagyás visszavonásakor mind működési, mind pénzügyi hatásokkal jár.

### <a name="operational-impact"></a>Működési hatás

Ha egy visszahívási kérelmet jóváhagynak, a jóváhagyási rekordot **Elutasítva** jelöléssel kell ellátni. A bejegyzés állapota visszaküldött **vagy** elutasított értékre **változik**, attól függően, hogy időbejegyzésről, költség- vagy anyaghasználati tételről van-e szó.

A projektcsapat tagja megtekintheti a bejegyzéseket, szerkesztheti, majd újra elküldheti a bejegyzéseket, vagy teljesen törölheti a bejegyzéseket.

Ha egy visszahívási kérelmet elutasítanak, akkor a bejegyzés állapota továbbra is **Jóváhagyva**, és a bejegyzés nem módosítható a projekt csapattagjának vagy a projekt jóváhagyójának.

### <a name="financial-impact"></a>Pénzügyi hatás

Ha egy visszahívási kérelmet jóváhagynak, a költség és az értékesítés vonatkozó aktuális tényezőit a következő módon frissítik:

- A **Beállítás állapota** mező frissül **Korrigált**-ra.
- A **Számlázás állapota** mező frissül **Megszakítva**-ra.

A következő lépésként létrejönnek a sztornózott bejegyzések a Tényadatok táblában. Sztornózott bejegyzések létrehozásához a rendszer átmásolja az eredeti tényadatok mezőinek értékeit. Csak a minőségi értékek nem lesznek átmásolva. Ezeket az értékeket sztornózza a rendszer. Mind a **Költség**, mind a **Számlázatlan értékesítés** tényadatai esetén létrejönnek sztornózott tényadatok. A **Beállítás állapota** mező **Nem állítható** értékre áll, és a **Számlázási állapot** mező értéke **Megszakítva** lesz. Ezeknek a változásoknak köszönhetően a projektre elszámolt kiadások és bevételmaradás már nem veszi figyelembe az aktuális tényezők által képviselt összegeket.

Ha a visszahívási kérelmet elutasítják, nincs pénzügyi hatása a projektre.

## <a name="changes-to-time-entry-records"></a>Változások az időbejegyzés rekordokban

Az alábbi ábra a jóváhagyott időbejegyzések és a megfelelő jóváhagyási rekordok esetében a visszahívásukkor bekövetkező változásokat mutatja be.

![Időbeviteli állapot átmenetei.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Költség- és anyaghasználati bejegyzési rekordok módosítása

Az alábbi ábra a jóváhagyott költség- és anyagfelhasználási tételeknél bekövetkező változásokat, valamint a megfelelő jóváhagyási rekordokat mutatja be visszahívásukkor.

![Költségbeviteli állapot átmenetei.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
