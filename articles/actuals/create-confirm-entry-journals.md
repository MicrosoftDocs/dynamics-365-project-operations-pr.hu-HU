---
title: Bejegyzésnaplók létrehozása és megerősítése
description: Ez a cikk az beviteli naplók létrehozásáról és megerősítéséről tartalmaz további információt a Microsoft Dynamics 365 Project Operations alkalmazásban.
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

A beviteli naplók segítségével közvetlenül a Microsoft Dynamics 365 Project Operations alkalmazásba rögzítheti tényadatokat. A Bejegyzés mező használata esetén nem kell idő-, költség- és anyaghasználati naplókat bevinni a Project Operations alkalmazásba.

Egyetlen beviteli naplóval több naplósort is létrehozhat. Amikor a napló meg van erősítve, egy Bejegyzés naplósor rögzíti a tényadatot a következő részletekkel:

- A költség vagy bevétel a kiválasztott tranzakció típusától függően
- A kiválasztott tranzakcióosztály. A rendelkezésre álló osztályok az **Idő**, a **Költség**, az **Anyag**, a **Foglaló**, a **Mérföldkő** és az **Adó** .
- A projekt és/vagy a feladat, amely ki van jelölve a naplósoron.

A következő lépésekkel hozzon létre Beviteli naplót a Project Operations alkalmazásban.

1. Válassza az **Értékesítés** \> **Tranzakciók** \> **Naplók** lehetőséget.
2. A **Beviteli naplók** listaoldalon a Műveletpanelen válassza az **Új** lehetőséget, egy új napló létrehozásához.
3. Az **Új napló** oldal **Leírás** mezőjében adja meg a napló leírását.
4. Győződjön meg róla, hogy a **Napló típusa** mező **Bejegyzés** legyen, majd válassza a **Mentés** lehetőséget. Az új Beviteli napló mentése után a **Naplósorok** lapnak meg kell jelenni a napló oldalon.
5. A **Naplósorok** lapon rács feletti eszköztárán válassza az **Új** lehetőséget egy Beviteli naplósor létrehozásához.
6. A **Gyors létrehozás** párbeszédpanelen, egy Beviteli naplósor létrehozásához , állítsa be a mezőket az alábbi táblázatban leírtak szerint.

    | Mező | Description | Funkcionális hatás |
    | --- | --- | --- |
    | Tranzakció osztálya | A naplósor hat tranzakciós osztály valamelyikébe sorokható: **Idő**, **Költség**, **Anyag**, **Foglaló**, **Mérföldkő** vagy **Adó**. | Az **Adó** tranzakcióosztály elavult a Project Operationsben. <br> Ha létrehoz egy **Adó** tranzakcióosztályt, akkor az nem fog feldolgozásra kerülni számlázás vagy a költség- vagy bevételszámítások során. A **Mérföldkő** csak bevételi tranzakcióosztály. <br>A **Foglaló** tranzakcióosztály az ügyféltől kapott előleget képviseli. Mindig számlázatlan és nem számlázható értékesítési sorok párjaként kell létrehozni. |
    | Tranzakció típusa | A költségek rögzítéséhez a **Költség**, a **Szervezetek közöttu értékesítés** és az **Erőforrás-kezelő részleg költsége** típusok használata szükséges.<br> A **Nem számlázott értékesítés** és **Számlázott értékesítés** tranzakciótípusokat a bevételek rögzítésére kell használni. | A **Foglaló** tranzakcióosztály csak a **Nem számlázott értékesítés** és **Számlázott értékesítés** tranzakciótípusokkal működik.<br> A **Mérföldkő** tranzakció osztály csak a **Számlázott értékesítés** tranzakciótípussal működik. <br>Az **Vállalatközi értékesítés** és az **Erőforrás-kezelő részleg költsége** tranzakciótípusok csak az **Idő** tranzakcióosztályra alkalmazhatók, és ezek csak Lite telepítésben érhetők el a Beviteli naplókhoz, a Project Operations Erőforrás/nem készletezett helyzetekben való telepítésekor nem. |
    | Termék kiválasztása | Az **Anyag** tranzakciós osztály kiválasztásakor ezzel a mezővel megadhatja, hogy az anyagtranzakció, amelyhez létrehozza a naplósort egy meglévő termékhez vagy nem katalogizált termékhez tartozik-e. | Ha a **Nem katalogizált termék** lehetőséget választja, beírhatja a termék nevét. |
    | Termék | Egy hivatkozás a termékre a katalógusból. | |
    | Description | A naplósor leírása a könnyebb azonosíthatóságot segíti. | A nem számlázott értékesítésinapló-soroknál az érték lesz a leírás a számlasor részleteinek létrehozásakor a leíráshoz. |
    | Külső leírás | A naplósor leírása, amely külső résztvevőkkel való megosztásra használható. | A nem számlázott értékesítésinapló-soroknál az érték lesz a külső leírás a számlasor részleteinek létrehozásakor. Ez megjelenhet az ügyfélnek küldött számlán is. |
    | Számlázási típus | Ez az érték jelzi, hogy a projektben felszámolható, kiegészítő vagy nem felszámolható összetevőnek számít-e. | Egy általános folyamatban számlázás típusa jellemzően a szerződésben meghatározott feltételekből származik. Ennek a mezőnek a értékét azonban a naplósor rögzítése során beírhatja. |
    | Dokumentum kelte | Dátum használata tranzakció bekövetkezésekor. | |
    | Kezdési dátum | A dátum használata tranzakció bekövetkezésekor. | Ez a mező a **Nem számlázott értékesítés** típusú tranzakciók a számlakészítési dátumával összehasonlításra használatos. Ez az összehasonlítás segít eldönteni, hogy a tranzakció jövőbeli vagy múltbeli-e. A számlához csak a korábbi dátumú tranzakciók lesznek hozzáadva. |
    | Befejező dátum | A dátum használata tranzakció bekövetkezésekor. | |
    | Könyvelési dátum | A könyvelési hatás rögzítésének dátumát használja. | |
    | Szerződéssor ügyfele | Alapértelmezésben, ha a szerződéssornak csak egy ügyfele van, akkor ez a mező a szerződéssoron a szerződéssor mentésekor beállított szerződéssor ügyfélre lesz beállítva. Ha a szerződéssorhoz több ügyfél tartozik, válassza ki a megfelelő ügyfelet a szerződéssoron. | Ha a rendszer nem tudja meghatározni a szerződéssor ügyfelét a naplósorban, és ha ez üres a naplósorból létrehozott **Nem számlázott értékesítés** típus tényadatában, akkor a tényadat nem lesz számlázva. |
    | Project | Válassza ki azt a projektet, amelyhez a tényadat rögzítve lesz. | A rendszer a kijelölt projekt, tranzakció osztály és feladat alapján megpróbálja meghatározni a szerződést, a szerződéssort és a szerződéssor ügyfelét. |
    | Feladatok | Válassza ki azt a feladatot, amelyhez a tényadat rögzítve lesz. | Ha a szerződés beállítása során szerződéssorokhoz társított feladatokat, akkor a rendszer a kijelölt feladatot a projekt- és a tranzakcióosztállyal együttesen fogja használni a szerződés, a szerződéssor és a szerződéssor ügyfelének meghatározásához. |
    | Tranzakció kategóriája | Válassza ki azt a tranzakciókategóriát, amelyhez a tényadat rögzítve lesz. | Kiadások esetén a kiválasztott tranzakciókategória határozza meg az alapértelmezett árat, amely mentéskor meg lesz adva a naplósorba. |
    | Beosztás | Ez a mező az Idő naplósorok szempontjából releváns. Jelölje ki annak az erőforrásnak a szerepkörét, aki időt töltött a projekten és/vagy feladaton. | Az Idő naplósorok esetén, amennyiben az alapértelmezett erőforrásköltségek és számlázási árfolyamok beviteléhez a gyári konfigurációt használja, a kijelölt szerepkör a beszerzési egységgel együttesen határozza meg a naplósor mentésekor beírt alapértelmezett árat. Ha egyéni konfigurációt használ az alapértelmezett árak bevitelére, akkor az ilyen konfigurációt ellenőriznie kell, annak meghatározására, hogy a **Szerepkör** mező használatos-e az alapértelmezett árértékek megadásához. |
    | Alvállalkozói szerződés | Ha a naplósor az alvállalkozói kapacitást jelenti, illetve az alvállalkozói kiadásokat vagy anyagokat válassza ki a megfelelő alvállalkozói szerződést. | A Költség naplósorok rögzítésekor a kijelölt alvállalkozói szerződés határozza meg az alapértelmezett egységköltség beviteléhez használt árlistát. |
    | Alvállalkozóiszerződés-sor | Ha a naplósor az alvállalkozói kapacitást jelenti, illetve az alvállalkozói kiadásokat vagy anyagokat válassza ki a megfelelő alvállalkozói szerződéssort. | Költség naplósorok rögzítésekor a kijelölt alvállalkozói sor gondoskodik arról, hogy az alvállalkozói sorban helyesen legyenek kiszámítva a rendelkezésre álló kapacitásszámítások. |
    | Összegszámítási mód | A mező értéke **A mennyiség és az ár összeszorzása** alapértelmezés szerint. Ennek a módszernek a használata esetén az összeget a rendszer *Mennyiség* × *Ár* képlettel számítja ki. A másik támogatott módszer a **Rögzített ár**. Ennek a módszernek a használata esetén az ár az összegre lesz beállítva, és a mennyiség nem lesz felhasználva a számításban. | |
    | Egységütemezés és egység | Az egység ütemezése és az egység együttesen határozza meg a mennyiség egységét. | Az egység és a tranzakciókategória kombinációja használatos az alapértelmezett árak beviteléhez a kiadásokhoz. A Project Operations alapértelmezett konfigurációjában az egység, a szerepkör és a beszerzési egység kombinációja használatos az alapértelmezett ár megadásához az időhöz. Ha egyéni konfigurációja van az alapértelmezett árak beviteléhez, az egységgel együtt lesz használva. A termék és az egység kombinációja használatos az anyagok alapértelmezett árának megadásához. |
    | Mennyiség | Adja meg a mennyiséget. | |
    | Ár | Ha az ár üresen marad a naplósor létrehozásakor, a rendszer a megfelelő értékeket használja az alapértelmezett árak megadására a tranzakcióosztálytól függően. Ha a naplósor létrehozásakor megadnak árat, akkor ez az ár lesz használva. | |
    | Adó | Adja az esetleges adóösszeget. | A megadott adóösszegétől függően a kiterjesztett összeg az *Összeg* + *Adó* képlettel lesz kiszámítva. |

## <a name="confirm-an-entry-journal"></a>Egy Beviteli napló megerősítése

Miután megadta az összes naplósort egy Beviteli naplóban, megerősítheti a naplót. Ez a folyamat a megfelelő projektekben tényadatként rögzíti az egyes sorokat.

A napló megerősítése után, már nem szerkesztheti egyik sorát sem.

## <a name="actuals-created-by-entry-journal-confirmation"></a>A Beviteli napló megerősítése után létrehozott tényadatok

Van néhány fontos különbség a Beviteli naplóval létrehozott tényadatok és az Idő, Költség és Anyaghasználati naplók jóváhagyása során, illetve a Project Operations számla jóváhagyása létrehozott tényadatok között:

- A Beviteli naplók nem tranzakciós kapcsolatok használatával kapcsolják össze a tényleges költségeket és a nemszámlázott tényleges értékesítéseket. Az Idő, Költség és Anyaghasználati naplók jóváhagyásakor létrehozott tényadatok, amelye jóvá vannak hagyva, mindig tranzakciókapcsolatokat használnak a költségek és számlázatlan értékestések tényadatainak társításához.
- A Beviteli naplók nem tranzakcióseredet használatával kapcsolják össze a tényleges költségeket és a nem számlázott tényleges értékesítéseket bármely eredetrekordhoz. Az Idő, Költség és Anyaghasználati naplók jóváhagyásakor létrehozott tényadatok, amelye jóvá vannak hagyva, mindig tranzakcióeredeteket használnak a költségek és számlázatlan értékesítések tényadatainak társításához a kiinduló időbejegyzéshez.
- A Beviteli naplóval létrehozott, nem számlázott tényleges értékesítések számlázásakor a számla jóváhagyása során létrehozott számlázott tényleges értékesítéseket a rendszer a nem számlázott tényleges értékesítésekkel, hasonlóan az Idő, a Költség és az Anyaghasználati naplók jóváhagyásakor létrehozott, nem számlázatlan tényleges értékesítésekhez.
- A beviteli naplósorok, amelyek ahhoz az időponthoz jönnek létre, amelyet a szervezetközi erőforrások adnak meg nem okozzák az **Erőforrás-kezelő részleg költsége** és **Szervezetközi értékesítések** típusú tényadatok automatikus létrehozását. Ezeket a tényadatokat manuálisan kell létrehozni. Ez a viselkedés különbözik a szervezetközi erőforrások által rögzített időbejegyzések viselkedésmódjatól. Ebben az esetben az idő jóváhagyásakor az alkalmazás automatikusan létrehozza a **Költség** típusú tényadatokat a projekten, valamint a **Erőforrás-kezelő részleg költsége** és **Szervezetközi értékesítések** típusú tényadatokat az alkalmazott saját részlegében. Ezután a tranzakciókapcsolatok segítségével ezeket a tényadatokat, illetve a tranzakció eredetét összekapcsolja az eredet időbejegyzéssel.
- A Beviteli naplók a megerősítéskor tényadatokat hoznak létre. Az ilyen tényadatok javításához azonban nem használhatók Helyesbítési naplók. Ez a viselkedés különbözik az idő-, költség- és anyaghasználati naplók jóváhagyásakor létrehozott tényadatok viselkedésmódjatól. Ebben az esetben az alkalmazás lehetővé teszi a Helyesbítési naplók segítségével a tényadatok javítását az esetleges hibák kijavítása érdekében, feltéve, hogy az ezeket a tényadatokat még nem számlázták. Ha már számlázva lettek, akkor is javíthat tényadatot, ha a tényadat teljes jóváírását feldolgozza az ügyfélhez.

> [!NOTE]
> A Bevitelin naplók nem írnak elő szigorú alapértelmezési szabályokat. Ezért a lehető legkevesebbet használja a Beviteli naplókat , és a lehető legnagyobb körültekintéssel járjon el, és ügyeljen arra, hogy ne hozzon létre helytelen pénzügyi adatokat a rendszerben. Amikor csak lehetséges, használja az Idő, a Költség és az Anyaghasználati naplóikat, a projektszerződések mérföldkő- és foglalóbeállításait, illetve a tényadatok létrehozásához a Beviteli naplók helyett a projektszámla megerősítési folyamatát.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
