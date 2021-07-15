---
title: Költségjelentések újragondolva
description: Ez témakör a költségjelentések bejegyzésének átalakított és újragondolt élményét ismerteti.
author: suvaidya
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f8c44f86ff7c00e2d5b927bbe6878be7ab6d7758
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251007"
---
# <a name="expense-reports-reimagined"></a>Költségjelentések újragondolva

A költségjelentés-bejegyzés áttervezésre került, hogy leegyszerűsítse a folyamatot, és lerövidítse a jelentés kitöltéséhez szükséges időt. A kiadások új felhasználói élményének főbb összetevői a következők:

- Új költségkezelési munkaterület, amely lehetővé teszi a delegált kiadások elérését.
- Új bizonylategyeztetési felhasználói élmény, amely jobban mutatja a fejlécszintű bizonylatokat, és egyszerűsíti a bizonylatok költségsorokhoz való csatolásának folyamatát.
- Egy új, írásvédett rács, amely lehetővé teszi még sok további költségsor és egyéb adatoszlop megtekintését. Most már megtekintheti az összes tételezett és felosztott sort, a fölérendelt kiadásokkal együtt.
- Egyszerűsített ablaktábla a kiadások szerkesztéséhez.
- Áttervezett hiba-, figyelmeztető és irányelvüzenetek a probléma megfelelő kontextusának és megértésének biztosítására, valamint a megoldási módjának ismertetésére. Eltávolítottunk számos üzenetet, amelyek azelőtt jelentek meg, hogy a felhasználók a feladataikat végrehajthatták volna, és megoldhatták volna a problémákat.
- Új oldal a kötelező mezők, a választható mezők és a nem szerepeltethető mezők megadásához. Ez az oldal segít csökkenteni a beállítandó mezők számát.
- A költségjelentések új megjelenése, így a jelentések már nem tűnnek úgy, mintha a rendszer a könyveléssel foglalkozó személyek számára készült volna.

Az új élmény bekapcsolásához a **Szolgáltatáskezelés** munkaterületen kapcsolhatja be a **Költségjelentések újragondolva** funkciót. Amikor bekapcsolja ezt a funkciót, a következő műveleteket hajtja végre a rendszer:

- A meglévő költségkezelési munkaterület az új munkaterületre cserélődik.
- A rendszer új, a költség mező láthatóságával kapcsolatos menüelemet vesz fel.
- A rendszer nem távolítja el a költségjelentések (a meglévő oldal) vagy a költségjelentés-mezők meglévő menüelemeit.
- A munkafolyamatok és a jóváhagyások továbbra is a meglévő költségjelentési oldalra irányítják át.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4IQFM]

## <a name="new-features"></a>Új szolgáltatások

| Új szolgáltatás | Ismertetés |
|---|----|
| Kiadás mező láthatósága | Egy új beállítási oldalon megadhatja, hogy mely mezőket kell tiltani egy szervezethez. Azt is megadhatja, hogy mely mezőkre van szükség, és mely mezők ajánlottak. |
| Kötelező mezők | Az új, egyszerű konfiguráció lehetővé teszi, hogy bizonyos mezőket a házirend-keretrendszer használata nélkül is kötelezővé tegyen. |
| Választható mezők | A program egy másik oldalt ad hozzá a választható mezők számára. Így az alkalmazottak nem úgy érzik, mintha be kellene állítaniuk a mezőket, de a mezők továbbra is könnyen elérhetők. |
| Nem csatolt bizonylatok hozzáadása | A nem csatolt bizonylatok költségjelentéshez való hozzáadásának lehetősége jobban látható a munkaterületen és a költségelszámolási jelentésben. |
| Továbbfejlesztett üzenetkezelés | Jobban láthatók a figyelmeztetéseket vagy a hibákat tartalmazó kiadási sorok. |
| Az üzenetek mennyiségének csökkentése az üzenetsávban| Az információs napló üzeneteinek száma csökkent, és erőfeszítéseket tettünk annak megakadályozására, hogy sok esetben duplikált üzenetek jelenjenek meg. |
| Gyakori műveletek csoportosítása | A felület megtisztult az új műveletek gomb hozzáadásával a legtöbb gyakori sorszintű művelethez, valamint egy három pontot tartalmazó gomb (...) hozzáadásával a fejléc és más ritkább műveletek esetében. |
| Új munkaterület a láthatóság növelése érdekében | Az új munkaterület egyesíti azokat a funkciókat és hivatkozásokat, amelyek segítségével a felhasználók különböző területekre léphetnek. |
| A meglévő kiadások és bizonylatok hozzáadása a kiadások létrehozása során | A költségjelentések létrehozásakor felveheti az összes kiadást, illetve kijelölheti a nem kapcsolódó költségeket. A nem kapcsolódó költségek a vállalati hitelkártya hírcsatornából importált, illetve a felhasználó által manuálisan létrehozott, de költségjelentéshez nem csatolt kiadások.|
| Árfolyamkalkulátor | Árfolyamkalkulátor került hozzáadásra, amely lehetővé teszi, hogy kiszámítsa a több pénznemű, saját pénzből fedezett tranzakciók árfolyamát. |
| Új kiadási sorok mentése és hozzáadása | A **Mentés** és az **Új** gombok új kiadások beírása esetén elérhetők, hogy gyorsabban megadhassa a kiadási sorokat. |
| Jobb láthatóság a felosztott és a tételezett sorokban | A tételezett és a felosztott sorok hozzá lettek adva közvetlenül a kiadások listájához, és segítségükkel könnyebben megállapíthatja, hogy vannak-e hibák. |
| Alkategóriák részleteinek megtekintése elemi sorokban | A fölérendelt költség elemi sorai az alkategóriák címkéit mutatják a költségjelentésben, így egy pillantással áttekinthet minden részletet.|
| Bizonylatok megjelenítése a tételezés során | A bizonylatok megjeleníthetők a tételezés. |
| Készpénzelőleg kiválasztása | Jelöljön ki egy vagy több készpénzelőleget egyetlen költségtranzakció teljesítéséhez. |
| Készpénzelőleg egyenlege | Amikor költségbejegyzést hoz létre a jóváhagyott és a kifizetett készpénzelőlegek alapján, valós időben áttekinti a készpénzelőlegek egyenlegét. |

A kezdeti kiadás a költségbejegyzési forgatókönyvekre fókuszál. A költségjelentés áttekintési vagy jóváhagyási forgatókönyve továbbra is a meglévő kiadásbejegyzési oldalt használja.

A következő funkciók nem támogatottak a Költségjelentések újragondolva munkaterületen de a későbbi kiadásokban tervezzük bevezetésüket: 

- Utazási kérelem integrációja
- Napidíj költségbejegyzések
- Ideiglenes jóváhagyói támogatás
- A munkafolyamat-előzmények megtekintésének lehetősége


[!INCLUDE[footer-include](../includes/footer-banner.md)]
