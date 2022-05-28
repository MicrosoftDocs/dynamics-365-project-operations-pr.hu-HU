---
title: Napidíj
description: Ez a témakör tájékoztatást nyújt arról, hogyan kell dolgozni a napidíjjal.
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
ms.openlocfilehash: fe72f066a6819c3b43e3977d5e7afb01ba95338c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596053"
---
# <a name="per-diem-expenses"></a>Napidíj

> [!IMPORTANT] 
> Az ebben a témakör leírt funkciók az előzetes verzió részeként érhetők el a megcélzott felhasználók számára.

A napidíj egy rögzített, előre meghatározott napi juttatás, amelyet a vállalat fizet alkalmazottainak a szállásért (szállodákért), étkezésekért és járulékos költségekért, amelyeket ezek az alkalmazottak a munka során viselnek. A vállalat ezt a juttatást a munkavállalóknak fizeti ahelyett, hogy a tényleges utazási költségeket fizetné. Az alkalmazottak az Incidentals/Other **per diem juttatást felhasználhatják** a fontos üzleti találkozókra vonatkozó tippek, szobaszerviz, mosoda vagy vegytisztítási szolgáltatások fedezésére. A napidíj változhat, attól függően, hogy a munkáltató úgy dönt- e, hogy megtéríti a szállás és az étkezés együttes költségét, vagy csak az étkezések és a járulékos költségek költségeit.

A napidíj az évszaktól, az utazás helyétől vagy mindkettőtől függhet. Napidíj-szabály létrehozásakor megadhatja, hogy a napidíj egy százaléka visszatartásra kerül, ha az alkalmazott ingyenes étkezést vagy szolgáltatásokat kap. Azt is beállíthatja, hogy a napidíj alkalmazható legyen az alkalmazott utazására.

A napidíjat úgy számítják ki, mint a napi teljes juttatást, levonva a munkavállalónak nyújtott étkezéscsökkentést (az ingyenes étkezés költségét).

## <a name="configure-per-diems"></a>Napidíjas konfiguráció

A napidíj konfigurálásához hajtsa végre az alábbi lépéseket.

1. Nyissa meg a **Költségkezelés** \> **beállítása** \> **általános** \> **költségkezelési paramétereket.**
2. **A Per diem** lapon, az **Étkezéscsökkentés** kiszámítása mezőben válassza ki a napidíj kiszámításának módját:

    - **Étkezés típusa utazásonként** – Számítsa ki a napidíjat a megadott étkezés típusa (reggeli, ebéd vagy vacsora) és az egyes étkezéstípusokra meghatározott étkezéscsökkentés alapján az utazás időtartama alatt.
    - **Étkezés típusa naponta** – Számítsa ki a napidíjat a bevitt étkezés típusa és az egyes étkezéstípusokra meghatározott étkezéscsökkentés alapján a napidíjhoz.
    - **Napi étkezések** száma – Számítsa ki a napi étkezések számát és a naponta biztosított étkezések számát.

3. Nyissa meg a **Költségkezelés** \> **beállítása** \> **számítások és kódok diem-helyekenkénti beállításait.** \> **·**
4. Adja hozzá azokat a helyeket, ahol a napidíj használható.
5. Minden hozzáadott helyhez a **Napidíj** lapon válassza ki a napidíj és pénznem értékét, amelyek a szállás, étkezés és egyéb költségek konkrét kezdési és befejezési dátumai között érvényesek. A napidíj és pénznemek konfigurálásához nyissa meg a **Költségkezelés** \> **beállítása** \> **számításokat és kódokat** \> **diemenként.**

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Napidíj az újragondolt költségfelületen

A napidíjas funkciót a 365-ös Pénzügyi verzió 10.0.25-ös és újabb verziójában **támogatja az újragondolt** Költségkezelési Microsoft Dynamics munkaterület.

A napidíj engedélyezéséhez kövesse az alábbi lépéseket.

1. **A Szolgáltatáskezelés** munkaterületen keresse meg és jelölje ki a **költségjelentések újragondolt** szolgáltatását a listában, majd válassza az Engedélyezés most **lehetőséget**.
2. Keresse meg és válassza ki a **költségjelentés újragondolt felületi** szolgáltatását a listában, majd válassza az Engedélyezés most **lehetőséget**.

## <a name="how-the-feature-works"></a>A funkció működése

Ez a szakasz három konfigurációs forgatókönyvre mutat be példákat. Minden egyes példánál az **Étkezéscsökkentés számítása mező szerint** más értékre van állítva. Mindhárom példa esetében a fizetendő teljes összeg megegyezik az étkezéscsökkentés alkalmazásáig. Ezt követően a fizetendő teljes összeg minden egyes példánál eltérő.

A három példához használt napidíj létrehozásához kövesse az alábbi lépéseket.

1. Nyissa meg a **Munkaterületek** \> **költségkezelése lehetőséget.**
2. Válassza az **Új költségjelentés lehetőséget**, vagy válasszon ki egy meglévő költségjelentést.
3. Adjon hozzá egy új költséget. A Kategória **mezőben válassza a** Napidíj **lehetőséget**. Válassza ki az utazás helyét, valamint kezdési és befejezési dátumát. A szállásra, étkezésre és járulékos költségekre (egyéb költségekre) vonatkozó napidíjat a kiválasztott helyre beállított napidíj alapján számítják ki.

    Például Redmond (USA) **lehetőséget választja** helyként. A napidíj erre a helyre 150 USA dollár (USD 150) a szállásért, USD 75 étkezésért és USD 5 a járulékosakért. A kezdési dátum január 10., a befejezési dátum pedig január 14. Ezért a kiválasztott időtartam öt nap, amikor a kiválasztott konfiguráció naptári napok az idővel, és a kiválasztott idő a kezdési és befejezési dátumokon 12:00 órakor kezdődik és végződik. Íme a számítások:

    - Teljes fizetendő összeg = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
    - Étkezés és a teljes mennyiség járulékos része = 5 × (75 + 5) = USD 400

Ha az utazás során reggelit, ebédet és vacsorát biztosítottak, ezeket az ételeket étkezéscsökkentésként kell elszámolni.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>1. példa: Napidíj, ahol az étkezés csökkentése az utazásonkénti étkezés típusán alapul

Ebben a példában az étkezés csökkentése 30% reggelire, 30% ebédre és 40% vacsorára. A Költségkezelési paraméterek **lapon az** **Étkezéscsökkentés számítása mező szerint** az Étkezéstípus számítása utazásonként értékre **van állítva**. Íme a számítások, ha három reggelit, két ebédet és nulla vacsorát biztosítottak a munkavállalónak:

- Étkezés csökkentése = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112.50
- Étkezések és járulékos események = 400 – 112,50 = USD 287.50
- Teljes fizetendő összeg = Teljes juttatás – Étkezéscsökkentés = 1150 – 112,50 = USD 1,037.50

![Napidíj, ahol az étkezés csökkentése az utazásonkénti étkezés típusán alapul.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>2. példa: Napidíj, ahol az étkezések csökkentése a napi étkezés típusán alapul

Ebben a példában az étkezés csökkentése 30% reggelire, 30% ebédre és 40% vacsorára. A Költségkezelési paraméterek lapon az **Étkezéscsökkentés kiszámítása mezőben** a **napi** Étkezéstípus értékre **van** állítva. Ebben az esetben a **Költség** szerkesztése párbeszédpanel Étkezés **rácsában törölje a jelet a** jelölőnégyzetekből, jelezve, hogy mely ételeket biztosították Önnek az utazás során.

Például itt vannak a számítások, ha a reggelit az utazás első három napjára biztosították:

- Napi étkezéscsökkentés az első három nap mindegyikére = 75 × 30% = USD 22.50
- Teljes étkezéscsökkentés = 3 × 22,50 = USD 67.50
- Étkezések és járulékos események az 1-től 3-ig terjedő napokban = 75 –22,50 = USD 57.50
- Összes étkezés és járulékos esemény = Étkezések és járulékos események összege öt nap alatt = 400 – 67,50 = USD 332.50
- Teljes fizetendő összeg = Teljes összeg – Étkezéscsökkentés = 1150 – 67,50 = USD 1,082.50

![Napidíj, ahol az étkezés csökkentése a napi étkezés típusán alapul.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>3. példa: Napidíj, ahol az étkezések csökkentése a napi étkezések számán alapul

Ebben a példában az étkezéscsökkentést a naponta biztosított étkezések száma alapján számítják ki (azaz a **Költségkezelési paraméterek oldalon az** étkezéscsökkentés kiszámítása mező szerint **beállítása** napi **étkezések** száma). A Költség **szerkesztése párbeszédpanel Étkezés** rácsában törölje a **jelet a** jelölőnégyzetekből, hogy jelezze, mely étkezések biztosítottak.
Ebben az esetben az étkezés csökkentése csak a rendelkezésre bocsátott ételek számán alapul, nem pedig a rendelkezésre álló étkezés típusán (reggeli / ebéd / vacsora).

Íme a napidíjra vonatkozó számítások, amikor a napidíjat szállásra, étkezésre USD 75 USD 150, és USD 5 a járulékos esetekre:

- **Teljes fizetendő** összeg = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
- **Egy étkezés:** Étkezés csökkentése = 20% = USD 15
- **Két étkezés:** Étkezés csökkentése = 50% = USD 37.50
- **Három étkezés:** Étkezés csökkentése = 100% = USD 75

Íme az étkezések és járulékos **juttatások** számításai, amelyek magukban foglalják a USD 5 a járulékosak esetében:

- 1. nap - Két étkezés = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- 2. nap - Két étkezés = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- 3. nap - Egy étkezés = (75 – 15) + 5 = 60 + 5 = USD 65
- 4. nap - Nulla étkezés = (75-0) + 5 = 75 + 5 = USD 80
- 5. nap - Három étkezés = (75 – 75) + 5 = 0 + 5 = USD 5

- Összes étkezés és járulékos esemény = Étkezések és járulékos események az 1. napra+ 2. nap +3+4+ 5. nap = USD 235
- Teljes étkezéscsökkentés = Étkezéscsökkentés az 1. napra+ 2. napra +3. nap+4+ 5. nap= 37,5+ 37,5+ 15 + 0+ 75 = USD 165
- Teljes fizetendő összeg = Teljes juttatás – Teljes étkezéscsökkentés = USD 1,150 - USD 165 = USD 985

![Napidíj, ahol az étkezés csökkentése a napi étkezések számán alapul.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> A Pénzügy 10.0.23-as verziójától kezdve, ha az újragondolt költségfelületet használja, nem hozhat létre napidíjas költségeket, amelyek egymást átfedő dátumokkal rendelkeznek. Ha megpróbálja, hibaüzenet jelenik meg.
