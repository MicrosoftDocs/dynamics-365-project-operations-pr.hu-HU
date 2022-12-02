---
title: 2021. decemberi újdonságok – A Project Operations Lite telepítés
description: Ez a cikk a Project Operations lite telepítés 2021. decemberi kiadásában elérhető minőségi frissítésekkel kapcsolatban nyújt tájékoztatást.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 301acc5be76fb0318d6298820b62ae5bb05efac3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914083"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>2021. decemberi újdonságok – A Project Operations Lite telepítés

_Érvényesség: Lite telepítés – ajánlattól proforma számlázásig_

Ez a cikk a következő Microsoft Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations 4.27.0.195, 4.27.0.242, 4.27.0.244 verziójú Dataverse-környezetben


## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

### <a name="subcontract-management"></a>Alvállalkozók kezelése 

- [Projektcsoporttagok alvállalkozásba adása](../subcontracting/subcontracting-project-team-members.md): A projektvezető létrehozhat elnevezett vagy általános csoporttagokat az alvállalkozói szerződésekkel és alvállalkozói sorokkal, hogy ez hatással legyen a személyzetkiosztásra és a becslésekre.
- [Alvállalkozásba adási lehetőségek a projektcsoporttagokhoz](../subcontracting/subcon-options.md): Amikor személyzeti döntéseket hoz az elnevezett vagy általános projektcsoport-tagokkal kapcsolatosan, a projektmenedzser a projektmenedzser áttekintheti a meglévő alvállalkozói szerződéseket, illetve új alvállalkozói szerződéseket hozhat létre. 
- [Az alvállalkozók erőforrás-hozzárendeléseinek költségelése](../subcontracting/costing-subcon-ra.md): A projekt költségbecslése figyelembe veszi az alvállalkozásba adott erőforrás-hozzárendeléseket, és az alvállalkozókhoz rendelt árlisták felhasználásával költségel. 
- [Az ütemezési tábla konfigurálása a szerződéses dolgozói és az alvállalkozói kapacitásának megjelenítéséhez](../subcontracting/configure-sb-subcon.md): A Project Operations ütemezési táblája mostantól konfigurálható a szerződés dolgozó típusú, lefoglalható erőforrások és alvállalkozói kapacitások keresésére és javasolására az alkalmazottakkal együtt. Ez a konfiguráció akkor alkalmazható, ha erőforrásokat keres a munkaerő környezetében egy adott projektkövetelményhez, vagy amikor egy projektkövetelmény környezetén kívül keres.
- [Projekt munkaerőkezelés szerződéses dolgozókkal és alvállalkozói kapacitással](../subcontracting/staffing-cw.md): A szerződéses dolgozók immár foglalhatók projektekhez az ütemezésitábla-élmények kihasználása érdekében.
- [Az alvállalkozásba adott összetevők projektjeinél idő, kiadások és anyaghasználat rögzítése](../subcontracting/recording-subcon-actuals.md): A szerződéses dolgozók rögzíthetnek időt és kiadásokat, valamint a projektcsoporttagok rögzíthetik a projekthez alvállakozói szerződés keretében vásárolt anyaghasználatot. Ennek eredményeképpen pontos költségeket lesznek rögzítve a megvásárolt kapacitást vagy anyagokat használó projekteknél.
- [Alvállalkozói szerződés állapotátváltásai](../subcontracting/subcon-states.md): Az alvállalkozói szerződések megerősíthetők az alvállalkozóval való tárgyalás megerősítéséhez, lezárhatók a teljesítés befejezésének jelzéséhez, vagy törölhetők a szerződés megszüntetésének jelzésére a beszállítóval a szállítás előtt.

### <a name="task-planning"></a>Feladattervezés
- Javított hibaelhárítás a rendszergazdák számára. Ha egy felhasználó nem tud megnyitni egy projektet, a rendszergazda a projektütemezési naplókban áttekintheti nem licenchez kapcsolódó hibákat a Project for the Web felől a [Projektütemezési naplókban](../../project-management/schedule-api-logs.md).
- [Feladat-ellenőrzőlisták használata a Microsoft Project for the web alkalmazásban](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). A Microsoft Project for the web alkalmazásban feladatlistát is felvehet az egyes cikkek nyomon követésére.

## <a name="quality-updates"></a>Minőségi frissítések

| **Funkcióterület** | **Hivatkozási szám** | **Minőségi frissítés** |
| --- | --- | --- |
| Tervezés és nyomon követés | 2392596. | Az API-k ütemezése mostantól lehetővé teszi a **Hátralévő erőfeszítés**, a **Teljesített erőfeszítés** és a **Teljesítés százaléka** mezők frissítését. |
| Tervezés és nyomon követés | 2478497. | Az Ütemezési API-k **Tevékenységszám** és **Feladatazonosító** mezői üresek lehet a bevitelkor, mert a rendszer automatikus számozással kitölti őket.|
| Idő és költség | 2468135. | A jóváhagyási kísérletek száma ötről háromra csökkent. |
| Idő és költség | 2468188. | Kijavították azt a problémát, hogy amikor a naplószöveg meghaladja a **jegyzet** entitás **notetext** attribútumának maximális hosszát. |
