---
title: A projektalapú szerződéssor felszámítható összetevőinek konfigurálása – Lite
description: Ez a témakör tájékoztatást nyújt arról, hogyan lehet a felszámítható összetevőket felvenni a Project Operations szerződéssoraiba.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 46429c94ca9aa1ebbbe9fc689a9a5bd6c52dc59e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177154"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>A projektalapú szerződéssor felszámítható összetevőinek konfigurálása – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

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

Az időhöz létrehozott becslések vagy tényleges adatok csak akkor tekinthetők felszámíthatónak , ha az **Idő** szerepel a szerződéssoron és ha a **Feladat** és a **Szerepkör** a szerződéssoron felszámíthatónak van konfigurálva.

A költséghez létrehozott becslések vagy tényleges adatok csak akkor tekinthetők felszámíthatónak , ha a **Költség** szerepel a szerződéssoron és ha a **Feladat** és a **Tranzakció** kategória a szerződéssoron felszámíthatónak van konfigurálva.


| Időt tartalmaz | Költséget tartalmaz | Feladatokat tartalmaz | Szerepkör           | Kategória       | Feladatok                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Igen           | Igen              | Teljes projekt | Felszámítható     | Felszámítható     | Számlázás egy tényleges Időhöz: **Számlázható** </br> Számlázás típusa egy tényleges kiadáshoz: **Számlázható**           |
| Igen           | Igen              | Kiválasztott feladatok | Felszámítható     | Felszámítható     | Számlázás egy tényleges Időhöz: **Számlázható** </br> Számlázás típusa egy tényleges kiadáshoz: **Számlázható**           |
| Igen           | Igen              | Kiválasztott feladatok | Fel nem számítható | Felszámítható     | Számlázás egy tényleges Időhöz: **Nem számlázható** </br> Számlázás típusa egy tényleges kiadáshoz: **Számlázható**       |
| Igen           | Igen              | Kiválasztott feladatok | Felszámítható     | Felszámítható     | Számlázás egy tényleges Időhöz: **Nem számlázható** </br> Számlázás típusa egy tényleges kiadáshoz: **Nem számlázható** |
| Igen           | Igen              | Kiválasztott feladatok | Fel nem számítható | Felszámítható     | Számlázás egy tényleges Időhöz: **Nem számlázható** </br> Számlázás típusa egy tényleges kiadáshoz: **Nem számlázható** |
| Igen           | Igen              | Kiválasztott feladatok | Fel nem számítható | Fel nem számítható | Számlázás egy tényleges Időhöz: **Nem számlázható** </br> Számlázás típusa egy tényleges kiadáshoz: **Nem számlázható** |
| Nincs            | Igen              | Teljes projekt | Nem állítható be   | Felszámítható     | Számlázás egy tényleges Időhöz: **Nem érhető el**</br>Számlázás típusa egy tényleges kiadáshoz: **Számlázható**          |
| Nincs            | Igen              | Teljes projekt | Nem állítható be   | Fel nem számítható | Számlázás egy tényleges Időhöz: **Nem érhető el**</br> Számlázás típusa egy tényleges kiadáshoz: **Nem számlázható**     |
| Igen           | Nincs               | Teljes projekt | Felszámítható     | Nem állítható be   | Számlázás egy tényleges Időhöz: **Számlázható** </br> Számlázás típusa egy tényleges kiadáshoz: **Nem érhető el**        |
| Igen           | Nincs               | Teljes projekt | Fel nem számítható | Nem állítható be   | Számlázás egy tényleges Időhöz: **Nem számlázható** </br>Számlázás típusa egy tényleges kiadáshoz: **Nem érhető el**   |
