---
title: Az ár miért alapértelmezett nulla a tényleges a tényleges időköltségeknél?
description: Annak meghatározása, hogy az ár miért alapértelmezett nulla a tényleges a tényleges időköltségeknél
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 635fe6dfb547e8b9f96ca1786912309a770e24c2
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146261"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Az ár miért alapértelmezett nulla a tényleges a tényleges időköltségeknél?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ez a gyakori kérdések rész azokra a tényleges költségekre vonatkozik, ahol a tranzakcióosztály Idő értékre van állítva, és tranzakció típusa Költség. A következő három ellenőrzés segít a hibaelhárításban, hogy az ár miért alapértelmezetten 0 a tényleges időköltségeknél.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>1. ellenőrzés: Azonosítsa a költségárlistát a projekthez

Keresés a projektet a tényleges projektmezőjében, majd ugorjon a projektlapra. Kattintson a mezőben a szerződő részleg hivatkozásra. A Szerződő részleg oldalon ellenőrizze, hogy a szerződő egység rendelkezik-e árlistával a költségárlista rácson.

Ha egynél több árlista van, akkor sikerült behatárolni a probléma. A Project Service szervezeti egységenként csak egy árlistát támogat. Távolítson el minden árlistát ehhez az entitáshoz, amíg a szervezeti egység költségárlista rácsához már csak egy árlista van csatolva.

Ha nincsenek csatolva árlisták a szervezeti egységhez , jegyezze fel a szervezeti egységet pénznemét. Menjen a Project Service alkalmazásba, majd a Paraméterek elemhez, és nyissa meg az Árlisták lapot, Ellenőrizze, hogy van-e árlista, amely Költségre és pénznemre hivatkozik, amely megfelel a Szervezeti egység pénznemének.
 
Ha nincsenek a kritériumnak megfelelő árlisták, akkor sikerült a problémát azonosítani. Győződjön meg arról, hogy legalább egy árlista van amelynek hivatkozása Költség értékre van állítva, és amelynek pénzneme megegyezik a szervezeti egységet pénznemével.

Ha egynél több árlista van, amely megfelel a feltételeknek, olvassa tovább a dokumentumot a további ellenőrzésekhez.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>2. ellenőrzés: A fentebb felsorolt árlisták bármelyike érvényese a tényleges időköltség napján?

Ahhoz, hogy a Project Service alapértelmezett árként vegye figyelembe az árlistát, az árlistának vonatkoznia kell az időköltség dátumán. Ellenőrizze a következőket, hogy a fentebb felsorolt árlisták érvényesek-e:

- Ellenőrizze, hogy a csatolt árlisták kezdő és befejező dátumai nem üresek-e az Általános lapon. Ha a kezdő és befejező dátumok fent azonosított árlistáknál üresek, akkor azonosította a problémát. 
- Jegyezze fel a tényleges időköltség kezdő dátum mezőjének tartalmát és ellenőrizze, hogy az azonosított árlisták bármelyike vonatkozik-e erre a dátumra. Például a tényleges időköltség dátuma az árlista kezdő és befejező dátuma közé kell essen. 
    - Ha nincs olyan árlista, amely vonatkozik az aktuális időköltség dátumára, akkor a problémát azonosította. Módosítsa az árlista kezdő és befejező dátumait annak érdekében, hogy az árlista vonatkozzon az időköltség a dátumára. 
    - Ha több olyan árlista van, amely vonatkozik az aktuális idő költség dátumára, akkor a problémát azonosította. Ezt úgy javíthatja, hogy az árlisták kezdő- és befejező dátumait úgy módosítja hogy csak egy árlista vonatkozzon, a tényleges időköltség dátumára. 
    - Ha csak egy árlista vonatkozik a tényleges időköltség dátumára, ugorjon a dokumentum következő szakaszára.
Amikor kész a szükséges javításokkal, hozzon létre újra egy időbejegyzést, és győződjön meg arról, hogy az aktuális időtöltség az érvényes árat mutatja-e.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>3. ellenőrzés: Van egy ár az árlistában az árazási dimenziókhoz az aktuális időköltséghez?

Ha sikeresen befejezte az 1. és 2 ellenőrzést, most már rendelkezik csak egy árlistával rendelkezik, amely érvényes a tényleges időköltség napján. Nyissa meg a ezt az árlistát, és lépjen a Szerepkörárak lapra. Győződjön meg arról, hogy van egy sor a rácson az árazási dimenziókhoz a tényleges költségnél.

Ha nincs sor a szerepkörár rácson az árazási dimenzióhoz a tényleges költségnél, azonosította a problémát. Hozzon létre egy sort Szerepkörárak rácson az árazási dimenziókhoz a tényleges időköltségnél. Amikor végzett ezzel, hozzon létre újra egy időbejegyzést, és győződjön meg arról, hogy az aktuális időköltség az érvényes árat mutatja-e.
 
Ha még mindig nem látható érvényes ár az aktuális időköltségnél, miután elvégezte a három ellenőrzést, hozzon létre egy támogatási jegyet.





[!INCLUDE[footer-include](../includes/footer-banner.md)]