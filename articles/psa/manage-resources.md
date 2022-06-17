---
title: Erőforrások kezelése
description: Ez a cikk az erőforrások kezelésének módjáról nyújt tájékoztatást.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 5709f7f179b14606690549c77ede7ba03b77e1b1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920431"
---
# <a name="manage-resources"></a>Erőforrások kezelése

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A Dynamics 365 Project Service Automation tartalmaz egy erőforrás-kezelő irányítópultot, amely vizuális áttekintést nyújt az erőforrásigényről és -felhasználásról a szervezet egészében. Az irányítópult diagramjait felhasználhatja a következő információk megjelenítésére:

- **Erőforrásigény** - Az **Aktív erőforrásigény** azokat a erőforrásokat mutatja, amelyeket benyújtottak. Az erőforrásokat szerepkör vagy projekt szerint összesíti.
- **Nem benyújtott erőforrásigény** - A **Hozzá nem rendelt erőforrásigény** ábra az összes, még nem benyújtott erőforrásigényt mutatja. Segít az erőforrás-kezelőknek megtekinteni a nem biztos igényeket, amelyeket erőforrás-kéréssel nyújthatnak be.
- **Számlázható felhasználás az elmúlt héten** - A **Használat szerep szerint** táblázat mutatja a szervezet tényleges számlázható felhasználásának százalékos arányát a szerepenkénti számlázandó felhasználás százalékában.

    > [!NOTE]
    > A **Használat szerep szerint** diagram elérhetővé tételéhez hozzon létre egy munkát, amely futtatja az UpdateRoleUtilization munkafolyamatot. Ez az ismétlődő munka hét naponként fut, hogy kiszámítsa a számlázható felhasználást az előző hét napra. Az eredményeket szerep szerint csoportosítják.

## <a name="manage-project-team-members"></a>Kezelje a projektcsoport tagjait

A projektmenedzserek az erőforrás-kezelő irányítópultját használhatják a projektek erőforrásainak kezelésére. Például felvehetnek egy csapattagot közvetlenül egy projektbe, és lefoglalhatják a csapattagot egy általános erőforrás által elfoglalt erőforrás-követelmények teljesítéséhez.

### <a name="add-a-team-member-directly-to-a-project"></a>Csapattag hozzáadása közvetlenül egy projekthez

Csapattag közvetlen hozzáadásához a projekthez a **Projektek** oldalon, a **Csapat** lapon válassza az **Új** lehetőséget. Megjelenik a **Gyors létrehozás: Projektcsapattag** párbeszédpanel. Ezen a párbeszédpanelen a következő feladatokat hajthatja végre:

- **Megnevezett erőforrás foglalása** - A **Foglalható erőforrás** mezőben válassza ki az erőforrás nevét. Ezután válassza ki a szerepet, állítsa be az időszakot, és válassza ki az allokációs módszert. A kiválasztott megnevezett erőforrás hozzáadódik a projekthez a kiválasztott elosztási módszer és az erőforrásnaptár használatával.
- **Általános erőforrás hozzáadása** - Hagyja üresen a **Foglalható erőforrás** mezőt, majd válassza ki a szerepet, állítsa be az időszakot, és válassza ki a preferált allokációs módszert. Általános erőforrást adunk a csoporthoz helyőrzőként, hogy megőrizzük a csoportban megnevezett erőforrások könyvelésére szolgáló igénymintát. A követelményt a projekt naptárának megfelelően kell megtenni.
- **Adjon meg egy elnevezett erőforrást a csapatnak erőforrás-kapacitás felhasználása nélkül** - A **Foglalható erőforrás** mezőben válassza ki az erőforrást. Ezután válassza ki az időszakot, és válassza a **Nincs** lehetőséget allokációs módszerként. Az erőforrás hozzáadódik a csapathoz, de az erőforrás kapacitása nem merül fel a foglalás során.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Csapattag lefoglalása az általános erőforrás erőforrásigényének teljesítéséhez

A PSA-ban egy általános erőforrást lefoglalhat egy projektcsoportra, és meghatározhatja a szerepet, a szükséges kapacitást és a kapacitás elosztását. Az erőforrás-igénynél meghatározhatja az általános erőforráshoz társított attribútumokat. Ezek a tulajdonságok tartalmazzák a szükséges készségeket, az előnyben részesített szervezeti egységet és az előnyben részesített erőforrásokat.

Kövesse ezeket a lépéseket a fejlesztői általános erőforráshoz szükséges készségek meghatározásához.

1. A **Projektek** oldalon, a **Csapat** lapon válassza az **Új** lehetőséget egy általános forrás lefoglalásához.

    ![Általános erőforrás lefoglalva a csapatra.](media/Resource-Management-image9.png)

2. A **Minden csapattag** nézetben, az **Erőforrásigény** oszlopban válassza ki a hivatkozást a szükséges készségek hozzáadásához az általános erőforráshoz.

    ![Követelmény hivatkozás.](media/Resource-Management-image10.png)

3. A megjelenő **Erőforrásigény** oldalon a **Tudás** rácsban válassza ki a három pontot (**...**), majd válassza az **Új igényjellemző hozzáadása** lehetőséget a szükséges képességek fejlesztőhöz való hozzáadásához.

    ![Új igényjellemző parancs hozzáadása.](media/Resource-Management-image11.png)

4. A megjelenő **Gyors létrehozás: Követelményjellemző** párbeszédpanelen a **Jellemző** mezőben válassza ki a szükséges képességeket. Ezután az **Értékelés** mezőben válassza ki az adott készséghez szükséges jártassági szintet. Végül, az **Erőforrásigény** mezőben állítsa be az erőforrások forrásának követelményét a szervezeti egységektől, vagy akár a megnevezett erőforrásokat is. Ha kész, válassza a **Mentés** lehetőséget.

    ![Gyors létrehozás: Követelményjellemző párbeszédpanel.](media/Resource-Management-image12.png)

5. A **Forrásigény** oldalon válassza a **Foglalás** elemet az erőforrásigény teljesítéséhez.

    ![Foglalás gomb az erőforrásigény oldalon.](media/Resource-Management-image13.png)

    Kiválaszthatja az általános erőforrást a **Minden csapat tagja** rácsból, majd a **Foglalás** lehetőséget választhatja.

    ![A Minden csoport tagja rács felett található Foglalás gomb.](media/Resource-Management-image14.png)

    > [!NOTE]
    > Ebben a példában 40 szükséges óra van, de nincs ténylegesen lekötött óra, mivel az általános forrásoknak nincs foglalása. Ezenkívül nincsenek kijelölt órák, mivel az általános erőforrást közvetlenül a csapathoz adták hozzá. Nem a feladat-hozzárendeléssel adták hozzá.

    Az **Ütemezési asszisztens** oldalon a rendelkezésre álló erőforrásokat az erőforrásigényben megadott követelmények szerint szűrheti. Az erőforrásokat az Ütemezési táblán megadott rendezési paraméterek szerint rendezzük.

    ![Ütemezési asszisztens oldal.](media/Resource-Management-image15.png)

    Itt található néhány gyakran használt szűrő:

    - **Jellemzők és minősítés** - Szűrés készségek, igazolások és egyéb erőforrás-tulajdonságok alapján, a jártassági besoroláson felül.
    - **Szerepek** - Szűrés az alapértelmezett szerepek szerint, amelyek a foglalható forrásokhoz vannak rendelve.
    - **Szervezeti egységek** - Foglalható erőforrások szűrése szervezeti egységek szerint, amelyekhez hozzá vannak rendelve.

6. Ha nem elégedett a kezdeti keresési eredményekkel, megváltoztathatja a szűrési kritériumokat. Bontsa ki a bal oldalon a **Szűrő nézet** ablakot, majd válassza a **Keresés** lehetőséget további források kereséséhez.

    ![Nézet szűrése ablaktábla.](media/Resource-Management-image16.png)

7. Az eredmények rendezésének megváltoztatásához válassza a **Rendezés** lehetőséget.

    ![Rendezés parancs.](media/Resource-Management-image17.png)

8. Válassza ki az erőforrásokat a követelményben megadott igénynek megfelelően, a rács tetején feltüntetett módon. Törölheti a cellák kiválasztását a rácsban, és nyitva hagyhatja az erőforrás-kapacitást. Egyszerre csak egy erőforrás választható lefoglaltként.

9. Válassza a **Foglalás** lehetőséget a kiválasztott erőforrás lefoglalásához, és hagyja nyitva az Ütemezési táblát, hogy további erőforrásokat válasszon ki. Alternatív megoldásként válassza a **Foglalás és kilépés** lehetőséget a kiválasztott erőforrás lefoglalásához és az Ütemezési tábla bezárásához.

    ![Foglalni kívánt erőforrás.](media/Resource-Management-image19.png)

    Értesítést kap a lefoglalt órákról. Az igény mutatói megmutatják, hogy a foglalási követelmény mennyire teljesül, és mennyi marad. Láthatja azt is, hogy mekkora a kiválasztott erőforrás kapacitása. Válassza a **Kibontás** lehetőséget az erőforrás-foglalás részletesebb megjelenítéséhez.

9. Térjen vissza a **Minden csapattag** nézethez. A rácsban vegye észre, hogy az általános erőforrást felváltotta a megnevezett erőforrás, és a 40 órát az erőforrás lekötöttként sorolja fel.

    ![Frissített Összes csapattag rács.](media/Resource-Management-image20.png)

    > [!NOTE]
    > A hozzárendelt órák nem kerülnek megjelenítésre, mert közvetlenül a csapatra voltak foglalva. Nem feladat-hozzárendeléssel foglaltak őket.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Általános erőforrások rendelése a feladatokhoz és az erőforrás-követelmények generálása

A PSA-ban létrehozhat feladatokat, majd általános erőforrásokat rendelhet hozzájuk. Ily módon az erőforrásigényt helyőrzők képviselhetik, miközben becsülheti az ütemtervet és a pénzügyi számokat. Ezután generálhat erőforrásigényeket az általános erőforrásokhoz, és teljesítheti azokat.

1. A **Projektek** oldalon, az **Ütemezés** lapon válassza a **Hozzáadás** lehetőséget a feladat létrehozásához.

    ![Új feladat létrehozva.](media/Resource-Management-image21.png)

2. Az **Erőforrások** mezőben válassza az **Erőforrás-választó** szimbólumot. Megjelenik az Erőforrás-választó, amely megmutatja a projekt meglévő csapattagjait.

    ![Erőforrás-választó.](media/Resource-Management-image22.png)

3. Írja be az új általános erőforrás nevét, majd válassza a **Létrehozás** lehetőséget.

    ![A beírt új általános erőforrás neve.](media/Resource-Management-image23.png)

4. A megjelenő **Gyors létrehozás: Projektcsapattag** párbeszédpanelen a **Szerep** mezőben válassza ki az általános erőforrás szerepét. Az **Erőforrásegység** mezőben válassza ki az általános erőforrás szervezeti egységét. Azután válassza a **Mentés** parancsot.

    ![Gyors létrehozás: Projektcsoporttag párbeszédpanel.](media/Resource-Management-image24.png)

    Az általános csoporttagot most kiosztották a feladathoz.

    ![A feladathoz kijelölt általános csapattag.](media/Resource-Management-image25.png)

    A **Csapat** lapon láthatja az új általános csapattagot. Vegye észre, hogy csak órákat adott meg. Ezek az órák az összes feladat összegét adják, amelyeket az általános csapattagnak kiosztottak. Az általános csapattagnak még nincs szüksége órára vagy erőforrás-igényre.

    ![Általános csapattag a Csapat lapon.](media/Resource-Management-image26.png)

5. Most az Erőforrás-választó segítségével hozzárendelheti az általános csapattagot más feladatokhoz.

    ![Általános csapattag az Erőforrás-választóban.](media/Resource-Management-image27.png)

    Ha befejezte az általános erőforrás hozzárendelését a feladatokhoz, generálhat egy erőforrás-követelményt az általános erőforráshoz.

5. A **Csapat** lapon válassza ki az általános erőforrást, majd válassza a **Követelmény generálása** lehetőséget.

    ![Követelmény generálása parancs.](media/Resource-Management-image28.png)

    A követelmény előállításakor az általános csapattagnak rendelkeznie kell a szükséges órákkal és egy linkkel az erőforrás-igényhez.

    ![Erőforrás-igény hivatkozás.](media/Resource-Management-image29.png)

    Miután egy megnevezett erőforrást lekötött, az általános erőforrás eltávolításra kerül a csapatból, és helyébe a megnevezett erőforrás kerül.

    ![Az általános erőforrás helyébe a megnevezett erőforrás lép.](media/Resource-Management-image30.png)

    Az **Ütemezés** lapon az általános erőforrás-hozzárendelések eltávolításra kerülnek, és helyébe a megnevezett erőforrás lép.

    ![Általános erőforrás-hozzárendelések az Ütemezés lapon megnevezett erőforrásokkal helyettesítve.](media/Resource-Management-image31.png)

    > [!NOTE]
    > Ez a viselkedés csak akkor fordul elő, ha a megnevezett erőforrást teljes mértékben lefoglalják az általános erőforrás-igényre. Ha egy megnevezett erőforrás részben helyettesíti az általános erőforrás-igényt, vagy több megnevezett erőforrás helyettesíti az általános erőforrás-követelményt, akkor az általános erőforrás továbbra is hozzá van rendelve a feladathoz.

    A következő ábrán egy 80 órás feladatot terveztek ötnapos időtartamra (napi 16 óra öt nap alatt), és hozzárendelték a **Funkcionális** nevű általános erőforráshoz.

    ![Nyolcvan órás, ötnapos feladat a Funkcionális általános erőforráshoz rendelve.](media/Resource-Management-image32.png)

    Amikor előállítja a követelményt, akkor az 80 órára szól öt napon keresztül.

    ![80 órára, öt napra generált követelmény.](media/Resource-Management-image33.png)

    Mivel a rendelkezésre álló erőforrások napi nyolc órán keresztül működnek, két erőforrásra van szükség a követelmény teljesítéséhez.

    ![Második erőforrás.](media/Resource-Management-image35.png)

    A **Csapat** lapon most láthatja, hogy az általános erőforrásnak nincs kötelező órája, de a hozzárendelt órák továbbra is megjelennek a teljesítést alkotó két megnevezett erőforrással együtt.

    ![Két megnevezett erőforrás a Csapat lapon.](media/Resource-Management-image36.png)

    Az **Ütemezés** lapon az általános erőforrás továbbra is hozzá van rendelve a feladathoz.

    ![Általános erőforrások az Ütemezés lapon.](media/Resource-Management-image37.png)

A PSA nem rendeli hozzá mindkét erőforrást a feladathoz, mert ez a viselkedés kevésbé kiszámítható ütemezést eredményezne. Ebben az egyszerű példában könnyű elosztani az órákat két erőforrás között. Az összetettebb forgatókönyvekben, amelyek több feladatot és több erőforrást foglalnak magukban, a PSA-nak feltételezéseket kell tennie arra vonatkozóan, hogy hogyan kell elosztani a több erőforráshoz kapott foglalásokat több feladat között.

Ezért ezekben a forgatókönyvekben a projektmenedzser felel a többszörös foglalás elemzéséért és a szükséges hozzárendeléséért. A foglalások kiosztásához a projektmenedzser az általános erőforrásokból a megnevezett erőforrásokhoz rendeli a feladatokat, majd az **Összehangolás** nézetet használja annak ellenőrzésére, hogy az allokáció a foglalásokkal együtt működik-e.

### <a name="edit-a-resource-requirement"></a>Erőforrásigény szerkesztése

Az erőforrásigény létrehozása után a projektmenedzser vagy az erőforrás-kezelő módosíthatja a részleteket, hogy finomítsa a keresési feltételeket az Ütemezési tábla használatakor. Az erőforrásigény szerkesztéséhez kövesse ezeket a lépéseket.

1. A **Projektek** oldalon, a **Csapat** lapon válassza ki az általános erőforrás követelményeinek hivatkozását.
2. A megjelenő **Erőforrásigény** oldalon frissíthet több attribútumot. Íme néhány példa:

    - Név
    - Kezdő dátum
    - Befejezési dátum
    - Időtartam
    - Erőforrás típusa

Az **Erőforrásigény** oldalon a projektmenedzser vagy az erőforrás-kezelő a következő információkat is meghatározhatja:

- Képességek
- Szerepkörök
- Erőforrás-preferenciák
- Előnyben részesített szervezeti egység

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Frissítse az erőforrás-foglalásokat, miután azokat egy projektre lefoglalták

Miután hozzáadott egy általános vagy megnevezett erőforrást egy projektcsoporthoz, megváltoztathatja az erőforrás foglalásait.

1. A **Projektek** oldalon, a **Csapat** lapon válassza ki a csapattagot, majd válassza a **Foglalás fenntartása** lehetőséget.

    ![Ütemezési tábla nyitva a kiválasztott csapattag számára.](media/Resource-Management-image40.png)

    Megjelenik az Ütemezési tábla, amely megmutatja a projektcsoport tagjainak foglalásait. Bővítse a csapattag rekordját, hogy megnézhesse az órákat, amelyeket ez a projekt és más projektek foglaltak le, felhasználva a csapattag kapacitását.

2. Válassza ki és húzza el a foglalást annak meghosszabbításához vagy rövidítéséhez. Megjelenik egy **Erőforrás-foglalás létrehozása** párbeszédpanel, amely lehetővé teszi a foglalás módosítását.

    ![Erőforrás-foglalás létrehozása párbeszédpanel.](media/Resource-Management-image41.png)

3. Kattintson a jobb gombbal a foglalásra. Ezután a helyi menü segítségével elvégezheti a következő műveleteket:

    - A foglalás állapotának módosítása.
    - A foglalás szerkesztése.
    - Egy erőforrás helyettesítése a projektcsoportban.

### <a name="change-the-booking-status"></a>A foglalás állapotának módosítása

Az alapértelmezett vagy az egyéni foglalás állapotának módosítása.

![Állapot módosítása parancs.](media/Resource-Management-image42.png)

A PSA a következő állapotokat tartalmazza:

- **Törölve** - Ez az állapot visszavonja egy erőforrás foglalását, és felszabadítja az erőforrás kapacitását.
- **Nehéz foglalás** - Ez az állapot felhasználja az erőforrás kapacitását. A foglalás jellemzően akkor veszi fel ezt az állapotot, amikor megnyitja a **Foglalás fenntartása** panelt a **Minden csapattag** rácsból a **Projektek** oldalon.
- **Puha foglalás** - Ez az állapot hozzáad egy erőforrást a csapathoz, de nem használja fel az erőforrás kapacitását. Ez azt jelzi, hogy az erőforrást fenntartották a lehetséges munkavégzéshez, de még mindig rendelkezik kapacitással, ha más munkákhoz szükséges. Az általános erőforrás-rendelkezésre állás szempontjából a puha foglalások eltérő státusszal rendelkeznek, mint a kemény foglalások.
- **Javasolt** - Ez az állapot egy erőforrás-menedzser vagy projektmenedzser erőforrásra tett javaslatát reprezentálja. A javaslatok nem használják fel egy erőforrás kapacitását, és az erőforrás nem kerül hozzáadásra a projekt csapatához. Annak érdekében, hogy az erőforrást a csapatba foglalhassák, a projektmenedzsernek el kell fogadnia a javaslatot.

### <a name="submit-resource-requests"></a>Erőforrás-kérelmek elküldése

Az erőforrás-kérelmek a kereslet (erőforrás-igény) teljesítésére szolgálnak, amelyet az erőforrás-kezelőnek teljesítenie kell. Ha egy általános erőforrás már létezik a csapatban, akkor közvetlenül küldhet erőforrás-kérelmet. Az erőforrás-igényt kétféle módon lehet teljesíteni:

- Az erőforrás-kezelő közvetlenül teljesíti a kérést. Ebben az esetben az általános erőforrást egy kemény foglalás váltja fel, amelynek megnevezett erőforrása van.
- Az erőforrás-kezelő erőforrást javasol a projektmenedzser számára, a projektvezető pedig jóváhagyja vagy elutasítja a javasolt erőforrást.

#### <a name="direct-fulfillment-of-resource-requests"></a>Az erőforrás-kérelmek közvetlen teljesítése

Amikor egy erőforrásigény keletkezik, a projekt vezetője benyújthat egy erőforrásigényt egy általános erőforrásra az erőforrás kiválasztásával, majd az **Igény benyújtása** ponttal.

![Igény benyújtása gomb.](media/Resource-Management-image45.png)

Az erőforrással kapcsolatos megjegyzéseket meg lehet adni az erőforrás-kezelőnek, aki teljesíti a kérést. Az igény benyújtása után a csapattag **Állapot** mezője **Beküldve** lesz.

![Opcionális megjegyzések beírása.](media/Resource-Management-image46.png)

Amikor az erőforrás-kezelő teljesíti a kérést, az általános csapattagot a **Minden csapattag** rácsban a megnevezett erőforrás váltja fel.

![Az általános csapattagot a Minden csapattag rácsban a megnevezett erőforrás váltja fel.](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Erőforrás-javaslat használata erőforrás-kérelmekhez

Ahelyett, hogy egy erőforrást közvetlenül egy erőforráskérésre foglalna, az erőforrás-kezelő erőforrást javasolhat a projektmenedzser számára. Az erőforrás-kezelő akkor használhatja ezt a lehetőséget, ha a követelményekhez nem áll rendelkezésre pontos egyezés. Amikor egy erőforrás-kezelő erőforrást javasol, a projektmenedzser látja, hogy az általános csapattag **Állapot** mezője **Áttekintés szükséges** lesz.

![Az általános csapattag állapota Áttekintés szükségesre váltva.](media/Resource-Management-image48.png)

A javasolt erőforrás megtekintéséhez és a javaslat foglalásának hatásának megjelenítéséhez kattintson duplán arra a csapattagra, amelynek **Áttekintés szükséges** státusza van. Ezután válassza a **Javasolt erőforrások** fület.

![Javasolt erőforrások fül.](media/Resource-Management-image49.png)

Válassza **Az összes javaslat elfogadása** elemet az összes javasolt erőforrás elfogadásához, vagy az **Összes javaslat elutasítása** opciót az elutasításhoz. Ha elfogadja a javasolt erőforrásokat, akkor ezeket a projektre csapattagokként foglalják, és felváltják az általános erőforrásokat.

> [!NOTE]
> Valamennyi elfogadott erőforrást el kell fogadnia vagy el kell utasítania. Részben nem fogadhatja el vagy utasíthatja el őket.

### <a name="substitute-a-resource-on-the-project-team"></a>Egy erőforrás felváltása a projektcsapatban

Időnként a projektmenedzsernek helyettesítenie kell egy lefoglalt csapattagot egy projektnél.

1. A **Projektek** lapon, a **Csapat** fülön válassza ki a helyettesítő erőforrást, majd válassza a **Foglalások fenntartása** lehetőséget.
2. Bontsa ki az erőforrást a hozzárendelt projektek megtekintéséhez.

    ![Az erőforrás kibontva a hozzárendelt projektek megjelenítéséhez.](media/Resource-Management-image50.png)

3. Kattintson a jobb gombbal a projektre, majd válassza a **Helyettesítő erőforrás** lehetőséget.
4. Ha ismeri az erőforrást, amelyet helyettesíteni szeretne az aktuális erőforrással, jelölje ki vagy írja be a nevet, majd válassza az **Újbóli hozzárendelés** lehetőséget.

    ![Helyettesítő erőforrás meghatározása.](media/Resource-Management-image51.png)

    Alternatív megoldásként, kövesse az alábbi lépéseket egy erőforrás kereséséhez:

    1. Válassza a **Helyettesítő keresése** lehetőséget.

        ![Helyettesítő erőforrás keresése.](media/Resource-Management-image52.png)

        Az Ütemezési segéd visszaadja az elérhető helyettesítők listáját. Az Ütemezési segédben tovább szűrheti a rendelkezésre álló erőforrásokat a megfelelő helyettesítő megtalálásához.

        ![A rendelkezésre álló helyettesítők listája.](media/Resource-Management-image53.png)

    2. Az erőforrás helyettesítéséhez válassza ki a kívánt erőforrást, majd válassza a **Helyettesítő** lehetőséget.

        ![Kiválasztott helyettesítő erőforrás.](media/Resource-Management-image54.png)

    A foglalásokat és a feladatokat az új erőforrás váltja fel.

    ![A foglalásokat és a feladatokat az új erőforrás váltja fel.](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>A csapattagok foglalásainak és feladatainak egyeztetése

A csapat tagjai számára a foglalások és a megbízások lazán kapcsolódnak egymáshoz. Más szavakkal: az erőforrásoknak lehetnek hozzárendelései, de foglalásai nem, vagy lehetnek foglalásaik, de nem lehet hozzárendeléseik. Ideális esetben a foglalásokat és a feladatokat össze kell hangolni, hogy az erőforrások képesek legyenek a feladat-hozzárendelések végrehajtására. Előfordulhat azonban, hogy a foglalások rendelkezésre álláson alapulnak, és a projekt folytatásakor a feladatok ütemezése változhat. Ezért a foglalások és feladatok laza csatolása rugalmasságot biztosít.

A PSA rendelkezik egy **Egyeztetés** lappal, amely lehetővé teszi a projektmenedzserek számára, hogy összehangolják a csapattagok foglalásait és a projektcsoportokhoz rendelt megbízásaikat.

![Egyeztetés fül.](media/Resource-Management-image56.png)

Az **Egyeztetés** lap a foglalásokat és a hozzárendeléseket az egyes csoporttagok egyedi feladat-hozzárendelésének szintjéig mutatja. A cellákban órákat jelenít meg, amelyek hónapoktól napokig terjedő időszakokat jelent.

A fül a projekt teljes nettó összértékét, valamint az Összesen oszlopot is mutatja.

Az egyes erőforrások esetében a fül kiszámítja a különbséget a csapattag foglalása és a csoporttag feladatainak összeállítása között. Ideális esetben ennek a különbségnek 0-nak (nulla) kell lennie. Más szavakkal, nem lehet különbség a foglalások és a megbízások között. A különbségek színesek és árnyaltak, hogy felhívják a figyelmet két körülményre:

- **Foglalási hiány** - Foglalási hiány akkor fordul elő, ha az erőforrás több hozzárendeléssel rendelkezik, mint a foglalások. Mivel ez a kapacitás nem volt fenntartva, a projektmenedzser javíthatja ezt a feltételt azáltal, hogy az erőforrás foglalásait kiterjeszti a hiány fedezésére.
- **Többletfoglalások** - Többletfoglalások akkor fordulnak elő, amikor egy erőforrást lefoglaltak a projekthez, de nem rendeltek hozzá feladatokhoz. Ez a feltétel elfogadható lehet azokban az esetekben, amikor az erőforrást a projekthez a feladat-hozzárendelés megtörténte előtt lefoglalták. Más esetekben azonban az erőforrást nem tervezik feladatokhoz rendelni. Ezekben az esetekben a projektmenedzsernek fontolóra kell vennie az erőforrás foglalásainak visszavonását, hogy a kapacitás felhasználható legyen egy másik projekthez.

Bizonyos esetekben, ha az időt a napi szintnél magasabb szinten nézi (például a hónap szintjén), akkor az erőforrás nettó különbsége nulla lehet (más szóval, foglalások = megbízások). Ha azonban az időt heti szinten tekinti, akkor láthatja, hogy az első héten nulla órás megbízások és 40 órás foglalások vannak, a második héten pedig 40 órás megbízások és nulla órás foglalások vannak. Összességében a foglalások és a feladatok összeegyeztethetők, de hetente különböznek.

Ha az időt magasabb szinteken tekinti meg, akkor az **Egyeztetés** lapon lévő cellák jelzik, hogy az alacsonyabb szinteken eltérések vannak. Ha egy cellába duplán kattint, nagyíthat, hogy megnézze a különbséget. Ezután jobb egérgombbal kattinthat a kicsinyítéshez. Ha kiválaszt egy erőforrást, majd használja a rács eszköztár **Következő különbség** vezérlőjét, a következő különbséghez ugorhat az adott erőforrás foglalása és hozzárendelése között. Ezután az **Előző különbség** vezérlővel visszatérhet. A különbségjelzőt és a navigációs viselkedést a **Beállítások** alatt is kikapcsolhatja.

![Különbségmutató.](media/Resource-Management-image57.png)

Ha az erőforráshoz feladatok vannak hozzárendelve, de nincs foglalása, akkor a **Projektek** oldalon, az **Egyeztetés** lapon válassza ki a foglalási hiányt, majd válassza a **Foglalás kiterjesztése** lehetőséget. Megjelenik a **Foglalás kiterjesztése** párbeszédpanel, amely megmutatja az erőforrás hiányának kezeléséhez szükséges foglalást. Ezenkívül megmutatja az erőforrás meglévő foglalásait az összes projektben vagy más ütemezhető entitásban. Ha az **OK** lehetőséget választja az erőforrás foglalásának elkészítéséhez, az erőforrás elérhetőségétől függetlenül túlfoglalást okozhat.

![A Foglalás kiterjesztése párbeszédpanel.](media/Resource-Management-image58.png)

A projektmenedzser vagy az erőforrás-kezelő ezután felhasználhatja az Ütemezési táblát olyan helyzetek kezelésére, amikor egy erőforrás túlfoglalása meghaladja a kapacitást.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
