---
title: Újdonságok - 2022. augusztus - Project Operations erőforrás/nem készletalapú forgatókönyvekhez
description: Ez a cikk a Project Operations 2022. augusztusi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást a Microsoft Dynamics 365 Project Operations erőforrás/nem készletalapú forgatókönyvek esetében.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403859"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok - 2022. augusztus - Project Operations erőforrás/nem készletalapú forgatókönyvekhez

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a cikk a következő Microsoft Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations 4.45.0.53 verziójú Dataverse-környezetben
- Projektmenedzsment és könyvelés a Dynamics 365 Finance 10.0.28-as verziójú környezetekben

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Ebben a kiadásban nincsenek frissítések a Project Operations kettős írású leképezéseihez. A Project Operations kettős írású leképezései aktuális listájának és verzióinak felsorolását lásd: [Project Operations kettős írás leképezési verziói](../environment/resource-dual-write-maps.md).

A Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése során mindig futtassa a környezetben a leképezés legújabb verzióját, és engedélyezze az összes kapcsolódó táblaleképezést. Előfordulhat, hogy bizonyos funkciók és képességek nem működnek megfelelően, ha a leképezés legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy gyári táblaleképezést, újra kell alkalmaznia a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha problémát tapasztal a leképezés elindításával kapcsolatban, kövesse a [Kettős írás hibaelhárítási útmutató térkép szakaszának Hiányzó táblaoszlopok című](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) részében található utasításokat.

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
|   Lehetőségkezelés | 2762089. | Hibakezelés a szerződés elvesztettként való lezárásakor, ha az automatikus mentés le van tiltva a szervezetben.|
|Projekttervezés és nyomon követés | 2767841. | Telemetriafrissítések a Projekt entitás Létrehozás és Frissítés forgatókönyveihez.|
|Számlázás és árképzés | 2771072. | Null referencia kivételkezelés árajánlat megnyerése esetén.|
|Számlázás és árképzés | 2844181. |Hiba a korrelációs azonosító lekérésében és a számlalétrehozás blokkolásában.|
|Számlázás és árképzés | 2852836. | A CE-ben létrehozott és vállalati költséghez hiányoznak vállalatközi tényadatok.|


### <a name="project-management-and-accounting-in-finance"></a>Projektmenedzsment és könyvelés a Finance-ban

Ha további tájékoztatást szeretne kapni a frissítésben található hibajavításokról, lépjen be a Microsoft Dynamics Lifecycle Services (LCS) szolgáltatásokba, és tekintse meg a [Tudásbázis cikket](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
