---
title: Emlékezzen a jóváhagyott idő- vagy költségbejegyzésre
description: Ez a témakör információkat tartalmaz egy korábban jóváhagyott idő- vagy költségügylet visszahívásáról.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 74df6e196c9f060f957d79aebc9640a162fb2913
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752308"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="2e791-103">Emlékezzen a jóváhagyott idő- vagy költségbejegyzésre</span><span class="sxs-lookup"><span data-stu-id="2e791-103">Recall approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2e791-104">A projektcsoport tagja vagy más személy, aki benyújt egy idő- vagy költségbejegyzést, visszavonhatja azt az idő- vagy költségszámítást, miután azt jóváhagyták.</span><span class="sxs-lookup"><span data-stu-id="2e791-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="2e791-105">A jóváhagyott idő- vagy költségbejegyzés visszahívásának két lépése van:</span><span class="sxs-lookup"><span data-stu-id="2e791-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="2e791-106">A benyújtó visszahívást kér.</span><span class="sxs-lookup"><span data-stu-id="2e791-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="2e791-107">A visszahívást jóváhagyó személy hagyja jóvá.</span><span class="sxs-lookup"><span data-stu-id="2e791-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="2e791-108">Kérjen visszahívást</span><span class="sxs-lookup"><span data-stu-id="2e791-108">Request a recall</span></span>

<span data-ttu-id="2e791-109">Kövesse ezeket a lépéseket egy jóváhagyott idő- vagy költségbejegyzés visszahívásának kérésére.</span><span class="sxs-lookup"><span data-stu-id="2e791-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="2e791-110">Időbeírásokhoz lépjen a **Projektek** \> **Saját munka** \> **Időbevitel** oldalba.</span><span class="sxs-lookup"><span data-stu-id="2e791-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="2e791-111">–vagy–</span><span class="sxs-lookup"><span data-stu-id="2e791-111">–or–</span></span>

    <span data-ttu-id="2e791-112">Költségbejegyzéshez lépjen a **Projektek** \> **Saját munka**\> **Kiadások** oldalra.</span><span class="sxs-lookup"><span data-stu-id="2e791-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="2e791-113">Időbeírásokhoz válassza ki az összes időbejegyzést a projekt és a feladat egy adott kombinációjára.</span><span class="sxs-lookup"><span data-stu-id="2e791-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="2e791-114">Alternatív megoldásként a rácsban válassza ki az egyes cellákat az adott időpontra egy adott dátumra egy adott projekthez.</span><span class="sxs-lookup"><span data-stu-id="2e791-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="2e791-115">–vagy–</span><span class="sxs-lookup"><span data-stu-id="2e791-115">–or–</span></span>

    <span data-ttu-id="2e791-116">Költségbejegyzés esetén válassza ki a visszahívandó költségbejegyzés sorát.</span><span class="sxs-lookup"><span data-stu-id="2e791-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="2e791-117">Válassza az **Előhívás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2e791-117">Select **Recall**.</span></span> <span data-ttu-id="2e791-118">Megjelenik a jóváhagyást kérő párbeszédpanel.</span><span class="sxs-lookup"><span data-stu-id="2e791-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="2e791-119">Ha a kiválasztott idő- és költségbejegyzéseket már jóváhagyták, a rendszer kéri, hogy írja be a visszahívás okát.</span><span class="sxs-lookup"><span data-stu-id="2e791-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="2e791-120">Írja be a visszahívás okát, majd a művelet megerősítéséhez válassza az **OK** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2e791-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="2e791-121">A rendszer kéri a bejegyzés jóváhagyóját a visszahívás jóváhagyására.</span><span class="sxs-lookup"><span data-stu-id="2e791-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="2e791-122">Noha a jóváhagyott idő- és költségbejegyzés visszahívható, ha egy jóváhagyott időt vagy költséget már számláztak az ügyfélnek, visszahívási kérelmet nem lehet létrehozni.</span><span class="sxs-lookup"><span data-stu-id="2e791-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="2e791-123">Az a felhasználó, aki megkísérel létrehozni visszahívási kérelmet, üzenetet kap, amelyben kijelenti, hogy az időt vagy a költségeket nem lehet visszahívni, mert már kiszámlázásra került.</span><span class="sxs-lookup"><span data-stu-id="2e791-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="2e791-124">A visszahívás jóváhagyása vagy elutasítása</span><span class="sxs-lookup"><span data-stu-id="2e791-124">Approve or reject a recall request</span></span>

<span data-ttu-id="2e791-125">A visszahívás jóváhagyásához vagy elutasításához kövesse ezeket a lépéseket.</span><span class="sxs-lookup"><span data-stu-id="2e791-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="2e791-126">Válassza a **Projektek** \> **Saját munka** \> **Jóváhagyások** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2e791-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="2e791-127">A **Jóváhagyások** lista oldalon módosítsa a nézetet **Jogosultsági kérelmek előhívása** nézetre.</span><span class="sxs-lookup"><span data-stu-id="2e791-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="2e791-128">Megjelenik a benyújtott visszahívási kérelmek listája.</span><span class="sxs-lookup"><span data-stu-id="2e791-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="2e791-129">Válasszon egy vagy több bejegyzést, majd válassza az **Jóváhagyás** vagy az **Elutasítás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2e791-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="2e791-130">Ha a **Jóváhagyást** választotta, figyelmeztető üzenetet kap, amely elmagyarázza a jóváhagyás hatását.</span><span class="sxs-lookup"><span data-stu-id="2e791-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="2e791-131">A művelet megerősítéséhez válassza az **OK** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2e791-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="2e791-132">A visszahívási kérelmet jóváhagyják.</span><span class="sxs-lookup"><span data-stu-id="2e791-132">The recall request is approved.</span></span>

    <span data-ttu-id="2e791-133">–vagy–</span><span class="sxs-lookup"><span data-stu-id="2e791-133">–or–</span></span>

    <span data-ttu-id="2e791-134">Ha az **Elutasítás** lehetőséget választotta, akkor a visszahívási kérelmet elutasítják.</span><span class="sxs-lookup"><span data-stu-id="2e791-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="2e791-135">Csakúgy, amikor visszahívást kérnek, akkor is, amikor a visszahívást jóváhagyják, a rendszer ellenőrzi az esetleges számlázási tevékenységeket az idő- vagy költségbejegyzésen.</span><span class="sxs-lookup"><span data-stu-id="2e791-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="2e791-136">Ha egy bejegyzésre már számláztak, vagy ha számlatervezetről van szó, akkor a jóváhagyó hibaüzenetet fog kapni, amely kijelenti, hogy az időt vagy a költségeket nem lehet jóváhagyni a visszahíváshoz, mert már számláztak.</span><span class="sxs-lookup"><span data-stu-id="2e791-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="2e791-137">A visszahívás kérésének hatása</span><span class="sxs-lookup"><span data-stu-id="2e791-137">Impact of a recall request</span></span>

<span data-ttu-id="2e791-138">A jóváhagyás visszavonásakor mind működési, mind pénzügyi hatásokkal jár.</span><span class="sxs-lookup"><span data-stu-id="2e791-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="2e791-139">Működési hatás</span><span class="sxs-lookup"><span data-stu-id="2e791-139">Operational impact</span></span>

<span data-ttu-id="2e791-140">Ha egy visszahívási kérelmet jóváhagynak, a jóváhagyási rekordot **Elutasítva** jelöléssel kell ellátni.</span><span class="sxs-lookup"><span data-stu-id="2e791-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="2e791-141">A bejegyzés állapota megváltozik **Visszatérített** vagy **Elutasított** értékre , attól függően, hogy időbejegyzés vagy költségbejegyzés van-e.</span><span class="sxs-lookup"><span data-stu-id="2e791-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="2e791-142">A projektcsoport tagja megtekintheti a bejegyzéseket, szerkesztheti és újra benyújthatja a bejegyzéseket, vagy teljes egészében törölheti a bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="2e791-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="2e791-143">Ha egy visszahívási kérelmet elutasítanak, akkor a bejegyzés állapota továbbra is **Jóváhagyva**, és a bejegyzés nem módosítható a projekt csapattagjának vagy a projekt jóváhagyójának.</span><span class="sxs-lookup"><span data-stu-id="2e791-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="2e791-144">Pénzügyi hatás</span><span class="sxs-lookup"><span data-stu-id="2e791-144">Financial impact</span></span>

<span data-ttu-id="2e791-145">Ha egy visszahívási kérelmet jóváhagynak, a költség és az értékesítés vonatkozó aktuális tényezőit a következő módon frissítik:</span><span class="sxs-lookup"><span data-stu-id="2e791-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="2e791-146">A **Beállítás állapota** mező frissül **Korrigált**-ra.</span><span class="sxs-lookup"><span data-stu-id="2e791-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="2e791-147">A **Számlázás állapota** mező frissül **Megszakítva**-ra.</span><span class="sxs-lookup"><span data-stu-id="2e791-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="2e791-148">A következő lépésként létrejönnek a sztornózott bejegyzések a Tényadatok táblában.</span><span class="sxs-lookup"><span data-stu-id="2e791-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="2e791-149">Sztornózott bejegyzések létrehozásához a rendszer átmásolja az eredeti tényadatok mezőinek értékeit.</span><span class="sxs-lookup"><span data-stu-id="2e791-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="2e791-150">Csak a minőségi értékek nem lesznek átmásolva.</span><span class="sxs-lookup"><span data-stu-id="2e791-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="2e791-151">Ezeket az értékeket sztornózza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="2e791-151">These values are reversed instead.</span></span> <span data-ttu-id="2e791-152">Mind a **Költség**, mind a **Számlázatlan értékesítés** tényadatai esetén létrejönnek sztornózott tényadatok.</span><span class="sxs-lookup"><span data-stu-id="2e791-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="2e791-153">A **Beállítás állapota** mező **Nem állítható** értékre áll, és a **Számlázási állapot** mező értéke **Megszakítva** lesz.</span><span class="sxs-lookup"><span data-stu-id="2e791-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="2e791-154">Ezeknek a változásoknak köszönhetően a projektre elszámolt kiadások és bevételmaradás már nem veszi figyelembe az aktuális tényezők által képviselt összegeket.</span><span class="sxs-lookup"><span data-stu-id="2e791-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="2e791-155">Ha a visszahívási kérelmet elutasítják, nincs pénzügyi hatása a projektre.</span><span class="sxs-lookup"><span data-stu-id="2e791-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="2e791-156">Változások az időbejegyzés rekordokban</span><span class="sxs-lookup"><span data-stu-id="2e791-156">Changes to time entry records</span></span>

<span data-ttu-id="2e791-157">Az alábbi ábra bemutatja a jóváhagyott időbejegyzéseknél a visszahíváskor bekövetkező változásokat.</span><span class="sxs-lookup"><span data-stu-id="2e791-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Időbeviteli állapotátmenetek](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="2e791-159">A költségbejegyzés nyilvántartásának változásai</span><span class="sxs-lookup"><span data-stu-id="2e791-159">Changes to expense entry records</span></span>

<span data-ttu-id="2e791-160">Az alábbi ábra bemutatja azokat a változásokat, amelyek a jóváhagyott kiadási tételeknél történnek visszahívásukkor.</span><span class="sxs-lookup"><span data-stu-id="2e791-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Költség belépési állapotátmenetek](media/ExpenseEntryStateTransitions.png)