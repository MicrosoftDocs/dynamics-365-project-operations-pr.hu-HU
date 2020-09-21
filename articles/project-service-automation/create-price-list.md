---
title: Árlista létrehozása
description: Árlista létrehozása a Project Service szolgáltatásban
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdd05aea-27a3-431d-9a80-2e220fb25e53
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 756af2fe3bc73d478b0355493aae6f0e49ac5835
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752315"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="e7c4a-103">Árlista létrehozása (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e7c4a-103">Create a price list (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e7c4a-104">Az árlisták egy sablont biztosítanak a partnerkezelők számára, amely segít nekik az árajánlatok és a projektek létrehozásában, illetve egy projekt költségeinek a m,egállapításában.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="e7c4a-105">Sorelemlistát biztosítanak szerepkörökhöz, költségekhez, illetve az egyes cikkekért majd felszámítandó árat.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="e7c4a-106">Több árlistát is létre tud hozni, így külön árszerkezetet tarthat karban a különböző régiókban amelyekben értékesít és az értékesítési csatornákat is szétválaszthatja.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="e7c4a-107">Érdemes legalább egy árlistát létrehozni minden pénznem esetében, amelyen számlázni szeretne az ügyfeleinek.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="e7c4a-108">Ha szeretne az elvégzendő munkához pénzügyi becsléseket létrehozni, győződjön meg arról, hogy minden projektnek biztonsági önköltségi és értékesítési árlistája.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="e7c4a-109">Állítson be egy alapértelmezett önköltségi és értékesítési árlistát, amely érvényes minden, a szervezetben létrehozott projektre.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="e7c4a-110">Az árlisták szerepkörökre és költségkategóriákra támaszkodnak, így árlisták létrehozása előtt ellenőrizze, hogy konfigurálta-e már a szerepköröket és kategóriákat, amelyeket használni kíván az árlista létrehozása előtt.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="e7c4a-111">Lépjen a **Project Service > Árlisták** pontba.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="e7c4a-112">Kattintson az **Új** elemre.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="e7c4a-113">A **Környezet** pontban válassza ki, hogy az árlistát mihez hozza létre: **Költség**, **Beszerzés** vagy **Értékesítés**.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="e7c4a-114">A **Név** mezőben adjon egy nevet az árlistának.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="e7c4a-115">A **Pénznem** mezőben válassza ki a pénznemet, amelyet a számlázáshoz vagy költségszámításhoz kíván használni.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="e7c4a-116">Az **Időegység** mezőben adja meg az időszakot, amelyre az ár vonatkozik, például nap vagy óra.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="e7c4a-117">Töltse ki a **Kezdő dátum**, **Befejező dátum** és **Leírás** mezőket szükség szerint.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="e7c4a-118">Kattintson a **Mentés** gombra a bejegyzés létrehozásához, hogy folytathassa a szerkesztést.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="e7c4a-119">Szerepkörár árlistához való hozzáadásához kattintson a **+** lehetőségre a **Szerepkörárak** alatt.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="e7c4a-120">A **Szerepkörár** panelen adja meg a részleteket, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="e7c4a-121">Folytassa a szerepkörárak hozzáadását, ameddig szükséges.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="e7c4a-122">Amikor végzett kattintson a **Mentés** gombra a képernyő jobb alsó sarkában.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="e7c4a-123">Költségkategória-ár árlistához való hozzáadásához kattintson a **+** lehetőségre a **Kategóriaárak** alatt.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="e7c4a-124">A **Tranzakciókategória-ár** panelen adja meg a részleteket, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="e7c4a-125">Folytassa a kategóriaárak hozzáadását, ameddig szükséges.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="e7c4a-126">Amikor végzett kattintson a **Mentés** gombra a képernyő jobb alsó sarkában.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="e7c4a-127">Árlistaelemek árlistához való hozzáadásához kattintson a **+** lehetőségre az **Árlistaelemek** alatt.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="e7c4a-128">Az **Árlistaelem** panelen adja meg a részleteket, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="e7c4a-129">Folytassa az árlistaelemek hozzáadását, ameddig szükséges.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="e7c4a-130">Amikor végzett kattintson a **Mentés** gombra a képernyő jobb alsó sarkában.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="e7c4a-131">Területi kapcsolatok árlistához való hozzáadásához kattintson a **+** lehetőségre a **Területi kapcsolatok** alatt.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="e7c4a-132">Az **Új kapcsolat** ablakban adja meg a részleteket, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="e7c4a-133">Folytassa a területi kapcsolatok hozzáadását, ameddig szükséges.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="e7c4a-134">Amikor végzett kattintson a **Mentés** gombra a képernyő jobb alsó sarkában.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e7c4a-135">Kapcsolódó információk</span><span class="sxs-lookup"><span data-stu-id="e7c4a-135">See Also</span></span>  
 [<span data-ttu-id="e7c4a-136">Project Service Automation konfigurálása</span><span class="sxs-lookup"><span data-stu-id="e7c4a-136">Configure Project Service Automation</span></span>](../project-service/configure.md)
