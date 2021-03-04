---
title: Általános foglalható erőforrások hozzárendelése egy feladathoz és projektcsoporthoz
description: Ez a témakör információt nyújt az általános erőforrásoknak a feladatokhoz és a projektcsoportokhoz való foglalásáról.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 684167f0a68872ef871fbaa06c5161e78045c9a5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145406"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Általános foglalható erőforrások hozzárendelése egy feladathoz és erőforrás-követelmények generálása 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A lefoglalások és a nevesített vagy valós erőforrások projekthez rendelése mellett általános erőforrásokat is hozzárendelhet a projekt feladataihoz. Ezek az erőforrások a nevesített erőforrások számára helyőrzőként szolgálhatnak, amíg készen nem áll a projekt nevesített erőforrásokkal való ellátására. 

1. Nyissa meg a **Projekt** oldalt a Project Service Automation (PSA) programban, majd az **Ütemezés** lapon adja meg az általános erőforrás pozíciójának nevét az ütemezés **Erőforrás** cellájában. Másik lehetőségként kattintson a cellában az **Erőforrás** ikonra, és nyissa meg az Erőforrás-választót, majd adja meg a létrehozni kívánt általános erőforrás nevét.

![Általános csoporttag létrehozása és hozzárendelése](media/RM-how-to-9.png)

Ekkor megnyílik a **Projektcsoport tag gyors létrehozása** panel. 

2. Adja meg az általános erőforráscsoport tagjának szerepkörét és szervezeti egységét, majd kattintson **Mentés** lehetőségre.

![Általános csoporttag gyors létrehozása](media/RM-how-to-10.png)

3. Miután létrehozta az új általános erőforráscsoport-tagot, az hozzárendelésre kerül a feladathoz. Az adott általános erőforrást továbbra is hozzárendelheti a feladatütemezésben szereplő egyéb feladatokhoz.

![Meglévő általános csoporttag hozzárendelése feladatokhoz](media/RM-how-to-11.png)

4. Miután hozzárendelte az általános erőforrást, létrehozhat egy erőforrás-követelményt, és teljesítheti azt közvetlen foglalással, vagy egy erőforrás-kérelemnek az erőforrás-kezelőnek való elküldésével.

![Általános csoporttagra vonatkozó követelmény létrehozása](media/RM-how-to-12.png)

A csoporttag rácson a fentiek szerint használhatja az erőforrás-választót, de általános erőforrásokat közvetlenül is hozzáadhat itt. Az erőforrások egy olyan erőforrás-követelménnyel kerülnek hozzáadásra, amely a **Gyors létrehozás: projekt csoporttag** panelen megadott kezdő/végdátumokon és felosztási módszereken alapul.

A különbség akkor jelenik meg, ha közvetlenül hozzáadja az általános csoporttagot, majd több feladatot rendel hozzá az általános erőforráshoz, mint ahány óra rendelkezésre áll azok lefedéséhez. Kattintson a **Követelmény létrehozása** lehetőségre a követelmény újbóli létrehozásához, a szükséges órák és a hozzárendelések kiegyensúlyozása érdekében.

Az **Erőforrás-követelmény** hivatkozásra kattintva a csoport rácson is megnyithatja a követelményt, és készségeket, előnyben részesített erőforrásokat stb. adhat hozzá.

![Erőforrás-követelmény](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]