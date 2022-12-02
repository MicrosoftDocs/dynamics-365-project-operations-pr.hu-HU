---
title: Újdonságok 2022. júliusában – Project Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez
description: Ez a cikk a Project Operations 2022. júliusi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást a Microsoft Dynamics 365 Project Operations erőforrás/nem készletalapú forgatókönyvek esetében.
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

Ez a cikk a következő Microsoft Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations 4.44.0.22 verziójú Dataverse-környezetben
- Projektmenedzsment és könyvelés a Dynamics 365 Finance 10.0.28-as verziójú környezetekben

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Ebben a kiadásban nincsenek frissítések a Project Operations kettős írású leképezéseihez. A Project Operations kettős írású leképezései aktuális listájának és verzióinak felsorolását lásd: [Project Operations kettős írás leképezési verziói](../environment/resource-dual-write-maps.md).

A Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése során mindig futtassa a környezetben a leképezés legújabb verzióját, és engedélyezze az összes kapcsolódó táblaleképezést. Előfordulhat, hogy bizonyos funkciók és képességek nem működnek megfelelően, ha a leképezés legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy gyári táblaleképezést, újra kell alkalmaznia a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha problémát tapasztal a leképezés elindításával kapcsolatban, kövesse a [Kettős írás hibaelhárítási útmutató térkép szakaszának Hiányzó táblaoszlopok című](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) részében található utasításokat.

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Központi telepítés és konfiguráció | 2761472. | Egy Project Operations telepítési hiba kezelve lett. |
| Számlázás és árképzés | 2746940. | Az alvállalkozói sornevének maximális hossza 100 karakter lehet. |
| Számlázás és árképzés | 2739162. | Az ügyfeleknek meg kell tudni tekinteniük a menüszalag gombokat a tényadatok rácsnézetében. |
| Projekttervezés és nyomon követés | 2730318. | A projekt tárgyában szereplő nem támogatott karakterek frissített ellenőrzése. |
| Számlázás és árképzés | 2705361. | A mérföldkő számlázott tényleges értékesítésinek szerepelnie kell a projektkövetés mezőkben. |
| Számlázás és árképzés | 2675880. | Megakadályozza, hogy egy projekteket egy szerződéssorhoz legyen kapcsolva, ami nem munkaalapú. |
| Számlázás és árképzés | 2664396. | Ha az árajanlat artistáját árajánlat nélkül mentik, akkor hiba szükséges, ami jelzi hogy az ajánlat nem lehet üres. |
| Számlázás és árképzés | 2184019. | Nem szabad megjeleníteni a **Feladatalapú számlázás** lapot olyan projekteknél, amelyekhez nincs mögöttes szerződés vagy ajánlat. |
| Idő és költség | 2754459. | Ha a ismétlődő ütemezés felhőfolyamat inaktív, mutasson egy címsávot, és mellőzze az aszinkron feldolgozást. |
| Számlázás és árképzés | 2724391. | Nem megfelelő kivétel jelenik meg, ha egy projektszerződés felosztása számlázási szabályból hiányzik egy ügyfélérték. |
| Számlázás és árképzés | 2708638. | A rendszer nem talált rekordot az Anyaghasználatok és Anyaghasználatok Jóváhagyásai táblázatos rácskeresése során|
| Számlázás és árképzés | 2686977. | A számlasor ellenőrzésének megakadályozása a számla létrehozásakor. |
| Számlázás és árképzés | 2683032. | A számlázható szerepkörök és kategóriák másolása nem méretez túl 5000 bejegyzésen.|
| Számlázás és árképzés | 2673363. | A projekt költségfogyasztási %-a sérült, ha a projekthez Ráfordítás- és Költségbecslések és tényadatai is léteznek. |

### <a name="project-management-and-accounting-in-finance"></a>Projektmenedzsment és könyvelés a Finance-ban

Ha további tájékoztatást szeretne kapni a frissítésben található hibajavításokról, lépjen be a Microsoft Dynamics Lifecycle Services (LCS) szolgáltatásokba, és tekintse meg a [Tudásbázis cikket](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Az érkező kiadásban alapértelmezetten bekapcsolt funkciók

Ez a kiadás a 10.0.29 verzióban alapértelmezetten bekapcsolt funkciókat tartalmazza. A legtöbb olyan funkció, amely automatikusan be lett kapcsolva, a [Funkciókezelésben](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) kikapcsolható. A jövőben előfordulhat, hogy egyes funkciók, amelyek automatikusan be vannak kapcsolva, eltávolításra kerülnek a Szolgáltatáskezelésből, és kötelezővé válnak. A változás biztosítja, hogy az ügyfelek a naprakész funkciókat használják, így a fejlesztések a hozzáadásuk során a jelenlegi funkciókra épülhessenek. A szolgáltatások egy évnél rövidebb idő alatt soha nem lesznek automatikusan engedélyezve, kivéve ha ez alapvető fontosságú.

| Funkció neve | Dátum engedélyezése | Funkció hozzáadva | Funkció állapota | Modul |
| --- | --- | --- |--- |--- |
| Az óratranzakció korrekciójának engedélyezése a finanszírozási szabály felosztásának módosítása alapján | 2022. szeptember 16. | 2020. október 7. | Alapértelmezés szerint be | Projektvezetés és könyvelés |
| Projekt beszerzési rendelés előre fizetett a számla sztornózása funkció | 2022. szeptember 16. | 2021. október 6. | Alapértelmezés szerint be | Projektvezetés és könyvelés |
| Számlajavaslatsorok törlése Project Operations erőforrás alapú / nem készletalapú forgatókönyvek használata esetén | 2022. szeptember 16. | 2021. október 6. | Alapértelmezés szerint be | Projektvezetés és könyvelés |
| A könyvelés korrekciója egy feladott projekttranzakción | 2022. szeptember 16. | 2020. május 10. | Alapértelmezés szerint be | Projektvezetés és könyvelés |
| Projekt alapértelmezett könyvelési beállításának engedélyezése | 2022. szeptember 16. | 2020. február 19. | Alapértelmezés szerint be | Projektvezetés és könyvelés |
| Több szerződéssor engedélyezése a projekthez | 2022. szeptember 16. | 2020. június 29. | Alapértelmezés szerint be | Projektvezetés és könyvelés |
| A Projektórák legyenek írásvédettek, ha a jelenlegi jóváhagyási állapot nem teszi lehetővé a szerkesztést | 2022. szeptember 16. | 2021. október 6. | Alapértelmezés szerint be | Projektvezetés és könyvelés |
| Az értékesítési sorok frissítésének engedélyezési a vásárlási sorokból, ha a beszerzési sorok módosítva vannak, és felügyeleti paraméter be van kapcsolva | 2022. szeptember 16. | 2020. október 7. | Alapértelmezés szerint be | Projektvezetés és könyvelés |
| A Project Operations a Dynamics 365 Customer Engagement alkalmazásban engedélyezése | 2022. szeptember 16. | 2020. június 29. | Alapértelmezés szerint be | Projektvezetés és könyvelés |
| Projekttranzakciók sztornójavítás funkciója | 2022. szeptember 16. | 2020. július 13. | Alapértelmezés szerint be | Projektvezetés és könyvelés |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>A jövőbeni kiadásban kötelezővé váló szolgáltatások

Ez a kiadás a 10.0.29 verziótól kötelező funkciókat tartalmazza.

| Funkció neve | Dátum engedélyezése | Funkció hozzáadva | Funkció állapota | Modul |
| --- | --- | --- | --- | --- |
| A véglegesített érték kiszámítása a finanszírozási forrásban az átváltási árfolyam kerekítése nélkül | 2022. szeptember 16. | 2020. június 14. | Kötelező | Projektvezetés és könyvelés |
| Projektkorrekció feladásának engedélyezése az eredeti tranzakcióval azonos főkönyvi számlával | 2022. szeptember 16. | 2020. június 14. | Kötelező | Projektvezetés és könyvelés |
| Projektszerződés végleges összegének részletei | 2022. szeptember 16. | 2019. augusztus 31. | Kötelező | Projektvezetés és könyvelés |
| Erőforrás szerinti rendezés engedélyezése projektszámla-ajánlat létrehozása során | 2022. szeptember 16. | 2019. augusztus 31. | Kötelező | Projektvezetés és könyvelés |
