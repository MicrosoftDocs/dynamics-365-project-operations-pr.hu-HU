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
ms.openlocfilehash: 2da6af3240d8e561d01b1fcd8d32b657dbac1588
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479567"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="c32df-103">A telepítés típusának meghatározása</span><span class="sxs-lookup"><span data-stu-id="c32df-103">Determine your deployment type</span></span>

<span data-ttu-id="c32df-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="c32df-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c32df-105">A licenc vásárlása után kezdje el itt meghatározni a Dynamics 365 Project Operations központi telepítési modelljét az [Irányított telepítési folyamat](https://aka.ms/provisionprojectoperations) használatával.</span><span class="sxs-lookup"><span data-stu-id="c32df-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="c32df-106">Miután befejezte az Irányított telepítési folyamatot, a rendszer a helyes felügyeleti portálra irányítja a telepítés befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="c32df-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="c32df-107">A telepítés befejezéséhez tekintse meg a telepítés részleteit.</span><span class="sxs-lookup"><span data-stu-id="c32df-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="c32df-108">A Dynamics meglévő Dynamics 365 Project Service Automation rendszert használó ügyfelei</span><span class="sxs-lookup"><span data-stu-id="c32df-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="c32df-109">A Project Operations a Project Service Automation szolgáltatással szállított képességeket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c32df-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="c32df-110">A frissítés elérési úta 2021-es 1 kiadási hullámban jelennek meg az ügyfelek számára.</span><span class="sxs-lookup"><span data-stu-id="c32df-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="c32df-111">A Dynamics 365 Finance Projektmenedzsment és könyvelés alkalmazást használó meglévő ügyfelei</span><span class="sxs-lookup"><span data-stu-id="c32df-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="c32df-112">A projektmenedzsment és-számlázási funkciót használó meglévő Finance ügyfelek továbbra is használhatják azt.</span><span class="sxs-lookup"><span data-stu-id="c32df-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="c32df-113">Lásd: [Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez](#pma).</span><span class="sxs-lookup"><span data-stu-id="c32df-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-regions"></a><span data-ttu-id="c32df-114">Központi telepítési régiók</span><span class="sxs-lookup"><span data-stu-id="c32df-114">Deployment regions</span></span>
<span data-ttu-id="c32df-115">Annak meghatározásához, hogy mely régiók támogatják a Project Operations központi telepítlését, lásd: [Földrajzi elérhetőség a Dynamics 365 és a Power Platform jelentés esetében](https://dynamics.microsoft.com/en-us/geographic-availability/).</span><span class="sxs-lookup"><span data-stu-id="c32df-115">To determine which regions support Project Operations deployment, see [Geographical availability for Dynamics 365 and Power Platform report](https://dynamics.microsoft.com/en-us/geographic-availability/).</span></span> <span data-ttu-id="c32df-116">Válassza a **Jelentés megtekintése** lehetőséget, majd a támogatott régiók megtekintéséhez bontsa ki a **Dynamics 365 > Operations Apps > Dynamics 365 Project Operations** alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="c32df-116">Select **View Report**, and expand **Dynamics 365 > Operations Apps > Dynamics 365 Project Operations** to view the supported regions.</span></span>

## <a name="deployment-types"></a><span data-ttu-id="c32df-117">A központi telepítés típusai</span><span class="sxs-lookup"><span data-stu-id="c32df-117">Deployment types</span></span>
<span data-ttu-id="c32df-118">A Project Operations több telepítési lehetőséget is támogat, hogy megfeleljen az igényeinek.</span><span class="sxs-lookup"><span data-stu-id="c32df-118">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="c32df-119">Akár új, akár meglévő Dynamics 365-ügyfél, a Project Operations képes támogatni az igényeit.</span><span class="sxs-lookup"><span data-stu-id="c32df-119">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="c32df-120">A [telepítési kérdőívünk](https://aka.ms/provisionprojectoperations) segítséget nyújt a megfelelő telepítés meghatározásában.</span><span class="sxs-lookup"><span data-stu-id="c32df-120">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="c32df-121">Az eredmények a következő telepítési típusok egyike felé irányítják:</span><span class="sxs-lookup"><span data-stu-id="c32df-121">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="c32df-122">Egyszerű telepítés – proforma számlázás</span><span class="sxs-lookup"><span data-stu-id="c32df-122">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="c32df-123">Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez</span><span class="sxs-lookup"><span data-stu-id="c32df-123">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="c32df-124">Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez</span><span class="sxs-lookup"><span data-stu-id="c32df-124">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="c32df-125">A Project Operations a készletalapú/gyártási megrendeléseken alapuló forgatókönyveket és a nem készletalapú/erőforrásalapú forgatókönyveket támogatja ugyanazon környezetben, jogientitás-szintű konfigurációkon keresztül.</span><span class="sxs-lookup"><span data-stu-id="c32df-125">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="c32df-126">A Contoso például az Egyesült államokbeli gyártási létesítményben a készletezett/termelési rendelés funkcióit használhatja (Jogi személy = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="c32df-126">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="c32df-127">A Contoso a nem készletezett/erőforrás alapú lehetőségeket használhatja a Contoso Robotics Arms karbantartási létesítményében az Egyesült Királyságban (a jogi személy = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="c32df-127">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="c32df-128">Egyszerű telepítés – proforma számlázás</span><span class="sxs-lookup"><span data-stu-id="c32df-128">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="c32df-129">A Lite telepítés a következő lehetőségeket tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="c32df-129">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="c32df-130">A Dynamics 365 Sales alkalmazás tapasztalatait kibővítő projektek Értékesítési folyamata</span><span class="sxs-lookup"><span data-stu-id="c32df-130">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="c32df-131">Projekttervezés a Microsoft Webes projekt segítségével</span><span class="sxs-lookup"><span data-stu-id="c32df-131">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="c32df-132">Többdimenziós árképzés</span><span class="sxs-lookup"><span data-stu-id="c32df-132">Multi-dimensional pricing</span></span>
- <span data-ttu-id="c32df-133">Egyesített erőforrás-kezelés</span><span class="sxs-lookup"><span data-stu-id="c32df-133">Unified resource management</span></span>
- <span data-ttu-id="c32df-134">Időkövetés</span><span class="sxs-lookup"><span data-stu-id="c32df-134">Time tracking</span></span>
- <span data-ttu-id="c32df-135">Alapvető költség</span><span class="sxs-lookup"><span data-stu-id="c32df-135">Basic expense</span></span>
- <span data-ttu-id="c32df-136">Proforma és az ügyfél felé irányuló számlázás</span><span class="sxs-lookup"><span data-stu-id="c32df-136">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="c32df-137">Központi telepítési lépések</span><span class="sxs-lookup"><span data-stu-id="c32df-137">Deployment steps</span></span>
<span data-ttu-id="c32df-138">Határozza meg a Project Operations legjobb telepítési modelljét a [telepítési kérdőív](https://aka.ms/provisionprojectoperations) használatával.</span><span class="sxs-lookup"><span data-stu-id="c32df-138">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="c32df-139">Ehhez a telepítéshez lásd: [Regisztráció az előzetes verziós előfizetésekre](lite-preview-subscription-sign-up.md) és az [Új környezet kiépítése](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="c32df-139">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="c32df-140">Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez</span><span class="sxs-lookup"><span data-stu-id="c32df-140">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="c32df-141">A Project Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez az alábbi képességeket tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="c32df-141">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="c32df-142">A Dynamics 365 Sales alkalmazást kibővítő projektek Értékesítési folyamata</span><span class="sxs-lookup"><span data-stu-id="c32df-142">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="c32df-143">Projekttervezés a Microsoft Webes projekt segítségével</span><span class="sxs-lookup"><span data-stu-id="c32df-143">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="c32df-144">Többdimenziós árképzés</span><span class="sxs-lookup"><span data-stu-id="c32df-144">Multi-dimensional pricing</span></span>
- <span data-ttu-id="c32df-145">Egyesített erőforrás-kezelés</span><span class="sxs-lookup"><span data-stu-id="c32df-145">Unified resource management</span></span>
- <span data-ttu-id="c32df-146">Időkövetés</span><span class="sxs-lookup"><span data-stu-id="c32df-146">Time tracking</span></span>
- <span data-ttu-id="c32df-147">Alapvető költség</span><span class="sxs-lookup"><span data-stu-id="c32df-147">Basic expense</span></span>
- <span data-ttu-id="c32df-148">Teljes költség</span><span class="sxs-lookup"><span data-stu-id="c32df-148">Full expense</span></span>
- <span data-ttu-id="c32df-149">Bizonylat OCR</span><span class="sxs-lookup"><span data-stu-id="c32df-149">Receipt OCR</span></span>
- <span data-ttu-id="c32df-150">Proforma és az ügyfél felé irányuló számlázás</span><span class="sxs-lookup"><span data-stu-id="c32df-150">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="c32df-151">Bevétel elszámolása projektekhez</span><span class="sxs-lookup"><span data-stu-id="c32df-151">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="c32df-152">Központi telepítési lépések</span><span class="sxs-lookup"><span data-stu-id="c32df-152">Deployment steps</span></span>
<span data-ttu-id="c32df-153">Határozza meg a Project Operations legjobb telepítési modelljét a [telepítési kérdőív](https://aka.ms/provisionprojectoperations) használatával.</span><span class="sxs-lookup"><span data-stu-id="c32df-153">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="c32df-154">Ehhez a telepítéshez lásd: [Regisztráció az előzetes verziós előfizetésekre](resource-sign-up-preview-subscription.md) és az [Új környezet kiépítése](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="c32df-154">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="c32df-155">Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez</span><span class="sxs-lookup"><span data-stu-id="c32df-155">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="c32df-156">Projekt tervezése WBS használatával</span><span class="sxs-lookup"><span data-stu-id="c32df-156">Project planning using WBS</span></span>
- <span data-ttu-id="c32df-157">Erőforráskezelés</span><span class="sxs-lookup"><span data-stu-id="c32df-157">Resource Management</span></span>
- <span data-ttu-id="c32df-158">Időkövetés</span><span class="sxs-lookup"><span data-stu-id="c32df-158">Time Tracking</span></span>
- <span data-ttu-id="c32df-159">Teljes költség</span><span class="sxs-lookup"><span data-stu-id="c32df-159">Full Expense</span></span>
- <span data-ttu-id="c32df-160">Bizonylat OCR</span><span class="sxs-lookup"><span data-stu-id="c32df-160">Receipt OCR</span></span>
- <span data-ttu-id="c32df-161">Teljes számlázás</span><span class="sxs-lookup"><span data-stu-id="c32df-161">Full Invoicing</span></span>
- <span data-ttu-id="c32df-162">Bevételfelismerés</span><span class="sxs-lookup"><span data-stu-id="c32df-162">Revenue Recognition</span></span>
- <span data-ttu-id="c32df-163">Termelési rendelések</span><span class="sxs-lookup"><span data-stu-id="c32df-163">Production Orders</span></span>
- <span data-ttu-id="c32df-164">Anyagok támogatása</span><span class="sxs-lookup"><span data-stu-id="c32df-164">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="c32df-165">Központi telepítési lépések</span><span class="sxs-lookup"><span data-stu-id="c32df-165">Deployment steps</span></span>
<span data-ttu-id="c32df-166">Határozza meg a Project Operations legjobb telepítési modelljét a [telepítési kérdőív](https://aka.ms/provisionprojectoperations) használatával.</span><span class="sxs-lookup"><span data-stu-id="c32df-166">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="c32df-167">Ehhez a telepítéshez lásd: [Regisztráció az előzetes verziós előfizetésekre](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) és az [Új környezet kiépítése](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="c32df-167">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
