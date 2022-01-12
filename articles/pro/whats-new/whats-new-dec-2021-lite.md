---
title: Újdonságok 2021 decemberében - Project Operations lite üzembe helyezése
description: Ez a témakör tájékoztatást nyújt a Project Operations lite telepítésének 2021. decemberi kiadásában elérhető minőségi frissítésekről.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942980"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Újdonságok 2021 decemberében - Project Operations lite üzembe helyezése

_Érvényesség: Lite telepítés – ajánlattól proforma számlázásig_

Ez a témakör a Microsoft következő összetevőire és verzióira Dynamics 365 Project Operations vonatkozik:

- Projektműveletek Dataverse környezeti verzióban 4.27.0.195, 4.27.0.242


## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

### <a name="subcontract-management"></a>Alvállalkozói menedzsment 

- [A projektcsapat tagjainak alvállalkozásba](../subcontracting/subcontracting-project-team-members.md) adása : A projektmenedzser alvállalkozókkal és alvállalkozói vonalakkal rendelkező megnevezett vagy általános csapattagokat hozhat létre a személyzet és a becslés befolyásolására.
- [Alvállalkozói lehetőségek a projektcsapat tagjai számára](../subcontracting/subcon-options.md) : A megnevezett vagy általános projektcsapattagok személyzetének választásakor a projektmenedzser áttekintheti a meglévő alvállalkozókat, vagy új alvállalkozókat hozhat létre egy vagy több projektcsapat-tag számára. 
- [Alvállalkozói erőforrás-hozzárendelések költségbecslése](../subcontracting/costing-subcon-ra.md) : A projektköltség-becslés figyelembe veszi az alvállalkozói erőforrás-hozzárendeléseket, és az alvállalkozókhoz kapcsolódó beszerzési árlisták használatával kerül ezekbe. 
- [Az Ütemezési tábla konfigurálása a szerződéses dolgozók és az alvállalkozói kapacitás megjelenítéséhez](../subcontracting/configure-sb-subcon.md) : A Project Operations ütemezési táblája mostantól konfigurálható a lefoglalható erőforrások és az alvállalkozói kapacitás szerződéses dolgozói típusának keresésére és javaslatára az alkalmazottakkal együtt. Ez a konfiguráció akkor alkalmazható, ha erőforrásokat keres egy adott projektkövetelmény személyzetének keretében, vagy ha egy projektkövetelmény környezetén kívül keres.
- [Szerződéses munkavállalókkal és alvállalkozói kapacitással rendelkező projekt](../subcontracting/staffing-cw.md) személyzete: A szerződéses munkavállalók mostantól lefoglalhatók olyan projektekre, amelyek kihasználják az ütemtervi fórum tapasztalatait.
- [Az alvállalkozói összetevők projektjeinek ideje, költségei és](../subcontracting/recording-subcon-actuals.md) anyaghasználata: A szerződéses alkalmazottak rögzíthetik az időt és a költségeket, és a projektcsapat tagjai rögzíthetik a projekt alvállalkozói felhasználásával vásárolt anyagok felhasználását is. Ez pontos költségek rögzítését eredményezi a megvásárolt kapacitást vagy anyagokat használó projektek esetében.
- [Állami átmenetek egy](../subcontracting/subcon-states.md) alvállalkozón: Az alvállalkozók megerősíthetők a szállítóval folytatott tárgyalások befejezéséhez, lezárhatók a szállítás befejezésének jelzésére, vagy törölhetők, hogy jelezzék a szállítóval kötött szerződés megszűnését a szállítás befejezése előtt.

### <a name="task-planning"></a>Feladattervezés
- Továbbfejlesztett hibaelhárítás a rendszergazdák számára. Ha egy felhasználó nem tud megnyitni egy projektet, a rendszergazda áttekintheti a Project for the webből generált, nem licenccel kapcsolatos hibákat a [Project ütemezési naplókban.](../../project-management/schedule-api-logs.md)
- [Feladat-ellenőrző listák használata a Microsoft Project for the web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) programban. A Microsoft Project for the web programban ellenőrzőlistát adhat hozzá egy tevékenységhez az egyes elemek nyomon követéséhez.

## <a name="quality-updates"></a>Minőségi frissítések

| **Funkcióterület** | **Hivatkozási szám** | **Minőségi frissítés** |
| --- | --- | --- |
| Tervezés és nyomon követés | 2392596 | Az ütemezési API-k mostantól engedélyezik a **Hátralévő erőfeszítés**, Az **erőfeszítés befejeződött és a Teljes** % mezők **frissítését**. |
| Tervezés és nyomon követés | 2478497 | Api-k ütemezése **A tevékenységszám** és a **tevékenységazonosító mezők** üresek lehetnek a bemeneten, mert a rendszer automatizált számozással tölti fel őket.|
| Idő és költség | 2468135 | A jóváhagyási újrapróbálkozások száma ötről háromra csökken. |
| Idő és költség | 2468188 | Kijavítottuk a problémát, mert a naplószöveg túllépte a **jegyzetszöveg**-entitás jegyzetszöveg-attribútumának maximális **hosszát**. |
