---
title: Foglaláselosztási módszerek a Project Service Automation alkalmazásban
description: Ez a témakör információkat nyújt a beosztás lefoglalásának különféle módjairól.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: a770a51c2bf05e227367efc834dbff2832a316f617ae4fe22a43572940f43cbe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000849"
---
# <a name="booking-allocation-methods-in-project-service-automation"></a>Foglaláselosztási módszerek a Project Service Automation alkalmazásban

[!include [banner](../includes/psa-now-project-operations.md)]

Függetlenül attól, hogy közvetlenül ad hozzá egy csapattagot egy projekthez a **Csapat** lapon, vagy bejegyez egy erőforrást az Ütemezés tábla egy projektjéhez vagy követelményéhez, többféle beosztásfoglalási módszer áll rendelkezésre. Ez a témakör ismerteti az egyes módszerek működését, és azt, hogy mely módszerek vezethetnek az erőforrások túlfoglalásához.

## <a name="full-capacity"></a>Teljes kapacitás 
A teljes kapacitás módszer az erőforrás teljes kapacitását foglalja le a megadott kezdő és befejező dátum között. Ha például egy erőforrás a naptárja szerint napi nyolc órát dolgozik heti öt nap, akkor az öt munkanapot felölelő kezdő és befejező dátum 40 órára fogja lefoglalni az erőforrást. A foglalás az erőforrás fennmaradó kapacitására való tekintet nélkül történik. Ha egy erőforrást már más projektekre foglaltak le az adott időszakban, a 40 óra további órákként lesz elkönyvelve, ami túlfoglalást eredményez.

## <a name="remaining-capacity"></a>Fennmaradó kapacitás
A fennmaradó kapacitás módszer csak akkor érhető el, ha közvetlenül végez foglalást egy projekthez az Ütemezés táblán. Ez a módszer az erőforrást rendelkezésre álló kapacitását a megadott dátumtartományban foglalja le. Ha például egy erőforrás kapacitása hetente 40 óra, és ebből már lefoglaltak 10 órát, akkor ugyanazon a héten történő foglalás a fennmaradó 30 óra lefoglalását jelenti.

## <a name="percentage-capacity"></a>Kapacitás százalékos értéke
A Százalékos kapacitási módszer az erőforrást a kapacitás százalékában foglalja le a megadott kezdő és befejező dátum között. Ha például egy erőforrás a naptárja szerint napi nyolc órát dolgozik heti öt nap, akkor az öt munkanapot 50%-os kapacitással felölelő kezdő és befejező dátum 20 órára fogja lefoglalni az erőforrást. Az egyes napi foglalások egyenlően oszlanak meg az időszakban, ebben a példában napi négy órában. A foglalás az erőforrás fennmaradó kapacitására való tekintet nélkül történik. Ha egy erőforrást már más projektekre foglaltak le abban az időszakban, a 20 óra további órákként lesz elkönyvelve, ami túlfoglalást eredményez.

## <a name="evenly-distribute-hours"></a>Órák egyenlő felosztása
Az egyenlően elosztott órák módszer az erőforrást a kapacitás meghatározott óraszámban foglalja le napi szinten a megadott kezdő és befejező dátum között. Például, ha egy erőforrást egy öt napos időszakban 20 órára foglalja le, akkor ez a módszer egyenletesen osztja el a 20 órát napi négy órára. A foglalás az erőforrás fennmaradó kapacitására való tekintet nélkül történik. Ha egy erőforrást már más projektekre foglaltak le abban az időszakban, a 20 óra további órákként lesz elkönyvelve, ami túlfoglalást eredményez.

## <a name="front-load-hours"></a>Órák minél gyorsabb felhasználása
Az előre ütemezett órák módszer az erőforrást a kapacitás meghatározott óraszámban, előre ütemezve foglalja le napi szinten a megadott kezdő és befejező dátum között. Az órák minél gyorsabb felhasználása az erőforrás rendelkezésre álló kapacitását „amint rendelkezésre áll, azonnal felhasználásra kerül” elven használ fel. Például, ha egy erőforrás munkaütemezése napi nyolc óra heti öt nap, és nincsenek aktuális foglalásai, akkor az erőforrás öt munkanapon keresztül történő 20 órás foglalása a következő napi foglalási mintát eredményezi: 

|         Foglalások          |    1. nap    |    2. nap    |    3. nap    |    4. nap    |    5. nap    |    Összeg    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    Meglévő foglalások    |    0        |    0        |    0        |    0        |    0        |    0        |
|    Új foglalás          |    8        |    8        |    4        |    0        |    0        |    20       |

Az órák minél gyorsabb felhasználása módszer figyelembe veszi a meglévő foglalásokat és a rendelkezésre álló kapacitást. Például ha ugyanaz az erőforrás már rendelkezik a munkahétre 20 óra foglalással, az új foglalások az alábbiak szerint foglalják le a fennmaradó kapacitást:

|   Foglalások          | 1. nap | 2. nap | 3. nap | 4. nap | 5. nap | Összeg |
|---------------------|-------|-------|-------|-------|-------|-------|
| Meglévő foglalások | 8     | 8     | 4     | 0     | 0     | 20    |
| Új foglalás       | 0     | 0     | 4     | 8     | 8     | 20    |

Mivel a rendelkezésre álló kapacitás számít, hibaüzenet jelenhet meg, ha az erőforrásnak nincs fennmaradó kapacitása, amit a foglalás le tudna foglalni. Ezzel a módszerrel nem lehetséges túlfoglalás.

## <a name="none"></a>Nincs
A Nincs módszer csak akkor érhető el, ha egy projekten belül a **Csapat** lapról végzi a foglalást. A módszer az erőforrást hozzáadja a projekthez csoporttagként, de nem hoz létre a foglalásokat, amelyek felveszik az erőforrás kapacitását. Ezt a módszert használják, amikor a projekt létrehozásakor az alapértelmezett projektvezető csoporttagot hozzáadják. A projektet létrehozó projektvezető felhasználó alapértelmezés szerint hozzáadásra kerül a projekthez, hogy a projekt entitásbejegyzésének legyen tulajdonosa, és legyen a projektben egy jóváhagyó. Mivel ennek a felhasználónak nincs foglalása, ha le akarja foglalni az erőforrást, akkor törölheti, majd újra hozzáadhatja azt egy másik beosztási módszer használatával, vagy hozzáadhatja az erőforrást feladatokhoz, majd az **Egyeztetés** lap **Foglalások meghosszabbítása** lehetőségének használatával hozhat létre foglalásokat a hozzárendelésekhez.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Túlfoglaláshoz vezető hozzárendelési módszerek
Összesítve, a hozzárendelés következő módjai vezethetnek túlfoglaláshoz, ha az erőforrás már kötelezettségekkel rendelkezik más projektekben (vagy más munkarendelésekban vagy ütemezhető entitásokban):

- Teljes kapacitás
- Kapacitás százalékos értéke
- Órák egyenlő felosztása

Ezen három hozzárendelési módszerek valamelyikének használatakor nem kap értesítést, hogy az erőforrás túlfoglalt. A túlfoglalás kijavításához az Ütemezés táblát kell használnia.


[!INCLUDE[footer-include](../includes/footer-banner.md)]