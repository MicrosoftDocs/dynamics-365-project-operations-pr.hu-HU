---
title: Azure-előfizetés hozzáadása LCS-projekthez
description: Ez a témakör az Azure-előfizetésnek egy LCS-projekttel való összekapcsolásával kapcsolatban tartalmaz tájékoztatást.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6daa86d453ec5022cdd75dff0394c8818292406c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000619"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="0073c-103">Azure-előfizetés hozzáadása LCS-projekthez</span><span class="sxs-lookup"><span data-stu-id="0073c-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="0073c-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="0073c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0073c-105">A felhőalapú környezeteket meglévő Azure-előfizetések segítségével kell telepíteni.</span><span class="sxs-lookup"><span data-stu-id="0073c-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="0073c-106">Ez a témakör bemutatja a meglévő Azure-előfizetésének egy LCS-projekttel való összekapcsolását.</span><span class="sxs-lookup"><span data-stu-id="0073c-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="0073c-107">Rendszergazdai jóváhagyás megadása</span><span class="sxs-lookup"><span data-stu-id="0073c-107">Grant admin consent</span></span>

1. <span data-ttu-id="0073c-108">Az LCS-projektjében, a **Környezetek** részen válassza a **Microsoft Azure beállításai** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="0073c-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Microsoft Azure beállításai](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="0073c-110">A **Projekt beállításai** oldalon, az **Azure-összekötők** lapon válassza az **Engedélyezés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="0073c-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="0073c-111">Ez lehetővé teszi a környezetek telepítését ehhez a projekthez.</span><span class="sxs-lookup"><span data-stu-id="0073c-111">This allows environments to be deployed to this project.</span></span>

![Azure-összekötők](./media/2AzureConnectors.png)

3. <span data-ttu-id="0073c-113">A rendszergazdai hozzájárulás biztosítása érdekében ismét válassza az **Engedélyezés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="0073c-113">Select **Authorize** again to provide admin consent.</span></span>

![Rendszergazdai jóváhagyás megadása](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="0073c-115">Fogadja el az engedélykérést.</span><span class="sxs-lookup"><span data-stu-id="0073c-115">Accept the permissions request.</span></span>

![Engedélykérés elfogadása](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="0073c-117">Az engedélyezés most már kész.</span><span class="sxs-lookup"><span data-stu-id="0073c-117">The authorization is now complete.</span></span> 

![Sikeres engedélyezés](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="0073c-119">Hozzáférés biztosítása a Dynamics Deployment Services számára az Azure-előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="0073c-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="0073c-120">Ugorjon a [Microsoft Azure-számlázás](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) lehetőségre, és válassza ki az előfizetését.</span><span class="sxs-lookup"><span data-stu-id="0073c-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="0073c-121">A Dynamics Deployment Services hozzáférést igényel ehhez az előfizetéshez, hogy képes legyen környezeteket telepíteni.</span><span class="sxs-lookup"><span data-stu-id="0073c-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Azure előfizetési adatok](./media/6AzureSubscription.png)

2. <span data-ttu-id="0073c-123">Válassza a navigációs ablak **Hozzáférés-vezérlés (IAM)** elemét, majd válassza a **Szerepkör-hozzárendelés hozzáadása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="0073c-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="0073c-124">A jobb oldalon lévő csúszka kiválasztásával jelölje ki a **Közreműködő szerepkör** elemet, és a megjelenő listájában keresse meg és jelölje ki a **Dynamics Deployment Services** szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="0073c-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="0073c-125">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="0073c-125">Select **Save**.</span></span>

![Hozzáférés az előfizetéshez](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="0073c-127">Előfizetés-összekötő hozzáadása egy LCS-projekthez</span><span class="sxs-lookup"><span data-stu-id="0073c-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="0073c-128">Az LCS-projektjében a **Microsoft Azure beállításai** oldalon válassza a **Hozzáadás** lehetőséget új összekötő hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="0073c-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="0073c-129">Adja meg az Azure-előfizetés azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="0073c-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="0073c-130">Az Azure-előfizetésének azonosítóját az [Azure Portal](https://ms.portal.azure.com/) webhelyen, a képernyő bal alsó részén található **Beállítások** alatt találja.</span><span class="sxs-lookup"><span data-stu-id="0073c-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="0073c-131">Az **Azure Resource Manager használatának konfigurálása** mezőben válassza az **Igen** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="0073c-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="0073c-132">Ügyeljen arra, hogy az Azure-előfizetésének AAD bérlői tartománya megfeleljen a tartományt birtokló Azure-előfizetésnek, amelyet használ, és válassza a **Következő** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="0073c-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="0073c-133">A **Microsoft Azure beállítása** képernyőn válassza a **Tovább** lehetőséget a megerősítéshez.</span><span class="sxs-lookup"><span data-stu-id="0073c-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="0073c-134">Ha a képernyőn hibaüzenet jelenik meg, akkor térjen vissza a témakör [Hozzáférés biztosítása a Dynamics Deployment Services számára az Azure-előfizetéshez](#provide) szakaszához, és ellenőrizze, hogy az összes lépést végrehajtotta-e.</span><span class="sxs-lookup"><span data-stu-id="0073c-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="0073c-135">Töltse le az Azure felügyeleti tanúsítványt a számítógép egy helyi mappájába.</span><span class="sxs-lookup"><span data-stu-id="0073c-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="0073c-136">Kérje meg az Azure előfizetés-rendszergazdát, hogy töltse fel a tanúsítványt az Azure felügyeleti portálra az előfizetés kiválasztásával és a **Beállítások** > **Felügyeleti tanúsítványok** pontra lépve.</span><span class="sxs-lookup"><span data-stu-id="0073c-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="0073c-137">Ez a tanúsítvány teszi lehetővé, hogy a LCS az Ön nevében kommunikáljon az Azure-ral.</span><span class="sxs-lookup"><span data-stu-id="0073c-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="0073c-138">Ezt a lépést kihagyhatja, ha a felhasználó hozzáféréssel rendelkezik az előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="0073c-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="0073c-139">Válassza a **Következő** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="0073c-139">Select  **Next**.</span></span>
8. <span data-ttu-id="0073c-140">Válassza ki a telepítendő Azure-régiót, és jelöljön ki egy olyan adatközpontot, amely közel van ahhoz a helyhez, ahol a rendszert használni kívánja.</span><span class="sxs-lookup"><span data-stu-id="0073c-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="0073c-141">Válassza a **Kapcsolódás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="0073c-141">Select  **Connect**.</span></span>

<span data-ttu-id="0073c-142">Sikeresen kapcsolódott az Azure-előfizetéséhez.</span><span class="sxs-lookup"><span data-stu-id="0073c-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="0073c-143">Most már telepítheti a Dynamics 365 Finance felhőalapú környezeteit.</span><span class="sxs-lookup"><span data-stu-id="0073c-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
