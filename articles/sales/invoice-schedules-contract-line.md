---
title: Számlaütemezés létrehozása egy projektalapú szerződéssoron
description: Ez a cikk arról nyújt tájékoztatást, hogyan hozhat létre számlaütemezéseket és mérföldköveket a szerződéssorokon.
author: rumant
ms.date: 10/17/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 490a61b67f54bdad95ecfce905191c381dddc85b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915003"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Számlaütemezés létrehozása egy projektalapú szerződéssoron 

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Immár létrehozhat egy számlázási ütemezést egy projektalapú szerződéssorhoz. A számlázás csak a szerződés megnyerése után engedélyezett, amikor egy projektszerződést hoz létre. A számla ütemezése lehetővé teszi, hogy a projekt alapú szerződéssorokhoz automatikusan létrejöjjenek a számlavázlatok. Ha azonban csak manuálisan hoz létre számlákat, akkor kihagyhatja a számlázási ütemezések létrehozását a szerződéssorokon.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Idő- és anyagelszámolású számlaütemezés létrehozása szerződéssorhoz

Amikor a szerződéssor számlázási módja Idő és anyag típusú móddal rendelkezik, létrehozhat dátumalapú számlaütemezést. Ha automatikusan szeretne létrehozni egy dátumalapú számlaütemezést, hajtsa végre az alábbi lépéseket.

1. Válassza a **Beállítások** > **Számlázási gyakoriság** lehetőséget, és állítson be egy számlázási gyakoriságot.
2. Nyissa meg a projektszerződés-rekordot és az **Összesítés** lapon a **Kért szállítási dátum** mezőben jelöljön ki egy dátumot.
3. Nyissa meg azt az **Idő-és anyag** szerződéssort, amelyhez dátumalapú számlaütemezést hoz létre. 
4. A **Számlaütemezés** lapon válassza ki a számlázás kezdete és a számlázási gyakoriság elemeket.
5. Az alrácson válassza a **Számlaütemezés előállítása** lehetőséget. Az számlaütemezés létre lesz hozva a **Számlakészítés dátuma**, a **Tranzakció határideje** és a **Futtatás állapota** mezőket a következő módon beállítva:

    - A **Számlakészítés dátuma** Ezt számla gyakorisága által meghatározott dátuma határozza meg.
    - A **Tranzakció határideje**: A Számlakészítés dátuma előtti nap.
    - A **Futtatás állapota** Beállítás automatikusan a **Nem fut** értékre van beállítva. Amikor az automatikus számlalétrehozási feladat egy bizonyos számlázási futtatási dátumnál fut, akkor a program a **Futtatás sikerült** vagy a **Futtatás nem sikerült** értékre módosítja majd a mezőt.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Rögzített áras számlaütemezés létrehozása szerződéssorhoz

Ha a szerződéssor rögzített számlázási móddal rendelkezik, akkor mérföldkőre épülő számlaütemezést hozhat létre. 

> [!NOTE]
> Nem hozhatók létre mérföldkövek a szerződéssorokon, ha nincs projekt leképezve a szerződéssorhoz.

Hajtsa végre az alábbi lépéseket, egy mérföldkő alapú számlaütemezés létrehozásához mérföldkövek egy rögzített, a naptári időszakra egyformán elosztott készletéhez.

1. Válassza a **Beállítások** > **Számlázási gyakoriság** lehetőséget, és állítson be egy számlázási gyakoriságot.
2. Nyissa meg a projektszerződés-rekordot és az **Összesítés** lapon a **Kért szállítási dátum** mezőben jelöljön ki egy dátumot.
3. Nyissa meg azt a **Rögzített áras** szerződéssort, amelyhez mérföldkő-ütemezést hoz létre. A **Számlázási mérföldkövek** lapon válassza ki a számlázás kezdete és a számlázási gyakoriság elemeket. 
4. Az alrácson válassza az **Időszakos mérföldkövek létrehozása** lehetőséget. A számla ütemezése a **Mérföldkő neve**, a **Mérföldkő dátuma** és a **Mérföldkő összege** mezőket a következőképpen jön létre:

    - **Mérföldkő neve**: Ezt a nevet a számla gyakorisága határozza meg.
    - A **Mérföldkő dátuma**: Ezt számla gyakorisága által meghatározott dátuma határozza meg.
    - **Mérföldkő összege**: Ezt az összeget úgy számítja ki a program, hogy a szerződéssoron szereplő szerződéses összeget elosztja a mérföldköveknek a gyakoriság, valamint a számlázás kezdete és a kért szállítási dátumok által megkövetelt számával.

    Ha a szerződéssor értéke a **Becsült adóösszeg** mezőben van, akkor ez a mező a periodikus mérföldkövek létrehozásakor egyenletesen lesz hozzárendelve az egyes mérföldkövekhez.

A számlázási mérföldköveknek meg kell egyezniük a szerződéssor szerződéses értékével. Ha nem, akkor hibaüzenet jelenik meg a **Szerződéssor** lapon. A hiba kijavításához ellenőrizze, hogy a számlázási mérföldkövek összege megegyezzen-e a sor szerződött értékével a mérföldkövek létrehozásával, szerkesztésével vagy törlésével. A módosítások elvégzése után frissítse a lapot a hiba eltávolításához.

### <a name="manually-create-milestones"></a>Mérföldkövek manuális létrehozása

A rögzített árú mérföldköveket létrehozhat manuálisan is, ha nem időszakosan vannak felosztva. A következő lépések elvégzésével manuálisan hozhat létre mérföldkövet.

1. Nyissa meg azt a rögzített árú szerződéssort, amelyhez mérföldkövet hoz létre, és a **Számla ütemezése** lap alrácson válassza az **+ Új szerződéssor mérföldkő létrehozása** lehetőséget. 
2. A **Mérföldkő létrehozása** lapon írja be a következő táblázat alapján a szükséges adatokat.

| Mező | Hely | Adatfolyam leírása | Alsóbb rétegbeli hatás |
| --- | --- | --- | --- |
| Mérföldkő neve | Gyorslétrehozás | A mérföldkő nevének szövegmezője. | Ez továbbvitelre kerül a projekt szerződéssor-mérföldkövéhez és a számlához. |
| Projektfeladat | Gyorslétrehozás | Ha a mérföldkő a projektfeladathoz van kötve, ezzel a hivatkozással egyéni logikát adhat hozzá a feladat állapota alapján a megadott mérföldkő-állapothoz. | Az alkalmazásnak nincs hatása alsóbb rétegekben ennek a feladathivatkozásnak az esetében. |
| Mérföldkő dátuma | Gyorslétrehozás | Állítsa be azt a dátumot, amikor az automatikus számlalétrehozási folyamatának keresnie kell a mérföldkő állapotát, hogy figyelembe vegye a számlázás szempontjából. | Ez továbbvitelre kerül a projekt szerződéssor-mérföldkövéhez és a számlához. |
| Számla állapota | Gyorslétrehozás | Mérföldkő létrehozásakor az állapot mindig a **Nem kész a számlázásra** vagy **Nem elkezdett** állapotra van beállítva. | Ez továbbvitelre kerül a projekt szerződéssor-mérföldkövéhez és a számlához. |
| Sor összege | Gyorslétrehozás | Az ügyfélnek számlázott mérföldkő összege vagy értéke. | Ez továbbvitelre kerül a projekt szerződéssor-mérföldkövéhez és a számlához. |
| Adó | Gyorslétrehozás | A mérföldkőre alkalmazott adó összege. | Ez továbbvitelre kerül a projekt szerződéssor-mérföldkövéhez és a számlához. |

3. Válassza a **Mentés és bezárás** lehetőséget.


[!INCLUDE[footer-include](../includes/footer-banner.md)]