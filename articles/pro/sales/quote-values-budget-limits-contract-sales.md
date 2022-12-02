---
title: Összefoglaló információk egy projektárajánlatról - Lite
description: Ez a cikk a projektárajánlatokra érvényes és azokat érintő információkkal és beállításokkal kapcsolatos tudnivalókat tartalmaz. (Sales)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3441348cb46804f8f76cb23b3f916fe69c3fbe99
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917027"
---
# <a name="header-details-for-project-quotes"></a>Fejlécadatok projektárajánlatok esetében

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a cikk ismerteti a projektárajánlatra vonatkozó információkat. Ezek közé tartoznak az összes árajánlatsort érintő beállítások, valamint az árajánlatra vonatkozó olyan információk, amelyeket az összes sortétel összegez a projektárajánlat fő teljesítménymutatóinak előmozdításához.

A következő táblázat a projektajánlat olyan összegző információs mezőit sorolja fel, amelyek egyediek a Dynamics 365 Project Operations alkalmazásban, vagy a Dynamics 365 Sales ajánlatainál viselkedésük valamilyen fontos változással rendelkezik.

| **Mező** | **Hely** | **Leírás** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- | --- |
| Típus szerint | Összegzés lap (rejtett) | Ez a értékkészlet mező a következő értékekkel rendelkezik:</br>- Munkaalapú (csak akkor érhető el, ha a Project Operations telepítve van)</br>- Cikkalapú (csak akkor érhető el, ha a Project Operations és a Sales telepítve van)</br>- Szolgáltatáskarbantartás-alapú (elérhető, ha a Dynamics 365 Field Service telepítve van) | A Project Operations alkalmazás használatakor a program automatikusan **Munkaalapú** értékre állítja a mezőt. Ez az árajánlatot projektalapú árajánlatként osztályozza. Az ajánlatnak projektalapúnak kell lennie, hogy minden projektspecifikus bővítmény és funkció futtatását lehetővé tegye. |
| Potenciális ügyfél | Összegzés lap | Hivatkozás az ügyfél vállalati vagy partneri rekordjára. Amikor a lehetőségből egy árajánlat kerül létrehozásra, ezt a mezőt a rendszer a lehetőség megfelelő mezőjéből másolja át. | A projektárajánlatban szereplő pénznemet a program az ügyfél pénzneme alapján állítja be alapértelmezettként. Ez az árajánlat mentése előtt azonban módosítható. |
| Partnerkezelő | Összegzés lap | Az üzlet partnerkezelőjének neve. Amikor a lehetőségből egy árajánlat kerül létrehozásra, ezt a mezőt a rendszer a lehetőség megfelelő mezőjéből másolja át. | A partnerkezelő felelős az ügyféllel való kapcsolat kezeléséért a projekt teljesítése során. A partnerkezelőhöz kötött foglalható erőforrásrekord alapján a szerződő részleg a projektárajánlatban szereplő alapján veszi fel az alapértelmezett értéket. |
| Szerződő részleg | Összegzés lap | Az árajánlathoz kapcsolódó projekt vagy projektek teljesítéséért felelős szervezeti egység. Amikor a lehetőségből egy árajánlat kerül létrehozásra, ezt a mezőt a rendszer a lehetőség megfelelő mezőjéből másolja át. | A szerződő egység a vállalat azon részlege, amely a projekteket az üzlet lezárását követően végrehajtja. Minden egyes szerződő egység pénznemmel rendelkezik, és ez a pénznem kerül felhasználásra a projekt végrehajtásához kapcsolódó becsült és ténylegesen felmerült költségek jelentésére. |
| Termékárlista | Összegzés lap | Ez a termékalapú árajánlatsorokban szereplő alapértelmezett árakhoz használt árlista. A mezőhöz tartozó lehetőségek listájában látható az árlisták listája, ahol az árlista pénzneme megegyezik az árajánlatban szereplő pénznemmel. Amikor a lehetőségből egy árajánlat kerül létrehozásra, ezt a mezőt a rendszer a lehetőség megfelelő mezőjéből másolja át. A lehetőség ezen mezőjének értéke alapértelmezés szerint a partnerrekordból származik, de módosítható. | Az árajánlat elnyerésekor a mező értékét a rendszer a létrehozott projektszerződéssorba másolja át. |
| Pénznem | Összegzés lap | Ez jelzi a pénznemet, amely az üzlet értékén jelentéséhez felhasználásra fog kerülni. Ez egyúttal az a pénznem, amelyben az ügyfél az üzlet elnyerésekor a számlát kapja. Amikor a lehetőségből egy árajánlat kerül létrehozásra, ezt a mezőt a rendszer a lehetőség megfelelő mezőjéből másolja át. A lehetőség ezen mezőjének értéke alapértelmezés szerint a partnerrekordból származik, de a felhasználó által módosítható. | Az árajánlat mentése után a mező már nem szerkeszthető. Az árajánlat termék- és projektárlistájának alapértelmezett értékének beállítására szolgál. Az árajánlat pénznemének meg kell egyeznie az árajánlaton szereplő pénznemmel. |
| Nem meghaladandó korlát | Összegzés lap | Ez jelzi az egyeztetett felső korlátot a végső értéken, amellyel az ügyfél egyetért az üzlet esetében. | Ez a felső korlát a végrehajtás során kerül kiértékelésre, és az üzlethez kapcsolódó összes sortételre és projektre érvényes. |
| Kért teljesítési dátum | Összegzés lap | Amikor a lehetőségből egy árajánlat kerül létrehozásra, ezt a mezőt a rendszer a lehetőség megfelelő mezőjéből másolja át. | Ez a dátum kerül használatra a számlaütemezések előállításához használt záró dátumként. |

Alább láthatók a projektárajánlatban rendelkezésre álló azon lapok és fő teljesítménymutatók, amelyek egyediek a Project Operations esetében, vagy néhány fontos változást okoznak a Sales árajánlataihoz képest:

| **Mező** | **Hely** | **Leírás** |
| --- | --- | --- |
| Jövedelmezőségi elemzés | Árajánlat lapja | A lap a következő metrikákat mutatja meg:</br>- Teljes felszámítható költség</br></br>- Teljes fel nem számítható költség</br>- Összbevétel</br>- Összbevétel (alappénznem)</br>- Bruttó nyereség</br>- Helyesbített bruttó nyereség|
| Összehasonlítás az ügyfél elvárásaival | Árajánlat lapja | Ez a lap a következő metrikákat mutatja meg:</br>- Becsült befejezés</br>- Kért befejezés</br>- Ügyfél költségvetése</br>- Árajánlat értéke |
| Árajánlat-elemzés | Árajánlat lapja | Ez a lap a projektárajánlat következő fő teljesítménymutatóit foglalja össze</br>- Összehasonlítás az ügyfelek költségvetésre és ütemezésre vonatkozó elvárásaival</br>- Bruttó nyereség</br>- Helyesbített bruttó nyereség |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
