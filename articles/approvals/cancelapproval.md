---
title: A korábban jóváhagyott bejegyzések jóváhagyásának visszavonása
description: Ez a cikk azt ismerteti, hogy a projektmenedzser hogyan vonhatja vissza a korábban jóváhagyott idő-, költség- vagy anyaghasználati bejegyzések jóváhagyását.
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
# <a name="cancel-the-approval-of-previously-approved-entries"></a>A korábban jóváhagyott bejegyzések jóváhagyásának visszavonása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az a projektmenedzser vagy jóváhagyó, aki korábban jóváhagyta az idő-, költség- vagy anyaghasználati bejegyzéseket, visszavonhatja a bejegyzések jóváhagyását. 

Kövesse az alábbi lépéseket egy korábban jóváhagyott idő-, költség- vagy anyaghasználati bejegyzés jóváhagyásának visszavonásához.

1. Válassza a **Projektek** \> **Saját munka** \> **Jóváhagyások** lehetőséget.
2. A **Jóváhagyások** listaoldalon megjelenik az összes jóváhagyásra váró időbejegyzés. Módosítsa a nézetet a **Saját korábbi jóváhagyások értékre**.
3. Válassza ki a törölni kívánt időt, költséget vagy anyag-jóváhagyásokat. Ezután a Műveleti ablaktáblán válassza a Jóváhagyás megszakítása **lehetőséget**.
4. A megjelenő megerősítő üzenet mezőben kattintson az OK gombra **a** művelet megerősítéséhez.

> [!IMPORTANT]
> Nem vonhatja vissza a korábban jóváhagyott idő-, költség- és anyaghasználati bejegyzések jóváhagyását, amelyeket már kiszámláztak a vevőnek. Ha megpróbálja, egy üzenet jelenik meg, amely szerint a jóváhagyás nem vonható le, mert már ki volt számlázva. Ebben az esetben csak akkor törölheti a jóváhagyást, ha helyesbítő számlát használ a teljes jóváírás vagy visszatérítés kiadására a vevőnek az eredeti számlán.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Egy korábban jóváhagyott bejegyzés jóváhagyásának visszavonásának hatása

A jóváhagyás visszavonása esetén a működési hatás és a pénzügyi hatás egyaránt fennáll.

### <a name="operational-impact"></a>Működési hatás

Ha egy bejegyzés jóváhagyását visszavonják, a jóváhagyási rekord elküldve **állapotúként** lesz megjelölve. A bejegyzés állapota Elküldve **állapotra** változik. Ebben a szakaszban a projektcsapat tagja visszahívhatja a bejegyzést anélkül, hogy visszahívási kérelmet küldene.

A jóváhagyó módosíthatja a Számlázható mennyiség és a **Számlázási típus** értékét, majd még egyszer jóváhagyhatja a bejegyzést **.**

### <a name="financial-impact"></a>Pénzügyi hatás

Ha egy bejegyzés jóváhagyását visszavonják, a költségekre és az értékesítésekre vonatkozó megfelelő tényleges adatokat a következő módon frissítik:

- A **Beállítás állapota** mező frissül **Korrigált**-ra.
- A **Számlázás állapota** mező frissül **Megszakítva**-ra.

A következő lépésként létrejönnek a sztornózott bejegyzések a Tényadatok táblában. Sztornózott bejegyzések létrehozásához a rendszer átmásolja az eredeti tényadatok mezőinek értékeit. Csak a minőségi értékek nem lesznek átmásolva. Ezeket az értékeket sztornózza a rendszer. Mind a **Költség**, mind a **Számlázatlan értékesítés** tényadatai esetén létrejönnek sztornózott tényadatok. A **Beállítás állapota** mező **Nem állítható** értékre áll, és a **Számlázási állapot** mező értéke **Megszakítva** lesz. Ezeknek a változásoknak köszönhetően a projektre elszámolt kiadások és bevételmaradás már nem veszi figyelembe az aktuális tényezők által képviselt összegeket.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
