---
title: Erőforrásbecslések
description: Ez a témakör az erőforrásbecslések Project Operations rendszerben történő számításának módjáról tartalmaz tájékoztatást.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127366"
---
# <a name="resource-estimates"></a><span data-ttu-id="8c64b-103">Erőforrásbecslések</span><span class="sxs-lookup"><span data-stu-id="8c64b-103">Resource estimates</span></span>

<span data-ttu-id="8c64b-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="8c64b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8c64b-105">Az erőforrás-becslések a megfelelő árképzési dimenziókkal rendelkező munkalebontási struktúrában meghatározott időfázisos erőfeszítésből származnak.</span><span class="sxs-lookup"><span data-stu-id="8c64b-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="8c64b-106">A számítások általában: **arány/hr érték az egyes szerepkörökhöz x órák száma**.</span><span class="sxs-lookup"><span data-stu-id="8c64b-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="8c64b-107">Az egyes erőforrások időfázisos erőfeszítéseit az erőforrás-hozzárendelési rekord tárolja.</span><span class="sxs-lookup"><span data-stu-id="8c64b-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="8c64b-108">Az árazás egy előre megadott árlistában van tárolva.</span><span class="sxs-lookup"><span data-stu-id="8c64b-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="8c64b-109">Az egységek átváltása a megfelelő árlista alapján kerül alkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="8c64b-109">Unit conversion is applied based on the applicable price list.</span></span>

![Erőforrásbecslések](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="8c64b-111">Alapértelmezett önköltségi ár és költségpénznem</span><span class="sxs-lookup"><span data-stu-id="8c64b-111">Default cost price and cost currency</span></span>

<span data-ttu-id="8c64b-112">Az önköltségi árak alapértelmezés szerint a szervezeti egységből származnak.</span><span class="sxs-lookup"><span data-stu-id="8c64b-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="8c64b-113">Alapértelmezett számlázási gyakoriság és értékesítési pénznem</span><span class="sxs-lookup"><span data-stu-id="8c64b-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="8c64b-114">Az értékesítési árak egy alkalommal kerülnek alkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="8c64b-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="8c64b-115">Az értékesítési árlista alapértelmezett hierarchiája a következő:</span><span class="sxs-lookup"><span data-stu-id="8c64b-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="8c64b-116">Cég</span><span class="sxs-lookup"><span data-stu-id="8c64b-116">Organization</span></span>
2. <span data-ttu-id="8c64b-117">Ügyfél</span><span class="sxs-lookup"><span data-stu-id="8c64b-117">Customer</span></span>
3. <span data-ttu-id="8c64b-118">Árajánlat/szerződés</span><span class="sxs-lookup"><span data-stu-id="8c64b-118">Quote/contract</span></span>
