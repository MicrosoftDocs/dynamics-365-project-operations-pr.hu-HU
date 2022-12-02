---
title: Újdonságok 2022. áprilisban – Project Operations erőforrásalapú vagy nem készletalapú forgatókönyvekhez
description: Ez a cikk a Project Operations 2022. áprilisi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást a Microsoft Dynamics 365 Project Operations erőforrás/nem készletalapú forgatókönyvek esetében.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110887"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok 2022. áprilisban – Project Operations erőforrásalapú vagy nem készletalapú forgatókönyvekhez

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a cikk a következő Microsoft Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations 4.41.0.45 verziójú Dataverse-környezetben
- Projektmenedzsment és könyvelés a Dynamics 365 Finance 10.0.26-os verziójú környezetekben

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

Beszerzési kategóriák használhatók a projekt beszerzési rendeléseihez és a függőben lévő szállítói számlákhoz. További információ: [Használjon beszerzési kategóriákat a projekt beszerzési rendeléseihez és a függőben lévő szállítói számlákhoz](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Az alábbi tábla a Project Operations 2022. márciusi kiadásában módosított vagy hozzáadott kettős írású térképeket tartalmazza.

| Entitásleképezés | Frissített verzió | Hozzászólások |
| -------------- | ------------------- | ------------|
| Project Operations integrációs projekt szállítói számlasort exportáló entitása (msdyn\_projectvendorinvoicelines) | 1.0.0.4 | Ez e leképezés beszerzési kategóriák használatát támogatja a projekt beszerzési rendeléseihez és a függőben lévő szállítói számlákhoz. |

A Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése során mindig futtassa a környezetben a leképezés legújabb verzióját, és engedélyezze az összes kapcsolódó táblaleképezést. Előfordulhat, hogy bizonyos funkciók és képességek nem működnek megfelelően, ha a leképezés legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy gyári táblaleképezést, újra kell alkalmaznia a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha problémát tapasztal a leképezés elindításával kapcsolatban, kövesse a [Kettős írás hibaelhárítási útmutató térkép szakaszának Hiányzó táblaoszlopok című](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) részében található utasításokat.

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| ------------ | ---------------- | -------------- |
| Idő és költség | 2573900. | A **Modern jóváhagyás** funkciót alapértelmezés szerint engedélyezni kell. |
| Számlázás és árképzés | 2603313. | Kijavított egy duplikált rekorddal kapcsolatos hibát amely megakadályozta a termékkel rendelkező árajánlat és szerződéssorok hozzáadását. |
| Központi telepítés és konfiguráció | 2611368. | Az ügyfelek a modern alkalmazástervező segítségével legfeljebb öt egyéni entitást adhatnak hozzá a megoldáshoz. |
| Idő és költség | 2628285. | Kijavított egy problémát, amely hatással volt a megfelelő erőforrás-kategória beállítására az időbevitel importálása során. |
|   Lehetőségkezelés| 2628815. | Frissítse az árajánlatsor részletes leírásának karakterkorlátját, hogy megfeleljen a feladat tárgya karakterkorlátának, hogy az importálás sikeres legyen az olyan feladatok esetén, amelyek tárgya 100 karakternél hosszabb. |
| Idő és költség| 2629547. | A projekt-jóváhagyások **Beküldő** mezője a bejegyzést beküldő felhasználóra kell mutasson. |
| Idő és költség| 2629865. | A **Kategória másolása** mező a feladatokon projektek másolásakor |
| Idő és költség| 2636463. | A jóváhagyások szűrőit a modern jóváhagyási űrlapokon javította. |
| Projekttervezés és nyomon követés | 2648300. | Kijavított egy problémát, amely megakadályozza a projekt tulajdonosának módosítását. |
| Számlázás és árképzés | 2563000. | Nem engedélyezettek a naplósorok a nem számlázott értékesítéshez, amennyiben a pénznem eltér a szerződés pénznemétől. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmenedzsment és könyvelés a Dynamics 365 Finance alkalmazásban

Ha további tájékoztatást szeretne kapni a frissítésben található hibajavításokról, lépjen be a Microsoft Dynamics Lifecycle Services (LCS) szolgáltatásokba, és tekintse meg a [Tudásbázis cikket](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
