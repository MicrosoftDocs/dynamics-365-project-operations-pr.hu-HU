---
title: Újdonságok 2022. májusában – Project Operations erőforrásalapú vagy nem készletalapú forgatókönyvekhez
description: Ez a cikk a Project Operations 2022. májusi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást a Microsoft Dynamics 365 Project Operations erőforrás/nem készletalapú forgatókönyvek esetében.
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

Ez a cikk a következő Microsoft Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations 4.42.0.70 verziójú Dataverse-környezetben
- Projektmenedzsment és könyvelés a Dynamics 365 Finance 10.0.26-os verziójú környezetekben

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Ebben a kiadásban nincsenek frissítések a Project Operations kettős írású leképezéseihez. A Project Operations kettős írású leképezései aktuális listájának és verzióinak felsorolását lásd: [Project Operations kettős írás leképezési verziói](../environment/resource-dual-write-maps.md).

A Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése során mindig futtassa a környezetben a leképezés legújabb verzióját, és engedélyezze az összes kapcsolódó táblaleképezést. Előfordulhat, hogy bizonyos funkciók és képességek nem működnek megfelelően, ha a leképezés legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy gyári táblaleképezést, újra kell alkalmaznia a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha problémát tapasztal a leképezés elindításával kapcsolatban, kövesse a [Kettős írás hibaelhárítási útmutató térkép szakaszának Hiányzó táblaoszlopok című](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) részében található utasításokat.

## <a name="quality-updates"></a>Minőségi frissítések
### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Erőforrás-kezelés | 2634019. | Javított hibaüzenetek az üzleti ellenőrzéshez, ha általános csoporttagokat adnak hozzá erőforrásként. |
| Projekttervezés és nyomon követés | 2648515. | Az **ownerid**, a **state** és a **status** korlátozott frissítései az ütemezési entitások esetében. |
| Számlázás és árképzés | 2653167. | A **Becslések** rács decimális elválasztójának követnie kell a **Személyes beállítások** formátumbeállításait. |
| Számlázás és árképzés| 2662251. | A **Javított egység** és **Egységcsoport** mezők értékei alaphelyzetbe állnak rekordok létrehozásakor az anyagbecslésekben. |
| Számlázás és árképzés| 2571408. | A számlázatlan tényleges értékesítések tényszámai egy proforma számlaazonosítóval vannak ellátva a vázlat számla létrehozásakor. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmenedzsment és könyvelés a Dynamics 365 Finance alkalmazásban

Ha további tájékoztatást szeretne kapni a frissítésben található hibajavításokról, lépjen be a Microsoft Dynamics Lifecycle Services (LCS) szolgáltatásokba, és tekintse meg a [Tudásbázis cikket](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
