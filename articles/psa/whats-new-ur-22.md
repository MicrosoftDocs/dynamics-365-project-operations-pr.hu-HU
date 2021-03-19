---
title: Újdonságok vagy változások a Project Service Automation 22-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 22-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 389897c2604974a0bf7f221758dd03e1748ffeb5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280581"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation 22-es frissítési kiadás, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 22-es frissítési kiadásában. A verzió build száma V 3.10.33.48, és általánosan elérhető lesz önálló frissítésként 2020 júniusában.

## <a name="update-release-22"></a>22-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások



**Idő és költség**

A következő problémák kerültek kijavításra:

- Az **Időbejegyzések** az importálás után nem lesznek automatikusan hozzáadva időbejegyzések ütemezéséhez.
- Az **Időbeviteli** rács dátumválasztója nem ismeri fel a felhasználó területi beállításait.

**Erőforráskezelés**

A következő problémák kerültek kijavításra:

- Manuális módban az **Erőforrás-hozzárendelési** körvonalak módosításait a rendszer nem ismeri fel az **Erőforráskövetelmények** létrehozásakor.
- Az **Erőforrás-kérelmek** nem támogatják az egyéni kérelemállapokat.

**Projektmenedzsment**

A következő problémák kerültek kijavításra:

- Dupla kattintással az EstimateGridControl nem megfelelően elemzi a holland formátumú számokat.
- A hozzárendelt órák nem frissülnek megfelelően, ha a hozzárendelések a Microsoft Project Desktop kliensbővítmény használatával módosulnak.
- A Projektek nyomon követése és a Becslések rácsa helytelen értékesítési pénznemkódot jelenít meg, ha a szerződés pénzneme eltér az ügyfél pénznemtől és a szervezet úgy lett konfigurálva hogy pénznem jele helyett pénznemkódokat jelenítsen meg.
- A csoporttagok befejezési dátuma egy napot hozzáad, ha a munkaórák ütemezése napi 24 órában történik.
- A Projekt ütemezésekor a tevékenységhez tartozó Tranzakciós kategória hozzáadása nem indítja el az automatikus mentést.
- A következő hibaüzenet jelenik meg, amikor egy csapattagot vesz fel a Projekt sablonba: „Az erőforrás-követelmények nem társíthatók projektsablonokkal”. 
- A menüszalag szabályának „msdyn.Approval.CanApproveOrReject” parancsfájlja időtúllépési hibát jelenít meg.

**Sales**

A következő problémák kerültek kijavításra:

- Az érvényesítési hibaüzenet nem jelenik meg, ha egy Önköltségi árlista van kiválasztva az „Új ajánlati projektárlista” űrlapon/entitáson.
- Ha az ajánlathoz tartozó üzleti folyamat az utolsó fázisban van, akkor a megnyertként lezárt ajánlat nem navigálja a felhasználót a létrehozott szerződésre.
- A **Ki nem számlázott értékesítések** sztornírozása az eredeti költséghez kapcsolódik az időbejegyzés visszahívásakor.
- A **Jóváhagyás** gomb kiválasztását követően a számla állapota nem módosul **Megerősített** értékre hacsak a számlát nem frissítik.


[!INCLUDE[footer-include](../includes/footer-banner.md)]