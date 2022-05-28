---
title: Tételnaplók létrehozása és megerősítése
description: Ez a témakör a Bejegyzésnaplók Microsoft programban való létrehozásáról és megerősítéséről nyújt tájékoztatást Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8cb768337bc197895a837670f93b99b132c97437
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584231"
---
# <a name="create-and-confirm-entry-journals"></a>Tételnaplók létrehozása és megerősítése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az Entry naplók segítségével közvetlenül a Microsoft alkalmazásban rögzítheti a tényleges adatokat Dynamics 365 Project Operations. A Tételnaplók használatakor nem kell idő-, költség- és anyaghasználati naplókat megadnia a Projektműveletek mezőben.

Egyetlen tételnaplóval több naplósort hozhat létre. A napló megerősítésekor a Tétel naplósor a következő részletekkel rögzíti a tényleges értéket:

- A költség vagy bevétel a kiválasztott tranzakciótípustól függően.
- A kiválasztott tranzakcióosztály. A rendelkezésre álló osztályok az **idő**, a költség **,** **az anyag**, **a retainer**, **a milestone** és **az adó**.
- A naplósorban kijelölt projekt és/vagy tevékenység.

Az alábbi lépéseket követve hozzon létre egy tételnaplót a Projektműveletek programban.

1. Nyissa meg az **Eladási** \> **tranzakciók** \> **naplóit.**
2. **A Bejegyzésnaplók** listalap Művelet ablaktábláján válassza az Új **lehetőséget** napló létrehozásához.
3. **Az Új naplólap** Megnevezés **mezőjében** adja meg a napló leírását.
4. Győződjön meg arról, hogy a **Napló típusa** mező értéke Tétel **, majd válassza a** Mentés **lehetőséget**. Az új bejegyzésnapló mentése után a naplólapon meg kell jelennie a **Naplósorok** lapnak.
5. **A Naplósorok** lap rács feletti eszköztárán válassza az Új **lehetőséget** a Bejegyzés naplósor létrehozásához.
6. **A** Tételnaplósor létrehozásához párbeszédpanelen állítsa be a mezőket az alábbi táblázatban leírtak szerint.

    | Mező | Description | Funkcionális hatás |
    | --- | --- | --- |
    | Tranzakció osztálya | A naplósor a hat tranzakciós osztály egyikébe sorolható: **Idő**, Költség **,** Anyag **,** **Megtartó**, **Mérföldkő** vagy **Adó**. | Az **adótranzakció-osztály** elavult a Projektműveletek mappában. <br> Ha létrehoz egy adótranzakciós **osztályt**, azt a rendszer nem dolgozza fel számlázással, illetve költség- vagy bevételszámítással. **A Milestone** egy csak bevételre vonatkozó tranzakciós osztály. <br>A **Retainer** tranzakcióosztály egy vevőtől kapott előleget jelöl. Mindig számlázott eladások és nem számlázott eladási naplósorok párjaként kell létrehozni. |
    | Tranzakció típusa | A költség rögzítéséhez a **Költség**, **az Interorg értékesítés** és **a beszerzési egységköltség** tranzakciótípusokat kell használni.<br> A bevétel rögzítéséhez a **Nem számlázott eladások** és **a számlázott értékesítés** tranzakciótípusokat kell használni. | A **Retainer** tranzakcióosztály csak a Nem számlázott eladások és **a** számlázott eladások **tranzakciótípusokkal** működik.<br> A **Milestone** tranzakciós osztály csak a **Számlázott eladás** tranzakciótípussal működik. <br>Az **Interorg értékesítési** és **beszerzési egységköltség-tranzakciótípusai** csak az Időtranzakció **osztályra vonatkoznak, és ezek csak a** Lite üzembe helyezési scneario bejegyzésnaplóiban kezelhetők, és nem akkor, ha a Projektműveleteket erőforrás- és nem raktározott forgatókönyvekben telepíti. |
    | Termék kiválasztása | Ha az Anyagtranzakció **osztály van kiválasztva, ez a** mező azt adhatja meg, hogy az anyagtranzakció, amelyhez a naplósort létrehozza, meglévő termék vagy beírási termék-e. | Ha a Beírás lehetőséget **választja**, megadhatja a termék nevét. |
    | Termék | Hivatkozás a katalógusból származó termékre. | |
    | Description | A naplósor leírása, amely megkönnyíti az azonosítást. | Nem számlázott eladási naplósorok esetén a program a számlasor részleteinek létrehozásakor az értéket használja leírásként. |
    | Külső leírás | A külső érdekelt felekkel való megosztásra használható naplósor leírása. | Nem számlázott eladási naplósorok esetén a program külső megnevezésként használja az értéket a számlasor részleteinek létrehozásakor. A vevőnek küldött számlán is megjelenhet. |
    | Számlázási típus | Olyan érték, amely azt jelzi, hogy a naplósor a projekt felszámítható, ingyenes vagy fel nemszámítható összetevőjének számít-e. | Egy tipikus folyamatban a számlázási típus a szerződésen beállított, egyeztetett feltételekből származik. Naplósor rögzítésekor azonban ebben a mezőben megadhat egy értéket. |
    | Dokumentum kelte | Használjon dátumot a tranzakció megtörténtének dátumára. | |
    | Kezdési dátum | Használja a tranzakció időpontjának dátumát. | Ez a mező a Kiegyenlítetlen eladás **típusú tranzakciók** számla létrehozásának dátumával való összehasonlításra szolgál. Ez az összehasonlítás segít eldönteni, hogy a tranzakció határidős vagy elavult-e. Csak lejárt dátumú tranzakciók kerülnek hozzáadásra a számlához. |
    | Befejező dátum | Használja a tranzakció időpontjának dátumát. | |
    | Könyvelési dátum | Használja azt a dátumot, amikor a könyvelési hatást rögzítik. | |
    | Szerződéssor vevője | Alapértelmezés szerint, ha a szerződéssornak csak egy vevője van, akkor ez a mező a naplósor mentésekor a szerződéssorban szereplő vevőre lesz állítva. Ha a szerződéssornak több vevője van, válassza ki a megfelelő vevőt a szerződéssorban. | Ha a rendszer nem tudja meghatározni a naplósorban szereplő szerződéssor vevőjét, és ha üres a naplósorból létrehozott Nem számlázott eladás **típus tényleges értékén**, akkor a tényleges nem lesz számlázva. |
    | Project | Válassza ki azt a projektet, amelyen rögzíteni szeretné a tényleges beállítást. | A kiválasztott projekt, tranzakcióosztály és tevékenység alapján a rendszer megpróbálja meghatározni a szerződést, a szerződéssort és a szerződéssor vevőjét. |
    | Feladatok | Válassza ki azt a feladatot, amelyen a tényleges beállítást rögzíteni szeretné. | Ha a szerződés beállítása során tevékenységeket társított a szerződéssorokhoz, a rendszer a kiválasztott tevékenységet, valamint a projekt- és tranzakcióosztályt használja a szerződés, a szerződéssor és a szerződéssor vevőjének meghatározásához. |
    | Tranzakció kategóriája | Válassza ki azt a tranzakciókategóriát, amelyen rögzíteni szeretné a tényleges beállítást. | Költségek esetén a kiválasztott tranzakciókategória határozza meg a naplósorban mentéskor beírandó alapértelmezett árat. |
    | Beosztás | Ez a mező az Időnapló sorokra vonatkozik. Válassza ki annak az erőforrásnak a szerepét, aki időt töltött a projekten és/vagy tevékenységen. | Időnaplósorok esetén, ha az alapértelmezett erőforrásköltségek és számladíjak beviteléhez a beépített konfigurációt használja, a program a kijelölt szerepkört a forrásegységcel együtt használja a naplósorban a mentéskor beírandó alapértelmezett ár meghatározásához. Ha egyéni konfigurációt használ az alapértelmezett árak beviteléhez, tekintse át ezt a konfigurációt annak megállapításához, hogy a Szerepkör **mező az** alapértelmezett árértékek megadására szolgál-e. |
    | Alvállalkozói szerződés | Ha a naplósor alvállalkozói kapacitást, illetve alvállalkozói költségeket vagy anyagokat jelöl, válassza ki a megfelelő alvállalkozói szerződést. | Költségnaplósorok rögzítésekor a kiválasztott alvállalkozó határozza meg az alapértelmezett egységköltség megadásához használt árlistát. |
    | Alvállalkozói sor | Ha a naplósor alvállalkozói kapacitást, illetve alvállalkozói költségeket vagy anyagokat jelöl, válassza ki a megfelelő alvállalkozói sort. | Költségnaplósorok rögzítésekor a kiválasztott alvállalkozói sor biztosítja az alvállalkozói sorban rendelkezésre álló kapacitásszámítások helyes kiszámítását. |
    | Összegszámítási mód | Alapértelmezés szerint ez a mező a Mennyiség és ár szorzata értékre **van állítva**. Ha ezt a módszert használja, a program az összeget mennyiségként *×* árként *számítja* ki. A másik támogatott módszer a **Fix ár**. Ha ezt a módszert használja, az ár az összegre lesz állítva, és a mennyiség nem lesz felhasználva a számításban. | |
    | Egységütemezés és egység | Az egységütemezés és az egység együttesen azonosítja a mennyiség egységét. | Az egység és a tranzakciós kategória kombinációja a költségek alapértelmezett árainak megadására szolgál. A Projektműveletek alapértelmezett konfigurációjában az egység, a szerepkör és a forrásegység kombinációja az alapértelmezett árak idő szerinti megadására szolgál. Ha egyéni konfigurációval rendelkezik az alapértelmezett árak beviteléhez, akkor azt a rendszer az egységgel együtt használja. A termék és az egység kombinációja az anyagok alapértelmezett árának megadására szolgál. |
    | Mennyiség | Adja meg a mennyiséget. | |
    | Ár | Ha az ár üresen marad a naplósor létrehozásakor, a program a tranzakcióosztálytól függően a megfelelő értékeket használja az alapértelmezett árak megadásához. Ha a naplósor létrehozásakor árat ad meg, a program ezt az árat használja. | |
    | Adó | Adja meg az adó összegét. | A megadott adóösszegtől függően a program a kiterjesztett összeget *Összegadóként* + *számítja* ki. |

## <a name="confirm-an-entry-journal"></a>Tételnapló megerősítése

Miután beírta az összes naplósort egy tételnaplóba, megerősítheti a naplót. Ez a folyamat minden naplósort ténylegesként rögzít a megfelelő projektekben.

A napló megerősítése után a továbbiakban nem szerkesztheti sem azt, sem annak sorait.

## <a name="actuals-created-by-entry-journal-confirmation"></a>A tételnapló visszaigazolása által létrehozott aktualitások

Van néhány kulcsfontosságú különbség a Tételnapló visszaigazolása által létrehozott tényleges értékek és a Projektműveletek programban az idő-, költség- és anyaghasználati naplók jóváhagyása és a számla-visszaigazolás során létrehozott tényleges értékek között:

- A tételnaplók nem használnak tranzakciós kapcsolatokat a tényleges költség és a nem számlázott értékesítési tényleges érték összekapcsolására. Az idő-, költség- és anyaghasználati naplók jóváhagyásakor létrehozott tényleges értékek mindig tranzakciós kapcsolatokat használnak a költség és a nem számlázott értékesítési tényleges értékek összekapcsolására.
- A tételnaplók nem használnak tranzakció eredetet a tényleges költség és a nem számlázott értékesítési tényleges értékek bármely származó rekordhoz való csatolására. Az idő-, költség- és anyaghasználati naplók jóváhagyásakor létrehozott tényleges értékek mindig tranzakciós eredetet használnak a költség- és nem számlázott értékesítési tényleges értékeknek az eredeti időbevitelhez való kapcsolásához.
- A Tételnapló visszaigazolásával létrehozott nem számlázott értékesítési tényleges értékek számlázásakor a számla megerősítése során létrehozott számlázott értékesítési tényleges értékek a nem számlázott értékesítési tényleges értékekhez kapcsolódnak, hasonlóan az idő-, költség- és anyaghasználati naplók jóváhagyásakor létrehozott nem számlázott értékesítési tényleges értékekhez.
- A szervezetközi erőforrások által megadott időre létrehozott tételnaplósorok nem eredményezik automatikusan a beszerzési egységköltség **és** az **Interorg sales** típusok tényleges értékét. Ezeket a tényleges adatokat manuálisan kell létrehozni. Ez a viselkedés eltér a szervezetközi erőforrások által rögzített időbejegyzések viselkedésétől. Ebben az esetben az idő jóváhagyásakor az alkalmazás automatikusan létrehozza a Költség **típus tényleges értékét a** projektben, valamint a beszerzési egység költségének **és** az Interorg Sales **típusoknak a** tényleges értékét az alkalmazott tulajdonosi részlegén. Ezután tranzakciós kapcsolatokat használ, hogy összekapcsolja ezeket a tényleges adatokat és a tranzakció eredetét, hogy összekapcsolja őket az eredeti időbevitellel.
- A tételnaplók megerősítésekor tényleges adatokat hoznak létre. A korrekciós naplók azonban nem használhatók a tényleges adatok kijavítására. Ez a viselkedés eltér az idő-, költség- és anyaghasználati naplók jóváhagyásakor létrehozott tényleges adatok viselkedésétől. Ebben az esetben az alkalmazás lehetővé teszi, hogy a Javítási naplók segítségével kijavítsa a tényleges adatokat a hibák kijavításához, feltéve, hogy ezeket a tényleges adatokat még nem számlázták ki. Ha már kiszámlázták őket, akkor is kijavíthat egy tényleges értéket, ha feldolgozza a tényleges teljes jóváírást a vevőnek.

> [!NOTE]
> A bejegyzésnaplók nem kényszerítenek szigorú alapértelmezett szabályokat. Ezért használja ezeket a bejegyzésnaplókat a lehető legkisebb mértékben, és legyen óvatos és körültekintő, hogy ne hozzon létre sérült pénzügyi adatokat a rendszerben. Amikor csak lehet, használja az Idő-, Költség- és Anyaghasználati naplókat, a projektszerződések mérföldkő- és megőrzőbeállítását, valamint a projektszámla-visszaigazolási folyamatot a Tételnaplók helyett a tényleges adatok létrehozásához.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
