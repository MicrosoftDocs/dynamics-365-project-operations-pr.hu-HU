---
title: A korábban jóváhagyott bejegyzések jóváhagyásának visszavonása
description: Ez a témakör bemutatja, hogy a projektmenedzser hogyan törölheti meg a korábban jóváhagyott idő-, költség- vagy anyaghasználati tételek jóváhagyását.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584783"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>A korábban jóváhagyott bejegyzések jóváhagyásának visszavonása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az a projektmenedzser vagy jóváhagyó, aki korábban jóváhagyta az idő-, költség- vagy anyaghasználati tételeket, visszavonhatja a bejegyzések jóváhagyását. 

Az alábbi lépéseket követve visszavonhatja egy korábban jóváhagyott idő-, költség- vagy anyaghasználati bejegyzés jóváhagyását.

1. Válassza a **Projektek** \> **Saját munka** \> **Jóváhagyások** lehetőséget.
2. A **Jóváhagyások** listalapon minden jóváhagyásra váró bejegyzés látható. Módosítsa a nézetet **Saját korábbi jóváhagyásokra**.
3. Válassza ki a visszavonandó időt, költséget vagy anyagjóváhagyást. Ezután a Művelet ablaktáblán válassza a Jóváhagyás visszavonása **lehetőséget**.
4. A megjelenő megerősítő üzenetmezőben válassza az OK **lehetőséget** a művelet megerősítéséhez.

> [!IMPORTANT]
> Nem szakíthatja meg a vevőnek már számlázott, korábban jóváhagyott idő-, költség- és anyaghasználati tétel jóváhagyását. Ha megpróbálja, megjelenik egy üzenet, amely kimondja, hogy a jóváhagyás nem vonható vissza, mert már kiszámlázták. Ebben az esetben csak akkor mondhatja vissza a jóváhagyást, ha helyesbítő számlát használnak az eredeti számlán szereplő vevő teljes jóváírásának vagy visszatérítésének kibocsátására.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Egy korábban jóváhagyott bejegyzés jóváhagyásának visszavonásának hatása

A jóváhagyás visszavonása esetén a működési hatás és a pénzügyi hatás egyaránt fennáll.

### <a name="operational-impact"></a>Működési hatás

Ha egy bejegyzés jóváhagyását visszavonják, a jóváhagyási rekord elküldve jelöléssel **lesz megjelölve**. A bejegyzés állapota Elküldve értékre **változik**. Ebben a szakaszban a projektcsapat tagja visszahívási kérelem benyújtása nélkül is visszahívhatja a bejegyzést.

A jóváhagyó módosíthatja a Számlázható mennyiség **és** a **Számlázási típus** értékeit, majd még egyszer jóváhagyhatja a bejegyzést.

### <a name="financial-impact"></a>Pénzügyi hatás

Ha egy tétel jóváhagyását visszavonják, a költség és az értékesítés megfelelő tényleges értéke a következőképpen frissül:

- A **Beállítás állapota** mező frissül **Korrigált**-ra.
- A **Számlázás állapota** mező frissül **Megszakítva**-ra.

A következő lépésként létrejönnek a sztornózott bejegyzések a Tényadatok táblában. Sztornózott bejegyzések létrehozásához a rendszer átmásolja az eredeti tényadatok mezőinek értékeit. Csak a minőségi értékek nem lesznek átmásolva. Ezeket az értékeket sztornózza a rendszer. Mind a **Költség**, mind a **Számlázatlan értékesítés** tényadatai esetén létrejönnek sztornózott tényadatok. A **Beállítás állapota** mező **Nem állítható** értékre áll, és a **Számlázási állapot** mező értéke **Megszakítva** lesz. Ezeknek a változásoknak köszönhetően a projektre elszámolt kiadások és bevételmaradás már nem veszi figyelembe az aktuális tényezők által képviselt összegeket.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
