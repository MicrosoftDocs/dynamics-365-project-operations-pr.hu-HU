---
title: Projektalapú proforma számla kezelése
description: Ez témakör a proforma projektalapú számlák kezeléséről használatáról nyújt információt.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b1b0f70f25d157e1d7e2d14dc011a048d698d299
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012544"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Projektalapú proforma számla kezelése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A Dynamics 365 Project Operations alkalmazásban a proforma számlák a Dynamics 365 Salesben szereplő számlák bővítményeként jönnek létre. A számlázás során azonban számos különbség van a számlázási folyamatban a Sales és a Project Operations között. Például nem lehet új számlát létrehozni a Project Operations **Számlák listája** oldaláról, de a Salesben igen. Ezek a különbségek és bővítmények olyan projektek számlázási folyamatainak támogatásához szükségesek, amelyek eltérnek az értékesítési rendelések tipikus számláitól.

> [!IMPORTANT]
> A különbségek miatt a számlák nem használhatók fel egymás helyettesítéseként a Sales és a Project Operations szolgáltatásban.

## <a name="invoice-header"></a>Számlafejléc

A következő információ egy proforma számla fejlécében érhető el a Project Operations alkalmazásban.

| Mező | Hely | Ismertetés |
| --- | --- | --- | 
| **Számlaazonosító** | **Összegzés** lap | A rendszer által létrehozott azonosító automatikusan a proforma számla létrehozásakor. Írásvédett mező, amely a szerkesztéstől le van zárva. Ez a mező az egyes proforma számlákra vonatkozó hivatkozásként használatos. |
| **Név** | **Összegzés** lap | Beállítva alapértelmezés szerint a projektszerződés nevére. Ez a mező szerkeszthető. | 
| **Pénznem** | **Összegzés** lap | Beállítva alapértelmezés szerint a projektszerződés pénznemére. Írásvédett mező, amely a szerkesztéstől le van zárva. |
| **Árlista** | **Összegzés** lap | Beállítva alapértelmezés szerint a projektszerződés árlistájára. Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Lehetőség** | **Összegzés** lap | A csatolt lehetőségre mutató hivatkozás. Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Szerződés** | **Összegzés** lap | A kapcsolt projektszerződésre mutató hivatkozás. Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Ügyfél** | **Összegzés** lap | A kapcsolt projektszerződésre mutató hivatkozás. Írásvédett mező, amely a szerkesztéstől le van zárva. |
| **Leírás** | **Összegzés** lap | A számlát leíró szöveges mező. Ez a mező szerkeszthető. | 
| **Számlázási cím** és kapcsolódó mezők | **Összegzés lap** | Az alapértelmezett értékeket a projektszerződés ügyfeléből állítják be. Ez a mező szerkeszthető.  | 
| **Állapot** | **Összegzés** lap | A következő beállításokat állítja be: **Aktív**, **Lezárt**, **Fizetett** és **Visszavonva**, illetve szerkeszthető. A Project Operations nem támogatott állapotai: **lezárt** és **visszavont** állapotú. </br> A számla létrehozásakor a állapot **Aktív** értékre van állítva. </br>Az állapotot csak a számla megerősítését követően kell **Fizetett** állapotra állítani.  | 
| **Projektszámla állapota** | **Összegzés** lap | A következő beállításokat állítja be: **Piszkozat**, **Ellenőrzés alatt**, **Megerősítve**, illetve szerkeszthető. A számla a **Piszkozat** és a **Felülvizsgálat alatt** állapotokban is szerkeszthető. A számla a megerősítést követően nem módosítható. | 
| **Részletmennyiség** | **Összegzés** lap | Az összes számlasor összegének összege az előlegek és a levonások után. Írásvédett mező, amely a szerkesztéstől le van zárva.  Ez a mező a végső összeg kiszámításához használható. | 
| **Engedmény (%)** | **Összegzés** lap | Ez a mező módosítható, ha meg szeretné adni az engedmény százalékát. A Project Operations működése nem támogatja ezt a mezőt. Ez egy nem támogatott mező.|  
| **Árengedmény összege** | **Összegzés** lap | Ez a mező módosítható, ha meg szeretné adni az engedmény összegét. A Project Operations működése nem támogatja ezt a mezőt. Ez egy nem támogatott mező. |  
| **Szállítás előtti összeg** | **Összegzés lap** | A teljes számlaösszeg a kedvezmények után. Írásvédett mező, amely a szerkesztéstől le van zárva. Ez a mező a végső összeg kiszámításához használható.  | 
| **Szállítási mennyiség** | **Összegzés** lap | Ez a mező módosítható, ha meg szeretné adni a szállítási összeget. A Project Operations működése nem támogatja ezt a mezőt. Ez egy nem támogatott mező. |
| **Összes adó** | **Összegzés** lap | A számlán szereplő összes számlasor teljes összege. Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Teljes összeg** | **Összegzés** lap | Az engedmények és az adók utáni végösszeg. A végösszeg az az összeg, amelyet az ügyfélnek ki kell fizetnie. | 

## <a name="project-based-invoice-lines"></a>Projektalapú számlasorok

A Project Operationsban mindig tartozik egy számlasor minden projektszerződéssorhoz. A számlasor akkor is létrejön, ha nincsenek tényleges adatok. A következő információ egy proforma számla sorában érhető el.

| Mező | Hely | Ismertetés | 
| --- | --- | --- |
| **Számlaazonosító** | **Általános** lap | A számla azonosítójára vonatkozó hivatkozás. Írásvédett mező, amely a szerkesztéstől le van zárva. A számlaazonosító hivatkozás segítségével visszatérhet a számla fejlécéhez. | 
| **Név** | **Általános** lap | A számlasor neve alapértelmezés szerint a szerződéssor nevéből van beállítva. Ez a mező szerkeszthető. |
| **Project** | **Általános** lap | A projekt a kapcsolódó projektszerződéssorban. Írásvédett mező, amely a szerkesztéstől le van zárva. A projekthivatkozás segítségével léphet a projektre. | 
| **Számlázási mód** | **Általános** lap | A számlázási mód a kapcsolódó projektszerződéssorban. Írásvédett mező, amely a szerkesztéstől le van zárva. |
| **Szerződéssor összege** | **Általános** lap | A kapcsolódó projektszerződéssor szerződéses összege. Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Kiszámlázva eddig** | **Általános** lap | Az összegek végösszege az adott számla minden számlasoradatában. Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Összeg** | **Általános** lap | Az összegek végösszege az adott számla minden számlázható számlasoradatában. Írásvédett mező, amely a szerkesztéstől le van zárva. Ez a mező a végső összeg kiszámításához használható a számlafejlécben. | 
| **Adó** | **Általános** lap | Az adóösszegek végösszege az adott számlasor minden számlasoradatában. Írásvédett mező, amely a szerkesztéstől le van zárva. Ez a mező a végső adóösszeg kiszámításához használható a számlafejlécben. | 
| **Kibővített összeg** | **Általános** lap | A teljes összegek végösszege (**Adó + összegek**) az adott számlasor minden számlázható számlasoradatában. Írásvédett mező, amely a szerkesztéstől le van zárva. Ez a mező a végső összeg kiszámításához használható a számlafejlécben. |

## <a name="invoice-line-details"></a>Számlasor részletei

A projekt számláján szereplő minden számlasor tartalmazza a számlasor részleteit. Ezek a soradatok a számla sorában hivatkozott, a szerződéssorhoz kapcsolódó, nem számlázott értékesítési tényadatokkal és mérföldkövekkel kapcsolatosak. Az összes ilyen tranzakcióhoz **Számlázásra kész** jelölést kell alkalmazni.

Az **Idő- és anyagszámla** sor esetén a számlasor részletei a **Számalsor** lap **Felszámítható**, **Nem felszámítható** és **Kiegészítő** lehetőségekbe vannak csoportosítva. A **számlázható számlasorok** részleteinek összegzése adja a számlasor összesítését. Az **Ingyenes** és a **Nem számlázható tényadatok** nem számítanak bele a számlasor összegébe.

**Rögzített árú számla** sor esetén a számlasor részletei olyan mérföldkövekből jönnek létre, amelyek a kapcsolódó szerződéssoron **Számlázásra kész** jelöléssel vannak ellátva. Miután a számlasor részletei egy mérföldkőből származnak, a mérföldkő számlázási állapota **Ügyfélszámla létrehozva** értékre frissül.

### <a name="edit-invoice-line-details"></a>Számlasorrészletek szerkesztése

A következő mezők a számlasor részletes adatain láthatók, amelyeket a rendszer nem számlázott értékesítési tényadattal támogat.

| Mező | Ismertetés |
| --- | --- | 
| **Számlasor** | A **számla azonosítójára** vonatkozó hivatkozás. Ez a mező írásvédett és nem szerkeszthető. Ez a hivatkozás segítségével visszatérhet a számla fejlécéhez. | 
| **Leírás** | A számlasoradat leírását. Beállítva alapértelmezett módon a **Belső megjegyzések** mezőből az **Időbejegyzés** menüpontban, és a **Leírás** mezőből a **Költségbejegyzés** menüpontban. A mező szerkeszthető.| 
| **Külső leírás** | A számlasoradat leírását. Beállítva alapértelmezett módon a **Külső megjegyzések** mezőből az **Időbejegyzés** menüpontban, és a **Leírás** mezőből a **Költségbejegyzés** menüpontban. A mező szerkeszthető. A Leírás segítségével megállapítható, hogy mi legyen az ügyfélnek küldendő nyomtatott számlán. A Project Operationsban a proforma-számla nem rendelkezik az összes szükséges funkcióval a számla nyomtatási beállításainak konfigurálásához. | 
| **Kezdő dátum** | Ez egy írásvédett mező, amely alapértelmezés szerint az erőforrás tényadatból állítható be. |
| **Project** | Ez egy írásvédett mező, amely alapértelmezés szerint a tényleges forrástól a projektig van beállítva a kapcsolódó szerződéssoron. |  
| **Feladatok** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. |
| **Tranzakció kategóriája** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Szerepkör** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. |  
| **Lefoglalható erőforrás** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Erőforrás-kezelő vállalat** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Erőforrás-kezelő részleg** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Mennyiség** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. |  
| **Egységütemezés** | Az időre vonatkozó számlasoradatoknál ez a beállítás értéke mindig idő, és nem szerkeszthető. A költségek esetében ez alapértelmezés szerint a forrás költségének tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Kiszerelés** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. |  
| **Ár** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. |
| **Pénznem** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Mennyiség** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Adó** | Alapértelmezés szerint a forrás tényleges értékét adja meg. A mező szerkeszthető.| 
| **Kibővített összeg** | Számított mező, kiszámítása: **Összeg + Adó**. Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Számlázási típus** | Alapértelmezés szerint a forrás tényleges értékét adja meg. A mező szerkeszthető. A **Számlázható** lehetőség kiválasztásával hozzáadja a sort a számlasor végösszegéhez. A **Kiegészítő** és a **Nem számlázható** kizárja az értéket a számlasor összegéből.| 
| **Termék kiválasztása** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. |
| **Termék** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Terméknév** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. |  
| **Nem katalogizált leírás** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. |
| **Tranzakció típusa** | Ez egy írásvédett mező, amely alapértelmezés szerint az erőforrás tényadatból **Számlázott értékesítés** értékre van beállítva. |  
| **Tranzakcióosztály** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | 

A következő mezők a számlasor részletes adatain láthatók, amelyeket a rendszer mérföldkővel támogat.

| Mező | Ismertetés |
| --- | --- | 
| **Számlasor** | A **számlasor azonosítójára** vonatkozó hivatkozás. Írásvédett mező, amely a szerkesztéstől le van zárva. A hivatkozás segítségével visszatérhet a számla fejlécéhez.  | 
| **Leírás** | A számlasoradat leírása. Alapértelmezés szerint a forrás mérföldkő leírásából van beállítva. | 
|**Külső leírás** | A számlasoradat leírása, amely alapértelmezés szerint a forrás mérföldkő leírásából van beállítva. Az adott mező segítségével megállapítható, hogy mi legyen az ügyfélnek küldendő nyomtatott számlán. A Project Operationsban a proforma-számla nem rendelkezik az összes szükséges funkcióval a számla nyomtatási beállításainak konfigurálásához. | 
| **Kezdő dátum** | A **Mérföldkő** dátumának megfelelő érték beállítása a forrásmérföldkőben. Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Project** | Alapértelmezés szerint a forrás mérföldkőből van beállítva. Írásvédett mező, amely a szerkesztéstől le van zárva. |
| **Feladat** | Alapértelmezés szerint a forrás mérföldkőből van beállítva. Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Tranzakció kategóriája** | Írásvédett mező, amely a szerkesztéstől le van zárva. |
| **Szerepkör** | Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Lefoglalható erőforrás** | Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Erőforrás-kezelő részleg** | Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Egységütemezés** | Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Egység** | Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Ár** | Alapértelmezés szerint a forrás mérföldkő összegéből van beállítva. Írásvédett mező, amely a szerkesztéstől le van zárva. |
| **Pénznem** | Alapértelmezés szerint a forrás mérföldkőből van beállítva. Írásvédett mező, amely a szerkesztéstől le van zárva. |
| **Összeg** | Alapértelmezés szerint a forrás mérföldkő összegéből van beállítva. Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Adó** | Alapértelmezés szerint a forrás mérföldkő adóösszegéből van beállítva. Írásvédett mező, amely a szerkesztéstől le van zárva. |
| **Kibővített összeg** | Alapértelmezés szerint a forrás mérföldkő bővített összegéből van beállítva. A mező szerkeszthető. | 
| **Számlázási típus** | Alapértelmezés szerint a **számlázható** értékre állítja be a rendszer. Írásvédett mező, amely a szerkesztéstől le van zárva. |
| **Tranzakció típusa** | Alapértelmezés szerint a forrás mérföldkőből van beállítva. Írásvédett mező, amely a szerkesztéstől le van zárva. | 
| **Tranzakció osztálya** | Alapértelmezés szerint a forrás mérföldkőből van beállítva. Írásvédett mező, amely a szerkesztéstől le van zárva. | 

## <a name="refresh-invoice-transactions"></a>Számlatranzakciók frissítése

Ha a számla létrehozása után beérkezett tényleges adatokkal rendelkezik, akkor ezeket a tényeket szerepeltetheti a számlán.

1. A **számlázási elmaradás nézetben** jelölje meg az adatokat **Számlázásra készként**.   
2. Nyissa meg a proforma számla tervezetét, és a **Műveletek** szalagon válassza a **Számlasor-tranzakciók frissítése** lehetőséget.

  A számlasor részletei minden olyan tényleges termékhez létrejönnek, amely korábbi dátummal vannak ellátva, és **Számlázásra kész** állapotúak, de nem szerepelnek a számlán.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
