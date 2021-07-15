---
title: Regisztráció az előzetes verziós előfizetésre – Lite
description: Ez a témakör a Project Operations Lite telepítés – ajánlattól proforma számlázásig alkalmazásra való regisztrálással és annak telepítésével kapcsolatos információkat tartalmaz.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334785"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="5ea71-103">Regisztráció az előzetes verziós előfizetésre – Lite</span><span class="sxs-lookup"><span data-stu-id="5ea71-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="5ea71-104">Ez témakör ismerteti, hogyan lehet előfizetni a próbaverziós ajánlatra és kiépíteni a Dynamics 365 Project Operations egyszerű telepítését a proforma számlázás kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="5ea71-104">This topic explains how to subscribe to the trial offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="5ea71-105">Ez a folyamat a Project Operations következő kiadásaiban változni fog.</span><span class="sxs-lookup"><span data-stu-id="5ea71-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5ea71-106">Előfeltételek</span><span class="sxs-lookup"><span data-stu-id="5ea71-106">Prerequisites</span></span>
- <span data-ttu-id="5ea71-107">Az előzetes verziót telepítő felhasználónak Azure-bérlői globális rendszergazdai jogosultsággal kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="5ea71-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="5ea71-108">A bérlőt az első ajánlat beválátása során hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="5ea71-108">You can create a tenant during the first offer redemption.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5ea71-109">A szervezetnél csak egy személynek, a bérlői rendszergazdának kell elvégeznie ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="5ea71-109">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="5ea71-110">Ha nem Ön ennek a kiadásnak az előfizetője, várjon, amíg a szervezete regisztrálva lesz, és megkapta a felhasználói hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="5ea71-110">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="5ea71-111">A próbaverziók a bérlőn és egyszer használhatók.</span><span class="sxs-lookup"><span data-stu-id="5ea71-111">Trials are single use in the tenant.</span></span> <span data-ttu-id="5ea71-112">Csak egyszer lehet futtatni a próbaverziót.</span><span class="sxs-lookup"><span data-stu-id="5ea71-112">You can only run a trial one time.</span></span> <span data-ttu-id="5ea71-113">Javasoljuk, hogy a próbaidőszak céljára hozzon létre új bérlőt.</span><span class="sxs-lookup"><span data-stu-id="5ea71-113">We recommend that you create a new tenant for the purpose of the trial.</span></span>

### <a name="dynamics-365-project-operations-trial"></a><span data-ttu-id="5ea71-114">Dynamics 365 Project Operations próbaverzió</span><span class="sxs-lookup"><span data-stu-id="5ea71-114">Dynamics 365 Project Operations trial</span></span> 

<span data-ttu-id="5ea71-115">Mielőtt elkezdené, ügyeljen arra, hogy a felhasználó munkafiókjával jelentkezzen be a böngészőbe abban a bérlőben, ahol a Project Operations előzetes verzióját szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="5ea71-115">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="5ea71-116">Menjen a [Project Operations próbaverzió](https://aka.ms/try-po) helyre az első ajánlati kód beváltásához, **Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="5ea71-116">Go to [Project Operations Trial](https://aka.ms/try-po) to redeem the first offer code, **Dynamics 365 Project Operations**.</span></span>
2. <span data-ttu-id="5ea71-117">Hagyja jóvá a megrendelést.</span><span class="sxs-lookup"><span data-stu-id="5ea71-117">Confirm your order.</span></span>

  <span data-ttu-id="5ea71-118">Látni fogja, hogy a megerősítő ajánlat sikeresen be lett váltva.</span><span class="sxs-lookup"><span data-stu-id="5ea71-118">You'll see the confirmation offer was successfully redeemed.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="5ea71-119">Licencek hozzárendelése</span><span class="sxs-lookup"><span data-stu-id="5ea71-119">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5ea71-120">A következő lépések végrehajtásához rendszergazdai hozzáféréssel kell rendelkeznie a szervezete Microsoft 365-portáljához.</span><span class="sxs-lookup"><span data-stu-id="5ea71-120">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="5ea71-121">Nyissa meg a [Microsoft 365 felügyeleti központot](https://portal.office.com/), és rendelje hozzá a licenceket a felhasználókhoz.</span><span class="sxs-lookup"><span data-stu-id="5ea71-121">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>
2. <span data-ttu-id="5ea71-122">Az **Aktív felhasználók** oldalon jelölje ki azokat a felhasználókat, akikhez licencet szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="5ea71-122">On the **Active users** page, select the users that you want to assign a license to.</span></span>
3. <span data-ttu-id="5ea71-123">Ellenőrizze, hogy a **Dynamics 365 Project Operations** licenc ki legyen jelölve.</span><span class="sxs-lookup"><span data-stu-id="5ea71-123">Verify that the **Dynamics 365 Project Operations** license is selected.</span></span> 
4. <span data-ttu-id="5ea71-124">Válassza a **Módosítások mentése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="5ea71-124">Select **Save changes**.</span></span>

## <a name="create-a-new-dataverse-environment"></a><span data-ttu-id="5ea71-125">Új Dataverse-környezet létrehozása</span><span class="sxs-lookup"><span data-stu-id="5ea71-125">Create a new Dataverse environment</span></span>

1. <span data-ttu-id="5ea71-126">Építsen ki új Project Operations Dataverse-telepítési környezetet a [Dataverse-telepítési modell](lite-deployment.md) utasításait követve.</span><span class="sxs-lookup"><span data-stu-id="5ea71-126">Provision a new Project Operations Dataverse deployment environment by following instructions in the topic, [Dataverse deployment model](lite-deployment.md).</span></span> <span data-ttu-id="5ea71-127">A környezet típusának kiválasztása esetén ügyeljen arra, hogy a **Próba (előfizetés alapú)** változatot használja.</span><span class="sxs-lookup"><span data-stu-id="5ea71-127">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>

  ![Új környezet](./media/19CreateEnvironment.png)

2. <span data-ttu-id="5ea71-129">Válassz a **Dynamics 365-alkalmazások engedélyezése** beállítást, és hagyja üresen az **Alkalmazások automatikus telepítése** jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="5ea71-129">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="5ea71-130">Válassza ki a **Mentés** gombot a környezet létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="5ea71-130">Select **Save** to create the environment.</span></span>

  ![Adatbázis hozzáadása](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="5ea71-132">A környezet létrehozása után telepítse a **Microsoft Dynamics 365 Project Operations** megoldást.</span><span class="sxs-lookup"><span data-stu-id="5ea71-132">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![Megoldás telepítése](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="5ea71-134">CDS-konfiguráció telepítése és a beállítási bemutató adatok alkalmazása</span><span class="sxs-lookup"><span data-stu-id="5ea71-134">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="5ea71-135">Telepítse a CDS-konfigurációt, és állítsa be a bemutató adatokat a következő témakör utasításait követve: [Bemutató beállítások és konfigurációs adatok alkalmazása](lite-apply-demo-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="5ea71-135">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
