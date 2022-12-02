---
title: Újdonságok 2022. júniusában – Project Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez
description: Ez a cikk a Project Operations 2022. júniusi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást a Microsoft Dynamics 365 Project Operations erőforrás/nem készletalapú forgatókönyvek esetében.
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

Ez a cikk a következő Microsoft Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations egy 4.43.0.77 vagy 4.43.0.119 verziójú Dataverse-környezetben
- Projektmenedzsment és könyvelés a Dynamics 365 Finance 10.0.27-es verziójú környezetekben

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Az alábbi táblázat a Project Operations 2022. júniusi kiadásában módosított vagy hozzáadott kettős írású térképeket tartalmazza.

| Entitásleképezés | Frissített verzió | Hozzászólások |
| --- | --- | --- |
| Project Operations integrációs projekt szállítói számlát exportáló entitása (msdyn_projectvendorinvoices) | 1.0.0.1 | Elavult a örökölt mező, és leképezve az új mezőre a szállítói számlák állapotkövetése számára. |

A Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése során mindig futtassa a környezetben a leképezés legújabb verzióját, és engedélyezze az összes kapcsolódó táblaleképezést. Előfordulhat, hogy bizonyos funkciók és képességek nem működnek megfelelően, ha a leképezés legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy gyári táblaleképezést, újra kell alkalmaznia a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha problémát tapasztal a leképezés elindításával kapcsolatban, kövesse a [Kettős írás hibaelhárítási útmutató térkép szakaszának Hiányzó táblaoszlopok című](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) részében található utasításokat.

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Alvállalkozásba adás | 2708885. | Javítottuk a hibaüzenetet, amely akkor jelenik meg, amikor a felhasználó létrehoz egy foglalható erőforrás fejlécrekordot, ahol egyetlen foglalható erőforrás sincs kitöltve. |
| Projekttervezés és nyomon követés | 2629441. | Kijavítottuk a munkafolyamat triggerlogikáját, hogy megakadályozza a végtelen ciklust a projektfeladatok frissítésekor. |
| Idő és költség | 2641209. | A hozzárendelések/foglalások időbejegyzéseinek importja esetén meg kell tartani a foglalható erőforrás-hivatkozást. |
| Projekttervezés és nyomon követés | 2651148. | A projektdokumentum fejlécét védeni kell.|
| Projekttervezés és nyomon követés | 2653145. | További ellenőrzések garantálják, hogy ne lehessen olyan projektrekordot létrehozni, amelynek a neve érvénytelen karaktereket tartalmaz. |
| Idő és költség | 2654710. | Javította a szűrést a **Jóváhagyások** oldalon. |
| Számlázás és árképzés | 2667805. | A hozzáadott ellenőrzésekkel megakadályozható, hogy a számlázott tényleges értékesítések akkor is létrejönnek, ha nem léteznek a mögöttes nem számlázott tényleges értékesítések. |
| Számlázás és árképzés | 2668378. | A hozzáadott érvényesítések segítségével megakadályozható, hogy egyéni árképzési dimenziót ne lehessen hozzáadni logikai név és mezőnév nincs megadva. |
| Alvállalkozásba adás | 2677485. | Frissítve lett a szállítói számlasorok kettős írási leképezésének célverzióját. |
| Idő és költség | 2700428. | Javítva lett a jóváhagyási logika, hogy a projekt más jóváhagyási készletei akkor is feldolgozhatók legyenek, ha a az egyik jóváhagyás készlet a rendszerfeladatokban elakadt. |

### <a name="project-management-and-accounting-in-finance"></a>Projektmenedzsment és könyvelés a Finance-ban

Ha további tájékoztatást szeretne kapni a frissítésben található hibajavításokról, lépjen be a Microsoft Dynamics Lifecycle Services (LCS) szolgáltatásokba, és tekintse meg a [Tudásbázis cikket](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
