---
title: Projektek és feladatok leképezése egy projektalapú szerződéssorra - Lite
description: Ez a cikk a projektek és feladatok szerződéssorhoz való hozzáadásával és eltávolításával kapcsolatban tartalmaz tájékoztatást.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c8075e3161acd904969f964e5ab32dfe04edc4b6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932529"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a>Projektek és feladatok leképezése egy projektalapú szerződéssorba 

_**A következőre vonatkozik:** Egyszerű központi telepítés – proforma számlázás, Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A Projektalapú szerződéssorokon leképezheti a projekt adott feladatait a szerződéssor.

Ha adott feladatokat rendel egy szerződéssorhoz, akkor a számlázási mód, a számlázhatósági beállítások, a nem meghaladandó korlát és a szerződéssoron definiált ügyfelek csak az adott feladatra lesznek érvényesek.

Ha olyan helyzet van, amikor egy projekt egyik fázisa, például a prototípus fázis, rögzített árú, és az összes többi fázis idő- és anyagelszámolású, akkor a prototípus fázist és az összes társított alárendelt feladatot hozzárendelheti az adott fázishoz tartozó szerződéssorhoz egy rögzített árú számlázási móddal.

A projekt munkalebontási struktúrájában (WBS) az összes többi fázis hozzárendelhető az idő- és anyagelszámolású szerződéssorhoz.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Feladatok társítása projektalapú szerződéssorokhoz

A feladatok társíthatók szerződéssorokhoz a **Számlázható feladatok** lapról a **Szerződéssor** oldalon, vagy a **Feladat számlázása** lapról a **Projekt** oldalon.

### <a name="from-the-contract-line-page"></a>Szerződéssor oldalról

Hajtsa végre a következő lépéseket a projekttevékenységek a szerződéssorhoz való társításához a **szerződéssor** lap **számlázható feladatok** lapján.

1. A projektalapú szerződéssor **Általános** lapján ellenőrizze, hogy kitöltötte a **Projekt** mezőt.
2. A **Hozzáadott feladatok** mezőben jelölje ki a **csak a kijelölt feladatokat**.
3. Módosítások mentése. Az űrlap frissítése megtörténik, és a **Számlázható feladatok** lap látható lesz.
4. Jelölje ki a **Számlázható feladatok** lapot, majd az alrácson válassza a **szerződéssor-feladat hozzáadása** elemet.
5. A **szerződéssor–feladatok** lap **feladatok** legördülő listájában jelölje ki a feladatot. 
6. Adja meg az adatokat a **Számlázási típus** mezőben, majd kattintson a **Mentés és bezárás** lehetőségre. A kijelölt feladat a szerződéssorhoz van társítva.

> [!NOTE]
> Ez nem a legoptimálisabb élmény a projekttevékenységek szerződéssorok közötti társításához. Az egyes projekteket manuálisan hozzá kell rendelni ehhez a tapasztalathoz. A preferált módszer a **projekt** oldal **feladatszámlázás** lapján érhető el.

### <a name="from-the-project-page"></a>A Projekt oldalról

Ez az optimális módszer a feladatok szerződéssorok közötti hozzárendelésére. Több feladatot is kijelölhet, és az összeset és alárendelt feladatait hozzárendelheti a kiválasztott szerződéssorhoz. Hajtsa végre a következő lépéseket a feladatok szerződéssorhoz való hozzárendeléséhez a **projekt** lapon.

1. A projektalapú szerződéssor **Általános** lapján ellenőrizze, hogy kitöltötte a **Projekt** mezőt.
2. A **Hozzáadott feladatok** mezőben jelölje ki a **csak a kijelölt feladatokat**.
3. Projektalapú szerződéssor mentése. Az űrlap frissítése megtörténik, és a **Számlázható feladatok** lap látható lesz. Ez csak csak ellenőrzési célokra szolgál.
4. A projektalapú szerződéssor **Általános** lapján a **Projekt** mezőben válassza ki a projekthivatkozást.
5. A **projekt** lapon jelölje ki a **feladat számlázása beállítás** lapot.
6. Két rács áll rendelkezésre. Az egyik rács a teljes projektre érvényes szerződéssorokhoz van. A második rács a feladatspecifikus számlázási beállításokra vonatkozik. A második rácsban jelöljön ki egy vagy több feladatot, majd jelölje be a **szerződéssorok társítása** jelölőnégyzetet.
7. A megnyíló párbeszédpanelen válasszon egy szerződéssort a legördülő listából.
8. A **Számlázási típus** legördülő lista segítségével jelölheti meg a feladatokat Számlázható vagy nem számlázható módon.
9. Jelölje be a jelölőnégyzetet, ha jelezni szeretné, hogy a társításnak tartalmaznia kell a kijelölt tevékenységek alárendelt feladatait is. A jelölőnégyzet bejelölésével a kijelölt feladatok alárendelt feladatait is társítja a szerződéssor.
10. Válassza az **OK** elemet a párbeszédpanel bezárásához.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Feladatok társításának visszavonása projektalapú szerződéssorokvól

### <a name="from-the-contract-line-page"></a>Szerződéssor oldalról

Hajtsa végre a következő lépéseket a projekttevékenységek a szerződéssorhoz való társításának visszavonásához a **szerződéssor** lap **számlázható feladatok** lapján.

1. A **számlázható feladatok** lapon jelölje be a **szerződéssor feladat törlése** jelölőnégyzetet.
2. Egy figyelmeztető üzenet jelzi, hogy a társítás megszüntetése a feladathoz előzőleg rögzített tényleges adatok sztornírozását okozhatja. A párbeszéden kattintson az **OK** gombra a feladat és a projektalapú szerződéssor közötti társítás eltávolításához. 

> [!NOTE]
> Ezzel a művelettel a feladat nem törlődik a projektből. Ehelyett eltávolítja a feladat-hozzárendelést a Projektalapú szerződéssorból.

### <a name="from-the-project-page"></a>A Projekt oldalról

Ez az optimálisabb élmény a projekttevékenységek szerződéssorok közötti társításának visszavonására. Több feladatot is kijelölhet, és az összeset és alárendelt feladatait is leválaszthatja a kiválasztott szerződéssorról. Hajtsa végre a következő lépéseket a feladatok szerződéssorhoz való hozzárendelésének visszavonásához.

1. A projektalapú szerződéssor **Általános** lapjáról a **Projekt** mezőben kattintson a projekt hivatkozására.
2. A **projekt** lapon jelölje ki a **feladat számlázása beállítás** lapot.
3. Az oldalon két rács van. Az egyik rács a teljes projektre vonatkozó szerződéssorokat tartalmazza, míg a második a feladatspecifikus számlázási beállításokra vonatkozik. A második rácsban jelöljön ki egy vagy több feladatot, majd jelölje be a **szerződéssorok társításának visszavonása** jelölőnégyzetet.
4. A megnyíló párbeszédpanelen válasszon egy szerződéssort a legördülő listából.
5. Jelölje be a jelölőnégyzetet, ha jelezni szeretné, hogy a társítást el kell távolítani a kijelölt tevékenységek alárendelt feladataiból is. A jelölőnégyzet bejelölésével a kijelölt feladatok alárendelt feladatait is leválasztja a szerződéssorból.
6. Kattintson az **OK** gombra. Egy figyelmeztető üzenet jelzi, hogy a társítás megszüntetése a feladathoz előzőleg rögzített tényleges adatok sztornírozását okozhatja. A figyelmeztető párbeszéden kattintson az **OK** gombra a feladat és a projektalapú szerződéssor közötti társítás eltávolításához.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
