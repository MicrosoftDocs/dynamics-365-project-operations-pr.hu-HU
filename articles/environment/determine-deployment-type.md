---
title: A telepítés típusának meghatározása
description: Ez a témakör a Project Operations az Ön vállalatának megfelelő telepítéstípusának megállapításában segítő információkat tartalmaz.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401221"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="0890b-103">A telepítés típusának meghatározása</span><span class="sxs-lookup"><span data-stu-id="0890b-103">Determine your deployment type</span></span>

<span data-ttu-id="0890b-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="0890b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0890b-105">Miután megvásárolta a licencet, kezdje itt a Dynamics 365 Project Operations legjobb telepítési modelljének meghatározásával az [Irányított telepítési folyamat](https://aka.ms/provisionprojectoperations) használatával.</span><span class="sxs-lookup"><span data-stu-id="0890b-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="0890b-106">Miután befejezte az Irányított telepítési folyamatot, a rendszer a helyes felügyeleti portálra irányítja a telepítés befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="0890b-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="0890b-107">A telepítés befejezéséhez tekintse meg a telepítés részleteit.</span><span class="sxs-lookup"><span data-stu-id="0890b-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="0890b-108">A Dynamics meglévő Dynamics 365 Project Service Automation rendszert használó ügyfelei</span><span class="sxs-lookup"><span data-stu-id="0890b-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="0890b-109">A Project Operations a Project Service Automation szolgáltatással szállított képességeket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0890b-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="0890b-110">A frissítés elérési úta 2021-es 1 kiadási hullámban jelennek meg az ügyfelek számára.</span><span class="sxs-lookup"><span data-stu-id="0890b-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="0890b-111">A Dynamics 365 Finance Projektmenedzsment és könyvelés alkalmazást használó meglévő ügyfelei</span><span class="sxs-lookup"><span data-stu-id="0890b-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="0890b-112">A projektmenedzsment és-számlázási funkciót használó meglévő Finance ügyfelek továbbra is használhatják azt.</span><span class="sxs-lookup"><span data-stu-id="0890b-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="0890b-113">Lásd: [Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez](#pma).</span><span class="sxs-lookup"><span data-stu-id="0890b-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="0890b-114">A központi telepítés típusai</span><span class="sxs-lookup"><span data-stu-id="0890b-114">Deployment types</span></span>
<span data-ttu-id="0890b-115">A Project Operations több telepítési lehetőséget is támogat, hogy megfeleljen az igényeinek.</span><span class="sxs-lookup"><span data-stu-id="0890b-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="0890b-116">Akár új, akár meglévő Dynamics 365-ügyfél, a Project Operations képes támogatni az igényeit.</span><span class="sxs-lookup"><span data-stu-id="0890b-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="0890b-117">A [telepítési kérdőívünk](https://aka.ms/provisionprojectoperations) segítséget nyújt a megfelelő telepítés meghatározásában.</span><span class="sxs-lookup"><span data-stu-id="0890b-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="0890b-118">Az eredmények a következő telepítési típusok egyike felé irányítják:</span><span class="sxs-lookup"><span data-stu-id="0890b-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="0890b-119">Egyszerű telepítés – proforma számlázás</span><span class="sxs-lookup"><span data-stu-id="0890b-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="0890b-120">Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez</span><span class="sxs-lookup"><span data-stu-id="0890b-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="0890b-121">Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez</span><span class="sxs-lookup"><span data-stu-id="0890b-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="0890b-122">A Project Operations a készletalapú/gyártási megrendeléseken alapuló forgatókönyveket és a nem készletalapú/erőforrásalapú forgatókönyveket támogatja ugyanazon környezetben, jogientitás-szintű konfigurációkon keresztül.</span><span class="sxs-lookup"><span data-stu-id="0890b-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="0890b-123">A Contoso például az Egyesült államokbeli gyártási létesítményben a készletezett/termelési rendelés funkcióit használhatja (Jogi személy = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="0890b-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="0890b-124">A Contoso a nem készletezett/erőforrás alapú lehetőségeket használhatja a Contoso Robotics Arms karbantartási létesítményében az Egyesült Királyságban (a jogi személy = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="0890b-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="0890b-125">Egyszerű telepítés – proforma számlázás</span><span class="sxs-lookup"><span data-stu-id="0890b-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="0890b-126">A Lite telepítés a következő lehetőségeket tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="0890b-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="0890b-127">A Dynamics 365 Sales alkalmazás tapasztalatait kibővítő projektek Értékesítési folyamata</span><span class="sxs-lookup"><span data-stu-id="0890b-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="0890b-128">Projekttervezés a Microsoft Webes projekt segítségével</span><span class="sxs-lookup"><span data-stu-id="0890b-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="0890b-129">Többdimenziós árképzés</span><span class="sxs-lookup"><span data-stu-id="0890b-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="0890b-130">Egyesített erőforrás-kezelés</span><span class="sxs-lookup"><span data-stu-id="0890b-130">Unified resource management</span></span>
- <span data-ttu-id="0890b-131">Időkövetés</span><span class="sxs-lookup"><span data-stu-id="0890b-131">Time tracking</span></span>
- <span data-ttu-id="0890b-132">Alapvető költség</span><span class="sxs-lookup"><span data-stu-id="0890b-132">Basic expense</span></span>
- <span data-ttu-id="0890b-133">Proforma és az ügyfél felé irányuló számlázás</span><span class="sxs-lookup"><span data-stu-id="0890b-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="0890b-134">Központi telepítési lépések</span><span class="sxs-lookup"><span data-stu-id="0890b-134">Deployment steps</span></span>
<span data-ttu-id="0890b-135">Határozza meg a Project Operations legjobb telepítési modelljét a [telepítési kérdőív](https://aka.ms/provisionprojectoperations) használatával.</span><span class="sxs-lookup"><span data-stu-id="0890b-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="0890b-136">Ehhez a telepítéshez lásd: [Regisztráció az előzetes verziós előfizetésekre](lite-preview-subscription-sign-up.md) és az [Új környezet kiépítése](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="0890b-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="0890b-137">Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez</span><span class="sxs-lookup"><span data-stu-id="0890b-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="0890b-138">A Project Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez az alábbi képességeket tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="0890b-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="0890b-139">A Dynamics 365 Sales alkalmazást kibővítő projektek Értékesítési folyamata</span><span class="sxs-lookup"><span data-stu-id="0890b-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="0890b-140">Projekttervezés a Microsoft Webes projekt segítségével</span><span class="sxs-lookup"><span data-stu-id="0890b-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="0890b-141">Többdimenziós árképzés</span><span class="sxs-lookup"><span data-stu-id="0890b-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="0890b-142">Egyesített erőforrás-kezelés</span><span class="sxs-lookup"><span data-stu-id="0890b-142">Unified resource management</span></span>
- <span data-ttu-id="0890b-143">Időkövetés</span><span class="sxs-lookup"><span data-stu-id="0890b-143">Time tracking</span></span>
- <span data-ttu-id="0890b-144">Alapvető költség</span><span class="sxs-lookup"><span data-stu-id="0890b-144">Basic expense</span></span>
- <span data-ttu-id="0890b-145">Teljes költség</span><span class="sxs-lookup"><span data-stu-id="0890b-145">Full expense</span></span>
- <span data-ttu-id="0890b-146">Bizonylat OCR</span><span class="sxs-lookup"><span data-stu-id="0890b-146">Receipt OCR</span></span>
- <span data-ttu-id="0890b-147">Proforma és az ügyfél felé irányuló számlázás</span><span class="sxs-lookup"><span data-stu-id="0890b-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="0890b-148">Bevétel elszámolása projektekhez</span><span class="sxs-lookup"><span data-stu-id="0890b-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="0890b-149">Központi telepítési lépések</span><span class="sxs-lookup"><span data-stu-id="0890b-149">Deployment steps</span></span>
<span data-ttu-id="0890b-150">Határozza meg a Project Operations legjobb telepítési modelljét a [telepítési kérdőív](https://aka.ms/provisionprojectoperations) használatával.</span><span class="sxs-lookup"><span data-stu-id="0890b-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="0890b-151">Ehhez a telepítéshez lásd: [Regisztráció az előzetes verziós előfizetésekre](resource-sign-up-preview-subscription.md) és az [Új környezet kiépítése](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="0890b-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="0890b-152">Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez</span><span class="sxs-lookup"><span data-stu-id="0890b-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="0890b-153">Projekt tervezése WBS használatával</span><span class="sxs-lookup"><span data-stu-id="0890b-153">Project planning using WBS</span></span>
- <span data-ttu-id="0890b-154">Erőforráskezelés</span><span class="sxs-lookup"><span data-stu-id="0890b-154">Resource Management</span></span>
- <span data-ttu-id="0890b-155">Időkövetés</span><span class="sxs-lookup"><span data-stu-id="0890b-155">Time Tracking</span></span>
- <span data-ttu-id="0890b-156">Teljes költség</span><span class="sxs-lookup"><span data-stu-id="0890b-156">Full Expense</span></span>
- <span data-ttu-id="0890b-157">Bizonylat OCR</span><span class="sxs-lookup"><span data-stu-id="0890b-157">Receipt OCR</span></span>
- <span data-ttu-id="0890b-158">Teljes számlázás</span><span class="sxs-lookup"><span data-stu-id="0890b-158">Full Invoicing</span></span>
- <span data-ttu-id="0890b-159">Bevételfelismerés</span><span class="sxs-lookup"><span data-stu-id="0890b-159">Revenue Recognition</span></span>
- <span data-ttu-id="0890b-160">Termelési rendelések</span><span class="sxs-lookup"><span data-stu-id="0890b-160">Production Orders</span></span>
- <span data-ttu-id="0890b-161">Anyagok támogatása</span><span class="sxs-lookup"><span data-stu-id="0890b-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="0890b-162">Központi telepítési lépések</span><span class="sxs-lookup"><span data-stu-id="0890b-162">Deployment steps</span></span>
<span data-ttu-id="0890b-163">Határozza meg a Project Operations legjobb telepítési modelljét a [telepítési kérdőív](https://aka.ms/provisionprojectoperations) használatával.</span><span class="sxs-lookup"><span data-stu-id="0890b-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="0890b-164">Ehhez a telepítéshez lásd: [Regisztráció az előzetes verziós előfizetésekre](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) és az [Új környezet kiépítése](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="0890b-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

