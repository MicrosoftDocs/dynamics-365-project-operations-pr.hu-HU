---
title: Újdonságok 2021. december - Project Operations lite deployment
description: Ez a témakör a Project Operations lite üzembe helyezésének 2021. decemberi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1ff0a14bf6cb445913bcba11f83234826014857
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585381"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Újdonságok 2021. december - Project Operations lite deployment

_Érvényesség: Lite telepítés – ajánlattól proforma számlázásig_

Ez a témakör a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Projektműveletek környezeti Dataverse verzióban 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

### <a name="subcontract-management"></a>Alvállalkozói tevékenység kezelése 

- [A projektcsapat tagjainak](../subcontracting/subcontracting-project-team-members.md) alvállalkozói: A projektmenedzser megnevezett vagy általános csapattagokat hozhat létre alvállalkozói szerződésekkel és alvállalkozói sorokkal, hogy befolyásolja a személyzetet és a becslést.
- [Alvállalkozói lehetőségek a projektcsapat tagjai](../subcontracting/subcon-options.md) számára: Amikor megnevezett vagy általános projektcsapat-tagok számára személyzeti döntéseket hoz, a projektmenedzser áttekintheti a meglévő alvállalkozókat, vagy új alvállalkozói szerződéseket hozhat létre egy vagy több projektcsapat-tag számára. 
- [Alvállalkozói erőforrás-hozzárendelések](../subcontracting/costing-subcon-ra.md) költségbecslése: A projektköltség-becslés figyelembe veszi az alvállalkozói erőforrás-hozzárendeléseket, és az alvállalkozókhoz társított beszerzési árlisták használatával kerül költséget. 
- [Az Ütemezési tábla konfigurálása a szerződéses dolgozók és az alvállalkozói kapacitás](../subcontracting/configure-sb-subcon.md) megjelenítésére: A Projektműveletek ütemezési táblája mostantól konfigurálható úgy, hogy az alkalmazottakkal együtt megkeresse és javasolja a szerződéses dolgozó típusú lefoglalható erőforrásokat és alvállalkozói kapacitást. Ez a konfiguráció akkor alkalmazható, ha erőforrásokat keres egy adott projektkövetelmény személyzeti környezetében, vagy ha egy projektkövetelmény kontextusán kívül keres.
- [A szerződéses munkavállalókkal és alvállalkozói kapacitással rendelkező projekt személyzete](../subcontracting/staffing-cw.md): A szerződéses munkavállalók most már az ütemterv-tábla tapasztalatait kihasználó projektekre foglalhatók.
- [Az alvállalkozói](../subcontracting/recording-subcon-actuals.md) összetevők projektjeinek idő-, költség- és anyagfelhasználásának rögzítése: A szerződéses dolgozók rögzíthetik az időt és a költségeket, és a projektcsapat tagjai a projekt alvállalkozói szerződéssel vásárolt anyagok felhasználását is rögzíthetik. Ez azt eredményezi, hogy pontos költségeket rögzítenek a megvásárolt kapacitást vagy anyagokat használó projekteknél.
- [Állami átmenetek egy alvállalkozói szerződésen](../subcontracting/subcon-states.md): Az alvállalkozók megerősíthetők a szállítóval folytatott tárgyalások befejezéséhez, lezárhatók a szállítás befejezésének jelzésére, vagy visszavonhatók, hogy jelezzék a szerződés megszüntetését az eladóval a szállítás befejezése előtt.

### <a name="task-planning"></a>Tevékenységtervezés
- Továbbfejlesztett hibaelhárítás rendszergazdák számára. Ha egy felhasználó nem tud megnyitni egy projektet, a rendszergazda áttekintheti a Project for the Web projektprogramozási naplóiban [a](../../project-management/schedule-api-logs.md) Project for the Web szolgáltatásból származó, nem licenccel kapcsolatos hibákat.
- [Használjon feladatellenőrző listákat a Microsoft Project for the Web programban](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). A Microsoft Project for the Web programban ellenőrzőlistát adhat egy tevékenységhez, hogy nyomon kövesse az egyes elemeket.

## <a name="quality-updates"></a>Minőségi frissítések

| **Funkcióterület** | **Hivatkozási szám** | **Minőségi frissítés** |
| --- | --- | --- |
| Tervezés és nyomon követés | 2392596 | Az ütemezési API-k mostantól lehetővé teszik a Hátralévő **erőfeszítés,** a Befejezett **erőfeszítés és** a **Készültségi** % mezők frissítését. |
| Tervezés és nyomon követés | 2478497 | Az API-k **ütemezése A tevékenységszám** és **a tevékenységazonosító** mezők üresek lehetnek a bemeneten, mert a rendszer automatikus számozással tölti fel őket.|
| Idő és költség | 2468135 | A jóváhagyási újrapróbálkozások száma ötről háromra csökken. |
| Idő és költség | 2468188 | Kijavítottuk azt a problémát, hogy a naplószöveg túllépte a jegyzettömb **entitás jegyzetszöveg-attribútumában** **a** maximális hosszúságot. |
