---
title: Nevesített erőforrások foglalása erőforrás-követelményekből
description: Ez a témakör a nevesített erőforrásoknak egy általános erőforrás-követelmény részére történő foglalásáról nyújt tájékoztatást.
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
ms.openlocfilehash: 50858d4fc55285b2e91117c6cbfb2419931b4197
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291037"
---
# <a name="book-named-resources-from-resource-requirements"></a>Nevesített erőforrások foglalása erőforrás-követelményekből

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Egy elnevezett erőforrás foglalható az erőforrás-követelménnyel rendelkező általános erőforrás lecserélése céljából.

1. A Project Service Automation (PSA) program **Projektek** lapján kattintson a **Csoport** fülre.
2. Válassza ki a listából azt az általános erőforrást, amelyhez erőforrás-követelmény tartozik, majd kattintson a **Foglalás** lehetőségre. Másik lehetőségként nyissa meg az erőforrás-követelményt, majd kattintson a **Foglalás** lehetőségre.


![Általános csoporttag foglalása](media/RM-how-to-14.png)


3. Az **Ütemezési segéd** lapon jelöljön ki egy elnevezett erőforrást a projektcsoport számára történő foglaláshoz, majd kattintson a **Foglalás** lehetőségre.

![Általános csoporttag foglalása az Ütemezési segéd használatával](media/RM-how-to-15.png)

Amikor a foglalás befejeződött, és azt egy elnevezett erőforrás teljesíti, az általános erőforrást az elnevezett erőforrás váltja fel.

![Az általános csoporttagot leváltó elnevezett csoporttag](media/RM-how-to-16.png)

Továbbá az ütemezésben szereplő hozzárendelések frissülnek az elnevezett erőforrással.

![A projektfeladatokhoz hozzárendelt elnevezett csoporttag](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Általános erőforrás követelményeinek teljesítése több elnevezett erőforrással
Egy általános erőforrás követelménye több elnevezett erőforrással is teljesíthető, hasonlóan, mint egy elnevezett erőforrás hozzárendelése esetén. Például, adott egy feladat, amely öt nap és 120 óra ráfordítást igényel. Ezt a feladatot nem lehet egy olyan erőforrással befejezni, amely egy ötnapos héten átlagosan napi nyolc órát dolgozik. 

![Öt nap alatt 120 órányi erőfeszítést igénylő feladat](media/RM-how-to-21.png)

A követelmény 120 órányi robotikai mérnöki tevékenység öt nap alatt, tehát napi 24 óra.

![Napi követelmény](media/RM-how-to-22.png)

Ez egy példa arra az esetre, amikor egy általános erőforrás-kérelem teljesítéséhez több elnevezett erőforrásra van szükség. A követelmény teljesítéséhez több erőforrást is le kell foglalnia.

![Több erőforrás foglalása a követelmény teljesítéséhez](media/RM-how-to-23.png)

A fő különbség ezen forgatókönyv esetén, hogy az általános erőforrás a feladathoz rendelt csoportban marad, és a foglalt elnevezett erőforráscsoport-tagok nem lesznek hozzárendelve a pozíció részeként. A projektvezető a munkát megfelelő módon hozzárendelheti az elnevezett erőforrásokhoz. Az **Egyeztetés** segíthet a projektkezelőnek a foglalás több erőforrás közötti lebontásában a feladat-hozzárendelésekhez. Ez nem történik meg automatikusan, mert a fenti egyszerű példánál bonyolultabb forgatókönyv esetén (például, ha a követelményt számos feladat teszi ki) a szándékkal, a rendszernek feltételeznie kell a projektkezelő által igényelt hozzárendelési módot. Mivel a rendszer nem érti a szándékot, előfordulhat, hogy a feltételezések eltérnek a szándékolt módszertől, és az nem megfelelő vagy kiszámíthatatlan eredményt okoz. A kiszámítható eredmény az, hogy az általános erőforrás mindaddig hozzá lesz rendelve, amíg a projetkezelő szándékosan hozza létre a hozzárendeléseket az **Egyeztetés** nézet segítségével.




[!INCLUDE[footer-include](../includes/footer-banner.md)]