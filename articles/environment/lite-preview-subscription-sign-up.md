---
title: Regisztráció az előzetes verziós előfizetésre – Lite
description: Ez a témakör a Project Operations Lite telepítés – ajánlattól proforma számlázásig alkalmazásra való regisztrálással és annak telepítésével kapcsolatos információkat tartalmaz.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6f4360b7febab57b97df0776ef9148d2a38f16a7
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175894"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="e7b6e-103">Regisztráció az előzetes verziós előfizetésre – Lite</span><span class="sxs-lookup"><span data-stu-id="e7b6e-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="e7b6e-104">Ez a témakör a Dynamics 365 Project Operations Lite telepítés – ajánlattól proforma számlázásig alkalmazásra előzetes verziós partnerajánlatára való regisztrálással és annak telepítésével kapcsolatos információkat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-104">This topic explains how to subscribe to the preview partner offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="e7b6e-105">Ez a folyamat a Project Operations következő kiadásaiban változni fog.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e7b6e-106">Előfeltételek</span><span class="sxs-lookup"><span data-stu-id="e7b6e-106">Prerequisites</span></span>

- <span data-ttu-id="e7b6e-107">Kapni fog egy e-mailt, amely meghívja, hogy részt vegyen az előzetes verzióban.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-107">You'll receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="e7b6e-108">Előzetes verziót kérhet a [Project Operations webhelyén](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="e7b6e-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="e7b6e-109">Az előzetes verziót telepítő felhasználónak Azure-bérlői globális rendszergazdai jogosultsággal kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="e7b6e-110">Tekintse át az összes általános szerződési feltételt.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-110">Review all terms and conditions.</span></span>

## <a name="subscribe"></a><span data-ttu-id="e7b6e-111">Feliratkozás</span><span class="sxs-lookup"><span data-stu-id="e7b6e-111">Subscribe</span></span>

<span data-ttu-id="e7b6e-112">Amikor megkapja az [előzetes verzióra vonatkozó kérelem](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) jóváhagyását, e-mailben két ajánlatot kap a Microsofttól.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-112">When you receive a [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) approval, you'll receive two offers from Microsoft by email.</span></span> <span data-ttu-id="e7b6e-113">Ez lehetővé teszi, hogy telepítse a Project Operations előzetes verzióját:</span><span class="sxs-lookup"><span data-stu-id="e7b6e-113">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="e7b6e-114">Dynamics 365 Project Operations (CRM) – Előzetes próbaverzió</span><span class="sxs-lookup"><span data-stu-id="e7b6e-114">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="e7b6e-115">Office 365 Project Operations – Előzetes próbaverzió</span><span class="sxs-lookup"><span data-stu-id="e7b6e-115">Office 365 Project Operations - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e7b6e-116">A szervezetnél csak egy személynek, a bérlői rendszergazdának kell elvégeznie ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-116">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="e7b6e-117">Ha nem Ön ennek a kiadásnak az előfizetője, várjon, amíg a szervezete regisztrálva lesz, és megkapta a felhasználói hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-117">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="e7b6e-118">Dynamics 365 Project Operations (CRM) – Előzetes próbaverzió</span><span class="sxs-lookup"><span data-stu-id="e7b6e-118">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="e7b6e-119">Mielőtt elkezdené, ügyeljen arra, hogy a felhasználó munkafiókjával jelentkezzen be a böngészőbe abban a bérlőben, ahol a Project Operations előzetes verzióját szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-119">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="e7b6e-120">Váltsa be az első **Dynamics 365 Project Operations (CRM) – előzetes próbaverzió** ajánlatkódját a böngésző URL-mezőjébe történő beillesztéssel.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-120">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Ajánlat beváltása](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="e7b6e-122">Hagyja jóvá a megrendelést.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-122">Confirm your order.</span></span>
<span data-ttu-id="e7b6e-123">![Ellenőrizze a sorrendet](./media/17ConfirmOrderNew.png)</span><span class="sxs-lookup"><span data-stu-id="e7b6e-123">![Confirm the order](./media/17ConfirmOrderNew.png)</span></span>

<span data-ttu-id="e7b6e-124">A megerősítő ajánlat sikeres beváltását láthatja.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-124">You'll see confirmation offer was successfully redeemed.</span></span>

![Jóváhagyás](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="e7b6e-126">Office 365 Project Operations – Előzetes próbaverzió</span><span class="sxs-lookup"><span data-stu-id="e7b6e-126">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="e7b6e-127">Ismételje meg ugyanazokat a lépéseket, mint az első ajánlatkóddal.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-127">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="e7b6e-128">Ügyeljen arra, hogy a második ajánlatkódot ugyanazzal a felhasználói fiókkal adja hozzá, amelyet az első ajánlatkódhoz használt.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-128">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="e7b6e-129">Licencek hozzárendelése</span><span class="sxs-lookup"><span data-stu-id="e7b6e-129">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e7b6e-130">A következő lépések végrehajtásához rendszergazdai hozzáféréssel kell rendelkeznie a szervezete Microsoft 365-portáljához.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-130">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="e7b6e-131">Nyissa meg a [Microsoft 365 felügyeleti központot](https://portal.office.com/), és rendelje hozzá a licenceket a felhasználókhoz.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-131">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Felügyeleti központ kezdőlapja](./media/14AdminPortal.png)

2. <span data-ttu-id="e7b6e-133">Az **Aktív felhasználók** oldalon jelölje ki azokat a felhasználókat, akikhez licencet szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-133">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Licencek hozzárendelése](./media/15AssignLicenses.png)

3. <span data-ttu-id="e7b6e-135">Ellenőrizze, hogy a **Dynamics 365 Project Operations (CRM) előzetes verzió** és az **Office 365 Project Operations - előzetes verzió** licencei ki legyenek választva majd válassza a módosítások mentése lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-135">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** licenses are selected.</span></span> 
4. <span data-ttu-id="e7b6e-136">Válassza a **Módosítások mentése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-136">Select **Save changes**.</span></span>

## <a name="create-a-new-cds-environment"></a><span data-ttu-id="e7b6e-137">Új CDS-környezet létrehozása</span><span class="sxs-lookup"><span data-stu-id="e7b6e-137">Create a new CDS environment</span></span>

1. <span data-ttu-id="e7b6e-138">Építsen ki új Project Pperations CDS-telepítési környezetet a [CDS telepítési modell](lite-deployment.md) utasításait követve.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-138">Provision a new Project Operations CDS deployment environment by following instructions in the topic, [CDS deployment model](lite-deployment.md).</span></span> <span data-ttu-id="e7b6e-139">A környezet típusának kiválasztása esetén ügyeljen arra, hogy a **Próba (előfizetés alapú)** változatot használja.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-139">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>
<span data-ttu-id="e7b6e-140">![Új környezet](./media/19CreateEnvironment.png)</span><span class="sxs-lookup"><span data-stu-id="e7b6e-140">![New environment](./media/19CreateEnvironment.png)</span></span>

2. <span data-ttu-id="e7b6e-141">Válassz a **Dynamics 365-alkalmazások engedélyezése** beállítást, és hagyja üresen az **Alkalmazások automatikus telepítése** jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-141">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="e7b6e-142">Válassza ki a **Mentés** gombot a környezet létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-142">Select **Save** to create the environment.</span></span>

![Adatbázis hozzáadása](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="e7b6e-144">A környezet létrehozása után telepítse a **Microsoft Dynamics 365 Project Operations** megoldást.</span><span class="sxs-lookup"><span data-stu-id="e7b6e-144">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![Megoldás telepítése](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="e7b6e-146">CDS-konfiguráció telepítése és a beállítási bemutató adatok alkalmazása</span><span class="sxs-lookup"><span data-stu-id="e7b6e-146">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="e7b6e-147">Telepítse a CDS-konfigurációt, és állítsa be a bemutató adatokat a következő témakör utasításait követve: [Bemutató beállítások és konfigurációs adatok alkalmazása](lite-apply-demo-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="e7b6e-147">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>
