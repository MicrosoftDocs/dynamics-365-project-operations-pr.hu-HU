---
title: 2021. szeptemberi újdonságok – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a cikk a Project Operations 2021. szeptemberi kiadásában elérhető minőségi frissítésekről nyújt információt erőforrás-/nem készletalapú forgatókönyvekhez.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c7f764b3e8ee3775167ee57b4f034e383899aea3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923375"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021. szeptemberi újdonságok – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

*Érvényesség: Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén*

Ez a cikk a következő Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

   - Project Operations 4.14.0.99 verziójú Microsoft Dataverse-környezetben.
   - Projektmenedzsment és könyvelés Dynamics 365 Finance környezetben 10.0.20-as verzió.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Ebben a kiadásban nincsenek frissítések a Project Operations kettős írású leképezéseihez. A Project Operations kettős írású leképezései aktuális listájának és verzióinak felsorolását lásd: [Project Operations kettős írás leképezési verziói](../environment/resource-dual-write-maps.md).

A Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése során mindig futtassa a környezetben a leképezés legújabb verzióját, és engedélyezze az összes kapcsolódó táblaleképezést. Előfordulhat, hogy bizonyos funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verziója **Kettős írás** oldalon látható a **Verzió** oszlopban. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabta az egyedi táblatérképet, újra kell alkalmaznia a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha probléma merül fel a leképezés indítása során, kövesse a Kettős írás hibakeresési útmutató [Hiányzó táblaoszlop-probléma a leképezésekben](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) részében található útmutatásokat.

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| **Funkcióterület** | **Hivatkozási szám** | **Minőségi frissítés** |
| --- | --- | --- |
| Idő és költség | 1811407 | Módosította a Projektjóváhagyó biztonsági szerepkört költségbevitel jóváhagyásokhoz. |
| Idő és költség | 1811438 | Módosította a Projektjóváhagyó biztonsági szerepkört az időbevitel jóváhagyás visszavonásához. |
| Idő és költség | 2370126 | Frissítette a **Projektfeladat** és a **Szerepkör** ikonokat az **Időbejegyzés** entitásban. |
| Idő és költség | 2379879 | A Dynamics 365 for Phone használata esetén kijavította a **Hét másolása** funkciót az időbevitelnél. |
| Számlázás és árképzés | 2371906 | A proforma számla összmennyiségének nem szabad módosíthatónak lennie a Project Operations alkalmazásban az erőforrás-alapú telepítések esetén. |
| Számlázás és árképzés | 2385802 | Javítottuk a projektösszegek frissítésekkor a negatív tényleges óráknál jelentkező hibát. |
| Számlázás és árképzés | 2389675 | Továbbfejlesztett proforma számlamegerősítés viselkedés. A hosszú ideje futó feladatok entitásának figyelembe kell vennie a könyvelés számára a megerősítő eredmények írásához szükséges tevékenységet. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmenedzsment és számvitel Dynamics 365 Finance

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Utazás és költség | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Nem megfelelőek a hitelkártyás tranzakciókból létrehozott költségből közzétett szállítói és áfatranzakciók. |
| Utazás és költség | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Nem megfelelő fizetési sorok jönne létre a fizetési napló létrehozásakor. |
| Utazás és költség | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Nem megfelelőek a hitelkártyás tranzakciókból létrehozott költségből közzétett áfatranzakciók. |
| Utazás és költség | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Egy költségsor törlése hosszú időt vehet igénybe. |
| Projekt könyvelése | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | A KB 4619395 alkalmazása tán nem támogatott a számsorozat **Folyamatos** értékre módosítása, és a becslés feladását követően a következő hibaüzenet jelenik meg: "A rendszer nem támogatja a Proj_X számsorozat "folyamatos" beállítását." |
| Projekt könyvelése | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Előfordulhat, hogy a szállítói számla könyvelése sikertelen lesz a következő hibaüzenettel: "A tranzakciók nincsenek kiegyenlítve 5/17/2021 alapján. (számviteli pénznem: 0,00 - jelentési pénznem: 0,01).” |
