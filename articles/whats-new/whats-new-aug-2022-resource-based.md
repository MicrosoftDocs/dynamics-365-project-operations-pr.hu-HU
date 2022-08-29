---
title: Újdonságok - 2022. augusztus - Project Operations erőforrás/nem készletalapú forgatókönyvekhez
description: Ez a cikk a Microsoft Dynamics 365 Project Operations 2022. augusztusi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást erőforrás-/nem készletalapú forgatókönyvekhez.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 112dbb98de09ef342c03d122a29cb8025058e47f
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348102"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok - 2022. augusztus - Project Operations erőforrás/nem készletalapú forgatókönyvekhez

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a cikk a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Project Operations egy Dataverse környezeti verzióban 4.45.0.53
- Projektmenedzsment és könyvelés Dynamics 365 Finance környezetben 10.0.28-as verzió

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Ebben a kiadásban nincsenek frissítések a Project Operations kettős írású leképezéseihez. A Project Operations kettős írású leképezései aktuális listájának és verzióinak felsorolását lásd: [Project Operations kettős írás leképezési verziói](../environment/resource-dual-write-maps.md).

Mindig futtassa a térkép legújabb verzióját a környezetében, és engedélyezze az összes kapcsolódó táblaleképezést a Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése közben. Előfordulhat, hogy egyes funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy beépített táblázattérképet, alkalmazza újra a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha a térkép indításakor problémába ütközik, kövesse a Kettős írás hibaelhárítási útmutató Hiányzó táblaoszlopok probléma a térképeken [című szakaszának utasításait](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
|   Lehetőségkezelés | 2762089. | Hibakezelés a szerződés lezárásakor elveszettként, ha az automatikus mentés le van tiltva a szervezetben.|

### <a name="project-management-and-accounting-in-finance"></a>Projektmenedzsment és számvitel a pénzügyekben

A frissítésben található hibajavításokkal kapcsolatos információkért jelentkezzen be a Lifecycle Services (LCS) szolgáltatásba Microsoft Dynamics, és tekintse meg a [tudásbáziscikket](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
