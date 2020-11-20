---
title: Project Operations-mezők mint árképzési dimenziók
description: Ez a témakör a mezőknek a Dynamics 365 Project Operations árképzési dimenzióiként való használatáról nyújt információkat.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 59367b35f15f806b109f606e912edc487d9e7685
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119241"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="4b083-103">Project Operations-mezők mint árképzési dimenziók</span><span class="sxs-lookup"><span data-stu-id="4b083-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="4b083-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="4b083-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4b083-105">A **Tények** entitás számos olyan mezőt tartalmaz, amelyek használható árképzési dimenzióként erőforrásalapú árképzéshez.</span><span class="sxs-lookup"><span data-stu-id="4b083-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="4b083-106">Például egy közös mező a **Foglalható erőforrás**.</span><span class="sxs-lookup"><span data-stu-id="4b083-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="4b083-107">Kisebb, 20-30-nél kevesebb számlázható erőforrással rendelkező cégeknél egyszerűbb megközelítés lehet az egyes erőforrásokra jellemző számla- és költségráták meghatározása.</span><span class="sxs-lookup"><span data-stu-id="4b083-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="4b083-108">Ahogy azonban a számlázható munkaerő nő, az erőforrás-specifikus arányok irreálisá válhatnak.</span><span class="sxs-lookup"><span data-stu-id="4b083-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="4b083-109">Az erőforrások kinevezésével, tapasztaltabbá válásával párhuzamosan, illetve ahogy az erőforrások új készségeket szereznek, az erőforrások költsége és a számlázási díjak módosulnak.</span><span class="sxs-lookup"><span data-stu-id="4b083-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="4b083-110">Egy másik példa a tranzakciós kategória.</span><span class="sxs-lookup"><span data-stu-id="4b083-110">Another example is that of transaction category.</span></span> <span data-ttu-id="4b083-111">Az ügyfelek és az implementálók a tranzakciós kategóriát használják a munka osztályozására, és a mező használatára az ár és a költség alapján a munka kategóriája alapján.</span><span class="sxs-lookup"><span data-stu-id="4b083-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
