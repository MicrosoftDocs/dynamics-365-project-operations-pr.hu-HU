---
title: Új környezet kiépítése
description: Ez a témakör az új Project Operations-környezet kialakításának módjával kapcsolatban tartalmaz tájékoztatást.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949365"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="3aa82-103">Új környezet kiépítése</span><span class="sxs-lookup"><span data-stu-id="3aa82-103">Provision a new environment</span></span>

<span data-ttu-id="3aa82-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="3aa82-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3aa82-105">Ez a témakör információt nyújt arról, hogyan lehet új Dynamics 365 Project Operations-környezetet létrehozni az erőforrás-/nem készletalapú forgatókönyvek esetén.</span><span class="sxs-lookup"><span data-stu-id="3aa82-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="3aa82-106">Az automatizált Project Operations-kiépítés engedélyezése egy LCS-projektben</span><span class="sxs-lookup"><span data-stu-id="3aa82-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="3aa82-107">A következő lépésekkel engedélyezheti az automatizált Project Operations-kiépítést az LCS-projektjéhez.</span><span class="sxs-lookup"><span data-stu-id="3aa82-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="3aa82-108">Lépjen az [LCS](https://lcs.dynamics.com/v2) lehetőségre, és válassza az **Előnézeti funkció kezelése** csempét.</span><span class="sxs-lookup"><span data-stu-id="3aa82-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="3aa82-109">Az **Előnézeti funkció** listában jelölje ki a **Project Operations** lehetőséget, majd válassza az **Előnézet funkció engedélyezve** lehetőséget a Project Operations engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="3aa82-109">In the **Preview feature** list, select **Project Operations** and the select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="3aa82-110">Ez a lépés csak egy alkalommal hajtható végre LCS-projektenként.</span><span class="sxs-lookup"><span data-stu-id="3aa82-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="3aa82-111">Project Operations-környezet kiépítése</span><span class="sxs-lookup"><span data-stu-id="3aa82-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="3aa82-112">Nyisson meg egy új Dynamics 365 Finance [bemutató környezet](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) vagy [teszt-/éles környezet](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) telepítést.</span><span class="sxs-lookup"><span data-stu-id="3aa82-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="3aa82-113">Haladjon végig a **Környezet kiépítése** varázslón.</span><span class="sxs-lookup"><span data-stu-id="3aa82-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="3aa82-114">Ügyeljen arra, hogy a kijelölt alkalmazás verziója 10.0.13 vagy magasabb legyen.</span><span class="sxs-lookup"><span data-stu-id="3aa82-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="3aa82-115">A Project Operations kiépítéséhez az **Speciális beállítások** területen válassza a **Common Data Service** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="3aa82-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="3aa82-116">Engedélyezze a **Common Data Service beállítást** az **Igen** kiválasztásával, majd adja meg az adatokat a kötelező mezőkben:</span><span class="sxs-lookup"><span data-stu-id="3aa82-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="3aa82-117">Adatfolyam neve</span><span class="sxs-lookup"><span data-stu-id="3aa82-117">Name</span></span>
  - <span data-ttu-id="3aa82-118">Régió</span><span class="sxs-lookup"><span data-stu-id="3aa82-118">Region</span></span>
  - <span data-ttu-id="3aa82-119">Nyelv</span><span class="sxs-lookup"><span data-stu-id="3aa82-119">Language</span></span>
  - <span data-ttu-id="3aa82-120">Pénznem</span><span class="sxs-lookup"><span data-stu-id="3aa82-120">Currency</span></span>
 
5. <span data-ttu-id="3aa82-121">A **Common Data Service-sablon** mezőben jelölje ki a **Project Operations** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="3aa82-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="3aa82-122">Válassza ki a telepítésének környezettípusát.</span><span class="sxs-lookup"><span data-stu-id="3aa82-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="3aa82-123">Az előfizetésen alapuló próbaverzió 30 napig teszi lehetővé a CDS-környezet telepítését.</span><span class="sxs-lookup"><span data-stu-id="3aa82-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Telepítés beállításai](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="3aa82-125">Válassza az **Elfogadom** lehetőséget a szolgáltatási feltételek elfogadásához, majd válassza a **Kész** lehetőséget a telepítési beállításokhoz való visszatéréshez.</span><span class="sxs-lookup"><span data-stu-id="3aa82-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Telepítési hozzájárulás](./media/2DeploymentConsent.png)

7. <span data-ttu-id="3aa82-127">Töltse ki a többi kötelező mezőt a varázslóban, és erősítse meg a telepítést.</span><span class="sxs-lookup"><span data-stu-id="3aa82-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="3aa82-128">A környezet kiépítési ideje a környezet típusától függően változik.</span><span class="sxs-lookup"><span data-stu-id="3aa82-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="3aa82-129">A kiépítés akár hat óráig is eltarthat.</span><span class="sxs-lookup"><span data-stu-id="3aa82-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="3aa82-130">A telepítés sikeres végrehajtása után a környezet **Telepített** állapottal jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="3aa82-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="3aa82-131">A környezet sikeres telepítésének ellenőrzéséhez válassza a **Bejelentkezés** lehetőséget, és jelentkezzen be a környezetbe a megerősítéshez.</span><span class="sxs-lookup"><span data-stu-id="3aa82-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![A  környezetek részletei](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="3aa82-133">Project Operations Finance bemutató adatainak alkalmazása (nem kötelező lépés)</span><span class="sxs-lookup"><span data-stu-id="3aa82-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="3aa82-134">A Project Operations Finance bemutató adatait a 10.0.13-as szervizkiadású felhőben szolgáltatott környezethez az [ebben a cikkben](resource-apply-finance-demo-data.md) leírtak szerint alkalmazhatja.</span><span class="sxs-lookup"><span data-stu-id="3aa82-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="3aa82-135">A Finance-környezet frissítéseinek alkalmazása.</span><span class="sxs-lookup"><span data-stu-id="3aa82-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="3aa82-136">A Project Operations egy Finance-környezetet igényel **10.0.13 (10.0.569.20009)** vagy újabb verziószámú alkalmazással.</span><span class="sxs-lookup"><span data-stu-id="3aa82-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="3aa82-137">Előfordulhat, hogy a Finance-környezetre minőségi frissítéseket kell alkalmaznia ahhoz, hogy ezt a verziót kapja.</span><span class="sxs-lookup"><span data-stu-id="3aa82-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="3aa82-138">A LCS **Környezet részletei** oldalán a **Rendelkezésre álló frissítések** területen válassza a **Frissítések megtekintése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="3aa82-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Frissítések megtekintése](./media/5ViewUpdates.png)

2. <span data-ttu-id="3aa82-140">A **Bináris frissítések** oldalon válassza a **Csomag mentése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="3aa82-140">On the **Binary updates** page, select **Save package.**</span></span>

![Csomag mentése](./media/6SavePackage.png)

3. <span data-ttu-id="3aa82-142">Kattintson az **Összes kiválasztása** elemre, majd válassza a **Csomag mentése** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="3aa82-142">Click **Select all** and then select **Save package**.</span></span>

![Frissítések áttekintése és mentése](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="3aa82-144">Adja meg a csomag nevét és leírását, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="3aa82-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="3aa82-145">Az internetkapcsolattól függően ez a folyamat eltarthat egy ideig.</span><span class="sxs-lookup"><span data-stu-id="3aa82-145">Depending on the internet connection, this process might take some time.</span></span>

![Csomag feltöltése az Eszközök könyvtárba](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="3aa82-147">A csomag mentése után válassza a **Kész** lehetőséget, és mentse a csomagot az LCS-projekt Eszközök könyvtárába.</span><span class="sxs-lookup"><span data-stu-id="3aa82-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="3aa82-148">A csomag mentése és ellenőrzése ~15 percet is igénybe vehet.</span><span class="sxs-lookup"><span data-stu-id="3aa82-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="3aa82-149">A frissítés alkalmazásához keresse meg a **Környezet részletei** oldalt az LCS-ben, és válassza a **Karbantartás** > **Frissítések alkalmazása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="3aa82-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Környezetek karbantartása](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="3aa82-151">A frissítések listájában jelölje ki a létrehozott csomagot, majd válassza az **Alkalmaz** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="3aa82-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Frissítések alkalmazása](./media/10ApplyUpdates.png)

<span data-ttu-id="3aa82-153">A környezet javítása eltarthat egy ideig.</span><span class="sxs-lookup"><span data-stu-id="3aa82-153">Environment servicing will take some time.</span></span> <span data-ttu-id="3aa82-154">Miután befejeződött, a környezet visszatér egy telepített állapotba.</span><span class="sxs-lookup"><span data-stu-id="3aa82-154">After it is complete, the environment will return to a deployed state.</span></span>

![Környezet telepítve](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="3aa82-156">Kettős írási kapcsolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="3aa82-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="3aa82-157">A LCS-projektben nyissa meg a **Környezet részletei** oldalt.</span><span class="sxs-lookup"><span data-stu-id="3aa82-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="3aa82-158">A **Common Data Service-környezet információi** területen válassza az **A CDS for Apps hivatkozása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="3aa82-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="3aa82-159">A hivatkozás létrejöttét követően válassza ismét az **A CDS for Apps hivatkozása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="3aa82-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="3aa82-160">A rendszer átirányítja a kettős írásra a Finance-ben.</span><span class="sxs-lookup"><span data-stu-id="3aa82-160">You will be redirected to Dual Write in Finance.</span></span>

![A CDS for Apps hivatkozása](./media/12LinktoCDS.png)

4. <span data-ttu-id="3aa82-162">Válassza **Megoldás alkalmazása** lehetőséget az integrációba leképezni kívánt entitások eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="3aa82-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Megoldások alkalmazása](./media/13ApplySolutions.png)

5. <span data-ttu-id="3aa82-164">Válassza ki a **Dynamics 365 Finance and Operations kettős írású entitások leképezése** és a **Dynamics 365 Project Operations kettős írású entitások leképezése** elemet, majd válassza az **Alkalmaz** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="3aa82-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Megoldások megerősítése](./media/14ConfirmSolutions.png)

<span data-ttu-id="3aa82-166">A megoldások alkalmazása után a kettős írási entitások alkalmazásra kerülnek a környezetre.</span><span class="sxs-lookup"><span data-stu-id="3aa82-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Megoldások alkalmazása](./media/15ApplyingSolutions.png)

<span data-ttu-id="3aa82-168">Az entitások alkalmazása után az összes elérhető leképezés megjelenik a környezetben.</span><span class="sxs-lookup"><span data-stu-id="3aa82-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Kettős írású leképezések](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="3aa82-170">Az adatentitások frissítése a frissítés után</span><span class="sxs-lookup"><span data-stu-id="3aa82-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="3aa82-171">A Finance-ben nyissa meg az **Adatkezelés** munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="3aa82-171">In Finance, go to the **Data management** workspace.</span></span>

![Adatkezelési munkaterület](./media/16DataManagement.png)

2. <span data-ttu-id="3aa82-173">Válassza ki a **Keretrendszer paraméterei** csempét.</span><span class="sxs-lookup"><span data-stu-id="3aa82-173">Select the **Framework parameters** tile.</span></span>

![Keretrendszer paraméterei](./media/17FrameworkParameters.png)

3. <span data-ttu-id="3aa82-175">Az **Entitás beállításai** oldalon válassza az **Entitások listájának frissítése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="3aa82-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Entitáslista frissítése](./media/18RefreshEntityList.png)

<span data-ttu-id="3aa82-177">A frissítés megközelítőleg 20 percet vesz igénybe.</span><span class="sxs-lookup"><span data-stu-id="3aa82-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="3aa82-178">A rendszer értesítést küld, amikor elkészült.</span><span class="sxs-lookup"><span data-stu-id="3aa82-178">You will receive an alert when it is complete.</span></span>

![Frissítés megerősítése](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="3aa82-180">Project Operations kettős írás leképezéseinek futtatása</span><span class="sxs-lookup"><span data-stu-id="3aa82-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="3aa82-181">A LCS-projektben nyissa meg a **Környezet részletei** oldalt.</span><span class="sxs-lookup"><span data-stu-id="3aa82-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="3aa82-182">A **Common Data Service-környezet információi** területen válassza az **A CDS for Apps hivatkozása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="3aa82-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="3aa82-183">Miután kijelölte a hivatkozást, a rendszer átirányítja a leképezésekben szereplő entitások listájára.</span><span class="sxs-lookup"><span data-stu-id="3aa82-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="3aa82-184">Indítsa el a leképezéseket következő táblázatban leírtak szerint.</span><span class="sxs-lookup"><span data-stu-id="3aa82-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="3aa82-185">Ügyeljen arra, hogy a listában szereplő sorrendet kövesse.</span><span class="sxs-lookup"><span data-stu-id="3aa82-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="3aa82-186">**Entitásleképezés**</span><span class="sxs-lookup"><span data-stu-id="3aa82-186">**Entity Map**</span></span> | <span data-ttu-id="3aa82-187">**Entitás frissítése**</span><span class="sxs-lookup"><span data-stu-id="3aa82-187">**Refresh entity**</span></span> | <span data-ttu-id="3aa82-188">**Kezdeti szinkronizálás**</span><span class="sxs-lookup"><span data-stu-id="3aa82-188">**Initial sync**</span></span> | <span data-ttu-id="3aa82-189">**Kezdeti szinkronizálás fő eleme**</span><span class="sxs-lookup"><span data-stu-id="3aa82-189">**Master for initial sync**</span></span> | <span data-ttu-id="3aa82-190">**Előfeltételek futtatása**</span><span class="sxs-lookup"><span data-stu-id="3aa82-190">**Run prerequisites**</span></span> | <span data-ttu-id="3aa82-191">**Előfeltételek kezdeti szinkronizálása**</span><span class="sxs-lookup"><span data-stu-id="3aa82-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="3aa82-192">**Az összes vállalat projekterőforrás-szerepkörei (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="3aa82-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="3aa82-193">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-193">No</span></span> | <span data-ttu-id="3aa82-194">Igen</span><span class="sxs-lookup"><span data-stu-id="3aa82-194">Yes</span></span> | <span data-ttu-id="3aa82-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3aa82-195">Common Data Service</span></span> | <span data-ttu-id="3aa82-196">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-196">No</span></span> | <span data-ttu-id="3aa82-197">N. a.</span><span class="sxs-lookup"><span data-stu-id="3aa82-197">N\A</span></span> |
| <span data-ttu-id="3aa82-198">**Jogi entitások (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="3aa82-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="3aa82-199">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-199">No</span></span> | <span data-ttu-id="3aa82-200">Igen</span><span class="sxs-lookup"><span data-stu-id="3aa82-200">Yes</span></span> | <span data-ttu-id="3aa82-201">Finance and Operations alkalmazások</span><span class="sxs-lookup"><span data-stu-id="3aa82-201">Finance and Operations apps</span></span> | <span data-ttu-id="3aa82-202">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-202">No</span></span> | <span data-ttu-id="3aa82-203">N. a.</span><span class="sxs-lookup"><span data-stu-id="3aa82-203">N\A</span></span> |
| <span data-ttu-id="3aa82-204">**Projekttevékenységek integrációjának tényleges adatai (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="3aa82-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="3aa82-205">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-205">No</span></span> | <span data-ttu-id="3aa82-206">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-206">No</span></span> | <span data-ttu-id="3aa82-207">N. a.</span><span class="sxs-lookup"><span data-stu-id="3aa82-207">N\A</span></span> | <span data-ttu-id="3aa82-208">Igen</span><span class="sxs-lookup"><span data-stu-id="3aa82-208">Yes</span></span> | <span data-ttu-id="3aa82-209">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-209">No</span></span> |
| <span data-ttu-id="3aa82-210">**Projektszerződéssorok (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="3aa82-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="3aa82-211">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-211">No</span></span> | <span data-ttu-id="3aa82-212">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-212">No</span></span> | <span data-ttu-id="3aa82-213">N. a.</span><span class="sxs-lookup"><span data-stu-id="3aa82-213">N\A</span></span> | <span data-ttu-id="3aa82-214">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-214">No</span></span> | <span data-ttu-id="3aa82-215">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-215">No</span></span> |
| <span data-ttu-id="3aa82-216">**A projekt tranzakciókapcsolatainak integrációs entitása (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="3aa82-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="3aa82-217">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-217">No</span></span> | <span data-ttu-id="3aa82-218">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-218">No</span></span> | <span data-ttu-id="3aa82-219">N. a.</span><span class="sxs-lookup"><span data-stu-id="3aa82-219">N\A</span></span> | <span data-ttu-id="3aa82-220">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-220">No</span></span> | <span data-ttu-id="3aa82-221">N. a.</span><span class="sxs-lookup"><span data-stu-id="3aa82-221">N\A</span></span> |
| <span data-ttu-id="3aa82-222">**A Project Operations integráció szerződéssor-mérföldkövei (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="3aa82-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="3aa82-223">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-223">No</span></span> | <span data-ttu-id="3aa82-224">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-224">No</span></span> | <span data-ttu-id="3aa82-225">N. a.</span><span class="sxs-lookup"><span data-stu-id="3aa82-225">N\A</span></span> | <span data-ttu-id="3aa82-226">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-226">No</span></span> | <span data-ttu-id="3aa82-227">N. a.</span><span class="sxs-lookup"><span data-stu-id="3aa82-227">N\A</span></span> |
| <span data-ttu-id="3aa82-228">**A Project Operations integrációs entitása kiadások becsléséhez (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="3aa82-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="3aa82-229">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-229">No</span></span> | <span data-ttu-id="3aa82-230">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-230">No</span></span> | <span data-ttu-id="3aa82-231">N. a.</span><span class="sxs-lookup"><span data-stu-id="3aa82-231">N\A</span></span> | <span data-ttu-id="3aa82-232">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-232">No</span></span> | <span data-ttu-id="3aa82-233">N. a.</span><span class="sxs-lookup"><span data-stu-id="3aa82-233">N\A</span></span> |
| <span data-ttu-id="3aa82-234">**A Project Operations integrációs entitása órabecslésekhez (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="3aa82-234">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="3aa82-235">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-235">No</span></span> | <span data-ttu-id="3aa82-236">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-236">No</span></span> | <span data-ttu-id="3aa82-237">N. a.</span><span class="sxs-lookup"><span data-stu-id="3aa82-237">N\A</span></span> | <span data-ttu-id="3aa82-238">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-238">No</span></span> | <span data-ttu-id="3aa82-239">N. a.</span><span class="sxs-lookup"><span data-stu-id="3aa82-239">N\A</span></span> |
| <span data-ttu-id="3aa82-240">**Project Operations integráció projektkiadások exportálási entitása (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="3aa82-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="3aa82-241">Igen</span><span class="sxs-lookup"><span data-stu-id="3aa82-241">Yes</span></span> | <span data-ttu-id="3aa82-242">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-242">No</span></span> | <span data-ttu-id="3aa82-243">N. a.</span><span class="sxs-lookup"><span data-stu-id="3aa82-243">N\A</span></span> | <span data-ttu-id="3aa82-244">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-244">No</span></span> | <span data-ttu-id="3aa82-245">N. a.</span><span class="sxs-lookup"><span data-stu-id="3aa82-245">N\A</span></span> |
| <span data-ttu-id="3aa82-246">**A Project Operations integrációs entitása órabecslésekhez (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="3aa82-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="3aa82-247">Igen</span><span class="sxs-lookup"><span data-stu-id="3aa82-247">Yes</span></span> | <span data-ttu-id="3aa82-248">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-248">No</span></span> | <span data-ttu-id="3aa82-249">N. a.</span><span class="sxs-lookup"><span data-stu-id="3aa82-249">N\A</span></span> | <span data-ttu-id="3aa82-250">Nincs</span><span class="sxs-lookup"><span data-stu-id="3aa82-250">No</span></span> | <span data-ttu-id="3aa82-251">N. a.</span><span class="sxs-lookup"><span data-stu-id="3aa82-251">N\A</span></span> |

4. <span data-ttu-id="3aa82-252">Az entitás frissítéséhez jelölje ki a leképezés nevét, majd válassza az **Entitások frissítése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="3aa82-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 
5. <span data-ttu-id="3aa82-253">A frissítés befejeződése után folytassa a leképezés futtatását.</span><span class="sxs-lookup"><span data-stu-id="3aa82-253">Proceed with running the map after the refresh is complete.</span></span>

![Leképezés frissítése](./media/20RefreshMapping.png)

<span data-ttu-id="3aa82-255">A következő leképezés engedélyezése előtt ellenőrizze, hogy a táblázatban a leképezés **Fut** állapotban van-e.</span><span class="sxs-lookup"><span data-stu-id="3aa82-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="3aa82-256">A nagy számú előfeltétellel rendelkező leképezések futtatása eltarthat egy ideig.</span><span class="sxs-lookup"><span data-stu-id="3aa82-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="3aa82-257">Az előfeltételekkel rendelkező leképezés futtatásához engedélyezze a **Kapcsolódó entitásleképezések megjelenítése** kapcsolót.</span><span class="sxs-lookup"><span data-stu-id="3aa82-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="3aa82-258">Ha a táblázat azt jelzi, hogy az **Előfeltétel kezdeti szinkronizálása** értéke **Nem**, ellenőrizze, hogy a **Kezdeti szinkronizálás** jelző **Ki** állapotban van-e minden előfeltétel leképezés előtt, mielőtt futtatá azokat.</span><span class="sxs-lookup"><span data-stu-id="3aa82-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Leképezés futtatása](./media/21RunMap.png)

6. <span data-ttu-id="3aa82-260">Ellenőrizze, hogy a projekthez kapcsolódó leképezések mindegyike futó állapotban van.</span><span class="sxs-lookup"><span data-stu-id="3aa82-260">Validate all project related maps are in the running state.</span></span>

![Minden leképezés fut](./media/22AllMapsRunning.png)

<span data-ttu-id="3aa82-262">A Project Operations-környezet most már ki van alakítva, és konfigurálva van.</span><span class="sxs-lookup"><span data-stu-id="3aa82-262">Your Project Operations environment is now provisioned and configured.</span></span>
