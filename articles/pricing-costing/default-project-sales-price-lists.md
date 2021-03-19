---
title: Alapértelmezett árlisták
description: Ez a témakör az alapértelmezett értékesítési és önköltségi árlistákról nyújt tájékoztatást a Project Operations alkalmazásban.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 04c97429ab8ac769dd22b4127432d80de8fde937
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275586"
---
# <a name="default-price-lists"></a>Alapértelmezett árlisták

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

## <a name="sales-price-lists"></a>Értékesítési árlisták

A Dynamics 365 Project Operations rendszerben minden projektajánlat és szerződés tartalmaz egy alapértelmezett értékesítési árlistát. 

### <a name="price-list-default-on-project-quotes"></a>Árlista alapértelmezései a projektajánlatokban
A rendszer a következő folyamatot hajtja végre annak meghatározásához, hogy mely árlista legyen alapértelmezett a projektajánlatban:

1. A rendszer megvizsgálja azokat az árlistákat, amelyek a partner projektárlistáihoz kapcsolódnak. 
2. Ha a partner bejegyzéséhez a projektárlisták vannak csatolva, akkor a rendszer a projekthez tartozó paraméterekhez csatolt értékesítési árlistát keresi meg, amelyek megfelelnek a projektajánlat pénznemének.
3. Következő lépésként a rendszer ellenőrzi a projekt ajánlat hatályossági dátumának megfelelő hatályosságú árlistákat. Pontosan azt a dátumot, amikor az árajánlatot létrehozták.
4. Ha több árlista is van, amelyek a projekt ajánlatának dátumán hatályosak, akkor az összes árlista alapértelmezés szerint szerepel a projektajánlatban.
5. Ha a projektajánlat dátumára vonatkozóan nincs hatályos árlista, akkor a projektárajánlatban nem szerepel alapértelmezett árlista. A projekt ajánlatában egy figyelmeztető üzenet fog megjelenni. Az üzenet jelzi, hogy mivel nincsenek csatolt projektárlisták, a becsült és a tényleges projektmunka és -költségek nem lesznek beárazva.

### <a name="price-list-default-on-project-contracts"></a>Árlista alapértelmezései a projektszerződésekben 
A rendszer a következő folyamatot hajtja végre annak meghatározásához, hogy mely árlista legyen alapértelmezett a projektszerződésben:

1. Ha a szerződés ajánlatból jön létre, akkor az ajánlaton szereplő projekt-árlisták átmásolása külön történik, és a projektszerződéshez kapcsolódik.
2. Ha a szerződés a semmiből jön létre, akkor a rendszer megnézi azokat az árlistákat, amelyek a Partner projektárlistáihoz kapcsolódnak. Ha a partner bejegyzéséhez a projektárlisták nincsenek csatolva, akkor a rendszer a projekthez tartozó paraméterekhez csatolt értékesítési árlistát keresi meg, amelyek megfelelnek a projektszerződés pénznemének.
4. Következő lépésként a rendszer ellenőrzi a projektszerződés hatályossági dátumának megfelelő hatályosságú árlistákat. Pontosan azt a dátumot, amikor a szerződést létrehozták.
5. Ha több árlista is van, amelyek a projektszerződés dátumán hatályosak, akkor az összes árlista alapértelmezés szerint szerepel a projektszerződésben.
6. Ha a projektszerződés dátumára vonatkozóan nincs hatályos árlista, akkor a projektszerződésben nem szerepel alapértelmezett árlista. A projektszerződésben egy figyelmeztető üzenet fog megjelenni. Az üzenet jelzi, hogy mivel nincsenek csatolt projektárlisták, a becsült és a tényleges projektmunka és -költségek nem lesznek beárazva.

## <a name="cost-price-lists"></a>Önköltségiár-listák

A önköltségi árlisták nem alapértelmezettek a Project Operations alkalmazásban szereplő bármely entitáshoz. Az önköltségi árlisták meghatározására a projekt költségeihez való használathoz mindig az adott pillanatban kerül sor. A rendszer a következő folyamatot hajtja végre annak meghatározásához, hogy mely árlista legyen használva a projekt önköltségéhez:

1. A rendszer először a projektajánlatkérő szervezeti egységéhez kapcsolt árlisták listáját vizsgálja meg.
2. A rendszer ezt követően azon árlisták hatályossági dátumát tekinti meg, amelyek megfelelnek a bejövő becslés vagy a tényleges sor dátumának. Ebben az esetben a *becslési sor* a Project Operations alkalmazásban a becslések mindhárom kontextusára vonatkozik:

    - Projektbecslési sor
    - Árajánlatsor részletei
    - Szerződéssor részletei
  
3. Ha a bejövő becslésen vagy a tényleges időpont dátumára vonatkozóan több olyan árlista is van, a legutóbb létrehozott árlista lesz kiválasztva.
4. Ha a projekt szerződő szervezeti egységéhez nincsenek árlisták csatolva, akkor a rendszer a projekthez tartozó paraméterekhez csatolt önköltségi árlistát keresi meg, amelyek megfelelnek a projektajánlat pénznemének.
5. A rendszer ezt követően azon árlisták hatályossági dátumát tekinti meg, amelyek megfelelnek a bejövő becslés vagy a tényleges sor dátumának. 
6. Ha a bejövő becslésen vagy a tényleges időpont dátumára vonatkozóan több olyan árlista is van, a legutóbb létrehozott árlista lesz kiválasztva.
7. Ha nincsenek olyan árlisták csatolva a projektparaméterekhez, amelyek megfelelnek a pénznemnek és az érvényességi dátumnak a rendszer alapértelmezetten nullára (0) állítja az önköltségi árat a bejövő becslésen vagy tényleges soron.


[!INCLUDE[footer-include](../includes/footer-banner.md)]