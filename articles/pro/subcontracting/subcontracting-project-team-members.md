---
title: Alvállalkozóiprojektcsoporttag-regisztráció
description: Ez a cikk a projektcsoporttagokra vonatkozó alvállalkozásba adás folyamatát ismerteti a Microsoft Dynamics 365 Project Operations alkalmazásban.
author: rumant
ms.date: 9/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a2f17d6f270029e3a517e99c7bb518cdb19b8d23
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522798"
---
# <a name="subcontracting-project-team-members"></a>Alvállalkozóiprojektcsoporttag-regisztráció

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Microsoft Dynamics 365 Project Operations alkalmazásbaban dönthet úgy hogy alvállalkozókét kezel személyzeti vagy nem személyzeti csoporttagokat.

- A nem személyzeti projektcsoporttagokhoz általános erőforrás van hozzárendelve.
- A személyzeti csoporttagokhoz egy elnevezett erőforrás van hozzárendelve.

Amikor egy projektcsoporttagot alvállalkozói sorhoz társít, a csoporttag minden feladat-hozzárendelése újra lesz költségelve az alvállalkozói szerződéshez csatolt beszerzési árlista alapján.  A **Projekt részletei** lap **Becslések** lapján az **Árak frissítése** gomb segítségével láthatja az alvállalkozásba adási döntésből származó frissített árképzési és/vagy költségszámítási eredményt. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Nem személyzeti projektcsoporttag alvállalkozói használata
A **Csoporttag részletei** lapon alvállalkozó és alvállalkozói sor mezők vannak, amelyek segítségével a projektvezető kifejezheti, hogyan szeretnék lehívni az alvállalkozótól szükséges kapacitást. Projektcsoporttag általános erőforrású való alvállalkozóként való használatához hajtsa végre a következő lépéseket:

1.  Válasszon egy alvállalkozót a **Csoporttag részletei** oldalon.

2.  Csak **Vázlat** vagy **Megerősítve** állapotú alvállalkozói szerződéseket választhat ki. A **Lezárt** vagy **Visszavont** alvállalkozók nem választhatók ki. 

3.  Az **Alvállalkozói sor** mező az alvállalkozó kiválasztása után válik láthatóvá.

4.  Az **Alvállalkozói sor** mezőben csak olyan alvállalkozói sorok választhatók ki, amelyek időre vonatkoznak. Nem jelölhet ki költségre vagy anyagra vonatkozó alvállalkozói sorokat.

5.  A projekt csoporttag rekordja szerepkörének meg kell egyeznie az alvállalkozó sor szerepkörével. Ez biztosítja, hogy a projekthez a becsült szerepköridő ugyanaz a szerepkör legyen, mint amit az alvállalkozói soron megvásárolnak. 

Amikor egy általános csoporttaghoz alvállalkozói és alvállalkozói sor van társítva, a program az általános csoporttagsor **Dolgozó típusa** mezőjét a **Szerződéses dolgozó** értékre frissíti, az **Alvállakozó érvényessége** értéke **Érvényes** értékre lesz állítva.

## <a name="subcontracting-a-staffed-project-team-member"></a>Személyzeti projektcsoporttag alvállalkozói használata
A csoport általános vagy nem személyzeti tagjaihoz hasonlóan, a személyzeti csoporttag-kapacitás is hozzárendelhető egy alvállalkozó szerződéshez. Elnevezett projektcsoporttag alvállalkozóként való használatához hajtsa végre a következő lépéseket:

1.  Győződjön meg róla, hogy a elnevezett erőforrás szerződéses dolgozó típusú foglalható erőforrásként van beállítva. Emellett arra is ügyeljen, hogy a foglalható erőforrás **Szállító** mezője megegyezzen a kiválasztott alvállalkozói szerződés szállítójával. 

2.  Csak **Vázlat** vagy **Megerősítve** állapotú alvállalkozói szerződéseket választhatja ki. A **Lezárt** vagy **Visszavont** alvállalkozók nem választhatók ki. 

3.  Az **Alvállalkozói sor** mező az alvállalkozó kiválasztása után válik láthatóvá.

4.  Az **Alvállalkozói sor** mezőben csak olyan alvállalkozói sorok választhatók ki, amelyek időre vonatkoznak. Nem jelölhet ki költségre vagy anyagra vonatkozó alvállalkozói sorokat.

5.  A projekt csoporttag rekordja szerepkörének meg kell egyeznie az alvállalkozó sor szerepkörével. Ez biztosítja, hogy a projekthez a becsült szerepköridő ugyanaz a szerepkör legyen, mint amit az alvállalkozói soron megvásárolnak. 

Az olyan elnevezett projektcsoporttagok, akik szerződés es dolgozó típusú **Foglalható erőforrásként** vannak beállítva esetében az alvállalkozói szerződés érvényessége **Nem érvényes** lesz, ha nincsenek alvállalkozói szerződéshez társítva. Amikor egy elnevezett csoporttaghoz alvállalkozói és alvállalkozói sor van társítva, a program a csoporttagsor **Dolgozó típusa** mezőjét a **Szerződéses dolgozó** értékre frissíti, az **Alvállakozó érvényessége** értéke **Érvényes** értékre lesz állítva.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
