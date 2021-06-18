---
title: Jóváhagyások áttekintése
description: Ez a témakör a jóváhagyások Project Operationsben való használatáról nyújt tájékoztatást.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 5e30b8a386805faee869f77e695d5ee492d78cdb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996704"
---
# <a name="approvals-overview"></a><span data-ttu-id="73849-103">Jóváhagyások áttekintése</span><span class="sxs-lookup"><span data-stu-id="73849-103">Approvals overview</span></span>

<span data-ttu-id="73849-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="73849-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="73849-105">Az idő-, költség- és anyaghasználati beküldések egy jóváhagyási munkafolyamaton haladnak át.</span><span class="sxs-lookup"><span data-stu-id="73849-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="73849-106">A bejegyzések jóváhagyását követően a rendszer a tényleges adatokban rögzíti a tranzakciókat, és az ütemezésben könyveli az időt.</span><span class="sxs-lookup"><span data-stu-id="73849-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="73849-107">Jóváhagyási munkamenet</span><span class="sxs-lookup"><span data-stu-id="73849-107">Approvals workflow</span></span>
<span data-ttu-id="73849-108">Idő-, költség- vagy anyagfelhasználási tétel létrehozásakor és elküldésekor jóváhagyási rekord jön létre.</span><span class="sxs-lookup"><span data-stu-id="73849-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="73849-109">A projekt jóváhagyója vagy vezetője áttekinti és jóváhagyja a bejegyzést.</span><span class="sxs-lookup"><span data-stu-id="73849-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="73849-110">Ha a bejegyzés egy projekthez kapcsolódik, a tényadatok a jóváhagyáskor jönnek létre.</span><span class="sxs-lookup"><span data-stu-id="73849-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="73849-111">Ez lehetővé teszi a költségek és a számlázás nyomon követését.</span><span class="sxs-lookup"><span data-stu-id="73849-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="73849-112">Bejegyzés jóváhagyása</span><span class="sxs-lookup"><span data-stu-id="73849-112">Approve an entry</span></span>
<span data-ttu-id="73849-113">A **Jóváhagyások** lapon válthat a különböző nézetek között, így megtekintheti a különböző típusú jóváhagyásokat.</span><span class="sxs-lookup"><span data-stu-id="73849-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="73849-114">Menjen a **Jóváhagyások** lapra, és válassza a **Költségek**, **Idő**, **Anyaghasználat** vagy a **Visszahívások** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="73849-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="73849-115">Tekintse át az egyes jóváhagyásokat, és jelölje ki a jóváhagyni kívántakat.</span><span class="sxs-lookup"><span data-stu-id="73849-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="73849-116">Válassza a **Jóváhagyás** lehetőséget a kijelölt bejegyzések jóváhagyásához.</span><span class="sxs-lookup"><span data-stu-id="73849-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="73849-117">A rendszer feldolgozza ezeket a bejegyzéseket, és tényadatokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="73849-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="73849-118">Bejegyzés elutasítása</span><span class="sxs-lookup"><span data-stu-id="73849-118">Reject an entry</span></span>
<span data-ttu-id="73849-119">A projekt jóváhagyójaként előfordulhat, hogy a felhasználónak vissza kell küldenie egy bejegyzést a felhasználóhoz helyesbítés céljából.</span><span class="sxs-lookup"><span data-stu-id="73849-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="73849-120">Menjen a **Jóváhagyások** lapra, és jelölje ki az elutasítani kívánt bejegyzést.</span><span class="sxs-lookup"><span data-stu-id="73849-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="73849-121">Válassza az **Elutasítás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="73849-121">Select **Reject**.</span></span>
3. <span data-ttu-id="73849-122">Nem kötelező, de hozzáadhat megjegyzést az **Elutasítási megjegyzések** párbeszédpanelen, hogy tájékoztassa a felhasználót a bejegyzés elutasításának okairól.</span><span class="sxs-lookup"><span data-stu-id="73849-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="73849-123">Kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="73849-123">Select **OK**.</span></span> <span data-ttu-id="73849-124">A rendszer visszaküldi a bejegyzést a felhasználónak.</span><span class="sxs-lookup"><span data-stu-id="73849-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="73849-125">Jóváhagyás visszavonása</span><span class="sxs-lookup"><span data-stu-id="73849-125">Cancel approval</span></span>
<span data-ttu-id="73849-126">Bizonyos esetekben előfordulhat, hogy törölnie kell egy korábban jóváhagyott bejegyzést.</span><span class="sxs-lookup"><span data-stu-id="73849-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="73849-127">Egy korábban jóváhagyott bejegyzés visszavonása pénzügyi hatással jár.</span><span class="sxs-lookup"><span data-stu-id="73849-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="73849-128">Visszahívási kérelmek jóváhagyása</span><span class="sxs-lookup"><span data-stu-id="73849-128">Approving recall requests</span></span>
<span data-ttu-id="73849-129">Bizonyos esetekben előfordulhat, hogy egy tanácsadónak vissza kell hívnia egy korábban jóváhagyott bejegyzést.</span><span class="sxs-lookup"><span data-stu-id="73849-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="73849-130">Egy korábban jóváhagyott bejegyzés visszavonása pénzügyi hatással jár.</span><span class="sxs-lookup"><span data-stu-id="73849-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="73849-131">A projekt jóváhagyójának jóvá kell hagynia a visszahívást a Tényadatokban sztornírozhassák a tranzakciót.</span><span class="sxs-lookup"><span data-stu-id="73849-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="73849-132">Projekt jóváhagyóinak megadása</span><span class="sxs-lookup"><span data-stu-id="73849-132">Specify Project approvers</span></span>
<span data-ttu-id="73849-133">Minden projekthez bizonyos számú projektcsapattag tartozik.</span><span class="sxs-lookup"><span data-stu-id="73849-133">Each project has a number of project team members.</span></span> <span data-ttu-id="73849-134">Megadhatja, hogy mely csoporttagok projektjóváhagyók is egyben.</span><span class="sxs-lookup"><span data-stu-id="73849-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="73849-135">Menjen a **Projektek** lapra, és nyissa meg a projektet a listából.</span><span class="sxs-lookup"><span data-stu-id="73849-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="73849-136">A **Csapat** lapon jelölje ki azt a csapattagot, aki a projekt jóváhagyója lesz, majd válassza a **Szerkesztés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="73849-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="73849-137">Állítsa a **Projektjóváhagyó** mezőjét **Igen** értékre.</span><span class="sxs-lookup"><span data-stu-id="73849-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="73849-138">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="73849-138">Select **Save**.</span></span>
5. <span data-ttu-id="73849-139">További projektjóváhagyók hozzáadásához ismételje meg a 2–4. lépést.</span><span class="sxs-lookup"><span data-stu-id="73849-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="73849-140">A felhasználó felettesének konfigurálása</span><span class="sxs-lookup"><span data-stu-id="73849-140">Configure the user's manager</span></span>

1. <span data-ttu-id="73849-141">Lépjen a **Beállítások** > **Biztonság** > **Felhasználók** részre.</span><span class="sxs-lookup"><span data-stu-id="73849-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="73849-142">Válassza ki azt a felhasználót, akihez vezetőt rendel, és a **Szervezet adatai** területen jelölje ki a vezetőt a listából.</span><span class="sxs-lookup"><span data-stu-id="73849-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="73849-143">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="73849-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
