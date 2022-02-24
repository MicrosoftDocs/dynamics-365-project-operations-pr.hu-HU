---
title: Az árajánlatsor számlázható összetevőinek konfigurálása
description: Ez a témakör a számlázható és nem számlázható összetevők beállításával kapcsolatban tartalmaz tájékoztatást a projekt alapú árajánlatok soraiban.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858296"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Az árajánlatsor felszámítható összetevőinek konfigurálása 

_**A következőre vonatkozik:** Egyszerű központi telepítés – proforma számlázás, Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A projektalapú ajánlati sor rendelkezhet *mellékelt* összetevőkkel és a *felszámítható* összetevőkkel.

A mellékelt összetevők a következőkre vonatkoznak:

  - Számlázási mód és ügyfél felosztások
  - Nem meghaladandó korlátok 
  - A projekt alapú ajánlatsor által meghatározott számlázási gyakorisági beállításai

A befoglalt összetevők egy részhalmaza a **Számlázási típus** mező segítségével állítható terhelhetőre. A **Számlázási típus** mező olyan értékkészlet, amely az ajánlatsorok környezetében az alábbi értékeket teszi lehetővé:

  - Felszámítható
  - Fel nem számítható

A felszámítható összetevők a feladatokon, szerepkörökön és tranzakciós kategóriákon határozhatók meg.

A felszámíthatóság az ajánlatsor feladataihoz van definiálva, és a sorban szereplő összes tranzakciós osztályra vonatkozik. Ha a szerződéssor **Feladatok belefoglalása** mezője üres, vagy a **Teljes projekt** értékre van állítva, a **Felszámítható feladatok** lap nem érhető el.

Az ajánlatsor szerepkörei meghatározott felszámíthatóság csak az **Idő** tranzakciós osztályra vonatkozik. Ha az **Idő belefoglalása** mező **Nem** értékre van állítva, a **Felszámítható szerepkörök** lap nem lesz elérhető.

Az ajánlati sor tranzakciós kategóriái meghatározott felszámíthatóság csak az **Költség** tranzakciós osztályra vonatkozik. Ha a **Költségek belefoglalása** mező **Nem** értékre van állítva, a **Számlázható kategóriák** lap nem lesz elérhető.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Projekttevékenység frissítése felszámítható vagy nem felszámítható értékre

A projekttevékenység egy projektalapú ajánlatsor kontextusában felszámítható vagy nem felszámítható lehet, így a következő beállításokat lehet használni.

Ha egy projekten alapuló ajánlati sor **Időt** és a **T1** feladatot tartalmazza, akkor a feladat számlázhatóként lesz az ajánlati sorhoz rendelve. Ha van egy második ajánlatsor , amely **Költségeket** tartalmaz , akkor a **T1** feladatot a szerződéssorok között nem felszámíthatóként társíthatja. Az eredmény az, hogy a feladathoz rögzített összes idő felszámítható, és a feladathoz rendelt minden költség nem felszámítható.

A feladatok számlázási típusa a projektalapú ajánlatsor **Számlázható feladatok** lapján állítható be az **Ajánlatisor-feladatok** alrács **Számlázási típus** mezőjének frissítésével. Másik lehetőségként frissítheti a projekttevékenységek számlázási típusát a **Számlázási típus** mezőben, a projekt számlázási beállítása alrácsán, amely a feladathoz társított ajánlati sorokat mutatja.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Szerepkör frissítése felszámítható vagy nem felszámítható értékre

A szerepkör egy adott, projekten alapuló ajánlati sor környezetében számlázható vagy nem számlázható lehet.

A szerepkör számlázási típusa a projektalapú ajánlatsor **Számlázható szerepkörök** lapján állítható be az **Számlázható szerepkörök** alrács **Számlázási típus** mezőjének frissítésével.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Tranzakciókategória frissítése felszámítható vagy nem felszámítható értékre

Egy tranzakciós kategória egy adott ajánlatsoron felszámítható vagy nem felszámítható lehet.

A tranzakció számlázási típusa a projektalapú ajánlatsor **Számlázható kategóriák** lapján állítható be az **Számlázható szerepkörök** alrács **Számlázási kategóriák** mezőjének frissítésével.

### <a name="resolve-chargeability"></a>A számlázhatóság feloldása
Az időre létrehozott becslés vagy tényadat csak akkor tekinthető felszámíthatónak, ha:

   - Az **Idő** szerepel az árajánlatsorban.
   - A **Szerepkör** az árajánlatsorban felszámíthatóként van konfigurálva.
   - A **Hozzáadott feladatok** érték **Kijelölt feladatok** elemre van állítva az árajánlatsoron. 

Ha ez a három dolog teljesül, akkor a **Feladat** felszámíthatóként konfigurálható. 

A költségre létrehozott becslés vagy tényadat csak akkor tekinthető felszámíthatónak, ha: 

   - A **Költség** szerepel az árajánlatsorban.
   - A **Tranzakciókategória** az árajánlatsorban felszámíthatóként van konfigurálva.
   - A **Hozzáadott feladatok** érték **Kijelölt feladatok** elemre van állítva az árajánlatsoron.

Ha ez a három dolog teljesül, akkor a **Feladat** felszámíthatóként konfigurálható. 

Az anyagra létrehozott becslés vagy tényadat csak akkor tekinthető felszámíthatónak, ha:

   - Az **Anyag** szerepel az árajánlatsorban.
   - A **Hozzáadott feladatok** érték **Kijelölt feladatok** elemre van állítva az árajánlatsoron.

Ha ez a két dolog teljesül, akkor a **Feladatot** felszámíthatóként kell konfigurálni. 


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
Számlázás egy tényleges Időhöz: Számlázható </p>
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
Felszámítható </p>
            </td>
            <td width="350" valign="top">
                <p>
Számlázás egy tényleges Időhöz: Számlázható </p>
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
