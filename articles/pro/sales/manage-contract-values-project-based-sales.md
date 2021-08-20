---
title: Projektalapú szerződéssorok áttekintése
description: Ez a témakör információkat nyújt a projektalapú szerződéssorok használatáról.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 7da8a7f898e6f0bb46d4cf6de65812e3aabb7416a2fdf2f9d9c8bad07e77cd85
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999049"
---
# <a name="project-based-contract-lines-overview"></a>Projektalapú szerződéssorok áttekintése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations szerződéssorai úgy vannak kialakítva, hogy tárolják a becsléseket és számlázási megállapodásokat a projektmunka adott komponenseire egy aktivitásban. A projektalapú szerződéssorok felépítése a projektek becsült és számlázási helyzetére vonatkozóan a következő fogalmakkal bővül:

- Számlázási mód
- Projekt és feladatleképezés
- Szerepeltetett tranzakciós osztályok
- Nem meghaladandó korlát
- Felszámíthatósági beállítás
- Becslések a szerződéssorok részleteinek használatával
- Szerződéssor ügyfelei

A következő táblázat a projektalapú szerződéssorok **Általános** lapján található mezőket tartalmazza, amelyek segítenek részletes, mindenre kiterjedő becslési és számlázási megoldásokat beállítania projektalapú munkához.

| Mező | Adatfolyam leírása | Alsóbb rétegbeli hatás |
| --- | --- | --- |
| **Név** | A szerződéssor neve. Ez azonosítja a becsült szerződés különálló összetevőjét. Az árajánlatból létrehozott projekt-szerződések esetén a program a projekt alapú árajánlati sor kapcsolódó értékéből másolja át az értéket. | A számla létrehozásakor a név át lesz másolva a projekt számlasorra, amelye ebből a szerződéssorból lesz létrehozva. |
| **Számlázási mód** | Az árajánlatból létrehozott projekt-szerződésben a program a az ajánlatsor kapcsolódó mezőjéből másolja át az értéket. Ez egy értékkészlet, amely a Project Operations által támogatott két fő szerződőmodellt képviseli:</br>- **Rögzített ár**</br>- **Idő és anyag** | A hivatkozott szerződéssor számlázási módja alapján a rendszer feldolgozza a tényleges tranzakciót. Ha a tényadat által hivatkozottszerződéssor idő-és anyagelszámolású számlázási módot tartalmaz, akkor a rendszer létrehozza a költség és a nem számlázott tényleges értékesítések bejegyzéseit. Ha a tényadat által hivatkozott szerződéssor rögzített árú számlázási móddal rendelkezik, akkor csak egy tényleges költség jön létre. |
| **Project** | Ezzel a mezővel azonosíthatja azt a projektet, amelyet az adott aktivitással kapcsolatos munkára fog használni. | Ezt az értéket a **Hozzáadott feladatok** és a **Hozzáadott tranzakcióosztályok** együtt fogja használni a szerződéssor-hivatkozás feloldásához egy tényleges vagy becslési sorrekordon. |
| **Hozzáadott feladatok** | Azt jelzi, hogy a szerződéssor tartalmazza-e a kijelölt projekt összes projekt-feladatát, vagy csak a feladatok egy részét. Ez egy értékkészlet, amelynek a következő lehetséges értékei vannak:</br>- **Összes projektfeladat**</br>- **Csak a kiválasztott projektfeladatok**. Az ebben a mezőben szereplő üres érték az **Összes projektfeladat** kijelölésével egyenlő. | Ha a **Csak a kiválasztott feladatok** lehetőség van kiválasztva, akkor kijelölhet bizonyos feladatokat, és hozzárendelheti őket ehhez a szerződés sorhoz a **Projekt** lap **Feladat számlázási beállítása** lapján. Ezt az értéket a program a **Projekt** és **Hozzáadott tranzakciók** osztályokkal együtt használja, hogy feloldja a szerződéssor hivatkozását egy tényadaton vagy egy becsléssor-rekordon. |
| **Idővel együtt** | Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt időtranzakciói vagy munkaköltségei szerepelnek-e a szerződéssoron. A **Nem** érték azt jelzi, hogy a kiválasztott projekthez tartozó időtranzakciók vagy munkaköltségek nem fognak szerepelni ebben a szerződéssorban. Az **Igen** érték azt jelzi, hogy fognak. | Ez az érték a projekttel együtt egy tényleges vagy becslési sorrekord szerződéssor-hivatkozásának feloldására szolgál. |
| **Költséggel együtt** | Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt önköltségei szerepelnek-e a szerződéssorban. A **Nem** érték azt jelzi, hogy a kiválasztott projekthez tartozó önköltség nem fog szerepelni ebben a szerződéssorban. Az **Igen** érték azt jelzi, hogy fog. | Ez az érték a projekttel együtt egy tényleges vagy becslési sorrekord szerződéssor-hivatkozásának feloldására szolgál. |
| **Anyagokkal együtt** | Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt anyagköltségei szerepelnek-e a szerződéssorban. A **Nem** érték azt jelzi, hogy az anyagköltségek nem szerepelnek a szerződéssorban. Az **Igen** érték azt jelzi, hogy fog. | Ez az érték a projekttel együtt egy tényleges vagy becslési sorrekord szerződéssor-hivatkozásának feloldására szolgál. |
| **Díjjal együtt** | Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt díjai szerepelnek-e a szerződéssorban. A **Nem** érték azt jelzi, hogy a kiválasztott projekthez tartozó díjak nem fognak szerepelni ebben a szerződéssorban. Az **Igen** érték azt jelzi, hogy fognak. | Ez az érték a projekttel együtt egy tényleges vagy becslési sorrekord szerződéssor-hivatkozásának feloldására szolgál. |
| **Szerződésben rögzített összeg** | Rögzített árú szerződéssor esetén ez az összeg egy megállapodott érték, ami számlázva lesz az ügyfélnek a szerződéssorhoz társított összes munkaösszetevőhöz. Idő és anyag szerződéssor esetén ez az összeg becsült érték arra vonatkozóan, ami számlázva lesz az ügyfélnek a szerződéssorhoz társított összes munkaösszetevőhöz. Árajánlatból létrehozott projekt-szerződésben a program a az ajánlatsor kapcsolódó mezőjéből másolja át az értéket. Ha egy projektalapú szerződéssor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és a program a szerződéssor részleteiben szereplő összegből összegzi. | Ha a szerződéssorhoz tartoznak sorrészletek, akkor ez az érték módosítható a sor részleteiben szereplő összegek módosításával. Rögzített árú szerződéssor esetén ez az érték a periodikus számlázási mérföldkövek után fizetendő összeg generálására szolgál. |
| **Becsült adó** | A felhasználó módosíthatja ezt a mezőt, hogy a szerződéssor összegére vonatkozóan megadja a becsült adót. Ha egy projektalapú szerződéssor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és a program a szerződéssor részleteiben szereplő adóösszegből összegzi. | Ha a szerződéssorhoz tartoznak sorrészletek, akkor ez az érték módosítható a sor részleteiben szereplő adóösszegek módosításával. Rögzített árú szerződéssor esetén ez az érték a periodikus számlázási mérföldkövekhez kapcsolódó adózás előtti összeg generálására szolgál. |
| **Szerződésben rögzített összeg adózás után** | A szerződéssor összege adózás után. Ez a mező csak olvasható, és számítása a következő: **Szerződött összeg + adó**. | Rögzített árú szerződéssor esetén ez az érték a periodikus számlázási mérföldkövekhez kapcsolódó adó generálására szolgál. |
| **Nem meghaladandó korlát** | A felhasználó szerkesztheti ezt a mezőt, és csak olyan projektalapú szerződéssorok esetén érhető el, amelyek számlázási módja idő és anyag értékre van beállítva. | A felhasználó szerkesztheti ezt a mezőt. Ha egy időhöz vagy anyaghoz tartozó tényadat erre a szerződéssorra hivatkozik, akkor tényadathoz tartozó összeg össze lesz vetve a szerződéssor nem túlléphető határértékével. Ez az értékelés a már elköltött és lekötött összegek figyelembe vételét követően fejeződik be. |
| **Ügyfél költségvetése** | Ez a mező szerkeszthető, és árajánlatból létrehozott projekt-szerződésben a program a az ajánlatsor kapcsolódó mezőjéből másolja át az értéket. | Ez a mező csak tájékoztatásra szolgál, és nincs későbbi jelentősége. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>A Projektalapú szerződéssorok Általános lapjának beállításaira vonatkozó ellenőrzési szabályok

1. szabály: Ha a **Hozzáadott feladatok** mező üres, vagy **Minden projekttevékenység** értékre van állítva , a projekt minden feladata szerepel a szerződéssoron.

2. szabály: Ha a **Hozzáadott feladatok** mező üres, vagy kifejezetten **Minden projektfeladat** értékre van beállítva, egy projekt vagy egy adott tranzakciós osztály egy szerződésnek csak egy projektalapú szerződéssorán szerepelhet.

3. szabály: Ha a **Hozzáadott feladatok** mező **Csak kiválasztott projektfeladatok** értékre van beállítva, egy projekt vagy egy adott tranzakciós osztály egy szerződésnek több projektalapú szerződéssorán szerepelhet.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Szerződés</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Szerződéssor</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Hozzáadott feladatok</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Idővel együtt</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Költséggel együtt</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Anyagokkal együtt</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Tartalmazás</strong>
                </p>
                <p>
                    <strong>Díj</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Érvényes/nem érvényes</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Ok</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Üres </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Nem érvényes </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Az 2. szabály megsértése. A P1 projektre vonatkozó időt, költséget, anyagokat és díjat az ÁS1 és ÁS2 szerződéssora is tartalmazza.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Üres </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Üres </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Nem érvényes </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Az 2. szabály megsértése. A P1 projektre vonatkozó időt, anyagokat és díjat az ÁS1 és ÁS2 szerződéssora is tartalmazza.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Üres </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Üres </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Érvényes </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
A P1 projektre vonatkozó időt, anyagokat és díjat az ÁS1 árajánlatsor tartalmazza.
                </p>
                <ul>
                    <li>
A P1 projektre vonatkozó költséget a CS2 tartalmazza.
                    </li>
                </ul>
                <p>
Nincs átfedés abban, hogy miket tartalmaznak az egyes szerződéssorok, így ez érvényes.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Üres </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Csak a kiválasztott feladatok </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Nem érvényes </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
A 2. szabály megsértése </p>
                <p>
A C1 tartalmazza a P1 projekttel kapcsolatos feladatok egy részhalmazának idejét, anyagait, költségeit és díjait.
                </p>
                <p>
A CL2 tartalmazza az egész P1 projektre vonatkozó időt, anyagokat, költségeket és díjakat, ezért átfedésben van a C1 sorral.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Üres </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Csak a kiválasztott feladatok </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Érvényes </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
A 3. szabály szerint </p>
                <p>
A C1 tartalmazza a P1 projekttel kapcsolatos feladatok egy részhalmazának idejét, költségeit, anyagait és díjait.
                </p>
                <p>
A CL2 tartalmazza a P1 projekttel kapcsolatos feladatok egy részhalmazának idejét, anyagait, költségeit és díjait.
                </p>
                <p>
Az egyetlen további ellenőrzés a CL1-es feladatok részhalmaza körül van, amely eltér a CL2-es feladatok részhalmazától, így biztosítva, hogy ne legyen semmilyen átfedés. Ezt a rendszer hajtja végre a feladatok társításakor.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Csak a kiválasztott feladatok </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
