---
title: Újdonságok vagy változások a Project Service Automation 19-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 19-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: b9baeca9e79e233c25a6310e426d755b9162bbad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280716"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation 19-es frissítési kiadás, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a PSA V3. 19-ös frissítési kiadásában. A verzió build száma V3.10.30.41, és általánosan elérhető lesz önálló frissítésként 2020 májusában.

## <a name="update-release-19"></a>19-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

**Idő és költség**

A következő problémák kerültek kijavításra: 

- Az időbejegyzés-importálásokból származtatott hibák nem megfelelően jelennek meg.
- Az időbeviteli rács nem támogatja a **csak dátum** típusú mezők működését.
- A Projekterőforrások nem tudnak költséget létrehozni egy projekttel.

**Projektmenedzsment**

A következő problémák kerültek kijavításra: 

-  Az unokafeladat a Befejezés (BefKB) kiszámítása során nem megfelelő erőfeszítés-becslést okoz.

**Sales**

A következő problémák kerültek kijavításra: 

- Az **Újraszámítás** művelet nem működik a költségszerződéssor részleteivel vagy az ajánlati sor részleteivel.
- Az **Árak frissítése** hiányzik a költségbecsléseknél.
-  Az ügyfelek nem tudják kiválasztani az egyéni szerződésállapot-okot a **Projektszerződés** oldalon.
- Az ügyfelek az árajánlatokból történő egyéni árlista létrehozásakor csökkentett teljesítményt tapasztalhatnak.
- Az ügyfelek inkonzisztenciát észlelhetnek a **kiszerelés** alapértelmezett értékeiben az **Árajánlatsor részletei** és **Szerződéssor részletei** oldalakon.
- Ha nem számlázható tranzakciókategóriájú cikkeket szeretne hozzáadni egy számlázható szerződéssorhoz, akkor a rendszer nem veszi figyelembe a tranzakciós kategória **Nem számlázható** számlázási típusát.
- Az ügyfelek nem használhatják az újonnan hozzáadott szerepköröket és kategóriát a korábban létrehozott szerződésekben.
- Az ügyfelek leromlott teljesítményt tapasztalhatnak a Szükségtelen beolvasásnál a PreValidateProjectTeamMemberUpdate.cs esetén
- A nem számlázhatóként beállított szerepköröket az **Erőforrás-kategóriák** listában a rendszernek hozzá kellene adnia a **Számlázható szerepkörök** laphoz **Nem számlázható** értékkel a projekt szerződéssorában.
- A projektek létrehozásakor az ügyfelek leromlott teljesítményt tapasztalhatnak, mivel a **GetBookableResourceIdFromUser** a foglalható erőforrások összes oszlopát beolvassa csak az elsődleges azonosító helyett.
- **TransactionType** entitásból hiányzik az ellenőrzés előtti frissítés beépülő modul, amellyel megakadályozható, hogy a felhasználók tranzakciótípusokhoz nem érvényes **Kiszerelések** és **UnitGroups** értékeket adjanak meg.
- Az **eltávolítás** lépés nem működik az időbejegyzés importálásához.


[!INCLUDE[footer-include](../includes/footer-banner.md)]