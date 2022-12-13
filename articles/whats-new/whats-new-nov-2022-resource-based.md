---
title: Újdonságok – 2022. november – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a cikk a Microsoft Dynamics 365 Project Operations 2022. novemberi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást az erőforrás-/nem készletalapú forgatókönyvekhez.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831132"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok – 2022. november – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a cikk a következő Microsoft Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations 4.58.0.119 verziójú Dataverse-környezetben
- Projektmenedzsment és könyvelés a Dynamics 365 Finance 10.0.30-es verziójú környezetekben

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Ebben a kiadásban nincsenek frissítések a Project Operations kettős írású leképezéseihez. A Project Operations kettős írású leképezései aktuális listájának és verzióinak felsorolását lásd: [Project Operations kettős írás leképezési verziói](../environment/resource-dual-write-maps.md).

A Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése során mindig futtassa a környezetben a leképezés legújabb verzióját, és engedélyezze az összes kapcsolódó táblaleképezést. Előfordulhat, hogy bizonyos funkciók és képességek nem működnek megfelelően, ha a leképezés legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy gyári táblaleképezést, újra kell alkalmaznia a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha problémát tapasztal a leképezés elindításával kapcsolatban, kövesse a [Kettős írás hibaelhárítási útmutató térkép szakaszának Hiányzó táblaoszlopok című](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) részében található utasításokat.

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Számlázás és árképzés | 2781818. | A kulcs nem található hiba az anyaghasználati napló alapértelmezett árának megadásakor. |
| Számlázás és árképzés | 2922373. | Nem lehet az idézőjeles sort olyan projekthez kapcsolni, amely elveszett árajánlatként zárult le. |
| Számlázás és árképzés | 2943206. | **A Projektentitás Szerződéssor** mezőjének nem kötelezőnek kell lennie. |
| Számlázás és árképzés | 2953182. | A helyesbítő számlák hibaüzenetének javítása.|
| Számlázás és árképzés | 2959500. | Nem lehet árajánlatsort csatolni olyan projekttevékenységhez, amely már társítva van egy elveszett árajánlathoz.|
| Számlázás és árképzés | 2959560. | "Ez az ügyfél már szerepel a projektszerződésben" üzenet érkezett, miközben bizonyos helyszíneken megnyertként zárta az árajánlatot. |
| Számlázás és árképzés | 3031727. | Az erőforrás-hozzárendelések sikertelenek, és a kötelező "msdyn_Company" mező hiányzik a hibából. |
| Számlázás és árképzés | 3036905. | A tulajdonos vállalat soha nem inicializálódik a ProjectTeamMember-en. |
| Lehetőségkezelés | 2763519. | Null értékű hivatkozási hiba az EnsureProjectContractAllowsUpdates fájlban. |
| Lehetőségkezelés | 2783798. | Ha projektbecsléseket importál az árajánlati sorba, a költség- és anyagbecslésekhez hiányoznak a tevékenységleírások.|
| Lehetőségkezelés | 2988635. | Javítsa a hiba msg leírását az Ügyfél árajánlatból törlésekor. |
| Lehetőségkezelés | 3001191. | Nem lehet árajánlatot létrehozni a Lehetőségből, ha a számlázási módszer null értékként van megadva. |
| Magasabb szintre váltás | 3012324. | A projekt átalakítása sikertelen volt egy olyan projektnél, amelynek nevében olyan vezérlőkarakterek szerepeltek, mint a Tab. || Projekttervezés és nyomon követés | 2790384. | A Függőben lévő műveletkészlet időtúllépése túl rövid. |
| Projekttervezés és nyomon követés | 3044275. | Hiányzó honosítás: missingProjectSchedulerErrorMessage. |
| Projekttervezés és nyomon követés | 3044277. | A Project Recon rácsa nem töltődik be, ha az ütemező nincs beállítva.|
| Erőforráskezelés | 2943153. | Frissítse a Követés lapot, hogy két tizedesjegyet jelenítsen meg az Időtartamhoz.|
| Alvállalkozásba adás | 2932774. | A szállítói számlasor csak olvasási hibája helytelenül jelenik meg. |
| Alvállalkozásba adás | 2939556. | A szállítói számla fejlécének állapotát nem szabad Piszkozat online törlésre állítani, ha nem aktív. |
| Idő és költség | 2939998. | Vegye fel az új TESA verziót a ProjOps-ban. |


### <a name="project-management-and-accounting-in-finance"></a>Projektmenedzsment és könyvelés a Finance-ban

Ha további tájékoztatást szeretne kapni a frissítésben található hibajavításokról, lépjen be a Microsoft Dynamics Lifecycle Services (LCS) szolgáltatásokba, és tekintse meg a [Tudásbázis cikket](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
