---
title: Újdonságok és változások a Project Service Automation 3. verziójában
description: Ez a témakör információkat nyújt arról, hogy milyen újdonságok és változások vannak a Project Service Automation 3. verziójában.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6ce4c549b04716d466efa262dbc6a4abf28ea9eb
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150671"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Újdonságok és változások a Project Service Automation 3. verziójában

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ez a témakör információkat ad a felhasználói felület (UI), a funkcionalitás és a terminológia változásairól a Project Service Automation programban a 2. vagy 1. verzió és a 3. verzió között.

## <a name="project-scheduling"></a>Projekt ütemezése
A korábbi verziókban Work Breakdown Structure (WBS) néven ismert projektütemezést átneveztük Ütemezésre, és az **Ütemezés** fülre kattintva érhető el. 

![Projekt ütemezése](media/psa-schedule-01.png)

Az ütemezés egy új felületet kínál az interakciókhoz, amely modern és könnyen kezelhető. Ugyanakkor az alapul szolgáló Project Service Automation ütemezés motorja nem változott. Az ütemezési rács szalagján lévő vezérlőgombok lehetővé teszik, hogy az ütemezéssel műveletet végezzen, mint a Project Service Automation előző verziójában. Az ütemterv további változásai a következők:

- **Gantt-diagram** - A Gantt-diagram már nem létezik. Egy új Gannt-diagram visszatér egy későbbi frissítésben.
- **Oszlopfejlécek** - Az oszlopfejléceket elrejtheti a rácsban, ha az oszlopcím melletti lefelé mutató nyílra kattint. 
- **Oszlopok** - A rejtett oszlopokat az **Oszlop hozzáadása** elemre kattintva jelenítheti meg. 
- **Tranzakciós kategória** - A **Tranzakciós kategória** keresés hozzáadódott az ütemezési rácshoz, és alapértelmezés szerint megjelenik. 
 
## <a name="project-templates"></a>Projektsablonok
A következő változtatások történtek a projektsablon funkciókban.

### <a name="create-a-project-template"></a>Projektsablon létrehozása 
A Project Service Automation előző verzióihoz hasonlóan a 3. változatban is létrehozhat egy projektsablont. A sablon csak ütemezést tartalmazhat, és az ütemezés hozzárendeléseket is tartalmazhat, de ez nem kötelező. Ha az ütemezésnek vannak hozzárendelései, akkor csak általános erőforrásokra vonatkozhatnak. Létrehozhat erőforrásigényeket az általános erőforrásokhoz, de ezeket nem lehet valós erőforrásokkal lefoglalni a sablonban. Nem foglalhat le valódi erőforrást egy csapat számára sablonban. 

### <a name="create-a-template-from-an-existing-template"></a>Sablon létrehozása egy meglévő sablonból
Amikor új projektsablont hoz létre egy meglévő sablonból a Project Service Automation 3. verziójában, a következő történik: 

- A forrásprojekt ütemezése lemásolásra kerül a sablonba. 
- Az általános erőforrásokat a csapatba másolják, és az összes általános erőforrás-hozzárendelés átmásolódik. Az általános erőforrásokra vonatkozó követelmények nem kerülnek átmásolásra. 

### <a name="create-a-template-from-an-existing-project"></a>Sablon létrehozása meglévő projektből
Amikor egy meglévő projektből új projektsablont hoz létre, a következő történik: 

- A forrásprojekt ütemezése lemásolásra kerül a sablonba. 
- Az általános erőforrásokat a csapatba másolják, és az összes általános erőforrás-hozzárendelés megőrződik. Az általános erőforrásokra vonatkozó követelmények nem kerülnek átmásolásra.    
- A kiosztott vagy nem kiosztott, megnevezett erőforrásokat eltávolítják a csapatból, és helyettesítik az általános erőforrásokkal.
- Ha vannak, az ügyféladatokat eltávolítják. 
- Ha vannak ilyenek, akkor az árajánlatokra és a szerződésekre való hivatkozásokat eltávolítják. 

### <a name="create-a-project-from-a-template"></a>Projekt létrehozása sablonból
Amikor új projektsablont hoz létre egy meglévő sablonból a Project Service Automation 3. verziójában, a következő történik:

- Az ütemezés, a csapat és a feladatok másolódnak az új projektbe.   
- A kezdő dátum vagy a másolás dátuma, vagy a felhasználó által kiválasztott dátum.   
- A sablonban erőforrás-követelményekkel rendelkező általános csapattagok esetén a követelményeket nem másolja vagy generálja automatikusan. Létre kell hoznia őket. 

## <a name="copy-a-project"></a>Projekt másolása
Amikor másol egy projektet a Project Service Automation 3. verziójában, a következő történik: 

- A becsült kezdési dátum másolódik, de megváltoztatható.  
- A projekt ütemterve és a feladatok lemásolódnak. 
- Az általános erőforrások és hozzárendeléseik lemásolódnak. Az általános erőforrások erőforrásigénye nem másolódik. Újra kell generálnia őket. 
- A valódi erőforrások és azok hozzárendelései nem másolódnak. Ehelyett ezeket általános erőforrások váltják fel. 
- A tényleges adatok nem másolódnak az új projektbe. 

## <a name="move-a-scheduled-project"></a>Ütemezett projekt áthelyezése
A meglévő projekt ütemezésének előremozgatásakor a következő történik: 

- A feladat dátumait automatikusan áthelyezik, hogy megfeleljenek a mozgási periódusnak. 
- A hozzárendelt általános erőforrások továbbra is hozzá vannak rendelve.   
- Ha ezeket a projekt áthelyezése előtt generálják, akkor az általános erőforrás követelményei változatlanok lesznek, és nem kerülnek automatikusan előállításra. Újból generálnia kell őket, hogy tükrözzék az új megbízásokat a feladatmozgás miatt. 
- A valós erőforrásokhoz rendelt feladatok változnak, hogy megfeleljenek a feladat dátummozgásának. A valós erőforrásokra vonatkozó foglalások nem változnak. A foglalásokat az egyeztetési nézet segítségével módosítania kell. 
- A foglalásokkal, de megbízásokkal nem rendelkező csapaterőforrások nem változnak. 
- A tényleges adatok nem mozognak. 

## <a name="estimates"></a>Becslések
A becsléseket két lapra osztottuk: **Erőforrás-hozzárendelés** és **Becslések**. Az **Erőforrás-hozzárendelés** lap tartalmazza az erőfeszítések becsléseit, és időben elosztott nézetben mutatja a feladatok erőforrás-hozzárendeléseit. A becsléseket az ütemezési motor által generált adatok alapján szerkesztheti.

![Az erőforrás-hozzárendelés lap, amely megmutatja az erőfeszítések becslését és a feladatok erőforrás-hozzárendeléseit](media/resource-assignments-tab-02.png)

A **Becslések** lapon megjelennek az erőforrás-hozzárendelések költségei és eladási összegei. Az összegek csak olvashatók. A költségek és az értékesítés árazását a csapatoknak az ütemezésben megadott megbízásai határozzák meg. Ez azt jelenti, hogy ha hozzárendelés nélkül van egy feladat, akkor a feladat a hozzá nem rendelt tároló alatt jelenik meg. Ez azt is jelenti, hogy a **szerepkör** nélkül, amely alapértelmezett árképzési dimenzió, nem lesznek becsült költségek vagy eladások, ha ügyféllel vagy projekthez rendelt szerződéssel/ajánlattal rendelkezik. 

![Becslések fül, amely megmutatja a költségeket és az eladási összegeket](media/estimates-tab-03.png)
  
A kategória az ütemezés nézetben is támogatott feladatoknál. A kategóriák szerinti csoportosítás a becslések időszakos nézetében jobb élményt nyújt, különösen akkor, ha a projektben költségelszámolással is rendelkezik. A költségbecsléseket egy külön fülön lévő rács segítségével adják meg. 

A költségbecsléseket a rácsba lehet beírni a **Költségbecslések** lapon. 

![Költségbecslések lap, amelyen megjelenik a költségbecslési rács](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Erőforrás kezelése
A Project Service Automation 3. verziójában, az új Unified Client felhasználói felülettel, valamint a foglalások és a megbízások kapcsolatának változásával a projekt személyzettel való ellátása általános vagy valós erőforrásokkal drasztikusan megváltozott a 2. és az 1. verzióhoz képest. Azonban a foglalható források fogalmak **valós** és **generikus** esetben is ugyanaz marad, mint ahogy a csapat tagjai, követelmények, feladatok, és a foglalások is.   

![Az erőforrás-választó használata](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Valódi foglalható erőforrás hozzárendelése 
A Project Service Automation 3. verziójában a foglalások és a feladat-hozzárendelések nincsenek olyan szorosan összefonódva, mint a Project Service Automation korábbi verzióiban. A csapatrács segítségével **valódi** csapattagot foglalhat le, hasonlóan a piacon lévőkhöz.

Az erőforrás-válogató segítségével az ütemezés segítségével kiválaszthatja a csapatnézetben létrehozott csapattagot, majd hozzárendelheti a feladatokhoz. Folytathatja a feladatok hozzárendelését, még a foglalásaik után is. Az **Egyeztetés** lapon összeegyeztetheti azokat a csapattagokat, akiknek eltérésük van a foglalásokban és a feladatokban.

Az erőforrás-választó megmutatja a projekt tagjait. Az erőforrás-választó segítségével egyéb foglalható erőforrásokat is kereshet és megnézhet, amelyek nem tartoznak a projekt csapatába. Megrendelheti őket egy feladathoz, és a projekt csapatának részévé válnak. Az **Ütemezési tábla** vagy az **Egyeztetés** lapon kell lefoglalnia őket.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Rendeljen egy általános foglalható erőforrást egy feladathoz és a projektcsoporthoz, majd valós erőforrással teljesítse az Ütemezési táblán keresztül 
A Project Service Automation 3. verziójában a csoportgenerálás funkciót nem használják általános erőforrásokhoz. Ehelyett létrehozhat és közvetlenül hozzárendelhet egy általános erőforrást az ütemezéshez azáltal, hogy beírja az általános erőforrás pozíciónevét az ütemezés erőforráscellájába. Vagy kiválaszthatja az erőforrásikont a cellában, majd az erőforrás-kiválasztóval írja be a létrehozni kívánt általános erőforrás nevét. Ez megnyit egy gyors létrehozási panelt, amely lehetővé teszi az általános erőforrás-csoporttag szerepének és szervezeti egységének beállítását. Az erőforrás létrehozása után hozzá van rendelve a feladathoz, és folytathatja az általános erőforrás hozzárendelését az ütemezés többi feladatához.    
 
Ha az erőforrást hozzárendelte az összes megfelelő feladathoz, létrehozhat egy erőforrásigényt, majd teljesítheti azt közvetlenül az **Ütemezési táblán** foglalással vagy egy erőforrásigény benyújtásával. Általános erőforrásokat közvetlenül a csapattagok rácsához is hozzáadhat. 

Az általános erőforrásokat az erőforrásigény nélkül és a projekt kezdő/befejező dátumával egészítik ki a projektcsoportban, amíg az erőforrásigényt nem generálják. Követelmény előállításához válassza ki az általános erőforrást, majd kattintson a **Létrehozás** gombra. Megjelenik a követelmény hivatkozás, és a szükséges órák kitöltésre kerülnek a kijelölt órákkal. Kattintson a hivatkozásra a követelmény megnyitásához és frissítéséhez.
  
Amikor a foglalás teljes, és egy megnevezett erőforrás teljes mértékben teljesíti, az általános erőforrás helyébe a megnevezett erőforrás kerül, és az ütemezésben szereplő hozzárendelés frissül a megnevezett erőforrással. 

A követelményekhez javasolt erőforrások most egy lapon tárolódnak, nem pedig egy külön szakaszban.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Több megnevezett erőforrás, amely teljesíti az általános erőforrást
Ha egy követelmény több erőforrással is teljesül, az általános erőforrás a csapatban marad, és a feladathoz van hozzárendelve. A megnevezett csapattagokat, akiket lefoglaltak, nem osztanak ki pozícióba. A projektmenedzser a szükséges munkákat hozzárendelheti a valódi erőforrásokhoz.  Az **Egyeztetés** nézet a foglalások több erőforrásonkénti bontását adja meg több feladat-hozzárendeléshez. Ez nem történik meg automatikusan, mert bonyolultabb forgatókönyvekben, például olyan esetekben, amikor a követelmény több feladatcsomagból áll, a projektvezető kiosztásának szándékát kell feltételezni. Mivel a rendszer nem érti a szándékot, a feltételezések valószínűleg eltérnek a tervezettől, és helytelen vagy kiszámíthatatlan eredmény fordul elő. A kiszámítható eredmény az, hogy az általános erőforrást addig kell kiosztani, amíg a projektmenedzser szándékosan hozzárendel erőforrásokat az **Egyeztetés** nézet segítségével.

### <a name="reconciliation"></a>Egyeztetés
Az **Egyeztetés** lapon a projektcsoport tagjainak foglalása és az összes feladat látható. A nézet órákat mutat a cellákban, amelyek hónapoktól napokig terjedő időpontokat jelentenek. Ez a nézet lehetővé teszi a projektmenedzserek számára, hogy összehangolják a csapattagok foglalásait és feladataikat a projektcsapatuk számára. Ez azért hasznos, mert a foglalások és a feladatkiosztások nincsenek szorosan összekapcsolva, ami nagyobb rugalmasságot biztosít a projekt megtervezésekor. 

![Egyeztetés fül, amely a projektcsoport tagjainak foglalásait és megbízásait mutatja](media/resource-reconciliation-tab-06.png)

Az egyes erőforrások esetében a nézet veszi a különbséget a csapattagok foglalása és a feladatok összeállítása között, és bemutatja a következő két különbséget, amelyek egy projektben történő foglalásoknál és feladatoknál előfordulhatnak: 

- **Foglaláshiány** - A foglaláshiány akkor fordul elő, ha egy erőforráshoz több hozzárendelés tartozik, mint foglalás. Mivel ez a kapacitás nem volt fenntartva, a projektmenedzser javíthatja ezt a feltételt azáltal, hogy az erőforrás foglalásait kiterjeszti a hiány fedezésére. 
- **Többletfoglalások** - Többletfoglalások akkor fordulnak elő, ha egy erőforrást lefoglaltak a projektre, de nem rendeltek hozzá feladatokhoz.  Ez elfogadható eset lehet, például ha az erőforrást a feladat kiosztása előtt lefoglalták. Más esetekben azonban előfordulhat, hogy az erőforrás nem rendelhető hozzá, és a projektmenedzsernek fontolóra kell vennie az erőforrás foglalásainak törlését, hogy a kapacitást egy másik projekthez felhasználhassák. 

Ha feladatokkal rendelkezik erőforrásokra foglalások nélkül (foglaláshiány), akkor kiválaszthatja az összesített foglaláshiányt, majd kattintson a **Foglalás kiterjesztése** elemre. Innentől megnézheti azt a foglalást, amelyre szükség van az erőforrás hiányának és elérhetőségének kezeléséhez. 
 
## <a name="time-and-expense"></a>Idő és költség
Ez a szakasz információkat tartalmaz az idő, a költségek és a jóváhagyások változásairól a Project Service Automation 3. verziójában. A Dynamics 365 Project Service Automation megoldás részeként az **Időbevitel** szolgáltatást frissítették, hogy kihasználják az Egyesített felület keretrendszerét. Ez lehetővé teszi egy következetes, egységes felhasználói felület biztosítását, amely a reszponzív kialakítást követi az optimális megtekintéshez bármilyen képernyőméretben vagy eszközön. 

### <a name="landing-page"></a>Kezdőlap
A nem kibővíthető egyedi időbeviteli környezetet kivezettük a 3. verzióban. Ehelyett most egy kibővíthető és hozzáférhető natív rácsélmény érhető el. Az időbeviteli funkcióhoz a bal oldali webhelytérkép segítségével férhet hozzá. Ezzel a változással többé nem lehet megadni időt hetenként. Ehelyett minden egyes naphoz időbejegyzést kell létrehoznia a rácsban. Néhány időbejegyzés létrehozása után a felhasználók tömegesen hozhatnak létre időbejegyzéseket a **Másolás** funkcióval, amelyet később a témakörben ismertetünk. 

![Időbeviteli céloldal](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Új időbejegyzések létrehozása 
Kattintson az **Új** elemre a szalagban, és nyisson meg egy gyors létrehozási oldalt az időbevitelhez, ahol megadhatja az időtartam percet, órát vagy napot. Ehhez csak kezdje el gépelni a h, m vagy d betűt a mennyiséggel.  

![Időbevitel gyors létrehozása](media/quick-create-time-entry-08.png)

A keresési mezőket rendszernézetek támogatják. Például, miután megadta a projekt adatait, a **Projektfeladat** mező alapértelmezés szerint **Saját nyitott projektfeladatok** nézetre van állítva. Időbejegyzések létrehozásához olyan feladatokhoz, amelyeket nem rendeltek hozzá a felhasználóhoz, kattintson a **Nézet megváltoztatása** elemre a keresésben, majd válassza a **Minden aktív projektfeladat** lehetőséget. Miután létrehozta az időbejegyzést és az megjelenik a rácsban, bármilyen sorértéket szerkeszthet közvetlenül a rácsban.  

### <a name="bulk-createcopy"></a>Tömeges létrehozás/másolás 
Néhány időbejegyzés létrehozása után a másolási funkcióval további időbejegyzéseket hozhat létre tömegesen. Kattintson a **Másolás** pontra a **Másolás** párbeszédpanel megnyitásához. A **Periódus ettől: Kezdő dátum** részben állítsa be azt a dátumtartományt, ahonnan az időszakokat másolni kell. A **Periódus eddig: Kezdő dátum** mezőben adja meg azt az időpontot, amelyre az időbejegyzéseket létre kell hozni. Kattintson a **Másolás** gombra az időbejegyzések másolásához a hét megfelelő napjára, amelyet a **Periódus eddig** jelöl. Például a múlt hét hétfői időbejegyzését a **Periódus eddig** mezőben megjelölt hét hétfőjére másolja. 

![Időbejegyzések tömeges másolása](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Adatok importálása 
A hozzárendelések és a csere ugyanazt a felhasználói felület mintát követik, amely lehetővé teszi a felhasználó számára, hogy meghatározza a dátumtartományt, ahova a foglalásokat importálni kell. Ezután kifejezetten ki kell választania azokat a foglalásokat, amelyeket másolni kell a **Vázlat** időbejegyzésekbe. A 3. verzióban már nem látja a **Javasolt** időbejegyzések mintáját a rácson és a naptárban.  

### <a name="change-in-calendar-control"></a>A naptárvezérlés változása
A 3. verzióban elmozdultunk az egyedi naptárvezérléstől, és most az UC naptárt használjuk a hét időbejegyzéseinek megjelenítésére. Ezzel a naptárral megtekintheti a napot, a hetet és a hónapot. 

> [!NOTE]
> A naptár korlátozása az, hogy ez a vezérlő nem támogatja az egyes naptárelemekkel kapcsolatos műveleteket. Például nem választhat ki egy vagy több naptárelemet, és nem küldheti el vagy törölheti azokat. A naptárelemre kattintva megnyitja az **Időbeviteli entitás** oldalt további műveletekhez. 

### <a name="extensibility"></a>Bővíthetőség
**Az egyedi mezők adatainak rögzítése csak idő- és költségbeviteli entitásokban** - Az időbevitel szerkeszthető rácsot, csak olvasható rácsot és naptárvezérlőket használ a platformon. Az összes vezérlő natív, ezért támogatni fogja a testreszabásokat. A Project Service Automation 3-as verziójában további egyedi mezőket adhat hozzá, beállíthatja a keresési mezőket, és az egyedi nézetekkel mentheti őket. Az egyedi üzleti logikát a kiválasztott értékek alapján az egyedi mezőkben is beállíthatja.  

**Az egyedi mezők adatainak rögzítése az idő- és költségbevitel során, és azokon a szervezeteken keresztüli propagálása, amelyek támogatják a benyújtási és jóváhagyási folyamatot** - Az időbevitelek tipikus feldolgozását az alábbi ábra mutatja.

![Időbejegyzési folyamat feldolgozása](media/process-time-entries-10.png)

Ha az üzleti követelmények előírják, hogy az idő- és költségentitásoknak rögzíteniük kell az egyedi árazási dimenziókat, és az egyéni árazási dimenzióban az idő- és bevételi erőforrás által meghatározott értékeket el kell terjeszteni az előző grafikán szereplő összes elem között, tekintse meg [Az egyedi mezők beállítása árazási dimenziókként](set-up-pricing-dimensions.md) című részt.

Az üzleti követelmények támogatása érdekében, amikor az idő- és költségentitásoknak rögzíteniük kell az egyedi, nem árképzési dimenziókat és el kell terjeszteni az értékeket, használhatja az árképzési dimenziók beállítását, és kifejezheti az egyéni dimenziókat árazási dimenzióként, költség és számlázási árak nélkül. Egy másik forgatókönyv az, ha egyéni mezőt ad az egyes entitásokhoz, ugyanazt a mezőnevet használva minden entitáshoz. Az egyedi beépülő modulok létrehozhatók a beküldési/jóváhagyási folyamatban részt vevő entitások rekordjai összekapcsolásához a tranzakció származási és kapcsolati entitásaival.  

### <a name="delegate-time-and-expense-entry"></a>Idő- és költségbejegyzés delegálása
A Common Data Service platform nem támogatja, hogy az egyik felhasználó megszemélyesítsen egy másik felhasználót, ami azt jelenti, hogy a Project Service Automation 3. verziójában nem támogatott a delegált idő- és költségbejegyzés. A partnerek és az ügyfelek azonban kihasználtak egy megoldást, hogy lehetővé tegyék a delegált időbeviteli környezetek támogatását a 3. verzióban. Ez csak ideiglenes megoldás, és nem teljes megoldás, ezért fontos megérteni a korlátozásokat, és ezt a megközelítést csak akkor lehet alkalmazni, ha a korlátozások elfogadhatók. 

> [!IMPORTANT]
> Ezt az információt csak a partner/ügyfél általi egyedi megvalósításra javasolt útmutatásnak kell tekinteni. A termékcsapat egyetlen támogatási csatornánkon keresztül sem fog hivatalos támogatást nyújtani ehhez a funkcióhoz.

### <a name="customization-details"></a>Testreszabási részletek 
A testreszabás lehetővé teszi a **Foglalható erőforrás** hozzáadását a létrehozási és szerkesztési élményekhez, amelyek lehetővé teszik a felhasználó számára, hogy delegáltként cselekedjen, ha a **Foglalási erőforrás** mezőt egy másik felhasználóra változtatja, akinek idő- és költségbejegyzéseket kell rögzíteni. A következő lépések az időbejegyzés átruházására vonatkoznak. Ugyanez az információ vonatkozik a költségbejegyzések átruházására. 
 
1.  Győződjön meg arról, hogy a delegált felhasználó globális biztonsági hozzáféréssel rendelkezik a projektekhez és a projektfeladatokhoz. 
1.  Mivel a **Foglalható erőforrás**, amely egy mező az **Időbejegyzés** entitáson, nincs megjelenítve a **Gyors létrehozás** oldalon, hozzá kell adnia.

    -vagy-

    Hozzon létre egy egyéni nézetet, amely magába foglalja a **Lefoglalható erőforrás** oszlopot, annak érdekében, hogy csak az erőforráshoz létrehozott időbejegyzések jelenjenek meg. Tegye közzé a testreszabásokat az alkalmazásmodul tervezőjén, hogy ez a nézet megjelenjen az **Időbejegyzések** oldal **Nézetválasztó** alatt. Két beépülő modul foglalkozik a kezelő beállításával a projekten kívüli időbejegyzésekhez:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Hozzon létre egy új beépülő modult, hogy felülírja a **Kezelő** mezőt a felhasználó **Foglalható erőforrás** mezőben kijelölt kezelőjének. Használja ugyanazt a **Végrehajtási szakaszt**, mint a sávon kívüli (OOB) beépülő modul (előzetes érvényesítés), és használjon olyan **Végrehajtási sorrendet**, amely magasabb, mint az OOB beépülő modulok (nagyobb, mint 1). Ez biztosítja, hogy az egyedi beépülő modul az OOB beépülő modulok után kerül végrehajtásra.  
 
### <a name="end-user-experience"></a>Végfelhasználói élmény
1.  Amikor létrehoz egy időbejegyzést a gyors létrehozási oldalon, írja be a Projektet és a Projekt feladat részleteit, majd válassza a **Foglalható erőforrás** mezőben azt a felhasználót, aki számára az időbejegyzéseket rögzíteni kell. 
2.  Alapértelmezés szerint ez a mező a bejelentkezett felhasználó, azonban mivel a felhasználó felülbírálja ezt a mezőt, az időbejegyzés létrejön a kiválasztott **Foglalható erőforrás** számára.
3.  Amikor benyújtja az ezekhez a rekordokhoz létrehozott időbejegyzéseket, a bejegyzéseket a rendszer sorba állítja a jóváhagyó számára a projektben. 
4.  Amikor visszahívja a másik felhasználó számára létrehozott időbejegyzéseket, az időbejegyzések visszatérnek **Vázlat** állapotba, a **Foglalható erőforrás** mező pedig a másik felhasználóhoz lesz beállítva. 
5.  Opcionálisan átválthat az egyedi nézetre, hogy kiszűrje a másik felhasználó számára létrehozott időbejegyzéseket. 
 
### <a name="limitations"></a>Korlátozások
A **Másolás** és **Importálás** funkció csak a bejelentkezett felhasználó számára működik. Ez azt jelenti, hogy nem lehet másolni vagy importálni az időbejegyzéseket, amelyeket a megrendelhető erőforrásként bejelentkezett felhasználó számára hoztak létre.

A nem projekt számára készült időbejegyzések át lesznek irányítva jóváhagyásra a foglalható erőforrás kezelőjéhez csak akkor, ha a fenti 4. lépést a **Testreszabási részletek** részben befejezték. Ellenkező esetben a másik felhasználó nem projektre vonatkozó időbejegyzései helytelenül kerülnek a bejelentkezett felhasználó kezelőjéhez. 

### <a name="other-changes"></a>Egyéb változások 
A **Foglalások és feladatok** funkció el lett távolítva. 

## <a name="multidimensional-pricing"></a>Többdimenziós árképzés
A rugalmasság maximalizálása és a különböző üzleti követelmények kielégítése érdekében a Project Service Automation 3. verziója támogatja az árképzési dimenziókészletek különálló alkalmazását a költségekre és a számlákra. A dimenzióértékeket alapértelmezésként lehet beállítani, majd tovább lehet terjeszteni a költség- és árazási folyamatban, az erőforrás profilozásától az időbevitelig és a projekt aktuális adataiig. Az ügyfél-specifikus konfiguráció és módosítás vagy kiterjesztés kihasználja a szokásos testreszabhatósági infrastruktúrát.

A Project Service Automation alapértelmezett árazási dimenziókkal, szerepekkel és erőforrásegységekkel kapható, és lehetővé teszi az árak és költségek beállítását az egyes szerep- és szervezeti egységek kombinációi számára.

Azoknak a Project Service Automation-ügyfeleknek, akik továbbra is használni szeretnék ezeket a kész mezőket árképzési dimenzióként a 3. verzióban, nem lesz megfigyelhető változás. Továbbra is használhatja a Project Service Automation szolgáltatást a megszokott módon. Ha azonban más kiegészítő attribútumokkal kell az erőforrásokat áraznia vagy költségelnie, a 3. verzió lehetővé teszi a saját egyedi árképzési dimenzióinak hozzáadását a Project Service Automation megoldáshoz. Az egyedi árazási dimenziók kiterjesztése bonyolult konfigurációs környezet. 

## <a name="quotes-and-contracts"></a>Árajánlatok és szerződések
A Project Service Automation 3. verziójában megváltoztak az árajánlatok és a szerződések beállításának és kezelésének szempontjai. A következő szakaszok részletesebb információkat tartalmaznak.

### <a name="set-up-chargeability-options"></a>A díjazhatósági lehetőségek beállítása
Az 1. és a 2. verzióban a szerepek és kategóriák díjazási beállítása az egyes árajánlatok és szerződések esetében a **Díjazhatóság** nézet segítségével történt, amely egy árajánlati sor vagy egy szerződési sor felső navigációjában volt. Itt határozhatott meg árakat ezekre a szerepekre és a Költség kategóriákra.

A 3. verziótól kezdve a díjazhatósági lehetőségek szerep- és költségkategóriák szerinti beállítása az ajánlati vagy a szerződési sor szintjén történik. Az árképzés beállítása elkülönül a Díjazhatósági beállítástól. A **Díjazható szerepkörök** és **Díjazható kategóriák** füleket a **Árajánlati sor** és **Szerződéses sor** oldalakon találja a felső navigáció használata nélkül.

![Díjazható szerepkörök](media/chargeable-12.png)
 
A Díjköteles szerepkörök és a Díjköteles kategóriák beállításánál a készen szerkeszthető rácsvezérlés is kihasználható. Az egyes szerepek és kategóriák esetében az árajánlat és a szerződéskötés szakaszában a számlázási típus támogatott opciói változatlanok maradnak a korábbi verziókhoz képest: **Díjazható** és **Nem díjazható**. Az **Ingyenes** nem támogatott típus az Árajánlat vagy a Szerződéskötés fázisa alatt. Az **Ingyenes** csak az Idő vagy Költség jóváhagyása során támogatott.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Hozzon létre és szerkesszen egyedi árakat Project Service Automation ajánlat és projektszerződés számára
Az 1. és a 2. verzióban az egyedi árlista használatát az egyes árajánlatokhoz és szerződésekhez a **Díjazhatóság** nézet **Árak szerkesztése** segítségével végezték. A **Díjazhatóság** nézet az ajánlat vagy a szerződés sor felső navigációjában található. Itt is beállíthatott díjazhatósági lehetőségeket a szerepkörökhöz és/vagy a költségkategóriákhoz.

A 3. verziótól kezdve a Project Service Automation árajánlaton és a Project Service Automation projektszerződésen az egyéni projektárlista létrehozását és használatát elkülönítették a díjazhatósági beállításoktól. A Project Service Automation ajánlata és a Project Service Automation projektszerződések egy új, **Projekt árlisták** nevű lapot kaptak. Ez a lap az összes Project Service Automation-ajánlathoz vagy projektszerződéshez csatolt nézetét mutatja. Egyéni árlista létrehozásához egy meglévő árlistából, amely már társítva van a projekt ajánlatához vagy szerződéséhez, kattintson az **Egyéni árképzés létrehozása** elemre. Ez elkészíti a kapcsolódó árlisták másolatát, és csatolja azokat az ajánlathoz vagy a szerződéshez. Most megnyithatja az árlistát, és szerkesztheti a szerepkör- vagy költségkategóriát, hogy ezek az árváltozások csak erre az árajánlatra vagy szerződésre vonatkozzanak. 
  
A következő ábra még az egyedi árlisták létrehozása előtti állapotot mutatja.

![Egyéni árlisták előtt](media/before-custom-price-lists-13.png)

A következő ábra az egyedi árlisták létrehozása utáni állapotot mutatja.

![Egyéni árlisták után](media/after-custom-price-lists-14.png)

> [!NOTE]
> Egy rövid késleltetés történhet, ha rákattint az **Egyéni árképzés létrehozása** elemre, addig, hogy az egyéni árlista létrejön. Javasoljuk, hogy frissítse a rácsot a többszöri kattintás helyett. Létrehozott egy egyéni árlistát, ha a társított árlista nevéhez hozzá van fűzve az árajánlat neve vagy a projektszerződés neve.


[!INCLUDE[footer-include](../includes/footer-banner.md)]