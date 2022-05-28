---
title: Újdonságok 2021. júliusában – Project Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez
description: A témakör a Project Operations 2021. júliusi kiadásában erőforrás-alapú vagy nem készletalapú forgatókönyvekhez elérhető minőségi frissítésekkel kapcsolatban nyújt tájékoztatást.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1c88f3b4747005bee0d68d0e8a4314c01ffdaf34
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600883"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok 2021. júliusában – Project Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez

*Érvényesség: Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén*

Ez a témakör a következő Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

   - Project Operations 4.12.0.148 vagy 4.12.0.152 verziójú Microsoft Dataverse-környezetben.
   - Projektmenedzsment és számvitel Dynamics 365 Finance környezetvédelmi verzióban 10.0.20.

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

Ez a kiadás a következő funkciókat tartalmazza:

- A rendszergazdák számára a PSS-naplók és a Műveletkészletek naplóinak a beállítások menüből való megtekintésének lehetősége. A naplókat 90 napig tárolja a rendszer.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Ebben a kiadásban nincsenek frissítések a Project Operations kettős írású leképezéseihez.

A Project Operations kettős írású leképezései aktuális listájának és verzióinak felsorolását lásd: [Project Operations kettős írás leképezési verziói](../environment/resource-dual-write-maps.md).

A Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése során mindig futtassa a környezetben a leképezés legújabb verzióját, és engedélyezze az összes kapcsolódó táblaleképezést. Előfordulhat, hogy bizonyos funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verziója **Kettős írás** oldalon látható a **Verzió** oszlopban. Aktiválhatja a leképzés új verzióját a **Táblaleképezés verziója** lehetőség kiválasztásával, majd a legújabb verzió kiválasztásával, majd a kiválasztott verzió mentésével. Ha testreszabta az egyedi táblatérképet, újra kell alkalmaznia a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha probléma merül fel a leképezés indítása során, kövesse a [Hiányzó táblaoszlopokkal kapcsolatos probléma a leképezésekben](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) részt a Kettős írás hibaelhárítási útmutatójában.

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| **Funkcióterület**              | **Hivatkozási szám** | **Minőségi frissítés**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Számlázás és árképzés           | 2224046              | A **Tranzakcióosztály** mező az **Árajánlatsor részletei** lapon szerkeszthető, de zárolva van, ha az **Árajánlatsor részletei** oldalról dolgozik.                                                                     |
| Számlázás és árképzés           | 2224400              | Az **Ajánlat lezárása megnyertként** művelet sikertelen, ha az ajánlathoz nem tartoznak dátummérföldkövek.                                                                                                                                    |
| Számlázás és árképzés           | 2234089              | Amikor kézzel ír be egy termékleírást, a rendszer törli a adatokat, miután mennyiséget adott meg egy anyagbecsléshez.                                                                                                                         |
| Számlázás és árképzés           | 2234100              | A **Feladatszámlázás beállítás** rács nem tartalmazza az **Anyag** oszlopot és az értékéta projekt **Feladat számlázása** lapján.                                                                                                       |
| Számlázás és árképzés           | 2277409              | A termékazonosító nem érhető el a szerződéssor-részleteiben egy anyagtípus sorához.                                                                                                                                        |
| Számlázás és árképzés           | 2281728              | A szerződéssorok létrehozása szükségtelenül újraértékeli a tényleges adatokat, jelentősen növelve az adatok mennyiségét, ami hatással van a teljesítményre.                                                                                |
| Számlázás és árképzés           | 2298668              | A rendszer nem távolítja el a visszahívott és törölt kiadásokhoz társított naplósorokat.                                                                                                                                     |
| Számlázás és árképzés           | 2300192              | Amikor több felhasználó szerkeszt egy számlát, lehetséges, egy új számlasor részleteinek léterhozása egy megerősített számlán.                                                                                   |
| Számlázás és árképzés           | 2301569              | A számlák nem javíthatók, ha egy 0\$ összegű foglalót alkalmaznak.                                                                                                                                        |
| Számlázás és árképzés           | 2307965              | Hiba történik, ha egy kategóriaárat hiányzó értékekkel hoznak létre.                                                                                                                           |
| Számlázás és árképzés           | 2326870              | Hiba történik a **Microsoft.Dynamics.ProjectService.Plugins.PostInvoserviceLineDelete** elemben, ha a **producttypecode** értéke null.                                                                            |
| Számlázás és árképzés           | 2332732              | Hiba történik, ha a szerződéssor mérföldkövét megrendeléssor nélkül hozzák létre.                                                                                                                |
| Projekttervezés és nyomon követés | 2181094              | A Projektütemezés API mostantól támogatja a PSS-naplókat és Műveletkészlet-naplókat, amelyek 90 napig vannak tárolva.                                                                                                                  |
| Projekttervezés és nyomon követés | 2254201              | A rendszer frissíti az **Ütemezési mód** címkéjét az alapértelmezett logikát leíró adatokkal.                                                                                                                                      |
| Projekttervezés és nyomon követés | 2300252              | Az **openProject** válasz gyorsítótára frissül, és tartalmazza a lexikális elem tuljdonosát a gyorsítótárban, az **alap URL-cím** és a **Szegmens URL-címe** elemekben, hogy a **Kérelmező URL-cím** mindig újra létrehozható legyen, ha az **alap URL-cím** megváltozik. |
| Projekttervezés és nyomon követés | 2301312              | Az **msdyn_membershipstatus** törölve lett a **Projekt csoporttag** nézetből.                                                                                                                                        |
| Projekttervezés és nyomon követés | 2302759              | A termékek feleslegesen beolvasásra kerülnek az **Erőforrás-hozzárendelések**, a **Becslések** és **Költségbecslések** lapokon.                                                                                                        |
| Projekttervezés és nyomon követés | 2308050              | A **CopyProject** hibát jelez: „Sikertelen a jogkivonat lekérése a távoli szolgálatással való kommunikációhoz”.                                                                                                                           |
| Projekttervezés és nyomon követés | 2322650              | A **Projektfeladat lista** nézete frissítve lett, hogy alapértelmezetten a feladat dátumát jelenítse meg.                                                                                                            |
| Projekttervezés és nyomon követés | 2327266              | A **CopyProject** „A kulcs nem található a szótárban” hibaüzenetet generál a becslések másolásakor.                                                                                                      |
| Projekttervezés és nyomon követés | 2328123              | A **CopyProject** sikertelen a következő hibával: „Sikertelen a jogkivonat lekérése a távoli szolgálatással való kommunikációhoz”.                                                                                                                          |
| Projekttervezés és nyomon követés | 2336258              | A **CopyProject** nem megfelelően másolja át az erőforrások pozícióneveit.                                                                                                                                                 |
| Számlázás és árképzés           | 2224476              | A **Foglalható erőforrás** mező nem áll megfelelően alaphelyeztbe a bejelentkezett felhasználóhoz az **Anyaghasználat** lapon.                                                                                                            |
| Erőforráskezelés           | 2277249              | Nem projektalapú erőforrás-követelmény frissítése során hiba történik.                                                                                                            |
| Erőforráskezelés           | 2323869              | Az erőforrás-kihasználtásg nem ismeri fel megfelelően a szűrt erőforrásokat.                                                                                                                                             |
| Idő és költség              | 2176538              | A rendszer helytelen szűrőoperátorokat alkalmaz az **Időbejegyzés** vezérlőre.                                                                                                                                                   |
| Idő és költség              | 2177462              | A rács egy időbejegyzésének törlésekor nem frissül a **Küldés**, a **Visszahívás**, a **Törlés** és a **Bejegyzés szerkesztése** gomb állapota a várakozásoknak megfelelően.                                                                                        |
| Idő és költség              | 2299985              | A **TimeEntalbumImportResourceAsignment** nem tartja meg a kezdő/záró időpontot a hozzárendelés-kontúrokból.                                                                                                  |
| Idő és költség              | 2318426              | Az időbejegyzés beküldését követően a zárolt mezők továbbra is szerkeszthetők.                                                                                                                                   |
| Idő és költség              | 2323749              | Hiba történik, ha egy foglalható erőforrás **Kapcsolódó** lapjáról költséget hoznak létre.                                                                                                      |
| Idő és költség              | 2327678              | Ha egy foglalható erőforrás **Kapcsolódó** lapjáról hoz létre időbejegyzést, a fölérendelt erőforrás nem lesz átadva időbejegyzés vezérlőnek.                                                                            |
| Általános                       | 2296857              | A hosszú feladatok előrehaladásának nyomon követése.                                                                                                                                                                        |
| Általános                       | 2253682              | A Project Operations kettős írású megoldását nem szabad telepíteni, ha a kettős írás alapcsolmag telkepítve van egy környezetben a kettős írású vezénylési megoldás nélkül.                                                |
| Általános                       | 2316420              | A Project Service alap központi kiépítése sikertelen az alkalmazásfelhasználó részlegének megváltozása esetén.                                                                                                                     |
| Általános                       | 2376405              | Rögzített közzétevőre épülő frissítéssel kapcsolatos probléma (A minőségi frissítés a 4.12.0.152 verzióban érhető el)                                                                                                                     |
### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektmenedzsment és számvitel Dynamics 365 Finance

| Funkcióterület                      | Hivatkozási szám | Minőségi frissítés                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektvezetés és könyvelés | 4620267          | Nem szabhat testre űrlapokat a **Cél** mező hozzáadásához a **Porjektben feladott tranzakció**, **Számlajavaslat létrehozása** és **Számlajavaslat** oldalakhoz.                                                                                                                                                                                         |
| Projektvezetés és könyvelés | 4613449          | Amikor kiválaszt egy Projektszerződés-azonosítót a Finaince-ban, a Project Operations integrált környezet megnyitja az oldalt egy rekord léterhozásához, ahelyett hogy megnyitná a már létrehozott projektszerződés oldalát.                                                                                                                                           |
| Projektvezetés és könyvelés | 4614445          | A Project Operations integrált forgatóköny-telepítésében nem szerkeszthető az előkészítésből importált számlajavaslat **Cikkáfacsoport** mezője. A cikkáfacsoportnak szerkeszthetőnek kell lennie egy megnyitott számlajavaslat esetében minden tranzakciótípushoz beleértve a számlát, órákat, kiadásokat és cikkeket. |
| Projektvezetés és könyvelés |                  | Negatív időtranzakció-helyesbítésből származó számlajavaslat nem tehető közzé.                                                                                                                                                                                                                                              |
| Projektvezetés és könyvelés |                  | A számlajavaslatok sorai duplikáltak, mivel az **Importálás előkészítésből** időszakos folyamat több példánya fut egyszerre.                                                                                                                                                                                                                |

