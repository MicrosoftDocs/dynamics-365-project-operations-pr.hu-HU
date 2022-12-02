---
title: Projektszerződés beállításai - Lite
description: Ez a cikk a szerződéssorokra hatással levő mezőkről, valamint az összes sorra vonatkozóan összefoglalt szerződésre vonatkozó információkra vonatkozó információkat tartalmaz.
author: rumant
ms.date: 03/08/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6123cbc028cf49cc198173697969f415b0789256
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917073"
---
# <a name="header-details-for-project-contracts"></a>Fejlécadatok projektszerződések esetében

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a cikk a teljes szerződésre vonatkozó mezőkre vonatkozó információkat tartalmaz, beleértve az összes szerződéssorra hatással levő beállításokat is. Ezenkívül tartalmaz a szerződésre vonatkozó, összes sorelemen keresztül összesített információkat, amelyek a projektszerződés KPI-jaira hatással vannak.

A következő táblázat a projektszerződés olyan mezőit sorolja fel, amelyek egyediek a Dynamics 365 Project Operations alkalmazásban, vagy a Dynamics 365 Sales értékesítési megrendelésinél viselkedésük valamilyen fontos változással rendelkezik.

| Mező | Hely | Adatfolyam leírása | Alsóbb rétegbeli hatás |
| --- | --- | --- | --- |
| Típus szerint | **Összegzés** lap (rejtett) | Ez a értékkészlet mező a következő beállításokkal rendelkezik:</br>- **Munkaalapú** (csak akkor érhető el, ha a Project Operations telepítve van)</br>- **Cikkalapú** (csak akkor érhető el, ha a Project Operations és a Sales telepítve van)</br>- **Szolgáltatáskarbantartás-alapú** (elérhető, ha a Dynamics 365 Field Service telepítve van) | A Project Operations esetében ennek a mezőnek az értéke alapértelmezés szerint a **Munkaalapú** és a szerződést projekt alapú szerződésként osztályozza. A szerződésnek projektalapúnak kell lennie, hogy minden projektspecifikus bővítmény és funkció futtatását lehetővé tegye. |
| Potenciális ügyfél | **Összegzés** lap | Hivatkozás az ügyfél vállalati vagy partneri rekordjára. Amikor az árajánlatból egy szerződés kerül létrehozásra, ezt a mezőt a rendszer az árajánlatrekord megfelelő mezőjéből másolja át. | A projektszerződés alapértelmezett értékében szereplő pénznemet a program az ügyfél pénzneme alapján állítja be alapértelmezettként. Ez a szerződés mentése előtt azonban módosítható. |
| Partnerkezelő | **Összegzés** lap | Az üzlet partnerkezelőjének neve. Amikor az árajánlatból egy szerződés kerül létrehozásra, ezt a mezőt a rendszer az árajánlatrekord megfelelő mezőjéből másolja át. | A partnerkezelő felelős az ügyféllel való kapcsolat kezeléséért a projekt teljesítése során. A partnerkezelőhöz kötött foglalható erőforrásrekord alapján a szerződő részleg a projektszerződésben szereplő alapján veszi fel az alapértelmezett értéket. |
| Szerződő részleg | **Összegzés** lap | A szerződéshez kapcsolódó projekt(ek) teljesítéséért felelős szervezeti egység. Amikor az árajánlatból egy szerződés kerül létrehozásra, ezt a mezőt a rendszer az árajánlatrekord megfelelő mezőjéből másolja át. | A szerződő részleg a vállalat azon részlege, amely a projekteket végrehajtja. Minden egyes szerződő egység pénznemmel rendelkezik, és ez a pénznem kerül felhasználásra a projekthez kapcsolódó becsült és ténylegesen felmerült költségek jelentésére. |
| Termékárlista | **Összegzés** lap | Ez a termékalapú szerződéssorokban szereplő alapértelmezett árakhoz használt árlista. A mezőhöz tartozó legördülő lehetőségek listájában látható az árlisták listája, ahol az árlista pénzneme megegyezik a szerződésben szereplő pénznemmel. Amikor az árajánlatból egy szerződés kerül létrehozásra, ezt a mezőt a rendszer az árajánlatrekord megfelelő mezőjéből másolja át. A projektszerződés ezen mezőjének értéke alapértelmezés szerint a partnerrekordból származik, de módosítható. | Nincs lefelé irányuló relevancia ehhez a mezőhöz. |
| Pénznem | **Összegzés** lap | Az üzlet értékének jelentésére szolgáló pénznem, valamint az a pénznem, amelyben az ügyfél számlázva lesz. Amikor az árajánlatból egy szerződés kerül létrehozásra, ezt a mezőt a rendszer az árajánlatrekord megfelelő mezőjéből másolja át. A projektszerződés ezen mezőjének értéke alapértelmezés szerint a partnerrekordból származik, de módosítható. | A szerződés mentése után a mező már nem szerkeszthető. A mező a szerződés termék- és projektárlistájának alapértelmezett értékének beállítására szolgál. A szerződés pénznemének meg kell egyeznie az árajánlaton szereplő pénznemmel. |
| Nem meghaladandó korlát | **Összegzés** lap | Ez a mező jelzi az egyeztetett felső korlátot a végső értéken, amellyel az ügyfél egyetért az üzlet esetében. | Ez a felső korlát a végrehajtás során kerül kiértékelésre, és az üzlethez kapcsolódó összes sortételre és projektre érvényes. |
| Kért kézbesítési dátum | **Összegzés** lap | Amikor a projektárajánlatból egy szerződés kerül létrehozásra, ezt a mezőt a rendszer az projektárajánlat megfelelő mezőjéből másolja át. | Ez a dátum kerül használatra a számlaütemezések előállításához használt záró dátumként. |

A következő fő teljesítménymutatók érhetők el a projekt szerződés **Szerződési teljesítmény** lapján. 

>[!NOTE]
>A **Szerződési teljesítmény** lapon található összes összeg a környezet alapértelmezett pénznemében van megjelölve.

| Mező | Hely | Description |
| --- | --- | --- |
| Szerződés értéke | Általános szerződés | A projektszerződés teljes értéke.|
| Számlázott összeg | Általános szerződés | A szerződésben szereplő összes számlán szereplő összegek összege.|
| Felmerült költség | Általános szerződés | A szerződéshez leképezett összes projektre vonatkozóan a naplózott összes költség összege. |
| Bruttó nyereség | Általános szerződés | Számlázott összeg – a felmerült költség adott dátumig/számlázott összeg |
| Várt árrés | Általános szerződés | (Szerződés értéke – becsült költség)/szerződés érték becsült költségei = a szerződésre leképezett összes projekt becsült költségének összege.|
| Szerződés értéke | Projektalapú sorok | A szerződéssor bemeneti értéke. |
| Számlázott összeg | Projektalapú sorok | Rögzített árú szerződéssor: az összes számlázott értékesítési mérföldkő összegének összege a szerződéshez létrehozott különféle számlák szerződéssoraihoz. Idő és anyag típusú szerződéssor: az összes számlázott értékesítési számlázható összegének összege a szerződéshez létrehozott különféle számlák szerződéssoraihoz. |
| Felmerült költség | Projektalapú sorok | A szerződési sorhoz leképezett összes projektre vonatkozóan a naplózott összes költség összege. |
| Bruttó nyereség | Projektalapú sorok | (Számlázott összeg – a felmerült költség adott dátumig)/számlázott összeg |
| Várt árrés | Projektalapú sorok | (Szerződéssor összege az alappénznemben – a szerződéssor becsült költsége alappénznemben)/szerződéssor összege alappénznemben |
| Felmerült költség | Projekt alapú sor részletei | Idő: az adott szerepkörhöz a szerződéssorhoz leképezett projektre vonatkozóan az időköltség tényleges értékének összege. Költségek: az adott kategóriához a szerződéssorhoz leképezett projektre vonatkozóan az az összes költség tényleges értékének összege. |
| Naplózott mennyiség | Projekt alapú sor részletei | Idő: egy szerepkörhöz, amely a szerződéssorhoz leképezett projektre vonatkozik, az időköltség teljes tényleges értékének mennyisége. Költségek: az adott költségkategóriához az adott szerződéssorhoz leképezett projektre vonatkozó költségek tényleges értékeinek össze mennyisége. |
| Számlázott összeg | Projekt alapú sor részletei | Rögzített árú szerződéssor esetén ez a mező a részletességi szinten üres marad, és csak a szerződéssor szintjén jelenik meg. Egy idő-és anyagelszámolású szerződéssor esetén a számítások a részletek szintjén végezhetők el. A részletek az összes számlázott bevételi sor összegét jelenítik meg az adott számlázható szerződéssor alapján. |
| Számlázott mennyiség | Projekt alapú sor részletei | Rögzített árú szerződéssor esetén ez a mező a részletességi szinten üres marad, és csak a szerződéssor szintjén jelenik meg. Egy idő-és anyagelszámolású szerződéssor esetén a számítások a részletek szintjén végezhetők el az időre és költségekre vonatkozóan. Idő: Az adott szerepkör összes számlázott bevételi során szereplő órák összegét jelenítik meg az adott számlázható szerződéssor alapján. Költségek: az adott költségkategóriához az adott szerződéssorhoz leképezett projektre vonatkozó költségek tényleges értékeinek össze mennyisége. |
| Szerződés értéke | Termékalapú sorok | A termék alapú szerződéssor szerződéssor értéke. |
| Számlázott összeg | Termékalapú sorok | Az összes számlasor összegének összege a szerződéshez létrehozott különféle számlákon a termék alapú szerződéssor alapján. |
| Felmerült költség | Termékalapú sorok | A termékalapú szerződési sorhoz leképezett naplózott összes költség összege. |
| Bruttó nyereség | Projektalapú sorok | Számlázott összeg – a felmerült költség adott dátumig/számlázott összeg |
| Várt árrés | Termékalapú sorok | (Szerződéssor értéke – a szerződéssor becsült költsége)/szerződéssor értéke |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
