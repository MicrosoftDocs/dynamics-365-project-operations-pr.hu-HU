---
title: Projekt ütemezése
description: Ez a témakör információt nyújt az ütemezés létrehozásáról.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 9a6b27050a19d8a7f2ed35f74b42bb4f371ad069
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078127"
---
# <a name="project-schedules"></a>Projekt ütemezése 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A projekt ütemezése ismerteti, hogy milyen munkát kell elvégezni, mely erőforrások fogják elvégezni a munkát, és azt az időkeretet, amelyen belül a munkát be kell fejezni. Ez az összes olyan munkát tükrözi, amely a projekt időben történő végrehajtásával jár. A Dynamics 365 Project Service Automation szolgáltatásban úgy hozható létre a projekt ütemezése, hogy a munkát kezelhető feladatokra bontja, megbecsüli az egyes feladatok elvégzéséhez szükséges időt, beállítja a feladat függőségeit, a feladat időtartamát, és megbecsüli a feladatokat végrehajtó általános erőforrásokat. A projekt ütemezése a projektoldal **Ütemezés** lapján jön létre.
 
## <a name="tasks"></a>Feladatok

A projekt ütemezésének létrehozásakor az első lépés a munka kezelhető részekre bontása. A PSA ütemezése a következő szolgáltatásokat támogatja:

- Projekt gyökércsomópontja
- Összefoglaló vagy tárolófeladatok
- Levélcsomópont-feladatok

### <a name="project-root-node"></a>Projekt gyökércsomópontja

A projekt gyökércsomópontja a projekt legfelső szintű összefoglaló feladata. Minden más projekttevékenység ez alapján jönnek létre. A gyökércsomópont nevét mindig a projekt nevére állítják be. A gyökércsomópont erőfeszítéseit, dátumait és időtartamát az alatta lévő hierarchia értékei alapján összegzik. A gyökércsomópont tulajdonságait nem szerkesztheti. A gyökércsomópontot nem is törölheti.

### <a name="summary-or-container-tasks"></a>Összefoglaló vagy tárolófeladatok 

Az összefoglaló feladatok alfeladatokkal vagy tároló feladatokkal rendelkeznek. Nem rendelkeznek erőfeszítéssel vagy költségekkel. Ehelyett erőfeszítéseik és költségeik a tároló feladatok erőfeszítéseinek és költségeinek összegét jelentik. Az összefoglaló feladat kezdő dátuma a tároló feladatok kezdő dátuma, a befejező dátum pedig a tároló feladatok befejező dátuma. Az összefoglaló feladat neve szerkeszthető, de az ütemezési tulajdonságok (erőfeszítés, dátumok és időtartam) nem szerkeszthetők. Ha töröl egy összefoglaló feladatot, akkor törli az összes tároló feladatot.

### <a name="leaf-node-tasks"></a>Levélcsomópont-feladatok

A levélcsomópont-feladatok képviselik a projekt legrészletesebb munkáját. Becsült erőfeszítéssel, erőforrásokkal, tervezett kezdési és befejezési dátummal, valamint időtartammal rendelkeznek.
 
## <a name="creating-a-task-hierarchy"></a>Feladathierarchia létrehozása

A következő lehetőségekkel hozhat létre feladathierarchiát:

- **Feladat hozzáadása** gomb
- **Feladat behúzása** gomb
- **Feladat kihúzása** gomb
- **Mozgatás felfelé** és **Mozgatás lefelé** gombok
- Kisegítő lehetőségek és billentyűparancsok

### <a name="add-task"></a>Feladat hozzáadása

A **Feladat hozzáadása** gomb segítségével új feladatot hozhat létre a hierarchiában. Ha nem választja ki a pozíciót, akkor a feladat a végén kerül beillesztésre. 

Minden feladathoz tartozik ütemezésazonosító. Az ütemezésazonosító azonosítja a feladat mélységét és helyét a hierarchiában. Vázlatos számozást használ. Az első szintű feladatokhoz a projekt gyökércsomópontja alatt az 1, 2, 3 stb. számozási séma kerül felhasználásra. Az első szint alatti feladatokhoz az 1.1, 1.2, 1.3 stb. számozási séma kerül felhasználásra.

### <a name="indent-task"></a>Feladat behúzása

Amikor egy feladatot behúznak, az a közvetlenül felette található feladat gyereke lesz. Ezután a feladat ütemezésazonosítóját újra kiszámítják úgy, hogy az új szülő ütemezésazonosítóján alapuljon, és kövesse a vázlatos számozási sémát. A szülőfeladat most már összefoglaló vagy tároló feladat. Így lesz a saját gyermekfeladatainak összegzése.

### <a name="outdent-task"></a>Feladat kihúzása 

Ha egy feladatot kihúztak, akkor már nem annak a feladatnak a gyermeke, amelyik a szülője volt. Az ütemezés azonosítóját ezután újra kiszámítja a rendszer, hogy tükrözze a feladat frissített mélységét és helyzetét a hierarchiában. Az előző szülőfeladat erőfeszítéseit, költségeit és dátumait újra kiszámítja a rendszer, így azok nem tartalmazzák ezt a feladatot.

### <a name="move-up-and-move-down"></a>Mozgatás felfelé és lefelé 

A **Mozgatás felfelé** és a **Mozgatás lefelé** gombokkal változtatható meg a feladat helyzete a szülőhierarchiában. Az ilyen típusú változások nem befolyásolják a feladat erőfeszítését, költségét, dátumait vagy időtartamát. Csak a feladat ütemezésazonosítóját érintik. Az ütemezésazonosítót újraszámítják úgy, hogy az tükrözze a feladat új helyzetét a szülő gyermekfeladat-listáján.

### <a name="accessibility-and-keyboard-shortcuts"></a>Kisegítő lehetőségek és billentyűparancsok

Az **Ütemezés** rács teljesen elérhető és képernyőolvasókkal, például a Narrátorral, JAWS vagy NVDA programokkal használható. A rácsterületen nyílbillentyűkkel mozoghat (a Microsoft Excel programhoz hasonlóan ), a Tab billentyű segítségével léphet tovább az interaktív felhasználói felület elemein, a lefelé mutató nyíl, az Enter vagy a szóköz segítségével választhat és hívhatja be a legördülő menüket. Az oszlopfejlécek szintén interaktívak. Az oszlopokat elrejtheti és megjelenítheti, a Tab billentyűvel és a nyílbillentyűkkel mozgathatja az oszlopfejléceket, és az eszköztár műveleti gombjait is használhatja. Ezenkívül a következő billentyűparancsokat használhatja:

- **Frissítés** : ALT+SHIFT+F5
- **Hozzáadás** : ALT+SHIFT+Insert
- **Törlés** : ALT+SHIFT+Delete
- **Mozgatás fel/le** : ALT+SHIFT+Fel/le nyilak
- **Behúzás/kihúzás** : ALT_SHIFT+Balra/jobbra nyilak
- **Hierarchiák kibontása/összecsukása** : ALT+SHIFT+Plusz/mínusz gombok

## <a name="task-attributes"></a>Feladat attribútumok

A feladat neve leírja az elvégzendő munkát. A PSA-ban a feladattal kapcsolatos attribútumok leírják a feladat ütemezését és a személyzeti követelményeket.

> ![Feladat attribútumok](media/project-2.png)
 
### <a name="schedule-attributes"></a>Attribútumok ütemezése

Az **Erőfeszítés** , a **Kezdő dátum** , a **Befejező dátum** és az **Időtartam** attribútumok határozzák meg a feladat ütemezését.

További ütemezési attribútumok a következők:

- **Erőfeszítés órái** : Adja meg a feladat elvégzéséhez szükséges órák becsült számát. 
- **Időtartam** : Adja meg a feladat elvégzéséhez szükséges munkanapok számát.
- **Ütemezésazonosító** : Ezzel az automatikusan generált azonosítóval rendelik meg a feladatokat a hierarchiában. A feladatok közötti függőségek kezelik a feladatok tényleges sorrendjét.
 
### <a name="staffing-attributes"></a>Munkaerő-attribútumok

A személyzet attribútumai az ütemterv **Erőforrások** mezőjével érhetők el. Vagy keressen meglévő erőforrást, vagy kattintson a **Létrehozás** elemre, és a **Gyors létrehozás** ablaktáblában új erőforrásként adja hozzá a projekt egyik csapattagját.

A **Szerepkör** , az **Erőforrásbiztosító egység** és a **Pozíció neve** mezők a feladat személyzeti követelményeinek leírására szolgálnak. A személyzeti attribútumokat és a feladatütemezést a rendelkezésre álló erőforrások megkeresésére használják az adott feladat végrehajtásához.

**Szerepkör** – Adja meg a feladat elvégzéséhez szükséges erőforrás típusát.

**Erőforrásbiztosító egység** – Adja meg azt az egységet, ahonnan megtörténik az erőforrások hozzárendelése a feladathoz. Ez az attribútum befolyásolja a feladat költség- és értékesítési becslését, ha az erőforrás költségét és számlamértékét erőforrásbiztosító egységek alapján állítják be.

**Pozíció neve** – Adjon meg egy barátságos nevet az általános erőforrás számára, hogy a név helyőrzőjeként szolgáljon azon erőforrás számára, amely végül elvégzi majd a munkát.

Az **Erőforrások** mező az általános erőforrás vagy a megnevezett erőforrás pozíciónevét tartalmazza, ha megtalálható valamelyik.

A **Kategória** mező azokat az értékeket tartalmazza, amelyek egy olyan szélesebb körű munkát jelölnek, amelybe a feladat csoportosítható. Ez a mező nem érinti az ütemezést vagy a személyzetet. Csak jelentéskészítéshez használják.

### <a name="task-dependencies"></a>Tevékenység függőségek 

A PSA-ban az ütemezést a feladatok közötti korábbi kapcsolatok létrehozására használhatja. A **Korábbi** mezőben a **Feladatok** alatt egy vagy több értéket vesz fel, hogy jelezze azokat a feladatokat, amelyektől a feladat függ. Ha egy feladathoz korábbi értékek vannak hozzárendelve, akkor a feladat csak a korábbi feladatok elvégzése után indulhat el. A függőség miatt a feladat tervezett kezdő dátumát visszaállítják a korábbi feladatok befejezésének napjára.

A feladat mód nincs hatással a korábbi/függő feladatok kezdő és befejező dátumának frissítéseire.

## <a name="task-mode"></a>Tevékenység mód 

A feladat mód határozza meg a levélcsomópont-feladatok ütemezését. A PSA minden feladathoz két feladatmódot támogat: automatikus ütemezés és kézi ütemezés.

### <a name="auto-scheduling"></a>Automatikus ütemezés 
 
Amikor a feladatmód beállítása **Automatikusan ütemezett** egy feladatnál, a feladatütemező motor ütemezési szabályokat használ a feladatattribútumokon a feladat ütemezésének meghatározására.

#### <a name="scheduling-rules"></a>Ütemezési szabályok

Alapértelmezés szerint, ha a levélcsomópont-feladatnak nincsenek elődei, akkor a kezdési dátum a projekt ütemezett kezdési dátumára lesz állítva. Egy levélcsomópont tevékenység időtartamot mindig a kezdő és befejezési dátumok közötti napok száma szerint számítják ki. Amikor egy feladat automatikusan ütemezett, az ütemező motor a következő szabályokat követi:

- A feladat kezdési és befejezési dátumának munkanapon kell lennie a projekt ütemezési naptárának megfelelően. 
- Bármely olyan feladat esetében, amely korábbi feladatokkal rendelkezik, a kezdő dátum automatikusan az elődei legújabb befejezési dátumára lesz állítva.
- Az erőfeszítést a következő képlet alapján számítják ki: Személyek száma × Időtartam × Órák a projekt naptárában standard munkanapon.

### <a name="manual-scheduling"></a>Kézi ütemezés

Ha az automatikus ütemezés szabályai nem felelnek meg az Ön igényeinek, beállíthatja a feladatmódot **Kézi ütemezés** értékre. Ez a beállítás megakadályozza, hogy az ütemezőmotor kiszámolja a többi ütemezési attribútum értékét. A feladatmódtól függetlenül, ha elődöket állít be a feladatokra, akkor mindig befolyásolni fogja a függő feladat kezdő dátumát.
