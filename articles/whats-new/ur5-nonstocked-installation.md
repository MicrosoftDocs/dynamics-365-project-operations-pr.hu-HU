---
title: A Finance környezetben való Project Operations frissítése
description: Ez a témakör információt nyújt a Dynamics 365 Finance környezetben való Project Operations frissítéséről.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 249b8dba17165da04596ec46a625131b9b4daeb5
ms.sourcegitcommit: f4fc6e3a81e8551da050e92f8fde85f8d7b52fbd
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/29/2020
ms.locfileid: "4816628"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="9db99-103">A Finance környezetben való Project Operations frissítése</span><span class="sxs-lookup"><span data-stu-id="9db99-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="9db99-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="9db99-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="9db99-105">Ez a témakör információt nyújt a Dynamics 365 Finance környezetben való Dynamics 365 Project Operations frissítéséről.</span><span class="sxs-lookup"><span data-stu-id="9db99-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="9db99-106">A Project Operations Update 5 (UR5) lehetőségre való frissítéséhez három művelet szükséges:</span><span class="sxs-lookup"><span data-stu-id="9db99-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="9db99-107">A csomag importálása az előzetes verzió projektjébe</span><span class="sxs-lookup"><span data-stu-id="9db99-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="9db99-108">A frissítés telepítése</span><span class="sxs-lookup"><span data-stu-id="9db99-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="9db99-109">Saját Dataverse környezet frissítése</span><span class="sxs-lookup"><span data-stu-id="9db99-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="9db99-110">A csomag importálása az LCS projektjébe</span><span class="sxs-lookup"><span data-stu-id="9db99-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="9db99-111">Bejelentkezés a [Lifecycle Services (LCS)](https://lcs.dynamics.com/) szolgáltatásba Projekttulajdonosként vagy Környezetkezelőként.</span><span class="sxs-lookup"><span data-stu-id="9db99-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="9db99-112">A Projektek listájából válassza az LCS projektjét.</span><span class="sxs-lookup"><span data-stu-id="9db99-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="9db99-113">A **Projekt** lap **Környezetek** csoportjában nyissa meg a frissíteni kívánt környezetet.</span><span class="sxs-lookup"><span data-stu-id="9db99-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="9db99-114">Erősítse meg, hogy a környezet működik.</span><span class="sxs-lookup"><span data-stu-id="9db99-114">Verify that the environment is running.</span></span> <span data-ttu-id="9db99-115">Ha nem indul el, indítsa el a környezetet.</span><span class="sxs-lookup"><span data-stu-id="9db99-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="9db99-116">A **Rendelkezésre álló frissítések** rész **Új kiadás** szakaszában válassza a **Frissítés megtekintése** lehetőséget a 10.0.15-ös frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="9db99-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Frissítés gomb megtekintése](media/view-update.png)

6. <span data-ttu-id="9db99-118">A **Bináris frissítések** oldalon válassza a **Csomag mentése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9db99-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="9db99-119">A **Frissítések áttekintése és mentése** oldalon válassza a **Csomag mentése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9db99-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="9db99-120">A megnyíló **Csomag mentése az eszköztárba** ablaktáblán adja meg a csomag nevét, majd válassza a **Csomag mentése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9db99-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="9db99-121">Amikor az LCS befejezte a csomag mentését, a **Kész** gomb engedélyezve lesz.</span><span class="sxs-lookup"><span data-stu-id="9db99-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="9db99-122">Válassza a **Kész** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9db99-122">Select **Done**.</span></span> <span data-ttu-id="9db99-123">Az LCS ellenőrzi a csomagot.</span><span class="sxs-lookup"><span data-stu-id="9db99-123">LCS will verify the package.</span></span> <span data-ttu-id="9db99-124">Az ellenőrzés eltarthat néhány percig, de legfeljebb egy óráig.</span><span class="sxs-lookup"><span data-stu-id="9db99-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="9db99-125">Alkalmazza a csomag frissítését</span><span class="sxs-lookup"><span data-stu-id="9db99-125">Apply the package update</span></span>

1. <span data-ttu-id="9db99-126">Az LCS-ben, a **Környezet részletei** lapon válassza a **Karbantartás** > **Frissítések alkalmazása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9db99-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="9db99-127">Válassza ki a listában a korábban mentett csomagot, majd válassza az **Alkalmaz** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9db99-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="9db99-128">A csomag telepítésének megerősítéséhez válassza az **Igen** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9db99-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Csomagtelepítés megerősítése párbeszédpanel](media/confirm-package-deployment.png)

4. <span data-ttu-id="9db99-130">Az alkalmazás frissítésének megerősítéséhez válassza az **Igen** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9db99-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Alkalmazásfrissítés megerősítése párbeszédpanel](media/confirm-application-update.png)

<span data-ttu-id="9db99-132">Elindul a telepítés és az alkalmazás frissítése.</span><span class="sxs-lookup"><span data-stu-id="9db99-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="9db99-133">A **Környezet részletei** lapon, a jobb felső sarokban a környezet állapota **Szolgáltatás** állapotra frissül.</span><span class="sxs-lookup"><span data-stu-id="9db99-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="9db99-134">Körülbelül két órán belül befejeződik a frissítés.</span><span class="sxs-lookup"><span data-stu-id="9db99-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="9db99-135">Az alkalmazás kiadási információi **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** érékre, a környezet állapota pedig **Telepítve** értékre frissül.</span><span class="sxs-lookup"><span data-stu-id="9db99-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="9db99-136">Saját Dataverse környezet frissítése</span><span class="sxs-lookup"><span data-stu-id="9db99-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="9db99-137">Jelentkezzen be a [Power Platform felügyeleti központjába](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="9db99-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="9db99-138">Keresse és nyissa meg a listában azt a környezetet, amelyet a Project Operations telepítéséhez használt.</span><span class="sxs-lookup"><span data-stu-id="9db99-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="9db99-139">A **Környezetek** lapon válassza az **Erőforrás** > **Dynamics 365 alkalmazások** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9db99-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="9db99-140">Keresse meg a listán a **Microsoft Dynamics 365 Project Operations**, az **Állapot** oszlopban pedig válassza az **Elérhető frissítés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9db99-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="9db99-141">Jelölje be az **Elfogadom a szolgáltatási feltételeket** jelölőnégyzetet, majd válassza a **Frissítés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9db99-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="9db99-142">A megoldás legújabb verziója kerül telepítésre.</span><span class="sxs-lookup"><span data-stu-id="9db99-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="9db99-143">A telepítés befejezését követően telepítve lesz a 4.5.0.134-es verzió.</span><span class="sxs-lookup"><span data-stu-id="9db99-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="9db99-144">Új funkciók konfigurálása</span><span class="sxs-lookup"><span data-stu-id="9db99-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="9db99-145">Kettős írás leképezésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="9db99-145">Enable dual-write mapping</span></span>

<span data-ttu-id="9db99-146">A Finance and Dataverse környezetek frissítésének befejezése után engedélyezheti a kettős írás leképezéseket.</span><span class="sxs-lookup"><span data-stu-id="9db99-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="9db99-147">Fejezze be az alábbi műveleteket a kettős írás leképezéseinek engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="9db99-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="9db99-148">A Customer Engagement környezet biztonsági beállításainak frissítése</span><span class="sxs-lookup"><span data-stu-id="9db99-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="9db99-149">Adatok frissítése entitásokban</span><span class="sxs-lookup"><span data-stu-id="9db99-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="9db99-150">A kettős írású leképezések frissítése és futtatása</span><span class="sxs-lookup"><span data-stu-id="9db99-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="9db99-151">A Dataverse környezet biztonsági beállításainak frissítése</span><span class="sxs-lookup"><span data-stu-id="9db99-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="9db99-152">Az entitások biztonsági jogosultságának alábbi frissítései az UR5-ös verzióra való frissítés részeként szükségesek.</span><span class="sxs-lookup"><span data-stu-id="9db99-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="9db99-153">A Dataverse környezetben válassza a **Beállítások** lehetőséget, és a **Rendszer** csoportban válassza a **Biztonság** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9db99-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Dataverse-környezet beállításai](media/Picture21.png)

2. <span data-ttu-id="9db99-155">Válassza a **Biztonsági szerepkörök** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9db99-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="9db99-156">A szerepkörök listájából válassza ki a **kettős írású alkalmazásfelhasználót**, majd válassza az **Egyéni entitások** fület.</span><span class="sxs-lookup"><span data-stu-id="9db99-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="9db99-157">Ellenőrizze, hogy rendelkezik-e a szerepkörhöz **Olvasás** és **Hozzáfűzés** jogosultságokkal a következőhöz:</span><span class="sxs-lookup"><span data-stu-id="9db99-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="9db99-158">**Pénznem árfolyamának típusa**</span><span class="sxs-lookup"><span data-stu-id="9db99-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="9db99-159">**Partnerek diagramja**</span><span class="sxs-lookup"><span data-stu-id="9db99-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="9db99-160">**Pénzügyi naptár**</span><span class="sxs-lookup"><span data-stu-id="9db99-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="9db99-161">**Főkönyv**</span><span class="sxs-lookup"><span data-stu-id="9db99-161">**Ledger**</span></span>

5. <span data-ttu-id="9db99-162">A biztonsági szerepkör után menjen a **Beállítások** > **Biztonsági** > **Csoportok** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="9db99-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="9db99-163">Ellenőrizze, hogy a **kettős írású alkalmazásfelhasználói** szerepkör alkalmazva van-e a csoportra.</span><span class="sxs-lookup"><span data-stu-id="9db99-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="9db99-164">Adatentitások frissítése a frissítésből</span><span class="sxs-lookup"><span data-stu-id="9db99-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="9db99-165">Nyissa meg a Finance környezetben az **Adatkezelés** munkaterületet, majd nyissa meg a **Keretrendszer paraméterei** oldalt.</span><span class="sxs-lookup"><span data-stu-id="9db99-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="9db99-166">Az **Entitásbeállítások** lapon válassza az **Entitáslista frissítése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9db99-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="9db99-167">Az entitás frissítésének megerősítéséhez válassza a **Bezárás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9db99-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="9db99-168">Ez a művelet körülbelül 20 percet vesz igénybe.</span><span class="sxs-lookup"><span data-stu-id="9db99-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="9db99-169">A frissítés befejezéséről értesítést fog kapni.</span><span class="sxs-lookup"><span data-stu-id="9db99-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="9db99-170">Kettős írás leképezéseinek frissítése</span><span class="sxs-lookup"><span data-stu-id="9db99-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="9db99-171">Az **Adatkezelés** munkaterületen válassza a **Kettős írás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9db99-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="9db99-172">Válassza a **Megoldások alkalmazása** lehetőséget, jelölje ki mindkét megoldást a listában, majd válassza az **Alkalmaz** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9db99-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="9db99-173">A **Kettős írás** lapon jelölje ki az alábbi táblákat, majd válassza a **Leállítás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9db99-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="9db99-174">**Project Operations integrációjának tényleges adatai (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="9db99-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="9db99-175">**Project Operations integrációs projekt költségkategóriái (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="9db99-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="9db99-176">**Project Operations integrációs tényleges projektköltségek exportálási entitása (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="9db99-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="9db99-177">A **Tábla leképezési verziója** lapon alkalmazza a leképezés új verzióját mindhárom entitásra.</span><span class="sxs-lookup"><span data-stu-id="9db99-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="9db99-178">A **Kettős írás** lapon válassza a futtatás lehetőséget a leképezések újraindításához.</span><span class="sxs-lookup"><span data-stu-id="9db99-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="9db99-179">A leképezések listájában válassza ki a **Főkönyvi (msdyn_ledgers)** leképezés minden előfeltételét, majd jelölje ki a **Kezdeti szinkronizálás** jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="9db99-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="9db99-180">Válassza ki a **Kezdeti szinkronizálás fő eleme** mezőjében az **Finance and Operations alkalmazásokat**, majd válassza a **Futtatás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9db99-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Főkönyvi leképezés szinkronizálása](media/DW6.png)
 
