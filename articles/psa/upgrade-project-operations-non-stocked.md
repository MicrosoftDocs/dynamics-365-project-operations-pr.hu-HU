---
title: Frissítés a Project Service Automation szolgáltatásról Project Operations alkalmazásra
description: Ez a cikk a Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Project Operations verzióra való frissítési folyamatáról nyújt áttekintést.
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
ms.openlocfilehash: ac2435c99f3aa9b2a6cdb08d7ce5f6628e7f6ac4
ms.sourcegitcommit: bea5f9b4066277344add1da3a1567ed56a0cfd31
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/02/2022
ms.locfileid: "9736669"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Frissítés a Project Service Automation szolgáltatásról Project Operations alkalmazásra

Nagyon örülünk, hogy bejelentheti a Microsoft Dynamics 365 Project Service Automation a Microsoft Dynamics 365 Project Operations verzióra való frissítésének három fázisa közül a másodikat. Ez a cikk áttekintést ad azoknak a az ügyfeleknek akik rész vesznek ebben az izgalmas folyamatban. 

A frissítés átadási programja három fázisra lesz felosztva.

| Frissítés kézbesítése | 1. fázis (2022. január) | 2. fázis (2022. november) | 3. fázis (2023. áprilisi hullám)  |
|------------------|------------------------|---------------------------|---------------------------|
| Nincs függőség projektek munkalebontási struktúrájával (WBS) | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS a Project Operations jelenleg támogatott korlátain belül | | :heavy_check_mark: | :heavy_check_mark: |
| WBS a Project Operations jelenleg támogatott korlátain kívül, beleértve a Project Desktop Client támogatását is | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>A frissítési folyamat jellemzői 

A frissítési folyamat részeként az oldaltérképhez a frissítési naplókat adtunk, hogy az rendszergazdák könnyebben diagnosztizálhassák a hibákat. Az új felület mellett új ellenőrzési szabályok is hozzá lesznek adva az adatok integritásának biztosításához a frissítés után. A következő ellenőrzésekkel egészül ki a frissítési folyamat.

| Ellenőrzések | 1. fázis (2022. január) | 2. fázis (2022. november) | 3. fázis  |
|-------------|------------------------|---------------------------|---------------------------|
| A WBS-t a gyakori adatintegritás-eltérések (például az ugyanazon fölérendelt feladathoz társított, de eltérő fölérendelt projekthez tartozó erőforrás-hozzárendelések) szempontjából is ellenőrizve lesz. | | :heavy_check_mark: | :heavy_check_mark: |
| A WBS ellenőrizve lesz a [Project for the Web ismert korlátozásai](/project-for-the-web/project-for-the-web-limits-and-boundaries) szempontjából is. | | :heavy_check_mark: | :heavy_check_mark: |
| A WBS ellenőrizve lesz a Project Desktop Client ismert korlátozásai szempontjából is. | |  | :heavy_check_mark: |
| A foglalható erőforrások és projektnaptárak ellenőrizve lesznek a gyakori nem kompatibilis naptárszabály-kivételek szempontjából is. | | :heavy_check_mark: | :heavy_check_mark: |

A 2. fázisban a Project Operations rendszerre frissítő ügyfelek a meglévő projektjei frissítve lesznek a csak olvasható élményre frissítik a projekttervezéshez. Ebben a csak olvasható élményben a teljes WBS látható lesz a követési rácson. A WBS szerkesztéséhez a projektvezetők kiválaszthatják az [**Átalakítás**](/PSA-Upgrade-Project-Conversion.md) lehetőséget a projekt főoldalán. Ezután egy háttérfolyamat frissíti a projektet, hogy az támogassa a Project for the Web új projektütemezési élményét. Ez a fázis megfelelő az olyan ügyfelek számára, akik a [Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries) ismert korlátain belül vannak.

A 3. fázisban a Project Desktop Client támogatása is hozzáadódik azoknak az ügyfeleknek az érdekében, hogy a abból az alkalmazásból tovább szerkesztenék a projektjeiket. Ha azonban a meglévő projekteket átalakítja az új Project for the Web élményhez, akkor minden átalakított projektnél le lesz tiltva a bővítmény elérése.

## <a name="prerequisites"></a>Előfeltételek

Ahhoz, hogy jogosult legyen az 1. fázis frissítésére, a következő feltételeknek kell teljesülnie:

- A célkörnyezet nem tartalmazhat rekordokat az **msdyn_projecttask** entitásban.
- Érvényes Project Operations-licenceket kell minden aktív felhasználóhoz hozzárendelni. 
- A frissítési folyamatot validálnia kell legalább egy olyan, nem éles környezetben, amely az éles környezethez igazított, reprezentatív adathalmazt tartalmaz.
- A célkörnyezetet Project Service Automation Update Release 37 (V3.10.58.120) vagy újabb verzióra kell frissíteni.

Ahhoz, hogy jogosult legyen az 2. fázis frissítésére, a következő feltételeknek kell teljesülnie:

- Érvényes Project Operations-licenceket kell minden aktív felhasználóhoz hozzárendelni. 
- A frissítési folyamatot validálnia kell legalább egy olyan, nem éles környezetben, amely az éles környezethez igazított, reprezentatív adathalmazt tartalmaz.
- A célkörnyezetet Project Service Automation Update Release 37 (V3.10.58.120) vagy újabb verzióra kell frissíteni.
- A feladatokat (msdyn_projecttask) tartalmazó környezeteket csak akkor támogatja a rendszer, ha a feladatok teljes száma projektenként 500 vagy kevesebb.

A 3. fázis előfeltételei frissítésre kerülnek az általános elérhetőségi dátum közeledtével.

## <a name="licensing"></a>Licencelés

Ha rendelkezik a aktív Project Service Automation licencekkel, telepítheti és használhatja a Project Operations alkalmazást, amely a Project Service Automation és szolgáltatásait és további szolgáltatásokat tartalmaz. Ily módon tesztelheti a Project Operations képességeit, miközben az éles környezetben tovább használhatja a Project Service Automation szolgáltatást. A Project Service Automation licencek lejárata után át kell térnie a Project Operations használatára. Az áttérés tervezéséhez figyelembe kell vennie azt a tényt, hogy a Project Operations licenc nem tartalmaz Project Service Automation licencet. Azok az ügyfelek, akiknek olyan forgatókönyvük van, hogy telepítették a Project Service Automation szolgáltatást, és a Project Operations szolgáltatásba való költözésük során tovább kell használniuk vagy növelniük kell a PSA-licenceik számát, ideiglenes PSA-licenceket kérhetnek a megvásárolt Project Operations-licencek alapján. Egy Project Service Automation licenc lesz kiadva egy Project Operations-licenchez. A következő hivatkozás segítségével igényelhetőek ideiglenes PSA-licencek: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Testreszabások tesztelése és átalakítása

Kiindulási pontként importálja az összes testreszabást egy tiszta Project Operations (Lite) környezetbe, hogy meggyőződjen az importálás sikerességéről, és arról, hogy az üzleti műveletek a várt módon működnek.

A következő dolgokra kell figyelni:

- A hiányzó függőségek miatt az importálás sikertelen lehet. Más szóval, a testreszabások referenciamezői vagy a Project Operationsből eltávolított egyéb összetevők. Ebben az esetben távolítsa el ezeket a függőségeket a fejlesztési környezetből.
- Ha a nem felügyelt és a felügyelt megoldások nem testreszabott összetevőket tartalmaznak, akkor távolítsa el ezeket az összetevőket a megoldásból. A **Projekt** entitás testreszabásakor például csak az entitásfejlécet vegye fel a megoldásba. Ne vegye fel az összes mezőt. Ha korábban az összes részösszetevőt hozzáadta, előfordulhat, hogy manuálisan kell létrehoznia egy új megoldást, és hozzá kell adnia a megfelelő összetevőket.
- Előfordulhat, hogy az űrlapok és nézetek nem az elvárt módon jelennek meg. Bizonyos körülmények között, ha bármely gyári űrlapot vagy nézetet testreszabta, a testreszabások megakadályozhatják a Project Operations új frissítéseinek életbe lépését. Ezeknek a problémáknak az azonosításához ajánlott egymás áttekintani a Project Operations érintetlen telepítését, illetve a testreszabásokat tartalmazó Project Operations példányt. Hasonlítsa össze a vállalat leggyakrabban használt űrlapjait, hogy meggyőződhessen arról, hogy az űrlapnak továbbra is értelme van, és hogy az űrlap tiszta verziójához képest nem-e hiányzik valami. A testre szabott nézetek kapcsán is végezzen hasonló egymás melletti áttekintést.
- Futásidőben az üzleti logika elbukhat. Mivel a beépülő modulokban található mezőkre mutató hivatkozásokat a rendszer nem ellenőrzi az importáláskor, az üzleti logika hibás lehet a már nem létező mezőkre mutató hivatkozások miatt, és a következő példára hasonlító hibaüzenet jelenhet meg: „A 'Project' entitás nem tartalmaz Name = 'msdyn_plannedhours' attribútumot és NameMapping = 'Logical' attribútumot. Ebben az esetben módosítsa a testreszabásokat úgy, hogy azok az új mezőket használják. Ha automatikusan létrehozott proxyosztályokat és erős típusú hivatkozásokat használ a beépülő modul logikájában, érdemes megfontolni az ilyen proxyk tiszta telepítésből való újragenerálását. Ily módon könnyen azonosíthatók az összes helyet, ahol a beépülő modulok az elavult mezőktől függnek.

A testreszabások frissítését követően a Project Operations tiszta importálásához lépjen tovább a következő lépésekre.

## <a name="end-to-end-testing-in-development-environments"></a>Végpontok között végzett tesztelés fejlesztési környezetben

### <a name="initiate-upgrade"></a>Frissítés kezdeményezése 

1. A Power Platform felügyeleti központban keresse meg, és jelölje ki környezetét. Majd az alkalmazások között keresse meg, és jelölje ki a **Dynamics 365 Project Operations** alkalmazást.
2. Az frissítés befejezéséhez válassza a **Telepítés** lehetőséget. A Power Platform felügyeleti központ új telepítésként jeleníti meg ezt a telepítést. Azonban a Project Service Automation egy korábbi verzióját észleli a rendszer, és frissíti a meglévő telepítést.

    A frissítés befejezését követően a környezetnek azt kell mutatnia, hogy a Project Operations telepítve van, és hogy a Project Service Automation nincs telepítve.

    A környezetben található adatok mennyiségétől, a frissítés több óráig is eltarthat. A frissítést kezelő központi csoportnak ennek megfelelően kell meg tervezni a frissítést, és nem munkaidőben futtatni a frissítést. Bizonyos esetekben, ha nagy az adatmennyiség, a frissítést a hétvégeken kell futtatni. Az ütemezésről a döntést alsóbb környezetekben végzett tesztelési eredmények alapján kell dönteni.

3. Szükség szerint frissítse az egyéni megoldásokat. Ezen a ponton helyezze üzembe a testreszabáson végzett módosításokat a cikk [Testreszabások tesztelése és átalakítása](#testing-and-refactoring-customizations) szakaszának megfelelően
4. Látogasson el a **make.powerapps.com** weboldalra, válassza ki a környezetet a portál jobb felső felében található legördülő listában, válassza a bal menü **Megoldások** parancsát, válassza az **Elavult Project Operations összetevők** megoldást, majd az **Eltávolítás** lehetőséget.

    Ez a megoldás egy ideiglenes megoldás, amely megtartja a frissítés során meglévő adatmodellt és összetevőket. A megoldás eltávolításával a már nem használt összes mezőt és összetevőt eltávolítja. Ily módon egyszerűsíthető a felület, és egyszerűbbé válik az integráció és a bővítés.
    
### <a name="upgrade-to-project-operations-lite"></a>Frissítés a Project Operations – Lite verzióra

A következő lépések ismertetik a frissítési folyamatot és a hozzá tartozó hibanaplózást:

1. **PSA verzió ellenőrzése:** A Project Operations telepítéséhez V3.10.58.120 vagy újabb verzió szükséges.
1. **Előzetes ellenőrzés:** Amikor egy rendszergazda frissítést kezdeményez, a rendszer minden egyes olyan entitáson futtat előzetes ellenőrzési műveletet, amely a Project Operations megoldás központi eleme. Ez a lépés ellenőrzi az összes entitáshivatkozás érvényességét, és biztosítja, hogy a WBS-hez kapcsolódó adatok a Project for the Web közzétett korlátozásain belül vannak.
1. **Metaadat-frissítés:** A sikeres előzetes ellenőrzés után a rendszer változtatásokat kezdeményez a sémában, és létrehoz egy elavult összetevő-megoldást. Az elavult megoldást a testreszabások szükséges újraépítése után eltávolíthatja. Ez a lépés a frissítési folyamat leghosszabb része, amely akár négy órát is igénybe vehet.
1. **Adatfrissítés:** Miután a metaadat-frissítési lépésben befejeződött az összes szükséges sémamódosítás, az adatok át lesznek költöztetve vannak az új sémába, és minden szükséges alaphelyzetbe állítás és újraszámítás megtörténik.
1. **Projektütemező motor frissítése:** Az adatok sikeres frissítése után a főoldal **Ütemezés** lapja új, **Feladatok** címkét kap. Ha egy felhasználó a frissítés után kiválasztja ezt a lapot, akkor a rendszer megkéri, hogy navigáljon a követési rácsra a WBS írásvédett verziójának megtekintéséhez. A WBS szerkesztéséhez kezdeményeznie kell az ütemezés [átalakítási folyamatát](/PSA-Upgrade-Project-Conversion.md). A meglévő WBS nélküli összes projekt közvetlenül, átalakítás nélkül használhatja az új ütemezési élményt.
 
### <a name="validate-common-scenarios"></a>Gyakori üzleti ellenőrzése

Javasoljuk, hogy a testreszabások ellenőrzésekor tekintse át a különböző alkalmazásokban támogatott üzleti folyamatokat is. Ezek az üzleti folyamatok többek között értékesítési entitások (például ajánlatok és szerződések) létrehozása, illetve WBS-eket és tényadatok jóváhagyását tartalmazó projektek.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>A Project Service Automation szolgáltatásról Project Operations alkalmazás közötti jelentős változások

Ez a szakasz a Project Service Automation és a Project Operations közötti főbb változásokról ad áttekintést.

### <a name="project-planning"></a>Projekt tervezése

A Project Operations projekttervezési lehetőségei a továbbiakban nem támaszkodnak ügyféloldali logikára és szerveroldali logikára. Ehelyett a Project Operations a Project for the Webet használja ütemezési motorként. Az ütemezési lehetőségek ilyen módosítása több új funkciót is támogat, ilyen például a Tábla és a Ganttg nézet, az erőforrás-központú tervezés, [feladat-ellenőrzőlista elemek](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) és projektütemezési módok. Az új ütemezési képességeket számos új [alkalmazásprogramozási felület (API)](../project-management/schedule-api-preview.md) is támogatja. Ezen API-k célja annak biztosítása, hogy egyetlen, a WBS szolgáltatásban található entitások létrehozására, frissítésére és törlésére szolgáló programozható művelet se okozzon sérülést az ütemezésben számított mezőknek.

### <a name="billing-and-pricing"></a>Számlázás és árképzés

A Project Operations folyamatos befektetései részeként számos új lehetőség áll rendelkezésre a Számlázás és Díjszabás szolgáltatásban. Íme néhány példa:

- [Anyaghasználat rögzítése projekteknél és projektfeladatoknál](../material/material-usage-log.md)
- [Alvállalkozók kezelése](../pro/subcontracting/managing-subcontracts-overview.md)
- [Foglalón alapuló szerződések beállítása](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Nem meghaladandó állapot és ellenőrzések szerződésen](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Feladat alapú számlázás

### <a name="resource-management"></a>Erőforrás-kezelés

A Project Operations opcionális támogatást nyújt a Universal Resource Scheduling (URS) táblához és az ütemezési segédhez. Ez az új élmény a 2023. áprilisi hullámtól válik kötelezővé.

## <a name="frequently-asked-questions"></a>Gyakori kérdések

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Jelenleg mely telepítési típusok támogatottak a frissítéshez?

| Source                                                 | Target                                                    | Állam                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations Lite központi telepítés                        | Támogatott               |
| Dynamics 365 Finance Projektmenedzsment és könyvelés | Project Operations Lite központi telepítés                        | Jelenleg nem támogatott |
| Finance Projektmenedzsment és könyvelés              | Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez     | Jelenleg nem támogatott |
| Project Service Automation 3.x                         | Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez     | Jelenleg nem támogatott |
| Project for the web (dedikált környezet)            | Project Operations Lite központi telepítés                        | Jelenleg nem támogatott |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Hogyan lehet telepíteni a Project Operations alkalmazást a frissítési eszköz elérhetősége előtt?

A frissítési eszközök elérhetősége előtt két lehetőség érhető el a Project Operations telepítéséhez:

- Új környezet kiépítése.
- A Project Operations különálló telepítése minden olyan értékesítési szervezetre, ahol nincs jelen a Project Service Automation nincs jelen.

Ha egy szervezeten telepítve van a Project Service Automation, de nem volt használva, az eltávolítható. A Project Service Automation teljes eltávolítása után a Project Operations ugyanazon a szervezetre telepíthető.
