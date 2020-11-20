---
title: Az árajánlatsor felszámítható összetevőinek konfigurálása - Lite
description: Ez a témakör a számlázható és nem számlázható összetevők beállításával kapcsolatban tartalmaz tájékoztatást a projekt alapú árajánlatok soraiban.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5d751ecd66975135c4afd5f18e896251ff34990
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177109"
---
# <a name="configure-the-chargeable-components-of-a-quote-line---lite"></a>Az árajánlatsor felszámítható összetevőinek konfigurálása - Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

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

A projekttevékenység egy projektalapú ajánlatsor kontextusában felszámítható vagy nem felszámítható lehet, így a következő beállításokat lehet használni:

Ha egy projekten alapuló ajánlati sor **Időt** és a **T1** feladatot tartalmazza, akkor a feladat számlázhatóként lesz az ajánlati sorhoz rendelve. Ha van egy második ajánlatsor , amely **Költségeket** tartalmaz , akkor a **T1** feladatot a szerződéssorok között nem felszámíthatóként társíthatja. Az eredmény az, hogy a feladathoz rögzített összes idő felszámítható, és a feladathoz rendelt minden költség nem felszámítható.

A feladatok számlázási típusa a projektalapú ajánlatsor **Számlázható feladatok** lapján állítható be az **Ajánlatisor-feladatok** alrács **Számlázási típus** mezőjének frissítésével. Másik lehetőségként frissítheti a projekttevékenységek számlázási típusát a **Számlázási típus** mezőben, a projekt számlázási beállítása alrácsán, amely a feladathoz társított ajánlati sorokat mutatja.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Szerepkör frissítése felszámítható vagy nem felszámítható értékre

A szerepkör egy adott, projekten alapuló ajánlati sor környezetében számlázható vagy nem számlázható lehet.

A szerepkör számlázási típusa a projektalapú ajánlatsor **Számlázható szerepkörök** lapján állítható be az **Számlázható szerepkörök** alrács **Számlázási típus** mezőjének frissítésével.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Tranzakciókategória frissítése felszámítható vagy nem felszámítható értékre

Egy tranzakciós kategória egy adott ajánlatsoron felszámítható vagy nem felszámítható lehet.

A tranzakció számlázási típusa a projektalapú ajánlatsor **Számlázható kategóriák** lapján állítható be az **Számlázható szerepkörök** alrács **Számlázási kategóriák** mezőjének frissítésével.

### <a name="resolve-chargeability"></a>A számlázhatóság feloldása
Az időhöz létrehozott becslések vagy tényleges adatok csak akkor tekinthetők felszámíthatónak , ha az **Idő** szerepel az ajánlatsoron és ha a **Feladat** és a **Szerepkör** az ajánlatsoron felszámíthatónak van konfigurálva.

A költséghez létrehozott becslések vagy tényleges adatok csak akkor tekinthetők felszámíthatónak , ha a **Költség** szerepel az ajánlatsoron és ha a **Feladat** és a **Tranzakciókategória** a szerződéssoron felszámíthatónak van konfigurálva.

| Időt tartalmaz | Költséget tartalmaz | Hozzáadott feladatok | Szerepkör | Kategória | Feladatok | Számlázás |
| --- | --- | --- | --- | --- | --- | --- |
| Igen | Igen | Teljes projekt | Felszámítható | Felszámítható | Nem állítható be | Számlázás egy tényleges Időhöz: Számlázható </br>Számlázás típusa egy tényleges kiadáshoz: Számlázható |
| Igen | Igen | Csak a kiválasztott feladatok | Felszámítható | Felszámítható | Felszámítható | Számlázás egy tényleges Időhöz: Számlázható</br>Számlázás típusa egy tényleges kiadáshoz: Számlázható |
| Igen | Igen | Csak a kiválasztott feladatok | Fel nem számítható | Felszámítható | Felszámítható | Számlázás egy tényleges Időhöz: Nem számlázható</br>Számlázás típusa egy tényleges kiadáshoz: Számlázható |
| Igen | Igen | Csak a kiválasztott feladatok | Felszámítható | Felszámítható | Nem számlázható | Számlázás egy tényleges Időhöz: Nem számlázható</br> Számlázás típusa egy tényleges kiadáshoz: Nem számlázható |
| Igen | Igen | Csak a kiválasztott feladatok | Nem számlázható | Felszámítható | Nem számlázható | Számlázás egy tényleges Időhöz: Nem számlázható</br> Számlázás típusa egy tényleges kiadáshoz: Nem számlázható |
| Igen | Igen | Csak a kiválasztott feladatok | Nem számlázható | Nem számlázható | Felszámítható | Számlázás egy tényleges Időhöz: Nem számlázható</br> Számlázás típusa egy tényleges kiadáshoz: Nem számlázható |
| Nincs | Igen | Teljes projekt | Nem állítható be | Felszámítható | Nem állítható be | Számlázás egy tényleges Időhöz: Nem érhető el </br>Számlázás típusa egy tényleges kiadáshoz: Számlázható |
| Nincs | Igen | Teljes projekt | Nem állítható be | Fel nem számítható | Nem állítható be | Számlázás egy tényleges Időhöz: Nem érhető el </br>Számlázás típusa egy tényleges kiadáshoz: Nem számlázható |
| Igen | Nincs | Teljes projekt | Felszámítható | Nem állítható be | Nem állítható be | Számlázás egy tényleges Időhöz: Számlázható</br>Számlázás típusa egy tényleges kiadáshoz: Nem érhető el |
| Igen | Nincs | Teljes projekt | Nem számlázható | Nem állítható be | Nem állítható be | Számlázás egy tényleges Időhöz: Nem számlázható </br>Számlázás típusa egy tényleges kiadáshoz: Nem érhető el |
