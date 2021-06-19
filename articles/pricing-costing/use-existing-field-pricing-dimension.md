---
title: Project Operations-mezők mint árképzési dimenziók
description: Ez a témakör a Dynamics 365 Project Operations rendszerben mezők árazási dimenzióként való használatáról nyújt információkat.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a29460b2a9dc9a9755e7e28a6cd9712c6b06e8c6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004489"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="25dae-103">Project Operations-mezők mint árképzési dimenziók</span><span class="sxs-lookup"><span data-stu-id="25dae-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="25dae-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="25dae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="25dae-105">A **Tények** entitás számos olyan mezőt tartalmaz, amelyek használható árképzési dimenzióként erőforrásalapú árképzéshez.</span><span class="sxs-lookup"><span data-stu-id="25dae-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="25dae-106">Például egy közös mező a **Foglalható erőforrás**.</span><span class="sxs-lookup"><span data-stu-id="25dae-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="25dae-107">Kisebb, 20-30-nél kevesebb számlázható erőforrással rendelkező cégeknél egyszerűbb megközelítés lehet az egyes erőforrásokra jellemző számla- és költségráták meghatározása.</span><span class="sxs-lookup"><span data-stu-id="25dae-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="25dae-108">Ahogy azonban a számlázható munkaerő nő, az erőforrás-specifikus arányok irreálisá válhatnak.</span><span class="sxs-lookup"><span data-stu-id="25dae-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="25dae-109">Az erőforrások kinevezésével, tapasztaltabbá válásával párhuzamosan, illetve ahogy az erőforrások új készségeket szereznek, az erőforrások költsége és a számlázási díjak módosulnak.</span><span class="sxs-lookup"><span data-stu-id="25dae-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="25dae-110">Egy másik példa a tranzakciós kategória.</span><span class="sxs-lookup"><span data-stu-id="25dae-110">Another example is that of transaction category.</span></span> <span data-ttu-id="25dae-111">Az ügyfelek és az implementálók a tranzakciós kategóriát használják a munka osztályozására, és a mező használatára az ár és a költség alapján a munka kategóriája alapján.</span><span class="sxs-lookup"><span data-stu-id="25dae-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]