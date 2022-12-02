---
title: Projektalapú árajánlatsorok áttekintése
description: Ez a cikk a projektalapú ajánlatsorok projektmunkához való használatáról tartalmaz tájékoztatást.
author: rumant
ms.date: 03/30/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 90c5affa25b113476e43f0bbbadd5c9615f9c05c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934461"
---
# <a name="project-based-quote-lines-overview"></a>Projektalapú árajánlatsorok áttekintése 

_**A következőre vonatkozik:** Egyszerű központi telepítés – proforma számlázás, Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A projektalapú ajánlati sorok úgy vannak kialakítva, hogy elősegítsék az aktivitásra vonatkozó projektmunka becslését. A projektalapú ajánlatsor felépítése a projektbecslésekhez a következő fogalmakkal bővül:

- Számlázási mód
- Projekt és feladatleképezés
- Szerepeltetett tranzakciós osztályok
- Nem meghaladandó korlát
- Felszámíthatósági beállítás
- Becslés az ajánlati sor részleteinek használatával
- Árajánlatsor ügyfelei

A következő táblázat a projektalapú árajánlatsor **Általános** lapján található mezőkre vonatkozó információkat tartalmaz. Ezek a mezők segítséget nyújtanak a projektmunka részletes, jól felépített becslési alapjainak kialakításában.

| **Mező** | **Leírás** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- |
| Adatfolyam neve | Az árajánlatsor neve, amely segít azonosítani a becsült árajánlat különálló összetevőjét. | A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja az árajánlat megnyerése után. |
| Számlázási mód | A lehetőségből létrehozott árajánlaton ezt az értéket a rendszer a lehetőség sor megfelelő mezőjéből másolja át. Ez a mező a Dynamics 365 Project Operations által támogatott két fő szerződési modellt tartalmazza:</br>- Rögzített ár</br>- Idő és anyag| Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva. |
| Project | Ezzel a nem kötelező mezővel azonosíthatja azt a projektet, amelyet a program az adott tevékenységgel kapcsolatos munkára fog használni. Amikor egy projektet egy ajánlati sorhoz rendelnek, az segítséget nyújt a felszámítható feladatok beállításában, valamint a projekten alapuló becslést hoz árajánlatsori részletekként az árajánlatsorba. Ha egy projekt nincs leképezve projektalapú árajánlatsorra, a becslést kézzel kell létrehozni az egyes árajánlati sorok részleteinek létrehozásával. | Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.|
| Hozzáadott feladatok | Azt jelzi, hogy az árajánlatsor a kijelölt projekt összes vagy néhány projektfeladatához kerül-e felhasználásra. Ez a mező az alábbi értékekkel rendelkezhet:</br>- Összes projektfeladat</br>- Csak a kiválasztott projektfeladatok</br>Ebben a mezőben az üres érték az **Összes projektfeladat** beállításnak felel meg. | Ha a **Csak kijelölt projektfeladatok** van kiválasztva a projektoldalon, akkor a **Feleadatszámlázási beállítás** fülön kiválaszthatja azokat a feladatokat, amelyek ehhez az árajánlatsorhoz társítják őket. Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva. |
| Idővel együtt | Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt időtranzakciói vagy munkaköltségei szerepelnek-e az árajánlatsor becslésében. A **Nem** érték azt jelzi, hogy az időtranzakciók és a munkaerőköltségek nem fognak szerepelni az árajánlatsorban szereplő becslésben. Az **Igen** érték azt jelzi, hogy az időtranzakciók és a munkaerőköltségek szerepelni fognak az árajánlatsorban szereplő becslésben. | Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva. |
| Költséggel együtt | Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt önköltségei szerepelnek-e az árajánlatsor becslésében. A **Nem** érték azt jelzi, hogy a kiadási költségek nem fognak szerepelni az árajánlatsorban szereplő becslésben. Az **Igen** érték azt jelzi, hogy a kiadási költségek szerepelni fognak az árajánlatsorban szereplő becslésben. | Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva. |
| Anyaggal együtt | Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt anyagköltségei szerepelnek-e az árajánlatsor becslésében. A **Nem** érték azt jelzi, hogy az anyagköltségek nem szerepelnek az árajánlatsor becslésében. Az **Igen** érték azt jelzi, hogy az anyagköltségek szerepelnek az árajánlatsor becslésében. | Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva. |
| Díjjal együtt | Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt díjai szerepelnek-e az árajánlatsor becslésében. A **Nem** érték azt jelzi, hogy a díjak nem fognak szerepelni az árajánlatsorban szereplő becslésben. Az **Igen** érték azt jelzi, hogy a díjak szerepelni fognak az árajánlatsorban szereplő becslésben. | Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva. |
| Megajánlott összeg | Ez az az összeg, amelyet az ügyfélnek a projektalapú árajánlatsorban előre jelzett összes munkára ki fognak számlázni. A lehetőségből létrehozott árajánlaton ezt az értéket a rendszer a lehetőség sor **Ügyfél költségvetése** mezőjéből másolja át. Ha a projektalapú árajánlatsor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és az árajánlatsor részleteiben szereplő összegből kerül összesítésre. | Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva. |
| Becsült adó | Ez egy szerkeszthető mező, amellyel a felhasználó hozzáadhatja a becsült adót az árajánlatsorhoz. Ha a projektalapú árajánlatsor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és az árajánlatsor részleteiben szereplő adóösszegből kerül összesítésre. | Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva. |
| Árajánlat összege adózás után | Ez a mező az árajánlatsor adózás utáni összege, amely csak olvasható. Az ebben a mezőben szereplő összeget a program *Árajánlat összege + adó* képlettel számítja ki. | Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva. |
| Nem meghaladandó korlát | Ez a mező szerkeszthető, és csak azokban a projektalapú árajánlatsorokban érhető el, amelyek **Idő és anyag** számlázási móddal rendelkeznek. | Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva. |
| Ügyfél költségvetése | A mező szerkeszthető, és a rendszer a lehetőség sor megfelelő mezőjéből másolja át, ha az árajánlat egy lehetőségből lett létrehozva. | Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>A projektalapú árajánlatsorok Általános lapján található mezőkre vonatkozó ellenőrzési szabályok

**1. szabály**: Ha a **Hozzáadott feladatok** mező üres, vagy ha az **Összes projektfeladat** értékre van beállítva, a projektet tartalmazza az árajánlatsor.

**2. szabály**: Ha a **Hozzáadott feladatok** mező üres, vagy ha az **Összes projektfeladat** értékre van beállítva, a projekt és egy bizonyos tranzakciós osztály csak az árajánlat egy projektalapú árajánlatsorában szerepelhet.

**3. szabály**: Ha a **Hozzáadott feladatok** mező a **Csak a kiválasztott projektfeladatok** értékre van beállítva, a projekt és egy bizonyos tranzakciós osztály az árajánlat több projektalapú árajánlatsorában szerepelhet.

**4. szabály**: Ha a lehetőség több árajánlattal rendelkezik, akkor különböző árajánlatokból származó ajánlati sorok szerepelhetnek, amelyek ugyanarra a projektre hivatkoznak, és ugyanazt a tranzakciós osztályt tartalmazzák.

**5. szabály**: Ha az ajánlatok nem ugyanahhoz a lehetőséghez tartoznak, akkor nem tartalmazhatják ugyanazokat a projekt- és tranzakciós osztályokat.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Lehetőség</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Ajánlat</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Árajánlatsor</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Hozzáadott feladatok</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Idővel együtt</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Költséggel együtt</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Anyaggal együtt</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Tartalmazás</strong>
                </p>
                <p>
                    <strong>Díj</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Érvényes/nem érvényes</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Ok</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
L1 </p>
            </td>
            <td width="39" valign="top">
                <p>
N1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ÁS1 </p>
            </td>
            <td width="41" valign="top">
                <p>
I1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Üres </p>
            </td>
            <td width="45" valign="top">
                <p>
Igen </p>
            </td>
            <td width="46" valign="top">
                <p>
Igen </p>
            </td>
            <td width="43" valign="top">
                <p>
Igen </p>
            </td>
            <td width="41" valign="top">
                <p>
Igen </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nem érvényes </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Az 2. szabály megsértése. A P1 projektre vonatkozó időt, költséget és díjat az ÁS1 és ÁS2 árajánlatsor tartalmazza </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
L1 </p>
            </td>
            <td width="39" valign="top">
                <p>
N1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ÁS2 </p>
            </td>
            <td width="41" valign="top">
                <p>
I1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Üres </p>
            </td>
            <td width="45" valign="top">
                <p>
Igen </p>
            </td>
            <td width="46" valign="top">
                <p>
Igen </p>
            </td>
            <td width="43" valign="top">
                <p>
Igen </p>
            </td>
            <td width="41" valign="top">
                <p>
Igen </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
L1 </p>
            </td>
            <td width="39" valign="top">
                <p>
N1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ÁS1 </p>
            </td>
            <td width="41" valign="top">
                <p>
I1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Üres </p>
            </td>
            <td width="45" valign="top">
                <p>
Igen </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Igen </p>
            </td>
            <td width="41" valign="top">
                <p>
Igen </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nem érvényes </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Az 2. szabály megsértése. A P1 projektre vonatkozó időt, anyagot és díjat az ÁS1 és ÁS2 árajánlatsor tartalmazza </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
L1 </p>
            </td>
            <td width="39" valign="top">
                <p>
N1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ÁS2 </p>
            </td>
            <td width="41" valign="top">
                <p>
I1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Üres </p>
            </td>
            <td width="45" valign="top">
                <p>
Igen </p>
            </td>
            <td width="46" valign="top">
                <p>
Igen </p>
            </td>
            <td width="43" valign="top">
                <p>
Igen </p>
            </td>
            <td width="41" valign="top">
                <p>
Igen </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
L1 </p>
            </td>
            <td width="39" valign="top">
                <p>
N1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ÁS1 </p>
            </td>
            <td width="41" valign="top">
                <p>
I1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Üres </p>
            </td>
            <td width="45" valign="top">
                <p>
Igen </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Igen </p>
            </td>
            <td width="41" valign="top">
                <p>
Igen </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Érvényes </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
A P1 projektre vonatkozó időt, anyagot és díjat az ÁS1 árajánlatsor tartalmazza <br>
A P1 projektre vonatkozó költséget az ÁS2 tartalmazza <br>
Nincs átfedés abban, hogy miket tartalmaznak az egyes árajánlatsorok, így ez érvényes.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
L1 </p>
            </td>
            <td width="39" valign="top">
                <p>
N1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ÁS2 </p>
            </td>
            <td width="41" valign="top">
                <p>
I1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Üres </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Igen </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
L1 </p>
            </td>
            <td width="39" valign="top">
                <p>
N1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ÁS1 </p>
            </td>
            <td width="41" valign="top">
                <p>
I1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Csak a kiválasztott feladatok </p>
            </td>
            <td width="45" valign="top">
                <p>
Igen </p>
            </td>
            <td width="46" valign="top">
                <p>
Igen </p>
            </td>
            <td width="43" valign="top">
                <p>
Igen </p>
            </td>
            <td width="41" valign="top">
                <p>
Igen </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nem érvényes </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
A 2. szabály megsértése </p>
                <p>
A Q1 tartalmazza a P1 projekttel kapcsolatos feladatok egy részhalmazának idejét, anyagát, költségeit és díjait </p>
                <p>
A QL2 tartalmazza az egész P1 projektre vonatkozó időt, költségeket és díjakat, ezért átfedésben van a Q1 sorral.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
L1 </p>
            </td>
            <td width="39" valign="top">
                <p>
N1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ÁS2 </p>
            </td>
            <td width="41" valign="top">
                <p>
I1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Üres </p>
            </td>
            <td width="45" valign="top">
                <p>
Igen </p>
            </td>
            <td width="46" valign="top">
                <p>
Igen </p>
            </td>
            <td width="43" valign="top">
                <p>
Igen </p>
            </td>
            <td width="41" valign="top">
                <p>
Igen </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
L1 </p>
            </td>
            <td width="39" valign="top">
                <p>
N1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ÁS1 </p>
            </td>
            <td width="41" valign="top">
                <p>
I1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Csak a kiválasztott feladatok </p>
            </td>
            <td width="45" valign="top">
                <p>
Igen </p>
            </td>
            <td width="46" valign="top">
                <p>
Igen </p>
            </td>
            <td width="43" valign="top">
                <p>
Igen </p>
            </td>
            <td width="41" valign="top">
                <p>
Igen </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Érvényes </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
A 3. szabály szerint </p>
                <p>
a Q1 tartalmazza a P1 projekttel kapcsolatos feladatok egy részhalmazának idejét, anyagát, költségeit és díjait.
                </p>
                <p>
A QL2 tartalmazza a P1 projekttel kapcsolatos feladatok egy részhalmazának idejét, anyagát, költségeit és díjait.
                </p>
                <p>
Az egyetlen további ellenőrzés a QL1-es feladatok részhalmaza körül van, amely eltér a QL2-es feladatok részhalmazától, így biztosítva, hogy nincs átfedés. Ezt a rendszer hajtja végre a feladatok társításakor.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
L1 </p>
            </td>
            <td width="39" valign="top">
                <p>
N1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ÁS2 </p>
            </td>
            <td width="41" valign="top">
                <p>
I1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Csak a kiválasztott feladatok </p>
            </td>
            <td width="45" valign="top">
                <p>
Igen </p>
            </td>
            <td width="46" valign="top">
                <p>
Igen </p>
            </td>
            <td width="43" valign="top">
                <p>
Igen </p>
            </td>
            <td width="41" valign="top">
                <p>
Igen </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
L1 </p>
            </td>
            <td width="39" valign="top">
                <p>
N1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ÁS1 </p>
            </td>
            <td width="41" valign="top">
                <p>
I1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Összes projektfeladat vagy üres </p>
            </td>
            <td width="45" valign="top">
                <p>
Igen </p>
            </td>
            <td width="46" valign="top">
                <p>
Igen </p>
            </td>
            <td width="43" valign="top">
                <p>
Igen </p>
            </td>
            <td width="41" valign="top">
                <p>
Igen </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Érvényes </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Az 5. szabály szerint a, Q1 és Q2 két árajánlat ugyanarra a lehetőségre, így mindkettő megbecsülheti a projekt ugyanazon összetevőit.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
L1 </p>
            </td>
            <td width="39" valign="top">
                <p>
N2 </p>
            </td>
            <td width="40" valign="top">
                <p>
ÁS1 </p>
            </td>
            <td width="41" valign="top">
                <p>
I1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Összes projektfeladat vagy üres </p>
            </td>
            <td width="45" valign="top">
                <p>
Igen </p>
            </td>
            <td width="46" valign="top">
                <p>
Igen </p>
            </td>
            <td width="43" valign="top">
                <p>
Igen </p>
            </td>
            <td width="41" valign="top">
                <p>
Igen </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
L1 </p>
            </td>
            <td width="39" valign="top">
                <p>
N1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ÁS1 </p>
            </td>
            <td width="41" valign="top">
                <p>
I1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Összes projektfeladat vagy üres </p>
            </td>
            <td width="45" valign="top">
                <p>
Igen </p>
            </td>
            <td width="46" valign="top">
                <p>
Igen </p>
            </td>
            <td width="43" valign="top">
                <p>
Igen </p>
            </td>
            <td width="41" valign="top">
                <p>
Igen </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nem érvényes </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
A 4. szabály szerint a, Q1 és Q2 két árajánlat különböző lehetőségekre, így nem becsülheti meg mindkettő a projekt ugyanazon összetevőit.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
L2 </p>
            </td>
            <td width="39" valign="top">
                <p>
N1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ÁS1 </p>
            </td>
            <td width="41" valign="top">
                <p>
I1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Összes projektfeladat vagy üres </p>
            </td>
            <td width="45" valign="top">
                <p>
Igen </p>
            </td>
            <td width="46" valign="top">
                <p>
Igen </p>
            </td>
            <td width="43" valign="top">
                <p>
Igen </p>
            </td>
            <td width="41" valign="top">
                <p>
Igen </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
