---
title: Újdonságok vagy változások a Project Service Automation 18-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 18-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3a6d3ee21ecf742b2253132f3d3cc1cb2b57af75
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119871"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation 18-as frissítési kiadás, V3

Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 18-es frissítési kiadásában. A verzió build száma V 3.10.8.12, és általánosan elérhető lesz önálló frissítésként 2020 áprilisában.

## <a name="update-release-18"></a>18-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

**Idő és költség**

- Javítva: A **Visszavonás**, **Kérelem** és **Jóváhagyás visszavonása** folyamatai kivételeket küldenek nem egyértelmű hibaüzenetekkel.
- Javítva: Amikor a **Jóváhagyás visszavonása** sikertelen egy költség esetében, a rendszer nem jeleníti meg a megfelelő kivétellel kapcsolatos hibát.
- Javítva: Az Időbejegyzés rács hibásan kezeli a munkaszüneti napokat Ausztráliában a nyári időszámítás (DST) októberi váltása után.
- Javítva: a helytelen alapértelmezési logika megakadályozza a kiadások beküldését.
- Javítva: Az időbejegyzés jóváhagyásának sikertelensége esetén a jóváhagyás **Függőben** állapotban marad.
- Javítva: SQL-hibák tömeges jóváhagyáskor (kettős zárolás / időtúllépés).
- Javítva: Az időbejegyzések jóváhagyása során a csoporttagok frissítése jelentős teljesítményproblémákat okoz a felhasználói élményben.

**Projektmenedzsment**

- Javítva: Az időzóna-értesítés áthelyezve az **Egyeztetés** nézetből a **Projekt** fő űrlapjára.
- Javítva: A naptár sablonjának alapértelmezése nem megfelelő egy új projektűrlap megnyitásakor.
- Javítva: A chromium alapú böngészőknél, a felhasználók nem tudják egyszerűen kiválaszthatja a megelőző tevékenységeket törlésre.
- Javítva: A **Projekt üres sablonból** létrehozása vagy másolása nem kapcsolódó feladatokat olvas be.
- Rögzített: Bizonyos szélsőséges esetekben új megbízás létrehozása a feladatrácsból duplikált bejegyzéseket eredményez.
- Javítva: Manuális módban a felhasználók nem tudják frissíteni a feladat kezdési dátumát az aktuálisan mentett dátumnál későbbire.

**Erőforráskezelés**

- Javítva: Az **Egyeztetés** nézet részösszeg sora helytelenül számítja ki a foglalások eltérését a foglalások meghosszabbítását követően.
- Javítva: Az **Egyeztetés** nézet helytelenül jeleníti meg az erőforrás-hozzárendeléseket, ha a foglalt erőforráshoz olyan naptár tartozik, amely egyezik meg a projektnaptárral.

**Sales**

- Rögzített: Az időbejegyzések újbóli jóváhagyása esetén (**Jóváhagyás > Visszavonás** ismételt jóváhagyás) egy duplikált, nem számlázható tényadat is létrehozásra kerül.