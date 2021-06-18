---
title: Microsoft Project Client integráció
description: A projektek ütemezésének tervezése és karbantartása összetett lehet, így a projektmenedzsereknek a feladat kezelését segítő eszközöket kell használniuk. A Microsoft Project Client programmal történő integráció segítséget nyújt a projekt munkalebontási struktúrájának megnyitásához és kezeléséhez.
author: Yowelle
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 032d726bb6206c563b573f30d13fe2697a13c949
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999449"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="d5b0d-104">Microsoft Project Client integráció</span><span class="sxs-lookup"><span data-stu-id="d5b0d-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5b0d-105">A projektek ütemezésének tervezése és karbantartása összetett lehet, így a projektmenedzsereknek a feladat kezelését segítő eszközöket kell használniuk.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="d5b0d-106">A Microsoft Project Client programmal történő integráció segítséget nyújt a projekt munkalebontási struktúrájának megnyitásához és kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="d5b0d-107">A projektmenedzser bármilyen változást közzétehet a Dynamics 365 Finance projekt munkalebontási szerkezetében.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="d5b0d-108">A júliusi frissítés (10.0.4 verzió) használata esetén a KB 4054797 és 4055884 telepítése szükséges.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="d5b0d-109">A Microsoft Project Client bővítmény konfigurálása</span><span class="sxs-lookup"><span data-stu-id="d5b0d-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="d5b0d-110">A Microsoft Project Client programmal való integráció engedélyezéséhez egy Microsoft Dynamics 365-bővítményt kell telepíteni a felhasználó kliensének Microsoft Project alkalmazásba.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="d5b0d-111">Ezt a **Projektmenedzsment-munkaterület** megnyitásával teheti meg.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="d5b0d-112">•   Kattintson a **Projektkliens-bővítmény konfigurálása** lehetőségre a **Hivatkozások** > **Beállítás** szakaszban a munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="d5b0d-113">•   Kattintson a **Megnyitás** lehetőségre, majd kattintson a **Futtatás** lehetőségre, amikor a rendszer rákérdez.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="d5b0d-114">A meglévő vázlat munkalebontási struktúra megnyitása és módosítása a Microsoft Project Client alkalmazásban</span><span class="sxs-lookup"><span data-stu-id="d5b0d-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="d5b0d-115">Ha egy Dynamics 365 Finance projekthez már létrehoztak egy munkalebontási struktúrát, akkor a munkalebontási struktúra megnyitható a Microsoft Project Client alkalmazásban, ha a munkalebontási struktúra vázlat állapotú.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="d5b0d-116">A **Projekt** oldalról való megnyitáshoz kattintson a **Megnyitás Microsoft Project alkalmazásban** hivatkozásra a **Terv** lapról. Ez az oldal megnyitható a Microsoft Project Client alkalmazásból is a **Megnyitás** lehetőségre kattintva a **Microsoft Dynamics 365** lapon. Válassza a **Jogi entitás** és a **Projekt** elemet a listáról.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="d5b0d-117">Ha Internet Explorer böngészőt használ, kattintson a **Mentés** gombra, hogy a fájl letöltési helyéről manuálisan meg tudja nyitni a fájlt.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="d5b0d-118">Másik lehetőségként a **Mentés és megnyitás** gombra kattintva nyissa meg a fájlt a Microsoft Project Client programban.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="d5b0d-119">Mentéskor ne nevezze át a fájlt.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="d5b0d-120">Mielőtt a Microsoft Project Client program segítségével szerkeszti a fájlt, ki kell vennie azt. Kattintson **Kivétel** lehetőségre a **Microsoft Dynamics 365** lapon. Ezzel megakadályozhatja, hogy több felhasználó egyidejűleg szerkessze a munkalebontási struktúrát a Finance rendszerből.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="d5b0d-121">Ha bármilyen módosítás befejezése után közzé szeretné tenni a munkalebontási struktúrát, akkor kattintson a **Beadás** lehetőségre a **Microsoft Dynamics 365** lapon.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="d5b0d-122">Ha egy projektcsapat már hozzá van adva a projekthez a Finance rendszerben, akkor a program a csoport tagjaival tölti fel az erőforráslistát.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="d5b0d-123">Ha egy projektcsapat még nincs hozzáadva a projekthez, akkor kiválaszthat erőforrásokat, és összeállíthatja a csapatot a Microsoft Project Client alkalmazásban az **Erőforrások** gombra kattintva a **Microsoft Dynamics 365** lapon.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="d5b0d-124">A bejelentkezési folyamat részeként a következő adatok kerülnek visszaszinkronizálásba a Finance alkalmazásba:</span><span class="sxs-lookup"><span data-stu-id="d5b0d-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="d5b0d-125">•   Feladat neve</span><span class="sxs-lookup"><span data-stu-id="d5b0d-125">•   Task name</span></span>

<span data-ttu-id="d5b0d-126">•   Kezdő dátum</span><span class="sxs-lookup"><span data-stu-id="d5b0d-126">•   Start date</span></span>

<span data-ttu-id="d5b0d-127">•   Befejezési dátum</span><span class="sxs-lookup"><span data-stu-id="d5b0d-127">•   Finish date</span></span>

<span data-ttu-id="d5b0d-128">•   Megelőző tevékenységek</span><span class="sxs-lookup"><span data-stu-id="d5b0d-128">•   Predecessors</span></span>

<span data-ttu-id="d5b0d-129">•   Erőforrásnevek</span><span class="sxs-lookup"><span data-stu-id="d5b0d-129">•   Resource names</span></span>

<span data-ttu-id="d5b0d-130">•   Kategória</span><span class="sxs-lookup"><span data-stu-id="d5b0d-130">•   Category</span></span>

<span data-ttu-id="d5b0d-131">•   Erőforrás-kategória</span><span class="sxs-lookup"><span data-stu-id="d5b0d-131">•   Resource category</span></span>

<span data-ttu-id="d5b0d-132">•   Munkaórák</span><span class="sxs-lookup"><span data-stu-id="d5b0d-132">•   Work hours</span></span>

<span data-ttu-id="d5b0d-133">•   Megjegyzések</span><span class="sxs-lookup"><span data-stu-id="d5b0d-133">•   Notes</span></span>

<span data-ttu-id="d5b0d-134">•   Prioritás</span><span class="sxs-lookup"><span data-stu-id="d5b0d-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="d5b0d-135">Ha további oszlopokat ad hozzá a Microsoft Project Client fájlhoz, akkor a program ezeket a fájlokat nem menti a fájlba, és a fájl ismételt megnyitásakor nem fog megjelenni.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="d5b0d-136">Meglévő projekt munkalebontási struktúrájának létrehozása a Microsoft Project Client használatával</span><span class="sxs-lookup"><span data-stu-id="d5b0d-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="d5b0d-137">Új munkalebontási struktúra létrehozásához a Microsoft Project Client használatával, tegye a következőket:</span><span class="sxs-lookup"><span data-stu-id="d5b0d-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="d5b0d-138">Nyissa meg a Microsoft Project Client alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="d5b0d-139">A **Microsoft Dynamics 365** lapon kattintson a **Megnyitás** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="d5b0d-140">Válassza ki a projekt **Jogi entitását**.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="d5b0d-141">Válassza ki a **Projekt** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="d5b0d-142">Kattintson a **Kivétel** lehetőségre a **Microsoft Dynamics 365** lapon.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="d5b0d-143">Ha készen áll a közzétételre a Finance rendszerbe, akkor kattintson **Beadás** lehetőségre a **Microsoft Dynamics 365** lapon.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="d5b0d-144">Meglévő projekt meglévő munkalebontási struktúrájának cseréje a Microsoft Project Client használatával</span><span class="sxs-lookup"><span data-stu-id="d5b0d-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="d5b0d-145">Ha új munkalebontási struktúrát szeretne létrehozni a Microsoft Project Client segítségével, és lecserélni egy meglévő projekt meglévő munkalebontási struktúráját, hajtsa végre a következő lépéseket:</span><span class="sxs-lookup"><span data-stu-id="d5b0d-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="d5b0d-146">Nyissa meg a Microsoft Project Client alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="d5b0d-147">Hozzon létre egy ütemezést a Microsoft Project Client alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="d5b0d-148">A **Microsoft Dynamics 365** lapon kattintson a **Változtatások mentése** > **Meglévő projekt cseréje** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="d5b0d-149">Válassza ki a projekt **Jogi entitását**.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="d5b0d-150">Válassza ki a **Projekt** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="d5b0d-151">Kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="d5b0d-152">Új projekt létrehozása a Microsoft Project Client alkalmazásból</span><span class="sxs-lookup"><span data-stu-id="d5b0d-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="d5b0d-153">Nyissa meg a Microsoft Project Client alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="d5b0d-154">Hozzon létre egy ütemezést a Microsoft Project Client alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="d5b0d-155">A **Microsoft Dynamics 365** lapon kattintson a **Változtatások mentése** > **Mentés új projektbe** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="d5b0d-156">Válassza ki a projekt **Jogi entitását**.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="d5b0d-157">Szükség esetén adja meg a **Projektazonosító** elemet.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="d5b0d-158">Adja meg a **Projektnév** elemet.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="d5b0d-159">Válassza ki a **Projekttípus**, a **Projektcsoport** és a **Projektszerződés azonosítója** elemeket.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="d5b0d-160">Másik lehetőségként új projektszerződés is létrehozható az **Új** elemre kattintva.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="d5b0d-161">Válassza ki az erőforrás biztosításához használt **Naptár** elemet.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="d5b0d-162">Kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="d5b0d-162">Click **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]