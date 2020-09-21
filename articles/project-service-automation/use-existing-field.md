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
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="c1030-103">Használjon egy meglévő mezőt a Project Service-ben árképzési dimenzióként</span><span class="sxs-lookup"><span data-stu-id="c1030-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="c1030-104">A Project Service Automation (PSA) az **Aktuális** entitáson számos mezőt tartalmaz, amelyek felhasználhatók árazási dimenziókként az erőforrás alapú árazáshoz a projekt szervezetekben.</span><span class="sxs-lookup"><span data-stu-id="c1030-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="c1030-105">Például egy közös mező a **Foglalható erőforrás**.</span><span class="sxs-lookup"><span data-stu-id="c1030-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="c1030-106">Kisebb, 20-30-nél kevesebb számlázható erőforrással rendelkező cégeknél egyszerűbb megközelítés lehet az egyes erőforrásokra jellemző számla- és költségráták meghatározása.</span><span class="sxs-lookup"><span data-stu-id="c1030-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="c1030-107">A számlázható munkaerő növekedésével azonban ez irreális lehet fenntartani, mivel az erőforrás költségek és a számlázási arányok változnak, amikor az erőforrásokat promócióba kezdik, több tapasztalatot szereznek, vagy más készségeket szereznek.</span><span class="sxs-lookup"><span data-stu-id="c1030-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="c1030-108">Mivel ez a megközelítés továbbra is működik egy bizonyos méretű vállalatnál, olvassa el a témát: [Használjon foglalható erőforrást árképzési dimenzióként](bookable-resource-pricing-dimension.md), hogy megértse, hogyan lehet egy létező Project Service mezőt használni árazási dimenzióként.</span><span class="sxs-lookup"><span data-stu-id="c1030-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="c1030-109">Egy másik példa a tranzakciós kategória.</span><span class="sxs-lookup"><span data-stu-id="c1030-109">Another example is that of transaction category.</span></span> <span data-ttu-id="c1030-110">Az ügyfelek és az implementálók a PSA tranzakciós kategóriáját használják a munka osztályozására, és a mező használatára az ár és a költség alapján a munka kategóriája alapján.</span><span class="sxs-lookup"><span data-stu-id="c1030-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="c1030-111">További információ: [Tranzakciós kategória használata árképzési dimenzióként](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="c1030-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>