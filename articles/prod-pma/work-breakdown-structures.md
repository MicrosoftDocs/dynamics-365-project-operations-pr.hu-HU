---
title: Munkalebontási struktúrák áttekintése
description: A munkalebontási struktúra (WBS) annak a munkának a leírása, amelyet egyadott projekthez készítenek el. Ez a feladatok olyan hierarchiája, amely a projektcsapat munka összetételével, valamint az egyes összetevők vagy feladatok méretével, költségével és időtartamával kapcsolatos ismereteit jelképezi.
author: Yowelle
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eddaf8a868845bde11c8bb7bc04f63777d628cf4
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369424"
---
# <a name="work-breakdown-structures-overview"></a>Munkalebontási struktúrák áttekintése

[!include [banner](../includes/banner.md)]

A munkalebontási struktúra (WBS) annak a munkának a leírása, amelyet egyadott projekthez készítenek el. Ez a feladatok olyan hierarchiája, amely a projektcsapat munka összetételével, valamint az egyes összetevők vagy feladatok méretével, költségével és időtartamával kapcsolatos ismereteit jelképezi. A WBS-nek három fő célja van:

-   A feladatok munkáinak részletezését vagy összetételét írja le.
-   A projektmunka ütemezése.
-   Az egyes feladatok költségének becslése.

A munkalebontási struktúra részletessége a becslések pontosságától, valamint a becslésekhez szükséges nyomonkövetési szinttől függ. Az ütemezési vagy a költségcsúszásokat nehezen megtűrő projektek általában részletesebb WBS-t igényelnek, és a munkafolyamatok és a WBS-hez kapcsolódó költségek gondos nyomon követését is igénylik. Az ilyen jellegű projektek az építőiparban és a mérnöki iparban gyakoriak. 

Ezzel szemben az olyan iparágakban lévő projektek, mint a média és a hirdetések, a szoftverek és az informatikai infrastruktúra általában egyfajta jellegűek, és a termelékenység a feladatot teljesítő egyén tapasztalatainak és kompetenciájának függvénye. Ezért ezek az iparágak a WBS-t a projektek méretének megközelítő becslésére használják, és nem a projekt előrehaladásának részletes nyomon követésére. 

A WBS építése olyan intenzív folyamat, amelyet általában hosszú időszakon keresztül végeznek, és amely emberek széles körétől igényel együttműködést és információkat. Ez a témakör ismerteti, hogyan használhatók a WBS-fejlesztések a becslésekre és a nyomon követésre vonatkozó követelmények teljesítésére.

## <a name="prerequisites-for-creating-a-wbs"></a>A WBS létrehozásának előfeltételei
WBS létrehozásához létre kell hoznia egy munkaütemezést, és meg kell becsülnie a munka költségét.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Munkaütemezés létrehozásának előfeltételei

A WBS-funkciók teljes körű ütemezési képességeinek használatához hajtsa végre a következő beállítást:

1.  Alapértelmezett naptár és projektnaptár beállítása:
    1.  Kattintson a **Projektmenedzsment és könyvelés** &gt; **Beállítás** &gt; **Projektmenedzsment és könyvelési paraméterek** &gt; **Ütemezés** lehetőségre. Az **Alapértelmezett munkanaptár** mezőben adjon meg egy alapértelmezett naptárat. Ez lesz a létrehozott új projektek alapértelmezett munkanaptára.
    2.  Egy adott projekt alapértelmezett naptárát megváltoztathatja. Kattintson a projekt részletei lapra, majd a **Projektcsapat és ütemezés** gyorslapon frissítse az **Ütemezési naptár** mezőt egy másik naptár kiválasztásával.

2.  Standard munkanapok és munkaórák beállítása. A projekt munkanaptáraként beállított naptárat használja a rendszer a WBS-ben a következő információk meghatározásához:

-   Munkanapok és szabadnapok
-   A munkaórák száma egy napon

A naptár munkanapjainak és munkaóráinak beállításához, illetve új naptár létrehozásához kattintson a **Szervezeti adminisztráció** &gt; **Általános** &gt; **Naptárak** lehetőségre.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>A munkaköltségek becslésének előfeltételei

A WBS teljes költségbecslési lehetőségeinek használatához be kell állítania a dolgozók, a munkakategóriák, költségek és díjak, valamint a cikkek költségeit és értékesítési árait.

-   A munka, költség és díj kategóriák költségének és értékesítési árának beállításához kattintson a **Projektmenedzsment és könyvelés** &gt; **Beállítás** &gt; **Árak** lehetőségre.
-   A cikkek költségének és értékesítési árának beállításához használja a **Kiadott termékek** listaoldal egyes cikkeinek **Kereskedelmi megállapodások** oldalát a Termékinformációk kezelése részben.

## <a name="creating-a-wbs"></a>WBS létrehozása
A WBS létrehozása három tevékenységet foglal magában:

1.  **Munkalebontás** – A munka lebontása kezelhető darabokra vagy feladatokra.
2.  **Munkaütemezés** – Becsülje meg a feladat végrehajtásához szükséges időt, állítsa be a feladatfüggőségeket, és válassza ki a feladatok kezdő és záró dátumát.
3.  **Költségbecslés** – Az egyes feladatok becsült költségei.

A következő szakaszok ismertetik, hogyan segíthetnek a WBS-funkciók az egyes tevékenységek végrehajtásában.

### <a name="work-decomposition"></a>Munkalebontás

A munkalebontás vagy -részletezés létrehozása általában az első lépés a WBS létrehozásának folyamatában. A WBS-funkció a következő alapvető konstrukciókat támogatja a munkarészletezéshez vagy lebontáshoz. 

**Projekt gyökérfeladata** A projekt gyökérfeladata a projekt legfelső szintű összefoglaló feladata. Minden más projekttevékenység ez alatt jön létre. A gyökérfeladat nevét mindig a projekt nevére állítják be. A gyökérszintű csomópont ráfordítása, dátumai és időtartama a gyökérfeladat alatti feladatok értékeit foglalja össze. Nem módosíthatja a gyökércsomópont tulajdonságait, és nem törölheti a gyökércsomópontot.

**Összefoglaló vagy tárolófeladatok** Az összefoglaló feladat olyan feladat, amely alatt alfeladatok vagy tagfeladatok vannak. Az összefoglaló tevékenység nem rendelkezik semmilyen munka erőkifejtéssel vagy saját költséggel. Ehelyett az összefoglaló feladat munkaerőfeszítése és -költsége a tagfeladatok munkaerőfeszítésének és költségének összege. A tagfeladatok legkorábbi kezdődátuma kerül felhasználásra az összefoglaló feladat kezdő dátumaként, és a tagfeladatok legutolsó záró dátuma kerül felhasználásra záró dátumként. Módosíthatja az összefoglaló feladat nevét, de nem módosíthatja az erőfeszítés, dátumok és időtartam ütemezési tulajdonságait. Ha töröl egy összefoglaló feladatot, akkor törli az összes tagfeladatot. 

**Levélcsomópont-feladatok** A levélcsomópont-feladat a projekt legrészletesebb munkacsomagját jelenti. A levélcsomópont becsült erőfeszítéssel, az erőforrások tervezett számával, tervezett kezdő és záró dátummal és időtartammal rendelkezik. 

A következő hierarchiaműveletek végrehajtásával engedélyezheti a munkahierarchia létrehozását vagy a projektek lebontását. 

**Új feladat** A létrehozott új feladatok mindegyike automatikusan hozzáadódik a gyökércsomóponthoz, és a rendszer automatikusan hozzárendel egy WBS-számot a feladathoz. A WBS-szám a feladat szintjének felel meg a hierarchiában. Az első szintű feladatokhoz a projekt gyökérfeladata alatt az 1, 2, 3 stb. számozási séma kerül felhasználásra. Az első szint alatti feladatokhoz az 1.1, 1.2, 1.3 stb. számozási séma kerül felhasználásra. Az előző szint alatt hozzáadott minden szint esetén új, pontozott számsorozatot ad hozzá a rendszer. 

Jelenleg nem szabhatja testre a WBS-számozást. 

**Feladat behúzása** Feladat behúzásakor az azt megelőző feladat gyermekévé válik. Az új gyermek feladat WBS-számát a rendszer automatikusan újraszámítja az új szülő WBS-száma alapján. A szülő feladat most egy összefoglaló vagy tárolófeladat, és ezért a tagfeladatok összesítése lesz. 

> [!NOTE] 
> Ha egy olyan feladat alatt húz be feladatokat, amely a behúzási művelet előtt levélcsomópont volt, az újonnan létrehozott összefoglaló feladat elveszíti a saját dátumait, erőfeszítését és erőforrásai számát. Ez most az új tagfeladatainak összesített értékeit használja. 

**Feladat kihúzása** Feladat kihúzásakor a feladat már nem lesz a szülőjének tagfeladata. A feladathoz tartozó WBS-számot a rendszer automatikusan újraszámítja, hogy tükrözze a feladat hierarchiában elfoglalt új szintjét. Az feladat előző szülőfeladatának erőfeszítéseit, költségeit és dátumait újra kiszámítja a rendszer, így azok nem tartalmazzák ezt a feladatot. 

**Mozgatás felfelé és lefelé** Amikor a feljebb és a **Mozgatás felfelé** és **Mozgatás lefelé** lehetőségre kattint, megváltoztatja a feladat pozícióját a szülőjének hierarchiáján belül. A feladat pozíciója nem befolyásolja a feladat erőfeszítését, költségét, dátumait vagy időtartamát. A feladathoz tartozó WBS-számot azonban a rendszer automatikusan újraszámítja, hogy tükrözze a feladat új pozícióját.

### <a name="schedule-estimation"></a>Ütemezés becslése

Az ütemezés becslése általában a második lépés a WBS létrehozásakor. Gyakorlati tanácsként célszerű a feladatok létrehozása után elvégezni az ütemezési becslést. A Pénzügy részben található **Munkalebontási szerkezet** oldal két szakaszból áll. A felső ablaktábla az ütemezések becslésére szolgál, és az alsó ablaktábla tartalmazza a **Becsült költségek és bevételek** lapot, amely a költségbecslés során használható. 
**Feladatfüggőségek** A WBS-ben a feladatok között megelőző kapcsolatot hozhat létre. Ha egy feladathoz megelőző feladatot rendel hozzá, akkor a feladat csak a megelőző feladatok elvégzése után indulhat el. A feladat tervezett kezdési dátuma automatikusan az összes elődje legkésőbbi dátumára van beállítva. 

**Feladatok ütemezése** Az alábbi tényezők határozzák meg a levélcsomópont-feladatok ütemezését:

-   Elődök
-   Erőfeszítés
-   Erőforrások száma
-   Kezdő és befejező dátumok

Egy olyan levélcsomópont-feladat kezdő dátuma, amely nem rendelkezik előzményekkel, automatikusan a projekt ütemezett kezdő dátuma lesz. Egy levélcsomópont tevékenység időtartamot mindig a kezdő és befejezési dátumok közötti napok száma szerint számítják ki. 

*<strong><em>Ütemezési szabályok</em></strong>* Ha az automatikus ütemezési támogatás be van kapcsolva, a következő szabályok vonatkoznak a levélcsomópont-feladatokhoz tartozó feladatok ütemezésére:

-   A feladat kezdési és befejezési dátumának munkanapon kell lennie a projekt ütemezési naptárának megfelelően.
-   Az előzményekkel rendelkező feladat kezdő dátuma automatikusan az előzmény legutóbbi záró dátuma.
-   A feladat erőfeszítését a következőképpen számítja ki automatikusan a rendszer:

Személyek száma × Időtartam × Órák száma a projektnaptár standard munkanapjában. 

Bizonyos esetekben érdemes lehet eltérni ezektől a szabályoktól. Az automatikus ütemezés kikapcsolásával megakadályozhatja, hogy a Pénzügy automatikusan beállítsa vagy kijavítsa a levélcsomópont-feladatok tulajdonságait. Ha egy feladathoz olyan adatokat ad meg, amelyek az ütemezési szabályok megsértését okozzák, a feladathoz egy ütemezési hiba ikon jelenik meg. Ha nem szeretné megjeleníteni az ütemezési hibákat, kattintson az **Ütemezési hibák megjelenítése** lehetőségre, és kapcsolja ki a funkciót. 

> [!NOTE] 
> Az összefoglaló vagy tárolófeladat értékeit a rendszer továbbra is a tagfeladatok értékeinek összegeként számítja ki, függetlenül attól, hogy be van-e kapcsolva az automatikus ütemezési támogatás. 

**Ütemezési hibák javítása** Amikor az automatikus ütemezési támogatás be van kapcsolva, nem valószínű, hogy ütemezési hibák jelentkeznek. Ha azonban kikapcsolja az automatikus ütemezési támogatást, majd később ismét visszakapcsolja, akkor az ütemezési hibák ikonjai megjelenhetnek a WBS-ben. 

**Ütemezési hibák javítása feladatonként** Ha egy adott feladat ütemezési hibájának ikonjára duplán kattint, egy párbeszédpanel megjeleníti az adott feladathoz tartozó összes ütemezési hibát. Eldöntheti, hogy a feladat mely ütemezési hibáit javítja. 

**Összes ütemezési hiba javítása** Ha azt szeretné, hogy a Pénzügy az összes ütemezési hibát kijavítsa a WBS-ben, akkor a Művelet panelen kattintson az **Összes ütemezési eltérés javítása** lehetőségre. 

> [!NOTE] 
> Ez a funkció jelentős módosításokat okozhat a WBS-ben. A hibákat a következő sorrendben kell kijavítani:

1.  A rendszer minden feladatra vonatkozóan módosítja a becsült erőfeszítést, így az megegyezik a projektnaptárban meghatározott kapacitással.
2.  Az egyes feladatok kezdési dátuma úgy módosul, hogy a feladat az megelőző feladatok befejezését követően induljon el.
3.  Az egyes feladatok kezdési dátuma úgy módosul, hogy a megelőző feladatok kezdési dátumai közötti hézagok el legyenek távolítva.

### <a name="cost-estimation"></a>Költségbecslés

A dokumentumban korábban említettek szerint az egyes levélcsomópontok feladataihoz tartozó költségbecslés a **Munkalebontási struktúra** oldal alsó panelén található **Becsült költségek és bevételek** lapon adható meg. 

> [!NOTE] 
> Az összefoglaló vagy tárolófeladathoz tartozó költségbecslés nem módosítható. Az összefoglaló feladathoz tartozó költségbecslés megegyezik a levélcsomópontjai költségbecsléseinek összegével. Az egyes feladatok becsült teljes költségét a rendszer a következő tranzakciótípusok becsült költségösszegeinek összegeként számítja ki:

-   Munka
-   Cikk vagy anyag
-   Költségek

A **Díj** tranzakciótípus a díjalapú bevétel becslésére szolgál. Ez a tranzakciótípus nem tartalmaz költségösszetevőt, ezért a költségbecslésben nem kerül figyelembevételre. 

A **Számlán** tranzakciótípus a szerződött értékesítési érték rögzítésére szolgál a rögzített érték típusú projektekben. Ez a tranzakciótípus szintén nem kerül figyelembevételre a költségbecslésben. 

Amikor megbecsüli a munka, az anyagok és a kiadások költségeit az egyes feladatokhoz, akkor a becsült költséghez hozzá kell rendelnie egy projektkategóriát. 

**Munkaerőköltségek becslése** Minden levélcsomópont-feladathoz órában számított munkaerőfeszítést és alapértelmezett kategóriát kell hozzárendelni. Ezért ha egy feladathoz ütemezést állít be, akkor a program automatikusan hozzáadja az adott tevékenységre vonatkozó munkaköltségbecslést a munka alapértelmezett kategóriájában. Ez a költségbecslés a **Becsült árbevétel és költségek** lapon jelenik meg, a feladat **Sor adatai** rácsában. Ha több munkaköltség-becslésre van szüksége, akkor ezen a lapon adhatja meg azokat. Ha növeli vagy csökkenti a munkaköltségbecslés óráit, a feladat ütemezését a rendszer automatikusan újraszámítja. 

**Költségek és anyagköltségek becslése** A **Becsült árbevétel és költségek** lapon lehetősége van lehetősége van a feladathoz tartozó költségek és anyagköltségek becslésére is, ha becslésre van szüksége. 

Az egyes munka- és költségbecsléssorokhoz tartozó költség és értékesítési ár a **Projektmenedzsment és könyvelés** &gt; **Beállítások** &gt; **Árképzés** alatti árképzési táblák kategóriáihoz megadott beállításon alapulnak. A cikkek esetében a költség és az értékesítési ár alapértelmezésben a **Kiadott termékek** listaoldal cikk vagy kereskedelmi megállapodás részéből kerül hozzáadásra a Termékinformációk kezelése részben.

## <a name="tracking-progress-on-the-wbs"></a>A WBS előrehaladásának nyomon követése
Egyes iparágak nagyon részletes szinten követik nyomon a projekt haladását a WBS alapján, míg mások a WBS magasabb szintjén követik a haladást. Ez a szakasz azt mutatja be, hogyan használható a WBS-követés a projekt követelményei esetében. 

A pénzügy három nézetet tartalmaz a projekt WBS-éhez: a Tervezési nézet, az Erőfeszítés-követési nézetet és a Költségkövetési nézetet.

### <a name="planning-view"></a>Tervezési nézet

A Tervezési nézet az ütemezésre és a költségre vonatkozó információk tervezett vagy alap becslését jeleníti meg. Bár nincsenek a projekt WBS verzióinak és alapértékeinek követésére szolgáló funkciók, az ebben a nézetben szereplő értékek az alapverziót képviselik. Ennek a témakörnek az Ütemezés becslése és a Költségbecslés szakaszai ezt a nézetet mutatják be, valamint azt, hogy milyen módon lehet a használatával WBS-t létrehozni.

### <a name="effort-tracking-view"></a>Erőfeszítések nyomon követésének megtekintése

Az Erőfeszítés követése nézet megjeleníti a feladatok előrehaladásának követését a WBS-ben. Összehasonlítja a feladat halmozott tényleges munkaóráit a tervezett munkaórákkal. A következő képletek az Erőfeszítés követése nézet értékeit adják meg:

-   Haladás százaléka = az eddigi tényleges erőfeszítés ÷ a feladathoz tervezett erőfeszítés
-   Hátralévő erőfeszítés (más néven Becslés a befejezéshez \[ETC – Estimate-to-complete\]) = tervezett erőfeszítés – az eddigi tényleges erőfeszítés
-   Teljes becslés (EAC) = fennmaradó erőfeszítés + az eddigi tényleges erőfeszítés
-   Tervezett erőfeszítés szórása = Tervezett erőfeszítés - EAC

Az Erőfeszítés nyomon követése nézet megjeleníti a feladat munkamennyiség-ingadozásának leképezését, attól függően, hogy az EAC nagyobb vagy kisebb-e, mint a tervezett erőfeszítés:

-   Ha az EAC meghaladja a tervezett erőfeszítéseket, akkor a feladat várhatóan több időt vesz igénybe, mint az eredetileg tervezték, és elmarad az ütemtervtől.
-   Ha az EAC kevesebb, mint a tervezett erőfeszítés, akkor a feladat várhatóan kevesebb időt vesz igénybe, mint az eredetileg tervezték, és előrehaladottabb állapotban van az ütemtervhez képest.

**Az erőfeszítések projektvezető általi újratervezése** Előfordulhat, hogy a projektmenedzsernek vagy egy másik, a projekt előrehaladását nyomon követő személynek felül kell vizsgálnia egy feladat eredeti becsléseit. Előfordulhat, hogy a feladat különböző okokból gyorsabban vagy lassabban halad, mint azt eredetileg várták. Előfordulhat például, hogy a hatókört szűkítették, vagy a munkavállalóknak kevesebb tapasztalata van, mint az eredetileg tervezték. A leképezések a projektmenedzser becslésről alkotott felfogása a projekt jelenlegi állapota alapján. Általánosságban nem ajánlott az alapértékek módosítása, mivel a projekt alapértéke a projekt ütemezésének és költségének becsült, széles körben közzétett dokumentuma, amelyet minden projektben érdekelt fél elfogadott. 

Kétféle módon tudja egy projektmenedzser módosítani a feladatok erőfeszítéseit:

-   Módosítja a hátralévő erőfeszítést, amelyet a rendszer automatikusan beállít a feladathoz tartozó tényleges hátralévő erőfeszítés frissítéséhez.
-   Módosítja a az előrehalaás százalékát, amelyet a rendszer automatikusan beállít a feladathoz tartozó tényleges előrehaladás frissítéséhez.

Mindkét megközelítés esetében átszámításra kerül a feladat ETC-je, EAC-je és az előrehaladási százalék, valamint a feladat várható erőfeszítésének varianciája. Az EAC, az ETC-t és az összefoglaló feladatok előrehaladási százalékát szintén újraszámolják, és frissítik a leképezett erőfeszítés-varianciát. 

**Módosított erőfeszítés az összefoglaló feladatok esetében** Módosíthatja az összefoglaló vagy tárolófeladatok erőfeszítését. Függetlenül attól, hogy ezeket az értékeket a fennmaradó erőfeszítéssel vagy az előrehaladás százalékával módosítja-e az összefoglaló feladatok esetében, a számítások automatikusan, a következő sorrendben kerülnek végrehajásra:

1.  Kiszámítják az EAC, ETC és a feladat előrehaladási százalékát.
2.  Az új EAC ugyanabban az arányban lesz szétosztva a gyermek feladatokra, mint az eredti EAC összeg.
3.  A rendszer kiszámítja az összes levélcsomópont-feladat új EAC-jét.
4.  A program az új EAC érték alapján újraszámítja a hátralévő erőfeszítést és az előrehaladási százalékot az összes érintett gyermek feladathoz. A program újraszámítja a feladatok erőfeszítésének szórását is.
5.  A program az összefoglaló feladatok EAC értékét is újraszámítja a levélcsomópontokból.

Ha meg szeretné adni, hogy milyen szinten történjen a WBS követése és karbantartása, kattintson a **Kibontás a szintre** lehetőségre az Erőfeszítés követése nézetben. A WBS automatikusan kibontásra kerül arra a szintre az Erőfeszítés követése nézetben, amikor megnyitja azt.

### <a name="cost-tracking-view"></a>Költségkövetési nézet

A Költségkövetés nézet egy feladat költségfelhasználásának nyomon követését jeleníti meg. Ebben a nézetben a feladatra a dátumig elköltött tényleges költséget a rendszer a feladathoz tartozó tervezett költséggel hasonlítja össze. A következő képletek a Költségkövetés nézet értékeit adják meg:

-   A felhasznált költség százalékos aránya = a mai napig ténylegesen elköltött költség ÷ A feladat tervezett költsége
-   Teljes költség (CTC) = Tervezett költség - a mai napig ténylegesen elköltött költség
-   Teljes becslés (EAC) = CTC + a mai napig ténylegesen elköltött költség
-   Tervezett költség szórás = Tervezett költség - EAC

Az Költségkövetés nézet megjeleníti a feladat költségingadozásának leképezését, attól függően, hogy az EAC nagyobb vagy kisebb-e, mint a tervezett költség:

-   Ha az EAC meghaladja a tervezett költséget, akkor a feladat várhatóan több pénzt vesz igénybe, mint azt eredetileg tervezték, és túllépi a költségvetést.
-   Ha az EAC kevesebb, mint a tervezett költség, akkor a feladat várhatóan kevesebb pénzt vesz igénybe, mint azt eredetileg tervezték, és nem éri el a költségvetést.

**A költség projektmenedzser általi újratervezése** A projektmenedzsereknek a CTC segítségével kell átvizsgálniuk az eredeti költségbecslést egy feladatra vonatkozóan. A projektmenedzser módosíthatja a CTC értékét a feladat végrehajtásához szükséges költségre. Ha módosítja a CTC értékét, akkor a program újra kiszámítja az adott feladathoz tartozó CTC, EAC és a felhasznált költség százalékos értékét, valamint a tervezett költség szórását a feladat esetében. Az EAC, az ETC és az felhasznált költség százalékos aránya az összefoglaló feladatok esetében szintén újraszámításra kerül, és frissítve lesz a tervezett költségszórásuk is. 

> [!NOTE] 
> Ha az Erőfeszítés követése nézetben módosítja a WBS-feladatokra vonatkozó erőfeszítést, akkor a program a Költségkövetés nézetben újraszámítja a feladat CTC, EAC értékét, a felhasznált költség százalékos arányát és a tervezett költségszórást. A költségek módosítása azonban nem befolyásolja az Erőfeszítés követése nézet értékeit, mert a tranzakciótípusok (munka, anyag vagy költség) vagy a projektkategóriák szerinti költségek nem kerülnek módosításra. 

**Összefoglaló feladatokra vonatkozó költségtervek áttekintése** Felülvizsgálhatja az Összefoglaló feladatokhoz tartozó költségeket, és a számítások automatikusan, a következő sorrendben történek:

1.  A rendszer újra kiszámítja a feladathoz tartozó EAC, CTC értéket és a felhasznált költség százalékos arányát.
2.  Az új EAC lebontásra kerül a gyermek feladatokra ugyanolyan arányban, mint az eredeti EAC a feladatokra.
3.  A rendszer kiszámítja az egyes feladatok új EAC-értékét.
4.  A CTS-t és a felhasznált költség százalékos arányát a rendszer újraszámítja az érintett gyermek feladatokhoz az EAC értéke alapján. A program újraszámítja a feladatok költségszórását is.
5.  A módosítás alapján a rendszer újraszámítja az összes összefoglaló feladathoz tartozó EAC-t.

Ha meg szeretné adni, hogy milyen szinten történjen a WBS követése és karbantartása, kattintson a **Kibontás a szintre** lehetőségre a Költségkövetés nézetben. A WBS kibontásra kerül arra a szintre a Költségkövetés nézetben, amikor megnyitja azt.

### <a name="earned-value-management"></a>Létrehozottérték-kezelés

A létrehozott érték módszer (EVM) segítségével nyomon követheti a projekt előrehaladását. A létrehozottérték-mérőszámok a projektmenedzser Szerepkörközpontjában tekinthetők meg. A létrehozottérték-diagram összetevő a tervezett és a tényleges költség időszakos értékeit jeleníti meg. Az aktuális dátumhoz tartozó létrehozott érték pontként jelennek meg. A létrehozott értékre vonatkozó időszakos adatok jelenleg nem érhetők el. 

A létrehozottérték-diagram időfázisa hét vagy hónap szerint jelenik meg. Ez a szakasz az EVM három pillérét ismerteti: a tervezett értéket, a létrehozott értéket és a tényleges költséget. 

**A tervezett érték** EVM elmélete kimondja, hogy a tervezett érték azt a kamatlábat képviseli, amellyel a projekt csapata a projekten értéket tervez realizálni. 

A pénzügy a 0:100 kereseti szabályt használja, amikor a tervezett értéket ábrázolja. A szabály szerint a feladat a befejező dátumától kerül feladásra a feladat értéke a feladathoz. Az érték csak akkor kerül könyvelésre, ha a feladat 100 százalékosan be van befejezve. 

A Projektmenedzsment és könyvelés részben meg kell adnia a levélcsomópontok záró dátumát és a tervezett költséget. Ha a tervezett érték grafikonja hét szerint jelenik meg, a tervezett érték hét szerint van összesítve az összes levélcsomópont-feladat esetében, a projekt időtartamára vonatkozóan. 

**Létrehozott érték** Az EVM elmélete szerint a létrehozott érték azt a kamatlábat képviseli, amellyel a projekt csapata a projekten ténylegesen realizálta az értéket. 

A pénzügy a 0:100 kereseti szabályt használja, amikor a létrehozott értéket ábrázolja. A szabály szerint a feladat a befejező dátumától kerül feladásra a feladat értéke a feladathoz. Az érték csak akkor kerül könyvelésre, ha a feladat 100 százalékosan be van befejezve. 

A létrehozott érték kiszámításakor figyelembe veszik az egyes feladatok előrehaladási százalékát. Az 0:100 kereseti szabály értelmében csak egy adott időszakban befejezett feladatok vehetők figyelembe a létrehozott értéknek az adott időszak végén történő számításakor. A projekt létrehozott értéket a rendszer a diagram létrehozásakor befejezett összes feladatra kiszámítja. 

> [!NOTE] 
> A WBS-követés rendszere jelenleg nem rendelkezik az egyes feladatok előrehaladási százalék előzményeinek tárolására szolgáló adatstruktúrákkal. A létrehozott értékek ezért csak a kocka feldolgozásának időpontjára vonatkozóan jeleníthetők meg. A kockát rendszeresen dolgozza fel a Szerepkörközpontban megjelenített létrehozottérték-adatok frissítéséhez. 

**Tényleges költség** Az EVM elmélet szerint, a tényleges költség képviseli azt az arányt, amellyel pénzt költenek a projektre. 

A projektbe kiküldött tranzakciók a tényleges költségsor ábrázolására szolgálnak. A költségeket dátum szerint összesítik. Ezeket az adatokat a program a tényleges költségek hét vagy hónap szerint történő ábrázolására használja a létrehozottérték-diagramon.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>A tervezett érték, a létrehozott érték és a tényleges költség koncepcióinak használata

**Ütemezés szórása** A tervezés során az idősoron végzett munkára vonatkozó előrejelzést hoz létre. Ezért a tervezett érték az a kamatláb, amely mellett a projekttervezők elképzelései szerint a projekt kivitelezésre kerül. Miután a projekt folyamatban van, a munkavégzés befejeződik, és a projekt értéket hoz létre. A tervezett érték és a létrehozott érték összehasonlításával megtekintheti, hogyan halad a munka a projekten. Az összehasonlítás eredménye az ütemezés szórása. 

Ha egy adott időszakra vonatkozóan a tervezett érték nagyobb, mint a létrehozott érték, a projekten végzett munka mennyisége kevesebb, mint a tervezett. A projekt emiatt elmarad az ütemtervtől. Mivel a tervezett érték és a létrehozott érték pénzösszegben van kifejezve, a projekt késése is pénzbeli értéket kap. 

Ha egy adott időszakra vonatkozóan a tervezett érték kisebb, mint a létrehozott érték, a projekten végzett munka mennyisége több, mint a tervezett. A projekt emiatt előrehaladottabb állapotban van az ütemtervhez képest. Ez az előny ideje is pénzbeli értéket kap.

**Költségszórás** Mivel a létrehozott érték az önköltségi árat használja szorzóként, a létrehozott érték a projekten végzett munka költségét jelzi. A projekt előrehaladtával a tranzakciónapló egy olyan rekordot biztosít, amely a ténylegesen a projektre költött pénzt tükrözi. Ha összehasonlítja a létrehozott értéket a tényleges költséggel, megtekintheti az elköltött pénzösszeget a létrehozott értékhez viszonyítva. Az összehasonlítás eredménye a költség szórása. 

Ha az adott időszakra fordított tényleges költség nagyobb, mint a létrehozott érték, több pénzt lett elköltve, mint amennyi érték létrejött. A projekt tehát túllépte a költségvetést. 

Ha az adott időszakra fordított tényleges költség kisebb, mint a létrehozott érték, több pénzt hozott létre, mint amennyit elköltöttek rá. A projekt tehát a költségvetésen belül van.

## <a name="wbs-templates"></a>WBS-sablonok
A WBS-sablonok funkció segítségével szabványos sablonokat hozhat létre a projektek számára. Ha a vállalat által kínált projektek sok ismételhető munkát foglalnak magukban, érdemes WBS-sablont létrehozni. 

A meglévő projektek WBS-listájából is létrehozhat WBS-sablont, így a projekt tervezése során összegyűjtött tudást és gyakorlati tanácsokat a későbbiekben is felhasználhatja hasonló projektekre. Néha azonban előfordulhat, hogy nincs értelme a teljes WBS sablonként való mentésére. Ebből kifolyólag a projekt WBS elemeiből is létrehozhat sablonokat.

### <a name="saving-a-projects-wbs-as-a-template"></a>A projekt WBS sablonként történő mentése

A sablon létrehozása után importálhatja azt egy új projekt WBS-be a gyökércsomópont alatt, vagy a projekt WBS-ben szereplő bármely feladat alatt.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>WBS-sablon importálása a projekt WBS-be

A feladatok importálásakor a rendszer a sablonban szereplő feladatokat annak a feladatnak a kezdő dátuma alapján rendezi, amely alatt importálva lettek. Az importálás során a sablonok feladatainak megelőző kapcsolatait a rendszer az importált feladatok kezdő dátumainak kiszámítására használja. A rendszer az importált feladatok befejezési dátumainak kiszámításához a célprojekt általános munkanaptárát alkalmazza, így az aktuális projekt munkanaptárában definiált munkanapokat és standard munkaórákat megőrzi a program. 

A becslési sorok költségösszegeinek és értékesítési árainak alkalmazása biztosítja, hogy a projekthez vagy a projektszerződéshez tartozó árak érvényes dátummal rendelkezzenek.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>A projekt WBS és a WBS-sablon közötti különbségek

-   A WBS-sablonokban szereplő feladatok nem rendelkeznek kezdő és záró dátummal.

A munkanapok és munkaszüneti napok nem állíthatók be a WBS-sablonokhoz.

-   A WBS-sablonok mindig az ütemezési naptárat használják, amely minden projekthez alapértelmezett naptárként van beállítva.

Az alapértelmezett ütemezési naptár csak a standard munkanapok óráinak megállapítására szolgál.

-   A megelőző kapcsolatok nincsenek a WBS-sablonba másolva.

Mivel a WBS-sablonok nem rendelkeznek dátumokkal, a megelőző záró dátumon alapuló kezdő dátum nem kötelező.

-   A program automatikusan létrehozza a munkaköltség becslési sorát, amikor egy WBS-sablonban létrejön egy feladat. Az értékesítési ár és a költség összege a kijelölt munkásról kerül másolásra.

A költség és a cikk költségei manuálisan is létrehozhatók, csakúgy, mint egy projekt WBS-en.

-   Az ütemezési hibák akkor jelennek meg, ha eltérések vannak a következő képlettől:

Erőfeszítés = erőforrások száma × időtartam × a standard munkanap óráinak száma 

Az összes ütemezési hibát kijavíthatja egyidejűleg az **Összes ütemezési hiba javítása** lehetőségre kattintva. 

Másik lehetőségként az ütemezési hibákat egyenként is kijavíthatja, ha az egyes feladatok figyelmeztető ikonjára kattint.





[!INCLUDE[footer-include](../includes/footer-banner.md)]