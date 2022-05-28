---
title: Szállító számlázása - Koncepció és létrehozás
description: Ez a témakör a szállítói számlák fogalmát, a használati forgatókönyveket és a szállítói számlák Microsoftban történő létrehozásának módját ismerteti Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dc9b3954b237294f52aa0bb74f8008a5dfdf78fd
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580551"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Szállító számlázása - Koncepció és létrehozás

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations szállítói számlázása a szállítók által a projekten nyújtott szolgáltatásokból és/vagy anyagokból származó költségek rögzítésére használható.

Ha a szolgáltatásokat és/vagy anyagokat alvállalkozóként adják át egy szállítónak, az alvállalkozó az adott szállítóval kötött szerződéses megállapodást jelenti. Mivel a szállító szállítja a szolgáltatásokat, vagy az anyagokat megkapja és felhasználja a projekttevékenységekben, a költségeket a projekten rögzítik. A szállító rendszeresen küld olyan számlákat, amelyeket ellenőriznek és egyeztetnek a projekten rögzített költségekkel. Az ellenőrzési folyamat befejezése után a szállítói számla megerősítésre kerül, és kifizetésre kerül.

## <a name="scenarios-for-use"></a>Használati forgatókönyvek

A Projektműveletek szállítói számlái két különböző forgatókönyv támogatására használhatók.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Az ügyfelek a teljes alvállalkozói élményt kihasználják

A szállítói számla felhasználói lehetővé teszik az alvállalkozói számlasorokra hivatkozó időtételek, anyagfelhasználás és költségtételek ellenőrzését és egyeztetését. Ezzel a folyamattal ellenőrizheti a szállítói számlasorok pontosságát. Az ellenőrzési folyamat befejezése és a szállítói számla megerősítése után az alkalmazás a jóváhagyott idő-, költség- és anyaghasználati naplókban rögzített tényleges adatokat sztornírozza, és a szállítói számlasorok használatával új költségalapokat hoz létre.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Az ügyfelek nem használják ki a teljes alvállalkozói élményt, de egységes képet szeretnének kapni a projektek költségeiről a Projektműveletekben

Ha az alvállalkozói folyamatot egy harmadik féltől származó rendszerben követi nyomon, akkor az adott külső rendszertől származó költségeket a Project Operations-be rögzítheti olyan szállítói számlák létrehozásával, amelyek nem hivatkoznak alvállalkozói szerződésekre. Ily módon a projektmenedzserek egységes, egységes képet kaphatnak egy adott projekt összes költségéről.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Szállítói számlák létrehozása a Projektműveletekben

A szállítói számlák kétféleképpen hozhatók létre:

- A szállítói számlalista vagy egyetlen szállítói számla részleteket tartalmazó lapján
- Az alvállalkozói listaoldalról vagy egyetlen alvállalkozói szerződés részletes oldaláról

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Létrehozás a szállítói számlalista oldaláról vagy a részletek lapjáról

1. Nyissa meg a **Szállítói számlák beszerzési** \> **értékét**.
2. A szállítói számlalista vagy egyetlen szállítói számla részletei lapján válassza az Új **lehetőséget** új szállítói számla létrehozásához.

Az így létrehozott szállítói számlák alvállalkozói szerződésekre is hivatkozhatnak.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Létrehozás az alvállalkozói listaoldalról vagy a részletek oldaláról

1. Nyissa meg az **Alvállalkozók vásárlását** \> **·**.
2. Jelöljön ki egy vagy több alvállalkozót.
3. Az alvállalkozói lista vagy egyetlen alvállalkozói szerződés részletei lapján válassza a Szállítói számla **létrehozása lehetőséget** új szállítói számla létrehozásához.

Minden kiválasztott alvállalkozóhoz létrejön egy új szállítói számla **Piszkozat** állapotú állapotban.

Az ily módon létrehozott szállítói számlák mindig a szállítói számla fejében szereplő alvállalkozói szerződésre hivatkoznak. Az alvállalkozó minden olyan sora, amely idő- és anyagszámlázási módszerrel rendelkezik, egy sor létrehozását eredményezi a szállítói számlán. Az alvállalkozó minden olyan sora, amely rögzített árú számlázási módszerrel rendelkezik, a szállítói számlán egy sor létrehozását eredményezi minden olyan alvállalkozói sor mérföldkőhöz, amelynek állapota **Kész a számlázásra**.

A program a következő mezőket és kapcsolódó rekordokat másolja az alvállalkozói szerződésből a szállítói számla fejlécébe:

- Eladó.
- A kapcsolódó árlisták árlistaként lesznek átmásolva a szállítói számlára.
- Pénznem:
- Ajánlatkérő egység.
- Fizetési feltételek.

Idő- és anyag alvállalkozói sorok esetén a program a következő mezőket és kapcsolódó rekordokat másolja át az alvállalkozói sorból a szállítói számla sorába:

- Alvállalkozói és alvállalkozói sorhivatkozások
- Tranzakcióosztály
- Beosztás
- Tranzakció kategóriája
- Termékmezők
- Project
- Feladatok
- Lefoglalható erőforrás

Rögzített árú alvállalkozói sorok esetén a program a következő mezőket másolja át az alvállalkozói sorból és az alvállalkozói sor mérföldkőjéből a szállítói számla sorába:

- Alvállalkozói és alvállalkozói sorhivatkozások.
- Tranzakciós osztály. Alapértelmezés szerint az érték Mérföldkő **lesz**.
- A mérföldkő neve és összege a program átmásolja a kapcsolódó alvállalkozói sor mérföldkőjét.
- A felhasználó kiválaszthat egy projektet és feladatot a szállítói számlasorban.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
