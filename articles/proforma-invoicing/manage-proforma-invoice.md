---
title: Proforma számla kezelése
description: Ez a témakör információt nyújt a proforma számlák kezeléséről és használatáról.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29e301062f8f3ba955a95953bc2e891f3acaf765
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287691"
---
# <a name="manage-a-proforma-invoice"></a>Proforma számla kezelése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A Dynamics 365 Project Operations alkalmazásban a proforma számlák a Dynamics 365 Salesben szereplő számlák bővítményeként jönnek létre. A számlázás során azonban számos különbség van a számlázási folyamatban a Sales és a Project Operations között. Például nem lehet új számlát létrehozni a Project Operations **Számlák listája** oldaláról, de a Salesben igen. Ezek a különbségek és bővítmények olyan projektek számlázási folyamatainak támogatásához szükségesek, amelyek eltérnek az értékesítési rendelések tipikus számláitól.

> [!IMPORTANT]
> A különbségek miatt a számlák nem használhatók fel egymás helyettesítéseként a Sales és a Project Operations szolgáltatásban.

## <a name="invoice-header"></a>Számlafejléc

A következő információ egy proforma számla fejlécében érhető el a Project Operations alkalmazásban.

| Mező | Hely | Adatfolyam leírása | Alsóbb rétegbeli hatás |
| --- | --- | --- | --- |
| **Számlaazonosító** | **Összegzés** lap | A rendszer által létrehozott azonosító automatikusan a proforma számla létrehozásakor. Írásvédett mező, amely a szerkesztéstől le van zárva. | Ez a mező az egyes proforma számlákra vonatkozó hivatkozásként használatos. |
| **Név** | **Összegzés** lap | Beállítva alapértelmezés szerint a projektszerződés nevére. Ezt a mezőt a felhasználó módosíthatja. | &nbsp;  |
| **Pénznem** | **Összegzés** lap | Beállítva alapértelmezés szerint a projektszerződés pénznemére. Írásvédett mező, amely a szerkesztéstől le van zárva. |&nbsp; |
| **Árlista** | **Összegzés** lap | Beállítva alapértelmezés szerint a projektszerződés árlistájára. Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Lehetőség** | **Összegzés** lap | A csatolt lehetőségre mutató hivatkozás. Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp;  |
| **Szerződés** | **Összegzés** lap | A kapcsolt projektszerződésre mutató hivatkozás. Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Ügyfél** | **Összegzés** lap | A kapcsolt projektszerződésre mutató hivatkozás. Írásvédett mező, amely a szerkesztéstől le van zárva. |&nbsp;  |
| **Leírás** | **Összegzés** lap | A számlát leíró szöveges mező. Ezt a mezőt a felhasználó módosíthatja. | &nbsp; |
| **Számlázási cím** és kapcsolódó mezők | **Összegzés lap** | Az alapértelmezett értékeket a projektszerződés ügyfeléből állítják be. Ezt a mezőt a felhasználó módosíthatja.  | &nbsp; |
| **Állapot** | **Összegzés** lap | A következő beállításokat állítja be: **Aktív**, **Lezárt**, **Fizetett** és **Visszavont**, és szerkesztheti a felhasználó. | A Project Operations nem támogatott állapotai: **lezárt** és **visszavont** állapotú. </br> A számla létrehozásakor a állapot **Aktív** értékre van állítva. </br>Az állapotot csak a számla megerősítését követően kell **Fizetett** állapotra állítani. |
| **Projektszámla állapota** | **Összegzés** lap | A következő beállításokat állítja be: **Piszkozat**, **Felülvizsgálat alatt** és **Megerősítve**, és szerkesztheti a felhasználó. | A számla a **Piszkozat** és a **Felülvizsgálat alatt** állapotokban is szerkeszthető. A számla a megerősítést követően nem módosítható. |
| **Részletmennyiség** | **Összegzés** lap | Az összes számlasor összegének összege az előlegek és a levonások után. Írásvédett mező, amely a szerkesztéstől le van zárva. | Ez a mező a végső összeg kiszámításához használható. |
| **Engedmény (%)** | **Összegzés** lap | Ez a mező módosítható, ha meg szeretné adni az engedmény százalékát. A Project Operations működése nem támogatja ezt a mezőt. | Ez egy nem támogatott mező. |
| **Árengedmény összege** | **Összegzés** lap | Ez a mező módosítható, ha meg szeretné adni az engedmény összegét. A Project Operations működése nem támogatja ezt a mezőt. | Ez egy nem támogatott mező. |
| **Szállítás előtti összeg** | **Összegzés lap** | A teljes számlaösszeg a kedvezmények után. Írásvédett mező, amely a szerkesztéstől le van zárva. | Ez a mező a végső összeg kiszámításához használható. |
| **Szállítási mennyiség** | **Összegzés** lap | Ez a mező módosítható, ha meg szeretné adni a szállítási összeget. A Project Operations működése nem támogatja ezt a mezőt. | Ez egy nem támogatott mező. |
| **Összes adó** | **Összegzés** lap | A számlán szereplő összes számlasor teljes összege. Írásvédett mező, amely a szerkesztéstől le van zárva. | Nincs. |
| **Összmennyiség** | **Összegzés** lap | Az engedmények és az adók utáni végösszeg. | A végösszeg az az összeg, amelyet az ügyfélnek ki kell fizetnie. |

## <a name="project-based-invoice-lines"></a>Projektalapú számlasorok

A Project Operationsban mindig tartozik egy számlasor minden projektszerződéssorhoz. A számlasor akkor is létrejön, ha nincsenek tényleges adatok. A következő információ egy proforma számla sorában érhető el.

| Mező | Hely | Adatfolyam leírása | Alsóbb rétegbeli hatás |
| --- | --- | --- | --- |
| **Számlaazonosító** | **Általános** lap | A számla azonosítójára vonatkozó hivatkozás. Írásvédett mező, amely a szerkesztéstől le van zárva. | A számlaazonosító hivatkozás segítségével visszatérhet a számla fejlécéhez. |
| **Név** | **Általános** lap | A számlasor neve alapértelmezés szerint a szerződéssor nevéből van beállítva. Ezt a mezőt a felhasználó módosíthatja. | &nbsp; |
| **Project** | **Általános** lap | A projekt a kapcsolódó projektszerződéssorban. Írásvédett mező, amely a szerkesztéstől le van zárva. | A projekthivatkozás segítségével léphet a projektre. |
| **Számlázási mód** | **Általános** lap | A számlázási mód a kapcsolódó projektszerződéssorban. Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Szerződéssor összege** | **Általános** lap | A kapcsolódó projektszerződéssor szerződéses összege. Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Kiszámlázva eddig** | **Általános** lap | Az összegek végösszege az adott számla minden számlasoradatában. Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Összeg** | **Általános** lap | Az összegek végösszege az adott számla minden számlázható számlasoradatában. Írásvédett mező, amely a szerkesztéstől le van zárva. | Ez a mező a végső összeg kiszámításához használható a számlafejlécben. |
| **Adó** | **Általános** lap | Az adóösszegek végösszege az adott számlasor minden számlasoradatában. Írásvédett mező, amely a szerkesztéstől le van zárva. | Ez a mező a végső adóösszeg kiszámításához használható a számlafejlécben. |
| **Kibővített összeg** | **Általános** lap | A teljes összegek végösszege (**Adó + összegek**) az adott számlasor minden számlázható számlasoradatában. Írásvédett mező, amely a szerkesztéstől le van zárva. | Ez a mező a végső összeg kiszámításához használható a számlafejlécben. |

## <a name="invoice-line-details"></a>Számlasor részletei

A projekt számláján szereplő minden számlasor tartalmazza a számlasor részleteit. Ezek a soradatok a számla sorában hivatkozott, a szerződéssorhoz kapcsolódó, nem számlázott értékesítési tényadatokkal és mérföldkövekkel kapcsolatosak. Az összes ilyen tranzakcióhoz **Számlázásra kész** jelölést kell alkalmazni.

Az **idő-és anyagelszámolású számla** sor esetében a számlasor részleteit a rendszer a **Számlasor** oldalon **Számlázható**, **Nem számlázható** és **Kiegészítő** csoportokba sorolja. A **számlázható számlasorok** részleteinek összegzése adja a számlasor összesítését. Az **Ingyenes** és a **Nem számlázható tényadatok** nem számítanak bele a számlasor összegébe.

A **rögzített árú számla** sora esetében a rendszer a számlasor adatait a kapcsolódó szerződéssor **számlázásra kész** ként megjelölt mérföldkövei alapján hozza létre. Miután a számlasor részletei egy mérföldkőből származnak, a mérföldkő számlázási állapota **Ügyfélszámla létrehozva** értékre frissül.

### <a name="edit-invoice-line-details"></a>Számlasorrészletek szerkesztése

A következő mezők a számlasor részletes adatain láthatók, amelyeket a rendszer nem számlázott értékesítési tényadattal támogat.

| Mező | Adatfolyam leírása | Alsóbb rétegbeli hatás |
| --- | --- | --- |
| **Számlasor** | A **számla azonosítójára** vonatkozó hivatkozás. Írásvédett mező, szerkesztésre zárolva. | Ez a hivatkozás segítségével visszatérhet a számla fejlécéhez. |
| **Leírás** | A számlasoradat leírását. Beállítva alapértelmezett módon a **Belső megjegyzések** mezőből az **Időbejegyzés** menüpontban, és a **Leírás** mezőből a **Költségbejegyzés** menüpontban. A mezőt a felhasználó módosíthatja.| &nbsp; |
| **Külső leírás** | A számlasoradat leírását. Beállítva alapértelmezett módon a **Külső megjegyzések** mezőből az **Időbejegyzés** menüpontban, és a **Leírás** mezőből a **Költségbejegyzés** menüpontban. A mezőt a felhasználó módosíthatja. | A Leírás segítségével megállapítható, hogy mi legyen az ügyfélnek küldendő nyomtatott számlán. A Project Operationsban a proforma-számla nem rendelkezik az összes szükséges funkcióval a számla nyomtatási beállításainak konfigurálásához. |
| **Kezdő dátum** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | Ez a mező olyan új számlasorrészletekben szerkeszthető, amelyet nem támogat forrás tényadata. |
| **Project** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | Beállítva alapértelmezés szerint a kapcsolódó szerződéssor projektjére. |
| **Feladat** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | A mező olyan új számlasorrészletekben szerkeszthető, amelyet nem támogat forrás tényadata. A legördülő lista a kapcsolódó projektszerződéssor összes feladatát mutatja.  |
| **Tranzakció kategóriája** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | A mező olyan új számlasorrészletekben szerkeszthető, amelyet nem támogat egy tényleges forrás. |
| **Szerepkör** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | A mező olyan új számlasorrészletekben szerkeszthető, amelyet nem támogat egy forrás tényadata. |
| **Lefoglalható erőforrás** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | A mező olyan új számlasorrészletekben szerkeszthető, amelyet nem támogat egy tényleges forrás. |
| **Erőforrás-kezelő vállalat** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | A mező olyan új számlasorrészletekben szerkeszthető, amelyet nem támogat egy forrás tényadata. |
| **Erőforrás-kezelő részleg** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | A mező olyan új számlasorrészletekben szerkeszthető, amelyet nem támogat egy forrás tényadata. |
| **Mennyiség** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | A mező olyan új számlasorrészletekben szerkeszthető, amelyet nem támogat egy forrás tényadata. |
| **Egységütemezés** | Az időre vonatkozó számlasoradatoknál ez a beállítás értéke mindig idő, és nem szerkeszthető. A költségek esetében ez alapértelmezés szerint a forrás költségének tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | Beállítva alapértelmezett módon **Idő** értékre egy új számlasoron, amelyet nem támogat egy tényleges érték. |
| **Egység** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | A mező olyan új számlasorrészletekben szerkeszthető, amelyet nem támogat egy forrás tényadata |
| **Ár** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | A mező olyan új számlasorrészletekben szerkeszthető, amelyet nem támogat egy forrás tényadata. Ha nem ad meg értéket, a **mentés** után alapértelmezés szerint be van állítva. |
| **Pénznem** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | A számla fejlécéből van alapértelmezés szerint beállítva, amikor az új számlarészletet hoz létre tényleges támogatás nélkül.  Írásvédett mező, amely a szerkesztéstől le van zárva. |
| **Összeg** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | Kiszámítva **Mennyiség\*Ár** elemként új számlarészlet létrehozásakor támogató tényadat nélkül. A **mentés** után számítja ki a program. Írásvédett mező, amely a szerkesztéstől le van zárva. |
| **Adó** | Alapértelmezés szerint a forrás tényleges értékét adja meg. A mezőt a felhasználó módosíthatja | A mező a felhasználó által módosítható, amikor egy új számlasorrészletet hoz létre, és amely nem rendelkezik tényleges támogatással. |
| **Kibővített összeg** | Számított mező, kiszámítása: **Összeg + Adó**. Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Számlázási típus** | Alapértelmezés szerint a forrás tényleges értékét adja meg. A mezőt a felhasználó módosíthatja. | A **Számlázható** lehetőség kiválasztásával hozzáadja a sort a számlasor végösszegéhez. A **Kiegészítő** és a **Nem számlázható** kizárja az értéket a számlasor összegéből. |
| **Tranzakció típusa** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | Alapértelmezés szerint a **számlázott értékesítésre** van beállítva, amikor új **Számlasorrészletet** hoz létre támogató tényadat nélkül.  |
| **Tranzakció osztálya** | Alapértelmezés szerint a forrás tényleges értékét adja meg. Írásvédett mező, amely a szerkesztéstől le van zárva. | Alapértelmezés szerint van beállítva attól függően, hogy a felhasználó **Idő**, **Költség** vagy **Díj** típusú számlasoradatot hoz létre, miközben új **Számlasoradatot** hoz létre tényleges támogatás nélkül. Szerkesztés elől zárolva. |

A következő mezők a számlasor részletes adatain láthatók, amelyeket a rendszer mérföldkővel támogat:

| Mező | Adatfolyam leírása | Alsóbb rétegbeli hatás |
| --- | --- | --- |
| **Számlasor** | A **számlasor azonosítójára** vonatkozó hivatkozás. Írásvédett mező, amely a szerkesztéstől le van zárva. | A hivatkozás segítségével visszatérhet a számla fejlécéhez. |
| **Leírás** | A számlasoradat leírása. Alapértelmezés szerint a forrás mérföldkő leírásából van beállítva. | &nbsp; |
|**Külső leírás** | A számlasoradat leírása, amely alapértelmezés szerint a forrás mérföldkő leírásából van beállítva. | Az adott mező segítségével megállapítható, hogy mi legyen az ügyfélnek küldendő nyomtatott számlán. A Project Operationsban a proforma-számla nem rendelkezik az összes szükséges funkcióval a számla nyomtatási beállításainak konfigurálásához. |
| **Kezdő dátum** | A **Mérföldkő** dátumának megfelelő érték beállítása a forrásmérföldkőben. Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Project** | Alapértelmezés szerint a forrás mérföldkőből van beállítva. Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Feladat** | Alapértelmezés szerint a forrás mérföldkőből van beállítva. Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Tranzakció kategóriája** | Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Szerepkör** | Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Lefoglalható erőforrás** | Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Erőforrás-kezelő részleg** | Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Egységütemezés** | Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Egység** | Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Ár** | Alapértelmezés szerint a forrás mérföldkő összegéből van beállítva. Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Pénznem** | Alapértelmezés szerint a forrás mérföldkőből van beállítva. Írásvédett mező, amely a szerkesztéstől le van zárva. |&nbsp; |
| **Összeg** | Alapértelmezés szerint a forrás mérföldkő összegéből van beállítva. Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Adó** | Alapértelmezés szerint a forrás mérföldkő adóösszegéből van beállítva. Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Kibővített összeg** | Alapértelmezés szerint a forrás mérföldkő bővített összegéből van beállítva. A mezőt a felhasználó módosíthatja | &nbsp; |
| **Számlázási típus** | Alapértelmezés szerint a **számlázható** értékre állítja be a rendszer. Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Tranzakció típusa** | Alapértelmezés szerint a forrás mérföldkőből van beállítva. Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |
| **Tranzakció osztálya** | Alapértelmezés szerint a forrás mérföldkőből van beállítva. Írásvédett mező, amely a szerkesztéstől le van zárva. | &nbsp; |

## <a name="refresh-invoice-transactions"></a>Számlatranzakciók frissítése

Ha a számla létrehozása után beérkezett tényleges adatokkal rendelkezik, akkor ezeket a tényeket szerepeltetheti a számlán.

1. A **számlázási elmaradás nézetben** jelölje meg az adatokat **Számlázásra készként**.   
2. Nyissa meg a proforma számlát, és a menüszalag **műveletek** lapján kattintson a **számlasor-tranzakciók frissítése** lehetőségre.

  Ezzel a számlasor adatait minden olyan tényleges értékhez létrehozza, amely **Számlázásra készként** van megjelölve, múltbeli dátumú, de nem szerepel a számlában.


[!INCLUDE[footer-include](../includes/footer-banner.md)]