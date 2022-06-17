---
title: Bejegyzésnaplók létrehozása és megerősítése
description: Ez a cikk arról nyújt tájékoztatást, hogyan hozhat létre és erősíthet meg bejegyzési naplókat a Microsoftban Dynamics 365 Project Operations.
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
ms.openlocfilehash: 138dccd72607d6515eeeffb066fa485f83eabbec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912335"
---
# <a name="create-and-confirm-entry-journals"></a>Bejegyzésnaplók létrehozása és megerősítése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A bejegyzési naplók segítségével közvetlenül a Microsoftban rögzítheti a tényleges adatokat Dynamics 365 Project Operations. A bejegyzési naplók használatakor nem kell megadnia az idő-, költség- és anyaghasználati naplókat a Project Operationsben.

Egyetlen bejegyzési napló lehetővé teszi több naplósor létrehozását. A napló megerősítésekor a bejegyzési napló sor a következő adatok tényleges adatait rögzíti:

- A költség vagy bevétel a kiválasztott tranzakciótípustól függően.
- A kiválasztott tranzakciós osztály. A rendelkezésre álló osztályok az **Idő, a Költség**, **az Anyag**, **a** Megtartó **,** a Mérföldkő **és** az **Adó**.
- A naplósorban kiválasztott projekt és/vagy tevékenység.

Kövesse az alábbi lépéseket egy bejegyzési napló létrehozásához a Project Operationsben.

1. Lépjen az **Értékesítési** \> **tranzakciók naplói** \> **oldalra.**
2. **A Bejegyzési naplók** listaoldal Műveleti ablaktábláján válassza az Új **lehetőséget** egy napló létrehozásához.
3. **Az Új napló** lap Leírás **mezőjében** adja meg a napló leírását.
4. Győződjön meg arról, hogy a **Napló típusa** mező Bejegyzés **értékre** van állítva, majd válassza a Mentés **lehetőséget**. Az új Bejegyzési napló mentése után a Naplólapon meg kell jelennie egy **Naplósorok** lapnak.
5. **A Naplósorok** lap rács feletti eszköztárán válassza az Új **lehetőséget** egy bejegyzési naplósor létrehozásához.
6. **A Bejegyzési naplósor létrehozásához használt Gyorslétrehozás** párbeszédpanelen állítsa be a mezőket az alábbi táblázatban leírtak szerint.

    | Mező | Description | Funkcionális hatás |
    | --- | --- | --- |
    | Tranzakció osztálya | A naplósor a hat tranzakciós osztály egyikébe sorolható: **Idő**, Költség **,** **Anyag**, **Megtartó**, **Mérföldkő** vagy **Adó**. | Az **Adótranzakció** osztály elavult a Project Operationsben. <br> Ha adótranzakciós **osztályt** hoz létre, azt nem számítja fel a rendszer számlázással, illetve költség- vagy bevételszámítással. **A Milestone** egy csak bevételt biztosító tranzakciós osztály. <br>A **Megtartó** tranzakciós osztály egy vevőtől kapott előleget jelöl. Mindig számlázott értékesítési és nem számlázott értékesítési naplósorok párjaként kell létrehozni. |
    | Tranzakció típusa | A költség rögzítéséhez a **Költség**, **az Interorg Értékesítés** és **az Erőforrásegység költségtranzakciós** típusokat kell használni.<br> A bevétel rögzítéséhez a **Számlázatlan értékesítések** és **a Számlázott értékesítés** tranzakciótípusokat kell használni. | A **Megőrző** tranzakciós osztály csak a Számlázatlan értékesítések **és** a **Számlázott értékesítések** tranzakciótípusokkal működik.<br> A **Mérföldkő** tranzakciós osztály csak a **Számlázott értékesítés** tranzakciótípussal működik. <br>Az **Interorg Sales** and **Resourcing unit cost** transaction típusok csak az **Időtranzakciós** osztályra vonatkoznak, és ezek csak a Lite deployment scneario bejegyzési naplóiban érhetők el, a Project Operations erőforrás/nem készletezett forgatókönyvekben való telepítésekor nem. |
    | Termék kiválasztása | Ha az Anyagtranzakció osztály van kiválasztva, ez a mező lehetővé teszi annak megadását, hogy az anyagtranzakció, amelyhez a naplósort létrehozza, meglévő termék vagy beírt termék.If can the **Material transaction class, this field (Anyagtranzakció**) osztály, ezzel a mezővel megadhatja, hogy az anyagtranzakció, amelyhez a naplósort létrehozza, létező vagy beírt termék-e. | Ha az Írási termék **lehetőséget választja**, megadhatja a termék nevét. |
    | Termék | Hivatkozás a termékre a katalógusból. | |
    | Description | A naplósor leírása, amely megkönnyíti az azonosítást. | A nem számlázott értékesítési naplósorok esetében a rendszer az értéket használja leírásként a számlasor részleteinek létrehozásakor. |
    | Külső leírás | A naplósor leírása, amely a külső érdekelt felekkel való megosztáshoz használható. | A nem számlázott értékesítési naplósorok esetében az érték lesz a külső leírás, amikor a számlasor részletei létrejönnek. A vevőnek küldött számlán is megjelenhet. |
    | Számlázási típus | Egy érték, amely jelzi, hogy a naplósor a projekt díjköteles, ingyenes vagy nem terhelhető összetevőjének számít-e bele. | Egy tipikus folyamatban a számlázási típus a szerződésen beállított, megállapodás szerinti feltételekből származik. Naplósor rögzítésekor azonban értéket is megadhat ebben a mezőben. |
    | Dokumentum kelte | Adjon meg egy dátumot, amikor a tranzakció történt. | |
    | Kezdési dátum | Használja a tranzakció bekövetkezésének dátumát. | Ez a mező összehasonlításra szolgál a számla létrehozásának dátumával a **nem számlázott értékesítés** típusú tranzakciók esetében. Ez az összehasonlítás segít eldönteni, hogy a tranzakció határidős vagy múltbeli dátumú-e. Csak a korábbi dátummal rendelkező tranzakciók kerülnek a számlára. |
    | Befejező dátum | Használja a tranzakció bekövetkezésének dátumát. | |
    | Könyvelési dátum | Használja azt a dátumot, amikor a számviteli hatás rögzítésre kerül. | |
    | Szerződéses vonali ügyfél | Alapértelmezés szerint, ha a szerződéssornak csak egy vevője van, ez a mező a naplósor mentésekor a szerződéssor vevőjére lesz beállítva. Ha a szerződéssornak több vevője van, válassza ki a megfelelő vevőt a szerződéssoron. | Ha a rendszer nem tudja meghatározni a szerződéssor vevőjét a naplósorban, és ha az üres a **naplósorból létrehozott Nem számlázott értékesítés** típus tényleges állapotában, akkor a tényleges nem lesz kiszámlázva. |
    | Project | Válassza ki azt a projektet, amelyen rögzíteni szeretné a tényleges beállítást. | A kiválasztott projekt, tranzakciós osztály és feladat alapján a rendszer megpróbálja meghatározni a szerződést, a szerződéssort és a szerződéssor vevőjét. |
    | Feladatok | Válassza ki azt a feladatot, amelyen rögzíteni szeretné a tényleges beállítást. | Ha a szerződés beállítása során feladatokat társított a szerződéssorokhoz, a rendszer a kiválasztott feladatot, valamint egy projekt- és tranzakcióosztályt fogja használni a szerződés, a szerződéssor és a szerződéssor-vevő meghatározásához. |
    | Tranzakció kategóriája | Válassza ki azt a tranzakciós kategóriát, amellyel rögzíteni szeretné a tényleges értéket. | A költségek esetében a kiválasztott tranzakciós kategória határozza meg azt az alapértelmezett árat, amely a naplósoron lesz megadva a mentéskor. |
    | Beosztás | Ez a mező az Időnapló soraihoz kapcsolódik. Válassza ki annak az erőforrásnak a szerepkörét, aki időt töltött a projekten és/vagy a tevékenységen. | Időnapló-sorok esetén, ha a beépített konfigurációt használja az alapértelmezett erőforrásköltségek és számladíjak beviteléhez, a rendszer a kiválasztott szerepkört az erőforrásegységgel együtt használja a naplósorban a mentéskor a naplósorban megadott alapértelmezett ár meghatározásához. Ha egyéni konfigurációt használ az alapértelmezett árak megadásához, tekintse át ezt a konfigurációt annak megállapításához, hogy a **Szerepkör** mező az alapértelmezett árértékek megadására szolgál-e. |
    | Alvállalkozói szerződés | Ha a naplósor alvállalkozói kapacitást, illetve alvállalkozásba adott költségeket vagy anyagokat képvisel, válassza ki a megfelelő alvállalkozói szerződést. | A költségnapló-sorok rögzítésekor a kiválasztott alvállalkozó határozza meg az alapértelmezett egységköltség megadásához használt árlistát. |
    | Alvállalkozói vonal | Ha a naplósor alvállalkozói kapacitást, illetve alvállalkozásba adott költségeket vagy anyagokat jelöl, válassza ki a megfelelő alvállalkozói sort. | A költségnapló-sorok rögzítésekor a kiválasztott alvállalkozói sor biztosítja, hogy az alvállalkozói sorban rendelkezésre álló kapacitásszámítások helyesen legyenek kiszámítva. |
    | Összegszámítási mód | Alapértelmezés szerint ez a mező a Mennyiség megszorzása árral értékre van **állítva**. Ha ezt a módszert használja, az összeg mennyiségként *×* árként *kerül* kiszámításra. A másik támogatott módszer a **Rögzített ár**. Ha ezt a módszert használja, az ár az összegre lesz beállítva, és a mennyiség nem lesz használva a számításban. | |
    | Egység ütemezése és egysége | Az egység ütemezése és az egység együttesen azonosítja a mennyiség egységét. | Az egység és a tranzakciós kategória kombinációja a költségek alapértelmezett árainak megadására szolgál. A Project Operations alapértelmezett konfigurációjában a rendszer az egység, a szerepkör és az erőforrásegység kombinációját használja az idő alapértelmezett árainak megadásához. Ha egyéni konfigurációval rendelkezik az alapértelmezett árak megadásához, akkor azt az egységgel együtt fogja használni. A termék és az egység kombinációját használják az anyagok alapértelmezett árainak megadására. |
    | Mennyiség | Adja meg a mennyiséget. | |
    | Ár | Ha az ár üresen marad a naplósor létrehozásakor, a rendszer a tranzakciós osztálytól függően a megfelelő értékeket használja az alapértelmezett árak megadásához. Ha a naplósor létrehozásakor meg van adva egy ár, akkor a rendszer ezt az árat használja. | |
    | Adó | Adja meg az adó összegét. | A megadott adóösszegtől függően a kiterjesztett összeg összege *adóként* + *kerül* kiszámításra. |

## <a name="confirm-an-entry-journal"></a>Nevezési napló megerősítése

Miután beírta az összes naplósort egy bejegyzési naplóba, megerősítheti a naplót. Ez a folyamat minden naplósort ténylegesként rögzít a megfelelő projekteken.

A napló megerősítése után már nem szerkesztheti azt vagy annak bármely sorát.

## <a name="actuals-created-by-entry-journal-confirmation"></a>A bejegyzési napló visszaigazolása által létrehozott tényleges adatok

Van néhány fő különbség a bejegyzési napló visszaigazolása által létrehozott tényleges adatok és az idő-, költség- és anyaghasználati naplók jóváhagyása, valamint a projektműveletekben a számla megerősítése során létrehozott tényleges adatok között:

- A bejegyzési naplók nem használnak tranzakciós kapcsolatokat a tényleges költség és a számlázatlan értékesítések tényleges összekapcsolására. Az idő-, költség- és anyaghasználati naplók jóváhagyásakor létrehozott tényleges adatok mindig tranzakciós kapcsolatokat használnak a költség és a nem számlázott értékesítési tényleges adatok összekapcsolásához.
- A bejegyzési naplók nem használnak tranzakciós eredetet a tényleges költség és a nem számlázott értékesítési tényleges adatok bármely származó rekordhoz való kapcsolásához. Az idő-, költség- és anyaghasználati naplók jóváhagyásakor létrehozott tényleges adatok mindig tranzakciós eredetet használnak a költségek és a nem számlázott értékesítési tényleges adatoknak az eredeti időbevitelhez való kapcsolásához.
- Amikor a bejegyzésnapló visszaigazolása által létrehozott, nem számlázott értékesítési tényleges adatokat számlázzák ki, a számlaigazolás során létrehozott számlázott értékesítési tényleges adatok a nem számlázott értékesítési tényleges adatokhoz kapcsolódnak, hasonlóan az idő-, költség- és anyaghasználati naplók jóváhagyásakor létrehozott, nem számlázott értékesítési tényleges adatokhoz.
- A szervezetek közötti erőforrások által megadott időre létrehozott bejegyzési naplósorok nem okozzák az erőforrásegység költségének **és** az Interorg Sales **típusoknak a** tényleges adatait. Ezeket a tényeket manuálisan kell létrehozni. Ez a viselkedés eltér a szervezetek közötti erőforrások által rögzített időbejegyzések viselkedésétől. Ebben az esetben az idő jóváhagyásakor az alkalmazás automatikusan létrehozza a **Költség** típus tényleges adatait a projekten, valamint a Resourcing egységköltség **és** az **Interorg Sales** típusok tényleges adatait az alkalmazott saját részlegén. Ezután tranzakciós kapcsolatokkal kapcsolja össze ezeket a tényleges adatokat és a tranzakciós eredetet, hogy összekapcsolja őket az eredeti időbevitellel.
- Amikor a bejegyzési naplók megerősítést nyernek, tényleges adatokat hoznak létre. A javítási naplók azonban nem használhatók a tényleges adatok kijavítására. Ez a viselkedés eltér az idő-, költség- és anyaghasználati naplók jóváhagyásakor létrehozott tényleges adatok viselkedésétől. Ebben az esetben az alkalmazás lehetővé teszi, hogy javítási naplókat használjon a tényleges adatok kijavításához a hibák kijavításához, feltéve, hogy ezeket a tényleges adatokat még nem számlázták ki. Ha már kiszámlázták őket, akkor is kijavíthatja a tényleges értéket, ha ennek a tényleges jóváírásnak a teljes jóváírását feldolgozza az ügyfélnek.

> [!NOTE]
> A bejegyzési naplók nem érvényesítik a szigorú alapértelmezett szabályokat. Ezért használja ezeket a bejegyzési naplókat a lehető legkevesebbet, és legyen óvatos és körültekintő annak biztosítása érdekében, hogy ne hozzon létre sérült pénzügyi adatokat a rendszerében. Amikor csak teheti, használja az idő-, költség- és anyaghasználati naplókat, a mérföldkő és a megtartó beállítását a projektszerződéseken, valamint a projektszámla-visszaigazolási folyamatot a bejegyzési naplók helyett a tényleges adatok létrehozásához.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
