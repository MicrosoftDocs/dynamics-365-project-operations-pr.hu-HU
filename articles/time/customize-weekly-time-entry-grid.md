---
title: Időbejegyzések kiterjesztése
description: Ez a témakör információt nyújt arról, hogy a fejlesztők hogyan tudják kiterjeszteni az időbejegyzés-vezérlőt.
author: stsporen
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: f446e24f3a61914a46a552fdc38b986d8b924747
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277161"
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

1. Adja hozzá az egyéni mezőt a gyors létrehozás párbeszédpanelhez.
2. Konfigurálja a rácsot az egyéni mező megjelenítéséhez.
3. Adja hozzá az egyéni mezőt a sorszerkesztési feladatfolyamathoz vagy a cellaszerkesztési feladatfolyamathoz.

Azt is ellenőrizze, hogy az új mező rendelkezik-e a szükséges érvényesítésekkel a sorban vagy a cellában lévő szerkesztési feladat folyamatában. E lépés részeként zárolja a mezőt az időbeviteli állapot alapján.

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Egyéni mező hozzáadása a gyors létrehozás párbeszédpanelhez
Az egyéni mezőt adja hozzá az **Időbejegyzés gyors létrehozása** párbeszédpanelhez, Majd az időbejegyzések hozzáadásakor egy érték adható meg az **Új** lehetőség kiválasztásával.

### <a name="configure-the-grid-to-show-the-custom-field"></a>A rács konfigurálása az egyéni mező megjelenítéséhez
Kétféle módon adhat hozzá egyéni mezőt a heti időbeviteli rácshoz:

  - Nézet testreszabása és egyéni mező hozzáadása
  - Alapértelmezett egyéni időbejegyzés létrehozása 


#### <a name="customize-a-view-and-add-a-custom-field"></a>Nézet testreszabása és egyéni mező hozzáadása

Lehetősége van a **Saját heti időbejegyzések** időbejegyzések nézet testreszabására és az egyedi mező hozzáadására. Kiválaszthatja az egyéni mező helyét és méretét a rácson, a nézetben szereplő tulajdonságok szerkesztésével.

#### <a name="create-a-new-default-custom-time-entry"></a>Alapértelmezett egyéni időbejegyzés létrehozása

Ennek a nézetnek tartalmaznia kell a **Leírás** és **Külső megjegyzések** mezőket, azon oszlopok mellett, amelyeket a rácson szeretne elhelyezni. 

1. A rács pozícióját, méretét és alapértelmezett rendezési sorrendjét úgy válassza meg, hogy szerkeszti ezeket a tulajdonságokat a nézetben. 
2. Állítsa be a nézet egyedi vezérlőjét úgy, hogy az egy **Időbeviteli rács** vezérlő legyen. 
3. Adja hozzá ezt a vezérlőt a nézethez, és válassza ki az internethez, a telefonhoz és a táblagéphez. 
4. Konfigurálja a heti időbeviteli rács paramétereit. 
5. Állítsa a **Kezdő dátum** mezőt **msdyn_date** értékre, állítsa az **Időtartam** mezőt **msdyn_duration** értékre, és állítsa az **Állapot** mezőt **msdyn_entrystatus** értékre. 
6. Az alapértelmezett nézet esetében a **Csak olvasható állapotlista** mező értéke **192350002,192350003,192350004**. A **Sorok szerkesztése munkafolyamat** mező beállítása **msdyn_timeentryrowedit**. A **Műveletsor cellájának szerkesztése** mező beállítása **msdyn_timeentryedit**. 
7. Testreszabhatja ezeket a mezőket az írásvédett állapot hozzáadásához vagy eltávolításához, vagy egy sor feladat alapú élmény (TBX) használatához a sor vagy cella szerkesztéséhez. Ezek a mezők immár statikus értékhez vannak kötve.


> [!NOTE] 
> Mindkét lehetőség eltávolítja a **Projekt** és a **Projektfeladat** entitásokból a kész szűréseket, így az entitások összes keresési nézete látható lesz. Azonnal csak a vonatkozó keresési nézetek láthatók.

Határozza meg a megfelelő feladatáramlást az egyéni mezőhöz. Ha hozzáadta a mezőt a rácshoz, akkor annak a sornak a szerkesztési feladatfolyamatában kell lennie, amelyet azokhoz a mezőkhöz használnak, amelyek az összes időbejegyzésre vonatkoznak. Ha az egyéni mezőnek minden nap egyedi értéke van, például egy egyedi mező a **Befejezési idő** számára, akkor a cellaszerkesztési feladatfolyamatba kell kerülnie.

Az egyéni mező feladatfolyamathoz való hozzáadásához húzza a **Mező** elemet az oldal megfelelő pozíciójába, majd állítsa be a mező tulajdonságait. Állítsa a **Forrás** tulajdonságot **Időbevitel** értékre, és állítsa az **Adatmező** tulajdonságot az egyedi mezőre. A **Mező** tulajdonság a megjelenített nevet adja meg a TBX oldalon. Válassza az **Alkalmaz** lehetőséget a mező módosításainak mentéséhez, majd válassza a **Frissítés** lehetőséget, hogy mentse a változtatásokat az oldalra.

Ha új, egyedi TBX oldalt szeretne használni, hozzon létre egy új eljárást. Állítsa a kategóriát **Üzleti folyamat** értékre, állítsa az entitást **Időbevitel** értékre, és állítsa az üzleti folyamat típusát **Folyamat futtatása feladatfolyamatként** értékre. A **Tulajdonságok** alatt az **Oldal neve** tulajdonságot az oldal megjelenített nevére kell beállítani. Adja hozzá az összes vonatkozó mezőt a TBX oldalhoz. Mentse és aktiválja a folyamatot. Frissítse az adott feladatáramlás egyedi vezérlő tulajdonságát a folyamat **Név** értékére.

### <a name="add-new-option-set-values"></a>Új beállítási értékek hozzáadása
Az opcionálisan beállított értékek kész mezőhöz történő hozzáadásához nyissa meg a mező szerkesztési oldalát, és a **Típus** alatt válassza a beállítás mellett a **Szerkesztés** lehetőséget. Adjon hozzá egy új opciót, amelynek egyedi címkéje és színe van. Ha új időbeviteli státust szeretne hozzáadni, akkor a kész mező neve **Beviteli állapot**, nem **Állapot**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Új időbeviteli állapot kijelölése csak olvashatóként
Ha egy új időbeviteli állapotot csak olvashatónak szeretne megadni, akkor adja hozzá az új időbeviteli értéket a **Csak olvasható állapotlista** tulajdonsághoz. Az időbeviteli rács szerkeszthető része az új állapotú sorok számára zárolva lesz.
Ezután adjon hozzá üzleti szabályokat az összes mező lezárásához az **Időbejegyzés sor szerkesztése** és az **Időbejegyzés szerkesztése** TBX oldalakon. Az oldalak üzleti szabályaihoz úgy férhet hozzá, hogy megnyitja az oldal üzletifolyamat-szerkesztőjét, majd kiválasztja az **Üzleti szabályok** lehetőséget. Az állapotot hozzáadhatja a feltételhez a meglévő üzleti szabályokban, vagy hozzáadhat egy új üzleti szabályt az új állapothoz.

### <a name="add-custom-validation-rules"></a>Egyéni ellenőrzési szabályok hozzáadása
Kétféle típusú ellenőrzési szabály adható hozzá a heti időbeviteli rács felhasználói élményéhez:

- Ügyféloldali üzleti szabályok, amelyek a gyorslétrehozási párbeszédpaneleken és a TBX-oldalakon működnek.
- Kiszolgálóoldali beépülőmodul-érvényesítések, amelyek minden időbejegyzés-frissítésre érvényesek.

#### <a name="business-rules"></a>Üzleti szabályok
Az üzleti szabályok segítségével zárolhatja és feloldhatja a mezőket, mezőkbe írhat be alapértelmezett értékeket, és meghatározhatja azokat az érvényesítéseket, amelyek csak az aktuális időbeviteli rekordból tartalmaznak információt. A TBX-oldal üzleti szabályaihoz úgy férhet hozzá, hogy megnyitja az oldal üzletifolyamat-szerkesztőjét, majd kiválasztja az **Üzleti szabályok** lehetőséget. Ezután szerkesztheti a meglévő üzleti szabályokat, vagy hozzáadhat új üzleti szabályokat. A még testreszabottabb ellenőrzésekhez használhat egy üzleti szabályt JavaScript futtatásához.

#### <a name="plug-in-validations"></a>Beépülő modul érvényesítések
A beépülő modul érvényesítéseket használhatja minden olyan érvényesítéshez, amely több kontextust igényel, mint amely egyetlen időbejegyzés-rekordban elérhető, vagy olyan ellenőrzésekhez, amelyeket a rácson belüli inline frissítésekkel kíván futtatni. Az érvényesítés befejezéséhez hozzon létre egy egyedi beépülő modult az **Időbejegyzés** entitáson.

### <a name="copying-time-entries"></a>Időbejegyzések másolása
Az **Időbejegyzés másolásához használt oszlopok** nézet használatával adja meg a másolandó mezők listáját az időbejegyzés során. A **Dátum** és az **Időtartam** kötelező mezők, és nem lehet ezeket eltávolítani a nézetből.


[!INCLUDE[footer-include](../includes/footer-banner.md)]