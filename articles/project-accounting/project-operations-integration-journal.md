---
title: A Project Operations integrációs naplója
description: Ez a cikk a Project Operations integrációs naplójának használatáról nyújt tájékoztatást.
author: sigitac
ms.date: 09/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e947fe895a1caa9c9ea092597957a859cd8d61c9
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541080"
---
# <a name="integration-journal-in-project-operations"></a>A Project Operations integrációs naplója

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Az idő-, költség- és anyagbejegyzések **Tényadat** tranzakciókat hoznak létre, amelyek a projekttel kapcsolatban befejezett tevékenységek működési nézetét jelentik. A Dynamics 365 Project Operations a könyvelők számára eszközt biztosít a tranzakciók felülvizsgálatára, és szükség esetén a számviteli attribútumok módosítására. A felülvizsgálat és a helyesbítések befejeződése után a tranzakciókat a projekt részfőkönyvébe és a főkönyvbe könyveli a rendszer. A könyvelő ezeket a tevékenységeket a **Project Operations-integráció** naplójával hajtja végre(**Dynamics 365 Finance** > **Projektmenedzsment és könyvelés** > **Naplók** > **Project Operations-integrációs** napló).

![Integrációs napló folyamata.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Rekordok létrehozása a Project Operations integrációs naplójában

A Project Operations integrációs napló rekordjai az **Importálás az előkészítési táblából** időszakos folyamat segítségével jönnek létre. A folyamat futtatásához nyissa meg a **Dynamics 365 Finance** > **Projektmenedzsment és Könyvelés** > **Időszakos** > **Project Operations-integráció** > **Importálás az előkészítési táblából** menüpontot. A folyamatot interaktív módon futtathatja, illetve beállíthatja, hogy a folyamat szükség szerint a háttérben fusson.

Az időszakos folyamat futtatásakor a rendszer megkeresi a Project Operations integrációs naplóhoz még nem hozzáadott összes tényleges adatot. Minden egyes tényleges tranzakcióhoz létrejön egy naplósor.
A rendszer a naplósorokat külön naplókba csoportosítja az **Időszakegység a Project Operations integrációs naplóban** mezőben kiválasztott érték alapján (**Finance** > **Projektmenedzsment és könyvelés** > **Beállítások** > **Projektmenedzsment és könyvelési paraméterek**, **Project Operations a Dynamics 365 Customer engagement alkalmazásban** lap). A mező lehetséges értékei a következők:

  - **Napok**: A tényadatok a tranzakció dátuma szerint vannak csoportosítva. Minden naphoz külön napló jön létre.
  - **Hónapok**: a tényleges adatok naptári hónap szerint vannak csoportosítva. Minden hónaphoz külön napló jön létre.
  - **Évek**: a tényleges adatok naptári év szerint vannak csoportosítva. Minden évhez külön napló jön létre.
  - **Összes**: az összes tényleges tranzakció ugyanabban az integrációs naplóban szerepel. Ha a napló nem érhető el az időszakos folyamat futtatásakor, például akkor, ha a napló a tranzakciók elszámolási folyamatában van, akkor létrejön egy új napló.

A naplósorok a Projektadatok alapján jönnek létre. A következő felsorolás tartalmazza a fontosabb alapértelmezett és átalakítási szabályok némelyikét:

  - Minden projekttényadat-tranzakcióhoz tartozik egy sor a Project Operations integrációs naplóban. Az idő- és anyagelszámolású számlázási típusokhoz tartozó költség és nem számlázott értékesítési tranzakciók külön sorokban jelennek meg.
  - A **dátum** mező a tranzakció dátumát jelöli. A **Könyvelési dátum** mező a tranzakció főkönyvbe történő rögzítésének dátumát jelenti. Ha a számlázási dátum egy [lezárt pénzügyi időszak](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) alatt van , és be van állítva a **Könyvelési dátum automatikus beállítása nyitott főkönyvi időszakra** paraméter a **Projekmenedzsment és könyvelési paraméterek** oldal **Pénzügyi** lapján, akkor a rendszer a tranzakció könyvelési dátumát módosítja a következő nyitott főkönyvi időszak első dátumára.
  - A **bizonylat** mező az összes tényleges tranzakcióhoz tartozó bizonylatszámot jeleníti meg. A bizonylatszám-sorozatot a **Számsorozatok** lapon, a **projektmenedzsment és a könyvelési paraméterek** lapon lehet megadni. Az egyes sorokhoz új szám tartozik. A bizonylat feladása után megtekintheti, hogyan kapcsolódik a költség és a nem számlázott értékesítési tranzakció a **kapcsolódó bizonylatok** kiválasztásával a **bizonylattranzakció** lapon.
  - A **Kategória** mező a kapcsolódó projekt tényadatainak tranzakciós kategóriája alapján egy projekttranzakciót és alapértelmezett értékeket jelent.
    - Ha a **tranzakció kategóriája** meg van adva a projekt tényadataiban és egy kapcsolódó **projektkategória** létezik egy adott jogi entitásban, akkor a kategória alapértelmezés szerint ebbe a kategóriába tartozik.
    - Ha a **Tranzakcióskategória** nincs beállítva a projekt tényadatában, a rendszer a **Projektkategória alapértelmezései** mezőben szereplő értéket használja a **Project Operations a Dynamics 365 Customer engagement alkalmazásban** lapon a **Projektmenedzsment és könyvelési paraméterek** oldalon.
  - Az **erőforrás** mező a tranzakcióhoz kapcsolódó projekterőforrást jelenti. Az erőforrás hivatkozásként szolgál az ügyfeleknek szóló projektszámla-ajánlatokhoz.
  - Az **Árfolyam mező** alapértelmezett értéke a **Devizaárfolyam értékéből** származik a Dynamics 365 Finance-ból. Ha az átváltási árfolyam beállítása hiányzik, akkor az **Importálás az előkészítésből** időszakos folyamat nem veszi fel a rekordot egy naplóba, és egy hibaüzenet jelenik meg a feladat végrehajtási naplójában.
  - A **Sortulajdonság** mező a projekt tényleges adatokban szereplő számlázási típust jelöli. A sortulajdonság és a számlázási típus leképezése a **Project Operations a Dynamics 365 Customer engagement alkalmazásban** lapon, a **Projektmenedzsment és könyvelési paraméterek** oldalon van meghatározva.

A Project Operations integrációsnapló-soraiban csak a következő számlázási attribútumok frissíthetők:

- **Számlázási áfacsoport** és a **Számlázási cikk áfacsoportja**
- **Pénzügyi dimenziók** (az **összegek elosztása** művelet használatával)

Az integrációs naplósorok nem törölhetők. Ugyanakkor a feladatlan sorokat a rendszer ismét beszúrja a naplóba, miután újra futtatja az **Importálás az előkészítésből** időszakos folyamatot.

### <a name="post-the-project-operations-integration-journal"></a>A Project Operations integrációs naplójának feladása

Az integrációs napló feladásakor létrejön egy projektrészfőkönyv és főkönyvi tranzakciók. Ezeket használják a lefelé irányuló ügyfélszámlázás során, a bevétel elszámolása és a pénzügyi jelentéskészítés során.

A kiválasztott Project Operations integrációs napló a Project Operations integrációs napló oldal **Feladás** menüpontjával adható fel. Minden napló automatikusan feladható az **Időszakos** > **Project Operations integráció** > **Project Operations intergációs napló feladása** helyen található folyamat feladásával.

A feladás interaktív módon vagy kötegben is elvégezhető. Ne feledje, hogy a 100 sornál több sort tartalmazó naplók automatikusan kötegelve lesznek feladva. A jobbteljesítmény érdekében, amikor a naplóknak sok sora van feladva egy kötegben, engedélyezze a **Project Operations integrációs naplók feladása több kötegelt feladatban** funkciót a **Funkciókezelés** munkaterületen. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>A közzétételi hibával rendelkező összes sor átvitele új naplóba

> [!NOTE]
> A funkció használatához engedélyezze az **Összes közzétételi hibával rendelkező sorok átvitele egy új Project Operations integrációs naplóba** funkciót a **Szolgáltatáskezelés** munkaterületen.

Ez a funkció segíti a Project Operations integrációjának élményét. Engedélyezésekor a kettős írási időzítési problémái és a beállítási problémák a továbbiakban nem akadályozzák az érvényes naplók feladását. A rendszer a Project Operations integrációs napló feladása során a napló minden sorát ellenőrzi. A hibát nem tartalmazó összes sort feladja, és létrehoz egy új naplót az összes közétételi hibával rendelkező sorhoz.

A feladási hibás sorokat tartalmazó naplók áttekintéséhez menjen a **Projektmenedzsment és a könyvelés** \> **Naplók** \> **Project Operations integrációs napló** lapra, és szűrje a naplók listáját az **Eredeti napló** mező segítségével. Az alábbi ábrán egy példa látható, ahol a **Project Operations integrációs napló** oldalon található naplók ilyen módon szűrve lettek.

![Ez eredeti napló látható a Project Operations integrációs napló oldalon.](./media/transferLines-originalJournal.png)

Ha egy rendszeres kötegfájl-feladat az integrációs napló feladására van beállítva, akkor a feladást a rendszer újra megkísérli, és a naplók fel lesznek adva, ha az időzítési probléma javítva lett. A fennmaradó adatokat manuálisan meg kell vizsgálni a naplók ellenőrzésével, és el kell végezni a megfelelő műveleteket.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
