---
title: Regisztráció a Project Operations előzetes verziós előfizetésekre az erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a témakör információt nyújt arról, hogyan lehet regisztrálni és telepíteni a Dynamics 365 Project Operations alkalmazást erőforrás-/nem készletalapú forgatókönyvek esetén.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948912"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="b171c-103">Regisztráció a Project Operations előzetes verziós előfizetésekre az erőforrás-/nem készletalapú forgatókönyvek esetén</span><span class="sxs-lookup"><span data-stu-id="b171c-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="b171c-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="b171c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b171c-105">Ez a témakör ismerteti, hogyan lehet előfizetni az előzetes verzióra/partnerajánlatra, és telepíteni a Project Operations-környezetet erőforrás-/nem készletalapú forgatókönyvek esetén.</span><span class="sxs-lookup"><span data-stu-id="b171c-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b171c-106">Előfeltételek</span><span class="sxs-lookup"><span data-stu-id="b171c-106">Prerequisites</span></span>

- <span data-ttu-id="b171c-107">Kapni fog egy e-mailt, amely meghívja, hogy részt vegyen az előzetes verzióban.</span><span class="sxs-lookup"><span data-stu-id="b171c-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="b171c-108">Előzetes verziót kérhet a [Project Operations webhelyén](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="b171c-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="b171c-109">Az előzetes verziót telepítő felhasználónak Azure-bérlői globális rendszergazdai jogosultsággal kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="b171c-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="b171c-110">A Finance-környezet telepítéséhez érvényes Azure-előfizetésre van szükség, amely környezetenként kerül számlázásra.</span><span class="sxs-lookup"><span data-stu-id="b171c-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="b171c-111">A kezdéshez használhatja a szervezet meglévő előfizetését, vagy egy [Azure-próbaverziót](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="b171c-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="b171c-112">A CDS-környezet korlátozott, 30 napos időszakra ingyenesen biztosítva lesz.</span><span class="sxs-lookup"><span data-stu-id="b171c-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="b171c-113">Feliratkozás</span><span class="sxs-lookup"><span data-stu-id="b171c-113">Subscribe</span></span>

<span data-ttu-id="b171c-114">Amikor megkapja az [előzetes verzióra vonatkozó kérelem](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) jóváhagyását, e-mailben két ajánlatot kap a Microsofttól.</span><span class="sxs-lookup"><span data-stu-id="b171c-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="b171c-115">Ez lehetővé teszi, hogy telepítse a Project Operations előzetes verzióját:</span><span class="sxs-lookup"><span data-stu-id="b171c-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="b171c-116">Dynamics 365 Project Operations – Előzetes próbaverzió</span><span class="sxs-lookup"><span data-stu-id="b171c-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="b171c-117">Dynamics 365 for Finance and Operations előzetes próbaverzió.</span><span class="sxs-lookup"><span data-stu-id="b171c-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b171c-118">A szervezetnél csak egy személynek, a bérlői rendszergazdának kell elvégeznie ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="b171c-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="b171c-119">Ha nem Ön ennek a kiadásnak az előfizetője, várjon, amíg a szervezete regisztrálva lesz, és megkapta a felhasználói hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="b171c-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="b171c-120">Dynamics 365 Project Operations – Előzetes próbaverzió</span><span class="sxs-lookup"><span data-stu-id="b171c-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="b171c-121">Váltsa ki az első ajánlatot, a **Dynamics 365 Project Operations próbaverzióját** az üdvözlő e-mailben megadott URL-címmel.</span><span class="sxs-lookup"><span data-stu-id="b171c-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![Első ajánlat](./media/1FirstOffer.png)

2. <span data-ttu-id="b171c-123">Ellenőrizze, hogy olyan felhasználóként jelentkezett-e be, aki ahhoz a szervezethez tartozik, amely a szolgáltatásra elő fog fizetni.</span><span class="sxs-lookup"><span data-stu-id="b171c-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="b171c-124">Folytassa az ajánlat beváltását.</span><span class="sxs-lookup"><span data-stu-id="b171c-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="b171c-125">Válassza az **Igen, hozzáadás a fiókomhoz** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="b171c-125">Select **Yes, add it to my account**.</span></span>

![Ajánlat beváltása](./media/2RedeemFirstOffer.png)

![Ajánlat megerősítése](./media/3ConfirmFirstOffer.png)

![Ajánlat beváltva](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="b171c-129">Dynamics 365 Finance előzetes próbaverzió</span><span class="sxs-lookup"><span data-stu-id="b171c-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="b171c-130">Ismételje meg ugyanezeket a lépéseket az üdvözlő e-mailben szereplő második ajánlattal.</span><span class="sxs-lookup"><span data-stu-id="b171c-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="b171c-131">Licencek hozzárendelése</span><span class="sxs-lookup"><span data-stu-id="b171c-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b171c-132">A következő lépések végrehajtásához rendszergazdai hozzáféréssel kell rendelkeznie a szervezete Office 365-portáljához.</span><span class="sxs-lookup"><span data-stu-id="b171c-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="b171c-133">Nyissa meg a [Microsoft 365 felügyeleti központot](https://portal.office.com/), és rendelje hozzá a licenceket a felhasználókhoz.</span><span class="sxs-lookup"><span data-stu-id="b171c-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![Office felügyeleti portál](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="b171c-135">Az **Aktív felhasználók** oldalon jelölje ki azokat a felhasználókat, akikhez licencet szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="b171c-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Licencek hozzárendelése](./media/6AssignLicenses.png)

3. <span data-ttu-id="b171c-137">Ellenőrizze, hogy a Project Operations licence ki van-e jelölve, majd válassza a **Módosítások mentése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="b171c-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="b171c-138">A Finance próbaverziójának ajánlatát nem kell felhasználóhoz rendelni.</span><span class="sxs-lookup"><span data-stu-id="b171c-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="b171c-139">Új projekt indítása LCS-ben</span><span class="sxs-lookup"><span data-stu-id="b171c-139">Start a new project in LCS</span></span>

<span data-ttu-id="b171c-140">Hozzon létre egy új LCS-projektet a következő témakörben leírtak szerint: [Új projekt indítása LCS-ben](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="b171c-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="b171c-141">Azure-előfizetés hozzáadása LCS-projekthez</span><span class="sxs-lookup"><span data-stu-id="b171c-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="b171c-142">A feladat végrehajtásához hajtsa végre a következő témakör lépéseit: [Azure-előfizetés hozzáadása LCS-projekthez](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="b171c-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="b171c-143">A Finance-bemutatókörnyezet telepítése a Project Operations erőforrás-/nem készletalapú forgatókönyvekhez alkalmazással</span><span class="sxs-lookup"><span data-stu-id="b171c-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="b171c-144">A telepítés végrehajtásához kövesse a következő témakör útmutatását: [Új környezet kiépítése](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="b171c-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="b171c-145">Használja a [bemutatókörnyezet](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) telepítési típust az előzetes verzióhoz.</span><span class="sxs-lookup"><span data-stu-id="b171c-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="b171c-146">CDS beállításainak és konfigurációs adatainak telepítése</span><span class="sxs-lookup"><span data-stu-id="b171c-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="b171c-147">Telepítse a CDS beállításait és konfigurációs adatait a következő témakörben leírtak szerint: [Beállítás és konfigurációs adatok alkalmazása a Common Data Service rendszerben](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="b171c-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

