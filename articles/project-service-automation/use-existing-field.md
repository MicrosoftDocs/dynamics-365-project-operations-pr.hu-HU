---
title: Használjon egy meglévő mezőt a Project Service-ben árképzési dimenzióként
description: Ez a témakör ismerteti a meglévő Project Service mezők árazási dimenzióként történő használatát.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: ed86e0c4-b2ea-4b3b-b9e3-cbfb3b512591
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: b280e2aeecc9d63fb65b77fad809edff817aff65
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752232"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>Használjon egy meglévő mezőt a Project Service-ben árképzési dimenzióként

A Project Service Automation (PSA) az **Aktuális** entitáson számos mezőt tartalmaz, amelyek felhasználhatók árazási dimenziókként az erőforrás alapú árazáshoz a projekt szervezetekben. Például egy közös mező a **Foglalható erőforrás**. Kisebb, 20-30-nél kevesebb számlázható erőforrással rendelkező cégeknél egyszerűbb megközelítés lehet az egyes erőforrásokra jellemző számla- és költségráták meghatározása. A számlázható munkaerő növekedésével azonban ez irreális lehet fenntartani, mivel az erőforrás költségek és a számlázási arányok változnak, amikor az erőforrásokat promócióba kezdik, több tapasztalatot szereznek, vagy más készségeket szereznek. Mivel ez a megközelítés továbbra is működik egy bizonyos méretű vállalatnál, olvassa el a témát: [Használjon foglalható erőforrást árképzési dimenzióként](bookable-resource-pricing-dimension.md), hogy megértse, hogyan lehet egy létező Project Service mezőt használni árazási dimenzióként.

Egy másik példa a tranzakciós kategória. Az ügyfelek és az implementálók a PSA tranzakciós kategóriáját használják a munka osztályozására, és a mező használatára az ár és a költség alapján a munka kategóriája alapján. További információ: [Tranzakciós kategória használata árképzési dimenzióként](transaction-category-pricing-dimension.md).
