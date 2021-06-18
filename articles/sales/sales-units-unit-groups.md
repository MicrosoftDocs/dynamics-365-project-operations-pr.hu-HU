---
title: Egységek és egységcsoportok
description: Ez a témakör az egységek és egységcsoportok Dynamics 365 Project Operations rendszerben történő létrehozásával kapcsolatban tartalmaz tájékoztatást.
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
ms.openlocfilehash: 646e20189efb4aab56972f01a52b1bff19f2e79f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996074"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="ceea6-103">Egységek és egységcsoportok</span><span class="sxs-lookup"><span data-stu-id="ceea6-103">Units and unit groups</span></span>

<span data-ttu-id="ceea6-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="ceea6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ceea6-105">Az egység az a mennyiség vagy mértékegység, amiben a terméket vagy szolgáltatásokat értékesíti.</span><span class="sxs-lookup"><span data-stu-id="ceea6-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="ceea6-106">Például a kertészeti készletek eladása esetén előfordulhat, hogy vetőmagot csomag, doboz és raklap egységben értékesíti.</span><span class="sxs-lookup"><span data-stu-id="ceea6-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="ceea6-107">Az egységcsoport ezen különböző kiszerelések gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="ceea6-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="ceea6-108">A témakör lépéseinek végrehajtásához rendszergazdai, Sales Professional menedzseri vagy ezzel egyenértékű jogosultsággal kell rendelkezni.</span><span class="sxs-lookup"><span data-stu-id="ceea6-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="ceea6-109">Egységcsoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="ceea6-109">Create a unit group</span></span>

1. <span data-ttu-id="ceea6-110">Az Oldaltérképen válassza az **Egységek** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="ceea6-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="ceea6-111">Válassza az **Új** lehetőséget, és az **Egységcsoport létrehozása** párbeszédpanelen adja meg az egység nevét.</span><span class="sxs-lookup"><span data-stu-id="ceea6-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="ceea6-112">Az **Eelsődleges egység** mezőbe írja be azt a legkisebb közös mértékegységet, amelyben a terméket forgalmazni fogják.</span><span class="sxs-lookup"><span data-stu-id="ceea6-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="ceea6-113">Megadhatja például a „darab” vagy az „uncia” értéket.</span><span class="sxs-lookup"><span data-stu-id="ceea6-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="ceea6-114">Kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="ceea6-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="ceea6-115">Egységek hozzáadása egységcsoportokhoz</span><span class="sxs-lookup"><span data-stu-id="ceea6-115">Add units to a unit group</span></span>

1. <span data-ttu-id="ceea6-116">Nyisson meg egy egységcsoportot, és a **Kapcsolódó** lapon válassza az **Egységek** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="ceea6-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="ceea6-117">Látni fogja, hogy az elsődleges egység már szerepel.</span><span class="sxs-lookup"><span data-stu-id="ceea6-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="ceea6-118">Válassza az **Új egység hozzáadása** lehetőséget, majd az **Árlistaelem gyors létrehozása** oldal **Név** mezőjében adja meg az egység nevét.</span><span class="sxs-lookup"><span data-stu-id="ceea6-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="ceea6-119">A **Mennyiség** mezőben adja meg azt a mennyiséget, amelyet az egység tartalmazni fog.</span><span class="sxs-lookup"><span data-stu-id="ceea6-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="ceea6-120">Ha egy doboz például két darabot tartalmaz, akkor a „2” értéket írja be.</span><span class="sxs-lookup"><span data-stu-id="ceea6-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="ceea6-121">Az **Alapegység** mezőben válasszon egy alapegységet, az egység legkisebb mértékegységének megadásához.</span><span class="sxs-lookup"><span data-stu-id="ceea6-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="ceea6-122">Megadhatja például a „Darab” lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="ceea6-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="ceea6-123">Válassza a **Mentés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="ceea6-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]