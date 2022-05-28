---
title: Újdonságok 2022. májusában – Project Operations erőforrásalapú vagy nem készletalapú forgatókönyvekhez
description: Ez a témakör a Microsoft Dynamics 365 Project Operations 2022. májusi kiadásában erőforrás-/nem raktározott forgatókönyvekhez elérhető minőségi frissítésekről nyújt tájékoztatást.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d3ac63f0d33d36cc5b6d4cea3ab8167e5974cfe6
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710140"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok 2022. májusában – Project Operations erőforrásalapú vagy nem készletalapú forgatókönyvekhez

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a témakör a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Projektműveletek környezeti Dataverse verzióban 4.42.0.70
- Projektmenedzsment és -számvitel Dynamics 365 Finance környezetben 10.0.26-os verzióban

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Ebben a kiadásban nincsenek frissítések a Project Operations kettős írású leképezéseihez. A Project Operations kettős írású leképezései aktuális listájának és verzióinak felsorolását lásd: [Project Operations kettős írás leképezési verziói](../environment/resource-dual-write-maps.md).

Mindig futtassa a térkép legújabb verzióját a környezetében, és engedélyezze az összes kapcsolódó táblaleképezést a Project Operations Dataverse megoldás és a Pénzügy megoldás verziójának frissítésekor. Előfordulhat, hogy egyes funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy beépített táblázattérképet, alkalmazza újra a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha a térkép indításakor problémát tapasztal, kövesse a Kettős írás hibaelhárítási útmutató Hiányzó táblázatoszlopok probléma a térképeken [című részében található utasításokat](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Minőségi frissítések
### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Erőforrás-kezelés | 2634019 | Továbbfejlesztett hibaüzenetek az üzleti ellenőrzéshez, amikor általános csapattagokat adnak hozzá erőforrásként. |
| Projekttervezés és nyomon követés | 2648515 | A tulajdonosi **azonosító,** az állapot **és** az **állapot** korlátozott frissítése az ütemezési entitásokban. |
| Számlázás és árképzés | 2653167 | A **Becslések** rács decimális elválasztójának követnie kell a **Személyes beállítások** formátumbeállításait. |
| Számlázás és árképzés| 2662251 | A Javított egység **és** az **Egység csoport** mezők értékei alapértelmezés szerint az anyagbecslésekben lévő rekordok létrehozásakor. |
| Számlázás és árképzés| 2571408 | A nem számlázott értékesítési tényleges értékeket proforma számlaazonosítóval bélyegzi le a program számlatervezet létrehozásakor. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmenedzsment és számvitel Dynamics 365 Finance

A frissítésben található hibajavításokkal kapcsolatos információkért jelentkezzen be az életciklus-szolgáltatásokba Microsoft Dynamics (LCS), és tekintse meg a [Tudásbázis-cikket](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
