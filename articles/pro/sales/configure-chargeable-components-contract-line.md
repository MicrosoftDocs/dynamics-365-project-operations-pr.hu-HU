---
title: A projektalapú szerződéssor felszámítható összetevőinek konfigurálása
description: Ez a témakör tájékoztatást nyújt arról, hogyan lehet a felszámítható összetevőket felvenni a Project Operations szerződéssoraiba.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003724"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>A projektalapú szerződéssor felszámítható összetevőinek konfigurálása

_**A következőre vonatkozik:** Egyszerű központi telepítés – proforma számlázás, Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A projektalapú szerződéssor rendelkezik *mellékelt* összetevőkkel és a *felszámítható* összetevőkkel.

A mellékelt összetevők olyan összetevők, amelyek a következőkhöz kapcsolódnak:

  - Számlázási mód és ügyfél felosztások
  - Nem meghaladandó korlátok 
  - A projekt alapú szerződéssor által meghatározott számlázási gyakorisági beállításai

A befoglalt összetevők egy részhalmaza a **Számlázási típus** mező segítségével állítható terhelhetőre. A **Számlázási típus** mező olyan értékkészlet, amely a szerződéssorok környezetében az alábbi értékeket teszi lehetővé:

  - Felszámítható
  - Fel nem számítható

A felszámítható összetevők a feladatokon, szerepkörökön és tranzakciós kategóriákon határozhatók meg.

A felszámíthatóság a projekt szerződéssor feladataihoz van definiálva, és a sorban szereplő összes tranzakciós osztályra vonatkozik. Ha a szerződéssor **Feladatok belefoglalása** mezője üres, vagy a **Teljes projekt** értékre van állítva, a **Felszámítható feladatok** lap nem lesz elérhető.

A Project szerződéssor szerepkörei meghatározott felszámíthatóság csak az **Idő** tranzakciós osztályra vonatkozik. Ha a szerződéssor **Idő belefoglalása** mezője **Nem** értékre van állítva, a **Felszámítható feladatok** lap nem lesz elérhető.

A Project szerződéssor tranzakciós kategóriái meghatározott felszámíthatóság csak az **Költség** tranzakciós osztályra vonatkozik. Ha a szerződéssor **Kiadások belefoglalása** mezője **Nem** értékre van állítva, a **Felszámítható kategóriák** lap nem lesz elérhető.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Projekttevékenység frissítése felszámítható vagy nem felszámítható értékre

A projekttevékenység egy adott szerződéssor felszámítható vagy nem felszámítható lehet, így a következő beállításokat lehet használni:

Ha egy projekten alapuló szerződéssor **Idő** típusú, és egy bizonyos feladatot tartalmaz, akkor a **T1** a felszámíthatóként van hozzárendelve. Ha van egy második szerződéssor , amely **Költséget** tartalmaz , akkor a T1 feladatot a szerződéssorok között nem felszámíthatóként társíthatja. Az eredmény az, hogy a feladathoz rögzített összes idő felszámítható, és minden költség nem felszámítható.

A feladatok számlázási típusa a szerződéssor **Számlázható feladatok** lapján állítható be a szerződéssor-feladatok alrács **Számlázási típus** mezőjének frissítésével. Másik lehetőségként frissítheti a **Számlázási típus** mezőt, a projekt számlázási beállítása alrácsán, amely a feladathoz társított szerződéssorokat mutatja.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Szerepkör frissítése felszámítható vagy nem felszámítható értékre

Egy szerepkör egy adott szerződéssoron felszámítható vagy nem felszámítható lehet.

A szerepkör számlázási típusa a szerződéssor **Számlázható szerepkörök** lapján állítható be. Ehhez frissítse a **Számlázható szerepkörök** alrács **Számlázási típus** mezőjét.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Tranzakciókategória frissítése felszámítható vagy nem felszámítható értékre

Egy tranzakciós kategória egy adott szerződéssoron felszámítható vagy nem felszámítható lehet.

A tranzakció számlázási típusa a projektalapú szerződéssor **Számlázható kategóriák** lapján állítható be. Ehhez frissítse a **Számlázható kategóriák** alrács **Számlázási típus** mezőjét.

### <a name="resolve-chargeability"></a>A számlázhatóság feloldása

Az időre létrehozott becslés vagy tényadat csak akkor tekinthető felszámíthatónak, ha:

   - Az **Idő** szerepel a szerződéssorban.
   - A **Szerepkör** a szerződéssorban felszámíthatóként van konfigurálva.
   - A **Hozzáadott feladatok** érték **Kijelölt feladatok** elemre van állítva a szerződéssoron.
 
 Ha ez a három dolog teljesül, akkor a feladat felszámíthatóként konfigurálható. 

A költségre létrehozott becslés vagy tényadat csak akkor tekinthető felszámíthatónak, ha:

   - A **Költség** szerepel a szerződéssorban
   - A **Tranzakciókategória** a szerződéssorban felszámíthatóként van konfigurálva
   - A **Hozzáadott feladatok** érték **Kijelölt feladat** elemre van állítva a szerződéssoron
  
 Ha ez a három dolog teljesül, akkor a **Feladat** felszámíthatóként konfigurálható. 

Az anyagra létrehozott becslés vagy tényadat csak akkor tekinthető felszámíthatónak, ha:

   - Az **Anyagok** szerepel a szerződéssorban
   - A **Hozzáadott feladatok** érték **Kijelölt feladatok** elemre van állítva a szerződéssoron

Ha ez a két dolog teljesül, akkor a **Feladat** felszámíthatóként konfigurálható. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Időt tartalmaz</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Költséget tartalmaz</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Anyagokkal együtt</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Hozzáadott feladatok</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Szerepkör</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Kategória</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Feladatok</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Felszámolhatósági hatás</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Igen </p>
            </td>
            <td width="78" valign="top">
                <p>
Igen </p>
            </td>
            <td width="63" valign="top">
                <p>
Igen </p>
            </td>
            <td width="75" valign="top">
                <p>
Teljes projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Felszámítható </p>
            </td>
            <td width="70" valign="top">
                <p>
Felszámítható </p>
            </td>
            <td width="65" valign="top">
                <p>
Nem állítható be </p>
            </td>
            <td width="350" valign="top">
                <p>
Számlázás egy tényleges Időhöz: <strong>Számítható</strong>
                </p>
                <p>
Számlázás típusa egy tényleges kiadáshoz: <strong>Számítható</strong>
                </p>
                <p>
Számlázási típus a tényanyagon: <strong>Számítható</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Igen </p>
            </td>
            <td width="78" valign="top">
                <p>
Igen </p>
            </td>
            <td width="63" valign="top">
                <p>
Igen </p>
            </td>
            <td width="75" valign="top">
                <p>
Csak a kiválasztott feladatok </p>
            </td>
            <td width="65" valign="top">
                <p>
Felszámítható </p>
            </td>
            <td width="70" valign="top">
                <p>
Felszámítható </p>
            </td>
            <td width="65" valign="top">
                <p>
Felszámítható </p>
            </td>
            <td width="350" valign="top">
                <p>
Számlázás egy tényleges Időhöz: <strong>Számítható</strong>
                </p>
                <p>
Számlázás típusa egy tényleges kiadáshoz: <strong>Számítható</strong>
                </p>
                <p>
Számlázási típus a tényanyagon: <strong>Számítható</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Igen </p>
            </td>
            <td width="78" valign="top">
                <p>
Igen </p>
            </td>
            <td width="63" valign="top">
                <p>
Igen </p>
            </td>
            <td width="75" valign="top">
                <p>
Csak a kiválasztott feladatok </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nem számítható</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Felszámítható </p>
            </td>
            <td width="65" valign="top">
                <p>
Felszámítható </p>
            </td>
            <td width="350" valign="top">
                <p>
Számlázás egy tényleges Időhöz: <strong>Fel nem számítható</strong>
                </p>
                <p>
Számlázás típusa egy tényleges kiadáshoz: Számlázható </p>
                <p>
Számlázási típus a tényanyagon: Felszámítható </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Igen </p>
            </td>
            <td width="78" valign="top">
                <p>
Igen </p>
            </td>
            <td width="63" valign="top">
                <p>
Igen </p>
            </td>
            <td width="75" valign="top">
                <p>
Csak a kiválasztott feladatok </p>
            </td>
            <td width="65" valign="top">
                <p>
Felszámítható </p>
            </td>
            <td width="70" valign="top">
                <p>
Felszámítható </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nem számítható</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Számlázás egy tényleges Időhöz: <strong>Fel nem számítható</strong>
                </p>
                <p>
Számlázás típusa egy tényleges költséghez: <strong>Nem számítható</strong>
                </p>
                <p>
Számlázás típusa egy tényleges adathoz: <strong>Nem számítható</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Igen </p>
            </td>
            <td width="78" valign="top">
                <p>
Igen </p>
            </td>
            <td width="63" valign="top">
                <p>
Igen </p>
            </td>
            <td width="75" valign="top">
                <p>
Csak a kiválasztott feladatok </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nem számítható</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Felszámítható </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nem számítható</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Számlázás egy tényleges Időhöz: <strong>Fel nem számítható</strong>
                </p>
                <p>
Számlázás típusa egy tényleges költséghez: <strong>Nem számítható</strong>
                </p>
                <p>
Számlázás típusa egy tényleges adathoz: <strong> Nem számítható</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Igen </p>
            </td>
            <td width="78" valign="top">
                <p>
Igen </p>
            </td>
            <td width="63" valign="top">
                <p>
Igen </p>
            </td>
            <td width="75" valign="top">
                <p>
Csak a kiválasztott feladatok </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nem számítható</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nem számítható</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Felszámítható </p>
            </td>
            <td width="350" valign="top">
                <p>
Számlázás egy tényleges Időhöz: <strong>Fel nem számítható</strong>
                </p>
                <p>
Számlázás típusa egy tényleges költséghez: <strong> Nem számítható</strong>
                </p>
                <p>
Számlázási típus a tényanyagon: Felszámítható </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Igen </p>
            </td>
            <td width="63" valign="top">
                <p>
Igen </p>
            </td>
            <td width="75" valign="top">
                <p>
Teljes projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Nem állítható be </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Felszámítható</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nem állítható be </p>
            </td>
            <td width="350" valign="top">
                <p>
Számlázás egy tényleges időhöz: <strong>Nem érhető el</strong>
                </p>
                <p>
Számlázás típusa egy tényleges kiadáshoz: Számlázható </p>
                <p>
Számlázási típus a tényanyagon: Felszámítható </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Igen </p>
            </td>
            <td width="63" valign="top">
                <p>
Igen </p>
            </td>
            <td width="75" valign="top">
                <p>
Teljes projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Nem állítható be </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nem számítható</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nem állítható be </p>
            </td>
            <td width="350" valign="top">
                <p>
Számlázás egy tényleges időhöz: <strong>Nem érhető el</strong>
                </p>
                <p>
Számlázás típusa egy tényleges költséghez: <strong> Nem számítható</strong>
                </p>
                <p>
Számlázási típus a tényanyagon: Felszámítható </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Igen </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Igen </p>
            </td>
            <td width="75" valign="top">
                <p>
Teljes projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Felszámítható </p>
            </td>
            <td width="70" valign="top">
                <p>
Nem állítható be </p>
            </td>
            <td width="65" valign="top">
                <p>
Nem állítható be </p>
            </td>
            <td width="350" valign="top">
                <p>
Számlázás egy tényleges Időhöz: Számlázható </p>
                <p>
Számlázás típusa egy tényleges költséghez: <strong>Nem érhető el</strong>
                </p>
                <p>
Számlázási típus a tényanyagon: Felszámítható </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Igen </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Igen </p>
            </td>
            <td width="75" valign="top">
                <p>
Teljes projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nem számítható</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Nem állítható be </p>
            </td>
            <td width="65" valign="top">
                <p>
Nem állítható be </p>
            </td>
            <td width="350" valign="top">
                <p>
Számlázás egy tényleges Időhöz: <strong>Fel nem számítható</strong>
                </p>
                <p>
Számlázás típusa egy tényleges költséghez: <strong>Nem érhető el</strong>
                </p>
                <p>
Számlázási típus a tényanyagon: Felszámítható </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Igen </p>
            </td>
            <td width="78" valign="top">
                <p>
Igen </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Teljes projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Felszámítható </p>
            </td>
            <td width="70" valign="top">
                <p>
Felszámítható </p>
            </td>
            <td width="65" valign="top">
                <p>
Nem állítható be </p>
            </td>
            <td width="350" valign="top">
                <p>
Számlázás egy tényleges Időhöz: Számlázható </p>
                <p>
Számlázás típusa egy tényleges kiadáshoz: Számlázható </p>
                <p>
Számlázás típusa egy tényleges anyaghoz: <strong>Nem érhető el</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Igen </p>
            </td>
            <td width="78" valign="top">
                <p>
Igen </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Teljes projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nem számítható</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nem számlázható</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nem állítható be </p>
            </td>
            <td width="350" valign="top">
                <p>
Számlázás egy tényleges Időhöz: <strong>Fel nem számítható</strong>
                </p>
                <p>
Számlázás típusa egy tényleges költséghez:<strong> Nem számítható </strong>
                </p>
                <p>
Számlázás típusa egy tényleges anyaghoz:<strong> Nem érhető el</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
