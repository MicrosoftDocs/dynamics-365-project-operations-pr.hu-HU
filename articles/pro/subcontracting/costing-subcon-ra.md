---
title: Alvállalkozói erőforrás-hozzárendelések költségbecslése
description: Ez a témakör néhány, a Microsoft Dynamics 365 Project Operations hogyan számítja ki az alvállalkozói erőforrás-hozzárendelések költségbecslését.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 09a2a86ea0e97376939d5bff6df9177747818ebb
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903675"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Alvállalkozói erőforrás-hozzárendelések költségbecslése

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Az alvállalkozó projektcsapat tagjainak feladat-hozzárendelései a **kapcsolódó** csapattag-rekord alvállalkozóihoz csatolt beszerzési árlistájának felhasználásával kerülnek költségszámításra. Ez eltér attól, ahogyan az alkalmazotti erőforrás-hozzárendelések költsége történik, ha az alkalmazotti erőforrások tevékenység-hozzárendeléseit a **projekt** szerződésezési egységéhez csatolt Önköltségi árlista használatával kerülik költségszámításra. 

Az alvállalkozásba adott általános projektcsapattagok esetében a hozzárendelések költsége az alvállalkozóhoz csatolt beszerzési árlista szerepköralapú árbeállításával történik. A beszerzési árak kifejezetten az egyes erőforrásokhoz is beállíthatók. Ezek az erőforrás-specifikus árak elsőbbséget élveznek, ha a megnevezett projektcsapattagok tevékenység-hozzárendelései szerződéses munkavállalók. 

A szerepkör-specifikus beszerzési ár és az erőforrás-specifikus alkalmazás prioritásának prioritását a **Paraméterek > az összegalapú díjszabási dimenziók árképzési dimenzióinak beállítása vezérli**.

Az alvállalkozók beszerzési árainak dimenzióbeállításán alapuló dinamikusan levezethető áraknak ez a funkciója hasonló ahhoz, ahogyan a teljes munkaidőben foglalkoztatottak költség- és számladíjai származnak. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Tevékenység-hozzárendelések létrehozása az alvállalkozói erőforrások költségbecslésének beszerzéséhez

Az alvállalkozóknak szánt feladat-hozzárendelések kétféleképpenhatók létre: 
- A **Feladatok** lap használata.
- A **Csapat** fül használatával.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Erőforrás-hozzárendelések létrehozása a Tevékenységek lap használatával
Egy **adott tevékenység Tevékenységek lapján található Erőforrások lista használatával** létrehozhat egy **feladat**-hozzárendelést egy megnevezett erőforráshoz vagy egy általános erőforráshoz. Ha a tevékenység hozzárendelt erőforrások legördülő listában választ ki egy elnevezett **erőforrást, és ez az erőforrás** szerződés-feldolgozó, a megnevezett erőforrás hozzá lesz rendelve a tevékenységhez, és létrejön egy megfelelő projektcsapattag-rekord, amelynek dolgozói típusa **Szerződés-feldolgozó** és **Érvényesség érvénytelen** **·**. Következő lépésként meg kell nyitnia a projektcsapat tagjának rekordját, és ki kell választania egy alvállalkozói és alvállalkozói vonalat. Ez frissíti a feladat-hozzárendelést, hogy hivatkozzon az alvállalkozói és alvállalkozói sorra, és frissíti a csapattag állapotát **Érvényesre**.

Ha úgy dönt, hogy általános csapattagot hoz létre a **hozzárendelt erőforrások legördülő listában,** az **Általános csapattag létrehozása párbeszédpanel lehetővé teszi** egy alvállalkozói és alvállalkozói sor kiválasztását. Amikor az általános erőforrás hozzá van rendelve a tevékenységhez, és létrejön a projektcsapat megfelelő bejegyzése, észre fogja venni, hogy a projektcsapat-bejegyzés a **Szerződés-feldolgozó** és érvényesség beállítású munkavégző típussal **jön** **létre**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Projektcsapattagok létrehozása a Csapat lapon
A projekt Csapat lapján létrehozhat egy általános vagy elnevezett csapattagot. A csapattag létrehozásakor kiválaszthatja az alvállalkozói és alvállalkozói vonalat. A csapattag létrehozása után a csapattagot hozzá kell rendelnie egy tevékenységhez a **hozzárendelt erőforrások** legördülő menü segítségével. 

## <a name="updating-estimates"></a>Becslések frissítése
Miután hozzárendelte a projektcsapat tagjait a tevékenységekhez, el kell navigálnia a **projekt Becsültek** lapjára, és válassza az Árak frissítése lehetőséget **annak biztosítása** érdekében, hogy az alvállalkozói erőforrás-hozzárendelések költségdíjai az alvállalkozóhoz csatolt beszerzési árlista alapján frissüljenek. A Microsoft nem rendeli el a hozzárendeletlen feladatokra vonatkozó Dynamics 365 Project Operations becsléseket. Ennek eredményeként tevékenység-hozzárendeléseket kell létrehoznia a projekt különböző tevékenységeinek ára és költsége érdekében. 

> [MEGJEGYZÉS!] Azok a projektcsapat-tagok, amelyek **feldolgozói típussal rendelkeznek** szerződéses **dolgozóként, de nem rendelkeznek** alvállalkozói hivatkozással, érvénytelenként vannak megjelölve **a** **Projektcsapat tagjai** rácson. Ha vannak ilyen állapotú projektcsapattagok, nyissa meg a projektcsapat tagjának rekordját, és manuálisan frissítse az alvállalkozói és alvállalkozói sormezőket úgy, hogy a pénzügyi költségbecslés pontosan tükrözze a Becslések lapon szereplő **alvállalkozói költségeket.** 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
