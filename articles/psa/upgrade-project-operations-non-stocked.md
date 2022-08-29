---
title: Frissítés a Project Service Automationről a Project Operationsre
description: Ez a cikk áttekintést nyújt a frissítés folyamatáról Microsoft Dynamics 365 Project Service Automation Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: c7958c1474820361269f19ea8c9279b96f087d7a
ms.sourcegitcommit: 8edd24201cded2672cec16cd5dc84c6a3516b6c2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2022
ms.locfileid: "9230254"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Frissítés a Project Service Automationről a Project Operationsre

Örömmel jelentjük be a három fázis közül az elsőt, amikor a frissítés a következőre Microsoft Dynamics 365 Project Service Automation frissül:Dynamics 365 Project Operations. Ez a cikk áttekintést nyújt azoknak az ügyfeleknek, akik elindulnak ezen az izgalmas úton. A jövőbeli cikkek fejlesztői szempontokat és a funkciók fejlesztésével kapcsolatos részleteket tartalmaznak. Nemcsak útmutatást nyújtanak a Project Operationsre való frissítésre való felkészüléshez, hanem azt is elmagyarázzák, hogy mire számíthat a frissítés után.

A frissítési teljesítési program három szakaszra oszlik.

| Frissítés kézbesítése | 1. szakasz (2022. január) | 2. fázis (2022. áprilisi hullám) | 3. fázis  |
|------------------|------------------------|---------------------------|---------------------------|
| Nincs függőség a projektek munkalebontási struktúrájától (WBS) | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| A WBS a projektműveletek jelenleg támogatott határain belül | | :heavy_check_mark: | :heavy_check_mark: |
| A munkalebontási struktúra a Project Operations jelenleg támogatott korlátain kívül esik, beleértve a Project asztali ügyfél támogatását is | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Frissítési folyamat funkciói 

A frissítési folyamat részeként frissítési naplókat adtunk hozzá az oldaltérképhez, hogy a rendszergazdák könnyebben diagnosztizálhassák a hibákat. Az új interfész mellett új érvényesítési szabályok is hozzáadódnak az adatok integritásának biztosításához a frissítés után. A következő ellenőrzések lesznek hozzáadva a frissítési folyamathoz.

| Érvényesítés | 1. szakasz (2022. január) | 2. fázis (2022. áprilisi hullám) | 3. fázis  |
|-------------|------------------------|---------------------------|---------------------------|
| A munkalebontási struktúrát a rendszer ellenőrzi a gyakori adatintegritási szabálysértések ellen (például olyan erőforrás-hozzárendelések, amelyek ugyanahhoz a szülőfeladathoz vannak társítva, de különböző szülőprojektekkel rendelkeznek). | | :heavy_check_mark: | :heavy_check_mark: |
| A munkalebontási struktúrát a rendszer a Project for the [Web ismert korlátai alapján érvényesíti](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| A munkalebontási struktúrát a rendszer a Project asztali ügyfélalkalmazás ismert korlátaival összeveti. | |  | :heavy_check_mark: |
| A lefoglalható erőforrásokat és a projektnaptárakat a rendszer a gyakori, nem kompatibilis naptárszabály-kivételek alapján értékeli ki. | | :heavy_check_mark: | :heavy_check_mark: |

A 2. fázisban a Project Operationsre frissítő ügyfelek meglévő projektjeiket csak olvasható felhasználói élményre frissítik a projekttervezéshez. Ebben a csak olvasható élményben a teljes munkalebontási struktúrát látni fogja a követőrácson. A munkalebontási struktúrához a projektmenedzserek kiválaszthatják a Konvertálás **lehetőséget** a projektek **főoldalán**. A háttérfolyamat ezután frissíti a projektet, hogy az támogassa a Project for the Web új projektütemezési élményét. Ez a fázis azoknak az ügyfeleknek megfelelő, akiknek olyan projektjeik vannak, amelyek megfelelnek a [Webes Projekt ismert korlátainak](/project-for-the-web/project-for-the-web-limits-and-boundaries).

A 3. fázisban a rendszer hozzáadja a Project asztali ügyfél támogatását, amely azoknak az ügyfeleknek a javára válik, akik továbbra is szerkeszteni szeretnék a projektjeiket az alkalmazásból. Ha azonban a meglévő projekteket átalakítja az új Webes Projekt felhasználói felületre, a bővítményhez való hozzáférés minden konvertált projektnél le lesz tiltva.

## <a name="prerequisites"></a>Előfeltételek

Ahhoz, hogy jogosult legyen az 1. fázisú frissítésre, az ügyfélnek meg kell felelnie a következő feltételeknek:

- A célkörnyezet nem tartalmazhat rekordokat a **msdyn_projecttask** entitásban.
- Érvényes Project Operations-licenceket kell hozzárendelni az ügyfél összes aktív felhasználójához. 
- Az ügyfélnek ellenőriznie kell a frissítési folyamatot legalább egy olyan nem éles környezetben, amely az éles adatokhoz igazított reprezentatív adatkészlettel rendelkezik.
- A célkörnyezetet frissíteni kell a Project Service Automation update release 41 (3.10.62.162) vagy újabb verziójára.

A 2. és a 3. fázis előfeltételei az általános rendelkezésre állási dátumok megközelítésével frissülnek.

## <a name="licensing"></a>Licencelés

Ha aktív licenccel rendelkezik a Project Service Automationhez, telepítheti és használhatja a Project Operationst, amely magában foglalja a Project Service Automation összes képességét és még sok mást. Ily módon tesztelheti a Project Operations képességeit, miközben továbbra is használja a Project Service Automationt éles környezetben. A Project Service Automation-licencek lejárta után át kell térnie a Project Operationsre. Az áttérés megtervezésekor figyelembe kell vennie azt a tényt, hogy a Project Operations licenc nem tartalmaz Project Service Automation-licencet.

## <a name="testing-and-refactoring-customizations"></a>Testreszabások tesztelése és újrabontása

Kiindulási pontként importálja az összes testreszabást egy tiszta Project Operations (Lite) környezetbe, hogy megbizonyosodjon arról, hogy az importálás sikeres, és hogy az üzleti műveletek a várt módon viselkednek- e.

Íme néhány dolog, amire figyelni kell:

- Az importálás sikertelen lehet a hiányzó függőségek miatt. Más szóval a testreszabások referenciamezőkre vagy más, a Project Operationsben eltávolított összetevőkre vonatkoznak. Ebben az esetben távolítsa el ezeket a függőségeket a fejlesztési környezetből.
- Ha a nem felügyelt és felügyelt megoldások nem testreszabott összetevőket tartalmaznak, távolítsa el ezeket az összetevőket a megoldásból. Ha például testreszabja a **Projekt** entitást, csak az entitásfejlécet adja hozzá a megoldáshoz. Ne adja hozzá az összes mezőt. Ha korábban már hozzáadta az összes alösszetevőt, előfordulhat, hogy manuálisan kell létrehoznia egy új megoldást, és hozzá kell adnia a megfelelő összetevőket.
- Előfordulhat, hogy az űrlapok és nézetek nem a várt módon jelennek meg. Bizonyos körülmények között, ha testreszabta a beépített űrlapok vagy nézetek bármelyikét, a testreszabások megakadályozhatják, hogy a Project Operations új frissítései életbe lépjenek. A problémák azonosításához javasoljuk, hogy végezze el a Project Operations tiszta telepítésének és a Testreszabásokat tartalmazó Projektműveletek telepítésének egymás melletti áttekintését. Hasonlítsa össze a vállalkozásban leggyakrabban használt űrlapokat, és győződjön meg arról, hogy az űrlap verziójának továbbra is van értelme, és nem hiányzik valami az űrlap tiszta verziójából. Végezze el ugyanazt a fajta egymás melletti ellenőrzést a testreszabott nézeteknél.
- Előfordulhat, hogy az üzleti logika futásidőben meghiúsul. Mivel a beépülő modulok mezőire mutató hivatkozások nem lesznek érvényesítve az importáláskor, az üzleti logika meghiúsulhat a már nem létező mezőkre mutató hivatkozások miatt, és a következő példához hasonló hibaüzenet jelenhet meg: "A projektentitás nem tartalmaz attribútumot a Name = 'msdyn_plannedhours' és a NameMapping = 'Logical' attribútummal." Ebben az esetben módosítsa a testreszabásokat úgy, hogy azok az új mezőket használják. Ha automatikusan generált proxyosztályokat és erős típushivatkozásokat használ a beépülő modul logikájában, fontolja meg a proxyk újragenerálását egy tiszta telepítésből. Ily módon könnyen azonosíthatja az összes olyan helyet, ahol a beépülő modulok elavult mezőktől függenek.

Miután frissítette a testreszabásokat a Project Operations tiszta importálásához, folytassa a következő lépésekkel.

## <a name="end-to-end-testing-in-development-environments"></a>Teljes körű tesztelés fejlesztési környezetekben

### <a name="initiate-upgrade"></a>Frissítés kezdeményezése 

1. Power Platform A felügyeleti központban keresse meg és válassza ki a környezetet. Ezután az alkalmazásokban keresse meg és válassza ki **Dynamics 365 Project Operations** a.
2. Válassza a Telepítés **lehetőséget** a frissítés elindításához. A Power Platform felügyeleti központ ezt a telepítést új telepítésként fogja bemutatni. A rendszer azonban észleli a Project Service Automation egy korábbi verziójának jelenlétét, és frissíti a meglévő telepítést.

    A frissítés befejezése után a környezetnek meg kell mutatnia, hogy a Project Operations telepítve van, és hogy a Project Service Automation nincs telepítve.

    > [!NOTE]
    > A környezetben lévő adatok mennyiségétől függően a frissítés több órát is igénybe vehet. A frissítést kezelő alapcsapatnak ennek megfelelően kell megterveznie, és munkaidőn kívül is futtatnia kell a frissítést. Bizonyos esetekben, ha az adatmennyiség nagy, a frissítést a hétvégén kell futtatni. Az ütemezésre vonatkozó döntésnek az alacsonyabb környezetekben végzett tesztelési eredményeken kell alapulnia.

3. Szükség szerint frissítse az egyéni megoldásokat. Ezen a ponton telepítse a testreszabásokon végrehajtott módosításokat a [cikk Testreszabások](#testing-and-refactoring-customizations) tesztelése és újrabontása szakaszában.
4. Lépjen a **Gépház** \> **megoldások**, és válassza a **Project Operations elavult összetevők** megoldásának eltávolítását.

    Ez a megoldás egy ideiglenes megoldás, amely a frissítés során meglévő adatmodellt és összetevőket tartalmazza. A megoldás eltávolításával eltávolítja az összes már nem használt mezőt és összetevőt. Ily módon egyszerűsítheti a felületet, és megkönnyítheti az integrációt és a kiterjesztést.
    
### <a name="validate-common-scenarios"></a>Gyakori forgatókönyvek érvényesítése

Az adott testreszabások ellenőrzésekor javasoljuk, hogy tekintse át az alkalmazásokban támogatott üzleti folyamatokat is. Ezek az üzleti folyamatok magukban foglalják többek között az értékesítési entitások, például árajánlatok és szerződések létrehozását, valamint olyan projektek létrehozását, amelyek magukban foglalják a WBS-eket és a tényleges adatok jóváhagyását.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Jelentős változások a Project Service Automation és a Project Operations között

Ez a szakasz összefoglalja a Project Service Automation és a Project Operations között várható főbb változásokat.

### <a name="project-planning"></a>Projekt tervezése

A Project Operations projekttervezési képességei már nem támaszkodnak kombinált ügyféloldali logikára és kiszolgálóoldali logikára. Ehelyett a Project Operations a Project for the Webet használja ütemezési motorként. Az ütemezési képességek ezen módosítása számos új funkciót tesz lehetővé, például a Tábla és a Gantt nézeteket, az erőforrás-vezérelt tervezést, [a tevékenység-ellenőrzőlista elemeit](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) és a projektütemezési módokat. Az új ütemezési képességeket az új [alkalmazásprogramozási felületek (API-k)](../project-management/schedule-api-preview.md) gazdag készlete is támogatja. Ezeknek az API-knak az a célja, hogy segítsenek biztosítani, hogy a WBS-ben az entitások létrehozására, frissítésére vagy törlésére szolgáló programozott művelet ne rontsa meg az ütemezés számított mezőit.

## <a name="billing-and-pricing"></a>Számlázás és árképzés

A Project Operationsbe történő folyamatos beruházások részeként számos új képesség érhető el a számlázás és az árképzés területén. Íme néhány példa:

- [Anyaghasználat rögzítése projekteken és projektfeladatokon](../material/material-usage-log.md)
- [Alvállalkozói szerződések kezelése](../pro/subcontracting/managing-subcontracts-overview.md)
- [Foglalón alapuló szerződések beállítása](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [A szerződés állapota és érvényesítése nem haladhatja meg a státuszt és az érvényesítést](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Feladatalapú számlázás

## <a name="frequently-asked-questions"></a>Gyakori kérdések

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Mely központi telepítési típusok támogatottak jelenleg a frissítéshez?

| Source                                                 | Target                                                    | Állam                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations Lite telepítése                        | Támogatott               |
| Dynamics 365 Finance Projektmenedzsment és számvitel | Project Operations Lite telepítése                        | Jelenleg nem támogatott |
| Pénzügyi projektmenedzsment és számvitel              | Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez     | Jelenleg nem támogatott |
| Project Service Automation 3.x                         | Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez     | Jelenleg nem támogatott |
| Project for the Web (dedikált környezet)            | Project Operations Lite telepítése                        | Jelenleg nem támogatott |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Hogyan telepíthetem a Project Operationst a frissítési eszközök elérhetővé tétele előtt?

A Project Operations két lehetőség közül választhat, mielőtt a frissítési eszközök elérhetővé válnának:

- Új környezet kiépítése.
- A Project Operationst külön helyezheti üzembe minden olyan értékesítési szervezeten, ahol a Project Service Automation nincs jelen.

> [!NOTE]
> Ha a Project Service Automation telepítve van egy szervezeten, de nem használták, akkor eltávolítható. Miután teljesen eltávolította a Project Service Automation alkalmazást, a Project Operations ugyanabba a szervezetbe telepíthető.
