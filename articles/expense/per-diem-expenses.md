---
title: Napidíjköltségek
description: Ez a cikk tájékoztatást nyújt arról, hogyan kell dolgozni a napidíjas költségekkel.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923191"
---
# <a name="per-diem-expenses"></a>Napidíjköltségek

> [!IMPORTANT] 
> A cikkben ismertetett funkciók a megcélzott felhasználók számára érhetők el az előzetes verzió részeként.

A napidíj egy rögzített, előre meghatározott napidíj, amelyet a vállalat fizet az alkalmazottainak szállásért (szállodákért), étkezésért és járulékos költségekért, amelyeket ezek az alkalmazottak viselnek, miközben munkába utaznak. A vállalat ezt a juttatást a tényleges utazási költségek kifizetése helyett fizeti ki az alkalmazottaknak. Az alkalmazottak a járulékos/egyéb **napidíjukat felhasználhatják** a tippek, a szobaszerviz, a mosoda vagy a vegytisztítási szolgáltatások fedezésére fontos üzleti találkozókon. A napidíj változhat attól függően, hogy a munkáltató úgy dönt-e, hogy megtéríti-e a szállás és az étkezés együttes költségét, vagy csak az étkezések és a járulékos költségek megtérítését.

A napidíj az évszaktól, az utazás helyétől vagy mindkettőtől függhet. Napidíj-alapú szabály létrehozásakor megadhatja, hogy a napidíj egy százalékát visszatartsa, ha egy alkalmazott ingyenes étkezést vagy szolgáltatásokat kap. Beállíthatja azt is, hogy a minimális óraszámot és a maximális óraszámot a napidíj alkalmazható legyen az alkalmazott utazására.

A napidíj a napidíjként történő kiszámítása a naponta kínált teljes juttatásként történik, levonva ebből a munkavállalónak nyújtott étkezéscsökkentést (az ingyenes étkezések költségét).

## <a name="configure-per-diems"></a>Napidíjas konfiguráció

A napidíj-költségek konfigurálásához kövesse az alábbi lépéseket.

1. Lépjen a **Költségkezelés** \> **beállítása** \> **általános** \> **költségkezelési paraméterek elemre.**
2. **A Napidíjas** lap Étkezés csökkentésének kiszámítása mezőjén **válassza** ki, hogyan kell kiszámítani a napidíjakat:

    - **Étkezés típusa utazásonként** – Számítsa ki a napidíjat a megadott étkezés típusa (reggeli, ebéd vagy vacsora) és az étkezés csökkentése alapján, amelyet az egyes étkezéstípusokhoz az utazás időtartamára vonatkozó napidíjra határoznak meg.
    - **Étkezés típusa naponta** – Számítsa ki a napidíjas napidíjat a beírt étkezés típusa és az egyes étkezési típusokra meghatározott étkezéscsökkentés alapján a napi napi napidíjra.
    - **Napi** étkezések száma - Számítsa ki a napidíjat a naponta megadott étkezések száma és az étkezés csökkentése alapján az egyes naponta biztosított étkezések száma alapján.

3. Lépjen a **Költségkezelés** \> **beállítási** \> **számításai és kódjai** \> **lapkahelyenként** elemre.
4. Adjon hozzá olyan helyeket, ahol a napidíjak felhasználhatók.
5. Minden hozzáadott helynél a **Napidíjak** lapon válassza ki a napidíj és a pénznemet, amelyek a szállás, étkezések és egyéb költségek adott kezdési és befejezési dátumai között érvényesek. A napidíjak és pénznemek konfigurálásához lépjen a **Költségkezelés** \> **beállítása** \> **Számítások és kódok** \> **napidíjként című témakörbe.**

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Napidíjak az újragondolt költségfelületen

A napidíjas funkciót az újragondolt **Költségkezelés** munkaterület támogatja a 365 Finance 10.0.25-ös és újabb verzióiban Microsoft Dynamics.

A napidíjak engedélyezéséhez kövesse az alábbi lépéseket.

1. **A Funkciókezelés** munkaterületen keresse meg és válassza ki a listában a **Költségjelentések újragondolva** funkciót, majd válassza az Engedélyezés most **lehetőséget**.
2. Keresse meg és válassza ki a listában a **Költségjelentés újragondolt felületének** lapkája funkciót, majd válassza az Engedélyezés most **lehetőséget**.

## <a name="how-the-feature-works"></a>A funkció működése

Ez a szakasz három konfigurációs forgatókönyvre mutat be példákat. Az étkezés csökkentésének **kiszámítása mező minden egyes példában** más értékre van állítva. Mindhárom példa esetében a fizetendő teljes összeg megegyezik az étkezés csökkentésének alkalmazásáig. Ezt követően a teljes fizetendő összeg minden példánál eltérő.

A három példához használt napidíj létrehozásához kövesse az alábbi lépéseket.

1. Lépjen a **Munkaterületek** \> **költségkezelése oldalra.**
2. Válassza az Új költségjelentés **lehetőséget**, vagy válasszon ki egy meglévő költségjelentést.
3. Adjon hozzá egy új költséget. A Kategória **mezőben válassza a** Napilaponként **lehetőséget**. Válaszd ki az utazásod helyét, valamint kezdési és befejezési dátumát. A szállásra, étkezésre és járulékos költségekre (egyéb költségekre) vonatkozó napidíjat a kiválasztott helyre beállított napidíj alapján számítják ki.

    Például Redmondot (USA) **választja** helyként. Az adott hely napidíja 150 amerikai dollár (150 USD) a szállásért, USD 75 az étkezésért és a USD 5 a járulékos költségekért. A kezdő dátum január 10., a befejezés dátuma január 14. Ezért a kiválasztott időtartam öt nap, amikor a kiválasztott konfiguráció naptári nap az idővel, és a kiválasztott idő a kezdési és befejezési dátumokon 12:00 órakor kezdődik és ér véget. Íme a számítások:

    - Teljes fizetendő összeg = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
    - Étkezés és a teljes mennyiségből származó járulékos rész = 5 × (75 + 5) = USD 400

Ha az utazás során reggelit, ebédet és vacsorát biztosítottak, ezeket az ételeket étkezéscsökkentésként kell elszámolni.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>1. példa: Napidíjanként, ahol az étkezés csökkentése az utazásonkénti étkezés típusán alapul

Ebben a példában az étkezés csökkentése 30 százalék a reggelinél, 30 százalék az ebédnél és 40 százalék a vacsoránál. A Költségkezelés paraméterei oldalon az **Étkezés** csökkentésének **kiszámítása mező értéke Étkezés típusa utazásonként értékre van állítva**.**·** Íme a számítások, ha három reggelit, két ebédet és nulla vacsorát biztosítottak a munkavállalónak:

- Étkezés csökkentése = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112.50
- Étkezések és járulékos étkezések = 400 – 112,50 = USD 287.50
- Teljes fizetendő összeg = Teljes támogatás – Étkezés csökkentése = 1 150 – 112,50 = USD 1,037.50

![Napidíj, ahol az étkezés csökkentése az utazásonkénti étkezés típusán alapul.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>2. példa: Napidíjasanként, ahol az étkezés csökkentése a napi étkezés típusán alapul

Ebben a példában az étkezés csökkentése 30 százalék a reggelinél, 30 százalék az ebédnél és 40 százalék a vacsoránál. A Költségkezelés paraméterei lapon az **Étkezés** csökkentésének **kiszámítása mező értéke Étkezés típusa naponta** értékre van állítva **.** Ebben az esetben a **Költség** szerkesztése párbeszédpanel Étkezések **rácsában törölje a** jelölőnégyzetek jelölését, hogy jelezze, mely étkezéseket biztosították Önnek az utazás során.

Például itt vannak a számítások, ha az utazás első három napjára reggelit biztosítottak:

- Napi étkezéscsökkentés az első három nap mindegyikében = 75 × 30% = USD 22.50
- Teljes étkezéscsökkentés = 3 × 22,50 = USD 67.50
- Étkezések és járulékos események az 1–3. napokban = 75 – 22,50 = USD 57.50
- Összes étkezés és járulékos étkezés = Az ötnapos étkezések és járulékos étkezések összege = 400 – 67,50 = USD 332.50
- Teljes fizetendő összeg = Teljes összeg – Étkezés csökkentése = 1 150 – 67,50 = USD 1,082.50

![Napidíjonkénti költség, ahol az étkezés csökkentése a napi étkezés típusán alapul.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>3. példa: Napidíjasanként, ahol az étkezések csökkentése a napi étkezések számán alapul

Ebben a példában az étkezés csökkentését a naponta megadott étkezések száma alapján számítjuk ki (azaz a **Költségkezelési paraméterek** oldalon az Étkezéscsökkentés kiszámítása mező szerint **oldalon a** Napi étkezések **száma értékre** van állítva). **A Költségek** szerkesztése párbeszédpanel Étkezések **rácsában törölje a jelet a** jelölőnégyzetekből, hogy jelezze, mely étkezések voltak megadva.
Ebben az esetben az étkezés csökkentése csak a rendelkezésre álló ételek számán alapul, nem pedig a rendelkezésre álló étkezés típusán (reggeli/ebéd/vacsora).

Íme a napidíjakra vonatkozó számítások, amikor a napidíjat szállásra USD 150, az étkezésre USD 75, valamint a járulékos USD 5:

- **Teljes fizetendő** összeg = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
- **Egy étkezés:** Étkezés csökkentése = 20% = USD 15
- **Két étkezés:** Étkezés csökkentése = 50% = USD 37.50
- **Három étkezés:** Étkezés csökkentése = 100% = USD 75

Íme az étkezésekre és a **járulékos juttatásokra** vonatkozó számítások, amelyek magukban foglalják a járulékos USD 5:

- 1. nap - Két étkezés megadva = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- 2. nap - Két étkezés = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- 3. nap - Egy étkezés megadva = (75 – 15) + 5 = 60 + 5 = USD 65
- 4. nap - Nulla étkezés = (75-0) + 5 = 75 + 5 = USD 80
- 5. nap - Három étkezés = (75 – 75) + 5 = 0 + 5 = USD 5

- Összes étkezés és járulékos étkezés = Étkezések és járulékos események az 1. napra+ 2. nap + 3. nap + 4. nap+ 5. nap = USD 235
- Teljes étkezéscsökkentés = Étkezéscsökkentés az 1. napra+ 2. nap +3. nap+4. nap+ 5. nap= 37,5+ 37,5+ 15 + 0+ 75 = USD 165
- Teljes fizetendő összeg = Összes támogatás – Teljes étkezéscsökkentés = USD 1,150 - USD 165 = USD 985

![Napidíjra vetítve, ahol az étkezés csökkentése a napi étkezések számán alapul.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> A Finance 10.0.23-as verziójától kezdve, ha az újragondolt költségfelületet használja, nem hozhat létre olyan napidíjas költségeket, amelyek egymást átfedő dátumokkal rendelkeznek. Ha megpróbálja, hibaüzenetet fog kapni.
