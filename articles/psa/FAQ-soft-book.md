---
title: Erőforrás puha foglalása
description: Ez a cikk arról nyújt tájékoztatást, hogyan ütemezheti vagy lágyan foglalhatja le a projektcsapat tagjait.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 6c666e5c0a83a3d1b440144a62cbd58a58c5db81
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929125"
---
# <a name="soft-book-a-resource"></a>Erőforrás puha foglalása

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Feltételesen ütemezhetők vagy „ideiglenesen lefoglalhatók” erőforrások egy projektcsoport számára annak a megjelenítéséhez, hogy erőforrásokat tervez hozzárendelni a projekthez. Az ideiglenes foglalások nem használják fel az erőforrás rendelkezésre álló kapacitását, és az ideiglenes lefoglalt csoporttagok hozzárendelhetők a projektfeladatokhoz. Azonban mivel ideiglenes foglalások nem használják fel az erőforrás rendelkezésre álló kapacitását, az erőforrás „véglegesen lefoglalható” más feladatokra az adott időszakon belül. Az általános erőforrásokon puha foglalás nem végezhető, illetve egy puha foglalás nem teljesítheti az általános erőforrásra vonatkozó kérelmet.

A projektcsoport puha foglalással foglalt tagjait a rendszer a **Projekt** oldal **Csoport** lapján listázza, puha foglalással foglalt óráik pedig a **Puha foglalásos órák** oszlopban láthatók az **Elnevezett csoporttagok** nézetben. A puha foglalással rendelkező csoport tagjai szintén szerepelnek az Ütemezés táblán. Mivel ezek puha foglalással kerültek foglalásra, az Ütemezés tábla ezen erőforrások kapacitásának semmilyen fogyasztását nem mutatja. A puha foglalással rögzített idő nem jelenik meg az **Egyeztetés** lapon, illetve, az Ütemezés tábla **Egyeztetés** lapjának **Foglalások meghosszabbítása** mezőjében sem látható. 

Kétféle módon lehet egy csoporttagot egy projekthez puha foglalással lefoglalni: közvetlenül az Ütemezés tábláról vagy a csoporttagnak a **Csoport** lapra történő felvételével. 

## <a name="soft-book-from-the-schedule-board"></a>Puha foglalás az Ütemezés tábláról
A következő lépésekkel elvégezheti az erőforrás puha foglalását az Ütemezés tábláról. 

1. Nyissa meg az Ütemezés táblát, majd a **Foglalási követelmények** panelen válassza a **Projekt** lapot.
2. Keresse meg azt a projektet, amelyhez szeretne egy erőforrás puha foglalással lefoglalni. Ha nagyszámú projekt van a listában, válassza a **Projekt** oszlopfejlécet, majd a szűrő segítségével keressen egy vagy több projektet.
3. Jelölje ki a projektet, majd húzza le az erőforrás időrácsára.
5. Az **Erőforrás-foglalás létrehozása** panelen állítsa be a kezdő és a befejező dátumot, állítsa a **Foglalás állapota** mezőt **Puha** értékre, majd állítsa be az órákat. 
6. Kattintson a **Foglalás** lehetőségre. Az erőforrás ekkor a **Csoport** lapon a projekt erőforrásaként látható. Az **Elnevezett csoporttag** nézetben láthatja a puha foglalással foglalt órákat a **Puha foglalásos órák** oszlopban.

> [!NOTE]
> Ekkor a puha foglalással foglalt feladatokat hozzárendelheti az **Ütemezés** lapon. Az **Egyeztetés** lapon az erőforrásnál a feladat hozzárendeléshez viszonyítva foglalási hátrány látható, mivel az **Egyeztetés** lap csak a kemény foglalásokat veszi figyelembe. A **Foglalások kiterjesztése** funkció segítségével az erőforrást kemény foglalással foglalhatja, hogy kiküszöbölje a kemény foglalások hátrányát az erőforrás-hozzárendelésekhez képest. A **Foglalás fenntartása** funkció használatával kézzel kell törölnie az erőforrás puha foglalását.

## <a name="soft-book-on-the-team-tab"></a>Ideiglenes lefoglalás a Csoport lapon

Csoporttagokat közvetlenül a **Csoport** lapon is hozzáadhat, majd foglalási állapotukat **Kemény** állapotról **Puha** állapotra módosíthatja a **Foglalások fenntartása** funkció segítségével. Ha ilyen módon vesz fel egy csoporttagot, az minden esetben kemény foglalást eredmény, kivéve ha a **Nincs** allokációs módszert választja ki.

A módszer használatához hajtsa végre a következő lépéseket.

1. A **Projekt** oldal **Csoport** lapján kattinton az **Új** lehetőségre.
2. Válassza ki a foglalható forrást, a szerepkört, valamint a kezdő és befejező dátumokat.
3. Válasszon egy, a **Nincs** módszertől eltérő allokációt.
4. Válassza a **Mentés** parancsot. Az erőforrást a rácson, az óráit pedig a **Kemény foglalású órák** oszlopban láthatja.
5. Az erőforrás foglalását a **Foglalások fenntartása** lehetőség kiválasztásával teheti meg.
6. Amikor az Ütemezés tábla megnyílik, bontsa ki az erőforrást a foglalások megjelenítéséhez. A foglalást **Kemény** foglalásként láthatja.
7. Kattintson jobb gombbal a foglalásra, és az **Állapot módosítása** elem alatt válassza a **Puha foglalás** \> **Puha** lehetőséget. A foglalás állapota ekkor **Puha** lesz.
8. Az ütemezés tábla bezárását követően láthatja, hogy az erőforrás órái a **Kemény foglalásos órák** oszlopból a **Puha foglalásos órák** oszlopba kerültek át a **Csoport** lap rácsán, ha az **Elnevezett csoporttagok** nézetben van.

> [!NOTE]
> Ha a **Foglalások fenntartása** funkciót használja a **Kemény** állapotról **Puha** állapotra való váltáshoz, majd kemény foglalással foglal egy erőforrást a csoporthoz, és feladatokat rendel hozzá az erőforráshoz, az erőforráshoz feladat-hozzárendelései megmaradnak. Az **Egyeztetés** lapon azonban az erőforrás foglalási hiányossággal fog rendelkezni, mivel csak a kemény foglalások kerülnek figyelembevételre a foglalások és a hozzárendelések összeegyeztetésekor. Az **Egyeztetés** lapon található **Foglalások kiterjesztése** funkció segítségével az erőforrást kemény foglalással foglalhatja, így küszöbölve ki a kemény foglalás és az erőforrás-hozzárendelések közötti hiányosságot. Az erőforrás puha foglalását törölnie kell a **Foglalások fenntartása** funkcióval.

Amikor készen áll módosítani az ideiglenesen lefoglalt csoporttag erőforrást végleges csoporttaggá, tegye a következőket:

1. Az Ütemezés táblán bontsa ki az erőforrást a foglalások megjelenítéséhez. Ekkor láthatja, hogy **Puha** foglalásról van szó.
2. Kattintson a jobb gombbal a foglalásra, és az **Állapot módosítása** szakasz alatt válassza a **Kemény foglalás** \> **Kemény** lehetőséget. A foglalás ekkor **Kemény** állapotra módosul.
3. Miután bezárta az Ütemezés táblát, térjen vissza a projekthez, és nyissa meg a **Csoport** lapot; ekkor az **Elnevezett csoporttagok** nézetben tartózkodva láthatja, hogy a **Csoport** lapon az erőforrás órái a **Puha foglalásos órák** oszlopból átkerültek a **Kemény foglalásos órák** oszlopba. Ha az erőforrást hozzárendelték feladatokhoz, akkor az **Egyeztetés** lapon nem jelennek meg a foglalási hiányok, mivel már kemény foglalással vannak foglalva.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
