---
title: Frissítés a projectszolgáltatás-automatizálásról a projektműveletekre
description: Ez a témakör áttekintést nyújt a rendszerről való frissítés folyamatáról Microsoft Dynamics 365 Project Service Automation Dynamics 365 Project Operations.
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
ms.openlocfilehash: 3f31173197a3055cdc51567261dd91925fc9f430
ms.sourcegitcommit: bec7382d1319d59645e8e79fdb20df58617c97c6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2022
ms.locfileid: "8626737"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Frissítés a projectszolgáltatás-automatizálásról a projektműveletekre

Izgatottan jelentjük be az első három fázist a frissítéshez Microsoft Dynamics 365 Project Service Automation Dynamics 365 Project Operations. Ez a témakör áttekintést nyújt azoknak az ügyfeleknek, akik elindulnak erre az izgalmas utazásra. A jövőbeli témák fejlesztői szempontokat és a funkciók fejlesztéseivel kapcsolatos részleteket tartalmaznak. Nem csak útmutatást nyújtanak a Project Operations-re való frissítésre való felkészüléshez, hanem azt is elmagyarázzák, hogy mire számíthat a frissítés után.

A frissítési kézbesítési program három fázisra oszlik.

| Frissítési kézbesítés | 1. fázis (2022. január) | 2. fázis (2022. áprilisi hullám) | 3. fázis  |
|------------------|------------------------|---------------------------|---------------------------|
| A projektek munkabontási struktúrájától (WBS) nem függ | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| A WBS a projektműveletek jelenleg támogatott határain belül | | :heavy_check_mark: | :heavy_check_mark: |
| A WBS a Project Operations jelenleg támogatott korlátain kívül esik, beleértve az asztali Project ügyfél támogatását is | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Frissítési folyamat szolgáltatásai 

A frissítési folyamat részeként frissítési naplókat adtunk a webhelytérképhez, hogy a rendszergazdák könnyebben diagnosztizálhassák a hibákat. Az új felület mellett új ellenőrzési szabályok is megjelennek az adatok integritásának biztosítása érdekében a frissítés után. A rendszer a következő érvényesítésekkel egészül ki a frissítési folyamatba.

| Érvényesítés | 1. fázis (2022. január) | 2. fázis (2022. áprilisi hullám) | 3. fázis  |
|-------------|------------------------|---------------------------|---------------------------|
| A WBS-t a rendszer ellenőrzi a rendszer az adatintegritás általános megsértései ellen (például olyan erőforrás-hozzárendelések ellen, amelyek ugyanahhoz a szülőfeladathoz vannak társítva, de különböző szülőprojektekkel rendelkeznek). | | :heavy_check_mark: | :heavy_check_mark: |
| A WBS a Project for the [Web ismert korlátaival szemben lesz érvényesítve](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| A WBS-t a Program az asztali Project ügyfél ismert korlátaival ellenőrzi. | |  | :heavy_check_mark: |
| A könyvelhető erőforrásokat és a projektnaptárakat a rendszer a gyakori inkompatibilis naptárszabály-kivételek alapján értékeli ki. | | :heavy_check_mark: | :heavy_check_mark: |

A 2. fázisban a Project Operations-re frissítést végző ügyfelek meglévő projektjeiket írásvédett élményre frissítik a projekttervezéshez. Ebben az írásvédett élményben a teljes WBS látható lesz a nyomkövető rácsban. A WBS szerkesztéséhez a projektmenedzserek a Fő **projektek** lapon választhatják a Konvertálás **lehetőséget**. A háttérfolyamat ezután frissíti a projektet, hogy támogassa a Project for the Web új projektütemezési élményét. Ez a fázis azoknak az ügyfeleknek megfelelő, akik olyan projektekkel rendelkeznek, amelyek megfelelnek a [Project for the Web ismert korlátainak](/project-for-the-web/project-for-the-web-limits-and-boundaries).

A 3. fázisban a Project asztali ügyfél támogatása is hozzáadódik azon ügyfelek javára, akik továbbra is szerkeszteni szeretnék projektjeiket az adott alkalmazásból. Ha azonban a meglévő projekteket a webes élmény új Projektjévé konvertálja, a bővítményhez való hozzáférés minden konvertált projektnél le lesz tiltva.

## <a name="prerequisites"></a>Előfeltételek

Ahhoz, hogy az ügyfél jogosult legyen az 1. fázisú frissítésre, a következő feltételeknek kell megfelelnie:

- A célkörnyezet nem tartalmazhat rekordokat a **msdyn_projecttask** entitásban.
- Az érvényes Project Operations licenceket az ügyfél összes aktív felhasználójához hozzá kell rendelni. 
- A vevőnek legalább egy olyan nem éles környezetben kell érvényesítenie a frissítési folyamatot, amely a termelési adatokhoz igazított reprezentatív adatkészlettel rendelkezik.
- A célkörnyezetet frissíteni kell a Project Service Automation Update Release 41 (3.10.62.162) vagy újabb verzióra.

A 2. és 3. fázis előfeltételei az általános rendelkezésre állási dátumok közeledtével frissülnek.

## <a name="licensing"></a>Licencelés

Ha aktív licencekkel rendelkezik a Project Service Automation szolgáltatásautomatizáláshoz, telepítheti és használhatja a Project Operations szolgáltatást, amely magában foglalja a Project Service Automation összes funkcióját és egyebeket. Ily módon tesztelheti a Project Operations képességeit, miközben továbbra is használja a Project Service Automation szolgáltatást az éles környezetben. A Project Service Automation licencek lejárta után át kell térnie a Project Operations szolgáltatásra. Az átmenet tervezésekor figyelembe kell vennie azt a tényt, hogy a Project Operations licenc nem tartalmaz Project Service Automation licencet.

## <a name="testing-and-refactoring-customizations"></a>Testreszabások tesztelése és újrafaktorozása

Kiindulási pontként importálja az összes testreszabást egy tiszta projektműveleti (lite) környezetbe, hogy megbizonyosodjon arról, hogy az importálás sikeres, és hogy az üzleti műveletek a várt módon viselkednek-e.

Íme néhány dolog, amire figyelni kell:

- Előfordulhat, hogy az importálás a hiányzó függőségek miatt meghiúsulhat. Más szóval, a testreszabások hivatkozási mezőkre vagy más, a Project Operations programban eltávolított összetevőkre. Ebben az esetben távolítsa el ezeket a függőségeket a fejlesztői környezetből.
- Ha a nem felügyelt és felügyelt megoldások nem testreszabott összetevőket tartalmaznak, távolítsa el ezeket az összetevőket a megoldásból. Ha például testreszabja a **Project** entitást, csak az entitásfejlécet adja hozzá a megoldáshoz. Ne adja hozzá az összes mezőt. Ha korábban már hozzáadta az összes alösszetevőt, előfordulhat, hogy manuálisan kell létrehoznia egy új megoldást, és hozzá kell adnia a megfelelő összetevőket.
- Előfordulhat, hogy az űrlapok és nézetek nem a várt módon jelennek meg. Bizonyos körülmények között, ha testreszabta a beépített űrlapok vagy nézetek bármelyikét, a testreszabások megakadályozhatják a Project Operations új frissítéseinek érvénybe lépését. A problémák azonosításához javasoljuk, hogy egymás mellett vizsgálja felül a Project Operations tiszta telepítését és a Project Operations telepítését, amely magában foglalja a testreszabásokat is. Hasonlítsa össze a vállalkozás leggyakrabban használt űrlapjait, hogy megbizonyosodjon arról, hogy az űrlap verziója még mindig van értelme, és nem hiányzik valami az űrlap tiszta verziójából. Végezze el ugyanazt az egymás melletti áttekintést a testreszabott nézetekhez.
- Az üzleti logika futásidőben meghiúsulhat. Mivel a beépülő modulok mezőire mutató hivatkozások nem lesznek érvényesítve az importáláskor, az üzleti logika meghiúsulhat a már nem létező mezőkre mutató hivatkozások miatt, és a következő példához hasonló hibaüzenet jelenhet meg: "A Project entitás nem tartalmaz a Name = "msdyn_plannedhours" és a NameMapping = "Logikai" attribútumot. Ebben az esetben módosítsa a testreszabásokat úgy, hogy azok az új mezőket használják. Ha a beépülő modul logikájában automatikusan létrehozott proxyosztályokat és erős típushivatkozásokat használ, fontolja meg a proxyk tiszta telepítésből történő újragenerálását. Ily módon könnyen azonosíthatja az összes olyan helyet, ahol a beépülő modulok elavult mezőktől függenek.

Miután frissítette a testreszabásokat a Project Operations tiszta importálásához, lépjen tovább a következő lépésekre.

## <a name="end-to-end-testing-in-development-environments"></a>Végpontok közötti tesztelés fejlesztői környezetben

### <a name="initiate-upgrade"></a>Frissítés kezdeményezése 

1. Power Platform Az Felügyeleti központban keresse meg és válassza ki a környezetet. Ezután az alkalmazásokban keresse meg és válassza ki **Dynamics 365 Project Operations** a lehetőséget.
2. A frissítés elindításához válassza a Telepítés **lehetőséget**. A Power Platform Felügyeleti központ ezt a telepítést új telepítésként mutatja be. A program azonban észleli a Project Service Automation egy korábbi verziójának jelenlétét, és frissíti a meglévő telepítést.

    A frissítés befejezése után a környezetnek jeleznie kell, hogy a Project Operations telepítve van, és hogy a Project Service Automation nincs telepítve.

    > [!NOTE]
    > A környezetben lévő adatok mennyiségétől függően a frissítés több órát is igénybe vehet. A frissítést kezelő központi csapatnak ennek megfelelően kell megterveznie és futtatnia kell a frissítést munkaidőn kívül. Bizonyos esetekben, ha az adatmennyiség nagy, a frissítést a hétvégén kell futtatni. Az ütemezéssel kapcsolatos döntésnek az alacsonyabb környezetekben végzett tesztelési eredményeken kell alapulnia.

3. Szükség szerint frissítse az egyéni megoldásokat. Ezen a ponton telepítse a testreszabások módosításait a [témakör Tesztelése és újrafaktorozása szakaszában](#testing-and-refactoring-customizations).
4. Nyissa meg a **Beállítások** \> **megoldások lehetőséget**, és válassza a **Project Operations Elavult összetevők** megoldásának eltávolítását.

    Ez a megoldás egy ideiglenes megoldás, amely a frissítés során meglévő adatmodellt és összetevőket tartalmazza. A megoldás eltávolításával eltávolíthatja az összes olyan mezőt és összetevőt, amelyet már nem használnak. Ily módon leegyszerűsítheti a felületet, és megkönnyíti az integrációt és a kiterjesztést.
    
### <a name="validate-common-scenarios"></a>Gyakori forgatókönyvek ellenőrzése

Az adott testreszabások ellenőrzésekor javasoljuk, hogy tekintse át az alkalmazásokban támogatott üzleti folyamatokat is. Ezek az üzleti folyamatok magukban foglalják, de nem kizárólagosan, az értékesítési egységek, például ajánlatok és szerződések létrehozását, valamint a WBS-eket és a tényleges adatok jóváhagyását tartalmazó projektek létrehozását.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Jelentős változások a projektszolgáltatás automatizálása és a projektműveletek között

Ez a szakasz összefoglalja azokat a főbb változásokat, amelyek a Project Service Automation és a Project Operations között várhatók.

### <a name="project-planning"></a>Projekt tervezése

A Project Operations projekttervezési képességei már nem támaszkodnak kombinált ügyféloldali logikára és kiszolgálóoldali logikára. Ehelyett a Project Operations a Project for the Web programot használja ütemezési motorként. Az ütemezési képességek ezen módosítása számos új funkciót tesz lehetővé, például a Tábla- és Gantt-nézeteket, az erőforrás-alapú tervezést, [a tevékenység-ellenőrzőlista-elemeket](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) és a projektütemezési módokat. Az új ütemezési képességeket az új [alkalmazásprogramozási felületek (API-k)](../project-management/schedule-api-preview.md) gazdag készlete is támogatja. Ezek az API-k segítenek biztosítani, hogy a WBS-ben lévő entitások létrehozásához, frissítéséhez vagy törléséhez szükséges programozott művelet ne rontsa meg az ütemezés számított mezőit.

## <a name="billing-and-pricing"></a>Számlázás és árképzés

A Projektműveletek folyamatos beruházásainak részeként számos új képesség áll rendelkezésre a számlázásban és az árképzésben. Íme néhány példa:

- [Projektek és projektfeladatok anyagfelhasználásának rögzítése](../material/material-usage-log.md)
- [Alvállalkozói tevékenység kezelése](../pro/subcontracting/managing-subcontracts-overview.md)
- [Foglalón alapuló szerződések beállítása](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [A szerződés állapota és érvényesítései nem lépik túl az állapotot és az ellenőrzéseket](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Feladatalapú számlázás

## <a name="frequently-asked-questions"></a>Gyakori kérdések

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Jelenleg mely telepítési típusok támogatottak a frissítéshez?

| Source                                                 | Target                                                    | Állam                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Projektműveletek lite telepítése                        | Támogatott               |
| Dynamics 365 Finance projektmenedzsment és számvitel | Projektműveletek lite telepítése                        | Jelenleg nem támogatott |
| Pénzügyi projektmenedzsment és számvitel              | Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez     | Jelenleg nem támogatott |
| Pénzügyi projektmenedzsment és számvitel              | Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez | Jelenleg nem támogatott |
| Projektszolgáltatás automatizálása 3.x                         | Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez     | Jelenleg nem támogatott |
| Project for the Web (dedikált környezet)            | Projektműveletek lite telepítése                        | Jelenleg nem támogatott |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Hogyan telepíthetem a Project Operations programot a frissítési eszköz rendelkezésre állása előtt?

A Project Operations telepítése a frissítési eszköz rendelkezésre állása előtt két lehetőség közül választhat:

- Új környezet kialakítása.
- A Project Operations külön telepítése minden olyan értékesítési szervezeten, ahol a Project Service Automation nincs jelen.

> [!NOTE]
> Ha a Project Service Automation telepítve van egy szervezeten, de nem használták, akkor eltávolítható. A Project Service Automation teljes eltávolítása után a Project Operations telepíthető ugyanarra a szervezetre.
