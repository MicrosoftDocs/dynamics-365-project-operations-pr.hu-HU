---
title: Regisztráció a Project Operations előzetes verziós előfizetésekre az erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a témakör információt nyújt arról, hogyan lehet regisztrálni és telepíteni a Dynamics 365 Project Operations alkalmazást erőforrás-/nem készletalapú forgatókönyvek esetén.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334830"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="14b4b-103">Regisztráció a Project Operations előzetes verziós előfizetésekre az erőforrás-/nem készletalapú forgatókönyvek esetén</span><span class="sxs-lookup"><span data-stu-id="14b4b-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="14b4b-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="14b4b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="14b4b-105">Ez témakör ismerteti, hogyan lehet előfizetni a próbaverziós ajánlatra, és hogyan lehet Project Operations környezetet telepíteni erőforrás-/nem készletalapú forgatókönyvekhez.</span><span class="sxs-lookup"><span data-stu-id="14b4b-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="14b4b-106">Előfeltételek</span><span class="sxs-lookup"><span data-stu-id="14b4b-106">Prerequisites</span></span>
- <span data-ttu-id="14b4b-107">Az előzetes verziót telepítő felhasználónak Azure-bérlői globális rendszergazdai jogosultsággal kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="14b4b-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="14b4b-108">A bérlőt az első ajánlat beválátása során hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="14b4b-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="14b4b-109">A Finance-környezet telepítéséhez érvényes Azure-előfizetésre van szükség, amely környezetenként kerül számlázásra.</span><span class="sxs-lookup"><span data-stu-id="14b4b-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="14b4b-110">A kezdéshez használhatja a szervezet meglévő előfizetését, vagy egy [Azure-próbaverziót](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="14b4b-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="14b4b-111">A CDS-környezet korlátozott, 30 napos időszakra ingyenesen biztosítva lesz.</span><span class="sxs-lookup"><span data-stu-id="14b4b-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="14b4b-112">A szervezetnél csak egy személynek, a bérlői rendszergazdának kell elvégeznie ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="14b4b-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="14b4b-113">Ha nem Ön ennek a kiadásnak az előfizetője, várjon, amíg a szervezete regisztrálva lesz, és megkapta a felhasználói hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="14b4b-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="14b4b-114">A próbaverziók a bérlőn és egyszer használhatók.</span><span class="sxs-lookup"><span data-stu-id="14b4b-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="14b4b-115">Csak egyszer lehet futtatni a próbaverziót.</span><span class="sxs-lookup"><span data-stu-id="14b4b-115">You can only run a trial one time.</span></span> <span data-ttu-id="14b4b-116">Javasoljuk, hogy a próbaidőszak céljára hozzon létre új bérlőt.</span><span class="sxs-lookup"><span data-stu-id="14b4b-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="14b4b-117">Dynamics 365 Project Operations (CE) - előzetes verziójú próbeverzió</span><span class="sxs-lookup"><span data-stu-id="14b4b-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="14b4b-118">Mielőtt elkezdené, ügyeljen arra, hogy a felhasználó munkafiókjával jelentkezzen be a böngészőbe abban a bérlőben, ahol a Project Operations előzetes verzióját szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="14b4b-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="14b4b-119">Váltsa be az első ajánlatkódot **Dynamics 365 Project Operations** itt [Project Operations próbaverzió](https://aka.ms/try-po).</span><span class="sxs-lookup"><span data-stu-id="14b4b-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="14b4b-120">Hagyja jóvá a megrendelést.</span><span class="sxs-lookup"><span data-stu-id="14b4b-120">Confirm your order.</span></span>

  <span data-ttu-id="14b4b-121">A megerősítő ajánlatot sikeres beváltását láthatja.</span><span class="sxs-lookup"><span data-stu-id="14b4b-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="14b4b-122">Dynamics 365 Finance előzetes próbaverzió</span><span class="sxs-lookup"><span data-stu-id="14b4b-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="14b4b-123">Menjen a [Dynamics 365 for Finance előzetesverzió kipróbálása](https://aka.ms/trypoche) helyre, és ismételje meg az előző szakasz lépéseit az ajánlattal, Iratkozzon fel a Felhőben szolgáltatott környezetre.</span><span class="sxs-lookup"><span data-stu-id="14b4b-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="14b4b-124">Licencek hozzárendelése</span><span class="sxs-lookup"><span data-stu-id="14b4b-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="14b4b-125">A következő lépések végrehajtásához rendszergazdai hozzáféréssel kell rendelkeznie a szervezete Microsoft 365-portáljához.</span><span class="sxs-lookup"><span data-stu-id="14b4b-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="14b4b-126">Nyissa meg a [Microsoft 365 felügyeleti központot](https://portal.office.com/), és rendelje hozzá a licenceket a felhasználókhoz.</span><span class="sxs-lookup"><span data-stu-id="14b4b-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="14b4b-127">Az **Aktív felhasználók** oldalon jelölje ki azokat a felhasználókat, akikhez licencet szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="14b4b-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="14b4b-128">Ellenőrizze, hogy a **Dynamics 365 Project Operations** licenc ki legyen jelölve, majd válassza a **Módosítások mentése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="14b4b-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="14b4b-129">A Finance próbaverziójának ajánlatát nem kell felhasználóhoz rendelni.</span><span class="sxs-lookup"><span data-stu-id="14b4b-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="14b4b-130">Új projekt indítása LCS-ben</span><span class="sxs-lookup"><span data-stu-id="14b4b-130">Start a new project in LCS</span></span>

<span data-ttu-id="14b4b-131">Hozzon létre egy új LCS-projektet a következő témakörben leírtak szerint: [Új projekt indítása LCS-ben](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="14b4b-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="14b4b-132">Azure-előfizetés hozzáadása LCS-projekthez</span><span class="sxs-lookup"><span data-stu-id="14b4b-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="14b4b-133">A feladat végrehajtásához hajtsa végre a következő témakör lépéseit: [Azure-előfizetés hozzáadása LCS-projekthez](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="14b4b-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="14b4b-134">A Finance-bemutatókörnyezet telepítése a Project Operations erőforrás-/nem készletalapú forgatókönyvekhez alkalmazással</span><span class="sxs-lookup"><span data-stu-id="14b4b-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="14b4b-135">A telepítés végrehajtásához kövesse a következő témakör útmutatását: [Új környezet kiépítése](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="14b4b-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="14b4b-136">Használja a [bemutatókörnyezet](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) telepítési típust az előzetes verzióhoz.</span><span class="sxs-lookup"><span data-stu-id="14b4b-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="14b4b-137">CDS beállításainak és konfigurációs adatainak telepítése</span><span class="sxs-lookup"><span data-stu-id="14b4b-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="14b4b-138">Telepítse a CDS beállításait és konfigurációs adatait a következő témakörben leírtak szerint: [Beállítás és konfigurációs adatok alkalmazása a Common Data Service rendszerben](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="14b4b-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="14b4b-139">Ezt a lépést csak a Finance bemutatókörnyezet telepítése és a bemutatóadatok elkészülte után hajtsa végre.</span><span class="sxs-lookup"><span data-stu-id="14b4b-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
