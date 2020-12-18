---
title: A projektalapú árajánlatsor felszámítható összetevőinek konfigurálása
description: Ez a témakör a projektenalapú ajánlatsorokban szereplő, számlázható és nem számlázható összetevőkkel kapcsolatban tartalmaz tájékoztatást.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 36765ab3687a8aaf3ae4a631516a1d61c14e981e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642546"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>A projektalapú árajánlatsor felszámítható összetevőinek konfigurálása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A projektalapú ajánlati sorok tartalmazhatnak számlázható és nem számlázható összetevőket.

A befoglalt összetevőkre a számlázási mód, az ügyfél felosztása, nem meghaladható határértékek és számlázási gyakoriság beállításai vonatkoznak, amelyek a projektalapú ajánlatsoron vannak meghatározva.
A befoglalt összetevők egy részhalmaza a **Számlázási típus** használatával számlázhatóként jelölhető meg . Az ajánlati sor környezetében a **Számlázás típusa** mezőben a következő lehetőségek közül választhat:

   - Felszámítható
   - Nem számlázható

A felszámítható összetevők a szerepkörökön és tranzakciós kategóriákon határozhatók meg.

A projekt ajánlati sor szerepkörein definiált díj csak az **Idő** tranzakciós osztályra vonatkozik. Ha egy projektajánlat sora esetében az **Idő belefoglalása** = **Nem**, a **Számlázható szerepkörök** lap nem érhető el.

A projekt ajánlati sor tranzakciós kategóriáin definiált számlázhatóság csak a **Kiadása** tranzakciós osztályra vonatkozik. Ha egy projektajánlat sora esetében a **Kiadások belefoglalása** = **Nem**, a **Számlázható kategóriák** lap nem érhető el.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Szerepkör frissítése felszámítható vagy nem felszámítható értékre
A szerepkör egy projekten alapuló ajánlati soron lehet számlázható vagy nem számlázható. A szerepkörön szereplő számlázási típus a projektalapú ajánlati sor **Számlázható szerepkörök** lapján állítható be. Ehhez frissítse a **Számlázható szerepkörök** alrács **Számlázási típus** alrácsát. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Tranzakciókategória frissítése felszámítható vagy nem felszámítható értékre
A tranzakciós kategória egy projekten alapuló ajánlati soron lehet számlázható vagy nem számlázható. A tranzakción szereplő számlázási típus a projektalapú ajánlati sor **Számlázható kategóriák** lapján állítható be. Ehhez frissítse a **Számlázható kategóriák** alrács **Számlázási típus** mezőjét. 

## <a name="resolve-chargeability"></a>A számlázhatóság feloldása

Az időhöz létrehozott elhatárolás vagy tényleges érték csak akkor lehet számlázható, ha az idő szerepel az ajánlati sorban, és ha a szerepkör a számlázhatóként van konfigurálva.
Egy költséghez létrehozott elhatárolás vagy tényleges érték csak akkor lehet számlázható, ha a költség szerepel az ajánlati sorban, és ha a tranzakciós kategória a számlázhatóként van konfigurálva. Az alábbi táblázat azt mutatja be, mi az alapértelmezett számlázhatóság az egyes tényadatokon. Az alapértelmezett értékek a befoglalt összetevőkön és az ajánlati sorban beállított számlázási típuson alapulnak.

| Időt tartalmaz | Költséget tartalmaz | Szerepkör | Kategória | Feladatok |
| --- | --- | --- | --- | --- |
| Igen | Igen | Felszámítható | Felszámítható | Számlázás egy tényleges Időhöz: Számlázható </br>Számlázás típusa egy tényleges kiadáshoz: Számlázható |
| Igen | Igen | Nem számlázható | Felszámítható | Számlázás egy tényleges Időhöz: Nem számlázható </br>Számlázás típusa egy tényleges kiadáshoz: Számlázható |
| Igen | Igen | Nem számlázható | Nem számlázható | Számlázás egy tényleges Időhöz: Nem számlázható </br>Számlázás típusa egy tényleges kiadáshoz: Nem számlázható |
| Nincs | Igen | Nem állítható be | Felszámítható | Számlázás egy tényleges Időhöz: Nem érhető el </br>Számlázás típusa egy tényleges kiadáshoz: Számlázható |
| Nincs | Igen | Nem állítható be | Nem számlázható | Számlázás egy tényleges Időhöz: Nem érhető el </br>Számlázás típusa egy tényleges kiadáshoz: Nem számlázható |
| Igen | Nincs | Felszámítható | Nem állítható be | Számlázás egy tényleges Időhöz: Számlázható </br>Számlázás típusa egy tényleges kiadáshoz: Nem érhető el |
| Igen | Nincs | Nem számlázható | Nem állítható be | Számlázás egy tényleges Időhöz: Nem számlázható </br> Számlázás típusa egy tényleges kiadáshoz: Nem érhető el |
