---
title: Regisztráció a Project Operations előzetes verziós előfizetésekre az erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a témakör információt nyújt arról, hogyan lehet regisztrálni és telepíteni a Dynamics 365 Project Operations alkalmazást erőforrás-/nem készletalapú forgatókönyvek esetén.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a03f021b1ae0a87dfc947976b8a16c8246e1684
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4077978"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="33352-103">Regisztráció a Project Operations előzetes verziós előfizetésekre az erőforrás-/nem készletalapú forgatókönyvek esetén</span><span class="sxs-lookup"><span data-stu-id="33352-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="33352-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="33352-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="33352-105">Ez a témakör ismerteti, hogyan lehet előfizetni az előzetes verzióra/partnerajánlatra, és telepíteni a Project Operations-környezetet erőforrás-/nem készletalapú forgatókönyvek esetén.</span><span class="sxs-lookup"><span data-stu-id="33352-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="33352-106">Előfeltételek</span><span class="sxs-lookup"><span data-stu-id="33352-106">Prerequisites</span></span>

- <span data-ttu-id="33352-107">Kapni fog egy e-mailt, amely meghívja, hogy részt vegyen az előzetes verzióban.</span><span class="sxs-lookup"><span data-stu-id="33352-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="33352-108">Előzetes verziót kérhet a [Project Operations webhelyén](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="33352-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="33352-109">Az előzetes verziót telepítő felhasználónak Azure-bérlői globális rendszergazdai jogosultsággal kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="33352-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="33352-110">A Finance-környezet telepítéséhez érvényes Azure-előfizetésre van szükség, amely környezetenként kerül számlázásra.</span><span class="sxs-lookup"><span data-stu-id="33352-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="33352-111">A kezdéshez használhatja a szervezet meglévő előfizetését, vagy egy [Azure-próbaverziót](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="33352-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="33352-112">A CDS-környezet korlátozott, 30 napos időszakra ingyenesen biztosítva lesz.</span><span class="sxs-lookup"><span data-stu-id="33352-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="33352-113">Feliratkozás</span><span class="sxs-lookup"><span data-stu-id="33352-113">Subscribe</span></span>

<span data-ttu-id="33352-114">Amikor megkapja az [előzetes verzióra vonatkozó kérelem](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) jóváhagyását, e-mailben három ajánlatot kap a Microsofttól.</span><span class="sxs-lookup"><span data-stu-id="33352-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive three offers from Microsoft by email.</span></span> <span data-ttu-id="33352-115">Ez lehetővé teszi, hogy telepítse a Project Operations előzetes verzióját:</span><span class="sxs-lookup"><span data-stu-id="33352-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="33352-116">Dynamics 365 Project Operations (CRM) – Előzetes próbaverzió</span><span class="sxs-lookup"><span data-stu-id="33352-116">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="33352-117">Office 365 Project Operations – Előzetes próbaverzió</span><span class="sxs-lookup"><span data-stu-id="33352-117">Office 365 Project Operations - Preview Trial</span></span>
- <span data-ttu-id="33352-118">Dynamics 365 Finance – előzetes próbaverzió</span><span class="sxs-lookup"><span data-stu-id="33352-118">Dynamics 365 Finance - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="33352-119">A szervezetnél csak egy személynek, a bérlői rendszergazdának kell elvégeznie ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="33352-119">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="33352-120">Ha nem Ön ennek a kiadásnak az előfizetője, várjon, amíg a szervezete regisztrálva lesz, és megkapta a felhasználói hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="33352-120">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="33352-121">Dynamics 365 Project Operations (CRM) – Előzetes próbaverzió</span><span class="sxs-lookup"><span data-stu-id="33352-121">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="33352-122">Mielőtt elkezdené, ügyeljen arra, hogy a felhasználó munkafiókjával jelentkezzen be a böngészőbe abban a bérlőben, ahol a Project Operations előzetes verzióját szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="33352-122">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="33352-123">Váltsa be az első **Dynamics 365 Project Operations (CRM) – előzetes próbaverzió** ajánlatkódját a böngésző URL-mezőjébe történő beillesztéssel.</span><span class="sxs-lookup"><span data-stu-id="33352-123">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Ajánlat beváltása](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="33352-125">Hagyja jóvá a megrendelést.</span><span class="sxs-lookup"><span data-stu-id="33352-125">Confirm your order.</span></span>

![Ellenőrizze a sorrendet](./media/17ConfirmOrderNew.png)

<span data-ttu-id="33352-127">A megerősítő ajánlatot sikeres beváltását láthatja.</span><span class="sxs-lookup"><span data-stu-id="33352-127">You will see confirmation offer was successfully redeemed.</span></span>

![Jóváhagyás](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="33352-129">Office 365 Project Operations – Előzetes próbaverzió</span><span class="sxs-lookup"><span data-stu-id="33352-129">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="33352-130">Ismételje meg ugyanazokat a lépéseket, mint az első ajánlatkóddal.</span><span class="sxs-lookup"><span data-stu-id="33352-130">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="33352-131">Ügyeljen arra, hogy a második ajánlatkódot ugyanazzal a felhasználói fiókkal adja hozzá, amelyet az első ajánlatkódhoz használt.</span><span class="sxs-lookup"><span data-stu-id="33352-131">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="33352-132">Dynamics 365 Finance előzetes próbaverzió</span><span class="sxs-lookup"><span data-stu-id="33352-132">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="33352-133">Ismételje meg ugyanezeket a lépéseket az üdvözlő e-mailben szereplő utolsó ajánlattal.</span><span class="sxs-lookup"><span data-stu-id="33352-133">Repeat the same steps with the last offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="33352-134">Licencek hozzárendelése</span><span class="sxs-lookup"><span data-stu-id="33352-134">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="33352-135">A következő lépések végrehajtásához rendszergazdai hozzáféréssel kell rendelkeznie a szervezete Microsoft 365-portáljához.</span><span class="sxs-lookup"><span data-stu-id="33352-135">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="33352-136">Nyissa meg a [Microsoft 365 felügyeleti központot](https://portal.office.com/), és rendelje hozzá a licenceket a felhasználókhoz.</span><span class="sxs-lookup"><span data-stu-id="33352-136">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Felügyeleti központ kezdőlapja](./media/14AdminPortal.png)

2. <span data-ttu-id="33352-138">Az **Aktív felhasználók** oldalon jelölje ki azokat a felhasználókat, akikhez licencet szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="33352-138">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Licencek hozzárendelése](./media/15AssignLicenses.png)

3. <span data-ttu-id="33352-140">Ellenőrizze, hogy a **Dynamics 365 Project Operations (CRM) előzetes verzió** és az **Office 365 Project Operations - előzetes verzió** licence ki van-e jelölve, majd válassza a **változtatások mentése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="33352-140">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** license have been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="33352-141">A Finance próbaverziójának ajánlatát nem kell felhasználóhoz rendelni.</span><span class="sxs-lookup"><span data-stu-id="33352-141">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="33352-142">Új projekt indítása LCS-ben</span><span class="sxs-lookup"><span data-stu-id="33352-142">Start a new project in LCS</span></span>

<span data-ttu-id="33352-143">Hozzon létre egy új LCS-projektet a következő témakörben leírtak szerint: [Új projekt indítása LCS-ben](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="33352-143">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="33352-144">Azure-előfizetés hozzáadása LCS-projekthez</span><span class="sxs-lookup"><span data-stu-id="33352-144">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="33352-145">A feladat végrehajtásához hajtsa végre a következő témakör lépéseit: [Azure-előfizetés hozzáadása LCS-projekthez](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="33352-145">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="33352-146">A Finance-bemutatókörnyezet telepítése a Project Operations erőforrás-/nem készletalapú forgatókönyvekhez alkalmazással</span><span class="sxs-lookup"><span data-stu-id="33352-146">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="33352-147">A telepítés végrehajtásához kövesse a következő témakör útmutatását: [Új környezet kiépítése](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="33352-147">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="33352-148">Használja a [bemutatókörnyezet](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) telepítési típust az előzetes verzióhoz.</span><span class="sxs-lookup"><span data-stu-id="33352-148">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="33352-149">CDS beállításainak és konfigurációs adatainak telepítése</span><span class="sxs-lookup"><span data-stu-id="33352-149">Install CDS setup and configuration data</span></span>

<span data-ttu-id="33352-150">Telepítse a CDS beállításait és konfigurációs adatait a következő témakörben leírtak szerint: [Beállítás és konfigurációs adatok alkalmazása a Common Data Service rendszerben](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="33352-150">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="33352-151">Ezt a lépést csak azután hajthatja végre, hogy Finance bemutatókörnyezete van telepítve, és elkészültek a bemutató adatok az FO-ban.</span><span class="sxs-lookup"><span data-stu-id="33352-151">Complete this step only after Finance demo environment is deployed and demo data in FO is ready.</span></span>
