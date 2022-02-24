---
title: Az önköltségi árak megoldása a becslésekhez és a tényekhez
description: Ez a témakör a becslések és a tényadatok önköltségi árának feloldásával kapcsolatban tartalmaz tájékoztatást.
author: rumant
manager: Annbe
ms.date: 04/09/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 13903acc22e765ddc5bc1b87428ef3565f2b0a44
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877315"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Az önköltségi árak megoldása a becslésekhez és a tényekhez

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Az önköltségi árak és az önköltségi árlista feloldásához a becslések és a tényadatok esetében a rendszer a kapcsolódó projekt **Dátum**, **Pénznem** és **Szerződéskötési egység** mezőiben szereplő információkat használja. Az önköltségi árlistája feloldását követően az alkalmazás feloldja a költségdíjat.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>A tényleges és a becslési sorok önköltségi díjainak feloldása Időhöz

Az Időre vonatkozó becslési sorok az ajánlatra és a szerződéssor részletes adataira hivatkoznak a projekthez tartozó idő-és erőforrás-hozzárendelésekhez.

A az önköltségi árlista feloldását követően a rendszer az Idő becslési sorban található **Szerepkör**, **Erőforrás-kezelési vállalat** és **Erőforrás-kezelési egység** mezőkkel felelteti meg a szerepkörársorokat a megoldott árlistában. Ez a megfeleltetés feltételezi, hogy a munkadíjhoz beépített árazási dimenziókat használnak. Ha bármely más mező alapján konfigurálja az árképzést a rendszerben, vagy a **Szerepkör**, **Erőforrás-kezelési vállalat** és az **Erőforrás-kezelési egység** mellett más mezőket is használ, akkor a rendszer ezzel a kombinációval kéri le az egyező szerepkörársort. Ha az alkalmazás egy olyan szerepkörársort talál, amely rendelkezik önköltségi rátával a **szerepkör**, **Erőforrás-kezelő vállalat** és az **erőforrás-kezelési egység** mező kombinációjára, amely az alapértelmezett önköltségi ráta. Ha az alkalmazás nem tudja pontosan összeegyeztetni a **Szerepkör**, az **Erőforrás-kezelő vállalat** és a **Erőforrás-kezelő egység** értékeinek kombinációjának, akkor a szerepkörársorokat a megegyező szerepkörértékkel fogja lekérni, de nullértékekkel fognak rendelkezni az **Erőforrás-kezelő egység** és a **Erőforrás-kezelő vállalat** lehetőségek. Miután egyező szerepkörárrekordot talált a megfelelő szerepkörár-értékkel, a költségár alapértelmezetten az adott rekordból fog származni. 

> [!NOTE]
> Ha eltérő prioritást állított be a **Szerepkör**, **Erőforrás-kezelő vállalat** és **Erőforrás-kezelési egység** mezőhöz, vagy ha más, magasabb prioritású dimenziók találhatók, ez a viselkedés ennek megfelelően változik. A rendszer a szerepkörárrekordokat olyan értékekkel kérdezi le, amelyek prioritási sorrendben megfelelnek az egyes árképzési dimenzióértékeknek azokkal a sorokkal, amelyek nullértékkel rendelkeznek a prioritási sorrendben utolsó dimenziókhoz.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>A tényleges és a becslési sorok önköltségi díjainak feloldása Költséghez

A Költség becslés sorai az ajánlatra, a költségekhez tartozó szerződéssor részleteire és a projekt költségbecslési soraira vonatkozik.

A az önköltségi árlista feloldását követően a rendszer az Idő becslési sorban található **Kategória**, **Egység** és **Kategóriaár** mezőkkel felelteti meg a szerepkörársorokat a megoldott árlistában. Ha a rendszer egy olyan kategória-ársort talál, amely rendelkezik önköltségi rátával a **Kategória** és az **Egység** mező kombinációjára, akkor az önköltségi ráta alapértelmezés szerint megjelenik. Ha a rendszer nem tudja megfeleltetni a **Kategória** és az **Egység** értékeiket vagy ha meg tudja találni a megfelelő kategória ársort de az árképzési mód nem **Egységár** költségráta alapértelmezés szerint nulla (0) lesz.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Költségárak megoldása a tényekhez és a becslésekhez az anyag számára

Az anyagra vonatkozó becsléssorok az anyagra vonatkozó ajánlatsor- és szerződéssor-részletekre hivatkoznak, valamint a projekt anyagbecslését jelölik.

Az önköltségi árlista feloldása után a rendszer a becsült sor **Termék** és **Kiszerelés** mezőinek kombinációját használja az anyagbecsléshez, hogy megfeleljen a feloldott árlista **Árlistaelemek** sorainak. Ha a rendszer olyan termékársort talál, amely a **Termék** és **Kiszerelés** mezőkombináció költségarányát tartalmazza, a költségarány alapértelmezettre lesz beállítva. Ha a rendszer nem tudja összeegyeztetni a **Termék** és **Kiszerelés** értékeket, a kiszerelésköltség alapértelmezetten nullára csökken. Ez az alapértelmezett értékre állás akkor is meg fog történni, ha van egy egyező árlista cikksor, de az árképzési módszer olyan standard költségen vagy jelenlegi költségen alapul, amely nincs meghatározva a termékben.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
