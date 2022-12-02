---
title: Erőforrásokhoz kapcsolódó idő pénzügyi becslései projekteknél
description: Ez a cikk az idő pénzügyi becslésének kiszámításáról nyújt tájékoztatást.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03416feb178d883bba57dc14692049503b151ffd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913531"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Erőforrásokhoz kapcsolódó idő pénzügyi becslései projekteknél

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az időre pénzügyi becsléseket három tényező alapján számítják ki: 

- A projektterv egyes levélcsomópont-feladathoz rendelt általános vagy elnevezett csoporttag típusa. 
- A munka típusa vagy összetettsége.
- Az erőforrás hozzárendelésének elosztása a feladaton. 

Az első két tényező befolyásolja az erőforrás hozzárendelésének egységköltségét vagy számlázási arányát. Az erőforrás-hozzárendelés egységköltségét vagy számlázási arányát a hozzárendelt erőforrás attribútumai határozzák meg. Ezek az attribútumok magukban foglalják azt a szervezeti egységet, amelyhez az erőforrás tartozik, valamint az erőforrás szabványos szerepkörét. Az erőforráshoz a vállalkozás számára releváns egyéni attribútumokat is hozzáadhat, például standard címet vagy tapasztalati szintet, és beállíhatja ezeket úgy, hogy befolyásolják a hozzárendelés egységköltségét vagy számlázási arányát.
Az erőforrás attribútumai mellett a munka attribútumai, például a feladat, szintén befolyásolhatják a hozzárendelés egységszámlázási arányát vagy költségarányát. Ha például bizonyos feladatok összetettebbek, az erőforrás hozzárendelése ezekhez a feladatokhoz magasabb egységköltséget vagy számlázási arányt eredményez, mint a kevésbé összetett feladatokhoz.   

A harmadik tényező biztosítja az órák mennyiségét az adott arányban. Azokban az esetekben, amikor egy feladat két áridőszakot fed le, valószínű, hogy az adott feladat erőforrás-hozzárendelésének első része a feladat második részének költségszámítása és ára eltér. Az egyes erőforrás-hozzárendelések ráfordítás-becslése összetett érték, amely a napi ráfordítás napi eloszlását tárolja.

A munka és az erőforrások egyéni attribútumainak árképzési és költségszámítási dimenzióként való beállításáról az [Árképzési dimenziók áttekintése](../pricing-costing/pricing-dimensions-overview.md) témakörben talál részletes utasításokat.

Az egyes erőforrás-hozzárendelések pénzügyi becslése a **hozzárendelés díj/óra és az órák számának szorzataként kerül kiszámításra.**  Az erőfeszítés-becsléshez hasonlóan az egyes erőforrás-hozzárendelések költségére és bevételére vonatkozó pénzügyi becslés egy összetett érték, amely a napi pénzösszeg napi elosztásával van tárolva. 

## <a name="summarizing-financial-estimates-for-time"></a>Az idő pénzügyi becsléseinek összefoglalása
A levélcsomópont-feladat időre vonatkozó pénzügyi becslése az adott feladathoz szükséges összes erőforrás-hozzárendelésre vonatkozó pénzügyi becslések összege.

Az összegző vagy szülő feladat időre vonatkozó pénzügyi becslése az összes gyermek feladatára vonatkozó pénzügyi becslések összege. Ez a projekt becsült munkaköltsége. 

![Erőforrásbecslések.](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Alapértelmezett önköltségi ár és költségpénznem

Az alapértelmezett önköltségi ár a projekt szerződéskötési egységéhez csatolt árlistákból származik. A projekt költségpénzneme mindig a projektben szereplő szerződő egység pénzneme. Az erőforrás-hozzárendelésen a költségre vonatkozó pénzügyi becslés a projekt költségpénznemében tárolódik. Néha az a pénznem, amelyben a költségárfolyam be van állítva az árlistában, eltér a projekt költségpénznemétől. Ezekben az esetekben az alkalmazás átváltja azt a pénznemet, amelyben az önköltségi ár a projekt pénznemére van beállítva. A **Becslések** rácson az összes költségbecslés megjelenik és össze van foglalva a projekt költségpénznemében. 

## <a name="default-bill-rate-and-sales-currency"></a>Alapértelmezett számlázási gyakoriság és értékesítési pénznem

Az alapértelmezett értékesítési ár a kapcsolódó projektszerződéshez csatolt projektárlistákból származik, ha meg lett nyerve az üzlet, vagy a kapcsolódó projektárajánlatból, ha az üzlet még az értékesítés előtti szakaszban van. A projekt értékesítési pénzneme mindig a projektben szereplő projekt árajánlatának vagy a projektszerződés pénzneme. Az erőforrás-hozzárendelésen az értékesítésre vonatkozó pénzügyi becslés a projekt értékesítési pénznemében tárolódik. A költségtől eltérően az árlistában beállított értékesítési ár soha nem különbözhet a projekt értékesítési pénznemétől. Nincs olyan forgatókönyv, amelyben valutaátváltásra lenne szükség. A **Becslések** rácson az összes értékesítésbecslés megjelenik és össze van foglalva a projekt értékesítési pénznemében. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
