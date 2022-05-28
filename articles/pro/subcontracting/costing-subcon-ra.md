---
title: Az alvállalkozók erőforrás-hozzárendelései költségeinek becslése
description: Ez a témakör néhány ismertetést tartalmaz, hogy a Microsoft Dynamics 365 Project Operations hogyan számítja ki az alvállalkozói erőforrás-hozzárendelések költségbecslését.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f276e12713261538d1e7520dac17243e578db433
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596697"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Az alvállalkozók erőforrás-hozzárendelései költségeinek becslése

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Az alvállalkozói projektcsapattagok tevékenység-hozzárendelései a **kapcsolódó csapattag-bejegyzés alvállalkozói szerződéséhez csatolt Beszerzési** árlista alapján kerülnek költségszámításra. Ez eltér attól, ahogyan az alkalmazotti erőforrás-hozzárendelések költségszámításra kerülnek, ha az alkalmazotti erőforrások tevékenység-hozzárendelései a **projekt szerződéskötési egységéhez csatolt Költség** árlista alapján kerülnek költségszámításra. 

Az alvállalkozói szerződéssel rendelkező általános projektcsapat-tagok esetében a hozzárendelések költsége az alvállalkozóhoz csatolt beszerzési árlista szerepköralapú árbeállítása alapján történik. A beszerzési árakat az egyes erőforrásokhoz is be lehet állítani. Ezek az erőforrás-specifikus árak elsőbbséget élveznek, ha a megnevezett projektcsapattagok tevékenység-hozzárendeléseinek költségszámítása szerződéses dolgozók. 

A szerepkör-specifikus beszerzési ár és az erőforrás-specifikus használatának prioritását a Díjszabási dimenzió prioritásának beállítása határozza meg a Paraméterek > összegalapú árképzési **dimenziókban**.

Az alvállalkozók beszerzési árainak dimenzióbeállításán alapuló dinamikusan levezetett árak ez a funkciója hasonló ahhoz, ahogyan a teljes munkaidőben foglalkoztatottak költség- és számlaárai származnak. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Feladat-hozzárendelések létrehozása alvállalkozói erőforrások költségbecslésének lekéréséhez

Az alvállalkozók feladat-hozzárendelései kétféleképpen hozhatók létre: 
- **A Feladatok** lap használata.
- **A Csapat** lap használata.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Erőforrás-hozzárendelések létrehozása a Feladatok lapon
**Egy adott tevékenység Tevékenységek** lapjának **Erőforrások** listájával létrehozhat egy elnevezett erőforráshoz vagy egy általános erőforráshoz tevékenység-hozzárendelést. Ha kiválaszt egy elnevezett erőforrást a **tevékenység Hozzárendelt erőforrások** legördülő listájából, és ez az erőforrás szerződéses dolgozó, a program hozzárendeli a megnevezett erőforrást a tevékenységhez, és létrejön egy megfelelő projektcsapat-tagrekord, amelynek dolgozótípusa **Szerződési dolgozó** és **Érvényessége** **érvénytelen**. Következő lépésként meg kell nyitnia a projektcsapat-tag bejegyzését, és ki kell választania egy alvállalkozói és alvállalkozói sort. Ezzel frissíti a tevékenység-hozzárendelést, hogy hivatkozás legyen az alvállalkozói és alvállalkozói sorra, és a csapattag állapotát érvényesre **is** frissíti.

Ha úgy dönt, hogy általános csapattagot hoz létre a **tevékenység Hozzárendelt erőforrások** legördülő listájából, az **Általános csapattag-létrehozás** párbeszédpanel lehetővé teszi alvállalkozói és alvállalkozói sor kiválasztását. Amikor az általános erőforrás hozzá van rendelve a tevékenységhez, és létrejön a megfelelő projektcsapattag-bejegyzés, észre fogja venni, hogy a projektcsapattag-bejegyzés úgy jön létre, hogy **a dolgozó típusa Szerződés dolgozói** típusú, az érvényességi állapot **pedig** **Érvényes**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Projektcsapattagok létrehozása a Csapat lapon
A projekt Csapat lapján létrehozhat egy általános vagy egy megnevezett csapattagot. A csapattag létrehozásakor kiválaszthatja az alvállalkozói és alvállalkozói sort. A csapattag létrehozása után a csoporttagot hozzá kell rendelnie egy tevékenységhez a **tevékenység Hozzárendelt erőforrások** legördülő listájával. 

## <a name="updating-estimates"></a>Becslések frissítése
Miután hozzárendelte a projektcsapat tagjait a tevékenységekhez, el kell navigálnia a **projekt Becslések** lapjára, és ki kell választania az Árak **frissítése lehetőséget** annak biztosítása érdekében, hogy az alvállalkozói erőforrás-hozzárendelések költségarányai az alvállalkozói szerződéshez csatolt beszerzési árlista alapján frissüljenek. A Microsoft Dynamics 365 Project Operations nem hoz létre becsléseket a ki nem osztott feladatokhoz. Ennek eredményeként tevékenység-hozzárendeléseket kell létrehoznia a projekt különböző tevékenységeinek árához és költségéhez. 

> [MEGJEGYZÉS!] Azok a projektcsapat-tagok, akik dolgozótípussal rendelkeznek **szerződéses dolgozóként** **, de nem rendelkeznek alvállalkozói hivatkozással, érvénytelenként** **vannak megjelölve a** Projektcsapat tagjai **rácson.** Ha vannak ilyen állapotú projektcsapat-tagok, nyissa meg a projektcsapat-tagbejegyzést, és manuálisan frissítse az alvállalkozói és alvállalkozói sormezőket úgy, hogy a pénzügyi költségbecslés pontosan tükrözze az alvállalkozói költséget a **Becslések** lapon. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
