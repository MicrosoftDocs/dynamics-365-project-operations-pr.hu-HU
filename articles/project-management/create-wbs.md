---
title: Munkalebontási struktúra létrehozása
description: Ez témakör ismerteti, hogyan lehet létrehozni az új ütemezési felületen a munkalebontási struktúrát (WBS) az alapvezérlők számára.
author: ruhercul
manager: tfehr
ms.date: 01/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 695bbc2ae1ba1e762472b5f5fa853c89017d2f52
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287016"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Munkalebontási struktúra (WBS) létrehozása

A projekt ütemezése ismerteti, hogy milyen munkát kell elvégezni, mely erőforrások fogják elvégezni a munkát, és azt az időkeretet, amelyen belül a munkát be kell fejezni. Az ütemterv tükrözi az összes projekt elküldésével időben társított munkát. A Dynamics 365 Project Operations-ben a következő szerint hozhat létre projektütemezést:

  - A munka kezelhető feladatokra való lebontása.
  - Az egyes feladatok végrehajtásához szükséges idő becslése.
  - Feladatfüggőségek beállítása.
  - A feladat időtartamának beállítása.
  - A feladatokat elvégző általános erőforrások becslése. 

A projekt ütemezése létre lett hozva a **Projekt** oldal **Ütemezés** fülén.

## <a name="tasks"></a>Feladatok

A projekt ütemezésének létrehozásakor az első lépés a munka kezelhető részekre bontása. A Project Operations ütemezése a következő szolgáltatásokat támogatja:

- Összefoglaló vagy tárolófeladatok
- Levélcsomópont-feladatok

### <a name="summary-tasks"></a>Feladatok összegzése

A Feladatok összegzése más összegző- vagy csomópontfeladatokat is tárol. Nem rendelkeznek erőfeszítéssel vagy költségekkel. Ehelyett erőfeszítéseik és költségeik a tároló feladatok erőfeszítéseinek és költségeinek összegét jelentik. Az összefoglaló feladat kezdő dátuma a tároló feladatok kezdő dátuma, a befejező dátum pedig a tároló feladatok befejező dátuma. Az összefoglaló feladat neve szerkeszthető, de az ütemezési tulajdonságok – ideértve az erőfeszítést, dátumokat és időtartamot – nem szerkeszthetők. Ha töröl egy összefoglaló feladatot, akkor törli az összes tároló feladatot.

### <a name="leaf-node-tasks"></a>Levélcsomópont-feladatok

A levélcsomópont-feladatok képviselik a projekt legrészletesebb munkáját. Becsült erőfeszítéssel, erőforrásokkal, tervezett kezdési és befejezési dátummal, valamint időtartammal rendelkeznek.

## <a name="create-a-task-hierarchy"></a>Hozzon létre egy feladathierarchiát

### <a name="add-a-task"></a>Feladat hozzáadása

Feladatidőtartam hozzáadásához hajtson végre egy vagy több feladatot.

1. Menjen a **Projektek** lehetőségre, és válassza ki és nyissa meg azt a projektrekordot, amelyhez ütemezést szeretne létrehozni. 
2. Válassza a **Feladatok** fület. 
3. Válassza az **Új feladat hozzáadása** lehetőséget, írja be a feladat nevét, majd nyomja meg az Enter billentyűt.
2. Adjon meg egy másik feladatnevet, majd nyomja meg újra az Enter billentyűt, amíg teljes nem lesz a feladatlista.

### <a name="manage-hierarchy-of-a-task"></a>Feladat hierarchiájának kezelése

Amikor egy feladatot behúznak, az a közvetlenül felette található feladat gyereke lesz. Ezután a feladat ütemezésazonosítóját újra kiszámítják úgy, hogy az új szülő ütemezésazonosítóján alapuljon, és kövesse a vázlatos számozási sémát. A szükő feladat most már összegző feladat. Így lesz a saját gyermekfeladatainak összegzése. Ha egy feladatot előléptettek, akkor már nem annak a feladatnak a gyermeke, amelyik a szülője volt. Az ütemezés azonosítóját ezután újra kiszámítja a rendszer, hogy tükrözze a feladat frissített mélységét és helyzetét a hierarchiában. Az előző szülőfeladat erőfeszítéseit, költségeit és dátumait újra kiszámítja a rendszer, így azok nem tartalmazzák ezt a feladatot.

Feladat behúzásához vagy előléptetéséhez hajtsa végre az alábbi lépéseket.

1. A **Projekt** lapon, a **Feladatok** fülön, az **Összefoglaló feladatok** alatt jelölje ki a feladat nevében a három függőleges pontot, majd válassza az **Alfeladattá alakítás** lehetőséget. 
2. Jelölje ki a behúzni vagy előléptetni kívánt feladatot. Egynél több feladat kijelöléséhez jelöljön ki egy feladatot, tartsa lenyomva a Ctrl billentyűt, és jelöljön ki további feladatokat.
2. Válassza a **Behúzás** vagy **Alfeladat előléptetése** funkciót a feladatok összefoglaló feladatok alá mozgatásához vagy azokból való kivételéhez.

### <a name="move-tasks-up-and-down"></a>Feladatok felfelé és lefelé mozgatása

A feladatok a munkalebontási struktúra bármely szintjére áthelyezhetők, az alábbi kétféle módon:

- Jelöljön ki még egy feladatot, és húzza őket a kívánt helyre.
- Jelöljön ki egy vagy több feladatot, kattintson a jobb gombbal, és válassza a **Kivágás** parancsot, jelölje ki az ütemezésben a célcellát, majd kattintson a jobb gombbal a **Beillesztés** parancsra.

## <a name="task-attributes"></a>Feladat attribútumok

A feladat neve leírja az elvégzendő munkát. A Project Operations-ben a feladattal kapcsolatos attribútumok leírják a feladat ütemezését és a személyzeti követelményeket.

## <a name="schedule-attributes"></a>Attribútumok ütemezése

Az **Erőfeszítés**, a **Kezdő dátum**, a **Befejező dátum** és az **Időtartam** attribútumok határozzák meg a feladat ütemezését.

Az alábbi tábla további ütemezési attribútumokat tartalmaz.

| **Végleges megjelenítendő név** | **Végleges leírása** |
| --- | --- |
| Befejezett munkamennyiség (óra) | A feladathoz tartozó elvégzett munka órákban kifejezve. |
| Időtartam | Megjeleníti a feladat időtartamát napokban. |
| Összes munkamennyiség | A feladathoz tartozó összes munka órákban kifejezve. |
| Befejezés | Befejező dátum és időpont. |
| % befejezve | A befejezett feladat készültségi százaléka. |
| Projektgyűjtő | A feladattábla gyűjtőnként csoportosítható, hogy minden gyűjtőnek saját oszlopa legyen. |
| Hátralévő munkamennyiség (óra) | A feladathoz tartozó fennmaradó munka órákban kifejezve. |
| Elejére | Kezdő dátum és időpont. |
| Adatfolyam neve | A feladat neve. |
| Azonosító | A munkalebontási struktúrában (WBS) található feladat azonosítója. |

Rendszergazdaként egyéni mezőket definiálhat a feladatentitáson. A mezők azonban nem jelennek meg az ütemezési táblázatban. Az egyéni mezők megtekintéséhez vegye fel őket a **Projektfeladat** részletei oldalon.

## <a name="staffing-attributes"></a>Munkaerő-attribútumok

A személyzet attribútumai az ütemterv **Erőforrások** mezőjével érhetők el. Vagy keressen meglévő erőforrást, vagy válassza a **Létrehozás** elemet, és a **Gyors létrehozás** ablaktáblában új erőforrásként adja hozzá a projekt egyik csapattagját.

A **Szerepkör**, az **Erőforrásbiztosító egység** és a **Pozíció neve** mezők a feladat személyzeti követelményeinek leírására szolgálnak. A személyzeti attribútumokat és a feladatütemezést a rendelkezésre álló erőforrások megkeresésére használják az adott feladat végrehajtásához.

   - **Szerepkör**: Adja meg a feladat elvégzéséhez szükséges erőforrás típusát.
   - **Erőforrásbiztosító egység**: Adja meg azt az egységet, ahonnan megtörténik az erőforrások hozzárendelése a feladathoz. Ez az attribútum befolyásolja a feladat költség- és értékesítési becslését, ha az erőforrás költségét és számlamértékét erőforrásbiztosító egységek alapján állítják be.
   - **Pozíció neve**: Adjon meg egy nevet az általános erőforrás számára, hogy a név helyőrzőjeként szolgáljon azon erőforrás számára, amely végül elvégzi majd a munkát.

Az **Erőforrások** mező az általános erőforrás vagy a megnevezett erőforrás pozíciónevét tartalmazza, ha megtalálható valamelyik.

A **Kategória** mező azokat az értékeket tartalmazza, amelyek egy olyan szélesebb körű munkát jelölnek, amelybe a feladat csoportosítható. Ez a mező nem érinti az ütemezést vagy a személyzetet. A mezőt ehelyett csak jelentéskészítésre használja a rendszer.

## <a name="task-dependencies"></a>Tevékenység függőségek

A Project Operations-ben az ütemezést a feladatok közötti korábbi kapcsolatok létrehozására használhatja. A **Korábbi** mező egy vagy több értéket vesz fel, hogy jelezze azokat a feladatokat, amelyektől a feladat függ. Ha egy feladathoz korábbi értékek vannak hozzárendelve, akkor a feladat csak a korábbi feladatok elvégzése után indulhat el. A függőség miatt a feladat tervezett kezdő dátumát visszaállítják a korábbi feladatok befejezésének napjára.

A feladat mód nincs hatással a korábbi/függő feladatok kezdő és befejező dátumának frissítéseire.

## <a name="accessibility-and-keyboard-shortcuts"></a>Kisegítő lehetőségek és billentyűparancsok

Az **Ütemezés** rács teljesen elérhető és képernyőolvasókkal, például a Narrátorral, JAWS vagy NVDA programokkal használható. A rácsterületen nyílbillentyűkkel mozoghat (a Microsoft Excel programhoz hasonlóan ), a Tab billentyű segítségével léphet tovább az interaktív felhasználói felület elemein, a lefelé mutató nyíl, az Enter vagy a szóköz segítségével választhat és lenyithatja a legördülő menüket.


[!INCLUDE[footer-include](../includes/footer-banner.md)]