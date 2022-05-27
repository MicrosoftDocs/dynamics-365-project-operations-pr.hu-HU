---
title: Az értékesítési árak megoldása a projektbecslésekhez és a tényekhez
description: Ez a témakör az értékesítési árak megoldása a projektbecslésekhez és a tényekhez művelethez nyújt információkat.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8aa731d48a3ce39dfbf4fc1e5934b0844caf2953
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575722"
---
# <a name="resolve-sales-prices-for-project-estimates-and-actuals"></a>Az értékesítési árak megoldása a projektbecslésekhez és a tényekhez

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A becsült és tény értékesítési árak feloldásakor a Dynamics 365 Project Operations alkalmazásban a rendszer először a kapcsolódó projektajánlat vagy szerződés dátumát és pénznemét használja az értékesítési árlista feloldásához. Az értékesítési árlista feloldását követően a rendszer feloldja az értékesítési vagy a számlázási rátát.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>A tényleges és a becslési sorok értékesítési arányainak feloldása időpontra

A Project Operations becslési sorai az időpontokra vonatkozóan jelzik az ajánlati sort és a szerződéssorok részleteit, valamint az erőforrás-hozzárendeléseket a projekten.

Miután megoldódott az értékesítési árlista, a rendszer a következő lépéseket hajtja végre a számlázási ráta alapértelmezett értékének meghatározására.

1. A rendszer az időre vonatkozó becslési sorban található **Szerepkör** és **Erőforrás-kezelési egység** mezőkkel felelteti meg a szerepkörársorokat a megoldott árlistában. Ez a megfeleltetés feltételezi, hogy a számlázási árakhoz beépített árazási dimenziókat használnak. Ha bármely más mező alapján konfigurálja az árképzést, vagy a **Szerepkör** és az **Erőforrás-kezelési egység** mellett, akkor a rendszer ezzel a kombinációval kéri le az egyező szerepkörársort.
2. Ha a rendszer egy olyan szerepkörársort talál, amely rendelkezik számlázási rátával a **szerepkör** és az **erőforrás-kezelési egység** mező kombinációjára, akkor a számlázási ráta alapértelmezés szerint megjelenik.
3. Ha a rendszer nem tudja egyeztetni a **szerepkör** és az **Erőforrás-kezelő egység** mezők értékeit, akkor lekéri az egyező szerepkört tartalmazó szerepkörársorokat, de az **Erőforrás-kezelés** nullértékeivel. Ha a rendszer talál egy megfelelő szerepkörárrekordot, akkor a program a számlázási ráta alapértelmezett értéket az adott rekordból veszi. Ez az egyeztetés feltételezi, hogy létezik beépített konfiguráció a **Szerepkör** és az **Erőforrás-kezelési egység** relatív prioritásához értékesítési árképzési dimenzióként.

> [!NOTE]
> Ha eltérő prioritást állított be a **Szerepkör** és **Erőforrás-kezelési egység** mezőhöz, vagy ha más, magasabb prioritású dimenziók találhatók, ez a viselkedés ennek megfelelően változik. A rendszer beolvassa a szerepkörárak rekordjait az egyes árazási dimenzióértékek egyező értékeivel az elsőbbségi sorrendben, azokkal a sorokkal, amelyek a legutóbb használt dimenziókra vonatkozóan nullértékkel rendelkeznek.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>A tényleges és a becslési sorok értékesítési arányainak feloldása költséghez

A Project Operations becslési sorai aköltségekre vonatkozóan jelzik az ajánlati sort és a szerződéssorok részleteit, a költségekre és a költségbecslési sorokra vonatkozóan a projekten.

Miután megoldódott az értékesítési árlista, a rendszer a következő lépéseket hajtja végre az értékesítési egységár alapértelmezett értékének meghatározására.

1. A rendszer a költségre vonatkozó becslési sorban található **Kategória** és **Egység** mezőkombinációval felelteti meg a kategória-ársorokat a megoldott árlistában.
2. Ha a rendszer egy olyan kategória-ársort talál, amely rendelkezik értékesítési rátával a **Kategória** és az **Egység** mező kombinációjára, akkor az értékesítési ráta alapértelmezés szerint megjelenik.
3. Ha a rendszer megfelelő kategória-árlistát talál, akkor az árképzési mód használható az értékesítési ár alapértelmezett értékének meghatározására. A következő táblázat mutatja be a költség alapértelmezett ármeghatározáso működését a Project Operationsban.

    | Környezet | Árképzési mód | Alapértelmezett ár |
    | --- | --- | --- |
    | Becslés | Kiszerelésenkénti ár | A kategória ár sora alapján |
    | &nbsp; | Költségen | 0.00. |
    | &nbsp; | Haszonkulcs feletti költség | 0.00. |
    | Tényadat | Kiszerelésenkénti ár | A kategória ár sora alapján |
    | &nbsp; | Költségen | A kapcsolódó költségek tényleges értéke alapján |
    | &nbsp; | Haszonkulcs feletti költség | A kategória ár sora szerint megadott árrés alkalmazása a kapcsolódó költség tényleges értékének egységköltségrátájára |

4. Ha a rendszernem nem sikerül egyeztetni a **Kategória** és **Egység** mezőértékeket, az értékesítési ráta alapértelmezett értéke nulla lesz (0).

## <a name="resolving-sales-rates-on-actual-and-estimate-lines-for-material"></a>Értékesítési árak megoldása a tényekhez és a becslésekhez az Anyag számára

A Project Operations szolgáltatásban az anyagbecslési sorok az anyagra vonatkozó ajánlatsor- és szerződéssor-részleteket, valamint a projekt anyagbecslési sorait jelölik.

Miután megoldódott az értékesítési árlista, a rendszer a következő lépéseket hajtja végre az értékesítési egységár alapértelmezett értékének meghatározására.

1. A rendszer a becslési sorban szereplő **Termék** és **Egység** mezőkombinációt használja az anyaghoz, hogy megegyezzen a feloldott árlista árlistaelemeivel.
2. Ha a rendszer olyan árlistaelem sort talál, amely a **Termék** és az **Egység** mezőkombináció eladási díját tartalmazza, illetve az árképzési módszer **Pénznem összege**, akkor a rendszer az árlistasorban megadott eladási árat használja.
3. Ha a **Termék** és **Egység** mező értékei nem egyeznek, az értékesítési ár nullára csökken.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
