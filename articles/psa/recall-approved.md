---
title: Emlékezzen a jóváhagyott idő- vagy költségbejegyzésre
description: Ez a témakör információkat tartalmaz egy korábban jóváhagyott idő- vagy költségügylet visszahívásáról.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 102da39d5940874a8e1f4220437ecdf386a7187b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120546"
---
# <a name="recall-approved-time-or-expense-entries"></a>Emlékezzen a jóváhagyott idő- vagy költségbejegyzésre

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A projektcsoport tagja vagy más személy, aki benyújt egy idő- vagy költségbejegyzést, visszavonhatja azt az idő- vagy költségszámítást, miután azt jóváhagyták. A jóváhagyott idő- vagy költségbejegyzés visszahívásának két lépése van:

1. A benyújtó visszahívást kér.
2. A visszahívást jóváhagyó személy hagyja jóvá.

## <a name="request-a-recall"></a>Kérjen visszahívást

Kövesse ezeket a lépéseket egy jóváhagyott idő- vagy költségbejegyzés visszahívásának kérésére.

1. Időbeírásokhoz lépjen a **Projektek** \> **Saját munka** \> **Időbevitel** oldalba.

    –vagy–

    Költségbejegyzéshez lépjen a **Projektek** \> **Saját munka**\> **Kiadások** oldalra.

2. Időbeírásokhoz válassza ki az összes időbejegyzést a projekt és a feladat egy adott kombinációjára. Alternatív megoldásként a rácsban válassza ki az egyes cellákat az adott időpontra egy adott dátumra egy adott projekthez.

    –vagy–

    Költségbejegyzés esetén válassza ki a visszahívandó költségbejegyzés sorát.

3. Válassza az **Előhívás** lehetőséget. Megjelenik a jóváhagyást kérő párbeszédpanel. Ha a kiválasztott idő- és költségbejegyzéseket már jóváhagyták, a rendszer kéri, hogy írja be a visszahívás okát.
4. Írja be a visszahívás okát, majd a művelet megerősítéséhez válassza az **OK** lehetőséget. A rendszer kéri a bejegyzés jóváhagyóját a visszahívás jóváhagyására.

> [!NOTE]
> Noha a jóváhagyott idő- és költségbejegyzés visszahívható, ha egy jóváhagyott időt vagy költséget már számláztak az ügyfélnek, visszahívási kérelmet nem lehet létrehozni. Az a felhasználó, aki megkísérel létrehozni visszahívási kérelmet, üzenetet kap, amelyben kijelenti, hogy az időt vagy a költségeket nem lehet visszahívni, mert már kiszámlázásra került.

## <a name="approve-or-reject-a-recall-request"></a>A visszahívás jóváhagyása vagy elutasítása

A visszahívás jóváhagyásához vagy elutasításához kövesse ezeket a lépéseket.

1. Válassza a **Projektek** \> **Saját munka** \> **Jóváhagyások** lehetőséget.
2. A **Jóváhagyások** lista oldalon módosítsa a nézetet **Jogosultsági kérelmek előhívása** nézetre. Megjelenik a benyújtott visszahívási kérelmek listája.
3. Válasszon egy vagy több bejegyzést, majd válassza az **Jóváhagyás** vagy az **Elutasítás** lehetőséget.
4. Ha a **Jóváhagyást** választotta, figyelmeztető üzenetet kap, amely elmagyarázza a jóváhagyás hatását. A művelet megerősítéséhez válassza az **OK** lehetőséget. A visszahívási kérelmet jóváhagyják.

    –vagy–

    Ha az **Elutasítás** lehetőséget választotta, akkor a visszahívási kérelmet elutasítják.

> [!NOTE]
> Csakúgy, amikor visszahívást kérnek, akkor is, amikor a visszahívást jóváhagyják, a rendszer ellenőrzi az esetleges számlázási tevékenységeket az idő- vagy költségbejegyzésen. Ha egy bejegyzésre már számláztak, vagy ha számlatervezetről van szó, akkor a jóváhagyó hibaüzenetet fog kapni, amely kijelenti, hogy az időt vagy a költségeket nem lehet jóváhagyni a visszahíváshoz, mert már számláztak.

## <a name="impact-of-a-recall-request"></a>A visszahívás kérésének hatása

A jóváhagyás visszavonásakor mind működési, mind pénzügyi hatásokkal jár.

### <a name="operational-impact"></a>Működési hatás

Ha egy visszahívási kérelmet jóváhagynak, a jóváhagyási rekordot **Elutasítva** jelöléssel kell ellátni. A bejegyzés állapota megváltozik **Visszatérített** vagy **Elutasított** értékre , attól függően, hogy időbejegyzés vagy költségbejegyzés van-e.

A projektcsoport tagja megtekintheti a bejegyzéseket, szerkesztheti és újra benyújthatja a bejegyzéseket, vagy teljes egészében törölheti a bejegyzéseket.

Ha egy visszahívási kérelmet elutasítanak, akkor a bejegyzés állapota továbbra is **Jóváhagyva**, és a bejegyzés nem módosítható a projekt csapattagjának vagy a projekt jóváhagyójának.

### <a name="financial-impact"></a>Pénzügyi hatás

Ha egy visszahívási kérelmet jóváhagynak, a költség és az értékesítés vonatkozó aktuális tényezőit a következő módon frissítik:

- A **Beállítás állapota** mező frissül **Korrigált**-ra.
- A **Számlázás állapota** mező frissül **Megszakítva**-ra.

A következő lépésként létrejönnek a sztornózott bejegyzések a Tényadatok táblában. Sztornózott bejegyzések létrehozásához a rendszer átmásolja az eredeti tényadatok mezőinek értékeit. Csak a minőségi értékek nem lesznek átmásolva. Ezeket az értékeket sztornózza a rendszer. Mind a **Költség**, mind a **Számlázatlan értékesítés** tényadatai esetén létrejönnek sztornózott tényadatok. A **Beállítás állapota** mező **Nem állítható** értékre áll, és a **Számlázási állapot** mező értéke **Megszakítva** lesz. Ezeknek a változásoknak köszönhetően a projektre elszámolt kiadások és bevételmaradás már nem veszi figyelembe az aktuális tényezők által képviselt összegeket.

Ha a visszahívási kérelmet elutasítják, nincs pénzügyi hatása a projektre.

## <a name="changes-to-time-entry-records"></a>Változások az időbejegyzés rekordokban

Az alábbi ábra bemutatja a jóváhagyott időbejegyzéseknél a visszahíváskor bekövetkező változásokat.

![Időbeviteli állapotátmenetek](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>A költségbejegyzés nyilvántartásának változásai

Az alábbi ábra bemutatja azokat a változásokat, amelyek a jóváhagyott kiadási tételeknél történnek visszahívásukkor.

![Költség belépési állapotátmenetek](media/ExpenseEntryStateTransitions.png)
