---
title: Projektárajánlatok létrehozása lehetőségekből
description: Ez a témakör a projektárajánlatok lehetőségekből történő létrehozását ismerteti.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898535"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="aa1f5-103">Projektárajánlatok létrehozása lehetőségekből</span><span class="sxs-lookup"><span data-stu-id="aa1f5-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="aa1f5-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="aa1f5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="aa1f5-105">Az árajánlatokat a következő módszerekkel lehet létrehozni a projektlehetőségekből:</span><span class="sxs-lookup"><span data-stu-id="aa1f5-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="aa1f5-106">Az **Árajánlatok** lapról a **Projektlehetőség** oldalon</span><span class="sxs-lookup"><span data-stu-id="aa1f5-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="aa1f5-107">A lehetőség értékesítési folyamatából</span><span class="sxs-lookup"><span data-stu-id="aa1f5-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="aa1f5-108">A lehetőség hivatkozásának egy meglévő árajánlaton történő frissítésével</span><span class="sxs-lookup"><span data-stu-id="aa1f5-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="aa1f5-109">Az Árajánlatok lapról a Projektlehetőség oldalon</span><span class="sxs-lookup"><span data-stu-id="aa1f5-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="aa1f5-110">Ha projektárajánlatot szeretne létrehozni egy lehetőségből, hajtsa végre az alábbi lépéseket.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="aa1f5-111">Nyissa meg a **Projektlehetőség** oldalt, és válassza az **Árajánlatok** lapot.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="aa1f5-112">Az **Árajánlatok** alrácson válassza a **+** lehetőséget, ha a lehetőség alapján új árajánlatot szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="aa1f5-113">A rendszer az összes lehetőségsort és a kapcsolódó projektárlistákat átmásolja az új árajánlatba a lehetőségből.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="aa1f5-114">A lehetőség értékesítési folyamatából</span><span class="sxs-lookup"><span data-stu-id="aa1f5-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="aa1f5-115">Ha egy árajánlatot szeretne létrehozni a lehetőség értékesítési folyamatából, hajtsa végre az alábbi lépéseket.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="aa1f5-116">A lehetőség értékesítési folyamatából nyissa meg a lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="aa1f5-117">Válassza a **Minősítés** fázist.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="aa1f5-118">Válassza **Tovább** lehetőséget, majd a **+ Létrehozás** lehetőséget úr árajánlat létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="aa1f5-119">Az új ajánlat **Összegzés** lapján található információk nagy része alapértelmezés szerint a lehetőségből fog megjelenni.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="aa1f5-120">Írja be a hiányzó szükséges adatokat, vagy szükség szerint frissítse az alapértelmezett értékeket az **Összesítés** lapon,</span><span class="sxs-lookup"><span data-stu-id="aa1f5-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="aa1f5-121">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-121">Select **Save**.</span></span> <span data-ttu-id="aa1f5-122">Létrejön az új árajánlat, és a lehetőséghez lesz társítva.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="aa1f5-123">Ezután megtekintheti az árajánlat adatait az **Árajánlatok** lapon a **Lehetőség** oldalon.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="aa1f5-124">A lehetőség értékesítési folyamata a következő fázisba lép át: **Ajánlat**.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="aa1f5-125">A lehetőség hivatkozásának egy meglévő árajánlaton történő frissítésével</span><span class="sxs-lookup"><span data-stu-id="aa1f5-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="aa1f5-126">A meglévő árajánlatok a lehetőséghez csatolhatók.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="aa1f5-127">Hajtsa végre az alábbi lépéseket a meglévő árajánlaton szereplő lehetőségadatok frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="aa1f5-128">Nyissa meg az **Árajánlat** oldalt, és válassza az **Összegzés** lapot.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="aa1f5-129">A **Lehetőség** mezőben jelölje ki azt a lehetőséget, amelyet az árajánlathoz szeretne csatolni.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="aa1f5-130">Az árajánlatot a lehetőség **Árajánlatok** rácsában tekintheti meg.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="aa1f5-131">A lehetőség értékesítési folyamata segítségével a lehetőség áthelyezhető a következő fázisba: **Ajánlat**.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="aa1f5-132">Ha a lehetőséget ebbe a fázisba helyezi, akkor ezt az árajánlatot a lehetőséghez társított árajánlatok listájából választhatja ki.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="aa1f5-133">Az árajánlat kiválasztása azt jelzi, hogy továbbhalad vele.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="aa1f5-134">A lehetőséghez kapcsolódó összes egyéb árajánlat továbbra is elérhető lesz, és mindaddig aktív marad, amíg az egyiket el nem nyerik.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="aa1f5-135">Az értékesítési folyamatot visszahelyezheti az előző (**Minősítés**) fázisba, és másik ajánlatot választhat ki, amellyel továbbléphet.</span><span class="sxs-lookup"><span data-stu-id="aa1f5-135">You can move the sales process back to the previous stage **Qualify**, and pick another quote to move forward with.</span></span>
