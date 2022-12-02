---
title: Újdonságok – 2021. november – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a cikk információval szolgál az erőforrás/nem készletalapú forgatókönyvek projektjeihez tartozó minőségi frissítésekről, amelyek a Project Operations 2021. novemberi kiadásában váltak elérhetővé.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d5b58965f728321cc30d4e476b0dacf621fdec71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932897"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok – 2021. november – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

*Érvényesség: Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén*

Ez a cikk a következő Microsoft Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155 verziójú Dataverse-környezetben
- Projektmenedzsment és könyvelés a Dynamics 365 Finance 10.0.22-es verziójú környezetekben

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

Ez a kiadás a következő funkciókat tartalmazza:

- A Projektütemezési alkalmazásprogramozási felületek (API-k) mostantól támogatják a projekthoz szükséges terméktámogatások létrehozására és törlésére vonatkozó képességet.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Ebben a kiadásban nincsenek frissítések a Project Operations kettős írású leképezéseihez. A Project Operations kettős írású leképezései aktuális listájának és verzióinak felsorolását lásd: [Project Operations kettős írás leképezési verziói](/dynamics365/project-operations/environment/resource-dual-write-maps).

A Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése során mindig futtassa a környezetben a leképezés legújabb verzióját, és engedélyezze az összes kapcsolódó táblaleképezést. Előfordulhat, hogy bizonyos funkciók és képességek nem működnek megfelelően, ha a leképezés legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy gyári táblaleképezést, újra kell alkalmaznia a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha problémát tapasztal a leképezés elindításával kapcsolatban, kövesse a [Kettős írás hibaelhárítási útmutató térkép szakaszának Hiányzó táblaoszlopok című](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) részében található utasításokat.

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-in-dataverse"></a>Project Operations a Dataverse-ben

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Számlázás és árképzés | 2240080. | A **Fizetési feltételek** mező nem lehet duplikált a proforma számlán. |
| Számlázás és árképzés | 2358236. | A számlakorrekciónak lehetővé kell tenni a nulla árú sorok korrekcióját. |
| Erőforráskezelés | 2410072. | Egy erőforrás beállításának engedélyezése, amely projektvezetőként van a feladathoz rendelve. |
| Számlázás és árképzés | 2430234. | Egy költségteljesítmény-számításokkal kapcsolatos probléma kijavítása. |
| Idő és költség | 2436978. | Idő bevitelének engedélyezése óó:pp formátumban. |
| Számlázás és árképzés | 2448623. | Az árlisták frissítésének engedélyezése a szervezeti egységhez való társításuk után. |
| Idő és költség | 2460396. | Az időbejegyzés törlésének engedélyezése a cella tartalmának törlésével. |
| Számlázás és árképzés | 2467386. | Feladattal rendelkező projekt törlésének engedélyezése, még akkor is, ha a feladat megnyert ajánlathoz van társítva. |
| Idő és költség | 2461744. | A **Saját sikertelen jóváhagyás** nézet csak **Elküldött** fázisban lévő projekt-jóváhagyásokat tartalmazza. |
| Idő és költség | 2464082. | Távolítsa el a kapcsolatot a projekt-jóváhagyások és a jóváhagyási halmaz között a cél állapot egyeztetésekor. |
| Idő és költség | 2468108. | Az Ütemezési feladatnak nem szabad **Feldolgozás** állapotot beállítani a jóváhagyási halmazhoz. |
| Idő és költség | 2471503. | Törölje a hét napos jóváhagyási halmazokat. |
| Számlázás és árképzés | 2480687. | Az ajánlatsor hivatkozását nem szabad eltávolítani az árajánlatsor mérföldkövének létrehozásakor. |

### <a name="project-management-and-accounting-in-finance"></a>Projektmenedzsment és könyvelés a Finance-ban

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Projektvezetés és könyvelés | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | A projektköltség-tranzakciókban a visszatartott szállítói összegek nem jelennek meg a tranzakciólistában. |
| Projektvezetés és könyvelés | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | A vállalatközi szállítói számla hibás, amikor a szállítói számlák integrálása be van kapcsolva. |
| Projektvezetés és könyvelés | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | A projektszámlák fizetési feltételei nem a várt módon működnek. |
| Projektvezetés és könyvelés | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Egy szállítói foglaló kiadásakor a bizonylat feladása további helytelen sorokat is tartalmaz. |
| Projektvezetés és könyvelés | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | A Project Operations integrációs naplója feladása nem sikerül, mert egy olyan számla dimenziói hiányoznak, amelyhez nincs feladva. |
| Projektvezetés és könyvelés | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | A **Projekt** lap nem szerkeszthető egy függőben lévő szállítói számlán, amikor egy beszerzési kategória van társítva a cikkhez. |
| Projektvezetés és könyvelés | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Ha nem jelentkezik be a Project Operations Dataverse-be, akkor hiányzik a navigációs ablak. |
| Projektvezetés és könyvelés | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Egy alkalmazott foglaló esetében, amikor bevételt ad fel egy projektszámláról, egy probléma történik, mert a tranzakciók a bizonylaton nem egyenlítődnek ki. |
| Projektvezetés és könyvelés | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | A számlajavaslatok feladása után a becslés létrehozása letiltja az importálásból a helyesbítési sorokat. |
| Projektvezetés és könyvelés | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | A teljes számlázott mérföldkövek rekordjának módosítása nem szabad, hogy lehetséges legyen. |
| Utazás és költség | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Minden költségjelentés látható, amikor kategóriára keres a Költség mobilalkalmazásban. |
| Utazás és költség | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | A szállítói tranzakciókkal és áfatranzakciókkal kapcsolatosan helytelen összegek vannak közzétéve egy olyan kiadásból, amelyet egy hitelkártyatranzakcióból hoznak létre. |
| Utazás és költség | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Egy irreleváns figyelmeztetés jelenik meg a **Költségjelentés** oldalának frissítésekekor. |
| Utazás és költség | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Nem a megfelelő ideiglenes jóváhagyó van használva, amikor ideiglenes jóváhagyót töröl, majd a költségjelentést a munkafolyamaton keresztüli újra beküldi. |
| Utazás és költség | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | A futásteljesítmény beállításával kapcsolatos feladási hiba történik. |
