---
title: Projektárlisták kezelése projektárajánlatokon - Lite
description: Ez a témakör a projektárlisták árajánlatokban történő használatát ismerteti. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2ff830c63f7acf4cc23ac75d44afa9c3553b8724
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175984"
---
# <a name="manage-project-price-lists-on-project-quotes---lite"></a>Projektárlisták kezelése projektárajánlatokon - Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A projektárajánlatok több dátum szerint érvényes értékesítési árlisták támogatására készültek. A Dynamics 365 Project Operations egy új, **Projektárlisták** nevű társított entitást adott hozzá. Ez az entitás egy a sokhoz típusú kapcsolattal rendelkezik a projektárajánlathoz.

A projektárlisták a projekt idő- és a kiadástranzakcióinak árazására szolgálnak. Ha egy ajánlathoz egy vagy több projektárlista tartozik, akkor ezek az árlisták kerülnek felhasználásra az idő- és költségbecslések, illetve az árajánlaton keresztül az árajánlattal társított projektek tényleges értékeinek árazására.

Ha egy projektárajánlat nem tartalmaz projektárlistát, a rendszer figyelmeztető üzenetet jelenít meg. Az üzenet jelzi, hogy mivel nincsenek projektárlisták, a becsült és a tényleges projektmunka és -költségek nem lesznek beárazva. Ehelyett nulla (0) árat fognak tartalmazni az értékesítési értékek esetében.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Projektárlista hozzárendelése vagy a hozzárendelésének törlése egy projektárajánlatnál

A következő lépések végrehajtásával hozhat létre vagy választhat ki egy adott árlistát a projektalapú munkák és kiadások becsléséhez.

1. Az árajánlaton válassza a **Projekt ára** lapot, majd az alrácson válassza az **+ Új projektárlista hozzáadása** elemet.
2. A Gyorslétrehozás lapon jelöljön ki egy árlistát. A legördülő listában láthatók azok az árlisták, amelyek a **Sales** értékre beállított környezettel rendelkeznek, és a pénznemük megegyezik az árajánlatban szereplő pénznemmel.
4. Adja meg a projektárlista hozzárendelésének leírását, és válassza a **Mentés és bezárás** lehetőséget.

Létrejön egy projektárlista-hozzárendelés.

Ez a folyamat megismételhető, ha egynél több projektárlistát kell társítania a projektárajánlathoz. Csak akkor hozzon létre több projektárlistát, ha különböző érvényességi dátumok vannak az egyes társított projektárlistákban.

> [!NOTE]
> A Project Operations nem támogatja az átfedésben lévő dátumérvényességet a projektárlistákon. Ha egy adott dátummal több projektárlista található egy tranzakcióhoz, akkor a tranzakció ára alapértelmezés szerint nulla (0) lesz.
A projektárlista-hozzárendelés eltávolításához jelölje ki a projektárlistát, majd válassza az **Árajánlat projektárlistájának törlése** lehetőséget. Az árlista törlődik az árajánlat projektárlistájából, de maga az árlista nem törlődik. Csak az árajánlathoz tartozó társítás törlődik.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Alapértelmezett projektárlisták beállítása az árajánlaton

A projektárlisták alapértelmezett értékre állíthatók be a projektárajánlatban. Ez a beállítás gondoskodik arról, hogy a szervezet minden árajánlata mindig az adott időszakra vonatkozó normál árlistával kezdjen.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Szervezeti alapértelmezés beállítása a projektárlistákhoz

1. Válassza a **Beállítások** > **Általános** > **Paraméterek** lehetőséget.
2. Az **Aktív paraméterek** listaoldalon keresse meg a rekordot, majd kattintson rá duplán, és nyissa meg. 
3. A **Paraméterek** oldalon jelölje ki az **Árlista** lapot. Az alapértelmezett árlisták listája jelenik meg. Ez a lista az általános önköltségi és értékesítési árlistákat tartalmazza. Ha az Ön által folytatott értékesítés minden pénzneméhez van itt társítva egy értékesítési árlista, akkor biztosíthatja, hogy ez az értékesítési árlista lesz az alapértelmezés az ebben a pénznemben lebonyolított ügyletek ügyfelei számára létrehozott minden árajánlat esetében.

### <a name="set-up-customer-specific-project-price-lists"></a>Ügyfélspecifikus projektárlisták beállítása

Ügyfélspecifikus projektárlisták is beállíthatók, ha az ügyfelekkel megkötötte a fő árképzési megállapodást.

Az ügyfélspecifikus projektárlista beállításához hajtsa végre a következő lépéseket.

1. A **Sales** területen válassza az **Ügyfelek** lehetőséget.
2. Az aktív partnerek listájában jelölje ki, és nyissa meg azt az ügyfélrekordot, amelyhez speciális árlista tartozik.
3. A **Projektárlisták** lapon új árlista-hozzárendelést hozhat létre, hogy tartalmazza az adott ügyfélre vonatkozó projektárlistát.

## <a name="create-custom-pricing-on-a-project-quote"></a>Egyéni árazás létrehozása egy projektárajánlatban

Miután a szervezeti és az ügyfélspecifikus alapértelmezett projektárlistákkal is rendelkezik, a projektárajánlatok automatikusan létrejönnek ezekkel a projektárlista-hozzárendelésekkel. Bizonyos esetekben azonban előfordulhat, hogy egyedi árazást kell létrehoznia egy adott projektárajánlathoz. 

1. A **Projektárajánlat** részen a **Projektárlista** lapon ellenőrizze az alrácsban, hogy nincs-e kiválasztva specifikus árlistarekord.
2. Válassza az **Egyéni árazás létrehozása** lehetőséget. Ezzel a rendszer az árajánlathoz jelenleg társított összes szabványos árlistáról másolatot készít, és ezeket a másolatokat társítja az árajánlathoz. A rendszer eltávolítja az általános árlisták meglévő hozzárendeléseit. Az értékesítő ezután megkezdheti az árak szerkesztését ezeken a példányokon. Ezek a megváltozott árak csak erre a projektárajánlatra vonatkoznak.
