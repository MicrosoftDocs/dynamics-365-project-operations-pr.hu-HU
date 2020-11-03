---
title: Újdonságok vagy változások a Project Service Automation 21-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 21-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: e8a15d5f723da528640c62c1892bac0d801c2bee
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078043"
---
# <a name="project-service-automation-update-release-21-v3"></a>Project Service Automation 21-es frissítési kiadás, V3

Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 21-es frissítési kiadásában. A verzió build száma V 3.10.32.50, és általánosan elérhető lesz önálló frissítésként 2020 júniusában.

## <a name="update-release-21"></a>21-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

**Idő és költség**

A következő problémák kerültek kijavításra:

- Amikor az irányítópulton található az **Időbeviteli rács vezérlő** , a rács nem használja az irányítópult rácsához tartozó tároló teljes szélességét.
- Bizonyos időzónák esetén az **Időbejegyzés** rácsvezérlő nem jeleníti meg a bejegyzéseket.
- A 21:00 óra utáni időpontok nem megfelelő napon jelennek meg.
- A felhasználók nem küldhetnek be költséget, ha a **Költségnyugta szükséges** költségkategória nem tartalmaz értéket.

**Erőforráskezelés**

A következő problémák kerültek kijavításra:

- Az inaktív foglalások az **Egyeztetés** nézetben jelennek meg.
- Az általános erőforrás-teljesítés esetében hiányzik az ellenőrzés az érvényes foglalási állapot meglétének biztosításához.

**Projektmenedzsment**

A következő problémák kerültek kijavításra:

- A **Projekt** űrlap rácsai ( **Erőforrás-hozzárendelés** , **Feladat** , **Egyeztetés** nézet, **Kiadások becslése** ) akkor is szerkeszthető maradnak, ha a projekt nem aktív.
- A duplikált ügyfelek nem egyesíthetők a megerősített projekt-szerződésekhez kapcsolt ügyfelekkel.
- Ha érvényes naptárral nem rendelkező erőforrást ad hozzá, akkor a rendszer nem küld vissza felhasználóbarát hibaüzenetet.
- A **Feladat hozzáadása** gomb a feladatrácson engedélyezve van, amikor a projekt társítva a van a **Microsoft Project bővítményhez**.
- Az erőfeszítés nem kontrollálhatóan nő, ha egy adott kategóriához tartozó feladatot egy erőforráshoz rendelnek, amelyhez olyan szerepkör tartozik, amelyhez önköltségi ár van meghatározva.

**Sales**

A következőket fejlesztettük:

- A **Számlázás gyakorisága** és a **Számlázás kezdete** át lett helyezve a **Számla ütemezése** lapra.

A következő problémák kerültek kijavításra:

- A **Teljes eladási ár** nulla (0) a **Kategóriához** annak ellenére, hogy a **Szerepkörhöz** nem nulla teljes értékesítési ár tartozik.
- Az ügyfelek nem módosíthatják a **Számlaállapot** mező értékét, **Számlázásra kész** értékre, amikor egy másik testreszabott folyamat egy további mezőt frissít.
- A **Számlasorok frissítése** gomb több duplikált sort is létrehozhat, ha az ismételten ki van választva.
- Az **Árak frissítése** gomb nem működik a **Szerepkörárak** alrácson **Betekintő nézet** űrlapon.
- Az **Értékesítési árlisták feloldási** logikája nem megfelelően kezeli az időzónákat, így az árlisták helytelenül lesznek kiválasztva.
- A projekt **Összes tényleges költsége** egyetlen időbevitel jóváhagyása után tört összeggel is elvégezhető.
- Az **Árfeloldás** logikája nem biztosít felhasználóbarát hibaüzenetet, ha a **Beolvasott szerepkörár** nem rendelkezik az **„Elsődleges kiszerelés”** és az **„Ár az elsődleges kiszerelésben”** mezőkben értékkel.
