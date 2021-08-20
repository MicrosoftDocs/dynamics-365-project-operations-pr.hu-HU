---
title: Projekt ütemezése munkalebontási szerkezettel
description: Projekt ütemezése munkalebontási struktúrával a Project Service szolgáltatásban
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 896f19746bde1ba6cf2acd6d558137f4271a5cd99424043053eefe128d3b4250
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996799"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Projekt ütemezése munkalebontási struktúrával (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

A projektütemterv adja meg, hogy milyen munkát kell végezni, milyen erőforrások végzik a munkát és az időkeretet, amelyben a munkát el kell végezni. A projekt ütemterv tükrözi az összes projekt elküldésével időben társított munkát. A projekt kezdeményezési szakaszában az első lépések egyike egy projekt ütemezéssel kell együtt megjelennie. Egy projektütemezés létrehozásásához, egy munkalebontási szerkezetet kell létrehoznia.  
  
 Hozzon létre munkalebontási szerkezettel rendelkező projekt ütemezést, amely segít :  
  
- Bontsa le a munkát kezelhető feladatokra  
  
- Végezze el a feladat befejezéséhez szükséges idő becslését  
  
- Állítsa be függőségeket és feladat időtartamát  
  
- Határozza meg az egyes feladatok elvégzéséhez szükséges szerepeket  
  
  A projekt ütemtervét a munkalebontási szerkezetben a projekt ütemezésnek ismert megjelenése és működése van, egy interaktív Gantt-diagrammal végezze el a befejezését.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Hozzon létre a projekt számára munkalebontási struktúrát  
 Hozzon létre munkalebontási szerkezetet a projektben a feladatok sorozatának jelképezéséhez. A munkalebontási szerkezet tartalmazza a tevékenységeket, követelményeket minden egyes tevékenység számára, és a bevétel-és költségadatokat. A munkalebontási szerkezetben megadhatja:  
  
-   A hierarchiában a tevékenységek sorozata  
  
-   Az egyéb tevékenységeket – ha, van ilyen – el kell végezni egy feladat elindítása előtt.  
  
-   A kezdő dátum, záró dátum, és a tevékenység időtartama  
  
-   A feladathoz szükséges órák száma  
  
-   Bármely szükséges munkavállalói képesség és oktatás  
  
-   A munkavállalók, akik hozzá vannak rendelve a tevékenységhez  
  
-   Becsült árbevétel és költségek  
  
## <a name="task-types"></a>Feladattípusok  
A következő típusú feladatokat fogja használni, a munkalebontási szerkezet létrehozásakor:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Projekt gyökércsomópontja** | A felső szintű összefoglaló tevékenység a projekt számára. Minden más projekttevékenység ez alapján jönnek létre. A legfelső szintű gyökér tevékenység neve a projekt neve. Az erőkifejtés, a dátumok és a gyökércsomópont időtartama a hierarchiában lenn található értékeken alapulnak. Nem módosíthatja a gyökér csomópont tulajdonságait vagy törölheti a gyökér csomópontot. | 
| **Összefoglaló vagy tárolófeladatok** | Összefoglaló tevékenység az a tevékenység, amely alatta altevékenységekkel rendelkezik. Az összefoglaló tevékenység nem rendelkezik semmilyen munka erőkifejtéssel vagy saját költséggel. A munka erőfeszítés és költség az altevékenységeinek összesítése. Módosíthatja az összefoglaló tevékenység nevét, de nem módosíthatja az erőkifejtést, a dátumokat, vagy az időtartamot, mert azokat automatikusan számítják ki. Az összegző tevékenység törlésével törlődik a feladat és az összes altevékenysége.|  
| **Levélcsomópont-feladatok** | A levél csomópont feladat jelöli a legrészletesebb munkát a projekten. Becsült erőkifejtéssel, az erőforrások tervezett számával, tervezett kezdési és befejezési dátummal és időtartammal rendelkezik.|

  
## <a name="task-hierarchy"></a>Feladat hierarchia  
 Feladat hierarchia létrehozásakor a következő lehetőségei vannak:  
  
- **Feladat hozzáadása**.   Egy pozícióban hozzáadhat egy feladatot, amelyet a feladat hierarchiában választ ki. Ha nem ad meg egy helyet, az új tevékenység végén jelenik meg.  
  
- **Tevékenység behúzása**.   Tervezzen meg egy feladatot a feladat utóda létrehozásához közvetlenül felette.  
  
- **Tevékenység kihúzása**.   Húzza ki egy tevékenységet ahhoz, hogy az eredeti szülő feladata altevékenységek ne legyen tovább érvényes.  
  
- **Mozgatás fel és Mozgatás le**.   Mozgassa fel és le a tevékenységeket a szülő feladata hierarchiájában. Tevékenység felfelé vagy lefelé helyezéséhez nem befolyásolja az erőforrást, a költséget, a dátumokat vagy az időtartamot.  
  
## <a name="task-attributes"></a>Feladat attribútumok  
 A tevékenység neve leírja az elvégzendő munkát. Különböző feladat attribútumok segítségével leírhatja a feladathoz az ütemezést és a munkaerő-szükségletet.  
  
### <a name="schedule-attributes"></a>Attribútumok ütemezése

 - Értékek hozzárendelése **Munkaórákhoz**, **Erőforrások számához**, **Kezdő dátumhoz**, **Befejezési dátumhoz**, és **időtartamhoz** a feladat ütemezésének meghatározása érdekében. 
 - **Erőfeszítés** a feladat elvégzéséhez szükséges órák becsült értéke.
 - **Erőforrások száma** egy becslés, amit a projekt menedzser a feladatba juttat annak érdekében, hogy a lehető legjobb ütemezést eredményezze. 
 - **Időtartam** (napokban) jelzi azon munka napok számát, amely a feladat végrehajtásához szükséges.  
  
### <a name="staffing-attributes"></a>Munkaerő-attribútumok

 - **Szerepkör**, **Erőforrás szervezeti egység**, **Erőforrások száma**, és **Erőforrások** leírják a munkaerő-szükségleteit a feladat számára. 
 - **Szerepkör** leírja a feladat elvégzéséhez szükséges erőforrások típusát. 
 - **Erőforrás szervezeti egység** jelzi, hogy a szervezeti egységet, amelyből az erőforrásokat személyzettel kell ellátni a tevékenység számára, ami hatással van a feladat költségi- és az értékesítési becslésére, mivel az erőforráshoz tartozó egység költségi árának meghatározását igazolja. 
 - **Erőforrások** tartalmazza az általános erőforrást vagy elnevezett erőforrást, amikor talál egyet.  
  
## <a name="task-dependencies"></a>Tevékenység függőségek  
 A munkalebontási szerkezetben lévő egy vagy több tevékenységei között megelőző kapcsolatokat hozhat létre. A feladathoz tartozó megelőző mező számára egy vagy több értéket állíthat be annak érdekében, hogy jelezze a tevékenységeket, amelyek rá vannak utalva. Amikor hozzárendel a tevékenységhez egy megelőző értéket, a feladat csak akkor indulhat el, amikor az összes megelőző tevékenység befejeződött. A feladaton a függőség beállítása a feladat tervezett kezdeti dátum újraszámítást az összes előzmény legutolsó végeként eredményezi. Az ütemezés megelőző jellegű hatásai nincsenek korlátozva a feladaton meghatározott feladat mód által.  
  
## <a name="task-mode"></a>Tevékenység mód  
 Tevékenység ütemezése azon fontos tényezők egyik, amelyek meghatározzák a levél csomópont feladatok ütemezése. Kétféle feladat mód tartozik minden egyes feladathoz: automatikus és kézi ütemezési mód..  
  
-   **Automatikus ütemezés**.   Amikor Automatikusan ütemezett módra állítja a feladatot, a feladatütemezési eszköz a következő feladatattribútumokra alkalmazza az ütemezési szabályokat, annak érdekében, hogy meghatározza az ütemezést a feladat számára:  
  
    -   Megelőző tevékenységek  
  
    -   Erőfeszítés  
  
    -   Erőforrások száma  
  
    -   Kezdő és befejező dátumok  
  
-   **Ütemezési szabályok**.   Egy olyan levélcsomópont-feladat kezdő dátuma, amely nem rendelkezik előzményekkel, alapértelmezés szerint a projekt ütemezett kezdő dátuma lesz. Egy levélcsomópont tevékenység időtartamot mindig a kezdő és befejezési dátumok közötti napok száma szerint számítják ki. Amikor a rendszer automatikusan beütemez egy feladatot, az ütemezési motor az alábbi szabályokat követi:  
  
    -   A feladat kezdő és záró dátumainak mindig munkanapoknak kell lennie a projektütemezési naptár szerint  
  
    -   Az előzményekkel rendelkező feladat kezdő dátuma alapértelmezés szerint az előzmény legutóbbi záró dátuma.  
  
    -   Tevékenység = Személyek száma * Időtartam * a projektnaptárban megjelenő szokásos munkanapok órái  
  
-   **Kézi ütemezés**.   Bizonyos esetekben érdemes lehet eltérni ezektől a szabályoktól. Ezekben az esetekben beállíthatja a tevékenységi módot a manuálisan ütemezendő feladat számára. Ez leállítja az ütemezési motort a többi ütemezési attribútum értékeinek kiszámításából. A tevékenység megelőző tevékenységek mindig befolyásolják a függő tevékenység kezdési dátumát.  
  
## <a name="create-a-work-breakdown-structure"></a>Hozzon létre a projekt számára munkalebontási struktúrát  
  
1.  Lépjen a **Project Service > Projektek** pontba.  
  
2.  Kattintson arra a projektre, amellyel dolgozni szeretne.  
  
3.  A képernyő felső részén található sávon válassza ki a projekt neve melletti, lefelé mutató nyilat, majd kattintson a Munkalebontási struktúra lehetőségre.  
  
4.  Feladat hozzáadásához kattintson a **Feladat hozzáadása**. Töltse ki a kötelező mezőket a feladathoz, és kattintson a **Mentés** gombra.  
  
5.  Folytassa a tevékenységek hozzáadásával, amíg befejeződik a munkalebontási szerkezet. A munkalebontási szerkezet létrehozásakor a következőket teheti a feladatok rendszerezése érdekében:  
  
    -   Jelöljön ki egy tevékenységet, és kattintson a **Behúzás** lehetőségre annak érdekében, hogy egy másik tevékenység alá helyezze, vagy kattintson a Kihúzás elemre a szintből történő kihúzás érdekében.  
  
    -   Jelöljön ki egy feladatot, és kattintson a **Mozgatás fel** vagy **Mozgatás Le** lehetőségre a listában történő fel- és lemozgatáshoz.  
  
    -   Kattintson a **Gantt elrejtése** elemre a Gantt diagram elrejtéséhez, majd kattintson a **Gantt megjelenítése** elemre az újbóli megjelenítéshez.  
  
    -   Jelöljön ki a Gantt-diagram számára egy másik időszakot az **Időskála** mezőben.  
  
6.  A munkalebontási struktúrában megadott szerepek projekt csapattagokhoz való hozzáadásához kattintson a **Projektcsoport létrehozása** lehetőségre.  
  
7.  Ha elkészült a módosításokkal, kattintson a **Mentés** lehetőségre a képernyő jobb alsó sarkában.  
  
### <a name="see-also"></a>Kapcsolódó információk  
 [Projektmenedzseri útmutató](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]