---
title: Projekterőforrások biztosítása
description: Ez a témakör információkat nyújt a projekterőforrások biztosításáról.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752162"
---
# <a name="project-resourcing"></a>Projekterőforrások biztosítása

[!include [banner](../includes/banner.md)]

Ez a témakör információkat nyújt a projekterőforrások biztosításáról.

Az egyik kihívás a projektmenedzserek és az erőforrás-menedzserek számára a projekt tervezési fázisában az erőforrás-elosztás, ahol meg kell határozniuk és le kell foglalniuk a megfelelő erőforrást a projekten végzett munkához. A Dynamics 365 Finance alkalmazásban a projektek erőforrás-biztosítási képességei lehetővé teszik ideiglenes erőforrásokként kezelt szerepek megadását, amelyek lefoglalhatók egy adott aktivitáshoz vagy egy aktivitás részéhez. Az ilyen típusú erőforrás-biztosítás segítségével a projektmenedzserek és az erőforrás-menedzserek a következő feladatokat hajthatják végre:

- Olyan szerepkört adhatnak meg, amely rendelkezik a szükséges kompetenciákkal, hogy könnyen megfeleltethető legyen az erőforrásokkal.
- Szerepkörök használatával megadhatják a fenntartott erőforrásokon alapuló kezdeti aktivitási ütemezést.
- Megbecsülhetik a költségeket, és egy kezdeti költségvetést határozhatnak meg a projektek hozzárendelt szerepkörei és erőforrásai alapján.
- A szerepkörök használatával megbecsülhetik az egyes aktivitásokhoz szükséges erőforrás-foglalások számát.
- Megbecsülhetik az erőforrások számát, amelyek a projekt teljes életciklusához szükségesek.
- Kidolgozhatnak egy munkalebontási struktúrát (WBS) a kezdeti erőforrás-hozzárendelések segítségével.

[![Projekt életciklusa](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

A projektek tervezése során a tervezett erőforrások lecserélhetők a munkatársakkal ellátott erőforrásokat. A projektmenedzser ugyancsak visszatérhet, és frissítheti az erőforrás-biztosítási foglalásokat a projekt bármely fázisában.

## <a name="set-up-project-resources"></a>Projekt-erőforrások beállítása
Be kell állítania egy naptárat, és társítania kell azt egy alkalmazotthoz vagy egy dolgozóhoz. A naptár a projekt és a projekt számára fenntartott erőforrások munkaidejének ütemezésére szolgál. A naptár beállítása során a projektmenedzserek az erőforrás-optimalizálás részeként az erőforrásszintek beállítását is elvégezhetik. A naptár ütemezése alapján a korlátozások alkalmazhatók az erőforrásokon. Beállíthat egy naptárat a **Naptárak** oldalon.

Amikor egy dolgozót projekterőforrásként állít be, kiválaszthatja azokat a dolgozókat, akik annál a vállalatnál dolgoznak, amelyhez az erőforrásokat beállítja. Másik lehetőségként kiválaszthat dolgozókat a szervezete más vállalataitól is. Ezek a dolgozók vállalatközi erőforrásként is ismertek.

A következő eljárások azt ismertetik, hogyan állítható be a dolgozó projekterőforrásként a vállalatánál, és hogyan állítható be egy vállalatközi projekterőforrás.

### <a name="set-up-a-worker-as-a-project-resource"></a>Alkalmazott beállítása projekterőforrásként

1. A **Dolgozók** oldalon található **Dolgozók** listában jelölje ki a projekterőforrásként hozzáadni kívánt munkatársat, és nyissa meg a munkabejegyzést.
2. A Művelet panelen válassza a **Projekt** &gt; **Beállítás** &gt; **Projektbeállítás** lehetőséget.
3. Jelöljön ki egy naptárt, majd zárja be az oldalt.

Az erőforrás alapértelmezett projektjeit az előzetes hozzárendelés típusaként is megadhatja. Az előzetes hozzárendelések akkor is használhatók, ha az erőforrás-menedzser vagy a projektmenedzser előre tudja, hogy mely projekteken fog az erőforrás dolgozni. Az előzetes hozzárendelések a projektszponzor vagy ügyfél kérésén is alapulhatnak. Projekt előzetes hozzárendeléséhez a **Projektek hozzárendelése** oldalon a **Projektek** lap **Hátralévő projektek** listájában válassza ki a megfelelő projektet.

### <a name="set-up-an-intercompany-resource"></a>Vállalatközi erőforrás beállítása

Ha a munkatársat vállalatközi erőforrásként állítja be, akkor a kölcsönadó vállalatnál és a kölcsönvevő vállalatnál is el kell végeznie a beállítást.

**A kölcsönadó vállalatnál**

1. A Pénzügy területen ellenőrizze, hogy a kölcsönző vállalat ki van-e jelölve, majd végezze el az előző, „Alkalmazott beállítása projekterőforrásként” című részben leírt eljárást.
2. A **Vállalatközi könyvelés** oldalon válassza az **Új** lehetőséget.
3. A **Jogi entitás azonosítója** mezőben válassza ki a kölcsönadó vállalatot. Töltse ki megfelelően a hátralévő mezőket, majd válassza a **Mentés** lehetőséget.
4. Az **Transzferár** oldalon válassza az **Új** lehetőséget.
5. A **Kölcsönbe vevő jogi személy** mezőben válassza ki a megfelelő vállalatot.
6. Ha csak az ennek a szakasznak a kezdetén létrehozott erőforrást kívánja kölcsönadni a kölcsönvevő vállalatnak, az **Erőforrás** mezőben jelölje ki a létrehozott erőforrás nevét. Ha a kölcsönadó vállalat összes erőforrását elérhetővé szeretné hozni a kölcsönvevő vállalat számára, akkor hagyja üresen az **Erőforrás** mezőt.
7. A **Projektmenedzsment és könyvelési paraméterek** oldal **Vállalatközi** lapján állítsa a **Vállalatközi erőforrás-ütemezés és az időnyilvántartások engedélyezése** beállítást **Igen** értékre.

**A kölcsönvevő vállalatnál**

- Az **Erőforrások listája** oldalon a keresési szűrőben írja be a kölcsönadó vállalathoz létrehozott erőforrás nevét annak ellenőrzéséhez, hogy a név szerepel-e a kölcsönvevő vállalathoz tartozó erőforráslistában.

## <a name="manage-resource-competencies"></a>Erőforrás-kompetenciák kezelése
Az erőforrás-kompetenciák az erőforrás-kezelés fontos részét képezik. A kompetenciák a készségek, az oktatás, a tanúsítványok és a projekttapasztalatok megfelelő egyensúlyával rendelkező erőforrások meghatározásához használhatók fel alapként. Minden egyes erőforráshoz be kell állítania ezeket az adatokat, és rendszeresen frissítenie kell őket. Ily módon maximalizálhatja a lehetőségeket, amikor bizonyos erőforrás-kompetenciákat a projekt erőforrás-hozzárendelése során megfeleltet a rendszer.

[![Példák a készségekre, a tanúsítványokra, az oktatásra és a projekttapasztalatokra](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

A következő eljárások ismertetik, hogyan kell beállítani az erőforrások bizonyos kompetenciáit.

A dolgozó kompetenciáinak beállításához használhatja a **Dolgozók** listáját az Emberi erőforrások területén, vagy az **Erőforrások** listaoldalon a Projektmenedzsment és könyvelés alatt. A következő eljárások esetében az Emberi erőforrások **Dolgozók** listaoldala kerül felhasználásra.

### <a name="set-up-competencies-certificates"></a>Kompetenciák beállítása: Tanúsítványok

1. A **Dolgozók** listaoldalon válassza ki a dolgozónak azt a sorát, amelyhez hozzá szeretné adni a tanúsítványinformációkat.
2. A Műveleti ablaktáblán a **Dolgozó** lapon, a **Kompetenciák** csoportban válassza a **Tanúsítványok** lehetőséget.
3. Válassza az **Új** lehetőséget, majd a **Tanúsítványtípus** mezőben válassza a **PMP** lehetőséget.
4. A **Kezdő dátum** mezőben válassza a **2015.01.10.** elemet, majd válassza a **Mentés** lehetőséget.

### <a name="set-up-competencies-skills"></a>Kompetenciák beállítása: Készségek

1. A **Dolgozók** listaoldalon győződjön meg arról, hogy az előző eljárásban használt dolgozó még mindig ki van választva. Ezután a Művelet panelen a **Dolgozó** lap **Kompetenciák** csoportjában válassza a **Készségek** lehetőséget.
2. Válassza az **Új** lehetőséget.
3. A **Készség** mezőben válassza a **Projektmenedzsment** lehetőséget.
4. A **Szint** mezőben válassza az **5 szakértő** lehetőséget.
5. A **Szint dátuma** mezőben válassza a **2014.01.14.** lehetőséget.
6. A **Tapasztalati évek** mezőben adja meg a **10** értéket.
7. Válassza a **Mentés** lehetőséget, és zárja be az oldalt.

## <a name="create-a-new-project"></a>Új projekt létrehozása
1. A **Projektmenedzsment** oldalon válassza az **Új projekt** lehetőséget, és adja meg a következő értékeket:

    - **Projekttípus:** Idő és anyag
    - **Projekt neve:** XYZ frissítés 2. fázis
    - **Projektcsoport:** TM\_WIP
    - **Projektszerződés azonosítója:** 00000002

2. Válassza a **Projekt létrehozása** lehetőséget.

### <a name="assign-a-resource-to-a-project"></a>Erőforrás hozzárendelése egy projekthez

1. A **Dolgozók** oldalon található **Dolgozók** listában jelölje ki annak a dolgozónak a rekordját, akihez korábban kompetenciákat hozott létre, és nyissa meg a dolgozó rekordját.
2. A Művelet panelen a **Projekt** lap **Beállítás** csoportjában válassza a **Projektek hozzárendelése** lehetőséget.
3. Az **Erőforrás-ellenőrzés projekt-hozzárendelései** oldal **Projektek** lapjának **Projekt hozzáadása a kijelölt projektekhez** mezőjében szűrjön az **XYZ frissítés 2. fázis** projektre.
4. A **Fennmaradó projektek** panelen válasszon ki egy projektet, majd válassza a nyíl gombot, majd adja hozzá a **Kijelölt projektek** panelhez.

Szükség szerint az erőforrásokhoz is hozzárendelhet kategóriákat. A kategória típusa vagy **Költség** vagy **Bevétel**. A kategória típusát a szervezete határozza meg. Ha egy erőforráshoz egyetlen kategória sincs hozzárendelve, akkor a Pénzügy az alapértelmezett kategóriát keresi ki a költség és a bevétel óránkénti ára esetében.

### <a name="set-up-project-resource-and-role-characteristics"></a>A projekt erőforrás- és szerepkörjellemzőinek beállítása

A projektmenedzser a projekterőforrások biztosításának funkciójával létrehozhatja a projekthez szükséges erőforrásokat. A szerepkörök használhatók, ha a megerősített erőforrások még nem ismertek az erőforrások lefoglalása esetén. A szerepkörök ideiglenesen lefoglalhatók fenntartott erőforrásként, így folytathatja a projektek tervezési fázisait.

[![Példa szerepkörre](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Forgatókönyv:** A Contoso egy olyan Idő és anyag projekt elvégzésével bízták meg, amelyhez jóváhagyott projekt-charta tartozik. A junior projektmenedzser még dolgozik a projekt hatókörének befejezésén. Az erőforrás-kezelő jelenleg azonosítja azokat az erőforrásokat, amelyek az új projekt munkájához lefoglalásra kerülnek. A projekt kritikus jellegéből adódóan a projekt szponzora az egyik szerepkörként a Senior projektmenedzsert kérelmezte. Az erőforrás-menedzsernek meg kell szereznie az új erőforrást, és meg kell adnia a szerepkört a rendszerben abban az esetben, ha a junior projektmenedzsernek erőforrásadatokra van szüksége a projekttervezés során.

A következő lépések azt mutatják, hogy az erőforrás-menedzser hogyan állíthatja be a Senior projektmenedzseri szerepkört, és társíthatja hozzá az erőforrás-jellemzőket. Később a szerepkör használható a szükséges erőforrás-kompetenciáknak megfelelő, rendelkezésre álló erőforrások keresésére.

1. A **Szerepek beállítása** oldalon válassza az **Új** lehetőséget, és adja meg a következő értékeket:

    - **Szerepkör-azonosító:** Senior projektmenedzser
    - **Leírás:** Senior projektmenedzser

2. Válassza a **Létrehozás** parancsot.
3. Válassza ki a **Senior projektmenedzser** szerepkört, majd válassza a **Tulajdonságok konfigurálása** lehetőséget.
4. A **Jellemzők típusa** mezőben válassza a **Készség** lehetőséget.
5. A **Rendelkezésre álló jellemzők** mezőben adja meg a keresendő készséget.
6. A **Jellemzők típusa** mezőben válassza a **Tanúsítvány** lehetőséget.
7. A **Rendelkezésre álló jellemzők** mezőben adja meg a keresendő tanúsítványtípust.

### <a name="assign-a-project-resource-to-a-project"></a>Projekterőforrás hozzárendelése egy projekthez

1. A **Minden projekt** oldalon jelölje ki az **XYZ frissítés 2. fázis** projektet.
2. A **Projektcsapat és ütemezés** lapon válassza a **Hozzáadás** lehetőséget.
3. A **Szerepkör** mezőben jelölje ki a **Csapattag** elemet.
4. Válassza a **Foglalás a naptárból** lehetőséget.
5. Az **Erőforrás elérhetősége** oldalon válassza a **Nézet beállításai** lehetőséget.
6. A **Nézet beállításainak módosítása** oldalon adja meg a következő értékeket:

    - **Dátumtartomány nézetének formátuma:** Nap
    - **Rendelkezésre állási leírások megjelenítése:** Igen
    - **Hátralévő kapacitás megjelenítése:** Igen

7. Válasszon ki egy erőforrást az erőforrások listájából.
8. Válassza **Végleges foglalás** és a **Teljes kapacitás** lehetőséget.


### <a name="assign-a-resource-to-a-default-role"></a>Rendeljen egy erőforrást az alapértelmezett szerephez

Segítségként a projekt- vagy erőforrás-menedzserek tovább fúrhatnak le az erőforrásokon, amelyek egy projekthez vannak lefoglalva. Az alapértelmezett szerepkör társítható meglévő erőforráshoz vagy újonnan megszerzett erőforráshoz. Amikor például Dániel felvették, megfelelő tapasztalattal és készségekkel rendelkezett az üzleti elemző szerepkör betöltésére. Az erőforrás-menedzser ezt a szerepkört rendelte Dánielhez alapértelmezett szerepkörként. Ezért az erőforrás-menedzser hozzáadta Dánielt a projekteken végzett munkához rendelkezésre álló üzleti elemzők készletéhez.

Az erőforrás-foglalás során a projektmenedzserek szűrhetik a projektek számára elérhető szerepkör-erőforrásokat. Ezeket az információkat felhasználhatják feltételként, amikor a többfeltételű döntési döntéselemzést hajtanak végre az erőforrás-teljesítés során. Emellett más erőforrás-jellemzőket is hozzáadhatnak a szűrőhöz, hogy olyan erőforrásokat keressenek, amelyek meghatározott készségekkel, oktatással és tapasztalattal rendelkeznek egy adott projekthez.

**Forgatókönyv:** Egy jóváhagyott projekt elindult, és a Senior projektmenedzser szerepe a projekt tervezési fázisában tervezett erőforrásként lett lefoglalva. Az erőforrás-menedzser most már megszerezte az erőforrást a Senior projektmenedzseri szerepkör betöltéséhez.

1. Az **Erőforrások listája** oldalon válassza a **Kovács Dániel** lehetőséget.
2. Az **Erőforrás szerepköre** oldalon válassza az **Új** lehetőséget, és adja meg a következő értékeket:

    - **Hatályos:** Adja meg az aktuális dátumot.
    - **Lejárat:** Adja meg a **Soha** értéket.
    - **Szerepkör:** Adja meg a **Senior projektmenedzser** értéket.

3. Válassza a **Mentés** lehetőséget, és zárja be az oldalt.
4. A **Kompetenciák** lapon adja hozzá a **ProjectMgmt** készséget és a **PMP** tanúsítványt.

## <a name="set-up-role-based-pricing"></a>Szerepalapú árazás beállítása
A szerepkörökhöz minden költség, értékesítési és transzferár beállítható.

1. Az **Értékesítési ár (óra)** oldalon válassza az **Új** lehetőséget, és adjon meg egy hatályossági dátumot.
2. A **Szerepkör** oszlopban jelöljön ki egy szerepkört.
3. Az **Árképzés** oszlopban adja meg a kijelölt erőforrás-szerepkör árát.

## <a name="form-a-project-team"></a>A projektcsapattól
Ahhoz, hogy a projektben korábban beállított szerepköröket használni lehessen, a projektmenedzsernek hozzá kell rendelnie a szerepköröket a projekthez. A projektekhez több szerepkör is hozzárendelhető. A félreértések elkerülése érdekében ezeket a szerepköröket a rendszer automatikusan címkézi a foglalás során. Ha például a projektvezető három szoftvermérnököt igényel, akkor három szoftvermérnök szerepkör jön létre automatikusan az **1. szoftvermérnök**, **2. szoftvermérnök** és **3. szoftvermérnök** címkével. Ha előzőleg beállította a szerepkörhöz tartozó szerepkörjellemzőket, akkor az erőforrás keresései során szűrőként lesznek alkalmazva. A keresés további finomítása érdekében szükség esetén további jellemzők adhatók hozzá.

A nézet beállításai is testreszabhatók, így könnyebben áttekinthető az erőforrások elérhetősége is. Vannak olyan lehetőségek is, amelyek óránkénti, napi, heti, havi, negyedéves és éves bontásban mutatják a rendelkezésre állást. Lehetőség van az erőforrások rendelkezésre álló és fennmaradó kapacitásának megjelenítésére is. Ez a beállítás időgazdálkodásra is hasznos, ha a tevékenységek vagy az erőforrások elérhetőségének rendelkezésre álló idejét becsüli meg.

A projektmenedzser kiválaszthat egy szerepkört az oldalon, majd ha rendelkezésre áll egy, a követelménynek megfelelő erőforrás, akkor válassza a lehetőséget a szerepkör betöltéséhez szükséges erőforrás lefoglalásához. Ne feledje, hogy az erőforrásokat nem kell ezen a ponton a tervezési fázisban lefoglalni. Ha WBS-t hoz létre, a szerepköröket a projekthez tartozó munkatársakkal ellátott erőforrásokkal helyettesítheti. Ha a szerepeket munkatársakkal ellátott erőforrásokra cseréli le a WBS-ben, az erőforrás-beállítás automatikusan frissíti a projektcsapat felsorolását és ütemezését.

[![Projektcsoport felsorolása, amely a szerepköröket és a tényleges erőforrásokat egyaránt tartalmazza](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

A projektmenedzser többféle lehetőséget kínál a projektek erőforrás-foglalására, például a **Hátralévő kapacitás**, a **Teljes kapacitás**, a **Kapacitás százalékos értéke**, valamint az **Órák megadása**. Ezek a foglalási lehetőségek bármikor visszavonhatók, ha az erőforrás-hozzárendelések megváltoznak. A foglalás két típusa támogatott:

- **Végleges foglalás** – Az erőforrás-foglalás jóváhagyása megtörtént, és megerősítésre került, hogy a megadott időtartamra az aktivitáson dolgozik.
- **Ideiglenes foglalás** – Az erőforrás-foglalások feltételesen beállításra kerültek az aktivitáson a megadott időtartamig végzett munkára.

Az alábbi eljárás bemutatja, hogyan hozhat létre egy projektcsapatot:

### <a name="create-a-project-team"></a>Projektcsapat létrehozása

1. A **Minden projekt** listaoldalon jelöljön ki egy projektet, majd válassza a **Szerkesztés** lehetőséget.
2. A **Projektcsapat és ütemezés** lap **Ütemezés záró dátuma** mezőjében adja meg az ütemezés kezdő dátumát és egy hónapot. Ha például az ütemezés kezdő dátuma 2017. június 24. (24/06/2017), írja be a **24/07/2017** értéket.
3. Válassza a **Hozzáadás** lehetőséget.
4. A **Szerepkörök hozzáadása a projekthez** panel **Szerepkör** mezőjében válassza a **Senior projektmenedzser** lehetőséget.
5. Válassza ki a **Szükséges kompetenciák** lehetőséget.
6. A **Jellemzők kiválasztása** lapon a Senior projektmenedzser szerepkörhöz előzőleg beállított jellemzők alapértelmezés szerint be vannak jelölve. Kattintson az **OK** gombra.
7. A **Szerepkör hozzáadása a projekthez** oldal **Erőforrások száma** mezőjében adja meg az **1** értéket.
8. Az **Erőforrás** mezőben a keresés megjeleníti az összes olyan erőforrást, amely rendelkezik a szükséges kompetenciákkal. Válassza a **Kovács Dániel** lehetőséget, majd kattintson a **Létrehozás** gombra.
9. A **Projekt** oldalon válassza a **Hozzáadás** lehetőséget.
10. A **Szerepkörök hozzáadása a projekthez** panel **Szerepkör** mezőjében válassza a **Csapattag** lehetőséget. Az **Erőforrások száma** mezőben adja meg az **5** értéket.
11. Válassza a **Létrehozás** parancsot.
12. A **Projektek** lapon válassza az **Erőforrás teljesítése** lehetőséget.

## <a name="resource-capacity-synchronization"></a>Erőforrás-kapacitás szinkronizálása
Az erőforrás-szinkronizálási folyamatok segítségével biztosítható, hogy a naptár és az alapnaptár adatai eljutnak a projekterőforrás-ütemezésébe. A naptár módosítása esetén a folyamat végrehajtja a projektek erőforrásainak ütemezéséhez szükséges frissítéseket. A folyamatok a teljesítmény javítását is segítik, mivel a naptár erőforrás-információit előre szinkronizálja a rendszer. Ezért gyorsabban történnek az erőforrás-ütemezési adatok frissítései. Javasoljuk, hogy a folyamatokat ne egyenként, hanem kötegelve ütemezze. Ellenkező esetben fennáll annak a veszélye, hogy valaki elfelejti a bezárólagos dátumokat, amikor az adatok legutóbbi szinkronizálása megtörtént. Ha nem bezárólagos dátumokat használ, akkor a szinkronizálás során hézagok keletkezhetnek.

![Naptár szinkronizálása](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Erőforráskapacitás-összesítések szinkronizálása

A szinkronizálási folyamat az összes erőforrásnaptár-információ szinkronizálására szolgál. Ezek az információk a projekt erőforrásnaptár-kapacitásainak táblázatában bekövetkezett változásokkal kapcsolatos alapvető naptár-információkat tartalmazza. Ha új erőforrásokat vesz fel a projektbe, a szinkronizálás segít biztosítani, hogy a frissített naptárinformációk elérhetők legyenek. A szinkronizálás bármikor végrehajtható.

Javasoljuk, hogy használja használjon köteget. A beállítások a kapacitásfoglalások szinkronizálása során érhetők el.

1. Válassza a **Projektmenedzsment és könyvelés** &gt; **Időszakos** &gt; **Kapacitás szinkronizálása** &gt; **Erőforráskapacitás-összesítések szinkronizálása** lehetőséget.
2. Adja meg a beállításokat a következő táblázatban.

    | Beállítás      | Ismertetés |
    |-------------|-------------|
    | Időszak kódja | Opcionálisan kiválaszthatja a főkönyvi dátum intervallumkódját az erőforráskapacitás-összesítések szinkronizálási folyamatához tartozó kezdő és záró dátumok beállításához. |
    | Kezdő dátum  | Adja meg az erőforráskapacitás-összesítések szinkronizálási folyamatának kezdő dátumát. |
    | Befejező dátum    | Adja meg az erőforráskapacitás-összesítések szinkronizálási folyamatának záró dátumát. |

[![Szinkronizálási folyamat](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Szerepkörök beállítása a WBS-sablonokhoz
A projektmenedzserek WBS-sablonokat állíthatnak be, amelyek akkor alkalmazhatók, amikor új projektekhez hoznak létre WBS-t. A projektmenedzserek szerepköröket vehetnek fel, amikor létrehoznak egy sablont. A következő eljárással lehet szerepkört rendelni egy WBS-sablonhoz.

1. Válassza a **Projektmenedzsment és könyvelés** &gt; **Beállítás** &gt; **Projektek** &gt; **Munkalebontási struktúra sablonok** lehetőséget.
2. Válassza ki a kijelölt WBS-sablon **Részletek** elemét.
3. Jelöljön ki egy feladatot a listából, majd a **Szerepkör** mezőben jelöljön ki egy szerepkört, amelyet hozzá szeretne rendelni a feladathoz.

### <a name="work-with-a-wbs"></a>WBS használata

Létrehozhat új WBS-t, vagy egy meglévő WBS-sablonból is másolhatja a WBS-t. A projektmenedzserek egyszerűen kezelhetik az erőforrásokat, ha szerepköröket rendelnek hozzá az új feladatokhoz a WBS-ben. A szerepköröket ki lehet cserélni az erőforrás megszerzését követően, illetve miután azonosításra került a feladaton dolgozó megerősített erőforrás. Ez a rugalmasság lehetővé teszi a projektmenedzserek számára a következő feladatok végrehajtását:

- A WBS munkacsomagokhoz szükséges erőforrások számának azonosítása.
- Projekt költségeinek becslése.
- Előzetes költségvetés meghatározása.
- Tevékenység időtartamának becslése a szerepkörök és erőforrások alapján.
- A rendelkezésre álló projektadatok alapján néhány projektvezetési terv kidolgozása.

A WBS további opciókkal lett bővítve az erőforrás-biztosítási funkció jobb kihasználásához.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Beállítás</th>
<th>Ismertetés</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Erőforrás-hozzárendelések</td>
<td>A WBS-ben szereplő feladatokhoz tartozó hozzárendelt erőforrások, dátumok, órák száma és foglalástípus megtekintése.</td>
</tr>
<tr class="even">
<td>Csapat automatikus generálása</td>
<td>A tervezett erőforrások automatikus hozzáadása a feladathoz társított szerepkörök használatával. A Pénzügy a szerepkörön alapuló többfeltételű döntési elemzés segítségével automatikusan javasol tervezett erőforrásokat. Miután a szerepkörök és az erőfeszítés (óra) be lett állítva a feladatokhoz a WBS-ben, és a struktúra kiadását követően válassza a <strong>Csapat automatikus generálása</strong> lehetőséget. A tervezett erőforrások szükséges száma hozzáadódik a WBS-hez, valamint a <strong>Projektcsapat és ütemezés</strong> lapon.</td>
</tr>
<tr class="odd">
<td>Erőforrás (legördülő lista)</td>
<td>Az <strong>Erőforrás-hozzárendelés indítása</strong> oldalon a megadott időtartam alapján kijelölheti az erőforrásokat a végleges vagy ideiglenes foglaláshoz. A nézet beállításainak módosításával megtekintheti és beállíthatja az erőforrás-tevékenységek időtartamát. Az erőforrásokat a munkacsomag szintjén adhatja meg és rendelheti hozzá a következő lehetőségek használatával:
<ul>
<li><strong>Elfogadás</strong> – A feladathoz rendelt erőforrás változásainak jóváhagyása.</li>
<li><strong>Visszavonás</strong> – A feladathoz rendelt erőforrás változásainak visszavonása.</li>
<li><strong>Automatikus hozzárendelés</strong> – A kijelölt feladathoz automatikusan kijelöli és hozzárendeli a rendszer a megfelelő szerepkörrel rendelkező, rendelkezésre álló munkatársakkal ellátott erőforrást.</li>
</ul></td>
</tr>
</tbody>
</table>

1. A **Minden projekt** oldalon jelölje ki az **XYZ frissítés 2. fázis** projektet.
2. Válassza a **Terv** &gt; **Tevékenységek** &gt; **Munkalebontási struktúra** lehetőséget.
3. Válassza az **Új** lehetőséget, ha a következő első szintű tevékenységeket szeretné hozzáadni a WBS-hez:

    - Kezdeményezés
    - Tervezés
    - Végrehajtás
    - Figyelés és vezérlés
    - Lezárva

4. Állítsa be a dátumokat és az erőfeszítést (óra), amint az a következő ábrán látható.

    [![Fátumok és erőfeszítés beállítása](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Jelölje ki a **Kezdeményezés** feladatsort, majd a **Szerepkör** mezőben válassza a **Senior projektmenedzser** lehetőséget.
6. Válassza a **Közzététel** lehetőséget.
7. Ugyanabban a sorban, az **Erőforrás** mezőben jelölje ki a **Kovács Dániel** elemet, majd válassza az **Elfogadás** lehetőséget.
8. Válassza ki a **Tervezés** feladatsort, majd a **Szerepkör** mezőben jelölje ki au **Üzleti elemző** elemet.
9. Válassza a **Közzététel** lehetőséget, majd válassza a **Csapat automatikus generálása** lehetőséget.
10. A megjelenő üzenetmezőben válassza az **Igen** lehetőséget.
11. Az **Erőforrás** mezőben ellenőrizze, hogy az érték az **1. üzleti elemző**.
12. Az **1. üzleti elemző** erőforrásnál nyissa meg a keresést, és válassza az **Erőforrás-hozzárendelések indítása** lehetőséget. Ezután válassza ki a feladathoz tartozó dolgozót.
13. Válassza az **Ideiglenes hozzárendelés** &gt; **Teljes kapacitás** lehetőséget.

    > [!NOTE] 
    > Nem kap figyelmeztetést arra vonatkozóan, hogy a megadott erőforrás most 2, mert az erőforrások száma 1 marad.

14. A **Munkalebontási struktúra** oldalon ellenőrizze az erőforrás-hozzárendelést a WBS-ben, majd válassza a **Mentés** lehetőséget.

## <a name="resource-fulfillment-for-planned-resources"></a>Tervezett erőforrások erőforrás-teljesítése
A projektmenedzserek megtervezhetik a projektek szükséges erőforrás-szerepköreit. Az erőforrás-menedzser ezeket a tervezett erőforrásokat kérésekként látja az **Erőforrás-teljesítés** oldalon, és tényleges erőforrásokat rendelhet hozzájuk.

1. A **Minden projekt** oldalon jelölje ki az **XYZ frissítés 2. fázis** projektet.
2. Jelölje ki a **Projekt** elemet, és válassza a **Szerkesztés** lehetőséget.
3. A **Projektcsapat és ütemezés** lapon válassza a **Hozzáadás** lehetőséget.
4. A **Szerepkörök hozzáadása** párbeszédpanelen jelölje ki a **Szoftverfejlesztő** szerepkört.
5. Válassza a **Létrehozás** lehetőséget, és zárja be a projektoldalt.
6. Az **Erőforrás-teljesítés** oldalon válassza az **1. szoftvertesztelő** lehetőséget az **XYZ frissítési projekt 2. fázis** projekt számára.
7. Válasszon ki egy dolgozót, majd válassza ismét a **Hozzárendelés** lehetőséget.
8. Ellenőrizze, hogy az **1. szoftverfejlesztő** sora eltávolításra került-e az **XYZ frissítési projekt 2. fázis** projekt esetében.
9. A **Projektcsapat és ütemezés** lapon az **XYZ frissítés 2. fázis** projektnél ellenőrizze, hogy az előző lépésben kiválasztott dolgozót **szoftverfejlesztőként** adták-e hozzá.

## <a name="requests-for-project-resources"></a>A projekt erőforrásaira vonatkozó kérelmek
A projektek erőforrás-ütemezésére vonatkozó funkció csak az erőforrás-menedzserek számára teszi lehetővé a munkatársakkal ellátott erőforrások elosztását aktivitásokra vagy projektekre. A szolgáltatás engedélyezéséhez hajtsa végre az alábbi műveleteket, vagy ellenőrizze, hogy befejeződtek-e:

- Számsorozatok beállítása.
- Projektmenedzsment és könyvelés munkafolyamatok beállítása.
- Erőforrás-igénylési munkafolyamatok engedélyezése.

Az előző feladatok befejezését követően az alábbi műveleteket hajthatja végre szükségletei szerint:

- Erőforrás-kérelmek létrehozása egy ideiglenesen lefoglalt, munkatársakkal ellátott erőforrásból.
- Erőforráskérelmek felügyelete.
- Erőforrás-kérelmek teljesítése.
- Munkatársakkal ellátott erőforrás kérelmezése a WBS-ből.
- Erőforrások foglalása egy projekthez egy munkatársakkal ellátott erőforrásra vonatkozó kérelem nélkül.

## <a name="monitor-project-teams"></a>Projektcsoportok figyelése
1. A **Minden projekt** oldalon jelölje ki az **XYZ frissítés 2. fázis** projekt **Projektazonosító** hivatkozását.
2. A **Projektcsapat és ütemezés** gyorslapon ellenőrizze, hogy helyesek-e a listában szereplő projekterőforrások.
