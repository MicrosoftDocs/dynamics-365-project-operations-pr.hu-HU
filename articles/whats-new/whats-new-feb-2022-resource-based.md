---
title: Újdonságok – 2022. február – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a cikk a Project Operations 2022. februári kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást erőforrás-/nem készletalapú forgatókönyvekhez.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932989"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok – 2022. február – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

*Érvényesség: Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén*

Ez a cikk a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Project Operations egy Dataverse környezeti verzióban 4.28.0.120
- Projektmenedzsment és könyvelés Dynamics 365 Finance környezetben 10.0.24-es verzió

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

- Ettől a kiadástól kezdve akár 300 csapattagot is hozzáadhat egyetlen projekthez. Korábban a csapattagok számának korlátja 150 volt. További információ: [Projektkorlátok](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>A Project Operations kettős írású térképfrissítései

Az alábbi lista azokat a kettős írású leképezéseket mutatja be, amelyeket módosítottak vagy hozzáadtak a Project Operations 2022. februári kiadásához.

| Entitásleképezés | Frissített verzió | Hozzászólások |
| --- | --- | --- |
| Project Operations integrációs projekt költségeinek exportálási entitása (msdyn\_ költségek) | 1.0.0.3 | Kiterjesztve a projekttevékenységek szinkronizálására a következőre:Dataverse. |

A Project Operations kettős írású leképezéseinek aktuális listájáért és verzióiért lásd: [Project Operations kettős írású térképverziók](../environment/resource-dual-write-maps.md).

Mindig futtassa a térkép legújabb verzióját a környezetében, és engedélyezze az összes kapcsolódó táblaleképezést a Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése közben. Előfordulhat, hogy egyes funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy beépített táblázattérképet, alkalmazza újra a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha a térkép indításakor problémába ütközik, kövesse a Kettős írás hibaelhárítási útmutató Hiányzó táblaoszlopok probléma a térképeken [című szakaszában található](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) utasításokat.

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Számlázás és árképzés | 2415109 | Az Operatív fizetési feltételek **mező alapértelmezett értékének** a projektszerződés vevői rekordjának és a proforma számlarekordnak kell lennie. |
| Számlázás és árképzés | 2497369 | Az anyagkorrekciónak követnie kell a **korrekciós** paraméterek dátumértékét. |
| Számlázás és árképzés | 2498697 | Továbbfejlesztettük az Időbevitel visszahívásának biztonsági **konfigurációját**. |
| Számlázás és árképzés | 2513824 | Erőforrás-alapú forgatókönyvek esetén a tranzakciós kategória azonosítója nem haladhatja meg a 28 karaktert a Project Operationsben. |
| Számlázás és árképzés | 2517455 | A **Számlasor tranzakcióinak** frissítése művelet nem aktiválható egyszerre több alkalommal ugyanazon számla esetében. |
| Számlázás és árképzés | 2517465 | A **Számlasor részleteinek** inaktiválása művelet le van tiltva, mert nem támogatott. |
| Számlázás és árképzés | 2556660 | Rögzítettük a dátum-effektivitás ellenőrzését, amely a projektparaméter-rekordhoz csatolt árlistán történik. |
|   Lehetőségkezelés | 2369202 | Kijavítottuk azt az üzleti logikát, amely ellenőrzi, hogy az egymást átfedő hatásidőpontokkal rendelkező árlisták csatolhatók-e ugyanahhoz a projektszerződéshez. |
|   Lehetőségkezelés | 2385965 | Kijavítottuk a viselkedést a **Projektszerződés** oldal Vevők **lapján, amikor a** Mentés és bezárás **lehetőséget választotta**. |
| Idő és költség | 2538503 | A projekttevékenységnek elérhetőnek kell lennie a **Projekt tényleges adatai** entitásban a költségjelentés feladása után. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektmenedzsment és könyvelés a Dynamics 365 Finance

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Projektvezetés és könyvelés | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | A szállítói jóváírások importálása során hiba történik. A hibaüzenet a következőt tartalmazza: "A megőrzési összeg nem lehet több, mint a fennmaradó nettó összeg." |
| Projektvezetés és könyvelés | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Ha egy számlajavaslat olyan nulla összegű díjtranzakciókat tartalmaz, amelyek nem számlázott értékesítési tényleges adatok, a számlázás nem történhet meg. |
| Projektvezetés és könyvelés | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | A közzétett költség nem megfelelő a vételár frissítése és **a változáskezelés** aktiválása engedélyezése után.|
| Projektvezetés és könyvelés | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Egy rögzített árú projekt feladási becslése helytelen pénznemet és összeget használ a becsült bizonylatban, még akkor is, ha a Projektszerződés pénznemének engedélyezése a **becslés kiszámításához** funkció engedélyezve van. |
| Projektvezetés és könyvelés | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **A ProjDMFDataPopulation\_ extension** nem kezdeményezhet hívást a változáskövetés engedélyezéséhez anélkül, hogy kivételeket észlelne azoknál az entitásoknál, amelyek nincsenek engedélyezve. |
| Projektvezetés és könyvelés | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | A kötegelt feladat akkor lesz javítva, ha több speciális naplót ad fel, és hiba történik. |
| Utazás és költség | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | A költségjelentésekben szereplő készpénzelőlegekkel kapcsolatos elszámolási probléma miatt az adóösszeget nem fedezik a készpénzelőleg részeként. |
| Utazás és költség | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Az áfaadatok nem szerepelnek a **Költség – Feladott tranzakciók** jelentésben. |
| Utazás és költség | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | A **Nyugták szükséges** költségszabályzat megsértése helytelenül figyelmeztetést jelenít meg a költségjelentéseken. |
| Utazás és költség | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | A projekttranzakciók nem tartalmazzák a nem megtérülő forgalmi adót a teljes értékesítési összegben, ha a tranzakció futásteljesítmény-ráfordítás eredménye. |
| Utazás és költség | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Ha egy tételes sornak van adója, nem módosíthatja a tételenkénti sor dátumát, és a forrásbizonylat állapota hiba lép fel. |

## <a name="removed-and-deprecated-features"></a>Eltávolított és elavult funkciók

A [Project Operations](removed-depreciated-features-project.md) eltávolított vagy elavult funkcióiról szóló cikk azokat a funkciókat ismerteti, amelyek eltávolításra vagy elavultak Dynamics 365 Project Operations.

- Az eltávolított funkciók a továbbiakban nem érhetőek el a termékben.
- Az elavult funkciók nincsenek aktív fejlesztés alatt, és előfordulhat, hogy egy későbbi frissítés során el lesznek távolítva.

Az elalvasztási bejelentés 12 hónappal azelőtt jelenik meg a [Project Operations](removed-depreciated-features-project.md) eltávolított vagy elavult funkcióiban, hogy bármely funkciót eltávolítana a termékből.

Az olyan módosítások megszakítása esetén, amelyek csak a fordítási időt érintik, de binárisan kompatibilisek a tesztkörnyezettel és az éles környezetekkel, az elavulási idő kevesebb, mint 12 hónap. Ezek a módosítások általában funkcionális frissítések, amelyeket a fordítón kell elvégezni.
