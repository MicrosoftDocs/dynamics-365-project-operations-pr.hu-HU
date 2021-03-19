---
title: A projektalapú szerződéssor felszámítható összetevőinek konfigurálása
description: Ez a témakör a számlázható és nem számlázható összetevőkkel kapcsolatban tartalmaz tájékoztatást a szerződéssorokban.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2266d8e0fe998e7161ede4cb4eaf7d3c70c54f71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278691"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>A projektalapú szerződéssor felszámítható összetevőinek konfigurálása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A projektalapú szerződéssor rendelkezhet mellékelt felszámítható összetevőkkel és nem felszámítható összetevőkkel.

A befoglalt összetevőkre a számlázási mód, az ügyfél felosztása, a nem meghaladandó korlátok és számlázási gyakoriság beállításai érvényesek, amelyek a projektalapú szerződéssoron vannak definiálva.

A befoglalt összetevők egy részhalmaza a **Számlázási típus** mező frissítésével állítható terhelhetőre.

A felszámítható összetevők a szerepkörökön és tranzakciós kategóriákon határozhatók meg.

A Project szerződéssor szerepkörei esetében a szerepkörhöz meghatározott felszámíthatóság csak az **Idő** tranzakciós osztályra vonatkozik. Ha az **Idő belefoglalása** **Nem** értékre van állítva egy projekt szerződéssorán, a **Felszámítható szerepkörök** lap nem lesz elérhető.

A Project szerződéssor tranzakciós kategóriái meghatározott felszámíthatóság csak az **Költség** tranzakciós osztályra vonatkozik. Ha a **Költségek belefoglalása** **Nem** értékre van állítva egy projekt szerződéssorán, a **Felszámítható kategóriák** lap nem lesz elérhető.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Szerepkör frissítése felszámítható vagy nem felszámítható értékre

Egy szerepkör egy adott projektalapú szerződéssoron felszámítható vagy nem felszámítható lehet.

A projektalapú ajánlatsor **Számlázható szerepkörök** lapján állítható be az **Számlázható szerepkörök** alrács **Számlázási típus** mezőjén frissítse a számlázási típusát egy szerepkörhöz.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Tranzakciókategória frissítése felszámítható vagy nem felszámítható értékre

Egy tranzakciós kategória egy adott projektalapú szerződéssoron felszámítható vagy nem felszámítható lehet.

A projektalapú ajánlatsor **Számlázható kategóriák** lapján állítható be az **Számlázható szerepkörök** alrács **Számlázási típus** mezőjén frissítse a számlázási típusát egy tranzakcióhoz.

### <a name="resolve-chargeability"></a>A számlázhatóság feloldása

Az időhöz létrehozott becslések vagy tényleges adatok csak akkor tekinthetők felszámíthatónak , ha az Idő szerepel a szerződéssoron, és ha a Szerepkör a szerződéssoron felszámíthatónak van konfigurálva.

A költséghez létrehozott becslések vagy tényleges adatok csak akkor lesznek tekinthetők felszámíthatónak , ha a költség szerepel a szerződéssoron és ha a a Tranzakciókategória a szerződéssoron felszámíthatónak van konfigurálva.

| Időt tartalmaz | Költséget tartalmaz | Szerepkör | Kategória | Feladatok |
| --- | --- | --- | --- | --- |
| Igen | Igen | Felszámítható | Felszámítható | Számlázás egy tényleges Időhöz: Számlázható </br>Számlázás típusa egy tényleges kiadáshoz: Számlázható |
| Igen | Igen | Nem számlázható | Felszámítható | Számlázás egy tényleges Időhöz: Nem számlázható </br>Számlázás típusa egy tényleges kiadáshoz: Számlázható |
| Igen | Igen | Nem számlázható | Nem számlázható | Számlázás egy tényleges Időhöz: Nem számlázható </br>Számlázás típusa egy tényleges kiadáshoz: Nem számlázható |
| Nincs | Igen | Nem állítható be | Felszámítható | Számlázás egy tényleges Időhöz: Nem érhető el </br>Számlázás típusa egy tényleges kiadáshoz:Számlázható |
| Nincs | Igen | Nem állítható be | Nem számlázható | Számlázás egy tényleges Időhöz: Nem érhető el </br>Számlázás típusa egy tényleges kiadáshoz: Nem számlázható |
| Igen | Nincs | Felszámítható | Nem állítható be | Számlázás egy tényleges Időhöz: Számlázható </br>Számlázás típusa egy tényleges kiadáshoz: Nem érhető el |
| Igen | Nincs | Nem számlázható | Nem állítható be | Számlázás egy tényleges Időhöz: Nem számlázható </br> Számlázás típusa egy tényleges kiadáshoz: Nem érhető el |


[!INCLUDE[footer-include](../includes/footer-banner.md)]