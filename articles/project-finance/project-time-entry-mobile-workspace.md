---
title: Projektidő-beviteli mobil munkaterület
description: Ez a témakör a Projektidő-beviteli mobil munkaterület használatáról nyújt információkat. Ez a munkaterület lehetővé teszi, hogy a felhasználók a mobileszköz segítségével időt adjanak meg és mentsenek a projekthez.
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: ee11f7f392676adb59bd25f6549737482faf5fdb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752238"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="f958f-104">Projektidő-beviteli mobil munkaterület</span><span class="sxs-lookup"><span data-stu-id="f958f-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f958f-105">Ez a témakör a **Projektidő-beviteli** mobil munkaterület használatáról nyújt információkat.</span><span class="sxs-lookup"><span data-stu-id="f958f-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="f958f-106">Ez a munkaterület lehetővé teszi, hogy a felhasználók a mobileszköz segítségével időt adjanak meg és mentsenek a projekthez.</span><span class="sxs-lookup"><span data-stu-id="f958f-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="f958f-107">Ez a mobil munkaterület a Dynamics 365 Unified Ops mobilalkalmazással való használatra készült.</span><span class="sxs-lookup"><span data-stu-id="f958f-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="f958f-108">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f958f-108">Overview</span></span>
<span data-ttu-id="f958f-109">A napi munkájuk részeként a projektek erőforrásai gyakran vannak helyszínen vagy utaznak.</span><span class="sxs-lookup"><span data-stu-id="f958f-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="f958f-110">A **Projektidő-beviteli** mobil munkaterület lehetővé teszi, hogy a felhasználók a kiválasztott mobileszközön bevigyék egy projekthez tartozó számlázható vagy nem számlázható idejüket.</span><span class="sxs-lookup"><span data-stu-id="f958f-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="f958f-111">Ezért a projekterőforrások bármikor és bárhol rögzíthetik az időbejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="f958f-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="f958f-112">Emellett megtekinthetik a már rögzített időbejegyzéseket is.</span><span class="sxs-lookup"><span data-stu-id="f958f-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="f958f-113">A **Projektidő-beviteli** mobil munkaterületen a felhasználók konkrétan a következő feladatokat végezhetik el:</span><span class="sxs-lookup"><span data-stu-id="f958f-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="f958f-114">A kiválasztott dátumnál adja meg az adott feladatra fordított órák számát.</span><span class="sxs-lookup"><span data-stu-id="f958f-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="f958f-115">Kereshet projekt neve vagy ügyfél alapján, hogy megtalálja a projektet, amelyhez időt kíván megadni.</span><span class="sxs-lookup"><span data-stu-id="f958f-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="f958f-116">Meghatározhatja a felhasznált idő kategóriáját és tevékenységét.</span><span class="sxs-lookup"><span data-stu-id="f958f-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="f958f-117">Rögzítse az időt számlázhatóként vagy nem számlázhatóként a projekt számára.</span><span class="sxs-lookup"><span data-stu-id="f958f-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="f958f-118">Opcionálisan megadhat külső és belső megjegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="f958f-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f958f-119">Előfeltételek</span><span class="sxs-lookup"><span data-stu-id="f958f-119">Prerequisites</span></span>
<span data-ttu-id="f958f-120">Az előfeltételek eltérnek a szervezetnél telepített Microsoft Dynamics 365 verziójától függően.</span><span class="sxs-lookup"><span data-stu-id="f958f-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="f958f-121">Előfeltételek a Dynamics 365 Finance használata esetén</span><span class="sxs-lookup"><span data-stu-id="f958f-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="f958f-122">Ha a szervezetnél Finance van telepítve, a rendszergazdának közzé kell tennie a **Projektidő-beviteli** mobil munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="f958f-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="f958f-123">További információk: [Mobil munkaterület közzététele](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="f958f-123">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="f958f-124">Előfeltételek, ha az 1611-es verziót használja a 3. vagy újabb platformfrissítéssel</span><span class="sxs-lookup"><span data-stu-id="f958f-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="f958f-125">Ha a z 1611-es verzió van telepítve a szervezeténél a 3. vagy újabb platformfrissítéssel, akkor a rendszergazdának a következő előfeltételeket kell elvégeznie.</span><span class="sxs-lookup"><span data-stu-id="f958f-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f958f-126">Előfeltétel</span><span class="sxs-lookup"><span data-stu-id="f958f-126">Prerequisite</span></span></th>
<th><span data-ttu-id="f958f-127">Szerepkör</span><span class="sxs-lookup"><span data-stu-id="f958f-127">Role</span></span></th>
<th><span data-ttu-id="f958f-128">Ismertetés</span><span class="sxs-lookup"><span data-stu-id="f958f-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="f958f-129">Telepítse a KB 4018050 elemet.</span><span class="sxs-lookup"><span data-stu-id="f958f-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="f958f-130">Rendszergazda</span><span class="sxs-lookup"><span data-stu-id="f958f-130">System administrator</span></span></td>
<td><span data-ttu-id="f958f-131">A KB 4018050 egy X++-frissítés vagy -metaadat-gyorsjavítás, amely a <strong>Projektidő-beviteli</strong> mobil munkaterületet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f958f-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="f958f-132">A KB 4018050 megvalósításához a rendszergazdának az alábbi lépéseket kell követnie.</span><span class="sxs-lookup"><span data-stu-id="f958f-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="f958f-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Töltse le a metaadat-gyorsjavítást a Microsoft Dynamics Lifecycle Services (LCS) szolgáltatásból</a>.</span><span class="sxs-lookup"><span data-stu-id="f958f-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="f958f-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Telepítse a metaadat-gyorsjavítást</a>.</span><span class="sxs-lookup"><span data-stu-id="f958f-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="f958f-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Hozzon létre egy telepíthető csomagot,</a> amely tartalmazza az <strong>ApplicationSuite</strong> és <strong>ProjectMobile</strong> modelleket, majd töltse fel a telepíthető csomagokat az LCS-re.</span><span class="sxs-lookup"><span data-stu-id="f958f-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="f958f-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Alkalmazza a telepíthető csomagot</a>.</span><span class="sxs-lookup"><span data-stu-id="f958f-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f958f-137">Tegye közzé a <strong>Projektidő-beviteli</strong> mobil munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="f958f-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="f958f-138">Rendszergazda</span><span class="sxs-lookup"><span data-stu-id="f958f-138">System administrator</span></span></td>
<td><span data-ttu-id="f958f-139">Lásd: <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobil munkaterület közzététele</a>.</span><span class="sxs-lookup"><span data-stu-id="f958f-139">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="f958f-140">Mobilalkalmazás letöltése és telepítése</span><span class="sxs-lookup"><span data-stu-id="f958f-140">Download and install the mobile app</span></span>

<span data-ttu-id="f958f-141">Finance and Operations mobilalkalmazás letöltése és telepítése:</span><span class="sxs-lookup"><span data-stu-id="f958f-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="f958f-142">Android rendszerű telefonokhoz</span><span class="sxs-lookup"><span data-stu-id="f958f-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="f958f-143">iPhone-okhoz</span><span class="sxs-lookup"><span data-stu-id="f958f-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="f958f-144">Bejelentkezés a mobilalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="f958f-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="f958f-145">Indítsa el az alkalmazást a mobileszközén.</span><span class="sxs-lookup"><span data-stu-id="f958f-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="f958f-146">Írja be a Dynamics 365 URL-címét.</span><span class="sxs-lookup"><span data-stu-id="f958f-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="f958f-147">Amikor először jelentkezik be, a rendszer kéri a felhasználónevét és a jelszavát.</span><span class="sxs-lookup"><span data-stu-id="f958f-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="f958f-148">Adja meg a hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="f958f-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="f958f-149">A bejelentkezés után megjelennek a vállalata számára elérhető munkaterületek.</span><span class="sxs-lookup"><span data-stu-id="f958f-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="f958f-150">Ne feledje, hogy ha a rendszergazda később új munkaterületet tesz közzé, akkor frissítenie kell a mobil munkaterületek listáját.</span><span class="sxs-lookup"><span data-stu-id="f958f-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="f958f-151">[![Frissítés húzással](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="f958f-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="f958f-152">Idő megadása a Projektidő-beviteli mobil munkaterület használatával</span><span class="sxs-lookup"><span data-stu-id="f958f-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="f958f-153">A mobileszközön jelölje ki a **Projektidő-beviteli** munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="f958f-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="f958f-154">Válassza az **Időbevitel** elemet.</span><span class="sxs-lookup"><span data-stu-id="f958f-154">Select **Time entry**.</span></span> <span data-ttu-id="f958f-155">A rendszer megjeleníti az aktuális hét naptári dátumait.</span><span class="sxs-lookup"><span data-stu-id="f958f-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="f958f-156">A kiválasztott dátumnál válassza a **Művelet** &gt; **Új bejegyzés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f958f-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="f958f-157">Adja meg a rögzítendő órák számát.</span><span class="sxs-lookup"><span data-stu-id="f958f-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="f958f-158">Válassza ki a projektet az időbevitelhez.</span><span class="sxs-lookup"><span data-stu-id="f958f-158">Select the project for the time entry.</span></span> <span data-ttu-id="f958f-159">A listák az alkalmazásba offline használat céljából betöltött projekteket jelenítik meg.</span><span class="sxs-lookup"><span data-stu-id="f958f-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="f958f-160">Alapértelmezés szerint 50 elem van betöltve, de a fejlesztők megváltoztathatják ezt a számot.</span><span class="sxs-lookup"><span data-stu-id="f958f-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="f958f-161">További tudnivalókért lásd: [Mobil platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="f958f-161">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
6.  <span data-ttu-id="f958f-162">Ha a projekt nem szerepel a listában, akkor válassza a **Keresés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f958f-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="f958f-163">Keressen név szerint, vagy váltson át projektnév vagy ügyfél szerinti keresésre.</span><span class="sxs-lookup"><span data-stu-id="f958f-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="f958f-164">Válasszon ki egy kategóriát.</span><span class="sxs-lookup"><span data-stu-id="f958f-164">Select a category.</span></span> <span data-ttu-id="f958f-165">A listák az alkalmazásba offline használat céljából betöltött kategóriákat jelenítik meg.</span><span class="sxs-lookup"><span data-stu-id="f958f-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="f958f-166">Alapértelmezés szerint 50 elem van betöltve, de a fejlesztők megváltoztathatják ezt a számot.</span><span class="sxs-lookup"><span data-stu-id="f958f-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="f958f-167">További tudnivalókért lásd: [Mobil platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="f958f-167">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
8.  <span data-ttu-id="f958f-168">Ha a kategória nem szerepel a listában, akkor válassza a **Keresés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f958f-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="f958f-169">Keressen kategória szerint, vagy váltson a kategórianév szerint történő keresésre.</span><span class="sxs-lookup"><span data-stu-id="f958f-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="f958f-170">Válasszon egy tevékenységet.</span><span class="sxs-lookup"><span data-stu-id="f958f-170">Select an activity.</span></span> <span data-ttu-id="f958f-171">A listák az alkalmazásba offline használat céljából betöltött tevékenységeket jelenítik meg.</span><span class="sxs-lookup"><span data-stu-id="f958f-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="f958f-172">Alapértelmezés szerint 50 elem van betöltve, de a fejlesztők megváltoztathatják ezt a számot.</span><span class="sxs-lookup"><span data-stu-id="f958f-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="f958f-173">További tudnivalókért lásd: [Mobil platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="f958f-173">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
10. <span data-ttu-id="f958f-174">Ha a tevékenység nem szerepel a listában, akkor válassza a **Keresés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f958f-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="f958f-175">Keressen a tevékenység száma alapján, vagy váltson át cél szerinti keresésre.</span><span class="sxs-lookup"><span data-stu-id="f958f-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="f958f-176">Válassza ki a sortulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="f958f-176">Select the line property.</span></span>
12. <span data-ttu-id="f958f-177">Opcionális: Megadhat külső és belső megjegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="f958f-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="f958f-178">Válassza a **Kész** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f958f-178">Select **Done**.</span></span>
