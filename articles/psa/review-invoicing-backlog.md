---
title: Tekintse át a projektek és a projektszerződések számlázási hátralékát
description: Ez a témakör információkat nyújt arról, hogy miként lehet áttekinteni az időt, a költségeket és a termékmaradványokat, és hogyan jelölheti meg őket készen a számlázásra.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: bdeeb100614cda78d0ba536310bb6b411c863b71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282786"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Tekintse át a projektek és a projektszerződések számlázási hátralékát

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ha egy tranzakció kész, hogy egy számlát létrehozott és feldolgozott, a tranzakciót **Számlázásra kész**-ként kell jelölni. Ez a témakör leírja a létrehozható tranzakciók típusait.

## <a name="review-the-time-and-material-billing-backlog"></a>Tekintse át az idő- és anyagszámlázási elmaradást

Amikor egy idő- vagy költségbejegyzés benyújtásra és a projekt jóváhagyására kerül sor, a PSA ténylegesen létrehozza a projektet. Ha a projekt és a tranzakciós osztály kombinációját egy idő- és anyagprojekt szerződési sorához rendelik, akkor a bejegyzés jóváhagyásakor két aktuális jön létre:

- Tényleges költség 
- Számlázatlan értékesítés tényleges

A nem értékesített tényleges tényezők a számlázási lemaradást képviselik, és számlázási állapotukat **Számlázásra kész**-re kell állítani. A projektszámla létrehozásakor a **Számlázásra kész** jelöléssel ellátott számlázatlan értékesített aktuális tényleges adatok számla sor részleteként kerülnek átmásolásra.

Az idő és az anyagok és a számlázási hátralék áttekintéséhez keresse meg az **Értékesítés** \> **Számlázás** \> **Idő és anyag számlázás hátralék** oldalát. Válassza ki az összes nem beépített értékesítési aktuális terméket, amely készen áll a számlázásra, majd válassza a **Számlázásra kész** lehetőséget. Ezeknek a tényleges értékeknek a számlázási állapota megváltozik: **Számlázásra kész**.

![Idő és anyag számlázási elmaradás](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Tekintse át a termék számlázási hátralékát

A PSA-ban, ha egy projektszerződés termék-alapú szerződéses sorokkal rendelkezik, akkor ezeket a sorokat számlázáskor veszik figyelembe, amikor a projekt-szerződéshez számlát készítenek. Azokat a termékeket, amelyek szerződéses soraival **Számlázásra kész** jelöléssel, a projekt számlájára másolják át a projekt számlára.

A termékek és a számlázási hátralék áttekintéséhez keresse meg az **Értékesítés** \> **Számlázás** \> **Termék számlázás hátralék** oldalát. Válassza ki az összes termék-alapú szerződés sort, amely készen áll a számlázásra, majd válassza a **Számlázásra kész** értéket. Ezeknek a soroknak a számlázási állapota megváltozik: **Számlázásra kész**.

![Termék számlázási elmaradása](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Tekintse át a rögzített árú szerződések számlázási mérföldköveit

Minden rögzített árú számlázási módszerrel rendelkező projektszerződés-sornak meg kell határoznia a szerződés mérföldköveit. Ezeket a szerződéses mérföldköveket csak akkor lehet számlázni, ha **készen állnak a számlázásra**. 

A számlázási mérföldkövek áttekintéséhez nyissa meg az **Értékesítés** \> **Számlázás** \> **Rögzített árú mérföldkövek** oldalt. Válassza ki azokat a mérföldköveket, amelyek készen állnak a számlázásra, majd válassza a **Számlázásra kész** elemet. Ezeknek a mérföldköveknek a számlázási állapota megváltozik: **Számlázásra kész**.

![Rögzített árú mérföldkövek](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]