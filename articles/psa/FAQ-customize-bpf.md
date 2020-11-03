---
title: Hogyan szabható testre a Projektfázisok üzleti folyamat?
description: A Projektfázisok üzleti folyamat testreszabásánek áttekintése.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2dccc33088cd9e49e7ffe609f9d9754ef33a5dba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078278"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Hogyan szabható testre a Projektfázisok üzleti folyamat?
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Van egy ismert korlátozása a Project Service alkalmazás korábbi verzióiban, amely szerint a Projektfázisok üzleti folyamat fázisneveinek pontosan egyezniük a várt angol nevekkel ( **Quote** , **Plan** , **Close** ). Ellenkező esetben az üzleti logika, amely a fázisok angol nevén alapul, nem működik megfelelően. Ezért nem láthatók a megszokott, a projektűrlapon elérhető műveletek, például a **Folyamatváltás** vagy a **Folyamat szerkesztése** , és az üzleti folyamat testreszabás nem javasolt. 

Ezt a korlátozást a 2.4.5.48 és újabb verziókat már feloldottuk. Ebben a cikkben javasolt megoldások találhatók, ha testre kell szabnia az alapértelmezett üzleti folyamatot a korábbi verziókban.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Az üzleti logika az angol fázisnevekkel való pontos egyezést követel meg

A Projektfázisok üzleti folyamatban üzleti logikát tartalmaz, amely az alkalmazásban az alábbi viselkedéseket váltja ki:
- Amikor a projekt társítva van egy ajánlattal, a kód a **Quote** fázisra állítja be az üzleti folyamatot.
- Amikor a projekt társítva van egy szerződéssel, a kód a **Plan** fázisra állítja be az üzleti folyamatot.
- Ha az üzleti folyamat eljut a **Close** fázisig, a projektrekordot inktiválja. A projekt inaktiválásakor a projektűrlap és a munkalebontási struktúra (WBS) csak olvasható beállítású lesz, megtörténik az elnevezett erőforrások foglalásainak elengedése, és bármilyen kapcsolódó árlisták inaktiválva lesznek.

Az üzleti logika az angol nevekre támaszkodik a projektfázisok esetében. Az angol fázisnevektől való függőség a fő ok, amiért a Projektfázisok üzleti folyamat testreszabása nem javasolt, valamint ezért nem láthatók a gyakran használt üzletifolyamat-műveleteket, mint a **Folyamatváltás** vagy a **Folyamat szerkesztése** a projektentitáson.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Mi történik, ha a fázisnevek nem egyeznek meg az angol nevekkel?

A Project Service alkalmazás 1.x verziójában a 8.2 platformon, ha a fázisok neve az üzleti folyamatban nem egyezik meg pontosan az angol fázisnevekkel, a rendszer átugorja azt az üzleti logikát, amely a megfelelő fázisra állítja az ajánlatokat vagy a szerződéseket, vagy amely bezárja a projektet. Hibaüzenet nem jelenik meg. Ezért úgy tűnik, hogy testreszabható a Projektfázisok üzleti folyamat. Azonban nem fognak működni az automatikus folyamatok az ajánlatok, a szerződések és a projektzárás esetében.

A Project Service alkalmazás 2.4.4.30 vagy korábbi verzióban a 9.0 platformon, jelentős architekturális változás történt az üzleti folyamatokban, amely az üzleti folyamat üzleti logikájának újraírását tette szükségessé. Ennek következtében, ha a fázisnevek nem egyeznek meg a várt angol nevekkel, hibaüzenetet kap. 

Ezért ha testre szeretné szabni a projektentitáshoz a Projektfázisok üzleti folyamatot, csak hozzáadhat teljesen új fázisokat az alapértelmezett üzleti folyamathoz a projektentitáshoz, miközben változatlanul tartja meg az **Ajánlat** , **Terv** és **Bezárás** fázisokat. Ez a korlátozás biztosítja, hogy nem kap hibákat az üzleti logikától, amely az üzleti folyamatban az angol fázisnevekre számít.

A 2.4.5.48 és újabb verziókban az üzleti logika, amelyről ebben a cikkben szó van, kikerült a projektentitás alapértelmezett üzleti folyamatából. A frissítés arra, vagy az újabb verziókra, lehetővé teszi majd az alapértelmezett üzleti folyamat lecserélését egy sajátra. 

## <a name="workarounds-for-earlier-versions"></a>Megkerülő megoldások a korábbi verziók esetén

Ha a frissítés nem lehetséges, testreszabhatja a Projektfázisok üzleti folyamatot az alábbi két módon a projektentitáshoz:

1. Adjon hozzá további fázisokat az alapértelmezett konfigurációhoz, miközben megtartja az angol fázisneveket az **Ajánlat** , a **Terv** és a **Bezárás** esetében.


![Fázisok hozzáadása az alapértelmezett konfigurációhoz képernyőkép](media/FAQ-Customize-BPF-1.png)
 
2. Hozzon létre saját üzleti folyamatot, és legyen ez az elsődleges üzleti folyamat a projektentitáshoz, ami lehetővé teszi bármilyen kívánt fázisnév használatát. Azonban ha ugyanazokat a szabványos projektfázisokat is használni kívánja – **Ajánlat** , **Terv** és **Bezárás** – néhány testreszabást kell végrehajtani. A bonyolultabb logika a projektzárás, amely továbbra is kiváltható csak a projektbejegyzés inaktiválásával.

![BPF testreszabása](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>További szempontok a Project Service alkalmazás 2.4.4.30 vagy korábbi verzió esetében a 9.0 platformon

A Project Service 2.4.4.30 vagy korábbi verziói esetében a 9.0 platformon, az egyéni üzleti folyamatban a **Fázis neve** mező annál a projektentitásnál, amely a **Projekt fázis szerint** diagramon és a projektlistanézetekben van használatban nem frissül, mert hozzá van kapcsolva az alapértelmezett Projektfázisok üzleti folyamathoz. A probléma a következő lépések végrehajtásával oldható meg:

- Adja hozzá egy egyéni mezőt, amely az aktuális üzletifolyamat-fázist rögzíti, és amely frissül, ahogy a felhasználó végighalad az egyéni üzleti folyamaton.

- Módosítsa a **Projekt fázis szerint** diagramot, hogy az egyéni mezőt használja az alapértelmezett beállítás helyett.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Lépések saját üzleti folyamat létrehozásához a projektentitáshoz

Saját üzleti folyamat létrehozásához a projektentitáshoz tegye a következőt:

1. Válassza a **Beállítások** > **Folyamatközpont** lehetőséget. A Projektfázisok üzleti folyamatot ne másolja le, mert ezzel a Project Service üzleti logikáját is lemásolná.

  ![Folyamat létrehozása](media/FAQ-Customize-BPF-3.png)

2. A Folyamattervező segítségével hozza létre a kívánt fázisneveket. Ha szeretné az alapértelmezett fázisok funkcióit az **Ajánlat** , **Terv** és **Bezárás** esetében, akkor kell létrehozni ezt az egyéni üzleti folyamat fázisnevei alapján.

   ![BPF testreszabásához használt Folyamattervező képernyőképe](media/FAQ-Customize-BPF-4.png) 

3. Kattintson a Folyamattervezőben a **Megrendelési folyamat** elemre, hogy az egyéni üzleti folyamatot tegye az elsődleges üzleti folyamattá a projektentitásba azzal, hogy áthelyezi a Projektfázisok üzleti folyamat fölé, a lista tetejére.


   [Megrendelési folyamat használata – képernyőkép](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>A következő lépések a Project Service alkalmazás 2.4.4.30 vagy korábbi verziójára vonatkoznak a 9.0 platformon

4. Adjon hozzá egy új egyéni mezőt a projektentitáshoz az fázisok rögzítésére az egyéni üzleti folyamatban. Üzleti logikát (beépülő modul vagy munkafolyamat) kell hozzáadnia, hogy a mező frissüljön az egyéni üzleti folyamat fázisának+ frissítésekor.

   ![Képernyőkép: projektentitás testreszabása](media/FAQ-Customize-BPF-6-720.png)

5. Módosítsa a **Projekt fázis szerint** diagramot, hogy az új egyéni mezőt használja a fázisokhoz.

   ![Képernyőkép: Projekt fázis szerint diagram használata](media/FAQ-Customize-BPF-7-720.png)

6. Módosítsa az összes érintett nézetet a projektentitáshoz, hogy tartalmazza az új egyéni mezőt a fázisokhoz.

   ![Képernyőkép: projektentitáson nézetek módosítása](media/FAQ-Customize-BPF-8-720.png)

