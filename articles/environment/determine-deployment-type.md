---
title: A telepítés típusának meghatározása
description: Ez a témakör a Project Operations az Ön vállalatának megfelelő telepítéstípusának megállapításában segítő információkat tartalmaz.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078096"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="c9747-103">A telepítés típusának meghatározása</span><span class="sxs-lookup"><span data-stu-id="c9747-103">Determine your deployment type</span></span>

<span data-ttu-id="c9747-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="c9747-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c9747-105">Miután megvásárolta a licencet, kezdje itt a Dynamics 365 Project Operations legjobb telepítési modelljének meghatározásával az [Irányított telepítési folyamat](https://aka.ms/provisionprojectoperations) használatával.</span><span class="sxs-lookup"><span data-stu-id="c9747-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="c9747-106">Miután befejezte az Irányított telepítési folyamatot, a rendszer a helyes felügyeleti portálra irányítja a telepítés befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="c9747-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="c9747-107">A telepítés befejezéséhez tekintse meg a telepítés részleteit.</span><span class="sxs-lookup"><span data-stu-id="c9747-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="c9747-108">A Dynamics meglévő Dynamics 365 Project Service Automation rendszert használó ügyfelei</span><span class="sxs-lookup"><span data-stu-id="c9747-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="c9747-109">A Project Operations a Project Service Automation szolgáltatással szállított képességeket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c9747-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="c9747-110">A jövőben ezen ügyfelek számára egy frissítési elérési út kerül kiadásra</span><span class="sxs-lookup"><span data-stu-id="c9747-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="c9747-111">A Dynamics 365 Finance Projektmenedzsment és könyvelés alkalmazást használó meglévő ügyfelei</span><span class="sxs-lookup"><span data-stu-id="c9747-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="c9747-112">A Finance Projektmenedzsment és könyvelés funkciót használó meglévő ügyfelei továbbra is használhatják azt változatlanul.</span><span class="sxs-lookup"><span data-stu-id="c9747-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="c9747-113">Lásd: [Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez](#pma).</span><span class="sxs-lookup"><span data-stu-id="c9747-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="c9747-114">A központi telepítés típusai</span><span class="sxs-lookup"><span data-stu-id="c9747-114">Deployment types</span></span>
<span data-ttu-id="c9747-115">A Project Operations több telepítési lehetőséget is támogat, hogy megfeleljen az igényeinek.</span><span class="sxs-lookup"><span data-stu-id="c9747-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="c9747-116">Akár új, akár meglévő Dynamics 365-ügyfél, a Project Operations képes támogatni az igényeit.</span><span class="sxs-lookup"><span data-stu-id="c9747-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="c9747-117">A [telepítési kérdőívünk](https://aka.ms/provisionprojectoperations) segítséget nyújt a megfelelő telepítés meghatározásában.</span><span class="sxs-lookup"><span data-stu-id="c9747-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="c9747-118">Az eredmények a következő telepítési típusok egyike felé irányítják:</span><span class="sxs-lookup"><span data-stu-id="c9747-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="c9747-119">Egyszerű telepítés – proforma számlázás</span><span class="sxs-lookup"><span data-stu-id="c9747-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="c9747-120">Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez</span><span class="sxs-lookup"><span data-stu-id="c9747-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="c9747-121">Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez</span><span class="sxs-lookup"><span data-stu-id="c9747-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="c9747-122">A Project Operations a készletalapú/gyártási megrendeléseken alapuló forgatókönyveket és a nem készletalapú/erőforrásalapú forgatókönyveket támogatja ugyanazon környezetben, jogientitás-szintű konfigurációkon keresztül.</span><span class="sxs-lookup"><span data-stu-id="c9747-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="c9747-123">A Contoso például az Egyesült államokbeli gyártási létesítményben a készletezett/termelési rendelés funkcióit használhatja (Jogi személy = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="c9747-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="c9747-124">A Contoso a nem készletezett/erőforrás alapú lehetőségeket használhatja a Contoso Robotics Arms karbantartási létesítményében az Egyesült Királyságban (a jogi személy = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="c9747-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="c9747-125">Egyszerű telepítés – proforma számlázás</span><span class="sxs-lookup"><span data-stu-id="c9747-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="c9747-126">A Lite telepítés a következő lehetőségeket tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="c9747-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="c9747-127">Projekttervezés a Microsoft Webes projekt segítségével</span><span class="sxs-lookup"><span data-stu-id="c9747-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="c9747-128">Többdimenziós árképzés</span><span class="sxs-lookup"><span data-stu-id="c9747-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="c9747-129">Egyesített erőforrás-kezelés</span><span class="sxs-lookup"><span data-stu-id="c9747-129">Unified Resource Management</span></span>
- <span data-ttu-id="c9747-130">Időkövetés</span><span class="sxs-lookup"><span data-stu-id="c9747-130">Time Tracking</span></span>
- <span data-ttu-id="c9747-131">Alapvető költség</span><span class="sxs-lookup"><span data-stu-id="c9747-131">Basic Expense</span></span>
- <span data-ttu-id="c9747-132">Számlajavaslat</span><span class="sxs-lookup"><span data-stu-id="c9747-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="c9747-133">Központi telepítési lépések</span><span class="sxs-lookup"><span data-stu-id="c9747-133">Deployment steps</span></span>
<span data-ttu-id="c9747-134">Határozza meg a Project Operations legjobb telepítési modelljét a [telepítési kérdőív](https://aka.ms/provisionprojectoperations) használatával.</span><span class="sxs-lookup"><span data-stu-id="c9747-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="c9747-135">Ehhez a telepítéshez lásd: [Regisztráció az előzetes verziós előfizetésekre](lite-preview-subscription-sign-up.md) és az [Új környezet kiépítése](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="c9747-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="c9747-136">Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez</span><span class="sxs-lookup"><span data-stu-id="c9747-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="c9747-137">A Project Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez az alábbi képességeket tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="c9747-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="c9747-138">Projekttervezés a Microsoft Webes projekt segítségével</span><span class="sxs-lookup"><span data-stu-id="c9747-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="c9747-139">Többdimenziós árképzés</span><span class="sxs-lookup"><span data-stu-id="c9747-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="c9747-140">Egyesített erőforrás-kezelés</span><span class="sxs-lookup"><span data-stu-id="c9747-140">Unified Resource Management</span></span>
- <span data-ttu-id="c9747-141">Időkövetés</span><span class="sxs-lookup"><span data-stu-id="c9747-141">Time Tracking</span></span>
- <span data-ttu-id="c9747-142">Alapvető költség</span><span class="sxs-lookup"><span data-stu-id="c9747-142">Basic Expense</span></span>
- <span data-ttu-id="c9747-143">Teljes költség</span><span class="sxs-lookup"><span data-stu-id="c9747-143">Full Expense</span></span>
- <span data-ttu-id="c9747-144">Bizonylat OCR</span><span class="sxs-lookup"><span data-stu-id="c9747-144">Receipt OCR</span></span>
- <span data-ttu-id="c9747-145">Teljes számlázás</span><span class="sxs-lookup"><span data-stu-id="c9747-145">Full Invoicing</span></span>
- <span data-ttu-id="c9747-146">Bevételfelismerés</span><span class="sxs-lookup"><span data-stu-id="c9747-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="c9747-147">Központi telepítési lépések</span><span class="sxs-lookup"><span data-stu-id="c9747-147">Deployment steps</span></span>
<span data-ttu-id="c9747-148">Határozza meg a Project Operations legjobb telepítési modelljét a [telepítési kérdőív](https://aka.ms/provisionprojectoperations) használatával.</span><span class="sxs-lookup"><span data-stu-id="c9747-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="c9747-149">Ehhez a telepítéshez lásd: [Regisztráció az előzetes verziós előfizetésekre](resource-sign-up-preview-subscription.md) és az [Új környezet kiépítése](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="c9747-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="c9747-150">Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez</span><span class="sxs-lookup"><span data-stu-id="c9747-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="c9747-151">Projekt tervezése WBS használatával</span><span class="sxs-lookup"><span data-stu-id="c9747-151">Project planning using WBS</span></span>
- <span data-ttu-id="c9747-152">Erőforráskezelés</span><span class="sxs-lookup"><span data-stu-id="c9747-152">Resource Management</span></span>
- <span data-ttu-id="c9747-153">Időkövetés</span><span class="sxs-lookup"><span data-stu-id="c9747-153">Time Tracking</span></span>
- <span data-ttu-id="c9747-154">Teljes költség</span><span class="sxs-lookup"><span data-stu-id="c9747-154">Full Expense</span></span>
- <span data-ttu-id="c9747-155">Bizonylat OCR</span><span class="sxs-lookup"><span data-stu-id="c9747-155">Receipt OCR</span></span>
- <span data-ttu-id="c9747-156">Teljes számlázás</span><span class="sxs-lookup"><span data-stu-id="c9747-156">Full Invoicing</span></span>
- <span data-ttu-id="c9747-157">Bevételfelismerés</span><span class="sxs-lookup"><span data-stu-id="c9747-157">Revenue Recognition</span></span>
- <span data-ttu-id="c9747-158">Termelési rendelések</span><span class="sxs-lookup"><span data-stu-id="c9747-158">Production Orders</span></span>
- <span data-ttu-id="c9747-159">Anyagok támogatása</span><span class="sxs-lookup"><span data-stu-id="c9747-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="c9747-160">Központi telepítési lépések</span><span class="sxs-lookup"><span data-stu-id="c9747-160">Deployment steps</span></span>
<span data-ttu-id="c9747-161">Határozza meg a Project Operations legjobb telepítési modelljét a [telepítési kérdőív](https://aka.ms/provisionprojectoperations) használatával.</span><span class="sxs-lookup"><span data-stu-id="c9747-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="c9747-162">Ehhez a telepítéshez lásd: [Regisztráció az előzetes verziós előfizetésekre](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) és az [Új környezet kiépítése](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="c9747-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

