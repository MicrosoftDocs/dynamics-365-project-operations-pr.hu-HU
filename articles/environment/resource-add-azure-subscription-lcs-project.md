---
title: Azure-előfizetés hozzáadása LCS-projekthez
description: Ez a témakör az Azure-előfizetésnek egy LCS-projekttel való összekapcsolásával kapcsolatban tartalmaz tájékoztatást.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948911"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a><span data-ttu-id="004b1-103">Azure-előfizetés hozzáadása LCS-projekthez</span><span class="sxs-lookup"><span data-stu-id="004b1-103">Add an Azure subscription to LCS project</span></span>

<span data-ttu-id="004b1-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="004b1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="004b1-105">A felhőalapú környezeteket meglévő Azure-előfizetések segítségével kell telepíteni.</span><span class="sxs-lookup"><span data-stu-id="004b1-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="004b1-106">Ez a témakör bemutatja a meglévő Azure-előfizetésének egy LCS-projekttel való összekapcsolását.</span><span class="sxs-lookup"><span data-stu-id="004b1-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="004b1-107">Rendszergazdai jóváhagyás megadása</span><span class="sxs-lookup"><span data-stu-id="004b1-107">Grant admin consent</span></span>

1. <span data-ttu-id="004b1-108">Az LCS-projektjében, a **Környezetek** részen válassza a **Microsoft Azure beállításai** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="004b1-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Microsoft Azure beállításai](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="004b1-110">A **Projekt beállításai** oldalon, az **Azure-összekötők** lapon válassza az **Engedélyezés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="004b1-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="004b1-111">Ez lehetővé teszi a környezetek telepítését ehhez a projekthez.</span><span class="sxs-lookup"><span data-stu-id="004b1-111">This allows environments to be deployed to this project.</span></span>

![Azure-összekötők](./media/2AzureConnectors.png)

3. <span data-ttu-id="004b1-113">A rendszergazdai hozzájárulás biztosítása érdekében ismét válassza az **Engedélyezés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="004b1-113">Select **Authorize** again to provide admin consent.</span></span>

![Rendszergazdai jóváhagyás megadása](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="004b1-115">Fogadja el az engedélykérést.</span><span class="sxs-lookup"><span data-stu-id="004b1-115">Accept the permissions request.</span></span>

![Engedélykérés elfogadása](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="004b1-117">Az engedélyezés most már kész.</span><span class="sxs-lookup"><span data-stu-id="004b1-117">The authorization is now complete.</span></span> 

![Sikeres engedélyezés](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="004b1-119">Hozzáférés biztosítása a Dynamics Deployment Services számára az Azure-előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="004b1-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="004b1-120">Ugorjon a [Microsoft Azure-számlázás](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) lehetőségre, és válassza ki az előfizetését.</span><span class="sxs-lookup"><span data-stu-id="004b1-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="004b1-121">A Dynamics Deployment Services hozzáférést igényel ehhez az előfizetéshez, hogy képes legyen környezeteket telepíteni.</span><span class="sxs-lookup"><span data-stu-id="004b1-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Azure előfizetési adatok](./media/6AzureSubscription.png)

2. <span data-ttu-id="004b1-123">Válassza a navigációs ablak **Hozzáférés-vezérlés (IAM)** elemét, majd válassza a **Szerepkör-hozzárendelés hozzáadása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="004b1-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="004b1-124">A jobb oldalon lévő csúszka kiválasztásával jelölje ki a **Közreműködő szerepkör** elemet, és a megjelenő listájában keresse meg és jelölje ki a **Dynamics Deployment Services** szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="004b1-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="004b1-125">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="004b1-125">Select **Save**.</span></span>

![Hozzáférés az előfizetéshez](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="004b1-127">Előfizetés-összekötő hozzáadása egy LCS-projekthez</span><span class="sxs-lookup"><span data-stu-id="004b1-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="004b1-128">Az LCS-projektjében a **Microsoft Azure beállításai** oldalon válassza a **Hozzáadás** lehetőséget új összekötő hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="004b1-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="004b1-129">Adja meg az Azure-előfizetés azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="004b1-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="004b1-130">Az Azure-előfizetésének azonosítóját az [Azure Portal](https://ms.portal.azure.com/) webhelyen, a képernyő bal alsó részén található **Beállítások** alatt találja.</span><span class="sxs-lookup"><span data-stu-id="004b1-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="004b1-131">Az **Azure Resource Manager használatának konfigurálása** mezőben válassza az **Igen** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="004b1-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="004b1-132">Ügyeljen arra, hogy az Azure-előfizetésének AAD bérlői tartománya megfeleljen a tartományt birtokló Azure-előfizetésnek, amelyet használ, és válassza a **Következő** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="004b1-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="004b1-133">A **Microsoft Azure beállítása** képernyőn válassza a **Tovább** lehetőséget a megerősítéshez.</span><span class="sxs-lookup"><span data-stu-id="004b1-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="004b1-134">Ha a képernyőn hibaüzenet jelenik meg, akkor térjen vissza a témakör [Hozzáférés biztosítása a Dynamics Deployment Services számára az Azure-előfizetéshez](#provide) szakaszához, és ellenőrizze, hogy az összes lépést végrehajtotta-e.</span><span class="sxs-lookup"><span data-stu-id="004b1-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="004b1-135">Töltse le az Azure felügyeleti tanúsítványt a számítógép egy helyi mappájába, majd töltse fel az Azure felügyeleti portálra a **Beállítások** > **Felügyeleti tanúsítványok** lehetőségről.</span><span class="sxs-lookup"><span data-stu-id="004b1-135">Download the Azure Management Certificate to a local folder on your computer, and then upload it to Azure Management Portal by going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="004b1-136">Ez a tanúsítvány lehetővé teszi, hogy az LCS az Ön nevében kommunikáljon az Azure-ral.</span><span class="sxs-lookup"><span data-stu-id="004b1-136">This certificate will enable LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="004b1-137">Ezt a lépést kihagyhatja, ha a felhasználó hozzáféréssel rendelkezik az előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="004b1-137">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="004b1-138">Válassza a **Következő** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="004b1-138">Select  **Next**.</span></span>
8. <span data-ttu-id="004b1-139">Válassza ki a telepítendő Azure-régiót, és jelöljön ki egy olyan adatközpontot, amely közel van ahhoz a helyhez, ahol a rendszert használni kívánja.</span><span class="sxs-lookup"><span data-stu-id="004b1-139">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="004b1-140">Válassza a **Kapcsolódás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="004b1-140">Select  **Connect**.</span></span>

<span data-ttu-id="004b1-141">Sikeresen kapcsolódott az Azure-előfizetéséhez.</span><span class="sxs-lookup"><span data-stu-id="004b1-141">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="004b1-142">Most már telepítheti a Dynamics 365 Finance felhőalapú környezeteit.</span><span class="sxs-lookup"><span data-stu-id="004b1-142">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>


