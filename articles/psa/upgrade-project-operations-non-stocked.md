---
title: Frissítés a Project Service Automation szolgáltatásról Project Operations alkalmazásra
description: Ez a cikk áttekintést nyújt a -ról a -ra Microsoft Dynamics 365 Project Service Automation való frissítés folyamatáról Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
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
ms.openlocfilehash: 2d7b372cac391fab7a81ac6ac5d2ea6d12977b5c
ms.sourcegitcommit: 9de444ae0460c8d15c77d225d0c0ad7f8445d5fc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/18/2022
ms.locfileid: "9686978"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Frissítés a Project Service Automation szolgáltatásról Project Operations alkalmazásra

Örömmel jelentjük be a Microsoftról Microsoft Dynamics 365 Project Service Automation való frissítés három fázisa közül a másodikat Dynamics 365 Project Operations. Ez a cikk áttekintést nyújt azoknak az ügyfeleknek, akik erre az izgalmas utazásra indulnak. 

A frissítés kézbesítési programja három fázisra oszlik.

| Frissítés kézbesítése | 1. fázis (2022. január) | 2. fázis (2022. november) | 3. fázis (2023. áprilisi hullám)  |
|------------------|------------------------|---------------------------|---------------------------|
| Nincs függőség a projektek munkalebontási struktúrájától (WBS) | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| A projektműveletek jelenleg támogatott korlátain belüli munkalebontási struktúra | | :heavy_check_mark: | :heavy_check_mark: |
| A projektműveletek jelenleg támogatott korlátain kívüli munkalebontási struktúra, beleértve a Project asztali ügyfélprogram támogatását is | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Frissítési folyamat funkciók 

A frissítési folyamat részeként frissítési naplókat adtunk hozzá az oldaltérképhez, hogy a rendszergazdák könnyebben diagnosztizálhassák a hibákat. Az új felület mellett új érvényesítési szabályok is hozzáadásra kerülnek, amelyek biztosítják az adatok integritását a frissítés után. A következő érvényesítések lesznek hozzáadva a frissítési folyamathoz.

| Érvényesítés | 1. fázis (2022. január) | 2. fázis (2022. november) | 3. fázis  |
|-------------|------------------------|---------------------------|---------------------------|
| A munkalebontási struktúrát a rendszer ellenőrzi a gyakori adatintegritás-megsértések (például az azonos szülőfeladathoz társított, de eltérő szülőprojektekkel rendelkező erőforrás-hozzárendelések) szempontjából. | | :heavy_check_mark: | :heavy_check_mark: |
| A munkalebontási struktúrát a [Project for the Web ismert korlátai alapján érvényesítjük](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| A munkalebontási struktúrát a rendszer a Project asztali ügyfél ismert korlátai alapján érvényesíti. | |  | :heavy_check_mark: |
| A foglalható erőforrásokat és a projektnaptárakat a rendszer a gyakori inkompatibilis naptárszabály-kivételek alapján értékeli ki. | | :heavy_check_mark: | :heavy_check_mark: |

A 2. fázisban a Project Operations verzióra frissítő ügyfelek meglévő projektjeit írásvédett felületre frissítik a projekttervezéshez. Ebben a csak olvasható élményben a teljes munkalebontási struktúra látható lesz a nyomkövetési rácsban. A munkalebontási struktúra szerkesztéséhez a projektmenedzserek kiválaszthatják a Konvertálás [**lehetőséget**](/PSA-Upgrade-Project-Conversion.md) a projekt főoldalán. Ezután egy háttérfolyamat frissíti a projektet, hogy az támogassa a webes Project új projektütemezési élményét. Ez a fázis olyan ügyfelek számára megfelelő, akik olyan projektekkel rendelkeznek, amelyek illeszkednek a [Webes](/project-for-the-web/project-for-the-web-limits-and-boundaries) Project ismert korlátaihoz.

A 3. fázisban a Project asztali ügyfélprogram támogatása is hozzáadásra kerül azon ügyfelek javára, akik továbbra is szerkeszteni szeretnék projektjeiket az adott alkalmazásból. Ha azonban a meglévő projekteket az új webes projektre konvertálja, a bővítményhez való hozzáférés minden konvertált projektnél le lesz tiltva.

## <a name="prerequisites"></a>Előfeltételek

Az 1. fázisú frissítésre való jogosultsághoz meg kell felelnie a következő feltételeknek:

- A célkörnyezet nem tartalmazhat rekordokat a **msdyn_projecttask** entitásban.
- Az érvényes Project Operations licenceket minden aktív felhasználóhoz hozzá kell rendelni. 
- A frissítési folyamatot legalább egy olyan nem éles környezetben kell ellenőriznie, amely az éles környezethez igazított reprezentatív adatkészletet tartalmaz.
- A célkörnyezetet frissíteni kell a Project Service Automation 37-es (V3.10.58.120) vagy újabb frissítésére.

A 2. fázisú frissítésre való jogosultsághoz meg kell felelnie a következő feltételeknek:

- Az érvényes Project Operations licenceket minden aktív felhasználóhoz hozzá kell rendelni. 
- A frissítési folyamatot legalább egy olyan nem éles környezetben kell ellenőriznie, amely az éles környezethez igazított reprezentatív adatkészletet tartalmaz.
- A célkörnyezetet frissíteni kell a Project Service Automation 37-es (V3.10.58.120) vagy újabb frissítésére.
- A feladatokat tartalmazó környezetek (msdyn_projecttask) csak akkor támogatottak, ha a tevékenységek teljes száma projektenként 500 vagy kevesebb.

A 3. fázis előfeltételei az általánosan elérhető dátum közeledtével frissülnek.

## <a name="licensing"></a>Licencelés

Ha aktív licenccel rendelkezik a Project Service Automation szolgáltatáshoz, telepítheti és használhatja a Project Operations szolgáltatást, amely a Project Service Automation összes funkcióját tartalmazza. Ezután egy külön környezetben tesztelheti a Project Operations képességeit, miközben továbbra is használja a Project Service Automationt az éles környezetben. A Project Service Automation-licencek lejárta után át kell térnie a Project Operations szolgáltatásra. Az áttérés tervezésekor figyelembe kell vennie azt a tényt, hogy a Project Operations licenc nem tartalmaz Project Service Automation licencet.

## <a name="testing-and-refactoring-customizations"></a>Testreszabások tesztelése és újrabontása

Kiindulási pontként importálja az összes testreszabást egy tiszta Project Operations (Lite) környezetbe, hogy megbizonyosodjon arról, hogy az importálás sikeres, és hogy az üzleti műveletek a várt módon viselkednek.

Íme néhány dolog, amire figyelni kell:

- Az importálás hiányzó függőségek miatt meghiúsulhat. Más szóval a testreszabások olyan mezőkre vagy egyéb összetevőkre hivatkoznak, amelyeket eltávolítottak a Project Operations alkalmazásból. Ebben az esetben távolítsa el ezeket a függőségeket a fejlesztési környezetből.
- Ha a nem felügyelt és felügyelt megoldások nem testreszabott összetevőket tartalmaznak, távolítsa el ezeket az összetevőket a megoldásból. Ha például testreszabja a Project **entitást, csak az entitásfejlécet adja hozzá a** megoldáshoz. Ne adja hozzá az összes mezőt. Ha korábban már hozzáadta az összes alösszetevőt, előfordulhat, hogy manuálisan kell létrehoznia egy új megoldást, és hozzá kell adnia a megfelelő összetevőket.
- Előfordulhat, hogy az űrlapok és nézetek nem a várt módon jelennek meg. Bizonyos körülmények között, ha testreszabta a beépített űrlapok vagy nézetek bármelyikét, a testreszabások megakadályozhatják a Project Operations új frissítéseinek érvénybe léptetését. A problémák azonosításához javasoljuk, hogy végezze el a Project Operations tiszta telepítésének és a testreszabásokat tartalmazó Project Operations telepítésének egymás melletti áttekintését. Hasonlítsd össze a vállalkozásodban leggyakrabban használt űrlapokat, és győződj meg arról, hogy az űrlap verziója továbbra is értelmes, és nem hiányzik valami az űrlap tiszta verziójából. Végezze el ugyanazt a típusú, egymás melletti ellenőrzést minden testreszabott nézetnél.
- Az üzleti logika futásidőben meghiúsulhat. Mivel a beépülő modulok mezőire mutató hivatkozásokat a rendszer nem érvényesíti az importáláskor, az üzleti logika meghiúsulhat a már nem létező mezőkre mutató hivatkozások miatt, és az alábbi példához hasonló hibaüzenet jelenhet meg: "A'Projekt' entitás nem tartalmaz Name = 'msdyn_plannedhours' és NameMapping = 'Logical' attribútumot." Ebben az esetben módosítsa a testreszabásokat úgy, hogy azok az új mezőket használják. Ha automatikusan generált proxyosztályokat és erős típushivatkozásokat használ a beépülő modul logikájában, fontolja meg a proxyk tiszta telepítésből való újragenerálását. Ily módon könnyen azonosíthatja az összes olyan helyet, ahol a beépülő modulok elavult mezőktől függenek.

Miután frissítette a testreszabásokat a projektműveletek tiszta importálásához, folytassa a következő lépésekkel.

## <a name="end-to-end-testing-in-development-environments"></a>Teljes körű tesztelés fejlesztési környezetekben

### <a name="initiate-upgrade"></a>Frissítés kezdeményezése 

1. Power Platform A felügyeleti központban keresse meg és válassza ki a környezetet. Ezután az alkalmazásokban keresse meg és válassza a **Dynamics 365 Project Operations** lehetőséget.
2. Válassza a Telepítés **lehetőséget** a frissítés elindításához. A felügyeleti központ ezt a Power Platform telepítést új telepítésként fogja bemutatni. A Project Service Automation korábbi verziójának jelenlétét azonban a rendszer észleli, és a meglévő telepítést frissíti.

    A frissítés befejezése után a környezetnek azt kell mutatnia, hogy a Project Operations telepítve van, és hogy a Project Service Automation nincs telepítve.

    A környezetben lévő adatok mennyiségétől függően a frissítés több órát is igénybe vehet. A frissítést kezelő központi csapatnak ennek megfelelően kell terveznie, és munkaidőn kívül kell futtatnia a frissítést. Bizonyos esetekben, ha az adatmennyiség nagy, a frissítést a hétvégén kell futtatni. Az ütemezéssel kapcsolatos döntésnek az alacsonyabb környezetekben végzett tesztelési eredményeken kell alapulnia.

3. Szükség szerint frissítse az egyéni megoldásokat. Ezen a ponton telepítse a testreszabásokon végrehajtott módosításokat a [cikk Testreszabások](#testing-and-refactoring-customizations) tesztelése és újrabontása szakaszában.
4. Nyissa meg a **Beállítások** \> **megoldásokat**, és válassza a **Project Operations elavult összetevők** megoldás eltávolítását.

    Ez a megoldás egy ideiglenes megoldás, amely a frissítés során meglévő adatmodellt és összetevőket tartalmazza. A megoldás eltávolításával eltávolítja az összes olyan mezőt és összetevőt, amely már nincs használatban. Ily módon egyszerűsítheti a felületet, és megkönnyítheti az integrációt és a kiterjesztést.
    
### <a name="upgrade-to-project-operations-lite"></a>Frissítés a Project Operations Lite verzióra

A következő lépések a frissítési folyamatot és a kapcsolódó hibanaplózást ismertetik:

1. **PSA-verzió ellenőrzése:** A Project Operations telepítéséhez V3.10.58.120 vagy újabb verzióval kell rendelkeznie.
1. **Előzetes érvényesítés:** Amikor egy rendszergazda frissítést kezdeményez, a rendszer egy előellenőrzési műveletet futtat minden olyan entitáson, amely a Project Operations megoldás központi eleme. Ez a lépés ellenőrzi, hogy minden entitáshivatkozás érvényes-e, és biztosítja, hogy a munkalebontási struktúrához kapcsolódó adatok a Project for the Web közzétett korlátain belül legyenek.
1. **Metaadatok frissítése:** A sikeres előzetes ellenőrzés után a rendszer módosításokat kezdeményez a sémában, és létrehoz egy elavult összetevő-megoldást. Ezt az elavult megoldást eltávolíthatja, miután elvégezte a testreszabások összes szükséges újrabontását. Ez a lépés a frissítési folyamat leghosszabb része, és akár négy órát is igénybe vehet.
1. **Adatfrissítés:** Miután a metaadat-frissítési lépésben az összes szükséges sémamódosítás befejeződött, a rendszer áttelepíti az adatokat az új sémába, és elvégzi a szükséges alapértelmezett beállításokat és újraszámításokat.
1. **Projektütemezési motor frissítése:** A sikeres adatfrissítés után a **főoldal Ütemezés** lapja Feladatok **címkével lesz ellátva**. Amikor egy felhasználó a frissítés után kiválasztja ezt a lapot, a rendszer arra irányítja, hogy navigáljon a nyomkövetési rácsra a WBS írásvédett verziójának megtekintéséhez. A munkalebontási struktúra szerkesztéséhez el kell indítaniuk az ütemezési [átalakítási folyamatot](/PSA-Upgrade-Project-Conversion.md). Minden olyan projekt, amely nem rendelkezik már meglévő WBS-sel, közvetlenül, átalakítás nélkül használhatja az új ütemezési élményt.
 
### <a name="validate-common-scenarios"></a>Gyakori forgatókönyvek ellenőrzése

Az adott testreszabások érvényesítésekor javasoljuk, hogy tekintse át az alkalmazások által támogatott üzleti folyamatokat is. Ezek az üzleti folyamatok magukban foglalják, de nem kizárólagosan, az értékesítési entitások, például árajánlatok és szerződések létrehozását, valamint a WBS-eket és a tényleges adatok jóváhagyását tartalmazó projektek létrehozását.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Jelentős változások a Project Service Automation és a Project Operations között

Ez a szakasz összefoglalja a Project Service Automation és a Project Operations között várható főbb változásokat.

### <a name="project-planning"></a>Projekt tervezése

A Project Operations projekttervezési képességei már nem támaszkodnak az ügyféloldali és a kiszolgálóoldali logika kombinációjára. Ehelyett a Project Operations a webes Projectet használja ütemezési motorként. Az ütemezési képességek ezen változása számos új funkciót tesz lehetővé, például a Tábla és Gantt nézeteket, az erőforrás-alapú tervezést, a tevékenységek ellenőrzőlista-elemeit [és](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) a projektütemezési módokat. Az új ütemezési képességeket az új [alkalmazásprogramozási felületek (API-k)](../project-management/schedule-api-preview.md) gazdag készlete is támogatja. Ezeknek az API-knak az a célja, hogy biztosítsák, hogy a munkalebontási struktúrában lévő entitások létrehozására, frissítésére vagy törlésére szolgáló programozott műveletek ne rongálják meg az ütemezés számított mezőit.

### <a name="billing-and-pricing"></a>Számlázás és árképzés

A Project Operations folyamatos befektetéseinek részeként számos új funkció érhető el a számlázásban és a díjszabásban. Íme néhány példa:

- [Anyagfelhasználás rögzítése projekteken és projektfeladatokon](../material/material-usage-log.md)
- [Alvállalkozói szerződések kezelése](../pro/subcontracting/managing-subcontracts-overview.md)
- [Foglalón alapuló szerződések beállítása](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [A szerződés nem haladhatja meg a státuszt és az érvényesítéseket](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Feladatalapú számlázás

### <a name="resource-management"></a>Erőforrás-kezelés

A Project Operations opcionális támogatást nyújt az (URS) táblához és az Universal Resource Scheduling ütemezési segédhez. Ez az új tapasztalat a 2023. áprilisi hullámban válik kötelezővé.

## <a name="frequently-asked-questions"></a>Gyakori kérdések

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Mely központi telepítési típusok támogatottak jelenleg a frissítéshez?

| Source                                                 | Target                                                    | Állam                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations Lite üzembe helyezés                        | Támogatott               |
| Dynamics 365 Finance Projektmenedzsment és számvitel | Project Operations Lite üzembe helyezés                        | Jelenleg nem támogatott |
| Pénzügyi projektmenedzsment és számvitel              | Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez     | Jelenleg nem támogatott |
| Project Service Automation 3.x                         | Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez     | Jelenleg nem támogatott |
| Webes projekt (dedikált környezet)            | Project Operations Lite üzembe helyezés                        | Jelenleg nem támogatott |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Hogyan telepíthetem a Project Operations rendszert, mielőtt a frissítési eszközök elérhetővé válnának?

A Project Operations két lehetőség közül választhat, mielőtt a frissítési eszközök elérhetővé válnának:

- Új környezet kiépítése.
- A Project Operations külön telepíthető minden olyan értékesítési szervezeten, ahol a Project Service Automation nincs jelen.

Ha a Project Service Automation telepítve van egy szervezeten, de nem használták, eltávolítható. A Project Service Automation teljes eltávolítása után a Project Operations telepíthető ugyanarra a szervezetre.
