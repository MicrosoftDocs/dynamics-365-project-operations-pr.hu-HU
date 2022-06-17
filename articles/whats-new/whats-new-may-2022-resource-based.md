---
title: Újdonságok 2022. májusában – Project Operations erőforrásalapú vagy nem készletalapú forgatókönyvekhez
description: Ez a cikk a Microsoft Dynamics 365 Project Operations 2022. májusi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást erőforrás-/nem készletalapú forgatókönyvekhez.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921397"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok 2022. májusában – Project Operations erőforrásalapú vagy nem készletalapú forgatókönyvekhez

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a cikk a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Project Operations egy Dataverse környezeti verzióban 4.42.0.70
- Projektmenedzsment és könyvelés Dynamics 365 Finance környezetben 10.0.26-os verzió

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Ebben a kiadásban nincsenek frissítések a Project Operations kettős írású leképezéseihez. A Project Operations kettős írású leképezései aktuális listájának és verzióinak felsorolását lásd: [Project Operations kettős írás leképezési verziói](../environment/resource-dual-write-maps.md).

Mindig futtassa a térkép legújabb verzióját a környezetében, és engedélyezze az összes kapcsolódó táblaleképezést a Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése közben. Előfordulhat, hogy egyes funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy beépített táblázattérképet, alkalmazza újra a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha a térkép indításakor problémába ütközik, kövesse a Kettős írás hibaelhárítási útmutató Hiányzó táblaoszlopok probléma a térképeken [című szakaszának utasításait](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Minőségi frissítések
### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Erőforrás-kezelés | 2634019 | Továbbfejlesztett hibaüzenetek az üzleti ellenőrzésekhez, amikor általános csapattagokat ad hozzá erőforrásként. |
| Projekttervezés és nyomon követés | 2648515 | A tulajdonosazonosító **,** az állapot **és** az **állapot** korlátozott frissítései az entitások ütemezésében. |
| Számlázás és árképzés | 2653167 | A **Becslések** rács decimális elválasztójának követnie kell a **Személyes beállítások formátumbeállításait**. |
| Számlázás és árképzés| 2662251 | A Javított egység **és** az **Egységcsoport** mezők értékei alapértelmezés szerint az anyagbecslésekben lévő rekordok létrehozásakor alapértelmezettek. |
| Számlázás és árképzés| 2571408 | A számlázatlan értékesítési tényleges adatokat a rendszer a számlavázlat létrehozásakor proforma számlaazonosítóval bélyegzi meg. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmenedzsment és számvitel Dynamics 365 Finance

A frissítésben található hibajavításokkal kapcsolatos információkért jelentkezzen be a Lifecycle Services (LCS) szolgáltatásba Microsoft Dynamics, és tekintse meg a [tudásbáziscikket](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
