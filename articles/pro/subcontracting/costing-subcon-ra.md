---
title: Az alvállalkozók erőforrás-hozzárendelései költségeinek becslése
description: Ez a cikk néhányat ismertet, hogyan számítja ki a Microsoft Dynamics 365 Project Operations az alvállalkozói erőforrás-hozzárendelések költségbecslését.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a4d0707f8373b5083272eacb7dc1318e82a23ac
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262062"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Az alvállalkozók erőforrás-hozzárendelései költségeinek becslése

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Az alvállalkozói projektcsapat tagjainak feladat-hozzárendelései a **kapcsolódó csapattagrekordban az alvállalkozóhoz csatolt Beszerzési** ár lista használatával kerülnek költségre. Ez eltér attól, ahogyan az alkalmazottak erőforrás-hozzárendeléseinek költségesek, ahol az alkalmazotti erőforrások tevékenység-hozzárendelései a **projekt szerződéses egységéhez csatolt Önköltségi** árlista használatával kerülnek költségre. 

Az alvállalkozásba adott általános projektcsapat-tagok esetében a hozzárendelések költsége egy szerepköralapú árbeállítással történik az alvállalkozói szerződéshez csatolt beszerzési árlistában. A beszerzési árak kifejezetten az egyes erőforrásokhoz is beállíthatók. Ezek az erőforrás-specifikus árak elsőbbséget élveznek, ha a megnevezett projektcsapat tagjainak költség-hozzárendeléseinek költségszámítása szerződéses dolgozók. 

A szerepkör-specifikus vételár használatának az erőforrás-specifikushoz viszonyított prioritását a díjszabási dimenzió prioritásának beállítása vezérli a Paraméterek > összegalapú árképzési **dimenziókban**.

Az alvállalkozók beszerzési árainak dimenzióbeállításán alapuló dinamikusan levezethető árak dinamikus levezetésének ez a funkciója hasonló ahhoz, ahogyan a teljes munkaidőben foglalkoztatottak költség- és számladíjait levezetik. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Tevékenység-hozzárendelések létrehozása az alvállalkozói erőforrások költségbecslésének lekéréséhez

Az alvállalkozók számára a feladat-hozzárendelések kétféleképpen hozhatók létre: 
- **A Feladatok** lap használata.
- **A Csapat** lap használata.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Erőforrás-hozzárendelések létrehozása a Feladatok lappal
**Egy adott tevékenység Tevékenységek** lapján található **Erőforrások** lista használatával tevékenység-hozzárendelést hozhat létre egy elnevezett erőforráshoz vagy egy általános erőforráshoz. Ha kiválaszt egy elnevezett erőforrást a **tevékenység Hozzárendelt erőforrások** legördülő listájából, és ez az erőforrás szerződéses dolgozó, a rendszer hozzárendeli az elnevezett erőforrást a tevékenységhez, és létrejön egy megfelelő projektcsapat-tagrekord, amelynek feldolgozói típusa Szerződés dolgozóra **, érvényessége** pedig **Érvénytelen** értékre **van állítva**. Következő lépésként meg kell nyitnia a projektcsapat tagrekordját, és ki kell választania egy alvállalkozói és alvállalkozói vonalat. Ez frissíti a feladat-hozzárendelést, hogy hivatkozással rendelkezzen az alvállalkozói és alvállalkozói sorra, és a csapattag állapotát is érvényesre **frissíti**.

Ha úgy dönt, hogy általános csapattagot hoz létre a **feladat Hozzárendelt erőforrások** legördülő menüből, az **Általános csapattagok létrehozása** párbeszédpanelen kiválaszthatja az alvállalkozói és alvállalkozói sort. Amikor az általános erőforrás hozzá van rendelve a tevékenységhez, és létrejön a megfelelő projektcsapattag-rekord, észre fogja venni, hogy a projektcsapattag-rekord úgy jön létre, hogy a dolgozó típusa Szerződés-feldolgozó és **Érvényes értékre** van **állítva**.**·**

### <a name="creating-project-team-members-using-the-team-tab"></a>Projektcsapattagok létrehozása a Csapat lapon
A projekt Csapat lapján létrehozhat egy általános vagy egy megnevezett csapattagot. A csapattag létrehozásakor kiválaszthatja az alvállalkozói és alvállalkozói sort. A csapattag létrehozása után hozzá kell rendelnie a csapattagot egy tevékenységhez a **feladat Hozzárendelt erőforrások** legördülő menüpontjában. 

## <a name="updating-estimates"></a>Becslések frissítése
Miután hozzárendelte a projektcsapat tagjait a **tevékenységekhez, a projekt Becslés** lapjára kell navigálnia, és ki kell választania az Árak **frissítése lehetőséget** annak biztosításához, hogy az alvállalkozói erőforrás-hozzárendelések költségarányai az alvállalkozói alvállalkozáshoz csatolt beszerzési árlista alapján frissüljenek. A becslések nem jönnek létre a nem hozzárendelt feladatokhoz a Microsoftban Dynamics 365 Project Operations. Ennek eredményeképpen tevékenység-hozzárendeléseket kell létrehoznia a projekt különböző tevékenységeinek árazásához és költségéhez. 

> [MEGJEGYZÉS!] Azok a projektcsapat-tagok, akik feldolgozó típusú szerződéssel rendelkező **feldolgozói** **típusúak**, de nem rendelkeznek alvállalkozói referenciával, érvénytelenként **vannak** megjelölve a **Projektcsapat tagjai** rácsban. Ha vannak ilyen állapotú projektcsapat-tagok, nyissa meg a projektcsapat tagjainak rekordját, és manuálisan frissítse az alvállalkozói és alvállalkozói sor mezőket, hogy a pénzügyi költségbecslés pontosan tükrözze az alvállalkozói költséget a **Becslések** lapon. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
