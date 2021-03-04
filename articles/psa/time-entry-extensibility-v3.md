---
title: A heti időbejegyzés testreszabása
description: Ez a témakör ismerteti az egyéni üzleti szabályok végrehajtásának módját, amelyek támogatják a szervezet gyakorlatait.
author: stsporen
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
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
ms.openlocfilehash: a34244884bc81da74ae3bf550bde6f982d04abd3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149636"
---
# <a name="customize-weekly-time-entry"></a>A heti időbejegyzés testreszabása 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A Microsoft Dynamics 365 Project Service Automation 3.3-as verziójában a Microsoft bevezetett egy modern rácsot, amely lehetővé teszi a projekt erőforrásai számára, hogy egyszerre akár hetenként, gyorsan beírhassák az időt. Az új heti időbeviteli rács dátum, sor vagy hét alapján összesített bejegyzéseket mutathat. Az erőforrások másolatot készíthetnek az időbejegyzésekről a héten belül, valamint tömegesen másolhatják az előző heteket is. A rendszer testreszabói testreszabhatják a nézetet mezők hozzáadásával, más entitásokra vonatkozó keresések hozzáadásával és az egyéni üzleti szabályok végrehajtásával a szervezet gyakorlatának támogatása érdekében.

Az időbevitel és az új heti időrendszer a webhelytérképen érhető el. A nem kiterjeszthető egyedi időbeviteli környezetet, amely a korábbi PSA-verziók részét képezte, felváltotta a bővíthető heti időbeviteli rács, valamint az alternatív környezet a csak olvasható rácson és a naptárban. E változás miatt a felhasználók heti mennyiségekben adhatják meg az időt.

## <a name="page-layout"></a>Oldalelrendezés
Az új heti időbeviteli rács egyéni vezérlőelem, amelynek eszköztára és két fő része van, a **Dimenziók** és az **Időtartam**. Az eszköztár tartalmaz egy gombot, amely csak az időbeviteli rács ezen egyedi vezérlésére vonatkozik. Ezzel szemben az oldal tetején található Műveleti ablaktábla gombjai a vezérlőelemek három típusára vonatkoznak, amelyek az időbevitelt támogatják: a heti időbeviteli vezérlés, a csak olvasható vezérlés és a naptárvezérlés.

### <a name="dimensions"></a>Méretek
A **Dimenziók** szakasz oszlopfejlécként mutatja az összes olyan méretet, amelyre az idő megadható. A következő dimenziók támogatottak készen:

- Projekt
- Projektfeladat
- Szerepkör
- Típus
- Bejegyzés állapota

A **Dimenziók** szakasz nem engedi meg a sorszerkesztést. Ezt a részt egy olyan nézet támogatja, amely lehetővé teszi az egyedi mezők hozzáadását a heti időbeviteli rácshoz. Az egyéni mezők hozzáadásával kapcsolatos információkat a téma későbbi szakaszában, a „Bővíthetőség” szakaszban talál.

### <a name="duration"></a>Időtartam
Az Időtartam szakasz a hét napjait mutatja oszlopfejlécként. Ez a szakasz lehetővé teszi a belső szerkesztést. Miután létrehozott egy időbeviteli sort, amely rendelkezik megfelelő dimenziókkal, a felhasználók gyorsan bevihetik az ezen dimenziókra fordított időt.

## <a name="create-a-new-time-entry"></a>Új időbejegyzés létrehozása
Új időbejegyzés létrehozásához az időbeviteli rácsban válassza az **Új** lehetőséget. Megjelenik az **Időbevitel gyors létrehozása** párbeszédablak. Ezen a párbeszédpanelen a felhasználók kiválaszthatják az időbeviteli dátumot, majd a **h**, **m** vagy **d** és egy szám beírásával beírhatják a **Projekt**, **Projektfeladat**, **Szerep** és **Időtartam** dimenziókat percben, órában vagy napban. A felhasználók beírhatnak egy leírást és megjegyzéseket, amelyek külsőleg megoszthatók az időbevitelre vonatkozóan. Amikor a felhasználó menti a módosításokat, akkor a dimenziókhoz beírt értékek megjelennek a **Dimenziók** szakaszban. A **Időtartam** mezőbe beírt időtartam-információk abban az időpontban jelennek meg, amelyre az időbejegyzés létrejött.

A keresési mezőket rendszernézetek támogatják. Például, miután egy felhasználó belépett egy projektbe, a **Projektfeladat** mező alapértelmezés szerint **Másolat** nézetre van állítva. Felhasználóhoz nem rendelt feladatokhoz időbejegyzések létrehozásához válassza a **Nézet módosítása** elemet a keresési párbeszédablakban, és válassza ki az **Összes aktív projektfeladat** nézetet.

## <a name="edit-a-time-entry"></a>Időbejegyzés szerkesztése
Az időbeviteli oldal egyes mezőinek, például a **Leírás** és a **Külső megjegyzések** részletei nem jelennek meg a heti időbeviteli rácsban. Ehelyett egy kis háromszögmutató jelenik meg az időtartamcellákban, amelyek rendelkeznek ezekkel a további részletekkel. Válassza ki a cellát, majd válassza a **Részletek szerkesztése** elemet az adatok megtekintéséhez a **Gyorsszerkesztés** ablaktáblában. Egy adott időbejegyzés részleteinek szerkesztéséhez vagy frissítéséhez, amelyek nem tartoznak a heti időbeviteli rácshoz, a felhasználóknak meg kell nyitniuk a **Gyorsszerkesztés** ablaktáblát.

## <a name="copy-a-time-entry-row"></a>Időbeviteli sor másolása
Az első beviteli sor létrehozása után a felhasználók választhatják a **Sor másolása** lehetőséget az egész sort egy új sorra másolásához. Ha egy sort ilyen módon másolnak, akkor a dimenziókat és az időtartamokat is lemásolják. A felhasználók választhatják a **Sor szerkesztése** elemet is, hogy a dimenzióértékeket és időtartamokat frissítsék az **Időtartam** szakaszban.

## <a name="open-a-time-entry"></a>Időbejegyzés megnyitása
Az optimális és gyors bevitel támogatására a legszembetűnőbb mezőkben a heti időbeviteli rács a kiválasztott dimenziók és időtartamok egy részhalmazát mutatja. Az egy bejegyzés összes részletének megtekintéséhez a **Bejegyzés szerkesztése** válassza a **Megnyitás** lehetőséget.

## <a name="submit-a-time-entry"></a>Időbejegyzés beküldése
A felhasználók egyetlen időbejegyzést vagy időbejegyzéscsoportot nyújthatnak be, kiválasztva a cellák egy tömbjét vagy egy teljes időbeviteli sort, majd a **Küldés** menüpontot használva. A benyújtott időbejegyzések olyan bejegyzésekként jelennek meg, amelyek jóváhagyásra várnak a jóváhagyók **Jóváhagyás** oldalán. Az időbejegyzések sikeres benyújtás után nem szerkeszthetők.

## <a name="recall-a-time-entry"></a>Időpont előhívása
Előhívhatja a benyújtott időbejegyzéseket. Előhívhat egyetlen időbejegyzést, időbejegyzés-blokkot vagy az időbejegyzések egész sorát. Az előhívott időbejegyzések az erőforrások számára elérhetők szerkesztésre.

## <a name="time-entry-status"></a>Időbejegyzés állapota
Az új időbejegyzések automatikusan **Vázlat** státuszt kapnak. Időbejegyzés benyújtásakor az állapot frissül **Beküldve** értékre. Amikor a benyújtott időbejegyzés jóváhagyásra kerül, az állapot frissül **Jóváhagyott** értékre. Ha egy időbejegyzés elutasításra kerül, az állapot frissül **Visszaadott** értékre, és a bejegyzés javításra és újbóli elküldésre rendelkezésre áll. Csak a **Vázlat** állapotú időbejegyzéseket lehet törölni.

## <a name="view-rejection-comments"></a>Az elutasító megjegyzések megtekintése
Ha egy jóváhagyó elutasítja az időbejegyzést, a jóváhagyó elutasító megjegyzéseket fűzhet hozzá, hogy segítse az erőforrást az elutasítás okának megértésében. Az időbejegyzés elutasító megjegyzéseinek megtekintéséhez válassza a **Bejegyzés megnyitása** lehetőséget. Az elutasító megjegyzések megjelennek az idővonalban. Az idővonalban az erőforrás válaszolhat az elutasító megjegyzésekre, mielőtt újból benyújtja a bejegyzést.

## <a name="copy-week"></a>Hét másolása
Néhány időbejegyzés létrehozása után a felhasználók választhatják a **Hét másolása** lehetőséget további időbejegyzések tömeges létrehozására. Megjelenik a **Másolás** párbeszédpanel. Az **Időszak kezdete** részben használja a **Kezdés dátuma** és **Végdátum** mezőket a dátumtartomány meghatározására, ahonnan másolni szeretné az időbejegyzéseket. Az **Időszak vége** szakaszban, a **Kezdő dátum** mezőben adja meg a dátumot, ahova időbejegyzéseket szeretne létrehozni. Ezután válassza a **Másolás** lehetőséget. Az „-ig” időszakban megadott dátumra elkészül a „kezdő” időszakban a hét megfelelő napjára vonatkozó időbejegyzések másolata. Például a múlt hét hétfői időbejegyzését annak a hétnek a hétfőjére másolják, amelyet „ide” periódusként adtak meg.

## <a name="import"></a>Importálás
Ugyanazt az alapvető eljárást használják a foglalásokból, megbízásokból és cserékből történő importáláshoz. A felhasználók megadhatják a dátumtartományt, ahonnan a foglalásokat importálták. Ezután kifejezetten ki kell választaniuk azokat a foglalásokat, amelyeket be kell vonni a vázlatos időbejegyzésekbe. Az előző kiadásban a javasolt időbejegyzések megjelentek a rácsban és a naptárban, és elvesztek a munkamenet frissítésekor.

## <a name="extensibility"></a>Bővíthetőség
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Egyéni mezők hozzáadása, amelyek kereséssel rendelkeznek más entitásokhoz
Három fő lépés van az egyéni mező hozzáadásához a heti időbeviteli rácshoz.

1.  Adja hozzá az egyéni mezőt a gyors létrehozás párbeszédpanelhez.
2.  Konfigurálja a rácsot az egyéni mező megjelenítéséhez.
3.  Adja hozzá az egyéni mezőt a sorszerkesztési feladatfolyamathoz vagy a cellaszerkesztési feladatfolyamathoz.

Azt is ellenőriznie kell, hogy az új mező rendelkezik-e a szükséges érvényesítésekkel a sorban vagy a cellában lévő szerkesztési feladat folyamatában. E lépés részeként le kell zárni a mezőt az időbeviteli állapot alapján.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Egyéni mező hozzáadása a gyors létrehozás párbeszédpanelhez
Az egyéni mezőt hozzá kell adnia az Időbejegyzés gyors létrehozása párbeszédpanelhez, hogy a felhasználók az **Új** gombbal beírhassanak értéket, amikor időbejegyzéseket adnak hozzá.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>A rács konfigurálása az egyéni mező megjelenítéséhez
Kétféle módon adhat hozzá egyéni mezőt a heti időbeviteli rácshoz. Az első lehetőség a **Heti** időbejegyzés nézet testreszabása és az egyedi mező hozzáadása. Kiválaszthatja az egyéni mező helyét és méretét a rácson, a nézetben szereplő tulajdonságok szerkesztésével.

A második lehetőség egy új, egyéni időbeviteli nézet létrehozása és alapértelmezett nézetként beállítása. Ennek a nézetnek tartalmaznia kell a **Leírás** és **Külső megjegyzések** mezőket, azon oszlopok mellett, amelyeket a rácson szeretne elhelyezni. A rács pozícióját, méretét és alapértelmezett rendezési sorrendjét úgy választhatja meg, hogy szerkeszti ezeket a tulajdonságokat a nézetben. Ezután állítsa be a nézet egyedi vezérlőjét úgy, hogy az egy **Időbeviteli rács** vezérlő legyen. Adja hozzá ezt a vezérlőt a nézethez, és válassza ki az internethez, a telefonhoz és a táblagéphez. Ezután konfigurálja a heti időbeviteli rács paramétereit. Állítsa a **Kezdő dátum** mezőt **msdyn_date** értékre, állítsa az **Időtartam** mezőt **msdyn_duration** értékre, és állítsa az **Állapot** mezőt **msdyn_entrystatus** értékre. Az alapértelmezett nézethez a **Csak olvasható állapotlista** mező **192350002,192350003,192350004** értékre van állítva, a **Sor szerkesztési feladatfolyam** mező **msdyn_timeentryrowedit**, a **Cellaszerkesztési folyamat** mező pedig **msdyn_timeentryedit** értékre van állítva. Testreszabhatja ezeket a mezőket az írásvédett állapot hozzáadásához vagy eltávolításához, vagy egy sor feladat alapú élmény (TBX) használatához a sor vagy cella szerkesztéséhez. Ezeket a mezőket statikus értékhez kell kötni.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Egyéni mező hozzáadása a megfelelő szerkesztési feladatfolyamathoz
A szerkesztéshez használt TBX oldalak a **Folyamatok** alatt találhatók. Az alapértelmezett oldalak: **Project Service - Időbejegyzési sor szerkesztése** és **Project Service - Időbejegyzés szerkesztése**. Szerkesztheti ezeket az alapértelmezett oldalakat, vagy létrehozhat új, egyedi TBX oldalakat.

> [!NOTE] 
> Mindkét lehetőség eltávolítja a **Projekt** és a **Projektfeladat** entitásokból a kész szűréseket, így az entitások összes keresési nézete látható lesz. Azonnal csak a vonatkozó keresési nézetek láthatók.

Meg kell határoznia a megfelelő feladatáramlást az egyéni mezőhöz. Valószínűleg, ha hozzáadta a mezőt a rácshoz, akkor annak a sornak a szerkesztési feladatfolyamatában kell lennie, amelyet azokhoz a mezőkhöz használnak, amelyek az összes időbejegyzésre vonatkoznak. Ha az egyéni mezőnek minden nap egyedi értéke van, például egy egyedi mező a **Befejezési idő** számára, akkor a cellaszerkesztési feladatfolyamatba kell kerülnie.

Az egyéni mező feladatfolyamathoz való hozzáadásához húzza a **Mező** elemet az oldal megfelelő pozíciójába, majd állítsa be annak tulajdonságait. Állítsa a **Forrás** tulajdonságot **Időbevitel** értékre, és állítsa az **Adatmező** tulajdonságot az egyedi mezőre. A **Mező** tulajdonság a megjelenített nevet adja meg a TBX oldalon. A módosítások mezőbe történő mentéséhez válassza az **Alkalmazás** lehetőséget. Ezután válassza a **Frissítés** elemet a módosítások mentéséhez az oldalra.

Ha új, egyedi TBX oldalt szeretne használni, hozzon létre egy új eljárást. Állítsa a kategóriát **Üzleti folyamat** értékre, állítsa az entitást **Időbevitel** értékre, és állítsa az üzleti folyamat típusát **Folyamat futtatása feladatfolyamatként** értékre. A **Tulajdonságok** alatt az **Oldal neve** tulajdonságot az oldal megjelenített nevére kell beállítani. Adja hozzá az összes vonatkozó mezőt a TBX oldalhoz. Mentse és aktiválja a folyamatot, majd frissítse az adott feladatáramlás egyedi vezérlő tulajdonságát a folyamat **Név** értékére.

### <a name="add-new-option-set-values"></a>Új beállítási értékek hozzáadása
Az opcionálisan beállított értékek kész mezőhöz történő hozzáadásához nyissa meg a mező szerkesztési oldalát, majd a **Típus** alatt válassza a beállítás mellett a **Szerkesztés** lehetőséget. Ezután adjon hozzá egy új opciót, amelynek egyedi címkéje és színe van. Ha új időbeviteli státust szeretne hozzáadni, akkor a kész mező neve **Beviteli állapot**, nem **Állapot**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Új időbeviteli állapot kijelölése csak olvashatóként
Ha egy új időbeviteli állapotot csak olvashatónak szeretne megadni, akkor adja hozzá az új időbeviteli értéket (a számot, ne a címkét) a **Csak olvasható állapotlista** tulajdonsághoz. Az időbeviteli rács szerkeszthető része az új állapotú sorok számára zárolva lesz.
Ezután adjon hozzá üzleti szabályokat az összes mező lezárásához az **Időbejegyzés sor szerkesztése** és az **Időbejegyzés szerkesztése** TBX oldalakon. Az oldalak üzleti szabályaihoz úgy férhet hozzá, hogy megnyitja az oldal üzletifolyamat-szerkesztőjét, majd kiválasztja az **Üzleti szabályok** lehetőséget. Az állapotot hozzáadhatja a feltételhez a meglévő üzleti szabályokban, vagy hozzáadhat egy új üzleti szabályt az új állapothoz.

### <a name="add-custom-validation-rules"></a>Egyéni ellenőrzési szabályok hozzáadása
Kétféle érvényesítési szabályt lehet felvenni a heti időbeviteli rács környezetébe: • Ügyféloldali üzleti szabályok, amelyek a gyorsan létrehozható párbeszédpanelek és TBX oldalakon működnek. • Szerveroldali beépülő modulok érvényesítései minden időbejegyzésre vonatkoznak

#### <a name="business-rules"></a>Üzleti szabályok
Az üzleti szabályok segítségével zárolhatja és feloldhatja a mezőket, mezőkbe írhat be alapértelmezett értékeket, és meghatározhatja azokat az érvényesítéseket, amelyek csak az aktuális időbeviteli rekordból tartalmaznak információt. A TBX-oldal üzleti szabályaihoz úgy férhet hozzá, hogy megnyitja az oldal üzletifolyamat-szerkesztőjét, majd kiválasztja az **Üzleti szabályok** lehetőséget. Ezután szerkesztheti a meglévő üzleti szabályokat, vagy hozzáadhat új üzleti szabályokat. A még testreszabottabb ellenőrzésekhez használhat egy üzleti szabályt JavaScript futtatásához.

#### <a name="plug-in-validations"></a>Beépülő modul érvényesítések
A beépülő modul érvényesítéseket használhatja minden olyan érvényesítéshez, amely több kontextust igényel, mint amely egyetlen időbejegyzés-rekordban elérhető, vagy olyan ellenőrzésekhez, amelyeket a rácson belüli inline frissítésekkel kíván futtatni. Az érvényesítés befejezéséhez hozzon létre egy egyedi beépülő modult az **Időbejegyzés** entitáson.

> [!IMPORTANT] 
> Jelenleg a TBX-oldalak ismert problémája megakadályozza a felhasználókat abban, hogy javítsák az információkat, és újból kiválasszák a Kész lehetőséget, ha a frissítés nem sikerül a beépülő modul érvényesítésében. Megkerülő megoldásként állítsa be az üzleti szabályok érvényesítését a helyzet lehető legnagyobb mértékű megelőzése érdekében.


[!INCLUDE[footer-include](../includes/footer-banner.md)]