---
title: Alvállalkozói szerződés mérföldkövei
description: Ez a cikk azt ismerteti, hogyan hozhat létre és tarthat fenn mérföldkő-alapú számlaütemezést egy szállítóval kötött alvállalkozói szerződéshez.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2fe26f5ba3c7bbc689c83a2ba67d444a09a264d5
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261796"
---
# <a name="subcontract-line-milestones"></a>Alvállalkozói szerződés mérföldkövei

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Dynamics 365 Project Operations rendszerben egy fix áras számlázási módszerrel rendelkező alvállalkozói szerződéssor meghatározhat egy mérföldkő alapú számlázási ütemtervet a szállítóval.

A szállítói számlázáshoz szükséges mérföldkövek automatikusan generálhatók egy meghatározott gyakorisággal, vagy manuálisan is létrehozhatók.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Automatikusan hozzon létre mérföldkő-alapú számlaütemezést egy alvállalkozói szerződéssorhoz

Végezze el a következő lépéseket, hogy automatikusan létrehozzon egy mérföldkő-alapú számlaütemezést egyenletesen elosztott mérföldkövek rögzített halmazához.

1. Menjen a **Beállítások** > **Számlázási gyakoriságok** menüpontba, és állítsa be a számlázási gyakoriságot az alvállalkozói szerződéssorokhoz.
2. Nyissa meg az **Alvállalkozói szerződések** oldalt, nyissa meg azt az alvállalkozói szerződést, amellyel dolgozni szeretne, majd nyissa meg azt a fix áras alvállalkozói szerződéssort, amelyhez mérföldkő-ütemtervet fog készíteni.
3. Az **Alvállalkozói szerződés sor Mérföldkövek** lapján válassza az **Időszakos mérföldkövek generálása** lehetőséget.
4. A párbeszédpanelen adja meg vagy válassza ki a dátumtartományt, a mérföldkövek számát és a számlázás gyakoriságát. Kiválaszthatja a kezdeti dátumot, vagy kiválaszthatja a mérföldkövek számát és a számlázás gyakoriságát vagy a kezdeti dátumot, vagy kiválaszthatja a végdátumot és a számlázás gyakoriságát. Nem választhatja ki a végdátumot és a mérföldkövek számát.
Ezen információk felhasználásával a rendszer mérföldköveket és rekordokat generál, amelyek a **Mérföldkövek** rácson jelennek meg.

   - **Mérföldkő neve** - A mérföldkő neve a számla gyakorisága alapján a mérföldkő dátumára van beállítva.
   - **Mérföldkő dátuma** - A számla gyakoriságán alapuló dátum.
   - **Mérföldkő-összeg** - Az alvállalkozói szerződés sorában szereplő részösszeg és a mérföldkövek számának elosztásával kerül kiszámításra.

Ha az alvállalkozói szerződés sorában a **Becsült adóösszeg** mezőben van érték, akkor ez az érték az időszakos mérföldkövek generálásakor minden egyes mérföldkőhöz egyenlő mértékben hozzáadódik.

Az alvállalkozói szerződéssor mérföldköveinek összegének meg kell egyeznie az alvállalkozói szerződéssor értékével. Ha nem egyenlőek, hiba történik. A hibát a mérföldkő- és adóösszegek létrehozásával, szerkesztésével vagy törlésével javíthatja, és ellenőrizheti, hogy a mérföldkőösszeg megegyezik-e az alvállalkozói szerződés sorának értékével. A módosítások elvégzése után mentse el és frissítse az oldalt, hogy megbizonyosodjon arról, hogy nincs több hiba.

## <a name="manually-create-subcontract-line-milestones"></a>Alvállalkozói szerződéssorok mérföldköveinek manuális létrehozása

A fix áras mérföldkövek egy alvállalkozói szerződéssoron manuálisan generálhatók, ha nincsenek periodikusan felosztva. Egy alvállalkozói sor mérföldkő manuális létrehozásához végezze el a következő lépéseket.

1. A navigációs ablaktáblán válassza az **Alvállalkozói szerződések** elemet, és nyissa meg azt az alvállalkozói szerződést, amellyel dolgozni szeretne.
2. Nyissa meg azt a fix áras alvállalkozói szerződéssort, amelyhez mérföldkövet szeretne létrehozni.
3. Az **Alvállalkozói szerződés sor mérföldkövei** lapon az alrácson válassza a **+ Új alvállalkozói szerződés sor mérföldkő** lehetőséget.
4. Az **Új alvállalkozói szerződéssor mérföldkő** lapon adja meg a szükséges információkat az alábbi táblázat alapján.

    | Mező | Ismertetés |Funkcionális hatás|
    | --- | --- |----------------------|
    | Mérföldkő neve | A mérföldkő neve. |Ez lesz megjelenítve első oszlopként minden olyan keresésben, amelyek az alvállalkozói sor mérföldköveken alapulnak. Az ezen mérföldkő alapján létrehozott szállítói számlasor az alvállalkozói sor mérföldkövének nevét is használja a szállító számlasorának alapértelmezett neveként.|
    | Ismertetés | A mérföldkő leírása. |Az ezen mérföldkő alapján létrehozott szállítói számlasor az alvállalkozói sor mérföldkövének leírását is használja a szállító számlasorának alapértelmezett leírásaként.|
    | Mérföldkő dátuma | Az a dátum, amikor az automatikus számlakészítési folyamatnak meg kell keresnie ennek a mérföldkőnek az állapotát, hogy a számlázáshoz figyelembe vegye.| Ez az érték lesz a szállító számlasorának alapértelmezett dátuma az alvállalkozói sorhoz való számlázásakor. |
    | Mennyiség | Az ügyfélnek számlázandó mérföldkő összege vagy értéke. |Ez az érték lesz a szállító számlasorának alapértelmezett mennyisége az alvállalkozói sorhoz való számlázásakor. |
    | Adó | A mérföldkőre alkalmazott adó összege.| Ez az érték lesz a szállító számlasorának alapértelmezett adómennyisége az alvállalkozói sorhoz való számlázásakor. |
    | Adó utáni összeg | Ez a csak olvasható mező számítása Összeg + Adó.|Ez az érték lesz a szállító számlasorának alapértelmezettje az alvállalkozói sorhoz való számlázásakor. |
    | Számla állapota | A mérföldkő létrehozásakor ez a státusz mindig a **Nem áll készen a számlázásra** állapotra van beállítva.|  Ha a státusz **Számlázásra kész**, a szállítói számla létrehozása során ez a mérföldkő szerepel a szállítói számlán. |

5. Válassza a **Mentés és bezárás** lehetőséget.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
