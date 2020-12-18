---
title: Új környezet kiépítése
description: Ez a témakör az új Project Operations-környezet kialakításának módjával kapcsolatban tartalmaz tájékoztatást.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ed502a1312b702e029d8910d62f72b8e0e4df06
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642977"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="94c59-103">Új környezet kiépítése</span><span class="sxs-lookup"><span data-stu-id="94c59-103">Provision a new environment</span></span>

<span data-ttu-id="94c59-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="94c59-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="94c59-105">Ez a témakör arról tartalmaz tájékoztatást, hogyan építhet ki új Dynamics 365 Project Operations-környezetet erőforrás-/nem készletalapú forgatókönyvekhez.</span><span class="sxs-lookup"><span data-stu-id="94c59-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="94c59-106">Az automatizált Project Operations-kiépítés engedélyezése egy LCS-projektben</span><span class="sxs-lookup"><span data-stu-id="94c59-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="94c59-107">A következő lépésekkel engedélyezheti az automatizált Project Operations-kiépítést az LCS-projektjéhez.</span><span class="sxs-lookup"><span data-stu-id="94c59-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="94c59-108">Lépjen az [LCS](https://lcs.dynamics.com/v2) lehetőségre, és válassza az **Előnézeti funkció kezelése** csempét.</span><span class="sxs-lookup"><span data-stu-id="94c59-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="94c59-109">Az **Előzetes funkció** listában jelölje ki a **Project Operations funkció** lehetőséget, majd válassza az **Előzetes funkció engedélyezve** lehetőséget a Project Operations engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="94c59-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="94c59-110">Ez a lépés csak egy alkalommal hajtható végre LCS-projektenként.</span><span class="sxs-lookup"><span data-stu-id="94c59-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="94c59-111">Project Operations-környezet kiépítése</span><span class="sxs-lookup"><span data-stu-id="94c59-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="94c59-112">Nyisson meg egy új Dynamics 365 Finance [bemutató környezet](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) vagy [teszt-/éles környezet](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) telepítést.</span><span class="sxs-lookup"><span data-stu-id="94c59-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="94c59-113">Haladjon végig a **Környezet kiépítése** varázslón.</span><span class="sxs-lookup"><span data-stu-id="94c59-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="94c59-114">Ügyeljen arra, hogy a kijelölt alkalmazás verziója 10.0.13 vagy magasabb legyen.</span><span class="sxs-lookup"><span data-stu-id="94c59-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="94c59-115">A Project Operations kiépítéséhez az **Speciális beállítások** területen válassza a **Common Data Service** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="94c59-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="94c59-116">Engedélyezze a **Common Data Service beállítást** az **Igen** kiválasztásával, majd adja meg az adatokat a kötelező mezőkben:</span><span class="sxs-lookup"><span data-stu-id="94c59-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="94c59-117">Adatfolyam neve</span><span class="sxs-lookup"><span data-stu-id="94c59-117">Name</span></span>
  - <span data-ttu-id="94c59-118">Régió</span><span class="sxs-lookup"><span data-stu-id="94c59-118">Region</span></span>
  - <span data-ttu-id="94c59-119">Nyelv</span><span class="sxs-lookup"><span data-stu-id="94c59-119">Language</span></span>
  - <span data-ttu-id="94c59-120">Pénznem</span><span class="sxs-lookup"><span data-stu-id="94c59-120">Currency</span></span>
 
5. <span data-ttu-id="94c59-121">A **Common Data Service-sablon** mezőben jelölje ki a **Project Operations** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="94c59-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="94c59-122">Válassza ki a telepítésének környezettípusát.</span><span class="sxs-lookup"><span data-stu-id="94c59-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="94c59-123">Az előfizetésen alapuló próbaverzió 30 napig teszi lehetővé a CDS-környezet telepítését.</span><span class="sxs-lookup"><span data-stu-id="94c59-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Telepítés beállításai](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="94c59-125">Válassza az **Elfogadom** lehetőséget a szolgáltatási feltételek elfogadásához, majd válassza a **Kész** lehetőséget a telepítési beállításokhoz való visszatéréshez.</span><span class="sxs-lookup"><span data-stu-id="94c59-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Telepítési hozzájárulás](./media/2DeploymentConsent.png)

7. <span data-ttu-id="94c59-127">Töltse ki a többi kötelező mezőt a varázslóban, és erősítse meg a telepítést.</span><span class="sxs-lookup"><span data-stu-id="94c59-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="94c59-128">A környezet kiépítési ideje a környezet típusától függően változik.</span><span class="sxs-lookup"><span data-stu-id="94c59-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="94c59-129">A kiépítés akár hat óráig is eltarthat.</span><span class="sxs-lookup"><span data-stu-id="94c59-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="94c59-130">A telepítés sikeres végrehajtása után a környezet **Telepített** állapottal jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="94c59-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="94c59-131">A környezet sikeres telepítésének ellenőrzéséhez válassza a **Bejelentkezés** lehetőséget, és jelentkezzen be a környezetbe a megerősítéshez.</span><span class="sxs-lookup"><span data-stu-id="94c59-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![A  környezetek részletei](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="94c59-133">Project Operations Finance bemutató adatainak alkalmazása (nem kötelező lépés)</span><span class="sxs-lookup"><span data-stu-id="94c59-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="94c59-134">A Project Operations Finance bemutató adatait a 10.0.13-as szervizkiadású felhőben szolgáltatott környezethez az [ebben a cikkben](resource-apply-finance-demo-data.md) leírtak szerint alkalmazhatja.</span><span class="sxs-lookup"><span data-stu-id="94c59-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="94c59-135">A Finance-környezet frissítéseinek alkalmazása.</span><span class="sxs-lookup"><span data-stu-id="94c59-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="94c59-136">A Project Operations egy Finance-környezetet igényel **10.0.13 (10.0.569.20009)** vagy újabb verziószámú alkalmazással.</span><span class="sxs-lookup"><span data-stu-id="94c59-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="94c59-137">Előfordulhat, hogy a Finance-környezetre minőségi frissítéseket kell alkalmaznia ahhoz, hogy ezt a verziót kapja.</span><span class="sxs-lookup"><span data-stu-id="94c59-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="94c59-138">A LCS **Környezet részletei** oldalán a **Rendelkezésre álló frissítések** területen válassza a **Frissítések megtekintése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="94c59-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Frissítések megtekintése](./media/5ViewUpdates.png)

2. <span data-ttu-id="94c59-140">A **Bináris frissítések** oldalon válassza a **Csomag mentése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="94c59-140">On the **Binary updates** page, select **Save package.**</span></span>

![Csomag mentése](./media/6SavePackage.png)

3. <span data-ttu-id="94c59-142">Kattintson az **Összes kiválasztása** elemre, majd válassza a **Csomag mentése** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="94c59-142">Click **Select all** and then select **Save package**.</span></span>

![Frissítések áttekintése és mentése](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="94c59-144">Adja meg a csomag nevét és leírását, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="94c59-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="94c59-145">Az internetkapcsolattól függően ez a folyamat eltarthat egy ideig.</span><span class="sxs-lookup"><span data-stu-id="94c59-145">Depending on the internet connection, this process might take some time.</span></span>

![Csomag feltöltése az Eszközök könyvtárba](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="94c59-147">A csomag mentése után válassza a **Kész** lehetőséget, és mentse a csomagot az LCS-projekt Eszközök könyvtárába.</span><span class="sxs-lookup"><span data-stu-id="94c59-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="94c59-148">A csomag mentése és ellenőrzése ~15 percet is igénybe vehet.</span><span class="sxs-lookup"><span data-stu-id="94c59-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="94c59-149">A frissítés alkalmazásához keresse meg a **Környezet részletei** oldalt az LCS-ben, és válassza a **Karbantartás** > **Frissítések alkalmazása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="94c59-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Környezetek karbantartása](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="94c59-151">A frissítések listájában jelölje ki a létrehozott csomagot, majd válassza az **Alkalmaz** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="94c59-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Frissítések alkalmazása](./media/10ApplyUpdates.png)

<span data-ttu-id="94c59-153">A környezet javítása eltarthat egy ideig.</span><span class="sxs-lookup"><span data-stu-id="94c59-153">Environment servicing will take some time.</span></span> <span data-ttu-id="94c59-154">Miután befejeződött, a környezet visszatér egy telepített állapotba.</span><span class="sxs-lookup"><span data-stu-id="94c59-154">After it is complete, the environment will return to a deployed state.</span></span>

![Környezet telepítve](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="94c59-156">Kettős írási kapcsolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="94c59-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="94c59-157">A LCS-projektben nyissa meg a **Környezet részletei** oldalt.</span><span class="sxs-lookup"><span data-stu-id="94c59-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="94c59-158">A **Common Data Service-környezet információi** területen válassza az **A CDS for Apps hivatkozása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="94c59-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="94c59-159">A hivatkozás létrejöttét követően válassza ismét az **A CDS for Apps hivatkozása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="94c59-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="94c59-160">A rendszer átirányítja a kettős írásra a Finance-ben.</span><span class="sxs-lookup"><span data-stu-id="94c59-160">You will be redirected to Dual Write in Finance.</span></span>

![A CDS for Apps hivatkozása](./media/12LinktoCDS.png)

4. <span data-ttu-id="94c59-162">Válassza **Megoldás alkalmazása** lehetőséget az integrációba leképezni kívánt entitások eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="94c59-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Megoldások alkalmazása](./media/13ApplySolutions.png)

5. <span data-ttu-id="94c59-164">Válassza a mindkét megoldást: **Dynamics 365 Finance and Operations kettős írású entitásleképezés** és **Dynamics 365 Project Operations kettős írású entitásleképezése**, majd válassza az **Alkalmaz** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="94c59-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Megoldások megerősítése](./media/14ConfirmSolutions.png)

<span data-ttu-id="94c59-166">A megoldások alkalmazása után a kettős írási entitások alkalmazásra kerülnek a környezetre.</span><span class="sxs-lookup"><span data-stu-id="94c59-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Megoldások alkalmazása](./media/15ApplyingSolutions.png)

<span data-ttu-id="94c59-168">Az entitások alkalmazása után az összes elérhető leképezés megjelenik a környezetben.</span><span class="sxs-lookup"><span data-stu-id="94c59-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Kettős írású leképezések](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="94c59-170">Az adatentitások frissítése a frissítés után</span><span class="sxs-lookup"><span data-stu-id="94c59-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="94c59-171">A Finance-ben nyissa meg az **Adatkezelés** munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="94c59-171">In Finance, go to the **Data management** workspace.</span></span>

![Adatkezelési munkaterület](./media/16DataManagement.png)

2. <span data-ttu-id="94c59-173">Válassza ki a **Keretrendszer paraméterei** csempét.</span><span class="sxs-lookup"><span data-stu-id="94c59-173">Select the **Framework parameters** tile.</span></span>

![Keretrendszer paraméterei](./media/17FrameworkParameters.png)

3. <span data-ttu-id="94c59-175">Az **Entitás beállításai** oldalon válassza az **Entitások listájának frissítése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="94c59-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Entitáslista frissítése](./media/18RefreshEntityList.png)

<span data-ttu-id="94c59-177">A frissítés megközelítőleg 20 percet vesz igénybe.</span><span class="sxs-lookup"><span data-stu-id="94c59-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="94c59-178">A rendszer értesítést küld, amikor elkészült.</span><span class="sxs-lookup"><span data-stu-id="94c59-178">You will receive an alert when it is complete.</span></span>

![Frissítés megerősítése](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="94c59-180">Project Operations kettős írás leképezéseinek futtatása</span><span class="sxs-lookup"><span data-stu-id="94c59-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="94c59-181">A LCS-projektben nyissa meg a **Környezet részletei** oldalt.</span><span class="sxs-lookup"><span data-stu-id="94c59-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="94c59-182">A **Common Data Service-környezet információi** területen válassza az **A CDS for Apps hivatkozása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="94c59-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="94c59-183">Miután kijelölte a hivatkozást, a rendszer átirányítja a leképezésekben szereplő entitások listájára.</span><span class="sxs-lookup"><span data-stu-id="94c59-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="94c59-184">Indítsa el a leképezéseket következő táblázatban leírtak szerint.</span><span class="sxs-lookup"><span data-stu-id="94c59-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="94c59-185">Ügyeljen arra, hogy a listában szereplő sorrendet kövesse.</span><span class="sxs-lookup"><span data-stu-id="94c59-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="94c59-186">**Entitásleképezés**</span><span class="sxs-lookup"><span data-stu-id="94c59-186">**Entity Map**</span></span> | <span data-ttu-id="94c59-187">**Entitás frissítése**</span><span class="sxs-lookup"><span data-stu-id="94c59-187">**Refresh entity**</span></span> | <span data-ttu-id="94c59-188">**Kezdeti szinkronizálás**</span><span class="sxs-lookup"><span data-stu-id="94c59-188">**Initial sync**</span></span> | <span data-ttu-id="94c59-189">**Kezdeti szinkronizálás fő eleme**</span><span class="sxs-lookup"><span data-stu-id="94c59-189">**Master for initial sync**</span></span> | <span data-ttu-id="94c59-190">**Előfeltételek futtatása**</span><span class="sxs-lookup"><span data-stu-id="94c59-190">**Run prerequisites**</span></span> | <span data-ttu-id="94c59-191">**Előfeltételek kezdeti szinkronizálása**</span><span class="sxs-lookup"><span data-stu-id="94c59-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="94c59-192">**Az összes vállalat projekterőforrás-szerepkörei (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="94c59-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="94c59-193">No</span><span class="sxs-lookup"><span data-stu-id="94c59-193">No</span></span> | <span data-ttu-id="94c59-194">Igen</span><span class="sxs-lookup"><span data-stu-id="94c59-194">Yes</span></span> | <span data-ttu-id="94c59-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="94c59-195">Common Data Service</span></span> | <span data-ttu-id="94c59-196">No</span><span class="sxs-lookup"><span data-stu-id="94c59-196">No</span></span> | <span data-ttu-id="94c59-197">N. a.</span><span class="sxs-lookup"><span data-stu-id="94c59-197">N\A</span></span> |
| <span data-ttu-id="94c59-198">**Jogi entitások (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="94c59-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="94c59-199">No</span><span class="sxs-lookup"><span data-stu-id="94c59-199">No</span></span> | <span data-ttu-id="94c59-200">Igen</span><span class="sxs-lookup"><span data-stu-id="94c59-200">Yes</span></span> | <span data-ttu-id="94c59-201">Finance and Operations alkalmazások</span><span class="sxs-lookup"><span data-stu-id="94c59-201">Finance and Operations apps</span></span> | <span data-ttu-id="94c59-202">No</span><span class="sxs-lookup"><span data-stu-id="94c59-202">No</span></span> | <span data-ttu-id="94c59-203">N. a.</span><span class="sxs-lookup"><span data-stu-id="94c59-203">N\A</span></span> |
| <span data-ttu-id="94c59-204">**Főkönyv (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="94c59-204">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="94c59-205">No</span><span class="sxs-lookup"><span data-stu-id="94c59-205">No</span></span> | <span data-ttu-id="94c59-206">Igen</span><span class="sxs-lookup"><span data-stu-id="94c59-206">Yes</span></span> | <span data-ttu-id="94c59-207">Finance and Operations alkalmazások</span><span class="sxs-lookup"><span data-stu-id="94c59-207">Finance and Operations apps</span></span> | <span data-ttu-id="94c59-208">Igen</span><span class="sxs-lookup"><span data-stu-id="94c59-208">Yes</span></span> | <span data-ttu-id="94c59-209">Igen, Finance and Operations alkalmazások</span><span class="sxs-lookup"><span data-stu-id="94c59-209">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="94c59-210">**Projekttevékenységek integrációjának tényleges adatai (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="94c59-210">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="94c59-211">No</span><span class="sxs-lookup"><span data-stu-id="94c59-211">No</span></span> | <span data-ttu-id="94c59-212">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-212">No</span></span> | <span data-ttu-id="94c59-213">N. a.</span><span class="sxs-lookup"><span data-stu-id="94c59-213">N\A</span></span> | <span data-ttu-id="94c59-214">Igen</span><span class="sxs-lookup"><span data-stu-id="94c59-214">Yes</span></span> | <span data-ttu-id="94c59-215">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-215">No</span></span> |
| <span data-ttu-id="94c59-216">**Projektszerződéssorok (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="94c59-216">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="94c59-217">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-217">No</span></span> | <span data-ttu-id="94c59-218">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-218">No</span></span> | <span data-ttu-id="94c59-219">N. a.</span><span class="sxs-lookup"><span data-stu-id="94c59-219">N\A</span></span> | <span data-ttu-id="94c59-220">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-220">No</span></span> | <span data-ttu-id="94c59-221">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-221">No</span></span> |
| <span data-ttu-id="94c59-222">**A projekt tranzakciókapcsolatainak integrációs entitása (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="94c59-222">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="94c59-223">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-223">No</span></span> | <span data-ttu-id="94c59-224">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-224">No</span></span> | <span data-ttu-id="94c59-225">N. a.</span><span class="sxs-lookup"><span data-stu-id="94c59-225">N\A</span></span> | <span data-ttu-id="94c59-226">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-226">No</span></span> | <span data-ttu-id="94c59-227">N. a.</span><span class="sxs-lookup"><span data-stu-id="94c59-227">N\A</span></span> |
| <span data-ttu-id="94c59-228">**A Project Operations integráció szerződéssor-mérföldkövei (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="94c59-228">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="94c59-229">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-229">No</span></span> | <span data-ttu-id="94c59-230">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-230">No</span></span> | <span data-ttu-id="94c59-231">N. a.</span><span class="sxs-lookup"><span data-stu-id="94c59-231">N\A</span></span> | <span data-ttu-id="94c59-232">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-232">No</span></span> | <span data-ttu-id="94c59-233">N. a.</span><span class="sxs-lookup"><span data-stu-id="94c59-233">N\A</span></span> |
| <span data-ttu-id="94c59-234">**A Project Operations integrációs entitása kiadások becsléséhez (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="94c59-234">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="94c59-235">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-235">No</span></span> | <span data-ttu-id="94c59-236">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-236">No</span></span> | <span data-ttu-id="94c59-237">N. a.</span><span class="sxs-lookup"><span data-stu-id="94c59-237">N\A</span></span> | <span data-ttu-id="94c59-238">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-238">No</span></span> | <span data-ttu-id="94c59-239">N. a.</span><span class="sxs-lookup"><span data-stu-id="94c59-239">N\A</span></span> |
| <span data-ttu-id="94c59-240">**Project Operations integráció projektköltség-kategóriák exportálási entitása (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="94c59-240">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="94c59-241">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-241">No</span></span> | <span data-ttu-id="94c59-242">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-242">No</span></span> | <span data-ttu-id="94c59-243">N. a.</span><span class="sxs-lookup"><span data-stu-id="94c59-243">N\A</span></span> | <span data-ttu-id="94c59-244">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-244">No</span></span> | <span data-ttu-id="94c59-245">N. a.</span><span class="sxs-lookup"><span data-stu-id="94c59-245">N\A</span></span> |
| <span data-ttu-id="94c59-246">**Project Operations integráció projektkiadások exportálási entitása (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="94c59-246">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="94c59-247">Igen</span><span class="sxs-lookup"><span data-stu-id="94c59-247">Yes</span></span> | <span data-ttu-id="94c59-248">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-248">No</span></span> | <span data-ttu-id="94c59-249">N. a.</span><span class="sxs-lookup"><span data-stu-id="94c59-249">N\A</span></span> | <span data-ttu-id="94c59-250">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-250">No</span></span> | <span data-ttu-id="94c59-251">N. a.</span><span class="sxs-lookup"><span data-stu-id="94c59-251">N\A</span></span> |
| <span data-ttu-id="94c59-252">**A Project Operations integrációs entitása órabecslésekhez (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="94c59-252">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="94c59-253">Igen</span><span class="sxs-lookup"><span data-stu-id="94c59-253">Yes</span></span> | <span data-ttu-id="94c59-254">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-254">No</span></span> | <span data-ttu-id="94c59-255">N. a.</span><span class="sxs-lookup"><span data-stu-id="94c59-255">N\A</span></span> | <span data-ttu-id="94c59-256">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c59-256">No</span></span> | <span data-ttu-id="94c59-257">N. a.</span><span class="sxs-lookup"><span data-stu-id="94c59-257">N\A</span></span> |


4. <span data-ttu-id="94c59-258">Az entitás frissítéséhez jelölje ki a leképezés nevét, majd válassza az **Entitások frissítése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="94c59-258">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Leképezés frissítése](./media/20RefreshMapping.png)

5. <span data-ttu-id="94c59-260">A frissítés befejeződése után futtassa a leképezést.</span><span class="sxs-lookup"><span data-stu-id="94c59-260">After the refresh is complete, run the map.</span></span> <span data-ttu-id="94c59-261">A következő leképezés engedélyezése előtt ellenőrizze, hogy a táblázatban a leképezés **Fut** állapotban van-e.</span><span class="sxs-lookup"><span data-stu-id="94c59-261">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="94c59-262">A nagy számú előfeltétellel rendelkező leképezések futtatása eltarthat egy ideig.</span><span class="sxs-lookup"><span data-stu-id="94c59-262">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="94c59-263">Az előfeltételekkel rendelkező leképezés futtatásához engedélyezze a **Kapcsolódó entitásleképezések megjelenítése** kapcsolót.</span><span class="sxs-lookup"><span data-stu-id="94c59-263">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="94c59-264">Ha a táblázat azt jelzi, hogy az **Előfeltétel kezdeti szinkronizálása** értéke **Nem**, ellenőrizze, hogy a **Kezdeti szinkronizálás** jelző **Ki** állapotban van-e minden előfeltétel leképezés előtt, mielőtt futtatá azokat.</span><span class="sxs-lookup"><span data-stu-id="94c59-264">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Leképezés futtatása](./media/21RunMap.png)

6. <span data-ttu-id="94c59-266">Ellenőrizze, hogy a projekthez kapcsolódó leképezések mindegyike futó állapotban van.</span><span class="sxs-lookup"><span data-stu-id="94c59-266">Validate all project related maps are in the running state.</span></span>

![Minden leképezés fut](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="94c59-268">Konfigurációs adatok alkalmazása a Project Operations szolgáltatáshoz használható CDS rendszerben (nem kötelező)</span><span class="sxs-lookup"><span data-stu-id="94c59-268">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="94c59-269">Ha alkalmazott bemutató adatokat a Finance környezetre, tekintse meg a [Konfigurációs adatok beállítása és alkalmazása a Common Data Service szolgáltatásban a Project Operationshoz](resource-apply-pro-setup-config-data.md) cikket a bemutató adatok CDS-környezetre való alkalmazásához.</span><span class="sxs-lookup"><span data-stu-id="94c59-269">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="94c59-270">A Project Operations-környezet most már ki van alakítva, és konfigurálva van.</span><span class="sxs-lookup"><span data-stu-id="94c59-270">Your Project Operations environment is now provisioned and configured.</span></span> 
