---
title: Újdonságok – 2021. november – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a témakör tájékoztatást nyújt az erőforrás/nem raktározott forgatókönyvek projektműveleteinek 2021. novemberi kiadásában elérhető minőségi frissítésekről.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 20f277bc9b6f571c0144eaaa867bb97c0cf30ddb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827329"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok – 2021. november – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

*Érvényesség: Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén*

Ez a témakör a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Projektműveletek Dataverse környezeti verzióban 4.26.0.145, 4.26.0.148, vagy 4.26.0.150
- Projektmenedzsment és számvitel Dynamics 365 Finance környezetben verzió 10.0.22

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

Ez a kiadás a következő funkciókat tartalmazza:

- A Project Scheduling alkalmazásprogramozási felületek (API-k) mostantól támogatják a Projekt-gyűjtők létrehozásának és törlésének képességét.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Ebben a kiadásban nincsenek frissítések a Project Operations kettős írású leképezéseihez. A Project Operations kettős írású leképezései aktuális listájának és verzióinak felsorolását lásd: [Project Operations kettős írás leképezési verziói](/dynamics365/project-operations/environment/resource-dual-write-maps).

Mindig futtassa a térkép legújabb verzióját a környezetében, és engedélyezze az összes kapcsolódó táblaleképezést a Project Operations Dataverse megoldás és a Pénzügyi megoldás verziójának frissítésekor. Előfordulhat, hogy egyes funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy beépített táblázatleképezést, alkalmazza újra a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha a térkép indításakor probléma merül fel, kövesse a [Kettős írás hibaelhárítási útmutató Térképen című cikkoszlopok című részében](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) található utasításokat.

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-in-dataverse"></a>Projektműveletek Dataverse

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Számlázás és árképzés | 2240080 | A **Fizetési feltételek mező nem** duplikálható a pro forma számlán. |
| Számlázás és árképzés | 2358236 | A számlakorrekciónak lehetővé kell tennie a nulla árú sorokkal kapcsolatos javításokat. |
| Erőforráskezelés | 2410072 | A tevékenységhez projektmenedzserként hozzárendelt erőforrás beállításának engedélyezése. |
| Számlázás és árképzés | 2430234 | Költségteljesítmény-számítási probléma megoldása. |
| Idő és költség | 2436978 | Hagyja meg az idő hh:mm formátumban való beírására. |
| Számlázás és árképzés | 2448623 | Lehetővé teszi az árlisták frissítését, miután egy szervezeti egységhez társították őket. |
| Idő és költség | 2460396 | A cella törlésével engedélyezze az időbejegyzés törlését. |
| Számlázás és árképzés | 2467386 | A tevékenységgel rendelkező projekt törlésének engedélyezése akkor is, ha a tevékenység egy megnyert ajánlathoz van társítva. |
| Idő és költség | 2461744 | A **Sikertelen** jóváhagyási nézet csak a Benyújtott szakaszban tartalmaz projekt-jóváhagyásokat. **·** |
| Idő és költség | 2464082 | Távolítsa el a hivatkozást a projekt-jóváhagyásokból a jóváhagyási készlethez, amikor a cél állapota megegyezik. |
| Idő és költség | 2468108 | Az Ütemezés feladat nem állíthat be **feldolgozási** állapotot a jóváhagyási készlethez. |
| Idő és költség | 2471503 | Hét napos jóváhagyási készletek törlése. |
| Számlázás és árképzés | 2480687 | Az ajánlatsor hivatkozása nem távolítható el ajánlatsor mérföldkő létrehozásakor. |

### <a name="project-management-and-accounting-in-finance"></a>Projektmenedzsment és számvitel a pénzügyekben

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Projektvezetés és könyvelés | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | A projektköltség-tranzakciókban megőrzött szállítói összegek nem jelennek meg a tranzakciólistában. |
| Projektvezetés és könyvelés | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | A vállalatközi szállítói számla megszakad, ha a szállítói számlaintegráció be van kapcsolva. |
| Projektvezetés és könyvelés | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | A projektszámlák fizetési feltételei nem a várt módon működnek. |
| Projektvezetés és könyvelés | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | A szállítói megőrzés felszabadításakor a bizonylat könyvelése további, helytelen sorokat is kínál. |
| Projektvezetés és könyvelés | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | A Projektműveletek integrációs napló feladásakor az meghiúsul, mert hiányoznak a nem könyvelt fiókok méretei. |
| Projektvezetés és könyvelés | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | A **Projekt lap nem** szerkeszthető függőben lévő szállítói számlán, amikor a beszerzési kategóriát a cikkhez rendeli. |
| Projektvezetés és könyvelés | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | A navigációs ablak hiányzik, ha nincs bejelentkezve a Project Operations Dataverse. |
| Projektvezetés és könyvelés | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Amikor egy alkalmazott rögzítő esetben projektszámlából származó bevételt könyvel, probléma merül fel, mert a bizonylat tranzakciói nem egyenleggel. |
| Projektvezetés és könyvelés | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | A számlajavaslat feladása után becslés létrehozása blokkolja a korrekciós sorokat az importálásból. |
| Projektvezetés és könyvelés | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | A teljes számlázott mérföldkőrekord módosítása nem lehetséges. |
| Utazás és költség | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Minden költségjelentés látható, ha kategóriát keres a Költség mobilalkalmazásban. |
| Utazás és költség | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | A szállítói tranzakciók és az áfatranzakciók helytelen összegeit a hitelkártya-tranzakcióból létrehozott költségből könyveli a termék. |
| Utazás és költség | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Irreleváns figyelmeztetés történik a **Költségjelentés oldal frissítésekor.** |
| Utazás és költség | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | A program rossz időközi jóváhagyót használ, amikor töröl egy időközi jóváhagyót, majd újra benyújt egy költségjelentést a munkafolyamaton keresztül. |
| Utazás és költség | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | A futásteljesítmény beállításához kapcsolódó feladási hiba lép fel. |
