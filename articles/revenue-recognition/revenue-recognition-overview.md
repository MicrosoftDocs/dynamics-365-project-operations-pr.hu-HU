---
title: Bevételelszámolás áttekintése
description: Ez a témakör információkat nyújt a bevételelszámolásról a Project Operations alkalmazásban.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013759"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="0952a-103">Bevételelszámolás áttekintése</span><span class="sxs-lookup"><span data-stu-id="0952a-103">Revenue recognition overview</span></span>

<span data-ttu-id="0952a-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="0952a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0952a-105">A Dynamics 365 Project Operations alkalmazásban a bevételelszámolási elvek a projekt vagy a projekt egy részének kiválasztott számlázási módszerén alapulnak.</span><span class="sxs-lookup"><span data-stu-id="0952a-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="0952a-106">Ez a témakör információkat nyújt a bevételelszámolásról a Project Operations alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="0952a-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="0952a-107">Az idő és anyag számlázási módszerrel könyvelt tranzakciók</span><span class="sxs-lookup"><span data-stu-id="0952a-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="0952a-108">A költség- és bevétel-elszámolás összefügg.</span><span class="sxs-lookup"><span data-stu-id="0952a-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="0952a-109">A tranzakciós költségeket és a nem számlázott értékesítéseket a [Project Operations integrációs naplójában](../project-accounting/project-operations-integration-journal.md) könyveli a program.</span><span class="sxs-lookup"><span data-stu-id="0952a-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="0952a-110">A projekt költség- és bevételi profilja határozza meg, hogy a nem számlázott értékesítési tranzakciók fel lesznek-e adva a főkönyvbe.</span><span class="sxs-lookup"><span data-stu-id="0952a-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="0952a-111">Ha az **Elhatárolt bevétel** lehetőséget választja, a rendszer a **Folyamatban lévő munka értékesítési értéke** és az **Elhatárolt bevétel eladási érték** számlákat használja a könyvelés során.</span><span class="sxs-lookup"><span data-stu-id="0952a-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="0952a-112">Alább egy példát lát erre a módszerre.</span><span class="sxs-lookup"><span data-stu-id="0952a-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="0952a-113">Tranzakció típusa</span><span class="sxs-lookup"><span data-stu-id="0952a-113">Transaction type</span></span> | <span data-ttu-id="0952a-114">Terhelés/Jóváírás</span><span class="sxs-lookup"><span data-stu-id="0952a-114">Debit/Credit</span></span> | <span data-ttu-id="0952a-115">Mennyiség</span><span class="sxs-lookup"><span data-stu-id="0952a-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="0952a-116">Folyamatban lévő termelés – értékesítési érték</span><span class="sxs-lookup"><span data-stu-id="0952a-116">WIP Sales value</span></span> | <span data-ttu-id="0952a-117">Terhelés</span><span class="sxs-lookup"><span data-stu-id="0952a-117">Debit</span></span> | <span data-ttu-id="0952a-118">100</span><span class="sxs-lookup"><span data-stu-id="0952a-118">100</span></span> |
  | <span data-ttu-id="0952a-119">Elhatárolt bevétel értékesítési értéke</span><span class="sxs-lookup"><span data-stu-id="0952a-119">Accrued revenue sales value</span></span> | <span data-ttu-id="0952a-120">Jóváírás</span><span class="sxs-lookup"><span data-stu-id="0952a-120">Credit</span></span> | <span data-ttu-id="0952a-121">100</span><span class="sxs-lookup"><span data-stu-id="0952a-121">100</span></span> |

- <span data-ttu-id="0952a-122">Bevétel a számlázásnál lesz elismerve.</span><span class="sxs-lookup"><span data-stu-id="0952a-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="0952a-123">A rendszer a feladás során a **Számlázott bevétel** számlát használja.</span><span class="sxs-lookup"><span data-stu-id="0952a-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="0952a-124">Alább egy példát lát erre a módszerre.</span><span class="sxs-lookup"><span data-stu-id="0952a-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="0952a-125">Tranzakció típusa</span><span class="sxs-lookup"><span data-stu-id="0952a-125">Transaction type</span></span> | <span data-ttu-id="0952a-126">Terhelés/Jóváírás</span><span class="sxs-lookup"><span data-stu-id="0952a-126">Debit/Credit</span></span> | <span data-ttu-id="0952a-127">Mennyiség</span><span class="sxs-lookup"><span data-stu-id="0952a-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="0952a-128">Vevő egyenlege</span><span class="sxs-lookup"><span data-stu-id="0952a-128">Customer balance</span></span> | <span data-ttu-id="0952a-129">Terhelés</span><span class="sxs-lookup"><span data-stu-id="0952a-129">Debit</span></span> | <span data-ttu-id="0952a-130">120</span><span class="sxs-lookup"><span data-stu-id="0952a-130">120</span></span> |
  | <span data-ttu-id="0952a-131">Fizetendő forgalmi adó</span><span class="sxs-lookup"><span data-stu-id="0952a-131">Sales tax payable</span></span> | <span data-ttu-id="0952a-132">Jóváírás</span><span class="sxs-lookup"><span data-stu-id="0952a-132">Credit</span></span> | <span data-ttu-id="0952a-133">20</span><span class="sxs-lookup"><span data-stu-id="0952a-133">20</span></span> |
  | <span data-ttu-id="0952a-134">Számlázott bevétel</span><span class="sxs-lookup"><span data-stu-id="0952a-134">Invoiced Revenue</span></span> | <span data-ttu-id="0952a-135">Jóváírás</span><span class="sxs-lookup"><span data-stu-id="0952a-135">Credit</span></span> | <span data-ttu-id="0952a-136">100</span><span class="sxs-lookup"><span data-stu-id="0952a-136">100</span></span> |

- <span data-ttu-id="0952a-137">Ha a bevétel elhatárolt volt a nem számlázott értékesítések feladásakor, a rendszer sztornírozza az elhatárolt bevételt a számlázáskor.</span><span class="sxs-lookup"><span data-stu-id="0952a-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="0952a-138">Tranzakció típusa</span><span class="sxs-lookup"><span data-stu-id="0952a-138">Transaction type</span></span> | <span data-ttu-id="0952a-139">Terhelés/Jóváírás</span><span class="sxs-lookup"><span data-stu-id="0952a-139">Debit/Credit</span></span> | <span data-ttu-id="0952a-140">Mennyiség</span><span class="sxs-lookup"><span data-stu-id="0952a-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="0952a-141">Folyamatban lévő termelés – értékesítési érték</span><span class="sxs-lookup"><span data-stu-id="0952a-141">WIP Sales value</span></span> | <span data-ttu-id="0952a-142">Jóváírás</span><span class="sxs-lookup"><span data-stu-id="0952a-142">Credit</span></span> | <span data-ttu-id="0952a-143">100</span><span class="sxs-lookup"><span data-stu-id="0952a-143">100</span></span> |
  | <span data-ttu-id="0952a-144">Elhatárolt bevétel értékesítési értéke</span><span class="sxs-lookup"><span data-stu-id="0952a-144">Accrued revenue sales value</span></span> | <span data-ttu-id="0952a-145">Terhelés</span><span class="sxs-lookup"><span data-stu-id="0952a-145">Debit</span></span> | <span data-ttu-id="0952a-146">100</span><span class="sxs-lookup"><span data-stu-id="0952a-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="0952a-147">A fixáras számlázási módszerrel könyvelt tranzakciók</span><span class="sxs-lookup"><span data-stu-id="0952a-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="0952a-148">A költség- és bevétel-elszámolás különállók.</span><span class="sxs-lookup"><span data-stu-id="0952a-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="0952a-149">A tranzakciós költségeket a [Project Operations integrációs naplójában](../project-accounting/project-operations-integration-journal.md) könyveli a program.</span><span class="sxs-lookup"><span data-stu-id="0952a-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="0952a-150">A nem számlázott értékesítési tranzakciók nem jönnek létre.</span><span class="sxs-lookup"><span data-stu-id="0952a-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="0952a-151">A bevétel akkor imemrtethető el a számlázás során, ha a projekt költség- és bevételi profiljánál a **Projektkészenlét számításához használt elv** **Nem folyamatban lévő munka**.</span><span class="sxs-lookup"><span data-stu-id="0952a-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="0952a-152">Ezt a módszert csak rövid távú, egyszerű projektekhez használja.</span><span class="sxs-lookup"><span data-stu-id="0952a-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="0952a-153">A bevétel fix árbevétel-becslésekkel ismertethető fel a **Befejezett szerződés** vagy a **Készültségi százalék bevétel-felismerés** módszerrel.</span><span class="sxs-lookup"><span data-stu-id="0952a-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0952a-154">További információforrások</span><span class="sxs-lookup"><span data-stu-id="0952a-154">Additional resources</span></span>
[<span data-ttu-id="0952a-155">Számlázható projektek könyvelésének konfigurálása cikk</span><span class="sxs-lookup"><span data-stu-id="0952a-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="0952a-156">Rögzített árú bevétel becslési projektjei</span><span class="sxs-lookup"><span data-stu-id="0952a-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="0952a-157">Bevételi becslések kezelése</span><span class="sxs-lookup"><span data-stu-id="0952a-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="0952a-158">Teljesítési költség módszerei</span><span class="sxs-lookup"><span data-stu-id="0952a-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]