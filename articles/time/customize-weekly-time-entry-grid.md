---
title: Időbejegyzések kiterjesztése
description: Ez a cikk információt nyújt arról, hogy a fejlesztők hogyan tudják kiterjeszteni az időbejegyzés-vezérlőt.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 7ed501af3fb2059ab3c3ab6f6c957fe518595d55
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914773"
---
# <a name="extending-time-entries"></a>Időbejegyzések kiterjesztése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations bővíthető egyéni időbevitel-vezérlőt tartalmaz. Ez a vezérlő többek között a következő funkciókat tartalmazza:

- Az idő vízszintes beírása egy hétre
- Összesítések nap, sor vagy hét szerint
- Sorok vagy hetek másolása
- Időbevitel a ÓÓ:pp vagy ÓÓ.óó formátumban (automatikusan ÓÓ.óó formátumra alakítva)
- Importálás hozzárendelésekből, foglalásokból vagy találkozókból

Az időbejegyzések kiterjesztése két területen lehetséges:
- [Egyéni időbejegyzések hozzáadása saját használatra](#add)
- [A heti időbejegyzési vezérlő testreszabása](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Egyéni időbejegyzések hozzáadása saját használatra

Az időbejegyzések több forgatókönyvben használt alapentitások. A 2020. áprilisi 1. hullámban, a TESA alapmegoldást bevezették. A TESA egy **Beállítások** entitást és egy új **Időbejegyzést kezelő felhasználó** biztonsági szerepkört biztosít. Az új mezők, a **msdyn_start** és a **msdyn_end**, amelyek közvetlen kapcsolatban állnak a **msdyn_duration** mezővel, szintén szerepelnek a rendszerben. Az új entitás, a biztonsági szerepkör és a mezők több termékre vonatkozóan egységesebb megközelítést biztosítanak az idővel kapcsolatban.


### <a name="time-source-entity"></a>Időforrás-entitás
| Mező | Adatfolyam leírása | 
|-------|------------|
| Adatfolyam neve  | Az időbejegyzés létrehozásakor a kijelölési értékként használt időforrás-bejegyzés neve. |
| Alapértelmezett időforrás [Időforrás: isdefault] | Alapértelmezés szerint csak egy időforrás lehet megjelölve az alapértelmezettként. Ez lehetővé teszi, hogy a bejegyzések mindegyike egy alapértelmezett időforrást használjon, ha nincs ilyen megadva. |
|Időforrás típusa [Időforrás: sourcetype] | A forrástípus egy beállítás (Időbejegyzés forrástípusa), amely lehetővé teszi az időforrás alkalmazáshoz való társítását. A Microsoft 190 000 000-nél nagyobb értékeket fenntartja.|


### <a name="time-entries-and-the-time-source-entity"></a>Időbejegyzések és az Időforrás-entitás
Minden időbejegyzés egy időforrásrekordhoz van társítva. Ez a rekord határozza meg, mely alkalmazások és miként dolgozzák fel az időbejegyzést.

Az időbejegyzések mindig folytonos időegységek, amelyek kezdése, befejezése és időtartama egymáshoz kapcsolódnak.

A logika a következő helyzetekben automatikusan frissíti az időbejegyzési rekordot:

- Ha a három következő mező közül kettő van megadva, akkor a program automatikusan kiszámítja a harmadikat: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- A **msdyn_start** és **msdyn_end** mezők figyelembe veszik az időzónákat.
- Az időbejegyzések csak az **msdyn_date** és **msdyn_duration** meghatározása esetén éjfélkor indulnak el. A **msdyn_start** és **msdyn_end** mezők ennek megfelelően frissülnek.

#### <a name="time-entry-types"></a>Időbejegyzés típusai

Az időbejegyzés rekordjaihoz társított típus tartozik, amely a társított alkalmazás beküldési folyamatában a viselkedést határozza meg.

|Felirat | Érték|
|-----|-----|
|Szünetel   |192,355,000|
|Utazás | 192,355,001|
|Túlóra   | 192,354,320|
|Munka   | 192,350,000|
|Hiányzás    | 192,350,001.|
|Szabadnap   | 192,350,002.|


## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>A heti időbejegyzési vezérlő testreszabása
A fejlesztők további mezőket és kereséseket vehetnek fel más entitásokhoz, valamint egyéni üzleti szabályokat valósíthatnak meg az üzleti forgatókönyvek támogatására.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Egyéni mezők hozzáadása, amelyek kereséssel rendelkeznek más entitásokhoz
Három fő lépés van az egyéni mező hozzáadásához a heti időbeviteli rácshoz.

1. Adja hozzá az egyéni mezőt a **Gyorslétrehozás** párbeszédpanelhez.
2. Konfigurálja a rácsot az egyéni mező megjelenítéséhez.
3. Adja hozzá az egyéni mezőt a **Sorszerkesztés** vagy **Időbejegyzés szerkesztése** oldalhoz igény szerint.

Azt is ellenőrizze, hogy az új mező rendelkezik-e a szükséges érvényesítésekkel a **Sorszerkesztés** vagy **Időbejegyzés-szerkesztés** oldalon. Ennek a feladatnak a részeként zárolja a mezőt az időbejegyzés állapota alapján.

Ha egyéni mezőt ad az **Időbejegyzés** rácshoz, majd közvetlenül a rácsban hoz létre időbejegyzéseket, akkor a bejegyzések egyéni mezője automatikusan úgy van beállítva, hogy az egyezzen a sorral. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Adja hozzá az egyéni mezőt a Gyors létrehozás párbeszédpanelhez
Az egyéni mezőt adja hozzá az **Gyorslétrehozás: Időbejegyzés** párbeszédpanelhez. A felhasználók ezután beírhatnak egy értéket, amikor az **Új** lehetőséget választva adnak hozzá időbejegyzéseket.

### <a name="configure-the-grid-to-show-the-custom-field"></a>A rács konfigurálása az egyéni mező megjelenítéséhez
Kétféle módon adhat hozzá egyéni mezőt a **Heti időbevitel** rácshoz.

- Lehetősége van a **Saját heti időbejegyzések** nézet testreszabására, és az egyedi mező hozzáadására. Meghatározhatja az egyéni mező helyét és méretét a rácson, a nézetben szereplő tulajdonságok szerkesztésével.
- Hozzon létre egy új, egyéni időbeviteli nézetet és alapértelmezett nézetként állítása be. Ennek a nézetnek tartalmaznia kell a **Leírás** és **Külső megjegyzések** mezőket, azon oszlopok mellett, amelyeket a rácson szeretne elhelyezni. A rács pozícióját, méretét és alapértelmezett rendezési sorrendjét úgy határozhatja meg, hogy szerkeszti ezeket a tulajdonságokat a nézetben. Ezután állítsa be a nézet egyedi vezérlőjét úgy, hogy az egy **Időbeviteli rács** vezérlő legyen. Adja hozzá ezt a vezérlőt a nézethez, és válassza ki a **Web**, **Telefon** és **Tablet** formátumokhoz. Ezután konfigurálja a **Heti időbeviteli rács** paramétereit. Állítsa a **Kezdő dátum** mezőt **msdyn\_date** értékre, állítsa az **Időtartam** mezőt **msdyn\_duration** értékre, és állítsa az **Állapot** mezőt **msdyn\_entrystatus** értékre. A **Csak olvasható állapotlistamező** beállítása **192350002 (jóváhagyott)**, **192350003 (beküldve)** vagy **192350004 (visszahívás igénylése)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Egyéni mező hozzáadása a megfelelő szerkesztési oldalhoz
Az időbejegyzések vagy időbejegyzés-sorok szerkesztéséhez használt lapok az **Űrlapok** alatt találhatók . A rács **Bejegyzés szerkesztés** bejegyzése gombja megnyitja a **Bejegyzés szerkesztése** oldalt, a **Sor szerkesztése** gomb pedig a **Sorszerkesztés** oldalt. Ezeket az oldalakat szerkesztheti úgy, hogy egyéni mezőket tartalmazzanak.

Mindkét lehetőség eltávolítja a **Projekt** és a **Projektfeladat** entitásokból a kész szűréseket, így az entitások összes keresési nézete látható lesz. Azonnal csak a vonatkozó keresési nézetek láthatók.

Meg kell határoznia a megfelelő oldalt az egyéni mezőhöz. Valószínűleg, ha hozzáadta a mezőt a rácshoz, akkor azon a **Sorszerkesztés** oldalon kell lennie, amelyet azokhoz a mezőkhöz használnak, amelyek az összes időbejegyzésre vonatkoznak. Ha az egyéni mezőnek minden napra egyedi értéke van a sorban (például ez egy egyéni mező a befejezési időhöz), akkor az **Időbejegyzés szerkesztése** oldalra lépjen.

Az egyéni mező az oldalhoz való hozzáadásához húzza a **Mező** elemet az oldal megfelelő pozíciójába, majd állítsa be annak tulajdonságait.

### <a name="add-new-option-set-values"></a>Új beállítási értékek hozzáadása
Ahhoz, hogy egyéni értékkészlet-értékeket adjon hozzá egy gyári mezőhöz, kövesse az alábbi lépéseket.

1. Nyissa meg a mező szerkesztési oldalát, majd a **Típus** alatt válassza a beállítás mellett a **Szerkesztés** lehetőséget.
2. Adjon hozzá egy új opciót, amelynek egyedi címkéje és színe van. Ha új időbeviteli státust szeretne hozzáadni, akkor a kész mező neve **Beviteli állapot**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Új időbeviteli állapot kijelölése csak olvashatóként
Ha egy új időbeviteli állapotot csak olvashatónak szeretne megadni, akkor adja hozzá az új időbeviteli értéket a **Csak olvasható állapotlista** tulajdonsághoz. Ügyeljen arra, hogy a számot adja hozzá, nem a címkét. Az időbeviteli rács szerkeszthető része az új állapotú sorok számára immár zárolva lesz. Ha eltérő módon szeretne konfigurálni a **Csak olvasható állapotlista** tulajdonságot a különböző **Időbejegyzés** nézetekhez, vegye fel az **Időbejegyzés** rácsot a nézet **Egyéni vezérlők** területére, és szükség szerint állítsa be a paramétereket.

Ezután adjon hozzá üzleti szabályokat az összes mező lezárásához az **Sor szerkesztése** és az **Időbejegyzés szerkesztése** oldalakon. Az oldalak üzleti szabályaihoz úgy férhet hozzá, hogy megnyitja az oldal folyamatszerkesztőjét, majd kiválasztja az **Üzleti szabályok** lehetőséget. Az állapotot hozzáadhatja a feltételhez a meglévő üzleti szabályokban, vagy hozzáadhat egy új üzleti szabályt az új állapothoz.

### <a name="add-custom-validation-rules"></a>Egyéni ellenőrzési szabályok hozzáadása
Kétféle típusú ellenőrzési szabályt adhat hozzá a **Heti időbevitel** rács felhasználói élményéhez:

- Az oldalakon működő ügyféloldali üzleti szabályok
- Kiszolgálóoldali beépülőmodul-érvényesítések, amelyek minden időbejegyzés-frissítésre érvényesek

#### <a name="client-side-business-rules"></a>Ügyféloldali üzleti szabályok
Az üzleti szabályok segítségével zárolhatja és feloldhatja a mezőket, mezőkbe írhat be alapértelmezett értékeket, és meghatározhatja azokat az érvényesítéseket, amelyek csak az aktuális időbeviteli rekordból tartalmaznak információt. Az oldal üzleti szabályaihoz úgy férhet hozzá, hogy megnyitja az egyes oldalak folyamatszerkesztőjét, majd kiválasztja az **Üzleti szabályok** lehetőséget. Ezután szerkesztheti a meglévő üzleti szabályokat, vagy hozzáadhat új üzleti szabályokat.

#### <a name="server-side-plug-in-validations"></a>Kiszolgálóoldali beépülőmodul-ellenőrzések
A beépülő modul érvényesítéseket használhatja minden olyan érvényesítéshez, amely több kontextust igényel, mint amely egyetlen időbejegyzés-rekordban elérhető. Ezeket a rácson belül, beágyazott frissítéseken futtatni kívánt ellenőrzésekhez is használhatja. Az ellenőrzések befejezéséhez hozzon létre egy egyedi beépülő modult az **Időbejegyzés** entitáson.

### <a name="limits"></a>Korlátozások
Jelenleg az **Időbeviteli** rács mérethatára 500 sor. Ha 500-nál több sor van, akkor a további sorok nem fognak megjelenni. Ezt a méretkorlátot nem lehet növelni.

### <a name="copying-time-entries"></a>Időbejegyzések másolása
Az **Időbejegyzés másolásához használt oszlopok** nézet használatával adja meg a másolandó mezők listáját az időbejegyzés során. A **Dátum** és az **Időtartam** kötelező mezők, és nem lehet ezeket eltávolítani a nézetből.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
