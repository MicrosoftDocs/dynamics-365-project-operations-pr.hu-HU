---
title: Az önköltségi árak megoldása a becsléseken és a tényeken – Lite
description: Ez a témakör a becsléseken a tényadatok önköltségi árának feloldásával kapcsolatban tartalmaz tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2afaa2231f4044dbcbfa24b91aec39289275a91
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764596"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Az önköltségi árak megoldása a becsléseken és a tényeken – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Az önköltségi árak és az önköltségi árlista feloldásához a becslések és a tényadatok esetében a rendszer a kapcsolódó projekt **Dátum**, **Pénznem** és **Szerződéskötési egység** mezőiben szereplő információkat használja. Az önköltségi árlistája feloldását követően az alkalmazás feloldja a költségdíjat.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>A tényleges és a becslési sorok önköltségi díjainak feloldása Időhöz

Az Időre vonatkozó becslési sorok az ajánlatra és a szerződéssor részletes adataira hivatkoznak a projekthez tartozó idő-és erőforrás-hozzárendelésekhez.

Az önköltségi árlista feloldása után az Idő becslési sorában szereplő **Szerepkör** és **Erőforrás-kezelő részleg** mezők egyeztetésre kerülnek az árlista szerepkörársoraival. Ez az egyezés feltételezi, hogy a munkaerőköltséghez a szokásos árképzési dimenziókat használja. Ha bármely más mező alapján konfigurálja az árképzést a rendszerben, vagy a **Szerepkör** és az **Erőforrás-kezelési egység** mellett más mezőket is használ, akkor a rendszer ezzel a kombinációval kéri le az egyező szerepkörársort. Ha az alkalmazás egy olyan szerepkörársort talál, amely rendelkezik önköltségi rátával a **Szerepkör** és az **Erőforrás-kezelési egység** mező kombinációjára, amely az alapértelmezett önköltségi ráta. Ha az alkalmazás nem tudja egyeztetni a **Szerepkör** és az **Erőforrás-kezelő egység** mezők értékeit, akkor lekéri az egyező szerepkört tartalmazó szerepkörársorokat, de az **Erőforrás-kezelő egység** nullértékeivel. Ha egy megfelelő szerepkör-ár rekordot talált, akkor a rendszer az adott bejegyzésből kiszámítja a költségdíj alapértékeit. 

> [!NOTE]
> Ha eltérő prioritást állított be a **Szerepkör** és **Erőforrás-kezelési egység** mezőhöz, vagy ha más, magasabb prioritású dimenziók találhatók, ez a viselkedés ennek megfelelően változik. A rendszer beolvassa a szerepkörárak rekordjait az egyes árazási dimenzióértékek egyező értékeivel az elsőbbségi sorrendben, azokkal a sorokkal, amelyek a legutóbb használt dimenziókra vonatkozóan nullértékkel rendelkeznek.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>A tényleges és a becslési sorok önköltségi díjainak feloldása Költséghez

A Költség becslés sorai az ajánlatra, a költségekhez tartozó szerződéssor részleteire és a projekt költségbecslési soraira vonatkozik.

A költségárlista feloldása után a rendszer a költségbecslés sor **Kategória** és **Egység** mezőinek kombinációját használja a feloldott árlista **Kategóriaársor** lehetőséggel való egyezéshez. Ha a rendszer egy olyan kategória-ársort talál, amely rendelkezik önköltségi rátával a **Kategória** és az **Egység** mező kombinációjára, akkor az önköltségi ráta alapértelmezés szerint megjelenik. Ha a rendszer nem tudja egyeztetni a **Kategória** és az **Egység** értékeket, vagy ha talál egy megfelelő kategóriaársort, de az árképzési mód nem az **Egységár**, akkor a költségarány az alapértelmezett nulla (0) lesz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]