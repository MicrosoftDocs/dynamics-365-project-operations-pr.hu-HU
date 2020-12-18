---
title: Bevételelszámolás áttekintése
description: Ez a témakör információkat nyújt a bevételelszámolásról a Project Operations alkalmazásban.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531452"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="5ebc2-103">Bevételelszámolás áttekintése</span><span class="sxs-lookup"><span data-stu-id="5ebc2-103">Revenue recognition overview</span></span>

<span data-ttu-id="5ebc2-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="5ebc2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5ebc2-105">A Dynamics 365 Project Operations alkalmazásban a bevételelszámolási elvek a projekt vagy a projekt egy részének kiválasztott számlázási módszerén alapulnak.</span><span class="sxs-lookup"><span data-stu-id="5ebc2-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="5ebc2-106">Ez a témakör információkat nyújt a bevételelszámolásról a Project Operations alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="5ebc2-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="5ebc2-107">Az idő és anyag számlázási módszerrel könyvelt tranzakciók</span><span class="sxs-lookup"><span data-stu-id="5ebc2-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="5ebc2-108">A költség- és bevétel-elszámolás összefügg.</span><span class="sxs-lookup"><span data-stu-id="5ebc2-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="5ebc2-109">A tranzakciós költségeket és a nem számlázott értékesítéseket a [Project Operations integrációs naplójában](../project-accounting/project-operations-integration-journal.md) könyveli a program.</span><span class="sxs-lookup"><span data-stu-id="5ebc2-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="5ebc2-110">A projekt költség- és bevételi profilja határozza meg, hogy a nem számlázott értékesítési tranzakciók fel lesznek-e adva a főkönyvbe.</span><span class="sxs-lookup"><span data-stu-id="5ebc2-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="5ebc2-111">Ha az **Elhatárolt bevétel** lehetőséget választja, a rendszer a **Folyamatban lévő munka értékesítési értéke** és az **Elhatárolt bevétel eladási érték** számlákat használja a könyvelés során.</span><span class="sxs-lookup"><span data-stu-id="5ebc2-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="5ebc2-112">Alább egy példát lát erre a módszerre.</span><span class="sxs-lookup"><span data-stu-id="5ebc2-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="5ebc2-113">Tranzakció típusa</span><span class="sxs-lookup"><span data-stu-id="5ebc2-113">Transaction type</span></span> | <span data-ttu-id="5ebc2-114">Terhelés/Jóváírás</span><span class="sxs-lookup"><span data-stu-id="5ebc2-114">Debit/Credit</span></span> | <span data-ttu-id="5ebc2-115">Mennyiség</span><span class="sxs-lookup"><span data-stu-id="5ebc2-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="5ebc2-116">Folyamatban lévő termelés – értékesítési érték</span><span class="sxs-lookup"><span data-stu-id="5ebc2-116">WIP Sales value</span></span> | <span data-ttu-id="5ebc2-117">Terhelés</span><span class="sxs-lookup"><span data-stu-id="5ebc2-117">Debit</span></span> | <span data-ttu-id="5ebc2-118">100</span><span class="sxs-lookup"><span data-stu-id="5ebc2-118">100</span></span> |
  | <span data-ttu-id="5ebc2-119">Elhatárolt bevétel értékesítési értéke</span><span class="sxs-lookup"><span data-stu-id="5ebc2-119">Accrued revenue sales value</span></span> | <span data-ttu-id="5ebc2-120">Jóváírás</span><span class="sxs-lookup"><span data-stu-id="5ebc2-120">Credit</span></span> | <span data-ttu-id="5ebc2-121">100</span><span class="sxs-lookup"><span data-stu-id="5ebc2-121">100</span></span> |

- <span data-ttu-id="5ebc2-122">Bevétel a számlázásnál lesz elismerve.</span><span class="sxs-lookup"><span data-stu-id="5ebc2-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="5ebc2-123">A rendszer a feladás során a **Számlázott bevétel** számlát használja.</span><span class="sxs-lookup"><span data-stu-id="5ebc2-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="5ebc2-124">Alább egy példát lát erre a módszerre.</span><span class="sxs-lookup"><span data-stu-id="5ebc2-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="5ebc2-125">Tranzakció típusa</span><span class="sxs-lookup"><span data-stu-id="5ebc2-125">Transaction type</span></span> | <span data-ttu-id="5ebc2-126">Terhelés/Jóváírás</span><span class="sxs-lookup"><span data-stu-id="5ebc2-126">Debit/Credit</span></span> | <span data-ttu-id="5ebc2-127">Mennyiség</span><span class="sxs-lookup"><span data-stu-id="5ebc2-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="5ebc2-128">Vevő egyenlege</span><span class="sxs-lookup"><span data-stu-id="5ebc2-128">Customer balance</span></span> | <span data-ttu-id="5ebc2-129">Terhelés</span><span class="sxs-lookup"><span data-stu-id="5ebc2-129">Debit</span></span> | <span data-ttu-id="5ebc2-130">120</span><span class="sxs-lookup"><span data-stu-id="5ebc2-130">120</span></span> |
  | <span data-ttu-id="5ebc2-131">Fizetendő forgalmi adó</span><span class="sxs-lookup"><span data-stu-id="5ebc2-131">Sales tax payable</span></span> | <span data-ttu-id="5ebc2-132">Jóváírás</span><span class="sxs-lookup"><span data-stu-id="5ebc2-132">Credit</span></span> | <span data-ttu-id="5ebc2-133">20</span><span class="sxs-lookup"><span data-stu-id="5ebc2-133">20</span></span> |
  | <span data-ttu-id="5ebc2-134">Számlázott bevétel</span><span class="sxs-lookup"><span data-stu-id="5ebc2-134">Invoiced Revenue</span></span> | <span data-ttu-id="5ebc2-135">Jóváírás</span><span class="sxs-lookup"><span data-stu-id="5ebc2-135">Credit</span></span> | <span data-ttu-id="5ebc2-136">100</span><span class="sxs-lookup"><span data-stu-id="5ebc2-136">100</span></span> |

- <span data-ttu-id="5ebc2-137">Ha a bevétel elhatárolt volt a nem számlázott értékesítések feladásakor, a rendszer sztornírozza az elhatárolt bevételt a számlázáskor.</span><span class="sxs-lookup"><span data-stu-id="5ebc2-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="5ebc2-138">Tranzakció típusa</span><span class="sxs-lookup"><span data-stu-id="5ebc2-138">Transaction type</span></span> | <span data-ttu-id="5ebc2-139">Terhelés/Jóváírás</span><span class="sxs-lookup"><span data-stu-id="5ebc2-139">Debit/Credit</span></span> | <span data-ttu-id="5ebc2-140">Mennyiség</span><span class="sxs-lookup"><span data-stu-id="5ebc2-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="5ebc2-141">Folyamatban lévő termelés – értékesítési érték</span><span class="sxs-lookup"><span data-stu-id="5ebc2-141">WIP Sales value</span></span> | <span data-ttu-id="5ebc2-142">Jóváírás</span><span class="sxs-lookup"><span data-stu-id="5ebc2-142">Credit</span></span> | <span data-ttu-id="5ebc2-143">100</span><span class="sxs-lookup"><span data-stu-id="5ebc2-143">100</span></span> |
  | <span data-ttu-id="5ebc2-144">Elhatárolt bevétel értékesítési értéke</span><span class="sxs-lookup"><span data-stu-id="5ebc2-144">Accrued revenue sales value</span></span> | <span data-ttu-id="5ebc2-145">Terhelés</span><span class="sxs-lookup"><span data-stu-id="5ebc2-145">Debit</span></span> | <span data-ttu-id="5ebc2-146">100</span><span class="sxs-lookup"><span data-stu-id="5ebc2-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="5ebc2-147">A fixáras számlázási módszerrel könyvelt tranzakciók</span><span class="sxs-lookup"><span data-stu-id="5ebc2-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="5ebc2-148">A költség- és bevétel-elszámolás különállók.</span><span class="sxs-lookup"><span data-stu-id="5ebc2-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="5ebc2-149">A tranzakciós költségeket a [Project Operations integrációs naplójában](../project-accounting/project-operations-integration-journal.md) könyveli a program.</span><span class="sxs-lookup"><span data-stu-id="5ebc2-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="5ebc2-150">A nem számlázott értékesítési tranzakciók nem jönnek létre.</span><span class="sxs-lookup"><span data-stu-id="5ebc2-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="5ebc2-151">A bevétel akkor imemrtethető el a számlázás során, ha a projekt költség- és bevételi profiljánál a **Projektkészenlét számításához használt elv** **Nem folyamatban lévő munka**.</span><span class="sxs-lookup"><span data-stu-id="5ebc2-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="5ebc2-152">Ezt a módszert csak rövid távú, egyszerű projektekhez használja.</span><span class="sxs-lookup"><span data-stu-id="5ebc2-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="5ebc2-153">A bevétel fix árbevétel-becslésekkel ismertethető fel a **Befejezett szerződés** vagy a **Készültségi százalék bevétel-felismerés** módszerrel.</span><span class="sxs-lookup"><span data-stu-id="5ebc2-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5ebc2-154">További információforrások</span><span class="sxs-lookup"><span data-stu-id="5ebc2-154">Additional resources</span></span>
[<span data-ttu-id="5ebc2-155">Számlázható projektek könyvelésének konfigurálása cikk</span><span class="sxs-lookup"><span data-stu-id="5ebc2-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="5ebc2-156">Rögzített árú bevétel becslési projektjei</span><span class="sxs-lookup"><span data-stu-id="5ebc2-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="5ebc2-157">Bevételi becslések kezelése</span><span class="sxs-lookup"><span data-stu-id="5ebc2-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="5ebc2-158">Teljesítési költség módszerei</span><span class="sxs-lookup"><span data-stu-id="5ebc2-158">Cost to complete methods</span></span>](cost-complete-methods.md)
