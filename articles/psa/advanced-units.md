---
title: Egységcsoportok és egységek
description: Ez a témakör az egységcsoportokról és egységekről tartalmaz információkat.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6620c99563394d1f3881d6bfdb72d01c1c4e8d6f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145586"
---
# <a name="unit-groups-and-units"></a>Egységcsoportok és egységek

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Az egységcsoportok és egységek a Microsoft Dynamics 365 alapentitásai. A egység egyetlen mértékegység, az egységek pedig egységcsoportokba csoportosíthatók. Az egység-csoportokat időnként a Dynamics 365 felhasználói felülete (UI) egységütemezésének is nevezik. 

Íme néhány példa egységekre és egységcsoportokra:
 
- **Egységcsoport**: Távolság 
    - **Egységek**: Mérföld, kilométer stb.
- **Egységcsoport**: Idő
    - **Egységek**: Óra, nap, hét stb. 

Ha egy egységcsoporthoz több egységet állít be, akkor a köztük érvényes átváltási tényezőt is be kell állítania az egységcsoport alapértelmezett vagy elsődleges egységeként beállított egység kijelölésével. 

Például ha az **Idő** egységcsoportban az **Óra** egységet állítja be elsődlegesként, a rendszer az **Óra** mértékegységet állítja be alapértelmezettként. Ha a következő beállított egység a **Nap**, akkor be kell állítania a **Nap** és **Óra** közötti átváltási tényezőt. Ha ezután a **Hét** mértékegységet adja hozzá harmadikként, akkor a **Hét** és a **Nap**, valamint az **Óra** közötti átváltási tényezőket is be kell állítania. 

A következő képen a **Nap** mértékegységre vonatkozó példa látható, ahol a **Mennyiség** mező az egy napon belüli órák számát mutatja, a **Hét** mértékegységre vonatkozó példa esetén pedig a **Mennyiség** mező mutatja az egy héten belüli napok számát.

> ![Egységcsoport: Információs oldal](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Egységek és egységcsoportok használata

A Dynamics 365 Project Service Automation az egységeket és egységcsoportokat a becslések és bejegyzések feldolgozásához használja mind a költségekre, mint az időre vonatkozóan. 

A költségek esetén minden költségkategóriához tartozik alapértelmezett egységcsoport és egység. Ezek az értékek alapértelmezett értékként szerepelnek az árlista-bejegyzésekben, a költségkategóriákra vonatkozóan. 

Vegyünk egy példát, amelyben van egy **Megtett távolság** nevű költségkategóriája. Ennek van egy **Távolság** nevű egységcsoportja, amelyben van egy **Mérföld** nevű alapértelmezett egység. Ha a **Távolság** egységcsoportot úgy állítja be, hogy két egységgel rendelkezzen (**Mérföld** és **Kilométer**), akkor kér árat állíthat be a **Megtett távolság** kategóriához egy árlistán: ár/mérföld és ár/kilométer.

| Költségkategória  | Egységcsoport  | Egység      | Árképzési mód  | Kiszerelésenkénti ár  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Távolság           | Távolság      | mérföld      | Kiszerelésenkénti ár    | 10 USD            |
| Távolság           | Távolság      | kilométer | Kiszerelésenkénti ár    |  6 USD            |

Amikor megad egy költséget egy projekthez, a rendszer a kategória és a költség szerinti egység kombinációja alapján meghatározza az árat. 

| Költség leírása        | Költségkategória  | Egység  | Mennyiség  | Egységár   |
|----------------------------|---------------------|-------|-----------|----------------|
| Az ügyfélhez autózás | Távolság             | mérföld  | 10        | 10 USD         |

Az idő esetén minden árlista fejlécében van egy **Alapértelmezett időegység** mező. Az érték az árlista fejlécének létrehozásakor állítható be. Ezzel az egységgel az adott árlista összes szerepkörön alapuló árát beállíthatja.

Az **Árajánlatra vonatkozó idő** mező becsléssorai tetszőleges időegységben megadhatók. A projektek és időbejegyzések becsléssorai azonban csak az **Óra** időegységét tudják használni. Ha az időbejegyzések vagy a becsléssorok egysége nem egyezik meg az adott szerepkörhöz tartozó árlista sorában szereplő egységgel, akkor a rendszer az árat a projektbecslésében vagy a projekt tényleges tranzakcióinál meghatározott egységekre váltja át.

A következő példa azt mutatja be, hogyan használja a PSA az egységcsoportokat, egységeket és átváltási tényezőket.
- Egységek

   - **Egységcsoport**: Idő 
   - **Egységek**: Óra 
    
    - **Nap** – Átváltási tényező: 8 óra       
    - **Hét** – Átváltási tényező: 40 óra  
        
- Árlista beállítása az A projektnél:

    - **Név**: Egyesült Királyság árazás 2016 
    - **Alapértelmezett időegység**: nap 
    - **Pénznem**: GBP

| Szerepkör      | Egységcsoport | Egység | Szervezeti egység | Ár   |
|-----------|------------|------|---------------------|---------|
| Fejlesztő | Time       | Day  | Contoso UK          | 800 GBP |

### <a name="time-entry"></a>Időbejegyzés

A következő táblázat bemutatja a PSA által létrehozott, három órás projekthez tartozó értékesítési oldali tranzakciót.


| Projekt   | Feladat    | Szerepkör      | Mennyiség | Egység  | Egységár | Számlázatlan értékesítési összeg |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| „A” projekt | Tervezés  | Fejlesztő | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Időegység GYIK

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>A PSA átváltja a különböző egységeket a kiadások esetén?
Szám Az egység átalakítása csak az időre vonatkozóan működik. A költségek esetén, ha a rendszer nem találja a költségkategória és egység kombinációjának árát, az ár alapértelmezés szerint 0,00 lesz.

### <a name="why-does-psa-convert-time-units"></a>Miért váltja át a PSA az időegységeket?
Egyes országokban és régiókban jogi követelmény, hogy a számlázási díj napokban legyen megadva. Az árak egyeztetése és az engedmény az árajánlati ciklus során az egyes számlázható szerepkörök napi árfolyamának felhasználásával történik. Az ütemezés becslése és az időbejegyzések órában vannak megadva. Az időegységek közötti különbség támogatásához a PSA átalakítja az időegységeket.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Módosíthatók az időegységek a projektbecsléseknél?
Szám Az ütemezési becslés jelenleg órákra van korlátozva, és nem módosítható.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Lehet szerkeszteni, törölni és hozzáadni az egységeket és egységcsoportokat?
Igen. Az **Idő** egységcsoport és az **Óra** egység kivételével az összes egység törölhető vagy szerkeszthető, és új egységek is hozzáadhatók. A PSA-ban az **Idő** egységcsoport és az **Óra** egység nem törölhető. Ezek azonban frissíthetők a **Név** mező lefordított szövegével.


[!INCLUDE[footer-include](../includes/footer-banner.md)]