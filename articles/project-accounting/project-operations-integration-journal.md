---
title: A Project Operations integrációs naplója
description: Ez a témakör a Project Operations integrációs naplójának használatáról nyújt tájékoztatást.
author: sigitac
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0021147530d1aa9f82cc54ca8c92b9977c1eea2c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287241"
---
# <a name="integration-journal-in-project-operations"></a>A Project Operations integrációs naplója

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Az idő- és Költségbejegyzések **tényleges érték** tranzakciókat hoznak létre, amelyek a projekttel kapcsolatban befejezett tevékenységek működési nézetét jelentik. A Dynamics 365 Project Operations a könyvelők számára eszközt biztosít a tranzakciók felülvizsgálatára, és szükség esetén a számviteli attribútumok módosítására. A felülvizsgálat és a helyesbítések befejeződése után a tranzakciókat a projekt részfőkönyvébe és a főkönyvbe könyveli a rendszer. A könyvelő ezeket a tevékenységeket a **Project Operations-integráció** naplójával hajtja végre(**Dynamics 365 Finance** > **Projektmenedzsment és könyvelés** > **Naplók** > **Project Operations-integrációs** napló).

![Integrációs napló folyamata](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Rekordok létrehozása a Project Operations integrációs naplójában

A Project Operations integrációs napló rekordjai az **Importálás az előkészítési táblából** időszakos folyamat segítségével jönnek létre. A folyamat futtatásához nyissa meg a **Dynamics 365 Finance** > **Projektmenedzsment és Könyvelés** > **Időszakos** > **Project Operations-integráció** > **Importálás az előkészítési táblából** menüpontot. A folyamatot interaktív módon futtathatja, illetve beállíthatja, hogy a folyamat szükség szerint a háttérben fusson.

Az időszakos folyamat futtatásakor a rendszer megkeresi a Project Operations integrációs naplóhoz még nem hozzáadott összes tényleges adatot. Minden egyes tényleges tranzakcióhoz létrejön egy naplósor.
A rendszer a naplósorokat külön naplókba csoportosítja az **Időszakegység a Project Operations integrációs naplóban** mezőben kiválasztott érték alapján (**Finance** > **Projektmenedzsment és könyvelés** > **Beállítás** > **Projektmenedzsment és könyvelési paraméterek**, **Project Operations a Dynamics 365 Customer Engagement szolgáltatásban** lap). A mező lehetséges értékei a következők:

  - **Napok**: A tényadatok a tranzakció dátuma szerint vannak csoportosítva. Minden naphoz külön napló jön létre.
  - **Hónapok**: a tényleges adatok naptári hónap szerint vannak csoportosítva. Minden hónaphoz külön napló jön létre.
  - **Évek**: a tényleges adatok naptári év szerint vannak csoportosítva. Minden évhez külön napló jön létre.
  - **Összes**: az összes tényleges tranzakció ugyanabban az integrációs naplóban szerepel. Ha a napló nem érhető el az időszakos folyamat futtatásakor, például akkor, ha a napló a tranzakciók elszámolási folyamatában van, akkor létrejön egy új napló.

A naplósorok a Projektadatok alapján jönnek létre. A következő felsorolás tartalmazza a fontosabb alapértelmezett és átalakítási szabályok némelyikét:

  - Minden projekttényadat-tranzakcióhoz tartozik egy sor a Project Operations integrációs naplóban. Az idő- és anyagelszámolású számlázási típusokhoz tartozó költség és nem számlázott értékesítési tranzakciók külön sorokban jelennek meg.
  - A **dátum** mező a tranzakció dátumát jelöli. A **Könyvelési dátum** mező a tranzakció főkönyvbe történő rögzítésének dátumát jelenti. Ha a számlázási dátum egy [lezárt pénzügyi időszak](https://docs.microsoft.com/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) alatt van , és be van állítva a **Könyvelési dátum automatikus beállítása nyitott főkönyvi időszakra** paraméter a **Projekmenedzsment és könyvelési paraméterek** oldal **Pénzügyi** lapján, akkor a rendszer a tranzakció könyvelési dátumát módosítja a következő nyitott főkönyvi időszak első dátumára.
  - A **bizonylat** mező az összes tényleges tranzakcióhoz tartozó bizonylatszámot jeleníti meg. A bizonylatszám-sorozatot a **Számsorozatok** lapon, a **projektmenedzsment és a könyvelési paraméterek** lapon lehet megadni. Az egyes sorokhoz új szám tartozik. A bizonylat feladása után megtekintheti, hogyan kapcsolódik a költség és a nem számlázott értékesítési tranzakció a **kapcsolódó bizonylatok** kiválasztásával a **bizonylattranzakció** lapon.
  - A **Kategória** mező a kapcsolódó projekt tényadatainak tranzakciós kategóriája alapján egy projekttranzakciót és alapértelmezett értékeket jelent.
    - Ha a **tranzakció kategóriája** meg van adva a projekt tényadataiban és egy kapcsolódó **projektkategória** létezik egy adott jogi entitásban, akkor a kategória alapértelmezés szerint ebbe a kategóriába tartozik.
    - Ha a **tranzakciós kategória** nincs beállítva a projekt tényadatában, a rendszer a **projektkategória alapértelmezései** mezőben szereplő értéket használja a **Project Operations a Dynamics 365 Customer Engagement szolgáltatásban** lapon a **Projektmenedzsment és könyvelési paraméterek** oldalon.
  - Az **erőforrás** mező a tranzakcióhoz kapcsolódó projekterőforrást jelenti. Az erőforrás hivatkozásként szolgál az ügyfeleknek szóló projektszámla-ajánlatokhoz.
  - Az **árfolyam** mező alapértelmezett értéke a **Devizaárfolyam** értékéből származik a Dynamics 365 Finance-ból. Ha az átváltási árfolyam beállítása hiányzik, akkor az **Importálás az előkészítésből** időszakos folyamat nem veszi fel a rekordot egy naplóba, és egy hibaüzenet jelenik meg a feladat végrehajtási naplójában.
  - A **Sortulajdonság** mező a projekt tényleges adatokban szereplő számlázási típust jelöli. A sortulajdonság és a számlázási típus leképezése a **Project Operations a Dynamics 365 Customer Engagement szolgáltatásban** lapon, a **Projektmenedzsment és könyvelési paraméterek** oldalon van meghatározva.

A Project Operations integrációsnapló-soraiban csak a következő számlázási attribútumok frissíthetők:

- **Számlázási áfacsoport** és a **Számlázási cikk áfacsoportja**
- **Pénzügyi dimenziók** (az **összegek elosztása** művelet használatával)

Az integrációs naplósorok törölhetők, de a feladatlan sorokat a rendszer ismét beszúrja a naplóba, miután újra futtatja az **Importálás az előkészítésből** időszakos folyamatot.

Az integrációs napló feladásakor létrejön egy projektrészfőkönyv és főkönyvi tranzakciók. Ezeket használják a lefelé irányuló ügyfélszámlázás során, a bevétel elszámolása és a pénzügyi jelentéskészítés során.


[!INCLUDE[footer-include](../includes/footer-banner.md)]