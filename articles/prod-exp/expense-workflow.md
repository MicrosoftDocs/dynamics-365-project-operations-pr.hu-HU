---
title: Költségkezelési munkafolyamat
description: Ez a témakör elmagyarázza, hogyan használható a Microsoft Dynamics 365 Finance munkafolyamatrendszere a költségjelentések felülvizsgálatának beállításához a Költségkezelésben.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51ac2712f62d5c5d85b21c0ea929517ccb893bca
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005209"
---
# <a name="expense-management-workflow"></a>Költségkezelési munkafolyamat

A munkafolyamatrendszert használhatja a költségjelentések felülvizsgálatának beállításához a Költségkezelésben. Beállíthat egy munkafolyamatot, amely a következő feltételeket használja a költségjelentés jóváhagyójának meghatározásához:

- Az alkalmazottak beosztási hierarchiája és az előre meghatározott jóváhagyási korlátok
- Többszintű jóváhagyás, amely támogatja az ideiglenes jóváhagyókat és a végső jóváhagyót
- Pénzügyi dimenziók és a projekt felelősségvállalása
- Adott felhasználókhoz vagy felhasználói csoportokhoz való hozzárendelés

Munkafolyamat-jóváhagyások létrehozhatók költségjelentés, utazási igénylés, készpénzelőleg és forgalmi adó (ÁFA) helyreállításához.

**Példa**

A következő folyamat egy Költségjelentég költségkezelési munkafolyamatára mutat be példát.

1. Egy alkalmazott létrehoz és elment egy költségjelentést.
2. Az alkalmazott beküldi költségjelentést jóváhagyásra. A jóváhagyót a munkafolyamat beállításakor meghatározott szabályok alapján határozzák meg.
3. A jóváhagyó értesítést kap, hogy a költségjelentés készen áll a jóváhagyásra. A jóváhagyó felülvizsgálja a költségjelentést, és ellenőrzi, hogy teljesülnek-e az alábbi feltételek:

    - A kiadások nem ütköznem semmilyen költségszabályzatba. Ha egy költség egy szabályzatba ütközik, a jóváhagyó ellenőrzi, hogy a költségjelentés tartalmaz-e érvényes üzleti indokolást.
    - A költségjelentésekhez elektronikus nyugták vannak csatolva.

4. A jóváhagyó jóváhagyja a költségjelentést.
5. A költségjelentés a Kötelezettségek koordinátorához van rendelve feladás céljából.
6. A következő lépések egyike történik, attól függően, hogy az automatikus feladás be van-e állítva:

    - Ha az automatikus feladás be van állítva, a költségjelentés feldolgozása kifizetéshez megtörténik, és a költségjelentés állapota frissül.
    - Ha nincs konfigurálva az automatikus feladás, a Kötelezettségek koordinátora ellenőrzi, hogy az összes eredeti nyugtát beküldték-e, és hogy a nyugták összhangban vannak-e a költségjelentés költségeivel. A költségjelentéshez megadott összes áfakódnak helyesnek kell lennie.

A követelmények ellenőrzése után a költségjelentés feladása megtörténik.

A költségjelentés feladása után a költségjelentéshez tartozó kifizetés engedélyezve lesz, és az alkalmazott visszatérítést kap.


[!INCLUDE[footer-include](../includes/footer-banner.md)]