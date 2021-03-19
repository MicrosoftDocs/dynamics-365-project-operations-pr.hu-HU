---
title: Használjon egy meglévő mezőt a Project Service-ben árképzési dimenzióként
description: Ez a témakör ismerteti a meglévő Project Service mezők árazási dimenzióként történő használatát.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ad03f5f7c1c9e93ca12a8c8d48ffbd2f80b1511f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281571"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>Használjon egy meglévő mezőt a Project Service-ben árképzési dimenzióként

[!include [banner](../includes/psa-now-project-operations.md)]

A Project Service Automation (PSA) az **Aktuális** entitáson számos mezőt tartalmaz, amelyek felhasználhatók árazási dimenziókként az erőforrás alapú árazáshoz a projekt szervezetekben. Például egy közös mező a **Foglalható erőforrás**. Kisebb, 20-30-nél kevesebb számlázható erőforrással rendelkező cégeknél egyszerűbb megközelítés lehet az egyes erőforrásokra jellemző számla- és költségráták meghatározása. A számlázható munkaerő növekedésével azonban adott arányokat irreális lehet fenntartani, mivel az erőforrás költségek és a számlázási arányok változnak, amikor az erőforrásokat promócióba kezdik, több tapasztalatot szereznek, vagy más készségeket szereznek. Mivel ez a megközelítés továbbra is működik egy bizonyos méretű vállalatnál, olvassa el: [Használjon foglalható erőforrást árképzési dimenzióként](bookable-resource-pricing-dimension.md), hogy megértse, hogyan lehet egy létező Project Service mezőt használni árazási dimenzióként.

Egy másik példa a tranzakciós kategória. Az ügyfelek és az implementálók a PSA tranzakciós kategóriáját használják a munka osztályozására, és a mező használatára az ár és a költség alapján a munka kategóriája alapján. További információ: [Tranzakciós kategória használata árképzési dimenzióként](transaction-category-pricing-dimension.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]