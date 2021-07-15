---
title: Projekt árajánlatsorok áttekintése
description: Ez témakör az árajánlatsorok projektmunkához történő használatáról nyújt tájékoztatást.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: c585bbc55119e678a4f75f5dfe8966a436db1a34
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368074"
---
# <a name="project-quote-lines-overview"></a>Projekt árajánlatsorok áttekintése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A projektalapú ajánlati sorok úgy vannak kialakítva, hogy elősegítsék az aktivitásra vonatkozó projektmunka becslését. A projektalapú ajánlatsor felépítése a projektbecslésekhez a következő fogalmakkal bővül:

- Számlázási mód
- Projektleképezés
- Szerepeltetett tranzakciós osztályok
- Nem meghaladandó korlát
- Felszámíthatósági beállítás
- Becslés az ajánlati sor részleteinek használatával
- Árajánlatsor ügyfelei

A következő táblázat a projektalapú árajánlatsor **Általános** lapján található mezőkre vonatkozó információkat tartalmaz. Ezek a mezők segítséget nyújtanak a projektmunka részletes, jól felépített becslési alapjainak kialakításában.

| **Mező** | **Leírás** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- |
| Adatfolyam neve | Az árajánlatsor neve, amely segít azonosítani a becslés alatt álló ajánlat elkülönített összetevőjét. | A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja az árajánlat megnyerése után. |
| Számlázási mód | A lehetőségből létrehozott árajánlaton ezt az értéket a rendszer a lehetőség sor megfelelő mezőjéből másolja át. Ez a mező a Dynamics 365 Project Operations által támogatott két fő szerződési modellt tartalmazza:</br>- Rögzített ár</br>- Idő és anyag| A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után. |
| Project | Ezzel a nem kötelező mezővel azonosíthatja azt a projektet, amelyet a program az adott tevékenységgel kapcsolatos munkára fog használni. Amikor egy projektet egy ajánlati sorhoz rendelnek, az segítséget nyújt a felszámítható feladatok beállításában, valamint a projekten alapuló becslést hoz árajánlatsori részletekként az árajánlatsorba. Ha egy projekt nincs leképezve projektalapú árajánlatsorra, a becslést kézzel kell létrehozni az egyes árajánlati sorok részleteinek létrehozásával. | A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után. |
| Idővel együtt | Az **Igen**/**Nem** jelző azt jelzi, hogy a kiválasztott projekten az időtranzakciók és a munkaerőköltségek szerepelni fognak-e az árajánlatsorban szereplő becslésben. A **Nem** érték azt jelzi, hogy az időtranzakciók és a munkaerőköltségek nem fognak szerepelni az árajánlatsorban szereplő becslésben. Az **Igen** érték azt jelzi, hogy az időtranzakciók és a munkaerőköltségek szerepelni fognak az árajánlatsorban szereplő becslésben. | A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után. |
| Költséggel együtt | Az **Igen**/**Nem** jelző azt jelzi, hogy a kiválasztott projekten a kiadási költségek szerepelni fognak-e az árajánlatsorban szereplő becslésben. A **Nem** érték azt jelzi, hogy a kiadási költségek nem fognak szerepelni az árajánlatsorban szereplő becslésben. Az **Igen** érték azt jelzi, hogy a kiadási költségek szerepelni fognak az árajánlatsorban szereplő becslésben. | A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után. |
| Díjjal együtt | Az **Igen**/**Nem** jelző azt jelzi, hogy a kiválasztott projekten a díjak szerepelni fognak-e az árajánlatsorban szereplő becslésben. A **Nem** érték azt jelzi, hogy a díjak nem fognak szerepelni az árajánlatsorban szereplő becslésben. Az **Igen** érték azt jelzi, hogy a díjak szerepelni fognak az árajánlatsorban szereplő becslésben. | A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után. |
| Megajánlott összeg | Ez az összeg jelenik meg árajánlatként az ügyfélnek az összes előrejelzett munka esetében a projektalapú árajánlatsoron. A lehetőségből létrehozott árajánlaton ezt az értéket a rendszer a lehetőség sor **Ügyfél költségvetése** mezőjéből másolja át. Ha a projektalapú árajánlatsor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és az árajánlatsor részleteiben szereplő összegből kerül összesítésre. | A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után. |
| Becsült adó | Ez egy szerkeszthető mező, amellyel a felhasználó hozzáadhatja a becsült adót az árajánlatsorhoz. Ha a projektalapú árajánlatsor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és az árajánlatsor részleteiben szereplő adóösszegből kerül összesítésre. | A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után. |
| Árajánlat összege adózás után | Ez a mező az árajánlatsor adózás utáni összege, amely csak olvasható. Az ebben a mezőben szereplő összeget a program *Árajánlat összege + adó* képlettel számítja ki. | A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után. |
| Nem meghaladandó korlát | Ez a mező szerkeszthető, és csak azokban a projektalapú árajánlatsorokban érhető el, amelyek **Idő és anyag** számlázási móddal rendelkeznek. | A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után. |
| Ügyfél költségvetése | A mező szerkeszthető, és a rendszer a lehetőség sor megfelelő mezőjéből másolja át, ha az árajánlat egy lehetőségből lett létrehozva. | A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>A projektalapú árajánlatsorok Általános lapján található mezőkre vonatkozó ellenőrzési szabályok

**1. szabály**: A kijelölt projekt bizonyos tranzakciós osztályai csak az árajánlat egy projektalapú árajánlatsorában szerepelhetnek.

**2. szabály**: Ha a lehetőség több árajánlattal rendelkezik, akkor különböző árajánlatokból származó ajánlati sorok szerepelhetnek, amelyek ugyanarra a projektre hivatkoznak, és ugyanazt a tranzakciós osztályt tartalmazzák.

**3. szabály**: Ha az ajánlatok nem ugyanahhoz a lehetőséghez tartoznak, akkor nem tartalmazhatják ugyanazokat a projekt- és tranzakciós osztályokat.

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Lehetőség</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Ajánlat</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Árajánlatsor</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
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
                    <strong>Ezzel együtt</strong>
                </p>
                <p>
                    <strong>Díj</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Érvényes/nem érvényes</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Ok</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
L1 </p>
            </td>
            <td width="41" valign="top">
                <p>
N1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ÁS1 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Nem érvényes </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Az 1. szabály megsértése. A P1 projektre vonatkozó időt, költséget és díjat mindkét árajánlatsor (ÁS1 és ÁS2) tartalmazza.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
L1 </p>
            </td>
            <td width="41" valign="top">
                <p>
N1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ÁS2 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
L1 </p>
            </td>
            <td width="41" valign="top">
                <p>
N1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ÁS1 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="48" valign="top">
                <p>
Nincs </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Nem érvényes </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Az 1. szabály megsértése. A P1 projektre vonatkozó időt és díjakat mindkét árajánlatsor (ÁS1 és ÁS2) tartalmazza.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
L1 </p>
            </td>
            <td width="41" valign="top">
                <p>
N1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ÁS2 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
L1 </p>
            </td>
            <td width="41" valign="top">
                <p>
N1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ÁS1 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="48" valign="top">
                <p>
Nincs </p>
            </td>
            <td width="42" valign="top">
                <p>
Igen </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Érvényes </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
A P1 projektre vonatkozó időt és díjat az ÁS1 tartalmazza.
A P1 projektre vonatkozó költséget az ÁS2 tartalmazza.
Az egyes árajánlatsorokban szereplő elemek között nincs átfedés, így az érvényes.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
L1 </p>
            </td>
            <td width="41" valign="top">
                <p>
N1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ÁS2 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Nincs </p>
            </td>
            <td width="48" valign="top">
                <p>
Igen </p>
            </td>
            <td width="42" valign="top">
                <p>
Nincs </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
L1 </p>
            </td>
            <td width="41" valign="top">
                <p>
N1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ÁS1 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Nem érvényes </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
A fenti 1. szabály megsértése </p>
                <p>
Az Á1 tartalmazza a teljes P1 projektre vonatkozó időt, költségeket és díjakat.
                </p>
                <p>
Az ÁS2 tartalmazza a teljes P1 teljes projektre vonatkozó időt, költségeket és díjakat, és átfedésben van az Á1-ben szereplő elemekkel.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
L1 </p>
            </td>
            <td width="41" valign="top">
                <p>
N1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ÁS2 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
L1 </p>
            </td>
            <td width="41" valign="top">
                <p>
N1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ÁS1 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
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
            <td width="54" valign="top">
                <p>
Érvényes </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
A 2. szabály alapján az Á1 és Á2 két árajánlat ugyanarra a lehetőségre, így mindkettő becsülheti egy projekt ugyanazon összetevőit.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
L1 </p>
            </td>
            <td width="41" valign="top">
                <p>
N2 </p>
            </td>
            <td width="42" valign="top">
                <p>
ÁS1 az Á2-n: </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
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
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
L1 </p>
            </td>
            <td width="41" valign="top">
                <p>
N1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ÁS1 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
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
            <td width="54" valign="top">
                <p>
Érvényes </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
A 3. szabály alapján az Á1 és Á2 két árajánlat különböző lehetőségekre, így nem becsülhetik ugyanazon projekt azonos összetevőit.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
L2 </p>
            </td>
            <td width="41" valign="top">
                <p>
N1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ÁS1 </p>
            </td>
            <td width="42" valign="top">
                <p>
I1 </p>
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
            <td width="54" valign="top">
                <p>
Nem érvényes </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
