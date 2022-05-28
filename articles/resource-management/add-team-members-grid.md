---
title: Csapattagok hozzáadása a Csapattag rácsból
description: Ez a témakör információkat nyújt a csapattag erőforrások kezeléséről.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 85dc7ab4b30359a24994f8f9bf38de3fc2325e60
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588095"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Csapattagok hozzáadása a Csapattag rácsból

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations tartalmaz egy erőforrás-kezelő irányítópultot, amely vizuális áttekintést nyújt az erőforrásigényről és -felhasználásról a szervezet egészében. Az irányítópult diagramjait felhasználhatja a következő információk megjelenítésére:

- **Erőforrásigény**: Az **Aktív erőforrásigény** azokat a erőforrásokat mutatja, amelyeket benyújtottak. Az erőforrásokat szerepkör vagy projekt szerint összesíti.
- **Nem benyújtott erőforrásigény**: A **Hozzá nem rendelt erőforrásigény** ábra az összes, még nem benyújtott erőforrásigényt mutatja. Ez a diagram segít az erőforrás-kezelőknek megtekinteni a nem biztos igényeket, amelyeket erőforráskéréssel nyújthatnak be.
- **Számlázható felhasználás az elmúlt héten**: A **Használat szerep szerint** táblázat mutatja a szervezet tényleges számlázható felhasználásának százalékos arányát a szerepenkénti számlázandó felhasználás százalékában.

    > [!NOTE]
    > A **Használat szerep szerint** diagram elérhetővé tételéhez hozzon létre egy munkát, amely futtatja az **UpdateRoleUtilization** munkafolyamatot. Ez az ismétlődő munka hét naponként fut, hogy kiszámítsa a számlázható felhasználást az előző hét napra. Az eredményeket szerep szerint csoportosítják.

## <a name="manage-project-team-members"></a>Kezelje a projektcsoport tagjait

A projektmenedzserek az erőforrás-kezelő irányítópultját használhatják a projektek erőforrásainak kezelésére. Például felvehetnek egy csapattagot közvetlenül egy projektbe, és lefoglalhatják a csapattagot egy általános erőforrás által elfoglalt erőforrás-követelmények teljesítéséhez.

### <a name="add-a-team-member-directly-to-a-project"></a>Csapattag hozzáadása közvetlenül egy projekthez

Csapattag közvetlen hozzáadásához a projekthez a **Projektek** űrlapon, a **Csapat** lapon válassza az **Új** lehetőséget. Megjelenik a **Gyors létrehozás: Projektcsapattag** párbeszédpanel. Ezen a párbeszédpanelen a következő feladatokat hajthatja végre:

- **Megnevezett erőforrás foglalása**: A **Foglalható erőforrás** mezőben válassza ki az erőforrás nevét. Ezután válassza ki a szerepet, állítsa be az időszakot, és válassza ki az allokációs módszert. A kiválasztott megnevezett erőforrás hozzáadódik a projekthez a kiválasztott elosztási módszer és az erőforrásnaptár használatával.
- **Általános erőforrás hozzáadása**: Hagyja üresen a **Foglalható erőforrás** mezőt, majd válassza ki a szerepet, állítsa be az időszakot, és válassza ki a preferált allokációs módszert. Az általános erőforrások helyőrzőként kerülnek hozzáadásra a csoporthoz. A helyőrző tartalmazza az igénymintát, amely az elnevezett erőforrások lefoglalására szolgál a csoporton. A követelményt a projekt naptárának megfelelően kell megtenni.
- **Adjon meg egy elnevezett erőforrást a csapatnak erőforrás-kapacitás felhasználása nélkül**: A **Foglalható erőforrás** mezőben válassza ki az erőforrást. Válassza ki az időszakot, majd válassza a **Nincs** lehetőséget allokációs módszerként. Az erőforrás hozzáadódik a csapathoz, de az erőforrás kapacitása nem merül fel a foglalás során.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Csapattag lefoglalása az általános erőforrás erőforrásigényének teljesítéséhez

A Project Operations alkalmazásban általános erőforrást foglalhat le egy projektcsoportra. Megadhatja a szerepkört, a szükséges kapacitást és a kapacitás elosztásának módját is. Az erőforrásigény esetében meghatározhatja az általános erőforráshoz társított attribútumokat. Ezek a tulajdonságok tartalmazzák a szükséges készségeket, az előnyben részesített szervezeti egységet és az előnyben részesített erőforrásokat.

Kövesse ezeket a lépéseket a fejlesztői általános erőforráshoz szükséges készségek meghatározásához.

1. A **Projektek** űrlapon, a **Csapat** lapon válassza az **Új** lehetőséget egy általános forrás lefoglalásához.
2. A **Minden csapattag** nézetben, az **Erőforrásigény** oszlopban válassza ki a hivatkozást a szükséges készségek hozzáadásához az általános erőforráshoz.
3. A megjelenő **Erőforrásigény** űrlapon a **Tudás** rácsban válassza ki a három pontot (**...**), majd válassza az **Új igényjellemző hozzáadása** lehetőséget a szükséges képességek fejlesztőhöz való hozzáadásához.
4. A **Gyors létrehozás: Követelményjellemző** párbeszédűrlapon a **Jellemző** mezőben válassza ki a szükséges képességeket.
5. Az **Értékelés** mezőben válassza ki az adott készséghez szükséges jártassági szintet. 
6. Az **Erőforrásigény** mezőben állítsa be az erőforrások forrásának követelményét a szervezeti egységektől, vagy akár a megnevezett erőforrásokat is. Ha kész, válassza a **Mentés** lehetőséget.
7. A **Forrásigény** űrlapon válassza a **Foglalás** elemet az erőforrásigény teljesítéséhez. Kiválaszthatja az általános erőforrást a **Minden csapat tagja** rácsból, majd a **Foglalás** lehetőséget választhatja.

    > [!NOTE]
    > Ebben a példában 40 szükséges óra van, de nincs ténylegesen lekötött óra, mivel az általános forrásoknak nincs foglalása. Ezenkívül nincsenek kijelölt órák, mivel az általános erőforrást közvetlenül a csapathoz adták hozzá a feladat-hozzárendeléssel történő hozzáadás helyett.

    Az **Ütemezési asszisztens** űrlapon a rendelkezésre álló erőforrásokat az erőforrásigényben megadott követelmények szerint szűrheti. Az erőforrásokat az Ütemezési táblán megadott rendezési paraméterek szerint rendezzük.

   A leggyakrabban használt szűrők a következők:

    - **Jellemzők és minősítés**: Szűrés készségek, igazolások és egyéb erőforrás-tulajdonságok alapján, a jártassági besoroláson felül.
    - **Szerepek**: Szűrés az alapértelmezett szerepek szerint, amelyek a foglalható forrásokhoz vannak rendelve.
    - **Szervezeti egységek**: Foglalható erőforrások szűrése szervezeti egységek szerint, amelyekhez hozzá vannak rendelve.

8. Ha nem elégedett a kezdeti keresési eredményekkel, megváltoztathatja a szűrési kritériumokat. Bontsa ki a bal oldalon a **Szűrő nézet** ablakot, majd válassza a **Keresés** lehetőséget további források kereséséhez. Az eredmények rendezésének megváltoztatásához válassza a **Rendezés** lehetőséget.
9. Válassza ki az erőforrásokat a követelményben megadott igénynek megfelelően, a rács tetején feltüntetett módon. Törölheti a cellák kiválasztását a rácsban, és nyitva hagyhatja az erőforrás-kapacitást. Egyszerre csak egy erőforrás választható lefoglaltként.
10. Válassza a **Foglalás** lehetőséget a kiválasztott erőforrás lefoglalásához, és hagyja nyitva az Ütemezési táblát, hogy további erőforrásokat válasszon ki. Alternatív megoldásként válassza a **Foglalás és kilépés** lehetőséget a kiválasztott erőforrás lefoglalásához és az Ütemezési tábla bezárásához.
11. Térjen vissza a **Minden csapattag** nézethez. A rácsban vegye észre, hogy az általános erőforrást felváltotta a megnevezett erőforrás, és a 40 órát az erőforrás lekötöttként sorolja fel.

    > [!NOTE]
    > A hozzárendelt órák nem kerülnek megjelenítésre, mert közvetlenül a csapatra voltak foglalva. Nem feladat-hozzárendeléssel foglaltak őket.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Általános erőforrások rendelése a feladatokhoz és az erőforrás-követelmények generálása

A Project Operations alkalmazásban létrehozhat feladatokat, majd általános erőforrásokat rendelhet hozzájuk. Az erőforrásigényt ezután helyőrzők képviselhetik, miközben becsülheti az ütemtervet és a pénzügyi számokat. Ezután generálhat erőforrásigényeket az általános erőforrásokhoz, és teljesítheti azokat.

1. A **Projektek** űrlapon, az **Ütemezés** lapon válassza a **Hozzáadás** lehetőséget a feladat létrehozásához.
2. Az **Erőforrások** mezőben válassza az **Erőforrás-választó** szimbólumot. Megjelenik az Erőforrás-választó, amely megmutatja a projekt meglévő csapattagjait.
3. Írja be az új általános erőforrás nevét, majd válassza a **Létrehozás** lehetőséget.
4. A megjelenő **Gyors létrehozás: Projektcsapattag** párbeszédpanelen a **Szerep** mezőben válassza ki az általános erőforrás szerepét. 
5. Az **Erőforrásegység** mezőben válassza ki az általános erőforrás szervezeti egységét. Azután válassza a **Mentés** parancsot. Az általános csoporttagot most kiosztották a feladathoz.

   A **Csapat** lapon láthatja az új általános csapattagot. Vegye észre, hogy csak órákat adott meg. Ezek az órák az összes feladat összegét adják, amelyeket az általános csapattagnak kiosztottak. Az általános csapattagnak nincs szüksége órára vagy erőforrás-igényre.

6. Most az Erőforrás-választó segítségével hozzárendelheti az általános csapattagot más feladatokhoz.

   Ha befejezte az általános erőforrás hozzárendelését a feladatokhoz, generálhat egy erőforrás-követelményt az általános erőforráshoz.

7. A **Csapat** lapon válassza ki az általános erőforrást, majd válassza a **Követelmény generálása** lehetőséget. A követelmény előállításakor az általános csapattagnak rendelkeznie kell a szükséges órákkal és egy linkkel az erőforrás-igényhez.

  Miután egy megnevezett erőforrást lekötött, az általános erőforrás eltávolításra kerül a csapatból, és helyébe a megnevezett erőforrás kerül. Az **Ütemezés** lapon az általános erőforrás-hozzárendelések eltávolításra kerülnek, és helyébe a megnevezett erőforrás lép.

  > [!NOTE]
  > Ez a viselkedés csak akkor fordul elő, ha a megnevezett erőforrást teljes mértékben lefoglalják az általános erőforrás-igényre. Ha egy megnevezett erőforrás részben helyettesíti az általános erőforrás-igényt, vagy több megnevezett erőforrás helyettesíti az általános erőforrás-követelményt, akkor az általános erőforrás továbbra is hozzá van rendelve a feladathoz.

A Project Operations alkalmazás nem rendeli hozzá mindkét erőforrást a feladathoz, mert ez a viselkedés kevésbé kiszámítható ütemezést eredményezne. Ebben az egyszerű példában könnyű elosztani az órákat két erőforrás között. Az összetettebb forgatókönyvekben, amelyek több feladatot és több erőforrást foglalnak magukban, a PSA-nak feltételezéseket kell tennie arra vonatkozóan, hogy hogyan kell elosztani a több erőforráshoz kapott foglalásokat több feladat között.

Ezért ezekben a forgatókönyvekben a projektmenedzser felel a többszörös foglalás elemzéséért és a szükséges hozzárendeléséért. A foglalások kiosztásához a projektmenedzser az általános erőforrásokból a megnevezett erőforrásokhoz rendeli a feladatokat, majd az **Összehangolás** nézetet használja annak ellenőrzésére, hogy az allokáció a foglalásokkal együtt működik-e.

### <a name="edit-a-resource-requirement"></a>Erőforrásigény szerkesztése

Az erőforrásigény létrehozása után a projektmenedzser vagy az erőforrás-kezelő módosíthatja a részleteket, hogy finomítsa a keresési feltételeket az Ütemezési tábla használatakor. Az erőforrásigény szerkesztéséhez kövesse ezeket a lépéseket.

1. A **Projektek** űrlapon, a **Csapat** lapon válassza ki az általános erőforrás követelményeinek hivatkozását.
2. A megjelenő **Erőforrás-követelmény** űrlapon adja meg a szükséges mezők információit.

   Az **Erőforrás-követelmény** űrlapon a projektmenedzser vagy az erőforrás-kezelő is definiálhatja a képzettségeket, a szerepköröket, az erőforrás-preferenciákat és az előnyben részesített szervezeti egységet.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Frissítse az erőforrás-foglalásokat, miután azokat egy projektre lefoglalták

Miután hozzáadott egy általános vagy megnevezett erőforrást egy projektcsoporthoz, megváltoztathatja az erőforrás foglalásait.

1. A **Projektek** űrlapon, a **Csapat** lapon válassza ki a csapattagot, majd válassza a **Foglalás fenntartása** lehetőséget.
 
   Megjelenik az Ütemezési tábla, amely megmutatja a projektcsoport tagjainak foglalásait. Bővítse a csapattag rekordját, hogy megnézhesse az órákat, amelyeket ez a projekt és más projektek foglaltak le, felhasználva a csapattag kapacitását.

2. Válassza ki és húzza el a foglalást annak meghosszabbításához vagy rövidítéséhez. Megjelenik egy **Erőforrás-foglalás létrehozása** párbeszédpanel, amely lehetővé teszi a foglalás módosítását.
3. Kattintson a jobb gombbal a foglalásra. Ezután a helyi menü segítségével elvégezheti a következő műveleteket:

    - A foglalás állapotának módosítása
    - A foglalás szerkesztése
    - Egy erőforrás felváltása a projektcsapatban

### <a name="change-the-booking-status"></a>A foglalás állapotának módosítása

Az alapértelmezett vagy az egyéni foglalás állapotának módosítása.

A Project Operations a következő állapotokat tartalmazza:

- **Törölve**: Visszavonja egy erőforrás foglalását, és felszabadítja az erőforrás kapacitását.
- **Végleges lefoglalás**: Felhasználja az erőforrás kapacitását. A foglalás jellemzően akkor veszi fel ezt az állapotot, amikor megnyitja a **Foglalás fenntartása** panelt a **Minden csapattag** rácsból a **Projektek** űrlapon.
- **Ideiglenes lefoglalás**: Hozzáad egy erőforrást a csapathoz, de nem használja fel az erőforrás kapacitását. Ez az állapot jelzi, hogy az erőforrást fenntartották a lehetséges munkavégzéshez, de még mindig rendelkezik kapacitással, ha más munkákhoz szükséges. Az általános erőforrás-rendelkezésre állás szempontjából a puha foglalások eltérő státusszal rendelkeznek, mint a kemény foglalások.
- **Javasolt**: Egy erőforrás-kezelő vagy projektmenedzser erőforrásra tett javaslatát reprezentálja. A javaslatok nem használják fel egy erőforrás kapacitását, és az erőforrás nem kerül hozzáadásra a projekt csapatához. Annak érdekében, hogy az erőforrást a csapatba foglalhassák, a projektmenedzsernek el kell fogadnia a javaslatot.

### <a name="submit-resource-requests"></a>Erőforrás-kérelmek elküldése

Az erőforrás-kérelmek a kereslet vagy erőforrás-igény teljesítésére szolgálnak, amelyet az erőforrás-kezelőnek teljesítenie kell. Ha egy általános erőforrás már létezik a csapatban, akkor közvetlenül küldhet erőforrás-kérelmet. Az erőforrás-igényt kétféle módon lehet teljesíteni:

- Az erőforrás-kezelő közvetlenül teljesíti a kérést. Ebben az esetben az általános erőforrást egy kemény foglalás váltja fel, amelynek megnevezett erőforrása van.
- Az erőforrás-kezelő erőforrást javasol a projektmenedzser számára, a projektmenedzser pedig jóváhagyja vagy elutasítja a javasolt erőforrást.

#### <a name="direct-fulfillment-of-resource-requests"></a>Az erőforrás-kérelmek közvetlen teljesítése

Amikor egy erőforrásigény keletkezik, a projektmenedzser benyújthat egy erőforrásigényt egy általános erőforrásra az erőforrás kiválasztásával, majd az **Igény benyújtása** ponttal. Az erőforrással kapcsolatos megjegyzéseket meg lehet adni az erőforrás-kezelőnek, aki teljesíti a kérést. Az igény benyújtása után a csapattag **Állapot** mezője **Beküldve** lesz. Amikor az erőforrás-kezelő teljesíti a kérést, az általános csapattagot a **Minden csapattag** rácsban a megnevezett erőforrás váltja fel.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Erőforrás-javaslat használata erőforrás-kérelmekhez

Ahelyett, hogy egy erőforrást közvetlenül egy erőforráskérésre foglalna, az erőforrás-kezelő erőforrást javasolhat a projektmenedzser számára. Az erőforrás-kezelő akkor használhatja ezt a lehetőséget, ha a követelményekhez nem áll rendelkezésre pontos egyezés. Amikor egy erőforrás-kezelő erőforrást javasol, a projektmenedzser látja, hogy az általános csapattag **Állapot** mezője **Áttekintés szükséges** lesz.

A javasolt erőforrást megtekintheti a javaslat foglalásának hatásával együtt. 

1. Kattintson duplán arra a csapattagra, amely **Ellenőrzés szükséges** állapottal rendelkezik. 
2. Válassza a **Javasolt erőforrások** fület.
3. Válassza **Az összes javaslat elfogadása** elemet az összes javasolt erőforrás elfogadásához, vagy az **Összes javaslat elutasítása** opciót az elutasításhoz. Ha elfogadja a javasolt erőforrásokat, akkor ezeket a projektre csapattagokként foglalják, és felváltják az általános erőforrásokat.

> [!NOTE]
> Valamennyi elfogadott erőforrást el kell fogadnia vagy el kell utasítania. Részben nem fogadhatja el vagy utasíthatja el őket.

### <a name="substitute-a-resource-on-the-project-team"></a>Egy erőforrás felváltása a projektcsapatban

Időnként a projektmenedzsernek helyettesítenie kell egy lefoglalt csapattagot egy projektnél.

1. A **Projektek** űrlapon, a **Csapat** fülön válassza ki a helyettesítő erőforrást, majd válassza a **Foglalások fenntartása** lehetőséget.
2. Bontsa ki az erőforrást a hozzárendelt projektek megtekintéséhez.
3. Kattintson a jobb gombbal a projektre, majd válassza a **Helyettesítő erőforrás** lehetőséget.
4. Ha ismeri az erőforrást, amelyet helyettesíteni szeretne az aktuális erőforrással, jelölje ki vagy írja be a nevet, majd válassza az **Újbóli hozzárendelés** lehetőséget.

Vagy, ha egy erőforrást kell keresnie, hajtsa végre a következő lépéseket.

1. Válassza a **Helyettesítő keresése** lehetőséget.

   Az Ütemezési segéd visszaadja az elérhető helyettesítők listáját. Az Ütemezési segédben tovább szűrheti a rendelkezésre álló erőforrásokat a megfelelő helyettesítő megtalálásához.

2. Az erőforrás helyettesítéséhez válassza ki a kívánt erőforrást, majd válassza a **Helyettesítő** lehetőséget.   

   A foglalásokat és a feladatokat az új erőforrás váltja fel.

## <a name="reconcile-team-member-bookings-and-assignments"></a>A csapattagok foglalásainak és feladatainak egyeztetése

A csapat tagjai számára a foglalások és a megbízások lazán kapcsolódnak egymáshoz. Más szavakkal: az erőforrásoknak lehetnek hozzárendelései, de foglalásai nem, vagy lehetnek foglalásaik, de nem lehet hozzárendeléseik. Ideális esetben a foglalásokat és a feladatokat össze kell hangolni, hogy az erőforrások képesek legyenek a feladat-hozzárendelések végrehajtására. Előfordulhat azonban, hogy a foglalások rendelkezésre álláson alapulnak, és a projekt folytatásakor a feladatok ütemezése változhat. Ezért a foglalások és feladatok laza csatolása rugalmasságot biztosít.

A Project Operations rendelkezik egy **Egyeztetés** lappal, amely lehetővé teszi a projektmenedzserek számára, hogy összehangolják a csapattagok foglalásait és a projektcsoportokhoz rendelt megbízásaikat.

Az **Egyeztetés** lap a foglalásokat és a hozzárendeléseket az egyes csoporttagok egyedi feladat-hozzárendelésének szintjéig mutatja. A cellákban órákat jelenít meg, amelyek hónapoktól napokig terjedő időszakokat jelent.

A fül a projekt teljes nettó összértékét, valamint az Összesen oszlopot is mutatja.

Az egyes erőforrások esetében a fül kiszámítja a különbséget a csapattag foglalása és a csoporttag feladatainak összeállítása között. Ideális esetben ennek a különbségnek 0-nak (nulla) kell lennie. Más szavakkal, nem lehet különbség a foglalások és a megbízások között. A különbségek színesek és árnyaltak, hogy felhívják a figyelmet két körülményre:

- **Foglalási hiány**: Akkor fordul elő, ha az erőforrás több hozzárendeléssel rendelkezik, mint a foglalások. Mivel ez a kapacitás nem volt fenntartva, a projektmenedzser javíthatja ezt a feltételt azáltal, hogy az erőforrás foglalásait kiterjeszti a hiány fedezésére.
- **Többletfoglalások**: Akkor fordulnak elő, amikor egy erőforrást lefoglaltak a projekthez, de nem rendeltek hozzá feladatokhoz. Ez a feltétel elfogadható lehet azokban az esetekben, amikor az erőforrást a projekthez a feladat-hozzárendelés megtörténte előtt lefoglalták. Más esetekben azonban az erőforrást nem tervezik feladatokhoz rendelni. Ezekben az esetekben a projektmenedzsernek fontolóra kell vennie az erőforrás foglalásainak visszavonását, hogy a kapacitás felhasználható legyen egy másik projekthez.

Bizonyos esetekben, ha az időt a napi szintnél magasabb szinten nézi (például a hónap szintjén), akkor az erőforrás nettó különbsége nulla lehet. Más szóval, foglalások = megbízások. Ha azonban az időt heti szinten tekinti, akkor láthatja, hogy az első héten nulla órás megbízások és 40 órás foglalások vannak, a második héten pedig 40 órás megbízások és nulla órás foglalások vannak. Összességében a foglalások és a feladatok összeegyeztethetők, de hetente különböznek.

Ha az időt magasabb szinteken tekinti meg, akkor az **Egyeztetés** lapon lévő cellák jelzik, hogy az alacsonyabb szinteken eltérések vannak. Ha egy cellába duplán kattint, nagyíthat, hogy megnézze a különbséget. Ezután jobb egérgombbal kattinthat a kicsinyítéshez. Ha kiválaszt egy erőforrást, majd kiválasztja a rács eszköztár **Következő különbség** elemét, a következő különbséghez ugorhat az adott erőforrás foglalása és hozzárendelése között. A visszalépéshez válassza az **Előző eltérés** lehetőséget. A különbségjelzőt és a navigációs viselkedést a **Beállítások** alatt is kikapcsolhatja.

Ha az erőforráshoz feladatok vannak hozzárendelve, de nincs foglalása, akkor a **Projektek** űrlapon, az **Egyeztetés** lapon válassza ki a foglalási hiányt, majd válassza a **Foglalás kiterjesztése** lehetőséget. Megjelenik a **Foglalás kiterjesztése** párbeszédpanel, amely megmutatja az erőforrás hiányának kezeléséhez szükséges foglalást. A párbeszédpanel ezenkívül megmutatja az erőforrás meglévő foglalásait az összes projektben vagy más ütemezhető entitásban. Ha az **OK** lehetőséget választja az erőforrás foglalásának elkészítéséhez, az erőforrás elérhetőségétől függetlenül túlfoglalást okozhat.

A projektmenedzser vagy az erőforrás-kezelő ezután felhasználhatja az Ütemezési táblát olyan helyzetek kezelésére, amikor egy erőforrás túlfoglalása meghaladja a kapacitást.


[!INCLUDE[footer-include](../includes/footer-banner.md)]