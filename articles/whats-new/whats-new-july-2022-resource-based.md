---
title: Újdonságok 2022. júliusában – Project Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez
description: Ez a cikk a Microsoft Dynamics 365 Project Operations 2022. júliusi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást erőforrás-/nem készletalapú forgatókönyvekhez.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403954"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok 2022. júliusában – Project Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a cikk a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Project Operations egy Dataverse környezeti verzióban 4.44.0.22
- Projektmenedzsment és könyvelés Dynamics 365 Finance környezetben 10.0.28-as verzió

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Ebben a kiadásban nincsenek frissítések a Project Operations kettős írású leképezéseihez. A Project Operations kettős írású leképezései aktuális listájának és verzióinak felsorolását lásd: [Project Operations kettős írás leképezési verziói](../environment/resource-dual-write-maps.md).

Mindig futtassa a térkép legújabb verzióját a környezetében, és engedélyezze az összes kapcsolódó táblaleképezést a Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése közben. Előfordulhat, hogy egyes funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy beépített táblázattérképet, alkalmazza újra a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha a térkép indításakor problémába ütközik, kövesse a Kettős írás hibaelhárítási útmutató Hiányzó táblaoszlopok probléma a térképeken [című szakaszának utasításait](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Központi telepítés és konfiguráció | 2761472. | A Project Operations telepítési hibája a rendszer kezeli. |
| Számlázás és árképzés | 2746940. | Az alvállalkozói sor nevének legfeljebb 100 karakter hosszúságúnak kell lennie. |
| Számlázás és árképzés | 2739162. | Az ügyfeleknek látniuk kell a menüszalag gombjait a tényleges rács nézetben. |
| Projekttervezés és nyomon követés | 2730318. | Frissítettük a projekt tárgyában lévő nem támogatott karakterek érvényesítését. |
| Számlázás és árképzés | 2705361. | A mérföldkőnek számlázott értékesítési tényeket bele kell foglalni a projektkövetési mezőkbe. |
| Számlázás és árképzés | 2675880. | Megakadályozhatja, hogy egy projekt olyan szerződéssorhoz kapcsolódjon, amely nem munkaalapú. |
| Számlázás és árképzés | 2664396. | Ha egy árajánlati árlistát árajánlat nélkül ment, akkor olyan hibának kell lennie, amely szerint az árajánlat nem lehet üres. |
| Számlázás és árképzés | 2184019. | A **Feladatalapú számlázás** lap nem jeleníthető meg olyan projekteknél, amelyek nem rendelkeznek támogatási szerződéssel vagy árajánlattal. |
| Idő és költség | 2754459. | Ha az ismétlődő ütemezési felhőfolyamat inaktív, jelenítse meg a szalagcímet, és kerülje meg az aszinkron feldolgozást. |
| Számlázás és árképzés | 2724391. | A rendszer rossz kivételt jelent, ha a projektszerződés felosztása számlázási szabályból hiányzik egy vevői érték. |
| Számlázás és árképzés | 2708638. | A rekord nem található meg az anyaghasználatok és jóváhagyások az anyaghasználatokhoz című témakörben a rácskereséssel végzett keresés során.|
| Számlázás és árképzés | 2686977. | A számlasor érvényesítésének megakadályozása a számla létrehozása során. |
| Számlázás és árképzés | 2683032. | A díjköteles szerepkörök és kategóriák másolása nem lépi túl az 5000 rekordot.|
| Számlázás és árképzés | 2673363. | A Project költségfelhasználási %-a sérült, ha a projekthez az Erőfeszítés és a Költségbecslések és a tényleges adatok is léteznek. |

### <a name="project-management-and-accounting-in-finance"></a>Projektmenedzsment és számvitel a pénzügyekben

A frissítésben található hibajavításokkal kapcsolatos információkért jelentkezzen be a Lifecycle Services (LCS) szolgáltatásba Microsoft Dynamics, és tekintse meg a [tudásbáziscikket](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Alapértelmezés szerint be van kapcsolva funkciók a közelgő kiadásban

Az alábbi táblázat azokat a szolgáltatásokat sorolja fel, amelyek alapértelmezés szerint be vannak kapcsolva a 10.0.29-es verzióban. A legtöbb automatikusan bekapcsolt funkció kikapcsolható a [Funkciókezelésben](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). A jövőben előfordulhat, hogy egyes, automatikusan bekapcsolt funkciók eltávolításra kerülnek a funkciókezelésből, és kötelezővé válnak. Ez a módosítás biztosítja, hogy az ügyfelek a jelenlegi funkciókat használják, így a fejlesztések a hozzáadáskor a jelenlegi funkciókra építhetnek. A funkciók soha nem lesznek automatikusan engedélyezve egy évnél rövidebb idő alatt, kivéve, ha elengedhetetlennek minősülnek.

| Funkció neve | Dátum engedélyezése | Hozzáadott funkció | Funkció állapota | Modul |
| --- | --- | --- |--- |--- |
| Az óratranzakció módosításának engedélyezése a finanszírozási szabály felosztásának változása alapján | 2022. szeptember 16. | 2020. október 7. | Alapértelmezés szerint be van kapcsolva | Projektvezetés és könyvelés |
| Projekt beszerzési rendelés előrefizetési számla visszafordítási funkciója | 2022. szeptember 16. | 2021. október 6. | Alapértelmezés szerint be van kapcsolva | Projektvezetés és könyvelés |
| Számlajavaslat-sorok törlése a Project Operations erőforrás-alapú/nem készletezett forgatókönyvekhez való használatakor | 2022. szeptember 16. | 2021. október 6. | Alapértelmezés szerint be van kapcsolva | Projektvezetés és könyvelés |
| Feladott projekttranzakció könyvelésének módosítása | 2022. szeptember 16. | 2020. május 10. | Alapértelmezés szerint be van kapcsolva | Projektvezetés és könyvelés |
| Alapértelmezett könyvelési beállítás engedélyezése a projekthez | 2022. szeptember 16. | 2020. február 19. | Alapértelmezés szerint be van kapcsolva | Projektvezetés és könyvelés |
| Több szerződéssor engedélyezése a projekthez | 2022. szeptember 16. | 2020. június 29. | Alapértelmezés szerint be van kapcsolva | Projektvezetés és könyvelés |
| A Project Hour-naplók olvashatóvá tétele, ha az aktuális jóváhagyási állapot nem teszi lehetővé a szerkesztést | 2022. szeptember 16. | 2021. október 6. | Alapértelmezés szerint be van kapcsolva | Projektvezetés és könyvelés |
| Értékesítési sorok szinkronizálásának engedélyezése a beszerzési sorokból a beszerzési sorok frissítésekor és a beszerzési rendelés módosításának kezelési paramétere bekapcsolásakor | 2022. szeptember 16. | 2020. október 7. | Alapértelmezés szerint be van kapcsolva | Projektvezetés és könyvelés |
| Projektműveletek engedélyezése Dynamics 365 Customer Engagement | 2022. szeptember 16. | 2020. június 29. | Alapértelmezés szerint be van kapcsolva | Projektvezetés és könyvelés |
| Projekttranzakció-visszafordítási korrekciós funkció | 2022. szeptember 16. | 2020. július 13. | Alapértelmezés szerint be van kapcsolva | Projektvezetés és könyvelés |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funkciók, amelyek kötelezővé válnak a következő kiadásban

Az alábbi táblázat azokat a funkciókat sorolja fel, amelyek a 10.0.29-es verziótól kezdve kötelezőek.

| Funkció neve | Dátum engedélyezése | Hozzáadott funkció | Funkció állapota | Modul |
| --- | --- | --- | --- | --- |
| Számítsa ki a finanszírozási forrás lekötött értékét az árfolyam kerekítése nélkül | 2022. szeptember 16. | 2020. június 14. | Kötelező | Projektvezetés és könyvelés |
| Projektkorrekció feladásának engedélyezése ugyanazzal a főkönyvi számlával, mint az eredeti tranzakció | 2022. szeptember 16. | 2020. június 14. | Kötelező | Projektvezetés és könyvelés |
| A projektszerződés lekötött összegének részletei | 2022. szeptember 16. | 2019. augusztus 31. | Kötelező | Projektvezetés és könyvelés |
| Erőforrás szerinti rendezés engedélyezése a projektszámla-javaslatok létrehozása során | 2022. szeptember 16. | 2019. augusztus 31. | Kötelező | Projektvezetés és könyvelés |
