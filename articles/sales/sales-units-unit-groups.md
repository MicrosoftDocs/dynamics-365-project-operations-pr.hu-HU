---
title: Egységek és egységcsoportok
description: Ez a témakör a Dynamics 365 Project Operations egységeinek és egységcsoportjainak létrehozásáról nyújt információkat.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 345a4f38ad0bc5acddb90cfd8cb3e92154e46513
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078215"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="be5c0-103">Egységek és egységcsoportok</span><span class="sxs-lookup"><span data-stu-id="be5c0-103">Units and unit groups</span></span>

<span data-ttu-id="be5c0-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="be5c0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="be5c0-105">Az egység az a mennyiség vagy mértékegység, amiben a terméket vagy szolgáltatásokat értékesíti.</span><span class="sxs-lookup"><span data-stu-id="be5c0-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="be5c0-106">Például a kertészeti készletek eladása esetén előfordulhat, hogy vetőmagot csomag, doboz és raklap egységben értékesíti.</span><span class="sxs-lookup"><span data-stu-id="be5c0-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="be5c0-107">Az egységcsoport ezen különböző kiszerelések gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="be5c0-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="be5c0-108">A témakör lépéseinek végrehajtásához rendszergazdai, Sales Professional menedzseri vagy ezzel egyenértékű jogosultsággal kell rendelkezni.</span><span class="sxs-lookup"><span data-stu-id="be5c0-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="be5c0-109">Egységcsoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="be5c0-109">Create a unit group</span></span>

1. <span data-ttu-id="be5c0-110">Az Oldaltérképen válassza az **Egységek** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="be5c0-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="be5c0-111">Válassza az **Új** lehetőséget, és az **Egységcsoport létrehozása** párbeszédpanelen adja meg az egység nevét.</span><span class="sxs-lookup"><span data-stu-id="be5c0-111">Select **New** , and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="be5c0-112">Az **Eelsődleges egység** mezőbe írja be azt a legkisebb közös mértékegységet, amelyben a terméket forgalmazni fogják.</span><span class="sxs-lookup"><span data-stu-id="be5c0-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="be5c0-113">Megadhatja például a „darab” vagy az „uncia” értéket.</span><span class="sxs-lookup"><span data-stu-id="be5c0-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="be5c0-114">Kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="be5c0-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="be5c0-115">Egységek hozzáadása egységcsoportokhoz</span><span class="sxs-lookup"><span data-stu-id="be5c0-115">Add units to a unit group</span></span>

1. <span data-ttu-id="be5c0-116">Nyisson meg egy egységcsoportot, és a **Kapcsolódó** lapon válassza az **Egységek** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="be5c0-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="be5c0-117">Látni fogja, hogy az elsődleges egység már szerepel.</span><span class="sxs-lookup"><span data-stu-id="be5c0-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="be5c0-118">Válassza az **Új egység hozzáadása** lehetőséget, majd az **Árlistaelem gyors létrehozása** oldal **Név** mezőjében adja meg az egység nevét.</span><span class="sxs-lookup"><span data-stu-id="be5c0-118">Select **Add New Unit** , and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="be5c0-119">A **Mennyiség** mezőben adja meg azt a mennyiséget, amelyet az egység tartalmazni fog.</span><span class="sxs-lookup"><span data-stu-id="be5c0-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="be5c0-120">Ha egy doboz például két darabot tartalmaz, akkor a „2” értéket írja be.</span><span class="sxs-lookup"><span data-stu-id="be5c0-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="be5c0-121">Az **Alapegység** mezőben válasszon egy alapegységet, az egység legkisebb mértékegységének megadásához.</span><span class="sxs-lookup"><span data-stu-id="be5c0-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="be5c0-122">Megadhatja például a „Darab” lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="be5c0-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="be5c0-123">Válassza a **Mentés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="be5c0-123">Select **Save** :</span></span>
