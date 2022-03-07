---
title: Fő fogalmak
description: Ez a témakör információkat nyújt az erőforrás-kezelés kulcsfontosságú koncepcióiról a Project Service Automation területén.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 8e56523a9a2fbe8bc07e6d46062f4e1c20e6d2fa2244b32ff53e96d898b0086c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995089"
---
# <a name="key-concepts"></a>Fő fogalmak

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Az alábbi táblázat meghatározza az Dynamics 365 Project Service Automation alkalmazásban használt kulcsfogalmakat.

| Koncepció                    | Definíció |
|----------------------------|------------|
| A projekt csapattagja        | A projektcsapat részeként a projektcsoport tagja lehet egy megnevezett erőforrás, amelynek van foglalása, egy megnevezett erőforrás, amelynek nincs foglalása, vagy egy általános erőforrás. A generikus erőforrásokhoz nincs foglalási lehetőség, azok a helyi projektekben vannak, és nincs kapacitáskorlátozás a projektek között. |
| A projekt általános forrása   | Erőforrás-helyőrző, amely lehetővé teszi, hogy csapatot és személyzetet alkosson egy projekttervet anélkül, hogy meg kellene ismernie a megnevezett erőforrást. A projekt naptárát használják általános erőforrás-naptárként. Az általános erőforrások hozzáadhatók egy projektcsoporthoz és hozzárendelhetők a feladatokhoz. |
| Lefoglalt órák               | Az erőforrás órákat egy projekthez képest nehéz lefoglalni, hogy garantáljuk a projekt munkájának befejezését. A lekötött órákat az erőforrás teljes kapacitása felhasználja. A foglalások csak a megnevezett erőforrások ellen irányulnak, nem pedig az általános erőforrások ellen. |
| Kijelölt órák             | Az erőforrás-órákat a projekt ütemezésében a feladatokhoz rendelik. A hozzárendelések megnevezhetők vagy általános erőforrásokkal szemben is. A megbízások függetlenek a foglalástól. |
| Szükséges órák             | A szükséges kapacitás, amelyet még nem tölt be egy megnevezett erőforrás. A megkövetelt órák csak azokra az általános csoporttagokra vonatkoznak, akik erőforrás-követelményeket generáltak. |
| Igény                     | A jelenlegi és a beérkező munkaterhelés. A Project Service Automation alkalmazásban a kereslet erőforrás-igényként vagy erőforrás-igényként jelenik meg. |
| Erőforrás-követelmény       | Olyan entitás, amelyet a szükséges órák, kezdési és befejezési dátumok, készségek, földrajz és egyéb árazási dimenziók rögzítésére használnak a szükséges erőforrásokhoz. Az erőforrás-igényeket vagy a projektcsoport tagjai generálják, vagy egyénileg hozzák létre. |
| Erőforrás-igény           | Egy entitás, amelyet „borítékként” használnak az erőforrás-követelmény teljesítéséhez, amelyet az erőforrás-kezelőnek teljesítenie kell. |
| Az erőforrás alapértelmezett szerepe      | Az erőforrás csoportosítása a felhasználás számításához. Feltételezzük, hogy az erőforrás rendelkezik a szerephez szükséges képességekkel, és teljesíti a szerep célhoz való felhasználását. |
| Erőforrás-szervező egység | Az a szervezeti egység, amelyhez az erőforrás hozzá van rendelve. |
| Körvonal                    | Feladat, követelmény vagy kiosztási óra, mivel napi eloszlásra bontják őket. Például egy ötnapos, 40 órás feladatot napi nyolc órára alakíthatunk öt nap alatt. |
| Egyeztető nézet        | Nézet, amely megmutatja a projektcsoport tagjainak foglalásait és feladatait. Ez a nézet lehetővé teszi, hogy a projektmenedzser megkeresse a foglalások és a feladatok közötti bármilyen eltérést, és bármilyen eltérés esetén korrekciós lépéseket tegyen. |
| Munkaórák                 | Az entitás, amelyet az erőforrás-kapacitás, valamint a munkaidő és a munkaidőn kívüli idő azonosítására használnak. Ezt az entitást erőforrásnaptárnak is nevezik. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]