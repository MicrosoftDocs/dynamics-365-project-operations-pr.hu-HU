---
title: Jóváhagyások áttekintése
description: Ez a témakör a jóváhagyások Project Operationsben való használatáról nyújt tájékoztatást.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4077952"
---
# <a name="approvals-overview"></a><span data-ttu-id="86a4b-103">Jóváhagyások áttekintése</span><span class="sxs-lookup"><span data-stu-id="86a4b-103">Approvals overview</span></span>

<span data-ttu-id="86a4b-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="86a4b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="86a4b-105">Az idő- és a kiadásbeküldések egy jóváhagyási munkafolyamaton mennek keresztül.</span><span class="sxs-lookup"><span data-stu-id="86a4b-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="86a4b-106">A bejegyzések jóváhagyását követően a rendszer a tényleges adatokban rögzíti a tranzakciókat, és az ütemezésben könyveli az időt.</span><span class="sxs-lookup"><span data-stu-id="86a4b-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="86a4b-107">Jóváhagyási munkamenet</span><span class="sxs-lookup"><span data-stu-id="86a4b-107">Approvals workflow</span></span>
<span data-ttu-id="86a4b-108">Amikor idő- vagy költségbejegyzést hoz létre és küld el, egy jóváhagyásibejegyzés jön létre.</span><span class="sxs-lookup"><span data-stu-id="86a4b-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="86a4b-109">A projekt jóváhagyója vagy felettese áttekinti és jóváhagyja a bejegyzést.</span><span class="sxs-lookup"><span data-stu-id="86a4b-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="86a4b-110">Ha a bejegyzés egy projekthez kapcsolódik, a jóváhagyásakor a rendszer létrehozza a tényleges adatokat.</span><span class="sxs-lookup"><span data-stu-id="86a4b-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="86a4b-111">Ez lehetővé teszi a költségek és a számlázás nyomon követését.</span><span class="sxs-lookup"><span data-stu-id="86a4b-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="86a4b-112">Bejegyzés jóváhagyása</span><span class="sxs-lookup"><span data-stu-id="86a4b-112">Approve an entry</span></span>
<span data-ttu-id="86a4b-113">A **Jóváhagyások** űrlap lehetővé teszi a különböző nézetek közötti váltást, így a különböző típusú jóváhagyások tekinthetők meg.</span><span class="sxs-lookup"><span data-stu-id="86a4b-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="86a4b-114">Nyissa meg a **Jóváhagyások** űrlapot, és válassza a **Kiadások** , az **Idő** vagy a **Visszahívások** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="86a4b-114">Go to the **Approvals** form and select **Expenses** , **Time** , or **Recalls**.</span></span>
2. <span data-ttu-id="86a4b-115">Tekintse át az egyes jóváhagyásokat, és jelölje ki a jóváhagyni kívántakat.</span><span class="sxs-lookup"><span data-stu-id="86a4b-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="86a4b-116">Válassza a **Jóváhagyás** lehetőséget a kijelölt bejegyzések jóváhagyásához.</span><span class="sxs-lookup"><span data-stu-id="86a4b-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="86a4b-117">A rendszer ezeket a bejegyzéseket feldolgozza, és tényleges adatokat vagy foglalást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="86a4b-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="86a4b-118">Bejegyzés elutasítása</span><span class="sxs-lookup"><span data-stu-id="86a4b-118">Reject an entry</span></span>
<span data-ttu-id="86a4b-119">A projekt jóváhagyójaként előfordulhat, hogy a felhasználónak vissza kell küldenie egy bejegyzést a felhasználóhoz helyesbítés céljából.</span><span class="sxs-lookup"><span data-stu-id="86a4b-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="86a4b-120">Nyissa meg a **Jóváhagyások** űrlapot, és válassza ki az elutasítani kívánt bejegyzést.</span><span class="sxs-lookup"><span data-stu-id="86a4b-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="86a4b-121">Válassza az **Elutasítás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="86a4b-121">Select **Reject**.</span></span>
3. <span data-ttu-id="86a4b-122">Nem kötelező – Megjegyzést adhat hozzá az **Elutasítási hozzászólások** párbeszédpanelen, hogy tájékoztassa a felhasználót a bejegyzés visszautasításának okáról.</span><span class="sxs-lookup"><span data-stu-id="86a4b-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="86a4b-123">Kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="86a4b-123">Select **OK**.</span></span> <span data-ttu-id="86a4b-124">A rendszer visszaküldi a bejegyzést a felhasználónak.</span><span class="sxs-lookup"><span data-stu-id="86a4b-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="86a4b-125">Bejegyzések visszavonása</span><span class="sxs-lookup"><span data-stu-id="86a4b-125">Recall entries</span></span>
<span data-ttu-id="86a4b-126">Előfordulhat, hogy egy elküldött bejegyzést vissza kell hívnia.</span><span class="sxs-lookup"><span data-stu-id="86a4b-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="86a4b-127">Ha a bejegyzést még nem hagyták jóvá, akkor a rendszer azonnal visszaküldi.</span><span class="sxs-lookup"><span data-stu-id="86a4b-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="86a4b-128">A jóváhagyott bejegyzésnek azonban jelentős hatása lehet.</span><span class="sxs-lookup"><span data-stu-id="86a4b-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="86a4b-129">A projekt jóváhagyójának jóvá kell hagynia a visszahívást a tranzakció sztornírozásához a tényleges adatokban.</span><span class="sxs-lookup"><span data-stu-id="86a4b-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="86a4b-130">Projekt jóváhagyóinak megadása</span><span class="sxs-lookup"><span data-stu-id="86a4b-130">Specify Project approvers</span></span>
<span data-ttu-id="86a4b-131">Minden projekthez bizonyos számú projektcsapattag tartozik.</span><span class="sxs-lookup"><span data-stu-id="86a4b-131">Each project has a number of project team members.</span></span> <span data-ttu-id="86a4b-132">Megadhatja, hogy mely csoporttagok projektjóváhagyók is egyben.</span><span class="sxs-lookup"><span data-stu-id="86a4b-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="86a4b-133">Lépjen a **Projektek** űrlapra, és nyissa meg a projektet a listából.</span><span class="sxs-lookup"><span data-stu-id="86a4b-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="86a4b-134">A **Csapat** lapon jelölje ki azt a csapattagot, aki a projekt jóváhagyója lesz, majd válassza a **Szerkesztés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="86a4b-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="86a4b-135">Állítsa a **Projektjóváhagyó** mezőjét **Igen** értékre.</span><span class="sxs-lookup"><span data-stu-id="86a4b-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="86a4b-136">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="86a4b-136">Select **Save**.</span></span>
5. <span data-ttu-id="86a4b-137">További projektjóváhagyók hozzáadásához ismételje meg a 2–4. lépést.</span><span class="sxs-lookup"><span data-stu-id="86a4b-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="86a4b-138">A felhasználó felettesének konfigurálása</span><span class="sxs-lookup"><span data-stu-id="86a4b-138">Configure the user's manager</span></span>

1. <span data-ttu-id="86a4b-139">Lépjen a **Beállítások** > **Biztonság** > **Felhasználók** részre.</span><span class="sxs-lookup"><span data-stu-id="86a4b-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="86a4b-140">Válassza ki azt a felhasználót, akihez vezetőt rendel, és a **Szervezet adatai** területen jelölje ki a vezetőt a listából.</span><span class="sxs-lookup"><span data-stu-id="86a4b-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="86a4b-141">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="86a4b-141">Select **Save**.</span></span>


