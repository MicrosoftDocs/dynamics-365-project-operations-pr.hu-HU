---
title: Frissítés a Project Service Automation-ről a Project Operations-re
description: Ez a témakör áttekintést nyújt a frissítés folyamatáról Microsoft Dynamics 365 Project Service Automation Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/05/2022
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
ms.openlocfilehash: 9363fd5a06b6b1ba023961b03228e13a53a82002
ms.sourcegitcommit: 5789766efae1e0cb513ea533e4f9ac1e553158a5
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/10/2022
ms.locfileid: "7954293"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Frissítés a Project Service Automation-ről a Project Operations-re

Izgatottan jelentjük be a három szakasz közül az elsőt Microsoft Dynamics 365 Project Service Automation a frissítéshez Dynamics 365 Project Operations. Ez a témakör áttekintést nyújt azoknak az ügyfeleknek, akik elindulnak erre az izgalmas utazásra. A jövőbeli témakörök közé tartoznak a fejlesztői szempontok és a funkciók fejlesztésével kapcsolatos részletek. Nem csak útmutatást nyújtanak a Projektműveletek frissítésére való felkészüléshez, hanem azt is elmagyarázzák, hogy mire számíthat a frissítés után.

A frissítési kézbesítési program három szakaszra oszlik.

| Kézbesítés frissítése | 1. fázis (2022. január) | 2. fázis (2022. áprilisi hullám) | 3. fázis (2022. áprilisi hullám) |
|------------------|------------------------|---------------------------|---------------------------|
| Nincs függőség a projektek munkalebontási struktúrájától (WBS) | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| A WBS a projektműveletek jelenleg támogatott határain belül | | :heavy_check_mark: | :heavy_check_mark: |
| A WBS a projektműveletek jelenleg támogatott korlátain kívül, beleértve az asztali projekt ügyfél támogatását is | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Frissítési folyamat szolgáltatásai 

A frissítési folyamat részeként frissítési naplókat adtunk hozzá a webhelytérképhez, hogy a rendszergazdák könnyebben diagnosztizálhassák a hibákat. Az új felület mellett új érvényesítési szabályok is bekerülnek a frissítés utáni adatintegritás biztosítása érdekében. A frissítési folyamat a következő érvényesítéseket fogja hozzáadni.

| Érvényesítés | 1. fázis (2022. január) | 2. fázis (2022. áprilisi hullám) | 3. fázis (2022. áprilisi hullám) |
|-------------|------------------------|---------------------------|---------------------------|
| A WBS érvényesítésre kerül a gyakori adatintegritások megsértése esetén (például olyan erőforrás-hozzárendelések, amelyek ugyanahhoz a szülőfeladathoz kapcsolódnak, de különböző szülőprojektekkel rendelkeznek). | | :heavy_check_mark: | :heavy_check_mark: |
| A WBS a Project [for the Web ismert korlátaival lesz érvényesítve](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| A WBS a Project asztali ügyfél ismert korlátaival lesz érvényesítve. | | :heavy_check_mark: | :heavy_check_mark: |
| A foglalható erőforrások és a projektnaptárak kiértékelése a gyakori inkompatibilis naptárszabály-kivételek alapján történik. | | :heavy_check_mark: | :heavy_check_mark: |

A 2. fázisban a Projektműveletekre frissített ügyfelek meglévő projektjeiket írásvédett, projekttervezési élményre frissítik. Ebben az írásvédett élményben a teljes WBS látható lesz a nyomkövető rácsban. A WBS szerkesztéséhez a projektmenedzserek a Fő Projektek lapon a Konvertálás **lehetőséget** **választhatják**. Ezután egy háttérfolyamat frissíti a projektet, hogy támogassa a Project for the Web új projektütemezési élményét. Ez a fázis azoknak az ügyfeleknek megfelelő, akik olyan projektekkel rendelkeznek, amelyek illeszkednek a [Project for the Web ismert korlátai](/project-for-the-web/project-for-the-web-limits-and-boundaries) közé.

A 3. fázisban a program hozzáadja a Project asztali ügyfél támogatását azon ügyfelek javára, akik továbbra is szerkeszteni szeretnék projektjeiket az adott alkalmazásból. Ha azonban a meglévő projekteket az új Webes projekt élménybe konvertálja, a bővítményhez való hozzáférés minden konvertált projekt esetében le lesz tiltva.

## <a name="prerequisites"></a>Előfeltételek

Ahhoz, hogy az ügyfél jogosult legyen az 1. fázisú frissítésre, meg kell felelnie a következő kritériumoknak:

- A célkörnyezet nem tartalmazhat rekordokat a **msdyn_projecttask** entitásban.
- Az érvényes Projektműveleti licenceket az ügyfél összes aktív felhasználójához hozzá kell rendelni. 
- Az ügyfélnek legalább egy olyan nem éles környezetben kell érvényesítenie a frissítési folyamatot, amely reprezentatív adatkészlettel rendelkezik, amely igazodik az éles adatokhoz.
- A célkörnyezetet frissíteni kell a Project Service Automation Update 38- as vagy újabb kiadására.

A 2. és 3. fázis előfeltételei az általános rendelkezésre állási dátumok megközelítésével frissülnek.

## <a name="licensing"></a>Licencelés

Ha aktív licenccel rendelkezik a Project Service Automation szolgáltatáshoz, telepítheti és használhatja a Project Operations-t, amely tartalmazza a Project Service Automation összes képességét és így tovább. Ily módon tesztelheti a Project Operations képességeit, miközben továbbra is használja a Project Service Automation-t az éles környezetben. A Project Service Automation licencek lejárta után át kell térnie a Project Operations-re. Az átmenet tervezésekor figyelembe kell vennie azt a tényt, hogy a Project Operations licenc nem tartalmaz Project Service Automation licencet.

## <a name="testing-and-refactoring-customizations"></a>Testreszabások tesztelése és újrafaktorálása

Kiindulási pontként importálja az összes testreszabást egy tiszta Project Operations (lite) környezetbe, hogy megerősítse, hogy az importálás sikeres, és hogy az üzleti műveletek a várt módon viselkednek.

Íme néhány dolog, amelyre figyelni kell:

- Előfordulhat, hogy az importálás a hiányzó függőségek miatt meghiúsul. Más szóval, a testreszabások referenciamezők vagy más összetevők, amelyeket eltávolítottak a Projektműveletekben. Ebben az esetben távolítsa el ezeket a függőségeket a fejlesztési környezetből.
- Ha a nem felügyelt és felügyelt megoldások nem testreszabott összetevőket tartalmaznak, távolítsa el ezeket az összetevőket a megoldásból. Ha például testreszabja a **Project** entitást, csak az entitásfejet adja hozzá a megoldáshoz. Ne adja hozzá az összes mezőt. Ha korábban már hozzáadta az összes alösszetevőt, előfordulhat, hogy manuálisan kell létrehoznia egy új megoldást, és hozzá kell adnia a megfelelő összetevőket.
- Előfordulhat, hogy az űrlapok és nézetek nem jelennek meg váratlannak. Bizonyos körülmények között, ha testreszabta a beépített űrlapok vagy nézetek bármelyikét, a testreszabások megakadályozhatják a Project Operations új frissítéseinek hatályba lépését. A problémák azonosításához javasoljuk, hogy végezze el a Projektműveletek tiszta telepítésének és a Project Operations testreszabásokat tartalmazó telepítésének egymás melletti felülvizsgálatát. Hasonlítsa össze a vállalkozás leggyakrabban használt űrlapjait annak megerősítéséhez, hogy az űrlap verziójának még mindig van értelme, és nem hiányzik valami az űrlap tiszta verziójából. Végezze el ugyanazt a típusú egymás melletti értékelést a testreszabott nézetek esetében.
- Az üzleti logika futásidőben meghiúsulhat. Mivel a bővítmények mezőire való hivatkozások nem lesznek érvényesítve az importáláskor, előfordulhat, hogy az üzleti logika sikertelen a már nem létező mezőkre való hivatkozások miatt, és a következő példához hasonló hibaüzenet jelenhet meg: "A Project" entitás nem tartalmaz attribútumot Név = "msdyn_plannedhours" és NameMapping = "Logikai". Ebben az esetben módosítsa a testreszabásokat úgy, hogy azok az új mezőket használják. Ha automatikusan generált proxyosztályokat és erős típushivatkozásokat használ a beépülő modul logikájában, fontolja meg a proxyk tiszta telepítésből történő újragenerálását. Ily módon egyszerűen azonosíthatja az összes olyan helyet, ahol a beépülő modulok elavult mezőktől függenek.

Miután frissítette a testreszabásokat a Project Operations tiszta importálásához, lépjen tovább a következő lépésekre.

## <a name="end-to-end-testing-in-lower-environments"></a>Végpontok között végzett tesztelés alacsonyabb környezetben

### <a name="run-the-upgrade-in-production"></a>A frissítés futtatása éles környezetben

1. A Power Platform Felügyeleti központban keresse meg és válassza ki a környezetet. Ezután az alkalmazásokban keresse meg és válassza a **Dynamics 365 Project Operations** lehetőséget.
2. A **frissítés** elindításához válassza a Telepítés lehetőséget. A Power Platform felügyeleti központ új telepítésként mutatja be a telepítést. A rendszer azonban észleli a Project Service Automation egy korábbi verziójának jelenlétét, és a meglévő telepítés frissül.

    A frissítés befejezése után a környezetnek meg kell mutatnia, hogy a Project Operations telepítve van, és hogy a Project Service Automation nincs telepítve.

    > [!NOTE]
    > A környezetben lévő adatok mennyiségétől függően a frissítés több órát is igénybe vehet. A frissítést kezelő központi csapatnak ennek megfelelően kell megterveznie, és nem munkaidőben kell futtatnia a frissítést. Bizonyos esetekben, ha az adatmennyiség nagy, a frissítést a hétvégén kell futtatni. Az ütemezéssel kapcsolatos döntésnek az alacsonyabb környezetekben végzett tesztelési eredményeken kell alapulnia.

3. Frissítse az egyéni megoldásokat, ha szükséges. Ezen a ponton telepítse a testreszabásokon végrehajtott módosításokat a [témakör Tesztelés és testreszabások újrafaktorálása](#testing-and-refactoring-customizations) szakaszában.
4. Lépjen a **Beállítások** \> **megoldások** elemre, és válassza a Project Operations Elavult összetevők megoldás **eltávolításához**.

    Ez a megoldás egy ideiglenes megoldás, amely a frissítés során jelen lévő meglévő adatmodelleket és összetevőket tartalmazza. A megoldás eltávolításával eltávolítja az összes olyan mezőt és összetevőt, amelyet már nem használnak. Ily módon egyszerűsítheti az interfészt, és megkönnyíti az integrációt és a kiterjesztést.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Jelentős változások a project service automation és a project operations között

Ez a szakasz összefoglalja a Project Service Automation és a Project Operations között várható főbb változásokat.

### <a name="project-planning"></a>Projekt tervezése

A Project Operations projekttervezési képességei már nem támaszkodnak az ügyféloldali logika és a kiszolgálóoldali logika kombinációjára. Ehelyett a Project Operations a Project for the Web programot használja ütemezési motorként. Az ütemezési képességek változása számos új funkciót tesz lehetővé, például a Board és a Gantt nézeteket, az erőforrás-vezérelt tervezést, [a tevékenység-ellenőrzőlista elemeket](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) és a projektütemezési módokat. Az új ütemezési képességeket új [alkalmazásprogramozási felületek (API-k) gazdag készlete is](../project-management/schedule-api-preview.md) támogatja. Ezek az API-k célja annak biztosítása, hogy a WBS entitásának létrehozására, frissítésére vagy törlésére szolgáló programozott műveletek ne rontsák az ütemezés számított mezőit.

## <a name="billing-and-pricing"></a>Számlázás és árképzés

A projektműveletek folyamatos beruházásainak részeként számos új képesség érhető el a számlázásban és az árképzésben. Íme néhány példa:

- [Anyagfelhasználás rögzítése projekteken és projektfeladatokon](../material/material-usage-log.md)
- [Alvállalkozói menedzsment](../pro/subcontracting/managing-subcontracts-overview.md)
- [Foglalón alapuló szerződések beállítása](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Szerződés túllépése állapot és érvényesítések](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Feladatalapú számlázás

## <a name="frequently-asked-questions"></a>Gyakori kérdések

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Mely központi telepítési típusok támogatottak jelenleg a frissítéshez?

| Source                                                 | Target                                                    | Állam                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations Lite üzembe helyezése                        | Támogatott               |
| Dynamics 365 Finance Projektmenedzsment és számvitel | Project Operations Lite üzembe helyezése                        | Jelenleg nem támogatott |
| Pénzügyi projektmenedzsment és számvitel              | Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez     | Jelenleg nem támogatott |
| Pénzügyi projektmenedzsment és számvitel              | Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez | Jelenleg nem támogatott |
| Projektszolgáltatás automatizálása 3.x                         | Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez     | Jelenleg nem támogatott |
| Webes projekt (dedikált környezet)            | Project Operations Lite üzembe helyezése                        | Jelenleg nem támogatott |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Hogyan telepíthetem a Project Operations-t, mielőtt a frissítési eszköz elérhető lenne?

A projektműveletek telepítésének két lehetősége van a frissítési eszköz rendelkezésre bocsátása előtt:

- Új környezet kialakítása.
- A Projektműveletek külön üzembe helyezése minden olyan értékesítési szervezetben, ahol a Project Service Automation nincs jelen.

> [!NOTE]
> Ha a Project Service Automation telepítve van egy szervezeten, de nem használták, eltávolítható. A Project Service Automation teljes eltávolítása után a Project Operations ugyanarra a szervezetre telepíthető.
