---
title: Újdonságok vagy változások a Project Service Automation 24-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 24-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3a37e71be2cce259d8aed0621d13393b6bbe4199
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126576"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation 24-es frissítési kiadás, V3

Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 24-es frissítési kiadásában. Ennek a verziónak a buildszáma V3.10.42.43, és általánosan elérhető egy önálló frissítésben 2020 októberében.

## <a name="update-release-24"></a>24-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

**Sales**

A következő problémák kerültek kijavításra:

- Probléma a termékek alapértelmezett árlistájának beállításakor.
- Az árajánlat elnyerésének teljesítménye lassú a beágyazott árlista és a szerepkörár bejegyzések másolása miatt.
- A **Projektszerződés/Értékesítési központ** > **Terméksorelem/Rendelési sor mennyisége** automatikusan a legközelebbi egész számra kerekítődik.
- A rendszerjogosultság bővítése az árlisták olvasásakor.
- A(z) **address1_freighttermscode** és a(z) **address1_shippingmethodcode** ügyfélcím mezőinek másolása az Árajánlat/Megrendelés mezőkbe. 


**Idő és költség**

A következő problémák kerültek kijavításra:

- Az **Időbeviteli rács** nem támogatja a **Csak dátum** időműködést.
- Az **Időbejegyzés** nem frissül automatikusan. Manuális frissítés szükséges.
- Nem lehet importálni az időpontokat egy hozzárendelésből, ha az erőforrás hozzárendeléseiben szünet (0 óra) van.
- Az időbejegyzés létrehozásakor állítsa a kezdést ugyanarra, mint a következő: **msdyn_date**.
- Ismételten engedélyezheti az időbejegyzés csoportos szerkesztését.

**Erőforráskezelés**

A következő problémák kerültek kijavításra:

- A napközbeni foglalás állapotának frissítése követelmény nélkül egy null értékű referenciakivételt hoz létre.
- Hiba történt az **Egyeztetés nézet** betöltésekor.


**Projektmenedzsment**

A következő problémák kerültek kijavításra:

- A **Projekt ütemezése** menüben **Manuális** értékről **Automatikus** értékre történő váltáskor az automatikus mentés nem fejeződik be.
- A költségeket nem szabad beleszámolni a **Projekt nyomonkövetési rács** pontban szereplő szórásokba.
- Következetlen viselkedés a **Becslések címke** oszlopok betöltésekor, szemben az **Időfázis** típusának módosításával.
- Előfordulhat, hogy a projekt tényleges költsége nem tükrözi **Tényadatok** pontban szereplő összegeket.
- Az **Összegzés** lapon szereplő **Becsült befejezési dátum** nem egyezik meg a **WBS-ütemezéssel**.
- A **Tényleges órák frissítése** a kihúzáson nem működik megfelelően.
- A gyökér **üzleti egységen** kívüli projektmenedzserek nem tudnak projekteket létrehozni.
- A feladat vagy a kategória változtatásai nem maradnak meg a **Költségbecslések** pontban.
- A **Szerződés másolata** átmásolja a számlák ütemezéseit, valamint a futtatási állapotot.
- A **Tényadatok frissítése** gomb hibásan számítja ki az összefoglaló feladatokat.
- Microsoft Project-bővítmény: javítja a null referenciahibát, ha bármelyik csapattaghoz egy üres erőforrásbiztosító egység tartozik.

