---
title: Újdonságok – 2022. február – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a cikk információval szolgál az erőforrás/nem készletalapú forgatókönyvek projektjeihez tartozó minőségi frissítésekről, amelyek a Project Operations 2022 februári kiadásában váltak elérhetővé.
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

Ez a cikk a következő Microsoft Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations 4.28.0.120 verziójú Dataverse-környezetben
- Projektmenedzsment és könyvelés a Dynamics 365 Finance 10.0.24-es verziójú környezetekben

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

- A kiadást követően egy projekthez legfeljebb 300 csoporttagot adhat hozzá. Korábban a csoporttagok számának korlátozása 150 volt. További információ: [Projektkorlátok](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Project Operations kettős írású leképzéseinek frissítése

Az alábbi lista a Project Operations 2022. februári kiadásában módosított vagy hozzáadott kettős írású térképeket tartalmazza.

| Entitásleképezés | Frissített verzió | Hozzászólások |
| --- | --- | --- |
| Project Operations integráció projektkiadások exportálási entitása (msdyn\_expenses) | 1.0.0.3 | Kiterjesztve a projekttevékenységek szinkronizálására a Dataverse-be. |

A Project Operations kettős írású leképezései aktuális listájának és verzióinak felsorolását lásd: [Project Operations kettős írás leképezési verziói](../environment/resource-dual-write-maps.md).

A Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése során mindig futtassa a környezetben a leképezés legújabb verzióját, és engedélyezze az összes kapcsolódó táblaleképezést. Előfordulhat, hogy bizonyos funkciók és képességek nem működnek megfelelően, ha a leképezés legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy gyári táblaleképezést, újra kell alkalmaznia a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha problémát tapasztal a leképezés elindításával kapcsolatban, kövesse a [Kettős írás hibaelhárítási útmutató térkép szakaszának Hiányzó táblaoszlopok című](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) részében található utasításokat.

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Számlázás és árképzés | 2415109. | A **Műveletek fizetési feltételei** mezőben az alapértelmezett értéknek a projektszerződés ügyfél-rekordjának és a proforma számla rekordjának kell lennie. |
| Számlázás és árképzés | 2497369. | Az anyagkorrekciónak a **Korrekció** paraméterekben megadott dátumértéket kell követnie. |
| Számlázás és árképzés | 2498697. | Javított a biztonsági beállításokat az **Időbevitel visszahívása** elemhez. |
| Számlázás és árképzés | 2513824. | Erőforrás alapú esetekben a tranzakciókategória azonosítója nem lehet 28 karakternél hosszabb a Project Operations alkalmazásban. |
| Számlázás és árképzés | 2517455. | A **Számlasor-tranzakciók frissítése** művelet nem aktiválható egyszerre több alkalommal ugyanahhoz a számlához. |
| Számlázás és árképzés | 2517465. | A **Számlasor részleteinek inaktiválása** művelet le van tiltva, mert az nem támogatott. |
| Számlázás és árképzés | 2556660. | Javítva lett projektparaméter-rekordhoz csatolt árlistán végzett érvényességidátum-ellenőrzés. |
|   Lehetőségkezelés | 2369202. | Javítva lett az üzleti logika, amely ellenőrzi, hogy ugyanahhoz a projektszerződéshez csatolhatók-e az egymást átfedő dátumokat tartalmazó árlisták. |
|   Lehetőségkezelés | 2385965. | Kijavította a viselkedést a **Projektszerződés** oldal **Ügyfelek** lapján, amikor a **Mentés és bezárás** lehetőséget választja. |
| Idő és költség | 2538503. | Egy projektfeladatnak elérhetőnek kell lennie a **Projekt tényadatai** entitásban egy költségjelentés feladása után. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektmenedzsment és könyvelés a Dynamics 365 Finance alkalmazásban

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Projektvezetés és könyvelés | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Hiba történik a szállítói jóváírások importálása során. A következő hibaüzenet jelenik meg: „A visszatartott összeg nem lehet nagyobb, mint a fennmaradó nettó összeg.” |
| Projektvezetés és könyvelés | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Ha a számlajavaslat olyan nulla összegű díjtranzakciókat tartalmaz, amelyek számlázatlan értékesítési tényadatok, a számlázás nem történhet meg. |
| Projektvezetés és könyvelés | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | A közzétett költség nem helyes a beszerzési ár frissítése és a **Változáskezelés aktiválása** engedélyezése után.|
| Projektvezetés és könyvelés | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | A rögzített árú projekt feladási becslése helytelen pénznemet és összeget használ a becslés bizonylatán, még akkor is, ha engedélyezve van a **Projektszerződés pénznemének engedélyezése a becslés kiszámításához** funkció. |
| Projektvezetés és könyvelés | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | A **ProjDMFDataPopulation\_Extension** nem küldhet hívást, hogy engedélyezze a változások követését kivételek bekövetkezése nélkül olyan entitásokhoz, amelyek nem engedélyezett konfigurációs kulcsokkal rendelkeznek. |
| Projektvezetés és könyvelés | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | A kötegelt feladat javítva lett, több speciális parancsfájl napló feladásakor és hiba történik. |
| Utazás és költség | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | A költségjelentések készpénz-előlegével kapcsolatos kiegyenlítési probléma miatt az adó összegét nem a készpénz-előleg nem fedezi. |
| Utazás és költség | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Az áfainformációkat nem tartalmazza a **Költség – Feladott tranzakciók** jelentés. |
| Utazás és költség | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | A **Nyugta szükséges** költségirányelv megszegése helytelenül figyelmeztetést jeleníti meg a költségjelentésekkel kapcsolatban. |
| Utazás és költség | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | A projekttranzakciók nem tartalmazzák a nem visszaigényelhető áfát a teljes értékesítési összegben, ha a tranzakció a futásteljesítmény-költség következménye. |
| Utazás és költség | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Ha egy tételezett sor adóval rendelkezik, a tételezési sor dátumát nem lehet módosítani, és forrás-dokumentum állapotával kapcsolatos hiba következik be. |

## <a name="removed-and-deprecated-features"></a>Eltávolított és elavult funkciók

A [Project Operations eltávolított vagy elavult funkciói](removed-depreciated-features-project.md) cikk ismerteti azokat a szolgáltatásokat, amelyek el lettek távolítva vagy avultatva lettek a Dynamics 365 Project Operations alkalmazásban.

- Az eltávolított funkciók a továbbiakban nem érhetőek el a termékben.
- Az elavult funkciók nem állnak aktív fejlesztés alatt, és előfordulhat, eltávolíthatják őket egy későbbi frissítésben.

Az avultatási közlemény 12 hónappal az előtt jelenik meg a [Project Operations eltávolított vagy elavult funkciói](removed-depreciated-features-project.md) cikkben, hogy a szolgáltatást eltávolítanák a termékből.

Olyan módosítások esetén, amelyek csak a fordítási időt érintik, de binárisan kompatibilisek a tesztkörnyezettel és a termelési környezettel, az elavulási idő 12 hónapnál rövidebb lesz. Ezek a változások általában olyan funkcionális frissítések, amelyeket a fordítón kell elvégezni.
