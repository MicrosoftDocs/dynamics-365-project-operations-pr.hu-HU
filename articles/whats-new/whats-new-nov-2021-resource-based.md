---
title: Újdonságok – 2021. november – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a cikk a Project Operations 2021. novemberi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást erőforrás-/nem készletalapú forgatókönyvekhez.
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

Ez a cikk a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Project Operations egy Dataverse környezeti verzióban 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Projektmenedzsment és könyvelés Dynamics 365 Finance környezetben 10.0.22-es verzió

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

Ez a kiadás a következő funkciókat tartalmazza:

- A Project Scheduling alkalmazásprogramozási felületek (API-k) mostantól támogatják a Project-gyűjtők létrehozásának és törlésének lehetőségét.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Ebben a kiadásban nincsenek frissítések a Project Operations kettős írású leképezéseihez. A Project Operations kettős írású leképezései aktuális listájának és verzióinak felsorolását lásd: [Project Operations kettős írás leképezési verziói](/dynamics365/project-operations/environment/resource-dual-write-maps).

Mindig futtassa a térkép legújabb verzióját a környezetében, és engedélyezze az összes kapcsolódó táblaleképezést a Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése közben. Előfordulhat, hogy egyes funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy beépített táblázattérképet, alkalmazza újra a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha a térkép indításakor problémába ütközik, kövesse a Kettős írás hibaelhárítási útmutató Hiányzó táblaoszlopok probléma a térképeken [című szakaszának utasításait](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-in-dataverse"></a>Projektműveletek itt: Dataverse

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Számlázás és árképzés | 2240080 | A **Fizetési feltételek** mező nem ismétlődik meg a pro forma számlán. |
| Számlázás és árképzés | 2358236 | A számlakorrekciónak lehetővé kell tennie a nulla árú sorokkal rendelkező javításokat. |
| Erőforráskezelés | 2410072 | A tevékenységhez projektmenedzserként rendelt erőforrás beállításának engedélyezése. |
| Számlázás és árképzés | 2430234 | Javítsa ki a költségteljesítmény-számítási problémát. |
| Idő és költség | 2436978 | Hagyjon időt a hh:mm formátumban történő beírására. |
| Számlázás és árképzés | 2448623 | Engedélyezze az árlisták frissítését, miután társították őket egy szervezeti egységhez. |
| Idő és költség | 2460396 | Hagyja, hogy egy időbejegyzés törlődjön a cella törlésével. |
| Számlázás és árképzés | 2467386 | Engedélyezze egy tevékenységgel rendelkező projekt törlését akkor is, ha a tevékenység megnyert árajánlathoz van társítva. |
| Idő és költség | 2461744 | A **Sikertelen jóváhagyásom** nézet csak a **Beküldött** szakaszban lévő projektjóváhagyásokat tartalmazza. |
| Idő és költség | 2464082 | Távolítsa el a hivatkozást a projektjóváhagyásokból a célállapot egyeztetésekor beállított jóváhagyási beállításra. |
| Idő és költség | 2468108 | Az Ütemezési feladat nem állíthat be **Feldolgozási** állapotot a jóváhagyási készlethez. |
| Idő és költség | 2471503 | Törölje a hétnapos jóváhagyási készleteket. |
| Számlázás és árképzés | 2480687 | Az idézőjelsor-hivatkozást nem szabad eltávolítani az árajánlatsor mérföldkövének létrehozásakor. |

### <a name="project-management-and-accounting-in-finance"></a>Projektmenedzsment és számvitel a pénzügyekben

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Projektvezetés és könyvelés | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | A projektköltség-tranzakciókban visszatartott szállítói összegek nem jelennek meg a tranzakciólistában. |
| Projektvezetés és könyvelés | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | A vállalatközi szállítói számla megszakad, ha a szállítói számla integrációja be van kapcsolva. |
| Projektvezetés és könyvelés | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | A projektszámlák fizetési feltételei nem a várt módon működnek. |
| Projektvezetés és könyvelés | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | A szállítói megtartás felszabadításakor a bizonylat feladása további sorokat tartalmaz, amelyek helytelenek. |
| Projektvezetés és könyvelés | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | A Project Operations integrációs naplójának feladásakor az meghiúsul, mert hiányoznak a dimenziók egy olyan fiókhoz, amely nem van közzétéve. |
| Projektvezetés és könyvelés | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | A **Projekt** lap nem szerkeszthető függőben lévő szállítói számlán, ha a beszerzési kategória hozzá van rendelve a cikkhez. |
| Projektvezetés és könyvelés | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | A navigációs ablak hiányzik, ha nincs bejelentkezve a Project Operations szolgáltatásba Dataverse. |
| Projektvezetés és könyvelés | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Amikor egy projektszámlából származó bevételt egy alkalmazott megőrzői esetben ad fel, probléma merül fel, mert a bizonylaton lévő tranzakciók nem állnak felül. |
| Projektvezetés és könyvelés | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | A becslés létrehozása a számlajavaslat feladása után megakadályozza a javítóvonalak importálását. |
| Projektvezetés és könyvelés | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | A teljes mértékben számlázott mérföldkő-rekord módosítása nem lehetséges. |
| Utazás és költség | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Minden költségjelentés látható, amikor egy kategóriát keres a Költség mobilalkalmazásban. |
| Utazás és költség | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | A szállítói tranzakciók és az áfatranzakciók helytelen összegei egy hitelkártya-tranzakcióból létrehozott költségből kerülnek feladásra. |
| Utazás és költség | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Irreleváns figyelmeztetés jelenik meg a **Költségjelentés** oldal frissítésekor. |
| Utazás és költség | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | A rendszer rossz ideiglenes jóváhagyót használ, amikor töröl egy ideiglenes jóváhagyót, majd újra elküldi a költségjelentést a munkafolyamaton keresztül. |
| Utazás és költség | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | A futásteljesítmény beállításával kapcsolatos feladási hiba lép fel. |
