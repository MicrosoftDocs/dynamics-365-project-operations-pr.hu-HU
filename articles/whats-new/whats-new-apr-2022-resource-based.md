---
title: Újdonságok 2022. áprilisban – Project Operations erőforrásalapú vagy nem készletalapú forgatókönyvekhez
description: Ez a cikk a Microsoft Dynamics 365 Project Operations 2022. áprilisi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást az erőforrás-/nem készletalapú forgatókönyvekhez.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ea1c96d64309990962f431b1c72ae47bf445bfa
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912381"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok 2022. áprilisban – Project Operations erőforrásalapú vagy nem készletalapú forgatókönyvekhez

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a cikk a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Project Operations egy Dataverse környezeti verzióban 4.41.0.45
- Projektmenedzsment és könyvelés Dynamics 365 Finance környezetben 10.0.26-os verzió

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

A beszerzési kategóriák projektbeszerzési rendelésekben és függőben lévő szállítói számlákban használhatók. További tájékoztatás: [Beszerzési kategóriák használata projektvásárlási rendelésekkel és függőben lévő szállítói számlákkal](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Az alábbi táblázat a Project Operations 2022. márciusi kiadásában módosított vagy hozzáadott kettős írású térképeket mutatja be.

| Entitásleképezés | Frissített verzió | Hozzászólások |
| -------------- | ------------------- | ------------|
| Project Operations integrációs projekt szállítói számla export entitás msdyn\_ projectvendorinvoicelines | 1.0.0.4 | Ez a térkép támogatja a beszerzési kategóriák használatát a beszerzési rendelésekkel és a függőben lévő szállítói számlákkal. |

Mindig futtassa a térkép legújabb verzióját a környezetében, és engedélyezze az összes kapcsolódó táblaleképezést a Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése közben. Előfordulhat, hogy egyes funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy beépített táblázattérképet, alkalmazza újra a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha a térkép indításakor problémába ütközik, kövesse a Kettős írás hibaelhárítási útmutató Hiányzó táblaoszlopok probléma a térképeken [című szakaszának utasításait](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| ------------ | ---------------- | -------------- |
| Idő és költség | 2573900 | A **Modern jóváhagyás** funkciót alapértelmezés szerint engedélyezni kell. |
| Számlázás és árképzés | 2603313 | Kijavítottunk egy ismétlődő rekordhibát, amely megakadályozta a termékkel rendelkező árajánlat- és szerződéssorok hozzáadását. |
| Üzembe helyezés és konfigurálás | 2611368 | Az ügyfeleknek képesnek kell lenniük arra, hogy akár öt egyéni entitást is hozzáadjanak a megoldáshoz a modern alkalmazástervező használatával. |
| Idő és költség | 2628285 | Kijavítottunk egy hibát, amely befolyásolta a megfelelő erőforrás-kategória beállítását az időbevitel importálása során. |
|   Lehetőségkezelés| 2628815 | Frissítse az idézőjelsor részletes leírásának karakterkorlátját úgy, hogy az megfeleljen a tevékenység tárgyának karakterkorlátjának, hogy az importálás sikeres legyen azokban a feladatokban, ahol a tárgy 100 karakternél hosszabb. |
| Idő és költség| 2629547 | A **projektjóváhagyások Beküldési szempontja** mezőnek arra a felhasználóra kell mutatnia, aki beadta a rekordot. |
| Idő és költség| 2629865 | A **Kategória** másolása mező a tevékenységekről a projektek másolásakor. |
| Idő és költség| 2636463 | Kijavítottuk a jóváhagyások szűrőit a modern jóváhagyási űrlapokon. |
| Projekttervezés és nyomon követés | 2648300 | Kijavítottunk egy hibát, amely megakadályozta a projekt tulajdonosának módosítását. |
| Számlázás és árképzés | 2563000 | Nem szabad megengedni a nem számlázott értékesítés naplósorait, ha a pénznem eltér a szerződés pénznemétől. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmenedzsment és számvitel Dynamics 365 Finance

A frissítésben található hibajavításokkal kapcsolatos információkért jelentkezzen be a Lifecycle Services (LCS) szolgáltatásba Microsoft Dynamics, és tekintse meg a [tudásbáziscikket](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
