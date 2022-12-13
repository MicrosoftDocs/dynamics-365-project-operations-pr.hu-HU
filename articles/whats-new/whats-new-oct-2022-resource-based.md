---
title: 2022. októberi újdonságok – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a cikk a Microsoft Dynamics 365 Project Operations 2022. októberi kiadásában az erőforrás-/nem készletalapú forgatókönyvekhez elérhető minőségi frissítésekről nyújt tájékoztatást.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806728"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022. októberi újdonságok – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a cikk a következő Microsoft Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations 4.57.0.176 verziójú Dataverse-környezetben
- Projektmenedzsment és könyvelés a Dynamics 365 Finance 10.0.30-es verziójú környezetekben

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

| Funkcióterület | Funkció neve | További információ |
| --- | --- | --- |
| Projekttervezés és nyomon követés | **Projektműveletek külső ütemezése**<br>A külső ütemezési mód lehetővé teszi az ügyfelek számára, hogy natív módon hozzanak létre, frissítsenek és töröljenek olyan entitásokat, amelyek a munkalebontási struktúrákhoz (WBS) kapcsolódnak a natív Dataverse API-k használatával, a webes Project által kényszerített aktuális korlátok nélkül. | [Külső ütemezés](/dynamics365/project-operations/project-management/external-scheduling) |
| Központi telepítés és konfiguráció | <p>**A központi telepítési típus kiválasztásának engedélyezése az ügyfelek számára**<br>A Project Operations termékvezérelt frissítései (PDU-k) a Project Operations kettős írási megoldásának automatikus telepítésére szolgálnak, amikor a kettős írási mag és a vezénylési megoldások telepítve vannak a környezetben.</p><p>Ez a funkció egy új **megoldásfrissítési viselkedési paramétert** vezet be a Project-paraméterekben. Ha ez a paraméter csak **Lite értékre** van állítva, a PUD-k már nem telepítik automatikusan a Project Operations kettős írási megoldást, még akkor sem, ha a kettős írási mag és a vezénylési megoldások telepítve vannak a környezetben. Ez a viselkedés előnyös lesz azoknak az ügyfeleknek, akik kettős írási megoldásokat terveznek használni az értékesítési rendelések pénzügyi és üzemeltetési alkalmazásokba való integrálására, de a Project Operations egyszerűsített módban szeretnék használni (azaz a pénzügyi és üzemeltetési alkalmazásokba való integráció nélkül).</p> | |
| Számlázás és árképzés | <p>**Pénznemek közötti átváltás a költség nélküli számlázatlan értékesítési tranzakcióhoz integrált környezetekben**<br>Azoknál az ügyfeleknél, akik a Project Operations rendszert a pénzügyi és üzemeltetési alkalmazásokkal integrálva használják (azaz az erőforrás/nem készletezett telepítési típusban), az átváltási árfolyamokat általában a pénzügyi és üzemeltetési alkalmazásokban határozzák meg. Ha azonban egy költségkategóriát a "költségen felüli" vagy a "ráírás a költséghez képest" árszámítási módszerrel kell árazni a vevő számlázásakor, akkor az értékesítési összeg kiszámításához használt árfolyam a Finance Dataverse and Operations alkalmazások átváltási árfolyamait használja.</p><p>Ez a funkció egy új **Pénznemátváltási viselkedés** paramétert vezet be a Projekt paramétereiben. Ha ez a paraméter Tartalékkal **kiterjesztve értékre** van állítva, a költségtranzakciók számlázatlan értékesítési összegei a pénzügyi és üzemeltetési alkalmazások árfolyamai alapján kerülnek kiszámításra.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Ebben a kiadásban nincsenek frissítések a Project Operations kettős írású leképezéseihez. A Project Operations kettős írású leképezései aktuális listájának és verzióinak felsorolását lásd: [Project Operations kettős írás leképezési verziói](../environment/resource-dual-write-maps.md).

A Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése során mindig futtassa a környezetben a leképezés legújabb verzióját, és engedélyezze az összes kapcsolódó táblaleképezést. Előfordulhat, hogy bizonyos funkciók és képességek nem működnek megfelelően, ha a leképezés legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy gyári táblaleképezést, újra kell alkalmaznia a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha problémát tapasztal a leképezés elindításával kapcsolatban, kövesse a [Kettős írás hibaelhárítási útmutató térkép szakaszának Hiányzó táblaoszlopok című](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) részében található utasításokat.

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Számlázás és árképzés | 2316317. | A rendszer lehetővé teszi olyan számlák létrehozását, amelyek nem tartalmaznak terhelhető tranzakciókat. |
| Számlázás és árképzés | 2737300. | Ellenőrizze az Ügyfél **mező rendelkezésre állását az** űrlap elérése előtt. |
| Számlázás és árképzés | 2744948. | Adjon hozzá egy null ellenőrzést a számlázási módszerhez. |
| Számlázás és árképzés | 2763515. | Null referencia hibakezelő esetén, ha hiányzik a számla adásvételi szerződése. |
| Számlázás és árképzés | 2844301. | A kötegelt számla létrehozása hiba miatt meghiúsul. |
| Számlázás és árképzés | 2845869. | A Szervezeti szolgáltatás helytelen tárolása. |
| Számlázás és árképzés | 2853729. | A szerepkör és az ár részletei a számlázási típus módosításakor frissülnek. |
| Számlázás és árképzés | 2940350. | A tényleges adatok árazásakor csak az aktív árlistákat kell automatikusan megadni. |
| Központi telepítés és konfiguráció | 3001206. | Az msdyn\_ replaylogheader entitás megakadályozza az ügyfélszervezetek frissítését. |
| Lehetőségkezelés | 2755582. | A null értékű kivételek kezelése a Felosztásos számlázási szabály segítőjében. |
| Lehetőségkezelés | 2761477. | Felosztásos számlázás használata esetén a mérföldkő (fejléc) törlése árva mérföldköveket hagy maga után. |
| Lehetőségkezelés | 2767595. | Amikor megnyitnak egy anyaghasználati rekordot a főképernyőn, a rekord foglalható erőforrása az aktuálisan bejelentkezett felhasználóra változik. |
| Projekttervezés és nyomon követés | 2790384. | A Függőben lévő műveletkészlet időtúllépése túl rövid. |
| Projekttervezés és nyomon követés | 2957840. | A tevékenységek nem menthetők, és az oszlopok nem adhatók hozzá az **Integrált projektműveletek Tevékenységek** lapjához. |
| Erőforráskezelés | 2751560. | Inkonzisztens előnyben részesített szervezeti egységek az erőforrás-követelményben. |
| Alvállalkozásba adás | 2853245. | A szállítói számlasor tényadatainak egyeztetése nem frissíti az ellenőrzési állapotot, ha egy szerződéssor már csatolva van a szállítói számla sorához. |
| Alvállalkozásba adás | 2907231. | A szállítói számlák feldolgozási szakasza nem haladhat előre. |
| Idő és költség | 2867363. | A rekordok nem esnek ki a Távollétek/Szabadságok jóváhagyásra nézetből, amikor várólistára kerülnek jóváhagyásra. |
| Idő és költség | 2894405. | TESA: A nem használt POC-könyvtár megfelelőségi problémákat okoz. |

### <a name="project-management-and-accounting-in-finance"></a>Projektmenedzsment és könyvelés a Finance-ban

Ha további tájékoztatást szeretne kapni a frissítésben található hibajavításokról, lépjen be a Microsoft Dynamics Lifecycle Services (LCS) szolgáltatásokba, és tekintse meg a [Tudásbázis cikket](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
