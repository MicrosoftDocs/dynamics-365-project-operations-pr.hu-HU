---
title: Az ár miért alapértelmezett nulla a tényleges értékesítési költségeknél?
description: A következő három ellenőrzés segít a hibaelhárításban, hogy az ár miért alapértelmezetten 0 a tényleges értékesítési költségeknél.
author: rumant
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: d7221b9b5db986c8d57688893014a1bfd9ac4e41
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581931"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Az ár miért alapértelmezett nulla a tényleges értékesítési költségeknél?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ez a gyakori kérdések rész azokra a tényleges költségekre vonatkozik, ahol a tranzakcióosztály Költség értékre van állítva, és tranzakció Számlázatlan értékesítés. A következő három ellenőrzés segít a hibaelhárításban, hogy az ár (számlázási díj) miért alapértelmezetten 0 a tényleges értékesítési költségeknél.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>1. ellenőrzés: Azonosítsa az értékesítési árlistát a projekthez

Keresés a projektet a tényleges projektmezőjében, és ugorjon a projektlapra. Majd menjen az Értékesítés lapra. A Projektszerződés sorai rácson kattintson a hivatkozásra a Projektszerződés mezőben. A Projektszerződés oldal jelenik meg. A Projektszerződés oldalon nyissa meg a Projektárlisták lapot. Ellenőrizze, hogy legalább egy árlista van-e itt.

Ha a Projektszerződés Árlisták rácsában nincs csatolva egyetlen árlista sem:

- Csatoljon egy árlistát a Projektárlisták rácshoz. Az árlistáknak, amelyeket itt csatolni lehet rendelkezniük kell egy kontextusmezővel a Sales-hez, és az árlista a pénznem mezőjének egyeznie kell a pénznem mezőjével. Amikor végzett a szükséges javításokkal, hozzon létre újra egy költségbejegyzést, és győződjön meg arról, hogy a számlázatlan aktuális értékesítés az érvényes árat mutatja-e.
- Ha több csatolt árlista van csatolva a Projektárlisták rácshoz, ugorjon a 2 ellenőrzéshez.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>2. ellenőrzés: A fentebb felsorolt árlisták érvényesek a tényleges költség napján?

Ahhoz, hogy a Project Service alapértelmezett árként vegye figyelembe az árlistát, az árlistának vonatkoznia kell az értékesítési költség dátumán. Ellenőrizze a következőket, hogy a fentebb felsorolt árlisták érvényesek-e:

- Először ellenőrizze, hogy a csatolt árlisták kezdő és befejező dátumai nem üresek-e az Általános lapon. Ha a kezdő és befejező dátumok fentebb azonosított árlistáknál üresek, akkor azonosította a problémát. 
- Jegyezze fel a tényleges értékesítési költség kezdő dátum mezőjének tartalmát és ellenőrizze, hogy az azonosított árlisták bármelyike vonatkozik-e erre a dátumra. Például a tényleges kiadás dátuma az árlista kezdő és befejező dátuma közé kell essen. 
    - Ha nincs olyan árlista, amely vonatkozik az aktuális értékesítési költség dátumára, akkor a problémát azonosította. Módosítsa az árlista kezdő és befejező dátumait annak érdekében, hogy az árlista vonatkozzon az aktuális költség a dátumára. 
    - Ha több olyan árlista van, amely vonatkozik az aktuális értékesítési költség dátumára, akkor a problémát azonosította. Az árlisták kezdő- és befejező dátumait úgy módosítja hogy csak egy árlista vonatkozzon, a tényleges kiadás dátumára. 
    - Ha csak egy árlista érvényes a tényleges kiadás dátumára, ugorjon a 3. ellenőrzésre.
Amikor kész a szükséges javításokkal, hozzon létre újra egy költségbejegyzést, és győződjön meg arról, hogy a számlázatlan aktuális értékesítés az érvényes árat mutatja-e.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>3. ellenőrzés: Tartozik érvényes ár a megfelelő projekt árlistában a költségkategóriához? 

Ha sikeresen befejezte az 1. és 2 ellenőrzést, most már rendelkezik csak egy projektárlistával rendelkezik, amely érvényes a tényleges értékesítési költség napján. Nyissa meg a ezt a projektárlistát, és lépjen a Kategóriaárak fülre. Győződjön meg arról, hogy van egy sor a rácson az adott költségkategóriához a tényleges költségnél.
 
- Ha nincs ilyen sor, akkor azonosított a problémát. Hozzon létre egy sort a Kategóriaárak lapon a tényleges költségnél. Majd hozzon létre újra egy költségbejegyzést, és győződjön meg arról, hogy a számlázatlan aktuális értékesítés az érvényes árat mutatja-e. 
- Ha a kategóriaárak rácsban a kategóriához immár tartozik sor, ellenőrizze, hogy a érvényes ár van-e benne.

Az érvényes ár meghatározásához használja az alábbi módszereket:

- Ha az Árképzési mód mezőben a Kategória ársoron az érték Költséggel, akkor az Értékesítési költség egységára a Költségbejegyzés értékére lesz alapértelmezetten állítva.
- Ha az Árképzési mód mezőben a Kategória ársoron az érték Árrés, ellenőrizze, hogy a Százalék mező értéke egy érvényes érték-e. Az Értékesítési költség egységára alapértelmezetten ezen árrés százalék alkalmazásával a Költség bejegyzésre lesz meghatározva
- Ha az Árképzési mód mezőben a Kategória ársoron az érték Kiszerelésenkénti ár, ellenőrizze, hogy a Százalék mező értéke egy érvényes érték-e. Az Értékesítési költség egységára alapértelmezetten az Ár mezőben meghatározott valutamennyiségre lesz állítva.

Ha a költségkategória árbeállítása nem érvényes, azonosította a problémát. A megoldás az, ha úgy szerkeszti kategória ársort, hogy a költségkategóriához a fenti szabályok szerinti ár tartozzon. Amikor végzett azzal, hozzon létre újra egy költségbejegyzést, majd ellenőrizze, hogy a számlázatlan aktuális értékesítés az érvényes árat mutatja-e.

Ha még mindig nem látható érvényes árat az aktuális értékesítési költségnél, miután elvégezte a három ellenőrzést, hozzon létre egy támogatási jegyet.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
