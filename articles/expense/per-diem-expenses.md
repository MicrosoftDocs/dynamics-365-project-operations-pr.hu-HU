---
title: Napidíjköltségek
description: Ez a cikk információt nyújt a napidíjas kiadások használatáról.
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
> A cikkben bemutatott funkció az előzetes verzió részeként áll rendelkezésre a megcélzott felhasználók számára.

A napidíjas fizetés rögzített, előre meghatározott napi költségtérítés, amit a vállalat fizet a alkalmazottainak szállás (szállodák), étkezés és egyéb járulékos kiadások fedezésére, amelyek az alkalmazottak számára a munkával kapcsolatos utazások során felmerülnek. A vállalat a tényleges utazási kiadások helyett ezt a költségtérítést fizeti az alkalmazottaknak. A munkatársak a **Járulékos/egyéb** napidíjas térítést használhatják a fontos üzleti értekezlethez kapcsolódó borravalók, szobaszolgáltatások, és mosoda. tisztítószolgáltatások fedezésére. A napidíj mértéke attól függően változhat, hogy a munkáltató visszatéríti-e a szállás és étkezések teljes költségét vagy csak az étkezéseket és a járulékos költségeket téríti.

A napidíj az évszaktól, az utazás helyétől vagy mindkettőtől függhet. Amikor napidíjat hoz létre, megadhatja, hogy a napidíj bizonyos százalékát visszatartsák, ha egy munkavállaló ingyenes étkezést vagy szolgáltatásokat kap. Beállíthatja azt a minimális és maximális óraszámot is, amelyre a napidíj a munkavállaló utazása esetében vonatkozhat.

A napidíjat a rendszer úgy számítja ki, hogy a napi teljes költségtérítésből kivonja az étkezésekkel kapcsolatos levonást (az ingyenes étkezás ára), amelyet a munkavállalónak biztosítanak.

## <a name="configure-per-diems"></a>Napidíjak konfigurálása

Az napidíjak konfigurálásához kövesse az alábbi lépéseket.

1. Válassza a **Költségkezelés** \> **Beállítás** \> **Általános** \> **Költségkezelési paraméterek** lehetőséget.
2. Az **Étkezési levonás számításának alapja** mezőben a **Napidíj** lapon adja meg, hogy hogyan kell kiszámítani a napidíjat:

    - **Étkezéstípus utanként**– A napidíj megadott étkezéstípus (reggeli, ebéd vagy vacsora) és az út időtartamára meghatározott az napidíjban egyes étkezéstípusokhoz meghatározott étkezési levonás alapján lesz kiszámítva.
    - **Étkezéstípus naponként**– A napidíj megadott étkezéstípus és a napra meghatározott az napidíjban egyes étkezéstípusokhoz meghatározott étkezési levonás alapján lesz kiszámítva.
    - **Étkezések száma naponta** – A napidíj kiszámítása a naponta megadott étkezések és az egyes napokhoz megadott étkezések számához, amelyek meg van adva az egyes napokhoz.

3. Válassza a **Költségkezelés** \> **Beállítások** \> **Számítások és kódok** \> **Napidíjhelyek** menüpontot.
4. Helyek hozzáadása, ahol a napidíj használható.
5. A **Napidíj** lapon hozzáadott helyek mindegyikéhez válassza ki a napidíj mértékét és a pénznemet, amely egy adott kezdő és záró dátum között érvényes a szállás, az étkezés és az egyéb költségek esetében. A napidíj díjainak és a pénznemeinek konfigurálásához válassza a **Költségkezelés** \> **Beállítások** \> **Számítások és kódok** \> **Napidíjak** menüpontot.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Napidíjak az újragondolt költségfelületen

A napidíj funkció támogatott a Microsoft Dynamics 365 Finance 10.0.25 és újabb verzióinak **Költségkezelés** munkaterületén.

Az napidíjak engedélyezéséhez hajtsa végre az alábbi lépéseket.

1. Keresse meg és jelölje ki a listában az **Költségjelentések újragondolva** szolgáltatást a **Szolgáltatáskezelés** munkaterületen, majd válassza az **Engedélyezés most** lehetőséget.
2. Keresse meg és jelölje ki a listában az **Napidíj Költségjelentések az újragondolt felületen** szolgáltatást a listában majd válassza az **Engedélyezés most** lehetőséget.

## <a name="how-the-feature-works"></a>A funkció működése

Ez a szakasz három konfigurálási helyzetre mutat be példákat. Minden egyes példában az **Étkezési levonás számításának alapja:** mező eltérő értékre van állítva. Mindhárom példa esetén a teljes kifizetendő összeg megegyezik az étkezési levonás alkalmazásáig. Ezután a teljes kifizetendő összeg különbözik az egyes példákban.

A mindhárom példához használt napidíjas költségének létrehozásához hajtsa végre a következő lépéseket.

1. Válassza a **Munkaterületek** \> **Költségkezelés** lehetőséget.
2. Válassza az **Új költségjelentés** lehetőséget, vagy válasszon ki egy meglévő költségjelentést.
3. Adjon hozzá egy új költséget. Válassza a **Kategória** mezőben a **Napidíj** lehetőséget. Adja meg az út helyét, valamint a kezdési és befejezési dátumát. A napidíj a szálláshoz étkezésekhez és egyéb költségekhez (egyéb kiadások) a kiválasztott helyhez beállított napi költségtérítés alapján lesz kiszámítva.

    A hely például **Redmond (USA)** lesz. Ennek a helynek a napi költségkerete 150 dollár (150 USD) szállásra, 75 amerikai dollár (USD) étkezésre, valamint 5 amerikai dollár (USD) egyéb költségekre. A kezdő dátum január 10, a záró dátum január 14. Így a kijelölt időtartam öt nap, amikor a kiválasztott konfiguráció naptári nap az idővel, és a kiválasztott idő a kezdő és a záró dátumon 12:00 órakor kezdődik és végződik. Itt vannak a számítások:

    - Teljes kifizetendő összeg = 5 × (150 + 75 + 5) = 5 × 230 = 1150 amerikai dollár (USD)
    - A teljes összeg étkezés és egyéb költségek része = 5 × (75 + 5) = 400 amerikai dollár (USD)

Ha az út során ebédet és vacsorát biztosítanak, akkor ezek az étkezések étkezéslevonásnak számítanak.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>1. példa: Napidíj, amikor az étkezési levonás az utankénti étkezéstípuson alapul

Ebben a példában az étkezési levonás 30 százalék a reggelire, 30 százalék az ebédre, a 40 százalékot a vacsorára. A **Költségkezelés paraméterei** oldalon az **Étkezési levonás számításának alapja:** mező beállítása **Étkezéstípus utanként**. Itt vannak a számítások, ha az alkalmazott számára három reggelit, két ebédet és két vacsorát biztosította munkáltató:

- Étkezési levonás = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = 112,50 amerikai dollár (USD)
- Étkezés és egyéb költségek = 400 – 112,50 = 287,50 amerikai dollár (USD)
- Összes kifizetendő összeg = Teljes költségtérítés – Étkezési levonás = 1150 – 112,50 = 1037,50 amerikai dollár (USD)

![Napidíj kiadás, amikor az étkezési levonás az utankénti étkezéstípuson alapul.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>2. példa: Napidíj, amikor az étkezési levonás az napi étkezéstípuson alapul

Ebben a példában az étkezési levonás 30 százalék a reggelire, 30 százalék az ebédre, a 40 százalékot a vacsorára. A **Költségkezelés paraméterei** oldalon az **Étkezési levonás számításának alapja:** mező beállítása **Étkezéstípus naponként**. Ebben az esetben a **Költség szerkesztése** párbeszédpanel **Étkezések** rácsában törölje a jelölőnégyzeteket annak jelzéséhez, hogy az út során milyen étkezések lettek biztosítva.

Itt vannak például a számítások arra az esetre hogy az út első három napja során volt biztosítva étkezés:

- Napi étkezési levonás az első három napra = 75 × 30% = 22,50 amerikai dollár (USD)
- Teljes étkezési levonás = 3 × 22,50 = 67,50 amerikai dollár (USD)
- Étkezések és egyéb költéségek események az 1– 3. napra = 75 – 22,50 = 57,50 amerikai dollár (USD)
- Összes étkezés és egyéb költség = Az étkezések és egyéb költésége öt napra = 400 – 67,50 = 332,50 amerikai dollár (USD)
- Összes kifizetendő összeg = Teljes összeg – Étkezési levonás = 1150 – 67,50 = 1082,50 amerikai dollár (USD)

![Napidíj kiadás, amikor az étkezési levonás az naponkénti étkezéstípuson alapul.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>3. példa: Napidíj, amikor az étkezési levonás az napi étkezések számán alapul

Ebben a példában az étkezési levonása az egy napon biztosított étkezések számán alapul (ez azt jelenti, hogy a **Költségkezelés paramétereinek** oldalán az **Étkezési levonás számításának alapja** mezőjének beállítása **Étkezések száma naponta**). A **Költség szerkesztése** párbeszédpanel **Étkezések** rácsában törölje a jelölőnégyzeteket annak jelzéséhez, hogy mely étkezések lettek biztosítva.
Ebben az esetben a étkezési levonás kizárólag a biztosított étkezések száma alapján történik, nem pedig a biztosított étkezés típusa (reggeli/ebéd/vacsora) alapján.

A következő számítások vannak alkalmazva, ha a napi költségkeret 150 amerikai dollár (USD) szállásra, 75 amerikai dollár (USD) étkezésekre, illetve ki lehet 5 amerikai dollár (USD) egyéb költségekre:

- **Teljes kifizetendő összeg** = 5 × (150 + 75 + 5) = 5 × 230 = 1150 amerikai dollár (USD)
- **Egy étkezés:** Étkezési levonás: 20% = 15 amerikai dollár (USD)
- **Két étkezés:** Étkezési levonás: 50% = 37,50 amerikai dollár (USD)
- **Három étkezés:** Étkezési levonás: 100% = 75 amerikai dollár (USD)

A következő számítások szolgálnak az **étkezések és egyéb költségek költségkerethez**, amely 5 amerikai dollárt (USD) tartalmaz egyéb költségekre:

- 1. nap – Két étkezés biztosítva = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 amerikai dollár (USD)
- 2. nap – Két étkezés biztosítva = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 amerikai dollár (USD)
- 3. nap – Két étkezés biztosítva = (75 – 15) + 5 = 60 + 5 = 65 amerikai dollár (USD)
- 4. nap – Nulla étkezés biztosítva = (75 – 0) + 5 = 75 + 5 = 80 amerikai dollár (USD)
- 5. nap – Három étkezés biztosítva = (75 – 75) + 5 = 0 + 5 = 5 amerikai dollár (USD)

- Összes étkezés és egyéb költség = Étkezések és egyéb költségek 1. nap + 2. nap + 3. nap + 4. nap + 5. nap = 235 amerikai dollár (USD)
- A teljes étkezési levonás = Étkezési levonás az 1. napra + 2. napra +3. napra + 4. napra + 5. napra = 37,5+ 37,5+ 15 + 0+ 75 = 165 amerikai dollár (USD)
- Összes kifizetendő összeg = Teljes költségtérítés – Teljes étkezési levonás = 1150 amerikai dollár (USD) – 165 amerikai dollár (USD)= 985 amerikai dollár (USD)

![Napidíj kiadás, amikor az étkezési levonás az étkezések számán múlik naponta.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> A Finaince 10.0.23-as verziójától, ha az újragondolt költségfelületet használja, nem hozhat létre napidíjas költségeket átfedő dátumokkal. Ha megpróbálja, egy hibaüzenet jelenik meg.
