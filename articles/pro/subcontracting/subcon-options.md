---
title: Alvállalkozói lehetőségek projektcsoporttagok számára
description: Ez a cikk a projektcsoporttagokra vonatkozó alvállalkozói lehetőségeket ismerteti a Microsoft Dynamics 365 Project Operations alkalmazásban.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 046b5d38ef7e433d02e3eac2e858a3333e941c45
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522281"
---
# <a name="subcontracting-options-for-project-team-members"></a>Alvállalkozói lehetőségek projektcsoporttagok számára

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Microsoft Dynamics 365 Project Operations alkalmazásban kiértékelheti a projektcsoport egy vagy több tagja számára elérhető alvállalkozói lehetőségeket. Az elérhető alvállalkozói lehetőségek a következőkre biztosítanak lehetőséget Önnek:

- Új alvállalkozói szerződés létrehozása és/vagy új sorok létrehozása egy meglévő alvállalkozó szerződések a kijelölt csoporttagokhoz. 
- Foglalást hozhat létre egy már meglévő alvállalkozó szerződéssel vagy alvállalkozói sorral szemben. 

Választhat az általános projektcsoporttagokhoz rendelkezésre álló alvállalkozói lehetőségek közül, illetve választhat a projektcsoport olyan tagjai közül, akikhez egy elnevezet erőforrás lett rendelve, aki egy szerződéses dolgozó. 

Nincsenek elérhető alvállalkozói lehetőségek a következőkhöz:

- Projektcsoport-tagok, akikhez munkavállalói kiosztással rendelkeznek. 
- Olyan projektcsoporttagok, akik már hozzá vannak rendelve egy alvállalkozói szerződéshez vagy alvállalkozói sorhoz. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Nem személyzeti projektcsoporttag alvállalkozói használata

A projektcsoport általános vagy nem alkalmazott tagjaira vonatkozó alvállalkozói lehetőségek áttekintéséhez és a rendelkezésre álló lehetőségek áttekintéséhez és kiválasztásához hajtsa végre a következő lépéseket:

1. Válasszon ki egy vagy több olyan projektcsoport-tagrekordot, ahol az erőforrás általános erőforrás.
2. Győződjön meg róla, hogy a kijelölt projektcsoporttag-rekordok egyike sincs még alvállalkozásba adva. 
3. Válassza ki az **Alvállalkozásba adás beállításai** elemet a projektcsoporttagok részrácsán. Megnyílik az **Alvállalkozásba adás beállításai** párbeszédpanel. 
4. Ha csak egy projektcsoporttag-rekordot jelölt ki az 1. lépésben, a következő beállítások használhatók:
    - Új alvállalkozói sorok létrehozása. 
    - Foglalás meglévő alvállalkozóhoz Ha több projektcsoport-tagrekordot jelölt ki az 1. lépésben, akkor az egyetlen elérhető lehetőség új alvállalkozói sorok létrehozása.
5. A meglévő alvállalkozósorral vonatkozó foglalási lehetőség lehetővé teszi egy olyan alvállalkozó és alvállalkozósor kiválasztását, amellyel szemben foglalni szeretne Amikor kijelöl egy alvállalkozói sort a kapacitás lefoglalásához, gondoskodnia kell arról, hogy a kijelölt alvállalkozói sor idő legyen, és hogy a projektcsoport tagja által megkövetelt szerepkör megegyezzen az alvállalkozói soron megvásárolt szerepkörrel.
6. Ha azt választja, hogy új alvállalkozói sorokat hoz létre a projektcsoport tagjai számára, akkor a rendszer lehetővé teszi a sorok létrehozásához használni kívánt alvállalkozói sorok kijelölését. Az új sorok létrehozásához kiválasztott alvállalkozónak **Vázlat** állapotúnak kell lennie. Ezzel a lehetőséggel új alvállalkozósorok létrehozására a kijelölt projektcsoport tagjai számára, a rendszer egy alvállalkozói sort hoz létre időhöz az egyes projektcsoporttagok számára. A szerepkör, az órák és a dátumok az egyes létrehozott alvállalkozói sorának projektcsoporttagjából lesznek másolva. 
7. Amikor egy általános csoporttaghoz alvállalkozói és alvállalkozói sor van társítva, a program az általános csoporttagsor **Dolgozó típusa** mezőjét a **Szerződéses dolgozó** értékre frissíti, az **Alvállakozó érvényessége** elem **Érvényes** értékre lesz állítva.

## <a name="subcontracting-a-staffed-project-team-member"></a>Személyzeti projektcsoporttag alvállalkozói használata

Az általános és a nem személyzeti csoporttagokhoz hasonlóan az alvállalkozói lehetőségek is megtekinthetők a személyzeti csoporttagokhoz is, amíg a személyzeti csoporttagok szerződéses dolgozók. A projektcsoport személyzeti vagy elnevezett tagjaira vonatkozó alvállalkozói lehetőségek áttekintéséhez és a rendelkezésre álló lehetőségek áttekintéséhez és kiválasztásához hajtsa végre a következő lépéseket:

1. Válasszon ki egy vagy több olyan projektcsoport-tagrekordot, ahol az erőforrás elnevezett szerződéses dolgozó.
2. Győződjön meg róla, hogy a kijelölt projektcsoporttag-rekordok egyike sincs még alvállalkozásba adva. 
3. Válassza ki az **Alvállalkozásba adás beállításai** elemet a projektcsoporttagok részrácsán. Megnyílik az **Alvállalkozásba adás beállításai** párbeszédpanel. 
4. Ha csak egy projektcsoporttag-rekordot jelölt ki az 1. lépésben, a következő beállítások használhatók:
      - Új alvállalkozói sorok létrehozása.
      - Foglalás egy meglévő alvállalkozóval szemben.
  Ha több projektcsoport-tagrekordot jelölt ki az 1. lépésben, akkor az egyetlen elérhető lehetőség új alvállalkozói sorok létrehozása.
5. A meglévő alvállalkozósorral vonatkozó foglalási lehetőség lehetővé teszi egy olyan alvállalkozó és alvállalkozósor kiválasztását, amellyel szemben foglalni szeretne Amikor kijelöl egy alvállalkozói sort a kapacitás lefoglalása érdekében, a következőket kell biztosítani:
      - A kijelölt alvállalkozói sor az időhöz tartozik. 
      - A projektcsoporttaghoz szükséges szerepkör megegyezik az alvállalkozói soron megvásárolt szerepkörrel. 
      - Az a szállító, akihez a szerződéses dolgozó társítva van, megegyezik az alvállalkozói szerződés szállítójával.
6. Ha azt választja, hogy új alvállalkozói sorokat hoz létre a projektcsoport tagjai számára, akkor a rendszer lehetővé teszi a sorok létrehozásához használni kívánt alvállalkozói sorok kijelölését. Ennél a beállításnál gondoskodnia kell arról, hogy az alvállalkozó, akihez a szerződéses dolgozó társítva van, megegyezik az alvállalkozói szerződés szállítójával. 
7. Az új sorok létrehozásához kiválasztott alvállalkozónak **Vázlat** állapotúnak kell lennie. Ezzel a lehetőséggel új alvállalkozósorok létrehozására a kijelölt projektcsoport tagjai számára, a rendszer egy alvállalkozói sort hoz létre időhöz az egyes projektcsoporttagok számára. A szerepkör, az órák és a dátumok az egyes létrehozott alvállalkozói sorának projektcsoporttagjából lesznek másolva.  
8. Amikor egy elnevezett csoporttaghoz alvállalkozói és alvállalkozói sor van társítva, a program az elnevezett csoporttagsor **Dolgozó típusa** mezőjét a **Szerződéses dolgozó** értékre frissíti, az **Alvállakozó érvényessége** elem **Érvényes** értékre lesz állítva.

## <a name="re-costing-subcontractor-assignments"></a>Alvállalkozók hozzárendelésének újraköltségezése

Amikor egy projektcsoport tagja (általános vagy elnevezett) alvállalkozói sorokhoz kapcsolódik az **Alvállalkozói beállítások** párbeszédpanel segítségével, a csoporttag feladataihoz való hozzárendelések újraköltségezésre kerülnek az alvállalkozóhoz csatolt beszerzési árlista alapján. A **Projekt részletei** lap **Becslések** lapján az **Árak frissítése** gomb segítségével láthatja az alvállalkozásba adási döntésből származó frissített árképzési és/vagy költségszámítási eredményt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
