---
title: A központi telepítés típusai
description: Ez a témakör a Project Operations az Ön vállalatának megfelelő telepítéstípusának megállapításában segítő információkat tartalmaz.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948908"
---
# <a name="deployment-types"></a><span data-ttu-id="fb479-103">A központi telepítés típusai</span><span class="sxs-lookup"><span data-stu-id="fb479-103">Deployment types</span></span>

<span data-ttu-id="fb479-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="fb479-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb479-105">Miután megvásárolta a licencet, kezdje itt a Dynamics 365 Project Operations legjobb telepítési modelljének meghatározásával az [Irányított telepítési folyamat](https://aka.ms/provisionprojectoperations) használatával.</span><span class="sxs-lookup"><span data-stu-id="fb479-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="fb479-106">Miután befejezte az Irányított telepítési folyamatot, a rendszer a helyes felügyeleti portálra irányítja a telepítés befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="fb479-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="fb479-107">A telepítés befejezéséhez tekintse meg a telepítés alábbi részleteit.</span><span class="sxs-lookup"><span data-stu-id="fb479-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="fb479-108">A Dynamics meglévő Dynamics 365 Project Service Automation rendszert használó ügyfelei</span><span class="sxs-lookup"><span data-stu-id="fb479-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="fb479-109">A Project Operations a Project Service Automation szolgáltatással szállított képességeket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fb479-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="fb479-110">A jövőben ezen ügyfelek számára egy frissítési elérési út kerül kiadásra</span><span class="sxs-lookup"><span data-stu-id="fb479-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="fb479-111">A Dynamics 365 Finance Projektmenedzsment és könyvelés alkalmazást használó meglévő ügyfelei</span><span class="sxs-lookup"><span data-stu-id="fb479-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="fb479-112">A Finance Projektmenedzsment és könyvelés funkciót használó meglévő ügyfelei továbbra is használhatják azt.</span><span class="sxs-lookup"><span data-stu-id="fb479-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="fb479-113">Lásd: [Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez](#pma).</span><span class="sxs-lookup"><span data-stu-id="fb479-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="fb479-114">A Project Operations több telepítési lehetőséget is támogat, hogy megfeleljen az igényeinek.</span><span class="sxs-lookup"><span data-stu-id="fb479-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="fb479-115">Akár új, akár meglévő Dynamics 365-ügyfél, a Project Operations képes támogatni az igényeit.</span><span class="sxs-lookup"><span data-stu-id="fb479-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="fb479-116">A [telepítési kérdőívünk](https://aka.ms/provisionprojectoperations) segítséget nyújt a megfelelő telepítés meghatározásában.</span><span class="sxs-lookup"><span data-stu-id="fb479-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="fb479-117">Az eredmények a következő telepítési típusok egyike felé irányítják:</span><span class="sxs-lookup"><span data-stu-id="fb479-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="fb479-118">Egyszerű telepítés – proforma számlázás</span><span class="sxs-lookup"><span data-stu-id="fb479-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="fb479-119">Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez</span><span class="sxs-lookup"><span data-stu-id="fb479-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="fb479-120">Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez</span><span class="sxs-lookup"><span data-stu-id="fb479-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="fb479-121">A Project Operations a készletalapú/gyártási megrendeléseken alapuló forgatókönyveket és a nem készletalapú/erőforrásalapú forgatókönyveket támogatja ugyanazon környezetben, jogientitás-szintű konfigurációkon keresztül.</span><span class="sxs-lookup"><span data-stu-id="fb479-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="fb479-122">A Contoso például az amerikai gyártói létesítményben (jogi entitás = Contoso Manufacturing United States) készletalapú/gyártási megrendeléseken alapuló képességeket, az Egyesült Királyságban található Contoso Robotics Arms szervizüzemben (jogi entitás = Contoso Robotics United Kingdom) pedig nem készletalapú/erőforrásalapú képességeket használhat.</span><span class="sxs-lookup"><span data-stu-id="fb479-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="fb479-123"><a name="lite"><a/>Egyszerű telepítés – proforma számlázás</span><span class="sxs-lookup"><span data-stu-id="fb479-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="fb479-124">A Lite telepítés a következő lehetőségeket tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="fb479-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="fb479-125">Projekttervezés a Microsoft Webes projekt segítségével</span><span class="sxs-lookup"><span data-stu-id="fb479-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="fb479-126">Többdimenziós árképzés</span><span class="sxs-lookup"><span data-stu-id="fb479-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="fb479-127">Egyesített erőforrás-kezelés</span><span class="sxs-lookup"><span data-stu-id="fb479-127">Unified Resource Management</span></span>
- <span data-ttu-id="fb479-128">Időkövetés</span><span class="sxs-lookup"><span data-stu-id="fb479-128">Time Tracking</span></span>
- <span data-ttu-id="fb479-129">Alapvető költség</span><span class="sxs-lookup"><span data-stu-id="fb479-129">Basic Expense</span></span>
- <span data-ttu-id="fb479-130">Számlajavaslat</span><span class="sxs-lookup"><span data-stu-id="fb479-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="fb479-131">Telepítési lépések:</span><span class="sxs-lookup"><span data-stu-id="fb479-131">Deployment steps:</span></span>
<span data-ttu-id="fb479-132">Határozza meg a Project Operations legjobb telepítési modelljét a [telepítési kérdőív](https://aka.ms/provisionprojectoperations) használatával.</span><span class="sxs-lookup"><span data-stu-id="fb479-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="fb479-133">Ehhez a telepítéshez lásd: [Regisztráció az előzetes verziós előfizetésekre](lite-preview-subscription-sign-up.md) és az [Új környezet kiépítése](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="fb479-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="fb479-134"><a name="integrated"><a/>Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez</span><span class="sxs-lookup"><span data-stu-id="fb479-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="fb479-135">A Project Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez az alábbi képességeket tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="fb479-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="fb479-136">Projekttervezés a Microsoft Webes projekt segítségével</span><span class="sxs-lookup"><span data-stu-id="fb479-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="fb479-137">Többdimenziós árképzés</span><span class="sxs-lookup"><span data-stu-id="fb479-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="fb479-138">Egyesített erőforrás-kezelés</span><span class="sxs-lookup"><span data-stu-id="fb479-138">Unified Resource Management</span></span>
- <span data-ttu-id="fb479-139">Időkövetés</span><span class="sxs-lookup"><span data-stu-id="fb479-139">Time Tracking</span></span>
- <span data-ttu-id="fb479-140">Alapvető költség</span><span class="sxs-lookup"><span data-stu-id="fb479-140">Basic Expense</span></span>
- <span data-ttu-id="fb479-141">Teljes költség</span><span class="sxs-lookup"><span data-stu-id="fb479-141">Full Expense</span></span>
- <span data-ttu-id="fb479-142">Bizonylat OCR</span><span class="sxs-lookup"><span data-stu-id="fb479-142">Receipt OCR</span></span>
- <span data-ttu-id="fb479-143">Teljes számlázás</span><span class="sxs-lookup"><span data-stu-id="fb479-143">Full Invoicing</span></span>
- <span data-ttu-id="fb479-144">Bevételfelismerés</span><span class="sxs-lookup"><span data-stu-id="fb479-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="fb479-145">Telepítési lépések:</span><span class="sxs-lookup"><span data-stu-id="fb479-145">Deployment steps:</span></span>
<span data-ttu-id="fb479-146">Határozza meg a Project Operations legjobb telepítési modelljét a [telepítési kérdőív](https://aka.ms/provisionprojectoperations) használatával.</span><span class="sxs-lookup"><span data-stu-id="fb479-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="fb479-147">Ehhez a telepítéshez lásd: [Regisztráció az előzetes verziós előfizetésekre](resource-sign-up-preview-subscription.md) és az [Új környezet kiépítése](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="fb479-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="fb479-148">Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez</span><span class="sxs-lookup"><span data-stu-id="fb479-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="fb479-149">Projekt tervezése WBS használatával</span><span class="sxs-lookup"><span data-stu-id="fb479-149">Project planning using WBS</span></span>
- <span data-ttu-id="fb479-150">Erőforráskezelés</span><span class="sxs-lookup"><span data-stu-id="fb479-150">Resource Management</span></span>
- <span data-ttu-id="fb479-151">Időkövetés</span><span class="sxs-lookup"><span data-stu-id="fb479-151">Time Tracking</span></span>
- <span data-ttu-id="fb479-152">Teljes költség</span><span class="sxs-lookup"><span data-stu-id="fb479-152">Full Expense</span></span>
- <span data-ttu-id="fb479-153">Bizonylat OCR</span><span class="sxs-lookup"><span data-stu-id="fb479-153">Receipt OCR</span></span>
- <span data-ttu-id="fb479-154">Teljes számlázás</span><span class="sxs-lookup"><span data-stu-id="fb479-154">Full Invoicing</span></span>
- <span data-ttu-id="fb479-155">Bevételfelismerés</span><span class="sxs-lookup"><span data-stu-id="fb479-155">Revenue Recognition</span></span>
- <span data-ttu-id="fb479-156">Termelési rendelések</span><span class="sxs-lookup"><span data-stu-id="fb479-156">Production Orders</span></span>
- <span data-ttu-id="fb479-157">Anyagok támogatása</span><span class="sxs-lookup"><span data-stu-id="fb479-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="fb479-158">Telepítési lépések:</span><span class="sxs-lookup"><span data-stu-id="fb479-158">Deployment steps:</span></span>
<span data-ttu-id="fb479-159">Határozza meg a Project Operations legjobb telepítési modelljét a [telepítési kérdőív](https://aka.ms/provisionprojectoperations) használatával.</span><span class="sxs-lookup"><span data-stu-id="fb479-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="fb479-160">Ehhez a telepítéshez lásd: [Regisztráció az előzetes verziós előfizetésekre](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) és az [Új környezet kiépítése](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="fb479-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



