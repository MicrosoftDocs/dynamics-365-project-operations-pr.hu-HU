---
title: Újdonságok 2021. december - Project Operations lite üzembe helyezése
description: Ez a cikk a Project Operations lite telepítésének 2021. decemberi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást.
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
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Újdonságok 2021. december - Project Operations lite üzembe helyezése

_Érvényesség: Lite telepítés – ajánlattól proforma számlázásig_

Ez a cikk a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Project Operations egy Dataverse környezeti verzióban 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

### <a name="subcontract-management"></a>Alvállalkozói szerződések kezelése 

- [Alvállalkozói projektcsapat tagjainak](../subcontracting/subcontracting-project-team-members.md): A projektmenedzser létrehozhat megnevezett vagy általános csapattagokat alvállalkozói és alvállalkozói vonalakkal a személyzet és a becslés befolyásolása érdekében.
- [Alvállalkozási lehetőségek a projektcsapat tagjainak](../subcontracting/subcon-options.md): Amikor a megnevezett vagy általános projektcsapat tagjai számára személyzeti döntéseket hoz, a projektmenedzser áttekintheti a meglévő alvállalkozói szerződéseket, vagy új alvállalkozói szerződéseket hozhat létre egy vagy több projektcsapat-tag számára. 
- [Alvállalkozói erőforrás-hozzárendelések](../subcontracting/costing-subcon-ra.md) költségbecslése: A projekt költségbecslése figyelembe veszi az alvállalkozói erőforrás-hozzárendeléseket, és az alvállalkozókhoz társított beszerzési árlisták használatával kerül nekik. 
- [Az ütemezési tábla konfigurálása a szerződéses dolgozók és az alvállalkozói kapacitás](../subcontracting/configure-sb-subcon.md) megjelenítésére: A Project Operations ütemezési táblája mostantól konfigurálható úgy, hogy az alkalmazottakkal együtt megkeresse és javasolja a szerződéses dolgozói típusát a foglalható erőforrásoknak és az alvállalkozói kapacitásnak. Ez a konfiguráció akkor alkalmazható, ha erőforrásokat keres egy adott projektkövetelmény személyzetének kontextusában, vagy ha a projektkövetelmény kontextusán kívül keres.
- [Projekt személyzete szerződéses alkalmazottakkal és alvállalkozói kapacitással](../subcontracting/staffing-cw.md): A szerződéses dolgozók mostantól lefoglalhatók olyan projektekre, amelyek az ütemezési igazgatóság tapasztalatait használják fel.
- [Idő, költségek és anyagfelhasználás rögzítése az alvállalkozói összetevők](../subcontracting/recording-subcon-actuals.md) projektjein: A szerződéses dolgozók rögzíthetik az időt és a költségeket, a projektcsapat tagjai pedig rögzíthetik a projekt alvállalkozói szerződésével vásárolt anyagok felhasználását is. Ez azt eredményezi, hogy a megvásárolt kapacitást vagy anyagokat felhasználó projektek pontos költségeit rögzítik.
- [Alvállalkozói szerződésre](../subcontracting/subcon-states.md) vonatkozó állapotátlépések: Az alvállalkozói szerződések megerősíthetők a szállítóval folytatott tárgyalások befejezéséhez, lezárhatók a szállítás befejezésének jelzésére, vagy lemondhatók, hogy jelezzék a szállítóval kötött szerződés megszűnését a szállítás befejezése előtt.

### <a name="task-planning"></a>Feladattervezés
- Továbbfejlesztett hibaelhárítás rendszergazdák számára. Ha egy felhasználó nem tud megnyitni egy projektet, a rendszergazda áttekintheti a Project for the webből létrehozott, licenccel nem kapcsolatos hibákat a Project ütemezési [naplóiban](../../project-management/schedule-api-logs.md).
- [Feladat-ellenőrzőlisták használata a](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) Webes Microsoft Projectben. A Webes Microsoft Projectben ellenőrzőlistát adhat hozzá egy feladathoz, hogy nyomon kövesse az adott elemeket.

## <a name="quality-updates"></a>Minőségi frissítések

| **Funkcióterület** | **Hivatkozási szám** | **Minőségi frissítés** |
| --- | --- | --- |
| Tervezés és nyomon követés | 2392596 | Az ütemezési API-k mostantól lehetővé teszik a Hátralévő **erőfeszítés,** a Befejezett **erőfeszítés és** a **Készültségi %** mezők frissítését. |
| Tervezés és nyomon követés | 2478497 | Az ÜTEMEZÉSI API-k **tevékenységszáma** és **a tevékenységazonosító** mezők üresek lehetnek a bevitelkor, mert a rendszer automatikus számozással tölti fel őket.|
| Idő és költség | 2468135 | A jóváhagyási újrapróbálkozások száma ötről háromra csökken. |
| Idő és költség | 2468188 | Kijavítottuk azt a hibát, amely miatt a naplószöveg túllépte a jegyzetszöveg attribútumában található maximális hosszúságot a **kommentár** entitás notetext **attribútumában**. |
