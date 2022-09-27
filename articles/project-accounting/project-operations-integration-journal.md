---
title: A Project Operations integrációs naplója
description: Ez a cikk az integrációs naplóval való munkáról nyújt tájékoztatást a Project Operationsben.
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

Az idő-, költség-, díj- és anyagbevitelek tényleges **tranzakciókat hoznak létre**, amelyek a projekttel szemben befejezett munka működési nézetét képviselik. A Dynamics 365 Project Operations a könyvelők számára eszközt biztosít a tranzakciók felülvizsgálatára, és szükség esetén a számviteli attribútumok módosítására. A felülvizsgálat és a helyesbítések befejeződése után a tranzakciókat a projekt részfőkönyvébe és a főkönyvbe könyveli a rendszer. A könyvelő ezeket a tevékenységeket a **Project Operations Integration** journal (**Dynamics 365 Finance** > **Project management and accounting** > **Journals** > **Project Operations Integration journal) segítségével végezheti** el.

![Integrációs napló folyamata.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Rekordok létrehozása a Project Operations integrációs naplójában

A Project Operations integrációs napló rekordjai az **Importálás az előkészítési táblából** időszakos folyamat segítségével jönnek létre. Ezt a folyamatot úgy futtathatja, hogy **megnyitja Dynamics 365 Finance** > **Project management and accounting Periodic Project Operations Integration Import from staging table (Projektkezelés és könyvelés** > **időszakos projektműveletek** > **integrációja** > **) integrációs táblázatot**. A folyamatot interaktív módon futtathatja, illetve beállíthatja, hogy a folyamat szükség szerint a háttérben fusson.

Az időszakos folyamat futtatásakor a rendszer megkeresi a Project Operations integrációs naplóhoz még nem hozzáadott összes tényleges adatot. Minden egyes tényleges tranzakcióhoz létrejön egy naplósor.
A rendszer a naplósorokat külön naplókba csoportosítja a Projektműveletek integrációs naplója **mező Időszaki egységében** kiválasztott érték alapján (**Finance** > **Project management and accounting** > **Setup Project management and accounting Setup** > **Project management and accounting parameters**, **Project Operations Dynamics 365 Customer Engagement** lapon). A mező lehetséges értékei a következők:

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
    - Ha **a Tranzakció kategória** nincs beállítva a Projekt tényleges elemében, a rendszer a **Projektkategória alapértelmezései mezőjében található értéket használja a** Projektműveletek **panelen, Dynamics 365 Customer Engagement** a Projektvezetési és könyvelési **paraméterek lapon**.
  - Az **erőforrás** mező a tranzakcióhoz kapcsolódó projekterőforrást jelenti. Az erőforrás hivatkozásként szolgál az ügyfeleknek szóló projektszámla-ajánlatokhoz.
  - Az **Árfolyam** mező alapértelmezés szerint a Dynamics 365 Finance beállított Devizaárfolyamból **származik**. Ha az átváltási árfolyam beállítása hiányzik, akkor az **Importálás az előkészítésből** időszakos folyamat nem veszi fel a rekordot egy naplóba, és egy hibaüzenet jelenik meg a feladat végrehajtási naplójában.
  - A **Sortulajdonság** mező a projekt tényleges adatokban szereplő számlázási típust jelöli. A sortulajdonságok és a számlázási típus leképezése a **Projektműveletek lapon, a Projektvezetési és könyvelési** paraméterek lap Dynamics 365 Customer Engagement **lapján** van meghatározva.

A Project Operations integrációsnapló-soraiban csak a következő számlázási attribútumok frissíthetők:

- **Számlázási áfacsoport** és a **Számlázási cikk áfacsoportja**
- **Pénzügyi dimenziók** (az **összegek elosztása** művelet használatával)

Az integrációs napló sorai törölhetők. A fel nem adott sorok azonban ismét bekerülnek a naplóba, miután újrafuttatta az Importálás az **átmeneti** időszaki folyamatból folyamatot.

### <a name="post-the-project-operations-integration-journal"></a>A Project Operations integrációs naplójának közzététele

Az integrációs napló feladásakor létrejön egy projektrészfőkönyv és főkönyvi tranzakciók. Ezeket használják a lefelé irányuló ügyfélszámlázás során, a bevétel elszámolása és a pénzügyi jelentéskészítés során.

A kiválasztott Project Operations integrációs napló a Post **használatával** adhatja fel a Project Operations integrációs naplójának oldalán. Minden napló automatikusan közzétehető egy folyamat futtatásával a Periodics Project Operations integrációja **a Project Operations projektműveletek** > **utáni integrációs naplójában** > **·**.

A feladás történhet interaktívan vagy kötegben. Vegye figyelembe, hogy a 100 sornál több sorból álló naplók automatikusan egy kötegben lesznek közzétéve. A jobb teljesítmény érdekében, ha a sok sort tartalmazó naplókat egy kötegben teszik közzé, engedélyezze a **Projektműveletek utáni integrációs napló több kötegelt feladat** használatával funkciót a **Funkciókezelés** munkaterületen. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>A feladási hibákat tartalmazó összes sor átvitele új naplóba

> [!NOTE]
> Ennek a képességnek a használatához engedélyezze az **Összes sor átvitele feladási hibákkal egy új Project Operations integrációs naplóba** funkciót a **Funkciókezelés** munkaterületen.

Ez a funkció segít javítani a Project Operations integrációs naplójának felhasználói élményét. Ha engedélyezve van, a kettős írás időzítésével kapcsolatos problémák és beállítási problémák már nem akadályozzák meg az érvényes naplók közzétételét. A Project Operations integrációs naplóba való feladás során a rendszer a napló minden sorát ellenőrzi. Közzéteszi az összes hibát nem tartalmazó sort, és új naplót hoz létre minden olyan sorhoz, amely feladási hibát tartalmaz.

A feladási hibasorokkal rendelkező naplók áttekintéséhez nyissa meg a **Projektvezetési és könyvelési** \> **naplók Projektműveletek** \> **integrációs naplóját**, és szűrje a naplók listáját az **Eredeti napló** mező használatával. A következő ábra egy olyan példát mutat be, ahol a **Project Operations integrációs naplólapján** található naplók ilyen módon lettek szűrve.

![Az eredeti napló a Project Operations integrációs napló oldalán jelenik meg.](./media/transferLines-originalJournal.png)

Ha egy időszakos kötegelt feladat úgy van konfigurálva, hogy közzétegye az integrációs naplót, a feladás újra megtörténik, és a naplók feladásra kerülnek, ha az időzítési probléma megoldódott. A fennmaradó naplókat manuálisan kell megvizsgálni a naplók áttekintésével és a szükséges intézkedések megtételével.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
