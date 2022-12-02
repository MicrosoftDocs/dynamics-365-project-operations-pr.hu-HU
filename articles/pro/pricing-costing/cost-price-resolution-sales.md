---
title: Az önköltségi ráták meghatározása a becslésekhez és a tényadatokhoz
description: Ez a cikk arról nyújt tájékoztatást, hogy a költségárakat hogyan használják a projekt alapú becslésekhez, és a tényadatok hogyan lesznek meghatározva.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c2295174df1ce766c6d1304f4e9c55d32d5c4775
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475234"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Az önköltségi ráták meghatározása a becslésekhez és a tényadatokhoz

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Az önköltségi ráták meghatározásához a becsléseken és tényadatokon a Microsoft Dynamics 365 Project Operations alkalmazásban, a rendszer a bejövő becslés dátumát és pénznemét használja vagy az önköltségi árlista meghatározásához használt aktuális kontextust. A tényleges kontextusban a rendszer a **Tranzakció dátuma** mező segítségével határozza meg, hogy melyik árlista alkalmazandó. A rendszer összeveti a bejövő becslés vagy tényadat **Tranzakció dátum** értékét az árlista **Hatályos kezdő dátum (Időzónától független)** és **Hatályos befejező dátum (Időzónától független)** értékeivel. Az önköltségi árlistája meghatározását a rendszer meghatározza az önköltséget. 

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Önköltéségi árak meghatározása becslésben és aktuális környezetben Időhöz

Az **Idő** becsült környezete a következőre utal:

- Árajánlatsor részletei **Időhöz**.
- Szerződéssor részletei **Időhöz**.
- Erőforrás-hozzárendelések egy projektben.

Az **Idő** aktuális környezete a következőre utal:

- A Beviteli és Helyesbítési napló sorai az **Időhöz**.
- Időbejegyzés beküldésekor létrehozott naplósorok.

Miután meghatározásara került egy önköltségi árlista, a rendszer a következő lépéseket hajtja végre a önköltségi ráta alapértelmezett értékének megadásához.

1. A rendszer a becslésben található **Szerepkör** és **Erőforrás-kezelési egység** mezők kombinációjával vagy az **Idő** aktuális kontextusával a szerepkörársorokkal a árlistában. Ez az egyeztetés feltételezi, hogy a munkaerőköltséghez a szokásos árképzési dimenziókat használja. Ha bármely más mező alapján konfigurálja az árképzést a rendszerben, vagy a **Szerepkör** és az **Erőforrás-kezelési egység** mellett más mezőket is használ, akkor a rendszer ezzel a kombinációval kéri le az egyező szerepkörársort.
1. Ha a rendszer egy olyan szerepkörársort talál, amely rendelkezik önköltségi rátával a **Szerepkör**, **Erőforrás-kezelő egység** és az erőforrás-kezelési egység mező kombinációjával, az az önköltségi ráta lesz használva alapértelmezett önköltségi rátaként.
1. Ha a rendszer nem tudja egyeztetni a **Szerepkör** és az **Erőforrás-kezelő egység** értékeit, akkor lekéri azokat a szerepkörársorokat, amelyek egyező értékekkel rendelkeznek a **Szerepkör** mezőhöz, de nulla értékekkel az **Erőforrás-kezelő részleg** mezőhöz. Ha a rendszer rendelkezik egy megfelelő szerepkörárrekorddal, akkor ennek a rekordnak az önköltésgi rátája lesz használva alapértelmezett önköltségi rátaként.

> [!NOTE]
> Ha eltérő prioritást állított be a **Szerepkör** és **Erőforrás-kezelési egység** mezőkhöz, vagy ha más, magasabb prioritású dimenziók találhatók, az előző viselkedés ennek megfelelően változik. A rendszer lekéri a szerepkörár rekordokat, amelyek olyan értékekkel rendelkeznek, amely megegyezik az egyes árképzési dimenziók értékével a prioritás sorrendjében. A dimenziókhoz null értékkel rendelkező sorok következnek utoljára.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>A tényadat és a becslési sorok önköltségi díjainak meghatározása Költséghez

A **Költség** becsült környezete a következőre utal:

- Árajánlatsor részletei **Költésghez**.
- Szerződéssor részletei **Költésghez**.
- Költségbecslések a projektben

A **Költség** aktuális környezete a következőre utal:

- A Beviteli és Helyesbítési napló sorai a **Költséghez**.
- Költségbejegyzés beküldésekor létrehozott naplósorok.

Miután meghatározásara került egy önköltségi árlista, a rendszer a következő lépéseket hajtja végre a önköltségi ráta alapértelmezett értékének megadásához.

1. A rendszer a becslésben található **Kategória** és **Egység** mezők kombinációjával vagy az **Költség** aktuális kontextusával a kategória-ársorokkal az árlistában.
1. Ha a rendszer egy olyan kategória-ársort talál, amely rendelkezik önköltségi rátával a **Kategória** és az **Egység** mező kombinációjára, akkor az önköltségi ráta lesz használva alapértelemezett önköltségi rátaként.
1. Ha a rendszer nem tudja összeegyeztetni a **Kategória** és az **Egység** értékeket, az ár alapértelmezetten **0**-ra nullára csökken.
1. A becslési környezetben, ha a rendszer nem talál egyező kategóriaár sort, de az árképzési módszer nem **Egységár** az önköltségi ráta alapértelmezett beállítása **0** (nulla).

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Önköltségi ráták meghatározása a tényadatokhoz és a becslésekhez az Anyag számára

Az **Anyag** becsült környezete a következőre utal:

- Árajánlatsor részletei **Anyaghoz**.
- Szerződéssor részletei **Anyaghoz**.
- Anyagbecslések a projekten.

Az **Anyag** aktuális környezete a következőre utal:

- A Beviteli és Helyesbítési napló sorai **Anyaghoz**.
- Az Anyaghasználati napló beküldésekor létrehozott naplósorok.

Miután meghatározásara került egy önköltségi árlista, a rendszer a következő lépéseket hajtja végre a önköltségi ráta alapértelmezett értékének megadásához.

1. A rendszer a becslésben található **Termék** és **Egység** mezők kombinációját vagy az **Anyag** aktuális kontextusát használja a árlistaelem sorokkal szemben az árlistában.
1. Ha a rendszer egy olyan árlistaelemet talál, amely rendelkezik önköltségi rátával a **Termék** és az **Egység** mező kombinációjára, akkor az önköltségi ráta lesz használva alapértelemezett önköltségi rátaként.
1. Ha a rendszer nem tudja összeegyeztetni a **Termék** és **Kiszerelés** értékeket az egységár alapértelemezett beállítása **0** (nulla).
1. A becslési vagy tényadat környezetben, ha a rendszer nem talál egyező árlistaelem-sort, de az árképzési módszer nem **Pénznem összege** az önköltségi ráta alapértelmezett beállítása **0** (nulla). Ez a viselkedés azért fordul elő, mert a Project Operations a projektnél használt anyagok esetében csak **Pénznemösszeg** árképzési módot támogatja.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
