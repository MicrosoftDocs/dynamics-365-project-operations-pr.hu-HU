---
title: Használjon egy meglévő mezőt a Project Service-ben árképzési dimenzióként
description: Ez a témakör ismerteti a meglévő Project Service mezők árazási dimenzióként történő használatát.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 09e565c91eda9dee6e0ec479a5c85d94d2591147
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008089"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>Használjon egy meglévő mezőt a Project Service-ben árképzési dimenzióként

[!include [banner](../includes/psa-now-project-operations.md)]

A Project Service Automation (PSA) az **Aktuális** entitáson számos mezőt tartalmaz, amelyek felhasználhatók árazási dimenziókként az erőforrás alapú árazáshoz a projekt szervezetekben. Például egy közös mező a **Foglalható erőforrás**. Kisebb, 20-30-nél kevesebb számlázható erőforrással rendelkező cégeknél egyszerűbb megközelítés lehet az egyes erőforrásokra jellemző számla- és költségráták meghatározása. A számlázható munkaerő növekedésével azonban adott arányokat irreális lehet fenntartani, mivel az erőforrás költségek és a számlázási arányok változnak, amikor az erőforrásokat promócióba kezdik, több tapasztalatot szereznek, vagy más készségeket szereznek. Mivel ez a megközelítés továbbra is működik egy bizonyos méretű vállalatnál, olvassa el: [Használjon foglalható erőforrást árképzési dimenzióként](bookable-resource-pricing-dimension.md), hogy megértse, hogyan lehet egy létező Project Service mezőt használni árazási dimenzióként.

Egy másik példa a tranzakciós kategória. Az ügyfelek és az implementálók a PSA tranzakciós kategóriáját használják a munka osztályozására, és a mező használatára az ár és a költség alapján a munka kategóriája alapján. További információ: [Tranzakciós kategória használata árképzési dimenzióként](transaction-category-pricing-dimension.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]