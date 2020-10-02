---
title: Termékek
description: Ez a témakör az ügyfeleknek a termékekről és a szervezet árképzéséről információkat biztosító termékkatalógusra vonatkozó információkat tartalmaz.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 28397fd49ad4cdb2c820ef4b6f198f410995ba0f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898714"
---
# <a name="products"></a>Termékek

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A termékek adják az üzlet gerincét. A termékkatalógus a Dynamics 365 Sales Professional alkalmazásban termékek és árképzési adataik gyűjteménye. Könnyítse meg üzletkötőinek értékesítéseik növelését egy termékkatalógus gyors létrehozásával.

## <a name="add-a-product"></a>Termék felvétele

1.  Ügyeljen arra, hogy az értékesítési menezser szakember vagy a rendszergazda szerepkörrel rendelkezzen, így termékeket vehet fel a Dynamics 365 Sales Professional alkalmazásba.
2.  Az oldaltérképen a **Beállítás** alatt válassz a **Termékek** lehetőséget.
3.  Válassza a **Termék hozzáadása** lehetőséget, és adja meg a következő információkat:

    -  **Név**
    -  **Termékazonosító**
    -  **Szülő**: Válasszon szülő termékcsaládot a termékhez. Ha egy termékcsaládban gyermek terméket hoz létre, a szülő termékcsalád neve itt szerepel. Ez a rekord mentése után nem módosítható.
    -  **Érvényesség kezdete**/**Érvényesség vége**:  az **Érvényesség kezdete** és az **Érvényesség vége** mezőkkel adhatja meg az időtartamot, ameddig egy termék érvényes.
    -  **Kiszereléscsoport**: Válasszon egy kiszereléscsoportot. Az egységcsoport azoknak a különböző egységeknek a gyűjteménye, amelyekben a terméket értékesítik, és azt határozza meg, hogy hogyan vannak az egyes elemek nagyobb mennyiségbe összecsoportosítva. Például a vetőmagok termékként történő hozzáadásakor, valószínűleg létrehozta a „Vetőmagok” nevű egységcsoportot, és elsődleges egységeként a „Csomag” egységet határozta meg.
    -  **Alapértelmezett kiszerelés**: a termék értékesítéséhez leggyakrabban használt kiszerelés kiválasztása. Az egység az a mértékegység, amiben a terméket értékesíti. Például amennyiben a vetőmagokat termékként adja hozzá, értékesítheti őket csomagonként, dobozonként vagy raklaponként. Ezek mindegyike a termék egyik egysége. Ha a vetőmagokat többnyire csomagban értékesítik, ezt adja meg egységként.
    -  **Alapértelmezett árlista**: ha új termékről van szó, akkor ez a mező írásvédett. Az alapértelmezett árlista kijelölése előtt az összes kötelező mezőt ki kell töltenie, és mentenie kell a bejegyzést. Annak ellenére, hogy az alapértelmezett árlistát nem kötelező megadni, a bejegyzés mentését követően érdemes megadni minden termék alapértelmezett árlistáját. Ezután, ha egy ügyfélbejegyzés nem tartalmaz árlistát, akkor a Sales az alapértelmezett árlistát használhatja az ajánlatok, megrendelések és számlák létrehozásához.
    -  **Használható tizedesek**: adjon meg 0 és 5 közötti egész számot. Ha a termék nem darabolható, akkor nullát adjon meg. A rendszer az ebbe a mezőbe beírt érték alapján ellenőrzi az ajánlaton, a megrendelésen vagy a számlán szereplő termékbejegyzés **Mennyiség** mezője tizedesjegyeinek a számát, ha nincs a termékhez árlista társítva.
    -  **Tárgy**: Társítsa a terméket egy tárggyal. A tárgyak segítségével kategorizálhatja a termékeket, és szűrheti a jelentéseket.

4.  Válassza a **Mentés** parancsot.
5.  A **További részletek** lap **Árlista elemei** szakaszában válassza a **További parancsok**, majd az **Új árlistaelem hozzáadása** lehetőséget.
7.  A **További részletek** lap **Termékkapcsolat** szakaszában kattintson a **További parancsok** ikonra, majd válassza az **Új termékkapcsolat hozzáadása** lehetőséget.
8.  Az **Új termékkapcsolat** űrlapon, adja meg a következő részleteket, és válassza ki a parancssávon a **Mentés és bezárás** parancsot:

    -   **Kapcsolódó termék**: Válasszon egy olyan terméket, amelyet kapcsolódó termékként kíván hozzáadni ahhoz a termékhez, amellyel éppen dolgozik.
    -   **Értékesítési kapcsolat típusa**: Válassza ki, hogy a terméket felülértékesítési, keresztértékesítési vagy helyettesítési termékként, illetve tartozékként kívánja hozzáadni.
    -   **Irány**: Válassza ki, hogy a termékek közötti kapcsolat egyirányú vagy kétirányú legyen. Ha az egyirányú lehetőséget választja, a **Kapcsolódó termék** mezőben kiválasztott termék megjelenik ajánlásként a meglévő termékhez, de fordítva nem.

9.  A termék űrlapon válassza a **Mentés**lehetőséget.

## <a name="import-products"></a>Termékek importálása

Az importálási sablonok segítségével tömegesen viheti be a termékadatokat a Dynamics 365 Sales rendszerbe.

## <a name="revise-a-product"></a>Egy termék felülvizsgálata

Tartsa termékleltárát frissítve a tulajdonságok szükség szerinti gyors felülvizsgálatával, és az információk közzétételével, így az értékesítési ügynökök láthatják a készet legújabb módosításait.

1.  Ügyeljen rá, hogy rendszergazda, rendszertestreszabó, értékesítési menedzser, értékesítési alelnök, marketingalelnök vagy vezérigazgató biztonsági szerepkörrel vagy hasonló engedélyekkel rendelkezzen.
2.  Az Oldaltérképen válassza a **Termékek** lehetőséget.
3.  Nyissa meg a módosítani kívánt aktív terméket, majd a parancssávon válassza a **Felülvizsgálat**lehetőséget.
4.  A **Felülvizsgálat megerősítése** párbeszédpanelen válassza a **Megerősítés** elemet. Ez a művelet módosítja a termék állapotát **Felülvizsgálat alatt** értékűre.
5.  A változtatások végrehajtása után a parancssorban válassza a **Közzététel** lehetőséget.

    > [!TIP]
    > A változtatások visszaállításához és a termék utolsó aktív verziójával való folytatáshoz válassza a **Visszaállítás** lehetőséget. Ez visszaváltoztatja a termék állapotát **Aktív** értékűre.

## <a name="clone-a-product"></a>Termék klónozása 

Ha új terméket hoz létre, időt takaríthat meg azzal, hogy egy meglévőt klónoz. Ezzel az eredeti rekord egy példányát hozza létre, amelyben – a név és az azonosító kivételével – minden részlet azonos.

1.  Ügyeljen rá, hogy rendszergazda, rendszertestreszabó, értékesítési menedzser, értékesítési alelnök, marketingalelnök vagy vezérigazgató biztonsági szerepkörrel vagy hasonló engedélyekkel rendelkezzen.
2.  Az Oldaltérképen válassza a **Termékek** lehetőséget.
3.  Jelölje ki azt a termékcsaládot, amelyet klónozni kíván, majd a parancssávon válassza a **Klónozás** lehetőséget. Megjelenik a jóváhagyást kérő párbeszédpanel.
4.  Válassza a **Megerősítés** elemet.

Ekkor megnyílik az új termékbejegyzés, amelynek részletei – a név és az azonosító kivételével – megegyeznek az eredetiével.

## <a name="retire-a-product"></a>Termék eltávolítása 

Ha szervezete már nem értékesít egy terméket, vezesse ki azt, hogy többé ne legyen elérhető az értékesítési ügynökei számára.

1.  Ügyeljen rá, hogy rendszergazda vagy Sales Professional menedzser biztonsági szerepkörrel vagy hasonló engedélyekkel rendelkezzen.
2.  Az Oldaltérképen válassza a **Termékek** lehetőséget.
3.  Nyissa meg az eltávolítani kívánt aktív terméket, majd a parancssávon válassza az **Eltávolítás**lehetőséget.
4.  A **Kivezetés megerősítése** párbeszédpanelen válassza a **Megerősítés** elemet.


## <a name="delete-a-product"></a>Termék törlése

Egy termék eladásának leállításához törölje azt.

> [!IMPORTANT]
> A törölt rekordok nem állíthatók vissza.

1.  Ügyeljen rá, hogy rendszergazda vagy Sales Professional menedzser biztonsági szerepkörrel vagy hasonló engedélyekkel rendelkezzen.
2.  Az Oldaltérképen válassza a **Termékek** lehetőséget.
3.  Jelölje ki azt a termékcsaládot, amelyet törölni kíván, majd a parancssávon válassza a **Törlés** lehetőséget.
4.  A **Törlés megerősítés** párbeszédpanelen válassza a **Folytatás** lehetőséget.
 
 ## <a name="quantity-factors-for-products"></a>A termékek mennyiségi tényezői

A mennyiségi tényezők támogatják az előfizetésen alapuló termékek értékesítését. Az előfizetésen alapuló termékek esetében az árajánlat vagy a projektszerződés sorában szereplő mennyiséget a felhasználói/hónap számában fejezik ki.

Az előfizetési szoftver ára általában a katalógusban kerül tárolásra havi felhasználónkénti árként. Ehelyett más időleírásokat is használhat. Az értékesítési folyamat során az árajánlatsorban a felhasználónkénti havi ár általában az IT-értékesítési ügynökkel való egyeztetés után és az általa megadott árengedménnyel születik meg. Minden egyes ügyletnek eltérő felhasználói száma és előfizetési hónapjai vannak. Az árajánlatsor összegének kiszámításához használt mennyiség a felhasználók számának és az előfizetési hónapoknak a szorzata.

A mennyiségi tényezők a termékattribútumokra támaszkodnak. Amikor egy adott termék tulajdonságait konfigurálja, mennyiségi tényezőként jelölheti meg ezen tulajdonságok egy részhalmazát vagy az összes tulajdonságot.

A rendszer ellenőrzi, hogy csak a numerikus vagy a numerikus adattípusú termékjellemzőket jelölte-e meg mennyiségi tényezőként. Ha egy termék, amelynek mennyiségi tényezőit konfigurálják, hozzáadásra kerül egy árajánlatsorhoz, az árajánlatsor **Mennyiség** mezője „csak olvasható” mező lesz. Miután megadta azon terméktulajdonságok értékeit, amelyek mennyiségi tényezők, a rendszer kiszámítja az árajánlatsor mennyiségét.

A következő tulajdonságok esetén például: 

- **Felhasználók száma**: A felhasználók száma 
- **Hónapok száma**: Az előfizetési hónapok száma
- **Termék cikkszáma** 

A **Felhasználók száma** és a **Hónapok száma** tulajdonságok megjelölhetők mennyiségi tényezőként a terméksor tulajdonságainak szerkesztésével. 
