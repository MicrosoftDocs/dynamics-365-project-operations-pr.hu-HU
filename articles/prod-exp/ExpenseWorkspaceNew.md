---
title: Átdolgozott költségjelentések
description: Ez a témakör a költségjelentés-bejegyzés újratervezett és újragondolt felhasználói élményére vonatkozó információkat tartalmaz.
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 7533f8aca317bd8d72e437592b5251fd3a866ba6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271986"
---
# <a name="redesigned-expense-reports"></a>Átdolgozott költségjelentések

A költségjelentés bevitele áttervezésre került, hogy egyszerűbbé tegye a költségjelentések elkészítésének folyamatát, és csökkentse a költségjelentés végrehajtásához szükséges időt. A kiadások új felhasználói élményének főbb összetevői a következők:

- Új költségkezelési munkaterület, amely lehetővé teszi a delegált kiadások elérését.
- Új bizonylategyeztetési felhasználói élmény, amely jobban mutatja a fejlécszintű bizonylatokat, és egyszerűsíti a bizonylatok költségsorokhoz való csatolásának folyamatát.
- Új írásvédett rács, amely több költségsor és további adatoszlopok megtekintését teszi lehetővé. Most már megtekintheti az összes tételezett és felosztott sort, a fölérendelt kiadásokkal együtt.
- Egyszerűsített ablaktábla a kiadások szerkesztéséhez.
- Áttervezett hiba-, figyelmeztető és irányelvüzenetek segítenek biztosítani a probléma megfelelő kontextusát és megértésének biztosítására, valamint a megoldási módjának ismertetésére. A Microsoft számos olyan üzenetet eltávolított, amelyek már azelőtt megjelentek, hogy a felhasználók elvégezhették volna a feladataikat, és foglalkozhattak volna a problémákkal, például a hiányos tételesítés üzenetet.
- Új lap, amelyen meghatározható hogy mely mezők szükségesek a szervezetnél, mely mezők nem kötelezőek, és mely mezők ne legyenek rögzítve. Ez az oldal segít csökkenteni a felhasználók által beállítandó mezők számát.
- A költségjelentések új megjelenése, így a jelentések már nem tűnnek úgy, mintha a rendszer a könyveléssel foglalkozó személyek számára készült volna.

Az új felhasználói élmény bekapcsolásához a **Funkciókezelés** munkaterület használatával kapcsolja be a **Költségjelentések újragondolva** funkciót. Amikor bekapcsolja ezt a funkciót, a következő műveleteket hajtja végre a rendszer:

- A meglévő költségkezelési munkaterület az új munkaterületre cserélődik.
- A rendszer új, a költség mező láthatóságával kapcsolatos menüelemet vesz fel.
- A rendszer nem távolítja el a költségjelentések (a meglévő oldal) vagy a költségjelentés-mezők meglévő menüelemeit.
- A munkafolyamatok és a jóváhagyások továbbra is a meglévő költségjelentési oldalra irányítják át.

## <a name="new-features"></a>Új szolgáltatások

| Új szolgáltatás | Ismertetés |
|---|----|
| Kiadás mező láthatósága | Az új beállítási oldalon megadhatja, hogy a szervezetre vonatkozóan mely mezők legyenek letiltva, és mely mezőkre van szükség, és mely mezők ajánlottak. |
| Kötelező mezők | Az új, egyszerű konfiguráció lehetővé teszi, hogy bizonyos mezőket a házirend-keretrendszer használata nélkül is kötelezővé tegyen. |
| Választható mezők | A program egy másik oldalt ad hozzá a választható mezők számára. Így az alkalmazottak nem úgy érzik, mintha be kellene állítaniuk a mezőket, de a mezők továbbra is könnyen elérhetők. |
| Nem csatolt bizonylatok hozzáadása | A nem csatolt bizonylatok költségjelentéshez való hozzáadásának lehetősége jobban látható a munkaterületen és a költségelszámolási jelentésben. |
| Továbbfejlesztett üzenetkezelés | Jobban láthatók a figyelmeztetéseket vagy a hibákat tartalmazó kiadási sorok. |
| Az üzenetek mennyiségének csökkentése az üzenetsávban| Az információs napló üzeneteinek száma csökkent, és erőfeszítéseket tettünk annak megakadályozására, hogy sok esetben duplikált üzenetek jelenjenek meg. |
| Gyakori műveletek csoportosítása | A felület megtisztult az új műveletek gomb hozzáadásával a legtöbb gyakori sorszintű művelethez, valamint egy három pontot tartalmazó gomb (...) hozzáadásával a fejléc és más ritkább műveletek esetében. |
| Új munkaterület a láthatóság növelése érdekében | Az új munkaterület egyesíti azokat a funkciókat és hivatkozásokat, amelyek segítségével a felhasználók különböző területekre léphetnek. |
| A meglévő kiadások és bizonylatok hozzáadása a kiadások létrehozása során | A költségjelentés létrehozásakor az összes vagy a kijelölt kiadásokat és bizonylatokat is hozzáadhatja. |
| Árfolyamkalkulátor | Árfolyamkalkulátor került hozzáadásra, amely lehetővé teszi, hogy kiszámítsa a több pénznemű, saját pénzből fedezett tranzakciók árfolyamát. |
| Új kiadási sorok mentése és hozzáadása | A **Mentés** és az **Új** gombok új kiadások beírása esetén elérhetők, hogy gyorsabban megadhassa a kiadási sorokat. |
| Jobb láthatóság a felosztott és a tételezett sorokban | A tételezett és a felosztott sorok hozzá lettek adva közvetlenül a kiadások listájához, és segítségükkel könnyebben megállapíthatja, hogy vannak szabályhibák vagy más hibák. |
| Bizonylatok megjelenítése a tételezés során | A bizonylatok megjeleníthetők a tételezés. |

A kezdeti kiadás a költségbejegyzési forgatókönyvekre fókuszál. A költségjelentés áttekintési vagy jóváhagyási forgatókönyve továbbra is a meglévő kiadásbejegyzési oldalt használja.

A következő funkciók megtalálhatók a meglévő oldalon, de még nincsenek jelen az új oldalon. A következő kiadások során újra bevezetésre kerülnek ezek a funkciók:

- Jóváhagyások
- A kötelezettségek jóváhagyása és a könyvelés módosításának képessége
- Több beviteli pont
- Utazási kérelem integrációja
- Adatentitás a kiadás mező láthatóságához
- A napidíjhoz kapcsolódó kiadások bejegyzése
- Sorszintű munkafolyamat
- Ideiglenes jóváhagyói támogatás
- Speciális tételesítés


[!INCLUDE[footer-include](../includes/footer-banner.md)]