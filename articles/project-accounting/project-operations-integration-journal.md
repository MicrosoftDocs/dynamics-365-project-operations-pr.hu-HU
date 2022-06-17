---
title: A Project Operations integrációs naplója
description: Ez a cikk az integrációs naplóval való munkáról nyújt tájékoztatást a Project Operationsben.
author: sigitac
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: befb1756ad77708805f3cbb06168b93e44296df0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923881"
---
# <a name="integration-journal-in-project-operations"></a>A Project Operations integrációs naplója

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Az idő- és Költségbejegyzések **tényleges érték** tranzakciókat hoznak létre, amelyek a projekttel kapcsolatban befejezett tevékenységek működési nézetét jelentik. A Dynamics 365 Project Operations a könyvelők számára eszközt biztosít a tranzakciók felülvizsgálatára, és szükség esetén a számviteli attribútumok módosítására. A felülvizsgálat és a helyesbítések befejeződése után a tranzakciókat a projekt részfőkönyvébe és a főkönyvbe könyveli a rendszer. A könyvelő ezeket a tevékenységeket a **Project Operations Integration** journal(**Dynamics 365 Finance** > **Project management and accounting** > **Journals** > **Project Operations Integration journal használatával végezheti** el.

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

Az integrációs naplósorok törölhetők, de a feladatlan sorokat a rendszer ismét beszúrja a naplóba, miután újra futtatja az **Importálás az előkészítésből** időszakos folyamatot.

Az integrációs napló feladásakor létrejön egy projektrészfőkönyv és főkönyvi tranzakciók. Ezeket használják a lefelé irányuló ügyfélszámlázás során, a bevétel elszámolása és a pénzügyi jelentéskészítés során.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
