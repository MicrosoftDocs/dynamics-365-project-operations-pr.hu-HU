---
title: Újdonságok – 2022. február – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a témakör tájékoztatást nyújt az erőforrás-/nem raktározott forgatókönyvek Projektműveleteinek 2022. februári kiadásában elérhető minőségi frissítésekről.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 76ae00517c857415c89d7a03f421686dad28da93
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600837"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok – 2022. február – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

*Érvényesség: Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén*

Ez a témakör a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Projektműveletek környezeti Dataverse verzióban 4.28.0.120
- Projektmenedzsment és számvitel Dynamics 365 Finance környezetben 10.0.24-es verzió

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

- Ettől a kiadástól kezdve legfeljebb 300 csapattagot adhat hozzá egyetlen projekthez. Korábban a csapattagok számának korlátja 150 volt. További információt a Projekt korlátai című témakörben [talál](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>A Project Operations kettős írású térképfrissítései

Az alábbi lista a Project Operations 2022. februári kiadásában módosított vagy hozzáadott kettős írási térképeket mutatja be.

| Entitásleképezés | Frissített verzió | Hozzászólások |
| --- | --- | --- |
| Projektműveletek integrációs projektköltségeinek exportálási entitása (msdyn-költségek\_) | 1.0.0.3 | Kiterjesztve a projekttevékenység szinkronizálásához a programra Dataverse. |

A Project Operations kettős írási leképezéseinek aktuális listáját és verzióit a Project Operations kettős írási leképezési verziói című témakörben [találja](../environment/resource-dual-write-maps.md).

Mindig futtassa a térkép legújabb verzióját a környezetében, és engedélyezze az összes kapcsolódó táblaleképezést a Project Operations Dataverse megoldás és a Pénzügy megoldás verziójának frissítésekor. Előfordulhat, hogy egyes funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy beépített táblázattérképet, alkalmazza újra a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha a térkép indításakor problémát tapasztal, kövesse a Kettős írás hibaelhárítási útmutató Hiányzó táblázatoszlopok probléma a térképeken [című részében található utasításokat](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Számlázás és árképzés | 2415109 | A Műveletek kifizetési feltételek **mező alapértelmezett értékének** a projektszerződés vevői rekordjának és a proforma számlarekordnak kell lennie. |
| Számlázás és árképzés | 2497369 | Az anyagkorrekciónak követnie kell a **Helyesbítési** paraméterek dátumértékét. |
| Számlázás és árképzés | 2498697 | Javította az időbevitel visszahívásának biztonsági **konfigurációját**. |
| Számlázás és árképzés | 2513824 | Erőforrásalapú forgatókönyvek esetén a tranzakciókategória-azonosító nem haladhatja meg a 28 karaktert a Projektműveletek mappában. |
| Számlázás és árképzés | 2517455 | A **Számlasor-tranzakciók** frissítése művelet nem aktiválható egyszerre többször ugyanarra a számlára. |
| Számlázás és árképzés | 2517465 | A **számlasor részleteinek** inaktiválása művelet le van tiltva, mert nem támogatott. |
| Számlázás és árképzés | 2556660 | Kijavítottuk a projektparaméter-rekordhoz csatolt árlistán végzett dátumhatás-ellenőrzést. |
|   Lehetőségkezelés | 2369202 | Kijavítottuk azt az üzleti logikát, amely ellenőrzi, hogy az egymást átfedő effektivitási dátummal rendelkező árlisták csatolhatók-e ugyanahhoz a projektszerződéshez. |
|   Lehetőségkezelés | 2385965 | Kijavítottuk a Projektszerződés lap Vevők lapján a Viselkedést **, amikor a** Mentés és bezárás **lehetőséget választja**.**·** |
| Idő és költség | 2538503 | A projekttevékenységnek elérhetőnek kell lennie a Projekt tényleges entitásában **a** költségjelentés feladása után. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektmenedzsment és számvitel Dynamics 365 Finance

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Projektvezetés és könyvelés | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | A szállítói jóváírások importálása során hiba lép fel. A hibaüzenet így szól: "A megtartási összeg nem lehet több, mint a fennmaradó nettó összeg." |
| Projektvezetés és könyvelés | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Ha egy számlajavaslat olyan nulla összegű díjtranzakciót tartalmaz, amely nem számlázható értékesítési tényleges érték, a számlázás nem történhet meg. |
| Projektvezetés és könyvelés | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | A feladott költség nem megfelelő a beszerzési ár frissítése és **a változáskezelés** aktiválása engedélyezése után.|
| Projektvezetés és könyvelés | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | A rögzített árú projektek feladási becslése a becsült bizonylat helytelen pénznemét és összegét használja, még akkor is, ha a Projektszerződés pénznemének engedélyezése becslésszámítási **funkció** engedélyezve van. |
| Projektvezetés és könyvelés | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **A ProjDMFDataPopulation\_ bővítmény** nem kezdeményezhet hívást a változáskövetés engedélyezésére anélkül, hogy kivételeket kapna az olyan entitások esetében, amelyek konfigurációs kulcsokkal rendelkeznek, amelyek nincsenek engedélyezve. |
| Projektvezetés és könyvelés | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | A kötegelt feldolgozás akkor rögzül, ha több speciális naplót könyvel, és hiba történik. |
| Utazás és költség | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | A költségjelentések készpénzelőlegeivel kapcsolatos elszámolási probléma miatt az adóösszeget nem fedezi a készpénzelőleg részeként. |
| Utazás és költség | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Az áfainformációk nem szerepelnek a **Költség - könyvelt tranzakciók** jelentésben. |
| Utazás és költség | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | A **bevételezések megkövetelt** költségházirend-megsértése helytelenül jelenít meg figyelmeztetést a költségjelentéseken. |
| Utazás és költség | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | A projekttranzakciók nem tartalmazzák a vissza nem térítendő áfát a teljes értékesítési összegben, ha a tranzakció kilométerköltség eredménye. |
| Utazás és költség | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Ha egy tételes sor adóval rendelkezik, a cikktételi sor dátuma nem módosítható, és forrásbizonylat-állapothiba lép fel. |

## <a name="removed-and-deprecated-features"></a>Eltávolított és elavult funkciók

A [Project Operations](removed-depreciated-features-project.md) témakör eltávolított vagy elavult szolgáltatásai a következőhöz lettek eltávolított vagy elavult Dynamics 365 Project Operations szolgáltatásokat írják le:

- Az eltávolított funkciók a továbbiakban nem érhetőek el a termékben.
- Az elavult funkció nincs aktív fejlesztés alatt, és egy későbbi frissítésben eltávolíthatók.

Az elavulás bejelentése megjelenik a [Project Operations](removed-depreciated-features-project.md) eltávolított vagy elavult funkcióiban témakör 12 hónappal azelőtt, hogy bármely funkciót eltávolítanának a termékből.

Olyan módosítások megszakítása esetén, amelyek csak a fordítási időt befolyásolják, de binárisan kompatibilisek a sandbox és az éles környezetekkel, az elavulási idő kevesebb, mint 12 hónap lesz. Ezek a módosítások általában funkcionális frissítések, amelyeket a fordítón kell elvégezni.
