---
title: Új környezet kiépítése
description: Ez a témakör az új Project Operations-környezet kialakításának módjával kapcsolatban tartalmaz tájékoztatást.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 09af2a7693c45d1d0b9c75420d018cc50d2cc0fa
ms.sourcegitcommit: 04c446746aad97fc3f4c3d441983c586b918a3a6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/11/2020
ms.locfileid: "4727793"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="8a4d4-103">Új környezet kiépítése</span><span class="sxs-lookup"><span data-stu-id="8a4d4-103">Provision a new environment</span></span>

<span data-ttu-id="8a4d4-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="8a4d4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8a4d4-105">Ez a témakör arról tartalmaz tájékoztatást, hogyan építhet ki új Dynamics 365 Project Operations-környezetet erőforrás-/nem készletalapú forgatókönyvekhez.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="8a4d4-106">Az automatizált Project Operations-kiépítés engedélyezése egy LCS-projektben</span><span class="sxs-lookup"><span data-stu-id="8a4d4-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="8a4d4-107">A következő lépésekkel engedélyezheti az automatizált Project Operations-kiépítést az LCS-projektjéhez.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="8a4d4-108">Lépjen az [LCS](https://lcs.dynamics.com/v2) lehetőségre, és válassza az **Előnézeti funkció kezelése** csempét.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="8a4d4-109">Az **Előzetes funkció** listában jelölje ki a **Project Operations funkció** lehetőséget, majd válassza az **Előzetes funkció engedélyezve** lehetőséget a Project Operations engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="8a4d4-110">Ez a lépés csak egy alkalommal hajtható végre LCS-projektenként.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="8a4d4-111">Project Operations-környezet kiépítése</span><span class="sxs-lookup"><span data-stu-id="8a4d4-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="8a4d4-112">Nyisson meg egy új Dynamics 365 Finance [bemutató környezet](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) vagy [teszt-/éles környezet](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) telepítést.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="8a4d4-113">Haladjon végig a **Környezet kiépítése** varázslón.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="8a4d4-114">Ügyeljen arra, hogy a kijelölt alkalmazás verziója 10.0.13 vagy magasabb legyen.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="8a4d4-115">A Project Operations kiépítéséhez az **Speciális beállítások** területen válassza a **Common Data Service** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="8a4d4-116">Engedélyezze a **Common Data Service beállítást** az **Igen** kiválasztásával, majd adja meg az adatokat a kötelező mezőkben:</span><span class="sxs-lookup"><span data-stu-id="8a4d4-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="8a4d4-117">Adatfolyam neve</span><span class="sxs-lookup"><span data-stu-id="8a4d4-117">Name</span></span>
  - <span data-ttu-id="8a4d4-118">Régió</span><span class="sxs-lookup"><span data-stu-id="8a4d4-118">Region</span></span>
  - <span data-ttu-id="8a4d4-119">Nyelv</span><span class="sxs-lookup"><span data-stu-id="8a4d4-119">Language</span></span>
  - <span data-ttu-id="8a4d4-120">Pénznem</span><span class="sxs-lookup"><span data-stu-id="8a4d4-120">Currency</span></span>
 
5. <span data-ttu-id="8a4d4-121">A **Common Data Service-sablon** mezőben jelölje ki a **Project Operations** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="8a4d4-122">Válassza ki a telepítésének környezettípusát.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="8a4d4-123">Az előfizetésen alapuló próbaverzió 30 napig teszi lehetővé a CDS-környezet telepítését.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Telepítés beállításai](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="8a4d4-125">Válassza az **Elfogadom** lehetőséget a szolgáltatási feltételek elfogadásához, majd válassza a **Kész** lehetőséget a telepítési beállításokhoz való visszatéréshez.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Telepítési hozzájárulás](./media/2DeploymentConsent.png)

7. <span data-ttu-id="8a4d4-127">Választható – Bemutató adatok alkalmazása a környezetre.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="8a4d4-128">Menjen a **Speciális beállítások** lehetőségre, válassza az **SQL Database konfiguráció testreszabása** lehetőséget, és állítsa be az **Alkalmazásadatbázis adathalmazának megadása** lehetőséget **Bemutató** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="8a4d4-129">Töltse ki a többi kötelező mezőt a varázslóban, és erősítse meg a telepítést.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="8a4d4-130">A környezet kiépítési ideje a környezet típusától függően eltér.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="8a4d4-131">A kiépítés akár hat óráig is eltarthat.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="8a4d4-132">A telepítés sikeres végrehajtása után a környezet **Telepített** állapottal jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="8a4d4-133">A környezet sikeres telepítésének megerősítéséhez válassza a **Bejelentkezés** lehetőséget, majd a megerősítéshez jelentkezzen be a környezetbe.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![A  környezetek részletei](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="8a4d4-135">A Finance-környezet frissítéseinek alkalmazása.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="8a4d4-136">A Project Operations egy Finance-környezetet igényel **10.0.13 (10.0.569.20009)** vagy újabb verziószámú alkalmazással.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="8a4d4-137">Előfordulhat, hogy a Finance-környezetre minőségi frissítéseket kell alkalmaznia ahhoz, hogy ezt a verziót kapja.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="8a4d4-138">A LCS **Környezet részletei** oldalán a **Rendelkezésre álló frissítések** területen válassza a **Frissítések megtekintése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Frissítések megtekintése](./media/5ViewUpdates.png)

2. <span data-ttu-id="8a4d4-140">A **Bináris frissítések** oldalon válassza a **Csomag mentése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-140">On the **Binary updates** page, select **Save package.**</span></span>

![Csomag mentése](./media/6SavePackage.png)

3. <span data-ttu-id="8a4d4-142">Kattintson az **Összes kiválasztása** elemre, majd válassza a **Csomag mentése** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-142">Click **Select all** and then select **Save package**.</span></span>

![Frissítések áttekintése és mentése](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="8a4d4-144">Adja meg a csomag nevét és leírását, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="8a4d4-145">Az internetkapcsolattól függően ez a folyamat eltarthat egy ideig.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-145">Depending on the internet connection, this process might take some time.</span></span>

![Csomag feltöltése az Eszközök könyvtárba](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="8a4d4-147">A csomag mentése után válassza a **Kész** lehetőséget, és mentse a csomagot az LCS-projekt Eszközök könyvtárába.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="8a4d4-148">A csomag mentése és ellenőrzése ~15 percet is igénybe vehet.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="8a4d4-149">A frissítés alkalmazásához keresse meg a **Környezet részletei** oldalt az LCS-ben, és válassza a **Karbantartás** > **Frissítések alkalmazása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Környezetek karbantartása](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="8a4d4-151">A frissítések listájában jelölje ki a létrehozott csomagot, majd válassza az **Alkalmaz** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Frissítések alkalmazása](./media/10ApplyUpdates.png)

<span data-ttu-id="8a4d4-153">A környezet javítása eltarthat egy ideig.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-153">Environment servicing will take some time.</span></span> <span data-ttu-id="8a4d4-154">Miután befejeződött, a környezet visszatér egy telepített állapotba.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-154">After it is complete, the environment will return to a deployed state.</span></span>

![Környezet telepítve](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="8a4d4-156">Kettős írási kapcsolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="8a4d4-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="8a4d4-157">A LCS-projektben nyissa meg a **Környezet részletei** oldalt.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="8a4d4-158">A **Common Data Service-környezet információi** területen válassza az **A CDS for Apps hivatkozása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="8a4d4-159">A hivatkozás létrejöttét követően válassza ismét az **A CDS for Apps hivatkozása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="8a4d4-160">A rendszer átirányítja a kettős írásra a Finance-ben.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-160">You will be redirected to Dual Write in Finance.</span></span>

![A CDS for Apps hivatkozása](./media/12LinktoCDS.png)

4. <span data-ttu-id="8a4d4-162">Válassza **Megoldás alkalmazása** lehetőséget az integrációba leképezni kívánt entitások eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Megoldások alkalmazása](./media/13ApplySolutions.png)

5. <span data-ttu-id="8a4d4-164">Válassza a mindkét megoldást: **Dynamics 365 Finance and Operations kettős írású entitásleképezés** és **Dynamics 365 Project Operations kettős írású entitásleképezése**, majd válassza az **Alkalmaz** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Megoldások megerősítése](./media/14ConfirmSolutions.png)

<span data-ttu-id="8a4d4-166">A megoldások alkalmazása után a kettős írási entitások alkalmazásra kerülnek a környezetre.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Megoldások alkalmazása](./media/15ApplyingSolutions.png)

<span data-ttu-id="8a4d4-168">Az entitások alkalmazása után az összes elérhető leképezés megjelenik a környezetben.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Kettős írású leképezések](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="8a4d4-170">Az adatentitások frissítése a frissítés után</span><span class="sxs-lookup"><span data-stu-id="8a4d4-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="8a4d4-171">A Finance-ben nyissa meg az **Adatkezelés** munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-171">In Finance, go to the **Data management** workspace.</span></span>

![Adatkezelési munkaterület](./media/16DataManagement.png)

2. <span data-ttu-id="8a4d4-173">Válassza ki a **Keretrendszer paraméterei** csempét.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-173">Select the **Framework parameters** tile.</span></span>

![Keretrendszer paraméterei](./media/17FrameworkParameters.png)

3. <span data-ttu-id="8a4d4-175">Az **Entitás beállításai** oldalon válassza az **Entitások listájának frissítése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Entitáslista frissítése](./media/18RefreshEntityList.png)

<span data-ttu-id="8a4d4-177">A frissítés megközelítőleg 20 percet vesz igénybe.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="8a4d4-178">A rendszer értesítést küld, amikor elkészült.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-178">You will receive an alert when it is complete.</span></span>

![Frissítés megerősítése](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="8a4d4-180">A Dataverse Project Operations biztonsági beállításainak frissítése</span><span class="sxs-lookup"><span data-stu-id="8a4d4-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="8a4d4-181">Menjen a Project Operations lehetőségre a Dataverse-környezetben.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="8a4d4-182">Válassza a **Beállítások** > **Biztonság** > **Biztonsági szerepkörök** elemet.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="8a4d4-183">A **Biztonsági szerepkörök** oldalon, a szerepkörök listájából válassza ki a **kettős írású alkalmazásfelhasználót**, majd válassza az **Egyéni entitások** fület.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="8a4d4-184">Ellenőrizze, hogy rendelkezik-e a szerepkörhöz **Olvasás** és **Hozzáfűzés** jogosultságokkal a következőhöz:</span><span class="sxs-lookup"><span data-stu-id="8a4d4-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="8a4d4-185">**Pénznem árfolyamának típusa**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="8a4d4-186">**Partnerek diagramja**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="8a4d4-187">**Pénzügyi naptár**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="8a4d4-188">**Főkönyv**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-188">**Ledger**</span></span>

5. <span data-ttu-id="8a4d4-189">A biztonsági szerepkör frissítése után válassza a **Beállítások** > **Biztonság** > **Csoportok** lehetőséget, és válassza ki az alapértelmezett csoportot a **Helyi vállalattulajdonos** csoportnézetben.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="8a4d4-190">Válassza a **Szerepkörök kezelése** lehetőséget, és ellenőrizze, hogy az alkalmazás **kettős írású alkalmazásfelhasználó** biztonsági jogosultsága érvényes-e erre a csoportra.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="8a4d4-191">Project Operations kettős írás leképezéseinek futtatása</span><span class="sxs-lookup"><span data-stu-id="8a4d4-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="8a4d4-192">A LCS-projektben nyissa meg a **Környezet részletei** oldalt.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="8a4d4-193">A **Common Data Service-környezet információi** területen válassza az **A CDS for Apps hivatkozása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="8a4d4-194">Miután kijelölte a hivatkozást, a rendszer átirányítja a leképezésekben szereplő entitások listájára.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="8a4d4-195">Indítsa el a leképezéseket következő táblázatban leírtak szerint.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="8a4d4-196">Ügyeljen arra, hogy a listában szereplő sorrendet kövesse.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="8a4d4-197">**Entitásleképezés**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-197">**Entity Map**</span></span> | <span data-ttu-id="8a4d4-198">**Entitás frissítése**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-198">**Refresh entity**</span></span> | <span data-ttu-id="8a4d4-199">**Kezdeti szinkronizálás**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-199">**Initial sync**</span></span> | <span data-ttu-id="8a4d4-200">**Kezdeti szinkronizálás fő eleme**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-200">**Master for initial sync**</span></span> | <span data-ttu-id="8a4d4-201">**Előfeltételek futtatása**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-201">**Run prerequisites**</span></span> | <span data-ttu-id="8a4d4-202">**Előfeltételek kezdeti szinkronizálása**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="8a4d4-203">**Az összes vállalat projekterőforrás-szerepkörei (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="8a4d4-204">No</span><span class="sxs-lookup"><span data-stu-id="8a4d4-204">No</span></span> | <span data-ttu-id="8a4d4-205">Igen</span><span class="sxs-lookup"><span data-stu-id="8a4d4-205">Yes</span></span> | <span data-ttu-id="8a4d4-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="8a4d4-206">Common Data Service</span></span> | <span data-ttu-id="8a4d4-207">No</span><span class="sxs-lookup"><span data-stu-id="8a4d4-207">No</span></span> | <span data-ttu-id="8a4d4-208">N. a.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-208">N\A</span></span> |
| <span data-ttu-id="8a4d4-209">**Jogi entitások (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="8a4d4-210">No</span><span class="sxs-lookup"><span data-stu-id="8a4d4-210">No</span></span> | <span data-ttu-id="8a4d4-211">Igen</span><span class="sxs-lookup"><span data-stu-id="8a4d4-211">Yes</span></span> | <span data-ttu-id="8a4d4-212">Finance and Operations alkalmazások</span><span class="sxs-lookup"><span data-stu-id="8a4d4-212">Finance and Operations apps</span></span> | <span data-ttu-id="8a4d4-213">No</span><span class="sxs-lookup"><span data-stu-id="8a4d4-213">No</span></span> | <span data-ttu-id="8a4d4-214">N. a.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-214">N\A</span></span> |
| <span data-ttu-id="8a4d4-215">**Főkönyv (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="8a4d4-216">No</span><span class="sxs-lookup"><span data-stu-id="8a4d4-216">No</span></span> | <span data-ttu-id="8a4d4-217">Igen</span><span class="sxs-lookup"><span data-stu-id="8a4d4-217">Yes</span></span> | <span data-ttu-id="8a4d4-218">Finance and Operations alkalmazások</span><span class="sxs-lookup"><span data-stu-id="8a4d4-218">Finance and Operations apps</span></span> | <span data-ttu-id="8a4d4-219">Igen</span><span class="sxs-lookup"><span data-stu-id="8a4d4-219">Yes</span></span> | <span data-ttu-id="8a4d4-220">Igen, Finance and Operations alkalmazások</span><span class="sxs-lookup"><span data-stu-id="8a4d4-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="8a4d4-221">**Projekttevékenységek integrációjának tényleges adatai (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="8a4d4-222">No</span><span class="sxs-lookup"><span data-stu-id="8a4d4-222">No</span></span> | <span data-ttu-id="8a4d4-223">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-223">No</span></span> | <span data-ttu-id="8a4d4-224">N. a.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-224">N\A</span></span> | <span data-ttu-id="8a4d4-225">Igen</span><span class="sxs-lookup"><span data-stu-id="8a4d4-225">Yes</span></span> | <span data-ttu-id="8a4d4-226">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-226">No</span></span> |
| <span data-ttu-id="8a4d4-227">**Projektszerződéssorok (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="8a4d4-228">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-228">No</span></span> | <span data-ttu-id="8a4d4-229">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-229">No</span></span> | <span data-ttu-id="8a4d4-230">N. a.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-230">N\A</span></span> | <span data-ttu-id="8a4d4-231">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-231">No</span></span> | <span data-ttu-id="8a4d4-232">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-232">No</span></span> |
| <span data-ttu-id="8a4d4-233">**A projekt tranzakciókapcsolatainak integrációs entitása (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="8a4d4-234">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-234">No</span></span> | <span data-ttu-id="8a4d4-235">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-235">No</span></span> | <span data-ttu-id="8a4d4-236">N. a.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-236">N\A</span></span> | <span data-ttu-id="8a4d4-237">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-237">No</span></span> | <span data-ttu-id="8a4d4-238">N. a.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-238">N\A</span></span> |
| <span data-ttu-id="8a4d4-239">**A Project Operations integráció szerződéssor-mérföldkövei (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="8a4d4-240">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-240">No</span></span> | <span data-ttu-id="8a4d4-241">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-241">No</span></span> | <span data-ttu-id="8a4d4-242">N. a.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-242">N\A</span></span> | <span data-ttu-id="8a4d4-243">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-243">No</span></span> | <span data-ttu-id="8a4d4-244">N. a.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-244">N\A</span></span> |
| <span data-ttu-id="8a4d4-245">**A Project Operations integrációs entitása kiadások becsléséhez (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="8a4d4-246">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-246">No</span></span> | <span data-ttu-id="8a4d4-247">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-247">No</span></span> | <span data-ttu-id="8a4d4-248">N. a.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-248">N\A</span></span> | <span data-ttu-id="8a4d4-249">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-249">No</span></span> | <span data-ttu-id="8a4d4-250">N. a.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-250">N\A</span></span> |
| <span data-ttu-id="8a4d4-251">**Project Operations integráció projektköltség-kategóriák exportálási entitása (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="8a4d4-252">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-252">No</span></span> | <span data-ttu-id="8a4d4-253">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-253">No</span></span> | <span data-ttu-id="8a4d4-254">N. a.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-254">N\A</span></span> | <span data-ttu-id="8a4d4-255">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-255">No</span></span> | <span data-ttu-id="8a4d4-256">N. a.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-256">N\A</span></span> |
| <span data-ttu-id="8a4d4-257">**Project Operations integráció projektkiadások exportálási entitása (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="8a4d4-258">Igen</span><span class="sxs-lookup"><span data-stu-id="8a4d4-258">Yes</span></span> | <span data-ttu-id="8a4d4-259">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-259">No</span></span> | <span data-ttu-id="8a4d4-260">N. a.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-260">N\A</span></span> | <span data-ttu-id="8a4d4-261">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-261">No</span></span> | <span data-ttu-id="8a4d4-262">N. a.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-262">N\A</span></span> |
| <span data-ttu-id="8a4d4-263">**A Project Operations integrációs entitása órabecslésekhez (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="8a4d4-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="8a4d4-264">Igen</span><span class="sxs-lookup"><span data-stu-id="8a4d4-264">Yes</span></span> | <span data-ttu-id="8a4d4-265">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-265">No</span></span> | <span data-ttu-id="8a4d4-266">N. a.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-266">N\A</span></span> | <span data-ttu-id="8a4d4-267">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4d4-267">No</span></span> | <span data-ttu-id="8a4d4-268">N. a.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-268">N\A</span></span> |


4. <span data-ttu-id="8a4d4-269">Az entitás frissítéséhez jelölje ki a leképezés nevét, majd válassza az **Entitások frissítése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Leképezés frissítése](./media/20RefreshMapping.png)

5. <span data-ttu-id="8a4d4-271">A frissítés befejeződése után futtassa a leképezést.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="8a4d4-272">A következő leképezés engedélyezése előtt ellenőrizze, hogy a táblázatban a leképezés **Fut** állapotban van-e.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="8a4d4-273">A nagy számú előfeltétellel rendelkező leképezések futtatása eltarthat egy ideig.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="8a4d4-274">Az előfeltételekkel rendelkező leképezés futtatásához engedélyezze a **Kapcsolódó entitásleképezések megjelenítése** kapcsolót.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="8a4d4-275">Ha a táblázat azt jelzi, hogy az **Előfeltétel kezdeti szinkronizálása** értéke **Nem**, ellenőrizze, hogy a **Kezdeti szinkronizálás** jelző **Ki** állapotban van-e minden előfeltétel leképezés előtt, mielőtt futtatá azokat.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Leképezés futtatása](./media/21RunMap.png)

6. <span data-ttu-id="8a4d4-277">Ellenőrizze, hogy a projekthez kapcsolódó leképezések mindegyike futó állapotban van.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-277">Validate all project related maps are in the running state.</span></span>

![Minden leképezés fut](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="8a4d4-279">Konfigurációs adatok alkalmazása a Project Operations szolgáltatáshoz használható CDS rendszerben (nem kötelező)</span><span class="sxs-lookup"><span data-stu-id="8a4d4-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="8a4d4-280">Ha alkalmazott bemutató adatokat a Finance környezetre, tekintse meg a [Konfigurációs adatok beállítása és alkalmazása a Common Data Service szolgáltatásban a Project Operationshoz](resource-apply-pro-setup-config-data.md) cikket a bemutató adatok CDS-környezetre való alkalmazásához.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="8a4d4-281">A Project Operations-környezet most már ki van alakítva, és konfigurálva van.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-281">Your Project Operations environment is now provisioned and configured.</span></span> 
