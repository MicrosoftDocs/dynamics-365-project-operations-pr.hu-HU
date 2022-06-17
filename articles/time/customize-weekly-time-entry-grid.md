---
title: Időbejegyzések kiterjesztése
description: Ez a cikk arról nyújt tájékoztatást, hogy a fejlesztők hogyan tudják meghosszabbítani az időbeviteli vezérlőket.
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
Minden időbejegyzés egy időforrásrekordhoz van társítva. Ez a rekord határozza meg, hogy mely alkalmazásoknak és hogyan kell feldolgozniuk az időbevitelt.

Az időbejegyzések mindig folytonos időegységek, amelyek kezdése, befejezése és időtartama egymáshoz kapcsolódnak.

A logika a következő helyzetekben automatikusan frissíti az időbejegyzési rekordot:

- Ha a három következő mező közül kettő van megadva, akkor a program automatikusan kiszámítja a harmadikat: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- A **msdyn_start** és **msdyn_end** mezők időzónával vannak tisztában.
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
3. Adja hozzá az egyéni mezőt a Sorszerkesztés **vagy** az **Időbevitel szerkesztési** oldalához, ha szükséges.

Győződjön meg arról, hogy az új mező rendelkezik a szükséges ellenőrzésekkel a Sorszerkesztés **vagy** az **Időbevitel szerkesztése** lapon. A feladat részeként zárolja a mezőt az időbevitel állapota alapján.

Amikor hozzáad egy egyéni mezőt az **Időbevitel** rácshoz, majd közvetlenül a rácsban hoz létre időbejegyzéseket, a bejegyzések egyéni mezője automatikusan úgy lesz beállítva, hogy az megfeleljen a sornak. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Az egyéni mező hozzáadása a Gyorslétrehozás párbeszédpanelhez
Adja hozzá az egyéni mezőt a **Gyorslétrehozás: Időbevitel** létrehozása párbeszédpanelhez. A felhasználók ezután beírhatnak egy értéket, amikor az **Új** lehetőséget választva adnak hozzá időbejegyzéseket.

### <a name="configure-the-grid-to-show-the-custom-field"></a>A rács konfigurálása az egyéni mező megjelenítéséhez
Kétféleképpen adhat hozzá egyéni mezőt a **Heti időbeviteli** rácshoz.

- Szabja testre a **Saját Heti időbejegyzések nézetet**, és adja hozzá az egyéni mezőt. Megadhatja az egyéni mező pozícióját és méretét a rácsban a nézet tulajdonságainak szerkesztésével.
- Hozzon létre egy új egyéni időbeviteli nézetet, és állítsa be alapértelmezett nézetként. Ennek a nézetnek tartalmaznia kell a **Leírás** és **a Külső megjegyzések** mezőket azokon az oszlopokon kívül, amelyeket a rácsnak tartalmaznia kell. A rács pozícióját, méretét és alapértelmezett rendezési sorrendjét a nézet tulajdonságainak szerkesztésével adhatja meg. Ezután állítsa be a nézet egyedi vezérlőjét úgy, hogy az egy **Időbeviteli rács** vezérlő legyen. Adja hozzá a vezérlőt a nézethez, és válassza ki a Web, a Telefon **és** a Táblagép **beállításhoz**. **·** Ezután konfigurálja a Heti időbeviteli **rács paramétereit**. Állítsa a **Kezdő dátum** mezőt msdyn **dátumra\_**, állítsa a **Duration** mezőt **msdyn\_ duration** értékre, és állítsa az **Állapot** mezőt msdyn **entrystatus\_ értékre**. A **Csak olvasható állapotlista** mező a következőre **van beállítva: 192350002 (Jóváhagyva)**, **192350003 (Elküldve)** vagy **192350004 (Visszahívás kérve)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Az egyéni mező hozzáadása a megfelelő szerkesztési laphoz
Az időbevitel vagy időbejegyzések sorának szerkesztéséhez használt oldalak az Űrlapok **alatt** találhatók. A **bejegyzés** szerkesztése gomb a rácsban megnyitja a **Bejegyzés** szerkesztése lapot, a **Sor** szerkesztése gomb pedig a **Sorszerkesztés** lapot. Ezeket az oldalakat szerkesztheti úgy, hogy egyéni mezőket tartalmazzanak.

Mindkét beállítás eltávolítja a Project **és** a **Project Tevékenység** entitások beépített szűrését, így az entitások összes keresési nézete láthatóvá válik. Azonnal csak a vonatkozó keresési nézetek láthatók.

Meg kell határoznia az egyéni mező megfelelő lapját. Valószínűleg, ha hozzáadta a mezőt a rácshoz, annak a Sorszerkesztési **oldalon kell lennie, amely az** időbejegyzések teljes sorára vonatkozó mezőkhöz használatos. Ha az egyéni mezőnek minden nap egyedi értéke van a sorban (például ha ez egy egyéni mező a befejezési időpontra), akkor az **Időbevitel szerkesztése** lapon kell lennie.

Ha hozzá szeretné adni az egyéni mezőt egy oldalhoz, húzzon egy **Mező** elemet az oldal megfelelő helyére, majd állítsa be a tulajdonságait.

### <a name="add-new-option-set-values"></a>Új beállítási értékek hozzáadása
Ha értékkészlet értékeket szeretne hozzáadni egy beépített mezőhöz, kövesse az alábbi lépéseket.

1. Nyissa meg a mező szerkesztési lapját, majd a Típus **csoportban** válassza a szerkesztés **lehetőséget** a értékkészlet mellett.
2. Adjon hozzá egy új opciót, amelynek egyedi címkéje és színe van. Ha új időbeviteli állapotot szeretne hozzáadni, a beépített mező neve **Entry Status (Bejegyzés állapota**) lesz.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Új időbeviteli állapot kijelölése csak olvashatóként
Ha egy új időbeviteli állapotot csak olvashatónak szeretne megadni, akkor adja hozzá az új időbeviteli értéket a **Csak olvasható állapotlista** tulajdonsághoz. Ügyeljen arra, hogy a számot adja hozzá, ne a címkét. Az időbeviteli rács szerkeszthető része mostantól zárolva lesz az új állapotú sorok számára. Ha a csak olvasható állapotlista **tulajdonságot eltérően szeretné beállítani a** különböző **Időbevitel** nézetekhez, adja hozzá az **Időbevitel** rácsot egy nézet Egyéni vezérlők **szakaszához**, és konfigurálja a paramétereket a megfelelő módon.

Ezután adjon hozzá üzleti szabályokat a Sorszerkesztés **és** az **Időbevitel szerkesztési oldalának összes mezőjének zárolásához**. Az oldalak üzleti szabályainak eléréséhez nyissa meg az egyes oldalakhoz tartozó űrlapszerkesztő, majd válassza az Üzleti szabályok **lehetőséget**. Az állapotot hozzáadhatja a feltételhez a meglévő üzleti szabályokban, vagy hozzáadhat egy új üzleti szabályt az új állapothoz.

### <a name="add-custom-validation-rules"></a>Egyéni ellenőrzési szabályok hozzáadása
A Heti időbeviteli **rácshoz kétféle érvényesítési szabályt** adhat hozzá:

- Az oldalakon működő ügyféloldali üzleti szabályok
- Kiszolgálóoldali beépülő modul érvényesítései, amelyek a bejegyzés minden frissítésére vonatkoznak

#### <a name="client-side-business-rules"></a>Ügyféloldali üzleti szabályok
Az üzleti szabályok segítségével zárolhatja és feloldhatja a mezőket, mezőkbe írhat be alapértelmezett értékeket, és meghatározhatja azokat az érvényesítéseket, amelyek csak az aktuális időbeviteli rekordból tartalmaznak információt. Egy oldal üzleti szabályainak eléréséhez nyissa meg a űrlapszerkesztő, majd válassza az Üzleti szabályok **lehetőséget**. Ezután szerkesztheti a meglévő üzleti szabályokat, vagy hozzáadhat új üzleti szabályokat.

#### <a name="server-side-plug-in-validations"></a>Kiszolgálóoldali beépülő modulok ellenőrzése
Beépülő modulos ellenőrzéseket kell használnia minden olyan ellenőrzéshez, amely több környezetet igényel, mint amennyi egy egyszeri bejegyzési rekordban elérhető. Ezeket minden olyan ellenőrzéshez is használnia kell, amelyet a rácsban lévő beágyazott frissítéseken szeretne futtatni. Az ellenőrzések befejezéséhez hozzon létre egy egyéni beépülő modult az **Időbevitel** entitáson.

### <a name="limits"></a>Korlátozások
Jelenleg az **Időbevitel** rács méretkorlátja 500 sor. Ha 500-nál több sor van, a felesleges sorok nem jelennek meg. Ezt a méretkorlátot nem lehet növelni.

### <a name="copying-time-entries"></a>Időbejegyzések másolása
Az **Időbejegyzés másolásához használt oszlopok** nézet használatával adja meg a másolandó mezők listáját az időbejegyzés során. A **Dátum** és az **Időtartam** kötelező mezők, és nem lehet ezeket eltávolítani a nézetből.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
