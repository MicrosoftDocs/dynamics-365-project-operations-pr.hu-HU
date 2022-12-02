---
title: Jóváhagyás visszavonása korábban jóváhagyott bejegyzéseken
description: Ez a cikk ismerteti, hogyan tudja a projektvezető visszavonni a korábban jóváhagyott időpontok, kiadások vagy anyaghasználati tételek jóváhagyását.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 08c2248a5fcfc9b7569871a76bc09234ffd172c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930459"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Jóváhagyás visszavonása korábban jóváhagyott bejegyzéseken

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A projektvezető vagy jóváhagyó, aki korábban jóváhagyott időpontok, kiadások vagy anyaghasználati tételeket, visszavonhatja ezeknek a bejegyzéseknek a jóváhagyását. 

Az alábbi lépéseket kövesse a korábban jóváhagyott idő- vagy anyaghasználati bejegyzés jóváhagyásának visszavonásához.

1. Válassza a **Projektek** \> **Saját munka** \> **Jóváhagyások** lehetőséget.
2. A **Jóváhagyások** listaoldal megjeleníti az összes olyan időbejegyzést, amely jóváhagyásra vár. Változtassa meg a nézetet a **Saját múltbeli jóváhagyások** nézetre.
3. Adja meg a visszavonni kívánt idő, költség vagy anyagjóváhagyásokat. Válassza a **Jóváhagyás visszavonása** elemet a műveleti panelen.
4. A megjelenő megerősítő üzenetben válassza a **OK** lehetőséget a művelet megerősítéséhez.

> [!IMPORTANT]
> Nem visszavonhatja olyan, korábban jóváhagyott időpont, költség és anyaghasználati tétel jóváhagyását, amely már ki lett számlázva az ügyfélnek. Ha megpróbálja, egy üzenet jelenik meg, amely szerint a jóváhagyás nem vonható vissza, mert már ki van számlázva. Ebben az esetben a jóváhagyást csak akkor lehet visszavonni, ha az eredeti számlához egy helyesbítő számlával ad jóváírást vagy teljes visszatérítést az ügyfélnek.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Egy korábban jóváhagyott bejegyzés visszavonásának hatása

A jóváhagyás visszavonása esetén a működési hatás és a pénzügyi hatás egyaránt fennáll.

### <a name="operational-impact"></a>Működési hatás

Ha egy bejegyzés jóváhagyását visszavonják, a jóváhagyás rekordja **Beküldve** értékkel lesz megjelölve. A bejegyzés állapota **Beküldve** állapotúra változik. Ebben a fázisban a projektcsoport tagja kérelem benyújtása nélkül vissza tudja hívni a bejegyzést.

A jóváhagyó módosíthatja a **Számlázható mennyiség** és **Számlázás típusa** értékeket, majd a bejegyzést még egyszer jóváhagyhatja.

### <a name="financial-impact"></a>Pénzügyi hatás

Ha egy bejegyzés jóváhagyását visszavonják, a költség és az értékesítés vonatkozó aktuális tényezőit a következő módon frissítik:

- A **Beállítás állapota** mező frissül **Korrigált**-ra.
- A **Számlázás állapota** mező frissül **Megszakítva**-ra.

A következő lépésként létrejönnek a sztornózott bejegyzések a Tényadatok táblában. Sztornózott bejegyzések létrehozásához a rendszer átmásolja az eredeti tényadatok mezőinek értékeit. Csak a minőségi értékek nem lesznek átmásolva. Ezeket az értékeket sztornózza a rendszer. Mind a **Költség**, mind a **Számlázatlan értékesítés** tényadatai esetén létrejönnek sztornózott tényadatok. A **Beállítás állapota** mező **Nem állítható** értékre áll, és a **Számlázási állapot** mező értéke **Megszakítva** lesz. Ezeknek a változásoknak köszönhetően a projektre elszámolt kiadások és bevételmaradás már nem veszi figyelembe az aktuális tényezők által képviselt összegeket.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
