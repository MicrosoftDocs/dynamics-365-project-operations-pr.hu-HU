---
title: Szállítói számlázás – koncepció és létrehozás
description: Ez a cikk ismerteti a szállítói számlák fogalmát, a használati forgatókönyveiket, és ismerteti azok létrehozási módszerét a Microsoft Dynamics 365 Project Operations alkalmazásban.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b57ec8cdb6097e6f2207056667aadfb43ee8acfc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261937"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Szállítói számlázás – koncepció és létrehozás

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations alkalmazásban a szállítói számlázás a szállítók által a projekten elvégzett szolgáltatásokból és/vagy anyagokból származó költségek rögzítésére használható.

Amikor szolgáltatásokat és/vagy anyagokat alvállalkozásba ad egy beszállítónak, az alvállalkozói szerződés az adott szállítóval kötött szerződéses megállapodást képviseli. Amint az szállító teljesíti a szolgáltatásokat, vagy ahogy az anyagokat megérkeztek és felhasználták a projektfeladatok során, a költségeket a projekthez rögzíti a rendszer. A szállító időszakosan számlákat küld, ezeket a számlákat ellenőrzik és megfelelteti a projektben rögzített költségekhez. Az ellenőrzési folyamat befejezése után a a szállító számlája meg lesz erősítve, és engedélyezve lesz a kifizetése.

## <a name="scenarios-for-use"></a>Használati forgatókönyvek

A Project Operations alkalmazásban szereplő szállítói számlák két különböző forgatókönyv támogatására használhatók.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Az ügyfelek, akik a teljes alvállalkozói élményt használják

A szállítói számla élmények lehetőséget biztosítanak az alvállalkozó által alvállalkozásba adott összetevőkre hivatkozó idő-, anyaghasználati és költségbejegyzések ellenőrzésére és egyeztetésére, valamint a szállítói számlasorokkal való egyeztetésére. Ezzel a folyamattal ellenőrizhető a szállítói számlasorok pontossága. Az ellenőrzési folyamat befejezése és a szállítói számla jóváhagyása után az alkalmazás visszavonja a jóváhagyott idő-, költség- és anyaghasználati naplókban rögzített tényadatokat, majd a szállító számlasorait használva új költség-tényadatokat hoz létre.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Az ügyfelek, akik nem használják a teljes alvállalkozói élményt, de egységes képben nézetet látni a projektek költségeiről a Project Operations alkalmazásban

Ha egy harmadik fél rendszerében követi nyomon az alvállalkozói folyamatokat, akkor az adott külső rendszerből a Project Operations alkalmazásba rögzítheti a költségeket olyan szállítói számlák létrehozásával, amelyek nem hivatkoznak az alvállalkozói szerződésekre. Így a projektvezetők egyetlen, egységes nézetben tekinthetik meg az adott projekt összes költségét.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Szállítói számlák létrehozása a Project Operations alkalmazásban

Új A szállítói számlák kétféleképpen hozhatók létre:

- A szállítói számla listaoldalról vagy egy szállítói számla részletek oldaláról
- Az alvállalkozói listaoldal vagy egy adott alvállalkozó részletes oldala

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Létrehozás a szállítói számlalistaoldalról vagy a részletek oldalról

1. Menjen a **Beszerzés** \> **Szállítói számlák** oldalra.
2. A szállítói számla listaoldalon vagy egy szállítói számla részletek lapján válassza az **Új** lehetőséget új szállítói számla létrehozásához.

Az ily módon létrehozott szállítói számlák alvállalkozói szerződésre is hivatkozhatnak.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Létrehozás az alvállalkozó listaoldalról vagy a részletek oldalról

1. Válassza a **Beszerzés** \> **Alvállalkozói szerződések** lehetőséget.
2. Válasszon ki egy vagy több alvállalkozói szerződést.
3. Az alvállalkozói szerződés listaoldalon vagy egy alvállalkozói szerződés részletek lapján válassza a **Szállítói számla létrehozása** lehetőséget új szállítói számla létrehozásához.

Egy új **Vázlat** állapotú új szállítói számla jön létre minden kiválasztott alvállalkozóhoz.

Az ily módon létrehozott szállítói számlák mindig hivatkoznak az alvállalkozó szerződésre a szállítói számla fejlécében. Az alvállalkozói szerződés minden olyan sor alapján, amely Idő és anyag számlázási módot tartalmaz, létrejön egy sor a szállítói számlán. Minden olyan alvállalkozói sor alapján, amely Rögzített árú számlázási módot alkalmaz, egy sor jön létre a szállítói számlán minden olyan alvállalkozóisor-mérföldkőhöz, amelynek állapota **Számlázásra kész**.

A következő mezőket és kapcsolódó rekordokat a rendszer az alvállalkozói szerződésből a szállítói számla fejlécébe másolja:

- Beszállító.
- A kapcsolódó árlistákat a rendszer árlistaként másolja a szállító számlájára.
- Pénznem:
- Szerződő részleg.
- Fizetési feltételek.

Idő és anyag típusú alvállalkozói sorok esetében a következő mezők és kapcsolódó rekordok lesznek másolva az alvállalkozó sorból a szállítói számlasorba:

- Alvállalkozói szerződés és alvállalkozói sor hivatkozások
- Tranzakcióosztály
- Beosztás
- Tranzakció kategóriája
- Termék mezők
- Project
- Feladatok
- Lefoglalható erőforrás

A Rögíztett árú típusú alvállalkozói sorok esetében a következő mezők lesznek másolva az alvállalkozó sorból és az alvállalkozói sor mérföldkőből a szállítói számlasorba:

- Alvállalkozói szerződés és alvállalkozói sor hivatkozások.
- Tranzakcióosztály. Az érték alapértelmezés szerint **Mérföldkő** lesz.
- A mérföldkő neve és összege a kapcsolódó alvállalkozói sor mérföldkövéből lesz másolva.
- A felhasználó kijelölheti a megfelelő a projektet és feladatot a szállítói számlasoron.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
