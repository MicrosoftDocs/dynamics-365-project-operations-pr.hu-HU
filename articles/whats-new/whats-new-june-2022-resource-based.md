---
title: Újdonságok 2022. júniusában – Project Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez
description: Ez a cikk a Microsoft Dynamics 365 Project Operations 2022. júniusi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást erőforrás-/nem készletalapú forgatókönyvekhez.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031334"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok 2022. júniusában – Project Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a cikk a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Project Operations egy Dataverse 4.43.0.77-es vagy 4.43.0.119-es verziójú környezeti környezetben
- Projektmenedzsment és könyvelés Dynamics 365 Finance környezetben 10.0.27-es verzió

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Az alábbi táblázat a Project Operations 2022. júniusi kiadásában módosított vagy hozzáadott kettős írású térképeket mutatja be.

| Entitásleképezés | Frissített verzió | Hozzászólások |
| --- | --- | --- |
| Project Operations integrációs projekt szállítói számlát exportáló entitása (msdyn_projectvendorinvoices) | 1.0.0.1 | Elavult az örökölt mező, és leképezte a szállítói számla állapotának nyomon követésére szolgáló új mezőre. |

Mindig futtassa a térkép legújabb verzióját a környezetében, és engedélyezze az összes kapcsolódó táblaleképezést a Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése közben. Előfordulhat, hogy egyes funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy beépített táblázattérképet, alkalmazza újra a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha a térkép indításakor problémába ütközik, kövesse a Kettős írás hibaelhárítási útmutató Hiányzó táblaoszlopok probléma a térképeken [című szakaszának utasításait](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Alvállalkozói | 2708885. | Kijavítottuk a hibaüzenetet, amely akkor jelenik meg, amikor egy felhasználó lefoglalható erőforrás-foglalási fejlécrekordot hozott létre, amelyben nincs kitöltve foglalható erőforrás. |
| Projekttervezés és nyomon követés | 2629441. | Kijavítottuk a munkafolyamatot kiváltó logikát, hogy megakadályozza a végtelen hurkot a projekttevékenységek frissítésekor. |
| Idő és költség | 2641209. | A hozzárendelésekből/foglalásokból származó időbeviteli importálásoknak meg kell őrizniük a foglalható erőforrás-referenciát. |
| Projekttervezés és nyomon követés | 2651148. | A projektdokumentum fejlécét meg kell őrizni.|
| Projekttervezés és nyomon követés | 2653145. | Hozzáadott ellenőrzések annak biztosítására, hogy ne lehessen olyan projektrekordot létrehozni, amelynek nevében nem érvényes karakterek szerepelnek. |
| Idő és költség | 2654710. | Kijavítottuk a szűrést a **Jóváhagyások** lapon. |
| Számlázás és árképzés | 2667805. | Hozzáadott ellenőrzések, amelyek segítenek megakadályozni a számlázott értékesítési tényleges adatok létrehozását, ha a számlázatlan értékesítési tényleges adatok nem léteznek. |
| Számlázás és árképzés | 2668378. | Hozzáadott ellenőrzések, amelyek segítenek megakadályozni az egyéni árképzési dimenziók hozzáadását, kivéve, ha a rendszer kitölti a logikai nevet és a mező nevét. |
| Alvállalkozói | 2677485. | Frissítettük a szállítói számlasorok kettős írású leképezésének célverzióját. |
| Idő és költség | 2700428. | Továbbfejlesztettük a jóváhagyási logikát, hogy a projekt más jóváhagyási készletei akkor is feldolgozhatók legyenek, ha az egyik jóváhagyási készlet elakadt a rendszerfeladatokban. |

### <a name="project-management-and-accounting-in-finance"></a>Projektmenedzsment és számvitel a pénzügyekben

A frissítésben található hibajavításokkal kapcsolatos információkért jelentkezzen be a Lifecycle Services (LCS) szolgáltatásba Microsoft Dynamics, és tekintse meg a [tudásbáziscikket](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
