---
title: Szállítói számlázás – koncepció és létrehozás
description: Ez a cikk a szállítói számlák fogalmát, a használati forgatókönyveket és a szállítói számlák Microsoftban történő létrehozásának módját ismerteti Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 38f0760697522b7a5e561cec7d38dfd5c3eaf9fc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911461"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Szállítói számlázás – koncepció és létrehozás

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoftnál Dynamics 365 Project Operations a szállítói számlázással rögzítheti a szállítók által a projekteken keresztüli szolgáltatások és/vagy anyagok szállításából származó költségeket.

Amikor a szolgáltatásokat és/vagy anyagokat alvállalkozásba adják egy szállítónak, az alvállalkozói szerződés az adott szállítóval kötött szerződéses megállapodást jelenti. Ahogy a szállító nyújtja a szolgáltatásokat, vagy az anyagokat megkapja és felhasználja a projektfeladatokhoz, a költségeket a projekten rögzítik. A szállító rendszeres időközönként olyan számlákat küld, amelyek ellenőrzöttek és egyeznek a projekten rögzített költségekkel. Az ellenőrzési folyamat befejezése után a szállítói számlát visszaigazolják, és kifizetésre felszabadítják.

## <a name="scenarios-for-use"></a>Használati forgatókönyvek

A Project Operations szállítói számlái két különböző forgatókönyv támogatására használhatók.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Az ügyfelek a teljes alvállalkozói élményt használják

A szállítói számla felhasználói felülete lehetővé teszi az alvállalkozásba adott összetevőkre hivatkozó időbevitelek, anyaghasználati és költségbejegyzések ellenőrzését és egyeztetését a szállítói számlasorokkal. Ezzel a folyamattal ellenőrizhető a szállítói számlasorok pontossága. Az ellenőrzési folyamat befejezése és a szállítói számla megerősítése után az alkalmazás visszavonja a jóváhagyott idő-, költség- és anyaghasználati naplókban rögzített tényleges adatokat, és új költség tényleges költségeket hoz létre a szállítói számlasorok használatával.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Az ügyfelek nem használják a teljes alvállalkozói élményt, de egységes képet szeretnének kapni a project operations-projektek költségeinekről

Ha az alvállalkozói folyamatot egy harmadik féltől származó rendszerben követi nyomon, az adott harmadik féltől származó rendszerből származó költségeket rögzítheti a Project Operationsbe olyan szállítói számlák létrehozásával, amelyek nem hivatkoznak alvállalkozói szerződésekre. Ily módon a projektmenedzserek egyetlen, egységes nézetet kaphatnak egy adott projekt összes költségéről.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Szállítói számlák létrehozása a Project Operationsben

A szállítói számlák kétféleképpen hozhatók létre:

- A szállítói számla listaoldaláról vagy egyetlen szállítói számla részletek oldaláról
- Az alvállalkozói lista oldaláról vagy egyetlen alvállalkozói szerződés részletes oldaláról

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Létrehozás a szállítói számla listaoldaláról vagy a részletek oldalról

1. Lépjen a **Szállítói számlák vásárlása** \> **elemre**.
2. A szállítói számla listaoldalán vagy egyetlen szállítói számla részletek lapján válassza az Új **lehetőséget** egy új szállítói számla létrehozásához.

Az így létrehozott szállítói számlák alvállalkozói szerződésre is hivatkozhatnak.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Létrehozás az alvállalkozói listaoldalról vagy a részletek oldalról

1. Lépjen az **Alvállalkozói** \> **szerződések vásárlása oldalra.**
2. Válasszon ki egy vagy több alvállalkozói szerződést.
3. Az alvállalkozói listaoldalon vagy egyetlen alvállalkozói szerződés részletei lapján válassza a Szállítói számla **létrehozása lehetőséget** egy új szállítói számla létrehozásához.

Minden kiválasztott alvállalkozói alvállalkozáshoz létrejön egy új szállítói számla **Vázlat** állapotban.

Az így létrehozott szállítói számlák mindig hivatkoznak a szállítói számla fejlécében található alvállalkozói szerződésre. Az alvállalkozói szerződés minden olyan sora, amely idő- és anyagszámlázási móddal rendelkezik, egy sor létrehozását eredményezi a szállítói számlán. Az alvállalkozói szerződés minden olyan sora, amely rögzített árú számlázási módszerrel rendelkezik, létrehoz egy sort a szállítói számlán minden olyan alvállalkozói sor mérföldkövet, amelynek állapota **Készen áll a számlára**.

A rendszer a következő mezőket és a kapcsolódó rekordokat másolja az alvállalkozói szerződésből a szállítói számla fejlécébe:

- Eladó.
- A kapcsolódó árlistákat a rendszer árlistaként másolja a szállítói számlára.
- Pénznem:
- Szerződő egység.
- Fizetési feltételek.

Az idő- és anyag-alvállalkozói sorok esetében a rendszer a következő mezőket és a kapcsolódó rekordokat másolja az alvállalkozói sorból a szállítói számla sorába:

- Alvállalkozói és alvállalkozói sorok hivatkozásai
- Tranzakcióosztály
- Beosztás
- Tranzakció kategóriája
- Termék mezők
- Project
- Feladatok
- Lefoglalható erőforrás

A Rögzített árú alvállalkozói sorok esetében a rendszer a következő mezőket másolja az alvállalkozói sorból és az alvállalkozói sor mérföldkövéből a szállítói számlasorba:

- Alvállalkozói és alvállalkozói sorok hivatkozásai.
- Tranzakciós osztály. Alapértelmezés szerint az érték Mérföldkő **lesz**.
- A mérföldkő neve és összege a kapcsolódó alvállalkozói sor mérföldkövéből lesz átmásolva.
- A felhasználó kiválaszthat egy projektet és feladatot a szállítói számlasoron.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
