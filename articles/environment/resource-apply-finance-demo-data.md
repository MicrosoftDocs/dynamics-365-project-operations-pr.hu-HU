---
title: A Project Operations bemutató adatainak alkalmazása a Finance felhőben szolgáltatott környezetbe
description: Ez a témakör ismerteti, hogyan lehet alkalmazni a Project Operations bemutató adatait a Dynamics 365 Finance felhőben szolgáltatott környezetre.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1a94862d5a024eb1630f33c0c96699e8b4b49bf2
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948915"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="45e8f-103">A Project Operations bemutató adatainak alkalmazása a Finance felhőben szolgáltatott környezetbe</span><span class="sxs-lookup"><span data-stu-id="45e8f-103">Apply Project Operations demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="45e8f-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="45e8f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

><span data-ttu-id="45e8f-105">[Fontos] Ez a témakör csak a Microsoft Dynamics 365 Finance 10.0.13-as verziója esetében alkalmazható, és csak felhőben üzemeltetett környezeten hajtható végre.</span><span class="sxs-lookup"><span data-stu-id="45e8f-105">[Important] This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="45e8f-106">A minőségi frissítések környezetbe való alkalmazása **ELŐTT** hajtsa végre a témakör lépéseit.</span><span class="sxs-lookup"><span data-stu-id="45e8f-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="45e8f-107">Az LCS-projektben nyissa meg a **Környezet részletei** oldalt.</span><span class="sxs-lookup"><span data-stu-id="45e8f-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="45e8f-108">Figyelje meg, hogy tartalmazza a környezethez a távoli asztali protokoll (RDP) használatával való kapcsolódáshoz szükséges adatokat.</span><span class="sxs-lookup"><span data-stu-id="45e8f-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![A  környezetek részletei](./media/1EnvironmentDetails.png)

<span data-ttu-id="45e8f-110">A kiemelt hitelesítő adatok első csoportja a helyi fiók hitelesítő adatai, és a távoli asztali kapcsolatra mutató hivatkozást tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="45e8f-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="45e8f-111">A hitelesítő adatok tartalmazzák a környezet rendszergazdai felhasználónevét és jelszavát.</span><span class="sxs-lookup"><span data-stu-id="45e8f-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="45e8f-112">A hitelesítő adatok második csoportja az SQL Server alkalmazásba való belépésre szolgál ebben a környezetben.</span><span class="sxs-lookup"><span data-stu-id="45e8f-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="45e8f-113">Kapcsolódjon távolról a környezethez a **Helyi fiókok** hivatkozással, és használja a **Helyi fiók hitelesítő adatait** a hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="45e8f-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="45e8f-114">Nyissa meg az **Internet Information Services** > **Alkalmazáskészletek** > **AOSService** részt, és állítsa le a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="45e8f-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="45e8f-115">Ezen a ponton leállítja a szolgáltatást, hogy folytathassa az SQL adatbázis cseréjét.</span><span class="sxs-lookup"><span data-stu-id="45e8f-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![AOS leállítása](./media/2StopAOS.png)

4. <span data-ttu-id="45e8f-117">Nyissa meg a **Szolgáltatások** részt, és állítsa le a következő két elemet:</span><span class="sxs-lookup"><span data-stu-id="45e8f-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="45e8f-118">Microsoft Dynamics 365 Unified Operations : Kötegkezelő szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="45e8f-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="45e8f-119">Microsoft Dynamics 365 Unified Operations: Adatimportálási és -exportálási keretrendszer</span><span class="sxs-lookup"><span data-stu-id="45e8f-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Szolgáltatások leállítása](./media/3StopServices.png)

5. <span data-ttu-id="45e8f-121">Nyissa meg a Microsoft SQL Server Management Studio alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="45e8f-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="45e8f-122">Jelentkezzen be az SQL-szerver hitelesítő adataival, és használja az axdbadmin felhasználót és jelszót az LCS **Környezetek részletei** oldaláról.</span><span class="sxs-lookup"><span data-stu-id="45e8f-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="45e8f-124">Az objektumtallózó **Adatbázisok** részén keresse meg az **AXDB** elemet.</span><span class="sxs-lookup"><span data-stu-id="45e8f-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="45e8f-125">Az adatbázist egy új adatbázissal helyettesíti, amely a [letöltőközpontban](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip) található.</span><span class="sxs-lookup"><span data-stu-id="45e8f-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="45e8f-126">Másolja a zip-fájlt a virtuális gépre, és csomagolja ki a zip-tartalmat.</span><span class="sxs-lookup"><span data-stu-id="45e8f-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="45e8f-127">Az SQL Server Management Studio alkalmazásban kattintson a jobb gombbal az **AxDB** elemre, majd válassza a **Feladatok** > **Visszaállítás** > **Adatbázis** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="45e8f-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Adatbázis visszaállítása](./media/5RestoreDatabase.png)

9. <span data-ttu-id="45e8f-129">Válassza a **Forráseszköz** lehetőséget, és keresse meg a másolt zip-ből kibontott fájlt.</span><span class="sxs-lookup"><span data-stu-id="45e8f-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Forráseszközök](./media/6SourceDevice.png)

10. <span data-ttu-id="45e8f-131">Válassza a **Beállítások** lehetőséget, majd válassza a **Meglévő adatbázis felülírása** és a **Céladatbázissal meglévő kapcsolatok lezárása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="45e8f-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="45e8f-132">Kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="45e8f-132">Select **OK**.</span></span>

![Beállítások visszaállítása](./media/7RestoreSetting.png)

<span data-ttu-id="45e8f-134">A rendszer megerősíti, hogy az AXDB-visszaállítás sikeresen megtörtént.</span><span class="sxs-lookup"><span data-stu-id="45e8f-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="45e8f-135">A visszaigazolás kézhezvételét követően lezárhatja az SQL Services Management Studio alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="45e8f-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="45e8f-136">Lépjen vissza az **Internet Information Services** > **Alkalmazáskészletek** > **AOSService** részhez, és indítsa el az AOSService alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="45e8f-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="45e8f-137">Nyissa meg a **Szolgáltatások** részt, és indítsa el a korábban leállított két szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="45e8f-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="45e8f-138">Keresse meg az AdminUserProvisioning eszközt ezen a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="45e8f-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="45e8f-139">Keresse a K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe alatt.</span><span class="sxs-lookup"><span data-stu-id="45e8f-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="45e8f-140">Futtassa a .ext-fájlt a saját felhasználói címét használva az **E-mail-cím** mezőben.</span><span class="sxs-lookup"><span data-stu-id="45e8f-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="45e8f-141">Válassza a **Küldés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="45e8f-141">Select **Submit**.</span></span>

![Rendszergazdai felhasználó átadása](./media/8AdminUserProvisioning.png)

<span data-ttu-id="45e8f-143">Ez pár percet is igénybe vehet.</span><span class="sxs-lookup"><span data-stu-id="45e8f-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="45e8f-144">Kapnia egy megerősítő üzenetet, hogy a rendszergazdai felhasználó sikeresen frissítve lett.</span><span class="sxs-lookup"><span data-stu-id="45e8f-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="45e8f-145">Végül, futtassa a parancssort rendszergazdaként az iisreset végrehajtásához</span><span class="sxs-lookup"><span data-stu-id="45e8f-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![IIS alaphelyzetbe állítás](./media/9IISReset.png)

18. <span data-ttu-id="45e8f-147">Zárja be a távoli asztali munkamenetet, és az LCS **Környezet részletei** oldal használatával lépjen be a környezetbe, és ellenőrizze, hogy az a várt módon működik.</span><span class="sxs-lookup"><span data-stu-id="45e8f-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
