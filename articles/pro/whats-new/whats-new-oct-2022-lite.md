---
title: 2022. október újdonságok – A Project Operations Lite telepítés
description: Ez a cikk a Microsoft Dynamics 365 Project Operations Lite központi telepítésének 2022. októberi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806735"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>2022. október újdonságok – A Project Operations Lite telepítés

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a cikk a következő Microsoft Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations 4.57.0.176 verziójú Dataverse-környezetben

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

| Funkcióterület | Funkció neve | További információ |
| --- | --- | --- |
| Projekttervezés és nyomon követés | **Projektműveletek külső ütemezése**<br>A külső ütemezési mód lehetővé teszi az ügyfelek számára, hogy natív módon hozzanak létre, frissítsenek és töröljenek olyan entitásokat, amelyek a munkalebontási struktúrákhoz (WBS) kapcsolódnak a natív Dataverse API-k használatával, a webes Project által kényszerített aktuális korlátok nélkül. | [Külső ütemezés](/dynamics365/project-operations/project-management/external-scheduling) |
| Központi telepítés és konfiguráció | <p>**A központi telepítési típus kiválasztásának engedélyezése az ügyfelek számára**<br>A Project Operations termékvezérelt frissítései (PDU-k) a Project Operations kettős írási megoldásának automatikus telepítésére szolgálnak, amikor a kettős írási mag és a vezénylési megoldások telepítve vannak a környezetben.</p><p>Ez a funkció egy új **megoldásfrissítési viselkedési paramétert** vezet be a Project-paraméterekben. Ha ez a paraméter csak **Lite értékre** van állítva, a PUD-k már nem telepítik automatikusan a Project Operations kettős írási megoldást, még akkor sem, ha a kettős írási mag és a vezénylési megoldások telepítve vannak a környezetben. Ez a viselkedés előnyös lesz azoknak az ügyfeleknek, akik kettős írási megoldásokat terveznek használni az értékesítési rendelések pénzügyi és üzemeltetési alkalmazásokba való integrálására, de a Project Operations egyszerűsített módban szeretnék használni (azaz a pénzügyi és üzemeltetési alkalmazásokba való integráció nélkül).</p> | |

## <a name="quality-updates"></a>Minőségi frissítések

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Számlázás és árképzés | 2316317. | A rendszer lehetővé teszi olyan számlák létrehozását, amelyek nem tartalmaznak terhelhető tranzakciókat. |
| Számlázás és árképzés | 2737300. | Ellenőrizze az Ügyfél mező rendelkezésre állását az űrlap elérése előtt. |
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
| Erőforráskezelés | 2751560. | Inkonzisztens előnyben részesített szervezeti egységek az erőforrás-követelményben. |
| Alvállalkozásba adás | 2907231. | A szállítói számlák feldolgozási szakasza nem haladhat előre. |
| Idő és költség | 2867363. | A rekordok nem esnek ki a Távollétek/Szabadságok jóváhagyásra nézetből, amikor várólistára kerülnek jóváhagyásra. |
| Idő és költség | 2894405. | TESA: A nem használt POC-könyvtár megfelelőségi problémákat okoz. |
