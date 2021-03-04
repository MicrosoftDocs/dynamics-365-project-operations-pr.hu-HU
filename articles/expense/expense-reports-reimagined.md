---
title: Költségjelentések újragondolva
description: Ez a témakör a költségjelentés-bejegyzés újratervezett és újragondolt felhasználói élményére vonatkozó információkat tartalmaz.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 18d7407681906361f3f818225efb8510ac981d98
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122797"
---
# <a name="expense-reports-reimagined"></a>Költségjelentések újragondolva

A költségjelentés-bejegyzés áttervezésre került, hogy leegyszerűsítse a folyamatot, és lerövidítse a jelentés kitöltéséhez szükséges időt. A kiadások új felhasználói élményének főbb összetevői a következők:

- Új költségkezelési munkaterület, amely lehetővé teszi a delegált kiadások elérését.
- Új bizonylategyeztetési felhasználói élmény, amely jobban mutatja a fejlécszintű bizonylatokat, és egyszerűsíti a bizonylatok költségsorokhoz való csatolásának folyamatát.
- Új írásvédett rács, amely több költségsor és további adatoszlopok megtekintését teszi lehetővé. Most már megtekintheti az összes tételezett és felosztott sort, a fölérendelt kiadásokkal együtt.
- Egyszerűsített ablaktábla a kiadások szerkesztéséhez.
- Áttervezett hiba-, figyelmeztető és irányelvüzenetek a probléma megfelelő kontextusának és megértésének biztosítására, valamint a megoldási módjának ismertetésére. Eltávolítottunk számos üzenetet, amelyek azelőtt jelentek meg, hogy a felhasználók a feladataikat végrehajthatták volna, és megoldhatták volna a problémákat.
- Új oldal a kötelező mezők, a választható mezők és a nem szerepeltethető mezők megadásához. Ez az oldal segít csökkenteni a beállítandó mezők számát.
- A költségjelentések új megjelenése, így a jelentések már nem tűnnek úgy, mintha a rendszer a könyveléssel foglalkozó személyek számára készült volna.

Az új felhasználói élmény bekapcsolásához a **Funkciókezelés** munkaterület használatával kapcsolja be a **Költségjelentések újragondolva** funkciót. Amikor bekapcsolja ezt a funkciót, a következő műveleteket hajtja végre a rendszer:

- A meglévő költségkezelési munkaterület az új munkaterületre cserélődik.
- A rendszer új, a költség mező láthatóságával kapcsolatos menüelemet vesz fel.
- A rendszer nem távolítja el a költségjelentések (a meglévő oldal) vagy a költségjelentés-mezők meglévő menüelemeit.
- A munkafolyamatok és a jóváhagyások továbbra is a meglévő költségjelentési oldalra irányítják át.

## <a name="getting-started-video-for-new-users"></a>Kezdeti lépésekkel kapcsolatos videó az új felhasználók számára

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

A [Dynamics 365 for Finance and Operations költségélmény](https://youtu.be/Ocy-MsTvEE0) videó (fent látható) a [Finance and Operations lejátszási listában](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) érhető el a YouTube-on.

## <a name="new-features"></a>Új szolgáltatások

| Új szolgáltatás | Adatfolyam leírása |
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
| Jobb láthatóság a felosztott és a tételezett sorokban | A tételezett és a felosztott sorok hozzá lettek adva közvetlenül a kiadások listájához, és segítségükkel könnyebben megállapíthatja, hogy vannak-e hibák. |
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