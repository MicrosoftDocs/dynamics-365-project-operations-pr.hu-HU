---
title: Időbejegyzések kiterjesztése
description: Ez a témakör információt nyújt arról, hogy a fejlesztők hogyan tudják kiterjeszteni az időbejegyzés-vezérlőt.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582989"
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
Minden időbejegyzés egy időforrásrekordhoz van társítva. Ez a rekord határozza meg, hogy mely alkalmazásoknak kell feldolgozniuk az időbevitelt és hogyan.

Az időbejegyzések mindig folytonos időegységek, amelyek kezdése, befejezése és időtartama egymáshoz kapcsolódnak.

A logika a következő helyzetekben automatikusan frissíti az időbejegyzési rekordot:

- Ha a három következő mező közül kettő van megadva, akkor a program automatikusan kiszámítja a harmadikat: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- A **msdyn_start** és **msdyn_end** mezők időzóna-tudatában vannak.
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

1. Adja hozzá az egyéni mezőt a **Gyors létrehozása** párbeszédpanelhez.
2. Konfigurálja a rácsot az egyéni mező megjelenítéséhez.
3. Adott esetben adja hozzá az egyéni mezőt a **Sor szerkesztése** vagy **az Időbejegyzés szerkesztése** laphoz.

Győződjön meg arról, hogy az új mező rendelkezik a szükséges ellenőrzésekkel a Sor szerkesztése **vagy** az **Időbejegyzés szerkesztése** lapon. A feladat részeként zárolja a mezőt az időbejegyzés állapota alapján.

Ha egyéni mezőt ad hozzá az **Időbevitel** rácshoz, majd közvetlenül a rácson hoz létre időtételeket, a program automatikusan beállítja a tételek egyéni mezőjét, hogy az megfeleljen a sornak. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Az egyéni mező hozzáadása a Gyors létrehozás párbeszédpanelhez
Adja hozzá az egyéni mezőt a **Gyors létrehozás: Időbevitel** létrehozása párbeszédpanelhez. A felhasználók ezután beírhatnak egy értéket, amikor az **Új** lehetőséget választva adnak hozzá időbejegyzéseket.

### <a name="configure-the-grid-to-show-the-custom-field"></a>A rács konfigurálása az egyéni mező megjelenítéséhez
Kétféleképpen adhat egyéni mezőt a **Heti időbevitel** rácshoz.

- Testreszabhatja a **Heti időtételek nézetet**, és adja hozzá az egyéni mezőt. A rács egyéni mezőjének helyét és méretét a nézet tulajdonságainak szerkesztésével határozhatja meg.
- Hozzon létre egy új egyéni időbeviteli nézetet, és állítsa be alapértelmezett nézetként. Ennek a nézetnek tartalmaznia kell a Leírás **és** a **Külső megjegyzések** mezőket azon oszlopok mellett, amelyeket a rácsnak tartalmaznia kell. A rács helyét, méretét és alapértelmezett rendezési sorrendjét a nézet tulajdonságainak szerkesztésével adhatja meg. Ezután állítsa be a nézet egyedi vezérlőjét úgy, hogy az egy **Időbeviteli rács** vezérlő legyen. Adja hozzá a vezérlőt a nézethez, és jelölje ki a web **, a telefon** és **a táblagép számára** **.** Ezután konfigurálja a **Heti időbeviteli** rács paramétereit. Állítsa a **Kezdési dátum** mezőt msdyn **dátumra\_**, állítsa az **Időtartam** mezőt msdyn **időtartamra\_**, és állítsa az **Állapot** mezőt msdyn **entrystatus\_ értékre**. Az **Írásvédett állapotlista** mező értéke **192350002 (jóváhagyva),** **192350003 (beküldve)** vagy **192350004 (visszahívás kért)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Egyéni mező hozzáadása a megfelelő szerkesztési laphoz
Az időbejegyzések vagy időbejegyzések sorozatának szerkesztésére használt lapok az Űrlapok **alatt** találhatók. A **rács Bejegyzés** szerkesztése gombja megnyitja a **Szerkesztés tétel** lapot, és a **Sor** szerkesztése gomb megnyitja a **Sor szerkesztése** lapot. Ezeket a lapokat úgy szerkesztheti, hogy egyéni mezőket tartalmazzanak.

Mindkét beállítás eltávolít néhány beépített szűrést a Projekt **- és** Projekttevékenység-entitásokon **·**, így az entitások összes keresési nézete látható legyen. Azonnal csak a vonatkozó keresési nézetek láthatók.

Meg kell határoznia az egyéni mezőnek megfelelő lapot. Valószínűleg, ha hozzáadta a mezőt a rácshoz, akkor annak a **Sor szerkesztése lapon kell megjelennie**, amely a teljes időtételsorra vonatkozó mezőkhöz használatos. Ha az egyéni mezőnek minden nap egyedi értéke van a sorban (például ha ez egy egyéni mező a befejezési időhöz), akkor az **Időbejegyzés szerkesztése lapon kell megjelennie**.

Ha az egyéni mezőt hozzá szeretné adni egy laphoz, húzzon egy **Mező** elemet a lap megfelelő helyére, majd állítsa be annak tulajdonságait.

### <a name="add-new-option-set-values"></a>Új beállítási értékek hozzáadása
Ha értékkészlet értékeket szeretne hozzáadni egy beépített mezőhöz, hajtsa végre az alábbi lépéseket.

1. Nyissa meg a mező szerkesztési lapját, majd a Típus csoportban **válassza a Szerkesztés** lehetőséget **a értékkészlet** mellett.
2. Adjon hozzá egy új opciót, amelynek egyedi címkéje és színe van. Ha új időtétel-állapotot szeretne hozzáadni, a beépített mező neve **Tétel állapota** lesz.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Új időbeviteli állapot kijelölése csak olvashatóként
Ha egy új időbeviteli állapotot csak olvashatónak szeretne megadni, akkor adja hozzá az új időbeviteli értéket a **Csak olvasható állapotlista** tulajdonsághoz. Ügyeljen arra, hogy a számot adja hozzá, ne a címkét. Az időbeviteli rács szerkeszthető része zárolva lesz az új állapotú sorokhoz. Ha a különböző **Időbevitel** nézetekhez eltérően szeretné beállítani az **Írásvédett állapotlista** tulajdonságot, adja hozzá az Időbeviteli **rácsot a** nézet Egyéni vezérlők **szakaszához**, és konfigurálja a paramétereket a megfelelő módon.

Ezután adjon hozzá üzleti szabályokat a Sor szerkesztése és az **Idő bejegyzés szerkesztése lapok összes mezőjének zárolásához**.**·** Az ezen oldalakra vonatkozó üzleti szabályok eléréséhez nyissa meg az egyes oldalak űrlapszerkesztő, majd válassza az Üzleti szabályok **lehetőséget**. Az állapotot hozzáadhatja a feltételhez a meglévő üzleti szabályokban, vagy hozzáadhat egy új üzleti szabályt az új állapothoz.

### <a name="add-custom-validation-rules"></a>Egyéni ellenőrzési szabályok hozzáadása
A Heti időbevitel **rácsának felhasználói élményéhez** kétféle ellenőrzési szabályt adhat hozzá:

- Az oldalakon működő ügyféloldali üzleti szabályok
- Kiszolgálóoldali beépülő modulok érvényesítése, amelyek minden időbejegyzési frissítésre vonatkoznak

#### <a name="client-side-business-rules"></a>Ügyféloldali üzleti szabályok
Az üzleti szabályok segítségével zárolhatja és feloldhatja a mezőket, mezőkbe írhat be alapértelmezett értékeket, és meghatározhatja azokat az érvényesítéseket, amelyek csak az aktuális időbeviteli rekordból tartalmaznak információt. A lap üzleti szabályainak eléréséhez nyissa meg a űrlapszerkesztő, majd válassza az Üzleti szabályok **lehetőséget**. Ezután szerkesztheti a meglévő üzleti szabályokat, vagy hozzáadhat új üzleti szabályokat.

#### <a name="server-side-plug-in-validations"></a>Kiszolgálóoldali beépülő modulok ellenőrzése
Beépülő modul-ellenőrzéseket kell használnia minden olyan ellenőrzéshez, amely több környezetet igényel, mint amennyi az egyetlen bejegyzésben elérhetőnél több környezetet igényel. Ezeket minden olyan ellenőrzéshez is használnia kell, amelyet a rács beágyazott frissítésein szeretne futtatni. Az ellenőrzések befejezéséhez hozzon létre egy egyéni beépülő modult az **Időbejegyzés** entitáson.

### <a name="limits"></a>Korlátozások
Jelenleg az **Időbejegyzési** rács méretkorlátja 500 sor. Ha több mint 500 sor van, a felesleges sorok nem jelennek meg. Ezt a méretkorlátot nem lehet növelni.

### <a name="copying-time-entries"></a>Időbejegyzések másolása
Az **Időbejegyzés másolásához használt oszlopok** nézet használatával adja meg a másolandó mezők listáját az időbejegyzés során. A **Dátum** és az **Időtartam** kötelező mezők, és nem lehet ezeket eltávolítani a nézetből.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
