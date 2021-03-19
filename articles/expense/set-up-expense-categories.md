---
title: Költségkategóriák beállítása
description: Ez a témakör a költségkategóriák és a megosztott kategóriák költségjelentésekhez való beállításával kapcsolatban tartalmaz tájékoztatást.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1589cf82626e744d35f31fef8e8437a5ad71360d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276126"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="4bbd6-103">Költségkategóriák beállítása</span><span class="sxs-lookup"><span data-stu-id="4bbd6-103">Set up expense categories</span></span>

<span data-ttu-id="4bbd6-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="4bbd6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4bbd6-105">Amikor az alkalmazottak költségjelentéseket készítenek, az általuk rögzített kiadásoknak egy költségkategóriához kell társítva lennie.</span><span class="sxs-lookup"><span data-stu-id="4bbd6-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="4bbd6-106">A költségkategóriák olyan megosztott kategóriákból származnak, amelyek megoszthatók a szervezet jogi entitásai között.</span><span class="sxs-lookup"><span data-stu-id="4bbd6-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="4bbd6-107">A szervezet definiálásának függvényében ezek a költségkategóriák más területeken is megoszthatók.</span><span class="sxs-lookup"><span data-stu-id="4bbd6-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="4bbd6-108">A szervezet definíciója és a megvalósítási csoport útmutatása alapján meg kell határozni, hogy a költségkezelésben használt kategóriákat csak a költségkezelésben -használja a program, vagy más területeken is meg kell osztania.</span><span class="sxs-lookup"><span data-stu-id="4bbd6-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="4bbd6-109">Ezek a kategóriák megoszthatók a Projektmenedzsment és könyvelés és a Költségkezelés vagy a Projektmenedzsment és könyvelés és Termelés között.</span><span class="sxs-lookup"><span data-stu-id="4bbd6-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="4bbd6-110">Nem oszthatók meg azonban a Költségkezelés és a Termelés között.</span><span class="sxs-lookup"><span data-stu-id="4bbd6-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="4bbd6-111">A beállítási folyamat megkezdése előtt a következő döntéseket kell meghozni minden egyes költségkategóriára vonatkozóan:</span><span class="sxs-lookup"><span data-stu-id="4bbd6-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="4bbd6-112">Mi a költségkategória?</span><span class="sxs-lookup"><span data-stu-id="4bbd6-112">What is the expense category?</span></span> <span data-ttu-id="4bbd6-113">Ilyenek például a repülőjáratok, a szállodák vagy az útiköltségtérítés kategóriái.</span><span class="sxs-lookup"><span data-stu-id="4bbd6-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="4bbd6-114">A költségkategória használható a Projektmenedzsment és könyvelés modulban is?</span><span class="sxs-lookup"><span data-stu-id="4bbd6-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="4bbd6-115">Ha igen, akkor a következő döntéseket kell meghoznia:</span><span class="sxs-lookup"><span data-stu-id="4bbd6-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="4bbd6-116">Milyen költségszámlákat fog használni a következő kiadásokhoz?</span><span class="sxs-lookup"><span data-stu-id="4bbd6-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="4bbd6-117">Költség</span><span class="sxs-lookup"><span data-stu-id="4bbd6-117">Cost</span></span>
        - <span data-ttu-id="4bbd6-118">Bérlista-hozzárendelés</span><span class="sxs-lookup"><span data-stu-id="4bbd6-118">Payroll allocation</span></span>
        - <span data-ttu-id="4bbd6-119">Folyamatban lévő termelés költségértéke</span><span class="sxs-lookup"><span data-stu-id="4bbd6-119">WIP-cost value</span></span>
        - <span data-ttu-id="4bbd6-120">Költségelem</span><span class="sxs-lookup"><span data-stu-id="4bbd6-120">Cost-item</span></span>
        - <span data-ttu-id="4bbd6-121">Folyamatban lévő termelés költségérték-eleme</span><span class="sxs-lookup"><span data-stu-id="4bbd6-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="4bbd6-122">Elhatárolt veszteség</span><span class="sxs-lookup"><span data-stu-id="4bbd6-122">Accrued loss</span></span>
        - <span data-ttu-id="4bbd6-123">Folyamatban lévő termelés elhatárolt vesztesége</span><span class="sxs-lookup"><span data-stu-id="4bbd6-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="4bbd6-124">Milyen bevételi számlákat fog használni a következő bevételi források esetén?</span><span class="sxs-lookup"><span data-stu-id="4bbd6-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="4bbd6-125">Számlázott bevétel</span><span class="sxs-lookup"><span data-stu-id="4bbd6-125">Invoiced revenue</span></span>
        - <span data-ttu-id="4bbd6-126">Elhatárolt bevétel – Értékesítési érték</span><span class="sxs-lookup"><span data-stu-id="4bbd6-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="4bbd6-127">Folyamatban lévő termelés – értékesítési érték</span><span class="sxs-lookup"><span data-stu-id="4bbd6-127">WIP-sales value</span></span>
        - <span data-ttu-id="4bbd6-128">Elhatárolt bevétel – termelés</span><span class="sxs-lookup"><span data-stu-id="4bbd6-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="4bbd6-129">Folyamatban lévő termelés</span><span class="sxs-lookup"><span data-stu-id="4bbd6-129">WIP-production</span></span>
        - <span data-ttu-id="4bbd6-130">Elhatárolt bevétel – profit</span><span class="sxs-lookup"><span data-stu-id="4bbd6-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="4bbd6-131">Folyamatban lévő termelés – profit</span><span class="sxs-lookup"><span data-stu-id="4bbd6-131">WIP-profit</span></span>
        - <span data-ttu-id="4bbd6-132">Elhatárolt bevétel – előfizetés</span><span class="sxs-lookup"><span data-stu-id="4bbd6-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="4bbd6-133">Folyamatban lévő termelés – előfizetés</span><span class="sxs-lookup"><span data-stu-id="4bbd6-133">WIP-subscription</span></span>

- <span data-ttu-id="4bbd6-134">Mi a költségtípus?</span><span class="sxs-lookup"><span data-stu-id="4bbd6-134">What is the expense type?</span></span>
- <span data-ttu-id="4bbd6-135">Mi a költségkategória alapértelmezett fizetési módja?</span><span class="sxs-lookup"><span data-stu-id="4bbd6-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="4bbd6-136">A költség kategóriába tartozó költségeket tételezni kell?</span><span class="sxs-lookup"><span data-stu-id="4bbd6-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="4bbd6-137">Mi a költségkategória fő alapértelmezett számlája?</span><span class="sxs-lookup"><span data-stu-id="4bbd6-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="4bbd6-138">Mi a költségkategória alapértelmezett cikkáfacsoportja?</span><span class="sxs-lookup"><span data-stu-id="4bbd6-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="4bbd6-139">Engedélyezve vannak a költségkategóriához további fizetési módok?</span><span class="sxs-lookup"><span data-stu-id="4bbd6-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="4bbd6-140">Ha igen, melyek ezek?</span><span class="sxs-lookup"><span data-stu-id="4bbd6-140">If so, what are they?</span></span>
- <span data-ttu-id="4bbd6-141">Vannak alkategóriák ebben a költségkategóriában?</span><span class="sxs-lookup"><span data-stu-id="4bbd6-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="4bbd6-142">Ha vannak alkategóriák, akkor a következő döntéseket kell meghoznia:</span><span class="sxs-lookup"><span data-stu-id="4bbd6-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="4bbd6-143">Van olyan alkategória, amely ki van zárva az adó visszaigényléséből?</span><span class="sxs-lookup"><span data-stu-id="4bbd6-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="4bbd6-144">Mi ezen alkategóriák cikkáfacsoportja?</span><span class="sxs-lookup"><span data-stu-id="4bbd6-144">What is the item sales tax group of the subcategories?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]