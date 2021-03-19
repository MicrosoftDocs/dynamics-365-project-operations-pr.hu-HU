---
title: Beszerzési rendelések projekthez
description: A cikk ismerteti a projekthez tartozó beszerzési rendelések létrehozásához használható különböző módszereket. A használt metódus függ a beszerzési rendelés céljétól, hogy mikor használják fel a beszerzett cikkeket, és attól is, hogy mikor számítják fel a cikkeket a projekthez.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3f5d196e0d7db4a6d8c4cfe834a335f4ef737c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289192"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="6d774-104">Beszerzési rendelések projekthez</span><span class="sxs-lookup"><span data-stu-id="6d774-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d774-105">A cikk ismerteti a projekthez tartozó beszerzési rendelések létrehozásához használható különböző módszereket.</span><span class="sxs-lookup"><span data-stu-id="6d774-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="6d774-106">A használt metódus függ a beszerzési rendelés céljétól, hogy mikor használják fel a beszerzett cikkeket, és attól is, hogy mikor számítják fel a cikkeket a projekthez.</span><span class="sxs-lookup"><span data-stu-id="6d774-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="6d774-107">Beszerzési rendelés létrehozásának módszerei</span><span class="sxs-lookup"><span data-stu-id="6d774-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="6d774-108">A következő módszerekkel hozhat létre beszerzési rendelést a Projektmenedzsment és könyvelés részben.</span><span class="sxs-lookup"><span data-stu-id="6d774-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="6d774-109">A beszerzési rendelés célja meghatározza, hogy mikor használják fel a beszerzési rendelést, és ebből következően pedig azt is, hogy mikor számítják fel a cikkeket a projekthez.</span><span class="sxs-lookup"><span data-stu-id="6d774-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6d774-110">Módszer</span><span class="sxs-lookup"><span data-stu-id="6d774-110">Method</span></span></th>
<th><span data-ttu-id="6d774-111">Cél</span><span class="sxs-lookup"><span data-stu-id="6d774-111">Purpose</span></span></th>
<th><span data-ttu-id="6d774-112">Cikkek felhasználása</span><span class="sxs-lookup"><span data-stu-id="6d774-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6d774-113">Hozzon létre egy beszerzési megrendelést közvetlenül egy projektből.</span><span class="sxs-lookup"><span data-stu-id="6d774-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="6d774-114">Ezzel a módszerrel cikkeket vásárolhat egy külső szállítótól a projektben való felhasználás céljából.</span><span class="sxs-lookup"><span data-stu-id="6d774-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="6d774-115">A beszerzési rendelést az alábbi két módszerrel hozhatja létre:</span><span class="sxs-lookup"><span data-stu-id="6d774-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="6d774-116">Magából a projektből.</span><span class="sxs-lookup"><span data-stu-id="6d774-116">From the project itself.</span></span> <span data-ttu-id="6d774-117">Ebben az esetben a projekt már meg van adva a beszerzési rendeléshez.</span><span class="sxs-lookup"><span data-stu-id="6d774-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="6d774-118">A projekt beszerzési rendeléséhez navigálva.</span><span class="sxs-lookup"><span data-stu-id="6d774-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="6d774-119">A beszerzési rendelés létrehozásához a szállítót és a projektet is ki kell választania.</span><span class="sxs-lookup"><span data-stu-id="6d774-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="6d774-120">A cikkek a szállítói számla frissítésekor kerülnek felhasználásra.</span><span class="sxs-lookup"><span data-stu-id="6d774-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d774-121">Hozzon létre egy beszerzési rendelést közvetlenül egy értékesítési rendelésből.</span><span class="sxs-lookup"><span data-stu-id="6d774-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="6d774-122">Ennek a módszernek a használatával akkor vásároljon cikkeket, amikor értékesítési rendelést hoz létre egy projektből.</span><span class="sxs-lookup"><span data-stu-id="6d774-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="6d774-123">A cikkek akkor kerülnek felhasználásra, amikor az értékesítési rendelés ki van számlázva az ügyfélnek.</span><span class="sxs-lookup"><span data-stu-id="6d774-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d774-124">Hozzon létre egy beszerzési rendelést egy cikkszükségletből.</span><span class="sxs-lookup"><span data-stu-id="6d774-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="6d774-125">Ennek a módszernek a használatával akkor vásároljon cikkeket, amikor cikkszükségletet hoz létre egy projektből.</span><span class="sxs-lookup"><span data-stu-id="6d774-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="6d774-126">A felhasznált cikkeket a cikkszükséglet frissítésekor használják fel.</span><span class="sxs-lookup"><span data-stu-id="6d774-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="6d774-127">A szállítói számla vagy a csomagjegyzék frissítésekor a rendszer felszólítja, hogy frissítse a szállítólevelet a cikkszükségleten.</span><span class="sxs-lookup"><span data-stu-id="6d774-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="6d774-128">További tudnivalókért lásd: [Cikkek bevételezése a beszerzési rendelésen cikkszükségletből](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="6d774-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]