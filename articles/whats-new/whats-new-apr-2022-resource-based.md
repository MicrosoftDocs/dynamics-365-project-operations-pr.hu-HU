---
title: Újdonságok 2022. áprilisban – Project Operations erőforrásalapú vagy nem készletalapú forgatókönyvekhez
description: Ez a témakör a Microsoft Dynamics 365 Project Operations 2022. áprilisi kiadásában erőforrás-/nem raktározott forgatókönyvekhez elérhető minőségi frissítésekről nyújt tájékoztatást.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc713e7a0dd6993e38ce3e3b2ba19f796a6f4773
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613327"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok 2022. áprilisban – Project Operations erőforrásalapú vagy nem készletalapú forgatókönyvekhez

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a témakör a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Projektműveletek környezeti Dataverse verzióban 4.41.0.45
- Projektmenedzsment és -számvitel Dynamics 365 Finance környezetben 10.0.26-os verzióban

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

A beszerzési kategóriák projekt beszerzési rendelésekben és függőben lévő szállítói számlákban használhatók. További információt a Beszerzési kategóriák használata projekt beszerzési rendelésekkel és függőben lévő szállítói számlákkal című témakörben [talál](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Az alábbi táblázat a Project Operations 2022. márciusi kiadásában módosított vagy hozzáadott kettős írási térképeket mutatja be.

| Entitásleképezés | Frissített verzió | Hozzászólások |
| -------------- | ------------------- | ------------|
| Projektműveletek integráció projekt szállítói számlasor exportálási entitás msdyn\_ projectvendorinvoicelines | 1.0.0.4 | Ez a térkép támogatja a beszerzési kategóriák használatát beszerzési rendelésekkel és függőben lévő szállítói számlákkal. |

Mindig futtassa a térkép legújabb verzióját a környezetében, és engedélyezze az összes kapcsolódó táblaleképezést a Project Operations Dataverse megoldás és a Pénzügy megoldás verziójának frissítésekor. Előfordulhat, hogy egyes funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy beépített táblázattérképet, alkalmazza újra a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha a térkép indításakor problémát tapasztal, kövesse a Kettős írás hibaelhárítási útmutató Hiányzó táblázatoszlopok probléma a térképeken [című részében található utasításokat](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| ------------ | ---------------- | -------------- |
| Idő és költség | 2573900 | A **Modern jóváhagyás** funkciót alapértelmezés szerint engedélyezni kell. |
| Számlázás és árképzés | 2603313 | Kijavítottunk egy ismétlődő rekordhibát, amely megakadályozta a terméket tartalmazó ajánlat- és szerződéssorok hozzáadását. |
| Telepítés és konfigurálás | 2611368 | Az ügyfeleknek legfeljebb öt egyéni entitást kell hozzáadniuk a megoldáshoz a modern alkalmazástervező használatával. |
| Idő és költség | 2628285 | Kijavítottunk egy hibát, amely hatással volt a megfelelő erőforráskategória beállításának képességére az időbevitel importálása során. |
|   Lehetőségkezelés| 2628815 | Frissítse az ajánlatsor részletleírásának karakterkorlátját, hogy az megfeleljen a tevékenység tárgy karakterkorlátjának, hogy az importálás sikeres legyen azoknál a tevékenységeknél, amelyek tárgya 100 karakternél hosszabb. |
| Idő és költség| 2629547 | A **projektjóváhagyások Elküldött rész mezőjének** a rekordot beküldő felhasználóra kell mutatnia. |
| Idő és költség| 2629865 | A **tevékenységek Másolás kategória** mezője a projektek másolásakor. |
| Idő és költség| 2636463 | Rögzítettük a szűrőket a jóváhagyásokra a modern jóváhagyási űrlapokon. |
| Projekttervezés és nyomon követés | 2648300 | Kijavítottunk egy hibát, amely megakadályozza a projekt tulajdonosának módosítását. |
| Számlázás és árképzés | 2563000 | Nem engedélyezhetők naplósorok olyan nem számlázott eladáshoz, amelyben a pénznem eltér a szerződés pénznemétől. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmenedzsment és számvitel Dynamics 365 Finance

A frissítésben található hibajavításokkal kapcsolatos információkért jelentkezzen be az életciklus-szolgáltatásokba Microsoft Dynamics (LCS), és tekintse meg a [Tudásbázis-cikket](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
