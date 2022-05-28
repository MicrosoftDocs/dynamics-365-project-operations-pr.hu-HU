---
title: Újdonságok 2021. júliusában – Project Operations egyszerű telepítés
description: A témakör a Project Operations 2021. júliusi kiadásában az egyszerű telepítésben elérhető minőségi frissítésekkel kapcsolatban nyújt tájékoztatást.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 475ceea3a6c6db9fe63e3950eaca5d9074faa766
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583955"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Újdonságok 2021. júliusában – Project Operations egyszerű telepítés

_Érvényesség: Lite telepítés – ajánlattól proforma számlázásig_

Ez a témakör a következő Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

  - Project Operations 4.12.0.148 vagy 4.12.0.152 verziójú Dataverse-környezetben.

## <a name="quality-updates"></a>Minőségi frissítések
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
