---
title: Tekintse át a projektek és a projektszerződések számlázási hátralékát
description: Ez a témakör információkat nyújt arról, hogy miként lehet áttekinteni az időt, a költségeket és a termékmaradványokat, és hogyan jelölheti meg őket készen a számlázásra.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: eb6d942d61bf8b5d20afb75c88716132a596bcbd
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078301"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="c56c5-103">Tekintse át a projektek és a projektszerződések számlázási hátralékát</span><span class="sxs-lookup"><span data-stu-id="c56c5-103">Review the invoicing backlog on projects and project contracts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c56c5-104">Ha egy tranzakció kész, hogy egy számlát létrehozott és feldolgozott, a tranzakciót **Számlázásra kész** -ként kell jelölni.</span><span class="sxs-lookup"><span data-stu-id="c56c5-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="c56c5-105">Ez a témakör leírja a létrehozható tranzakciók típusait.</span><span class="sxs-lookup"><span data-stu-id="c56c5-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="c56c5-106">Tekintse át az idő- és anyagszámlázási elmaradást</span><span class="sxs-lookup"><span data-stu-id="c56c5-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="c56c5-107">Amikor egy idő- vagy költségbejegyzés benyújtásra és a projekt jóváhagyására kerül sor, a PSA ténylegesen létrehozza a projektet.</span><span class="sxs-lookup"><span data-stu-id="c56c5-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="c56c5-108">Ha a projekt és a tranzakciós osztály kombinációját egy idő- és anyagprojekt szerződési sorához rendelik, akkor a bejegyzés jóváhagyásakor két aktuális jön létre:</span><span class="sxs-lookup"><span data-stu-id="c56c5-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="c56c5-109">Tényleges költség</span><span class="sxs-lookup"><span data-stu-id="c56c5-109">Cost actual</span></span> 
- <span data-ttu-id="c56c5-110">Számlázatlan értékesítés tényleges</span><span class="sxs-lookup"><span data-stu-id="c56c5-110">Unbilled sales actual</span></span>

<span data-ttu-id="c56c5-111">A nem értékesített tényleges tényezők a számlázási lemaradást képviselik, és számlázási állapotukat **Számlázásra kész** -re kell állítani.</span><span class="sxs-lookup"><span data-stu-id="c56c5-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="c56c5-112">A projektszámla létrehozásakor a **Számlázásra kész** jelöléssel ellátott számlázatlan értékesített aktuális tényleges adatok számla sor részleteként kerülnek átmásolásra.</span><span class="sxs-lookup"><span data-stu-id="c56c5-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="c56c5-113">Az idő és az anyagok és a számlázási hátralék áttekintéséhez keresse meg az **Értékesítés** \> **Számlázás** \> **Idő és anyag számlázás hátralék** oldalát.</span><span class="sxs-lookup"><span data-stu-id="c56c5-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="c56c5-114">Válassza ki az összes nem beépített értékesítési aktuális terméket, amely készen áll a számlázásra, majd válassza a **Számlázásra kész** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c56c5-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="c56c5-115">Ezeknek a tényleges értékeknek a számlázási állapota megváltozik: **Számlázásra kész**.</span><span class="sxs-lookup"><span data-stu-id="c56c5-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Idő és anyag számlázási elmaradás](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="c56c5-117">Tekintse át a termék számlázási hátralékát</span><span class="sxs-lookup"><span data-stu-id="c56c5-117">Review the product billing backlog</span></span>

<span data-ttu-id="c56c5-118">A PSA-ban, ha egy projektszerződés termék-alapú szerződéses sorokkal rendelkezik, akkor ezeket a sorokat számlázáskor veszik figyelembe, amikor a projekt-szerződéshez számlát készítenek.</span><span class="sxs-lookup"><span data-stu-id="c56c5-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="c56c5-119">Azokat a termékeket, amelyek szerződéses soraival **Számlázásra kész** jelöléssel, a projekt számlájára másolják át a projekt számlára.</span><span class="sxs-lookup"><span data-stu-id="c56c5-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="c56c5-120">A termékek és a számlázási hátralék áttekintéséhez keresse meg az **Értékesítés** \> **Számlázás** \> **Termék számlázás hátralék** oldalát.</span><span class="sxs-lookup"><span data-stu-id="c56c5-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="c56c5-121">Válassza ki az összes termék-alapú szerződés sort, amely készen áll a számlázásra, majd válassza a **Számlázásra kész** értéket.</span><span class="sxs-lookup"><span data-stu-id="c56c5-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="c56c5-122">Ezeknek a soroknak a számlázási állapota megváltozik: **Számlázásra kész**.</span><span class="sxs-lookup"><span data-stu-id="c56c5-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Termék számlázási elmaradása](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="c56c5-124">Tekintse át a rögzített árú szerződések számlázási mérföldköveit</span><span class="sxs-lookup"><span data-stu-id="c56c5-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="c56c5-125">Minden rögzített árú számlázási módszerrel rendelkező projektszerződés-sornak meg kell határoznia a szerződés mérföldköveit.</span><span class="sxs-lookup"><span data-stu-id="c56c5-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="c56c5-126">Ezeket a szerződéses mérföldköveket csak akkor lehet számlázni, ha **készen állnak a számlázásra**.</span><span class="sxs-lookup"><span data-stu-id="c56c5-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="c56c5-127">A számlázási mérföldkövek áttekintéséhez nyissa meg az **Értékesítés** \> **Számlázás** \> **Rögzített árú mérföldkövek** oldalt.</span><span class="sxs-lookup"><span data-stu-id="c56c5-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="c56c5-128">Válassza ki azokat a mérföldköveket, amelyek készen állnak a számlázásra, majd válassza a **Számlázásra kész** elemet.</span><span class="sxs-lookup"><span data-stu-id="c56c5-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="c56c5-129">Ezeknek a mérföldköveknek a számlázási állapota megváltozik: **Számlázásra kész**.</span><span class="sxs-lookup"><span data-stu-id="c56c5-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Rögzített árú mérföldkövek](media/FPBacklog.png)
