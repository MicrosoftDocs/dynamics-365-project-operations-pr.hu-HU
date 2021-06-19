---
title: Az önköltségi árak megoldása a becsléseken és a tényeken
description: Ez a témakör arról nyújt tájékoztatást, hogy a költségárakat hogyan használják a projektbecslésekhez, és a tényadatok hogyan lesznek megoldva.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6b42bc97251aec7259d314fe51b3a012edf597aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004399"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Az önköltségi árak megoldása a becsléseken és a tényeken 

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

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Költségárak megoldása a tényekhez és a becslésekhez az Anyag számára

Az Anyagra vonatkozó becsléssorok az anyagra vonatkozó ajánlatsor- és szerződéssor-részletekre hivatkoznak, valamint a projekt anyagbecslését jelölik.

Az önköltségi árlista feloldása után a rendszer a becsült sor **Termék** és **Kiszerelés** mezőinek kombinációját használja az anyagbecsléshez, hogy megfeleljen a feloldott árlista **Árlistaelemek** sorainak. Ha a rendszer olyan termékársort talál, amely a **Termék** és **Kiszerelés** mezőkombináció költségarányát tartalmazza, a költségarány alapértelmezettre lesz beállítva. Ha a rendszer nem tudja összeegyeztetni a **Termék** és **Kiszerelés** értékeket, vagy ha meg tudja találni az egyező árlistaelemsort, de az árképzési módszer a Standard költségen vagy a Jelenlegi költségen alapul, és egyik sincs meghatározva a terméken, akkor a kiszerelésköltség alapértelmezés szerint nulla.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
