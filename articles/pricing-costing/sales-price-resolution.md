---
title: Az értékesítési árak megoldása a becslésekhez és a tényekhez
description: Ez a témakör a becslések és a tényadatok értékesítési díjának megoldásával kapcsolatban tartalmaz tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8c18dd734312b2dd147381169f5c3dc38a68a601
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119556"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Az értékesítési árak megoldása a becslésekhez és a tényekhez

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ha a becslések és a tényleges adatok értékesítési árát megoldják a Dynamics 365 Project Operationsban, a rendszer először a kapcsolódó projektajánlat vagy szerződés dátumát és pénznemét használja az értékesítési árlista feloldásához. Az értékesítési árlista feloldását követően a rendszer feloldja az értékesítési vagy a számlázási rátát.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>A tényleges és a becslési sorok értékesítési arányainak feloldása időpontra

A Project Operations becslési sorai az időpontokra vonatkozóan jelzik az ajánlati sort és a szerződéssorok részleteit, valamint az erőforrás-hozzárendeléseket a projekten.

Miután megoldódott az értékesítési árlista, a rendszer a következő lépéseket hajtja végre a számlázási ráta alapértelmezett értékének meghatározására.

1. A rendszer az időre vonatkozó becslési sorban található **Szerepkör**, **Erőforrás-kezelési vállalat** és **Erőforrás-kezelési egység** mezőkkel felelteti meg a szerepkörársorokat a megoldott árlistában. Ez a megfeleltetés feltételezi, hogy a számlázási árakhoz beépített árazási dimenziókat használnak. Ha bármely más mező alapján konfigurálja az árképzést, vagy a **Szerepkör**, **Erőforrás-kezelési vállalat** és az **Erőforrás-kezelési egység** mellett, akkor a rendszer ezzel a kombinációval kéri le az egyező szerepkörársort.
2. Ha a rendszer egy olyan szerepkörársort talál, amely rendelkezik számlázási rátával a **szerepkör**, **Erőforrás-kezelő vállalat** és az **erőforrás-kezelési egység** mező kombinációjára, akkor a számlázási ráta alapértelmezés szerint megjelenik.
3. Ha a rendszer nem tudja egyeztetni a **szerepkör**, **Erőforrás-kezelő vállalat** és az **Erőforrás-kezelő egység** mezők értékeit, akkor lekéri az egyező szerepkört tartalmazó szerepkörársorokat, de az **Erőforrás-kezelő egység** nullértékeivel. Ha a rendszer talál egy megfelelő szerepkörárrekordot, akkor a program a számlázási ráta alapértelmezett értéket az adott rekordból veszi. Ez az egyeztetés feltételezi, hogy létezik beépített konfiguráció a **Szerepkör** és az **Erőforrás-kezelési egység** relatív prioritásához értékesítési árképzési dimenzióként.

> [!NOTE]
> Ha eltérő prioritást állított be a **Szerepkör**, **Erőforrás-kezelő vállalat** és **Erőforrás-kezelési egység** mezőhöz, vagy ha más, magasabb prioritású dimenziók találhatók, ez a viselkedés ennek megfelelően változik. A rendszer beolvassa a szerepkörárak rekordjait az egyes árazási dimenzióértékek egyező értékeivel az elsőbbségi sorrendben, azokkal a sorokkal, amelyek a legutóbb használt dimenziókra vonatkozóan nullértékkel rendelkeznek.

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
