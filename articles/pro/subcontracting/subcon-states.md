---
title: Állapotátváltások az alvállalkozói szerződésben
description: Ez a cikk a Microsoft Dynamics 365 Project Operations alvállalkozóira vonatkozó állapotátmeneteket ismerteti az alvállalkozó létrehozásakor, végrehajtásakor és lezárásakor.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2804fc30f8dade42dc1093e5fc0f01fa1db22ca3
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522937"
---
# <a name="state-transitions-on-a-subcontract"></a>Állapotátváltások az alvállalkozói szerződésben 

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Ez a cikk ismerteti a alvállalkozókra vonatkozó állapotátváltásokat a Microsoft Dynamics 365 Project Operations alkalmazásban. Minden állapot vázlatként, megerősítettként, lezártként vagy visszavontként jelenik meg. Az alábbi kép az állapotátmeneteket mutatja be.

![Alvállalkozói állapot modellje](../media/SubconStates.png)  

A következő táblázat azt mutatja be, hogy az egyes állapotok mit képviselnek a Project Operations alvállalkozói életciklusában.

| State | Description | Engedélyezett átmenetek |
| --- | --- | --- |
| Piszkozat | Ez egy alvállalkozói szerződés kezdeti állapotát jelenti. Az beszállítóval folytatott egyeztetések folyamatban vannak. A sorok és az árképzés is változhat. Ebben az állapotban alvállalkozói szerződés használhatók az erőforrások és anyagok projektkövetelményének becslésére és személyzeti hozzárendelésére. Egy projektben időre, költségre és anyaghasználatra is hivatkozhat. Az ebben az állapotban lévő alvállalkozói szerződések szerkeszthetők és törölhetők. | Megerősítve |
| Megerősítve | Ez az alvállalkozónak azt a fázisát jelenti, amikor az alvállalkozóval az árképzésről és a megvásárolt sorcikkekről folytatott tárgyalások befejeződnek. Az anyagok tényleges és/vagy az alvállalkozói erőforrások által végzett munka tényleges átadása azonban még folyamatban van. Ebben az állapotban alvállalkozói szerződés használhatók az erőforrások és anyagok projektkövetelményének becslésére és személyzeti hozzárendelésére. Egy projektben időre, költségre és anyaghasználatra is hivatkozhat. Az ebben az állapotban lévő alvállalkozói szerződések nem szerkeszthetők és törölhetők. A **Mégse** gomb lehetővé teszi egy megerősített alvállalkozó szerződés érvénytelenítését. A **Újranyitás** gomb segítségével az alvállalkozó újra megnyitható, így vissza tudja hozni **Vázlat** állapotba. A **Bezárás** gombbal lezárhat egy megerősített alvállalkozói szerződést. | Bezárva <br> Megszakított <br> Piszkozat |
| Bezárva | Ez az alvállalkozói szerződésnek az a fázisa, amikor ténylegesen történik az anyagok szállítása és/vagy az alvállalkozói erőforrások által történő elvégzése. Ebben az állapotban alvállalkozói szerződés már nem használható az erőforrások és anyagok projektkövetelményének becslésére és személyzeti hozzárendelésére. Mindemellett egy projektben időre, költségre és anyaghasználatra már nem hivatkozhat. Az ebben az állapotban lévő alvállalkozói szerződések nem szerkeszthetők és törölhetők. | None |
| Megszakított | Ez az alvállalkozói szerződésnek az a fázisa, amikor az anyagok szállítása és/vagy az alvállalkozói erőforrások által történő elvégzése már nem szükséges. Az ebben az állapotban alvállalkozói szerződés nem használhatók fel az erőforrások és anyagok projektkövetelményének becslésére és személyzeti hozzárendelésére, és nem hivatkozhat egy projekten időre, költségre és anyaghasználatra. Az ebben az állapotban lévő alvállalkozói szerződések nem szerkeszthetők és törölhetők. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
