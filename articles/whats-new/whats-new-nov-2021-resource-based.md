---
title: Újdonságok – 2021. november – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a témakör tájékoztatást nyújt a Project Operations erőforrás-/nem készletalapú forgatókönyvek projektműveleteinek 2021. novemberi kiadásában elérhető minőségi frissítésekről.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 730f9f051c62f44734f2d7915517baf439b1a0b8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584875"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok – 2021. november – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

*Érvényesség: Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén*

Ez a témakör a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Projektműveletek környezeti Dataverse verzióban 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Projektmenedzsment és számvitel Dynamics 365 Finance környezetben 10.0.22-es verzió

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

Ez a kiadás a következő funkciókat tartalmazza:

- A Project Scheduling alkalmazásprogramozási felületek (API-k) mostantól támogatják a Project-gyűjtők létrehozásának és törlésének lehetőségét.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Ebben a kiadásban nincsenek frissítések a Project Operations kettős írású leképezéseihez. A Project Operations kettős írású leképezései aktuális listájának és verzióinak felsorolását lásd: [Project Operations kettős írás leképezési verziói](/dynamics365/project-operations/environment/resource-dual-write-maps).

Mindig futtassa a térkép legújabb verzióját a környezetében, és engedélyezze az összes kapcsolódó táblaleképezést a Project Operations Dataverse megoldás és a Pénzügy megoldás verziójának frissítésekor. Előfordulhat, hogy egyes funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy beépített táblázattérképet, alkalmazza újra a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha a térkép indításakor problémát tapasztal, kövesse a Kettős írás hibaelhárítási útmutató Hiányzó táblázatoszlopok probléma a térképeken [című részében található utasításokat](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-in-dataverse"></a>Projektműveletek helye Dataverse

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Számlázás és árképzés | 2240080 | A **Fizetési feltételek** mezőt nem szabad megismételni a pro forma számlán. |
| Számlázás és árképzés | 2358236 | A számlajavításnak lehetővé kell tennie a nulla árú sorokat tartalmazó javításokat. |
| Erőforráskezelés | 2410072 | A tevékenységhez projektmenedzserként hozzárendelt erőforrás beállításának engedélyezése. |
| Számlázás és árképzés | 2430234 | Költségteljesítmény-számítási probléma javítása. |
| Idő és költség | 2436978 | Hagyja, hogy az idő hh:mm formátumban legyen megadva. |
| Számlázás és árképzés | 2448623 | Az árlisták frissítésének engedélyezése, miután egy szervezeti egységhez vannak társítva. |
| Idő és költség | 2460396 | A cella törlésével törölhet egy időbejegyzést. |
| Számlázás és árképzés | 2467386 | A tevékenységet tartalmazó projekt törlésének engedélyezése, még akkor is, ha a tevékenység nyertes ajánlathoz van társítva. |
| Idő és költség | 2461744 | A **Saját sikertelen jóváhagyás** nézet csak a **Beérkezett szakasz** projekt-jóváhagyásait tartalmazza. |
| Idő és költség | 2464082 | Távolítsa el a hivatkozást a projektjóváhagyásokból a jóváhagyási készlethez, amikor a célállapot megegyezik. |
| Idő és költség | 2468108 | Az Ütemezés feladat nem állíthat be **feldolgozási** állapotot a jóváhagyási készlethez. |
| Idő és költség | 2471503 | Hét napos jóváhagyási készletek törlése. |
| Számlázás és árképzés | 2480687 | Az ajánlatsor hivatkozását nem szabad eltávolítani ajánlatsor mérföldkő létrehozásakor. |

### <a name="project-management-and-accounting-in-finance"></a>Projektmenedzsment és számvitel a pénzügyekben

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Projektvezetés és könyvelés | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | A projektköltség-tranzakciókban visszatartott szállítói összegek nem jelennek meg a tranzakciós listában. |
| Projektvezetés és könyvelés | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | A vállalatközi szállítói számla megszakad, ha a szállítói számla integrációja be van kapcsolva. |
| Projektvezetés és könyvelés | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | A projektszámlák fizetési feltételei nem a várt módon működnek. |
| Projektvezetés és könyvelés | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | A szállítói megőrzés felszabadításakor a bizonylat feladása további helytelen sorokat tartalmaz. |
| Projektvezetés és könyvelés | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | A Project Operations integrációs napló könyvelésekor az sikertelen lesz, mert hiányzik a dimenziója egy olyan számlának, amelyre nincs feladva. |
| Projektvezetés és könyvelés | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | A **Projekt** lap nem szerkeszthető függőben lévő szállítói számlán, ha a beszerzési kategória hozzá van rendelve a cikkhez. |
| Projektvezetés és könyvelés | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | A navigációs ablak hiányzik, ha nincs bejelentkezve a Project Operations programba Dataverse. |
| Projektvezetés és könyvelés | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Ha egy projektszámlából származó bevételt egy alkalmazott megtartó esetben könyvel, a probléma azért következik be, mert a bizonylat tranzakciói nem egyensúlyoznak. |
| Projektvezetés és könyvelés | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Becslés létrehozása számlajavaslat feladása után blokkolja a helyesbítő sorokat az importálásból. |
| Projektvezetés és könyvelés | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | A teljes mértékben számlázott mérföldkőrekord módosítása nem lehetséges. |
| Utazás és költség | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Minden költségjelentés látható, amikor kategóriát keres a Költség mobilalkalmazásban. |
| Utazás és költség | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | A szállítói tranzakciókon és az áfatranzakciókon helytelen összegek feladása egy hitelkártya-tranzakcióból létrehozott költségből történik. |
| Utazás és költség | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | A Költségjelentés **lap frissítésekor** irreleváns figyelmeztetés jelenik meg. |
| Utazás és költség | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | A rendszer nem megfelelő időközi jóváhagyót használ, amikor töröl egy időközi jóváhagyót, majd újra elküld egy költségjelentést a munkafolyamaton keresztül. |
| Utazás és költség | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | A futásteljesítmény beállításával kapcsolatos feladási hiba lép fel. |
