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
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286521"
---
# <a name="resource-estimates"></a><span data-ttu-id="090de-103">Erőforrásbecslések</span><span class="sxs-lookup"><span data-stu-id="090de-103">Resource estimates</span></span>

<span data-ttu-id="090de-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="090de-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="090de-105">Az erőforrás-becslések a megfelelő árképzési dimenziókkal rendelkező munkalebontási struktúrában meghatározott időfázisos erőfeszítésből származnak.</span><span class="sxs-lookup"><span data-stu-id="090de-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="090de-106">A számítások általában: **arány/hr érték az egyes szerepkörökhöz x órák száma**.</span><span class="sxs-lookup"><span data-stu-id="090de-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="090de-107">Az egyes erőforrások időfázisos erőfeszítéseit az erőforrás-hozzárendelési rekord tárolja.</span><span class="sxs-lookup"><span data-stu-id="090de-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="090de-108">Az árazás egy előre megadott árlistában van tárolva.</span><span class="sxs-lookup"><span data-stu-id="090de-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="090de-109">Az egységek átváltása a megfelelő árlista alapján kerül alkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="090de-109">Unit conversion is applied based on the applicable price list.</span></span>

![Erőforrásbecslések](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="090de-111">Alapértelmezett önköltségi ár és költségpénznem</span><span class="sxs-lookup"><span data-stu-id="090de-111">Default cost price and cost currency</span></span>

<span data-ttu-id="090de-112">Az önköltségi árak alapértelmezés szerint a szervezeti egységből származnak.</span><span class="sxs-lookup"><span data-stu-id="090de-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="090de-113">Alapértelmezett számlázási gyakoriság és értékesítési pénznem</span><span class="sxs-lookup"><span data-stu-id="090de-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="090de-114">Az értékesítési árak egy alkalommal kerülnek alkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="090de-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="090de-115">Az értékesítési árlista alapértelmezett hierarchiája a következő:</span><span class="sxs-lookup"><span data-stu-id="090de-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="090de-116">Cég</span><span class="sxs-lookup"><span data-stu-id="090de-116">Organization</span></span>
2. <span data-ttu-id="090de-117">Ügyfél</span><span class="sxs-lookup"><span data-stu-id="090de-117">Customer</span></span>
3. <span data-ttu-id="090de-118">Árajánlat/szerződés</span><span class="sxs-lookup"><span data-stu-id="090de-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]