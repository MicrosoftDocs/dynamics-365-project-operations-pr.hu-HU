---
title: A korábban jóváhagyott idő- és költségbejegyzések visszavonása
description: Ez a témakör a projekt jóváhagyott idő- és költségtranzakciójának visszavonásával kapcsolatban tartalmaz tájékoztatást.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2fc74aba2a837b7cdff55385ffa20d78c2678bb7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752140"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="11260-103">A korábban jóváhagyott idő- vagy költségbejegyzések visszavonása</span><span class="sxs-lookup"><span data-stu-id="11260-103">Cancel previously approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="11260-104">A Dynamics 365 Project Service Automation legújabb verziójában a jóváhagyók visszavonhatják a korábban jóváhagyott idő- és költségbejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="11260-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="11260-105">Korábban jóváhagyott idő- vagy költségbejegyzés visszavonása</span><span class="sxs-lookup"><span data-stu-id="11260-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="11260-106">Az alábbi lépések végrehajtásával vonhatja vissza a korábban jóváhagyott idő- vagy költségbejegyzést.</span><span class="sxs-lookup"><span data-stu-id="11260-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="11260-107">Válassza a **Projektek** \> **Saját munka** \> **Jóváhagyások** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="11260-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="11260-108">A **Jóváhagyások** listaoldalon módosítsa a nézetet a **Saját korábbi jóváhagyások** értékre.</span><span class="sxs-lookup"><span data-stu-id="11260-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="11260-109">Megjelenik a korábban jóváhagyott idő- és költségbejegyzések listája.</span><span class="sxs-lookup"><span data-stu-id="11260-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="11260-110">Jelöljön ki egy vagy több bejegyzést, majd jelölje be a **Jóváhagyás visszavonása** jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="11260-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="11260-111">Figyelmeztető üzenet jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="11260-111">You receive a warning message.</span></span>
4. <span data-ttu-id="11260-112">A jóváhagyás visszavonásához válassza az **OK** gombot.</span><span class="sxs-lookup"><span data-stu-id="11260-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="11260-113">Az idő- és a költségbejegyzés-jóváhagyás visszavonásának hatásáról</span><span class="sxs-lookup"><span data-stu-id="11260-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="11260-114">A jóváhagyás visszavonása esetén a működési hatás és a pénzügyi hatás egyaránt fennáll.</span><span class="sxs-lookup"><span data-stu-id="11260-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="11260-115">Működési hatás</span><span class="sxs-lookup"><span data-stu-id="11260-115">Operational impact</span></span>

<span data-ttu-id="11260-116">A műveletek oldalon a jóváhagyás visszavonásakor a rekord állapota **Tervezet**értékre van állítva, és a jóváhagyás már nem jelenik meg a **Saját korábbi jóváhagyások** nézetben.</span><span class="sxs-lookup"><span data-stu-id="11260-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="11260-117">Ehelyett a visszavont jóváhagyás vagy a **Jóváhagyandó időbejegyzések** nézetben, vagy a **Jóváhagyandó bejegyzések** nézetben jelenik meg attól függően, hogy idő- vagy költségbejegyzés volt-e.</span><span class="sxs-lookup"><span data-stu-id="11260-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="11260-118">Emellett a kapcsolódó idő- vagy költségbejegyzés állapota **Beküldött** lesz, így a kapcsolódó bejegyzés konzisztens lesz a **Tervezet** állapotban lévő jóváhagyásokkal.</span><span class="sxs-lookup"><span data-stu-id="11260-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="11260-119">Jóváhagyóként a jóváhagyás néhány mezőjét szerkesztheti, amelynek állapota **Tervezet**.</span><span class="sxs-lookup"><span data-stu-id="11260-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="11260-120">Ezekhez a mezőkhöz tartozik a **Számlázás típusa** és az **Időbejegyzések számlázható órái**.</span><span class="sxs-lookup"><span data-stu-id="11260-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="11260-121">A módosítások végrehajtása után ismét jóváhagyhatja a rekordot.</span><span class="sxs-lookup"><span data-stu-id="11260-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="11260-122">Másik lehetőségként elutasíthatja a bejegyzést.</span><span class="sxs-lookup"><span data-stu-id="11260-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="11260-123">Ha elutasítja egy időbejegyzés jóváhagyását, akkor a bejegyzés állapota **Visszaküldött** lesz.</span><span class="sxs-lookup"><span data-stu-id="11260-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="11260-124">Ha elutasítja egy költségbejegyzés jóváhagyását, akkor a bejegyzés állapota **Elutasított** lesz.</span><span class="sxs-lookup"><span data-stu-id="11260-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="11260-125">A visszaküldött és a visszautasított bejegyzések működése megegyezik a **Tervezet** állapotú bejegyzésekkel.</span><span class="sxs-lookup"><span data-stu-id="11260-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="11260-126">A projektcsapat bármelyik tagja elvégezheti a bejegyzéshez szükséges változtatásokat, majd újból beküldheti jóváhagyásra, vagy teljesen törölheti a bejegyzést.</span><span class="sxs-lookup"><span data-stu-id="11260-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="11260-127">Pénzügyi hatás</span><span class="sxs-lookup"><span data-stu-id="11260-127">Financial impact</span></span>

<span data-ttu-id="11260-128">A projektet a jóváhagyás visszavonása után is éri pénzügyi hatás.</span><span class="sxs-lookup"><span data-stu-id="11260-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="11260-129">Előrször is a következő módon frissíti a rendszer a megfelelő költség- és értékesítési tényadatokat:</span><span class="sxs-lookup"><span data-stu-id="11260-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="11260-130">A korrekció állapota **Korrigálva**érték lesz.</span><span class="sxs-lookup"><span data-stu-id="11260-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="11260-131">A számlázás állapota **Visszavonva**érték lesz.</span><span class="sxs-lookup"><span data-stu-id="11260-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="11260-132">A következő lépésként létrejönnek a sztornózott bejegyzések a Tényadatok táblában.</span><span class="sxs-lookup"><span data-stu-id="11260-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="11260-133">Sztornózott bejegyzések létrehozásához a rendszer átmásolja az eredeti tényadatok mezőinek értékeit.</span><span class="sxs-lookup"><span data-stu-id="11260-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="11260-134">Csak a minőségi értékek nem lesznek átmásolva.</span><span class="sxs-lookup"><span data-stu-id="11260-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="11260-135">Ezeket az értékeket sztornózza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="11260-135">These values are reversed instead.</span></span> <span data-ttu-id="11260-136">Mind a **Költség**, mind a **Számlázatlan értékesítés** tényadatai esetén létrejönnek sztornózott tényadatok.</span><span class="sxs-lookup"><span data-stu-id="11260-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="11260-137">A sztornózott tényadat **Korrekció állapota** mezőjének értéke **Nem korrigálható**, a számlázás állapota mező értéke **Visszavonva** lesz.</span><span class="sxs-lookup"><span data-stu-id="11260-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="11260-138">A módosítások elvégzése után a projektre költött összegként és a projekt bevételi tartalékaként rögzített összeg a továbbiakban nem lesz felszámítva az ezen tényadatok által jelentett összegek esetén.</span><span class="sxs-lookup"><span data-stu-id="11260-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
