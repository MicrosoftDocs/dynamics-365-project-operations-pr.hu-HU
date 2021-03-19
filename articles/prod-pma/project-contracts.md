---
title: Projektszerződések
description: Ez a témakör példákat tartalmaz a különféle típusú projektekhez és finanszírozási forrásokhoz létrehozható projektszerződésekre, valamint a szerződések kezelésére és a projektügyfeleknek történő számlázásra.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b53eb6ff3f98e7efc3d6b997cd4d877025225936
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289552"
---
# <a name="project-contracts"></a><span data-ttu-id="fdc78-103">Projektszerződések</span><span class="sxs-lookup"><span data-stu-id="fdc78-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fdc78-104">Ez a cikk példákat tartalmaz a különféle típusú projektekhez és finanszírozási forrásokhoz létrehozható projektszerződésekre, valamint a szerződések kezelésére és a projektügyfeleknek történő számlázásra.</span><span class="sxs-lookup"><span data-stu-id="fdc78-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="fdc78-105">A projektszerződéshez létrehozott projekt típusa határozza meg a projektügyfelek esetében alkalmazott számlázási módot.</span><span class="sxs-lookup"><span data-stu-id="fdc78-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="fdc78-106">A projektszerződések és a kapcsolódó projektek módosíthatók, de a projekttípus nem.</span><span class="sxs-lookup"><span data-stu-id="fdc78-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="fdc78-107">A projektszerződések használatával egyszerre számlázhat egy vagy több projektet.</span><span class="sxs-lookup"><span data-stu-id="fdc78-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="fdc78-108">A projektszerződés segít továbbá a projekt struktúrájában szereplő összes alprojekt egységes számlázási eljárásának biztosításában.</span><span class="sxs-lookup"><span data-stu-id="fdc78-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="fdc78-109">Minden számlázásra kerülő projektet egy projektszerződéshez kell társítani.</span><span class="sxs-lookup"><span data-stu-id="fdc78-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="fdc78-110">A projektszerződés beállításai a projektszerződéshez társított összes projektre és alprojektre vonatkoznak.</span><span class="sxs-lookup"><span data-stu-id="fdc78-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="fdc78-111">A projektszerződések egy vagy több finanszírozási forrást is meghatározhatnak.</span><span class="sxs-lookup"><span data-stu-id="fdc78-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="fdc78-112">Ezért feloszthatja a számlázási több finanszírozói között, beállíthat finanszírozási korlátokat, hogy a finanszírozási források esetében egy megadott összeget ne lépjen túl a számlázás, és konfigurálhatja a kiadások felszámítására vonatkozó finanszírozási szabályok.</span><span class="sxs-lookup"><span data-stu-id="fdc78-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="fdc78-113">Projektszerződések finanszírozása</span><span class="sxs-lookup"><span data-stu-id="fdc78-113">Funding for project contracts</span></span>
<span data-ttu-id="fdc78-114">Egyes projektszerződések azt határozzák meg, hogy több fél osztozik a felelősségen a projekt költségeinek finanszírozása terén.</span><span class="sxs-lookup"><span data-stu-id="fdc78-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="fdc78-115">Íme néhány példa:</span><span class="sxs-lookup"><span data-stu-id="fdc78-115">Here are some examples:</span></span>

-   <span data-ttu-id="fdc78-116">A több divíziót tartalmazó nagy ügyfél azt kéri, hogy a projektek finanszírozása divíziók szerint legyen megosztva.</span><span class="sxs-lookup"><span data-stu-id="fdc78-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="fdc78-117">A vállalat egy nagy projekt költségeit egy külső szervezettel osztja meg.</span><span class="sxs-lookup"><span data-stu-id="fdc78-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="fdc78-118">Egy közúti projektet két önkormányzat társfinanszíroz.</span><span class="sxs-lookup"><span data-stu-id="fdc78-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="fdc78-119">Egy hídprojektet kormányzati támogatás és egy magánvállalat finanszíroz.</span><span class="sxs-lookup"><span data-stu-id="fdc78-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="fdc78-120">A Dynamics 365 Finance alkalmazásban egyetlen tranzakció vagy egy teljes projekt számlázását feloszthatja több ügyfél, támogatás vagy szervezet között.</span><span class="sxs-lookup"><span data-stu-id="fdc78-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="fdc78-121">A több finanszírozóval rendelkező projektek esetében a speciális finanszírozási projekt finanszírozásához hozzájáruló feleket finanszírozási forrásoknak nevezik.</span><span class="sxs-lookup"><span data-stu-id="fdc78-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="fdc78-122">Az ügyfél, szervezet vagy támogatás finanszírozási forrásként való meghatározása után egy vagy több finanszírozási szabályhoz rendelhető hozzá.</span><span class="sxs-lookup"><span data-stu-id="fdc78-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="fdc78-123">A finanszírozási szabályok tartalmazzák azokat a feltételeket, amelyek meghatározzák, hogy a felszámított költségek hogyan vannak kiosztva a projektek különböző finanszírozási forrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="fdc78-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="fdc78-124">Mivel a készletezett cikkek – például a beszerzési igénylésekben és a beszerzési rendeléseken megjelenő elemek – nem oszthatók szét, a költség összege nem osztható szét több finanszírozási forrás között a terjesztés időpontjában.</span><span class="sxs-lookup"><span data-stu-id="fdc78-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="fdc78-125">A finanszírozási forrás értéke ezért 0 (nulla) marad a készletkiadás könyveléséig.</span><span class="sxs-lookup"><span data-stu-id="fdc78-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="fdc78-126">A készlet kiadásának könyvelésekor a program a költségösszeget a projekt partnerek közötti felosztási szabályainak megfelelően felosztja.</span><span class="sxs-lookup"><span data-stu-id="fdc78-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="fdc78-127">Az alábbiakban néhány lépést mutatunk be, amelyek végrehajtásával megkönnyítheti a számlázás több finanszírozási forrás közötti felosztását:</span><span class="sxs-lookup"><span data-stu-id="fdc78-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="fdc78-128">Adja meg, hogy a projekthez bevitt összes tranzakció ugyanazt az értékesítési pénznemet használja, mint a projektszerződés.</span><span class="sxs-lookup"><span data-stu-id="fdc78-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="fdc78-129">Állítson be finanszírozási korlátokat, hogy egy finanszírozási forrás irányában egy adott összegnél több ne legyen kiszámlázva a projekttel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="fdc78-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="fdc78-130">Konfigurálja a finanszírozási szabályokat és a finanszírozási korlátozásokat az egyes dolgozók, cikkek, kategóriák, kategóriacsoportok és tranzakciótípusok esetén (vagy minden tranzakciótípus esetén).</span><span class="sxs-lookup"><span data-stu-id="fdc78-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="fdc78-131">Válasszon ki opcionális kezdő és záró dátumokat az egyes finanszírozási szabályok érvényességi idejének meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="fdc78-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="fdc78-132">Határozza meg az egyes finanszírozási források felelősségének százalékos arányát.</span><span class="sxs-lookup"><span data-stu-id="fdc78-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="fdc78-133">Határozza meg, hogy melyik finanszírozási forrás felelős a finanszírozási allokációs számítások miatti kerekítési különbségekért.</span><span class="sxs-lookup"><span data-stu-id="fdc78-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="fdc78-134">Állítson be szabályokat, amelyek meghatározzák, hogy a projekt költségei hogyan kerülnek kiszámlázásra a külső ügyfelek számára, és hogyan kerülnek felszámításra a belső szervezetek számára.</span><span class="sxs-lookup"><span data-stu-id="fdc78-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="fdc78-135">Rögzítse a tranzakciókat egy visszatartott finanszírozási számlán, amíg további finanszírozás nem szerezhető, vagy amíg úgy nem dönt, hogy a költségeket belsőleg viseli.</span><span class="sxs-lookup"><span data-stu-id="fdc78-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="fdc78-136">Annak megállapításához, hogy mely adócsoport társítandó egy tranzakcióhoz, a rendszer egy adócsoport-hozzárendelést keres a projektben.</span><span class="sxs-lookup"><span data-stu-id="fdc78-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="fdc78-137">Ha a projekt szintjén nem történt meg az adócsoport-hozzárendelés, a program a projektszerződésben keres.</span><span class="sxs-lookup"><span data-stu-id="fdc78-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="fdc78-138">Példa: Több finanszírozási forrás (egyszerű)</span><span class="sxs-lookup"><span data-stu-id="fdc78-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="fdc78-139">A következő táblázat a több finanszírozási forrás közötti finanszírozásfelosztás kezelésére szolgáló forgatókönyveket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="fdc78-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="fdc78-140">Ezek a forgatókönyvek a következő feltételezéseken alapulnak:</span><span class="sxs-lookup"><span data-stu-id="fdc78-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="fdc78-141">A prioritási beállításokat a rendszer figyelembe veszi a pénzösszegek felosztásában a finanszírozási szabályok egyéb feltételeinek alkalmazása előtt.</span><span class="sxs-lookup"><span data-stu-id="fdc78-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="fdc78-142">Nincs megadva dátumtartomány a d időszak meghatározására, amikor a finanszírozási szabály érvényes.</span><span class="sxs-lookup"><span data-stu-id="fdc78-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fdc78-143"><strong>Forgatókönyv</strong></span><span class="sxs-lookup"><span data-stu-id="fdc78-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="fdc78-144"><strong>Finanszírozási forrás</strong></span><span class="sxs-lookup"><span data-stu-id="fdc78-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="fdc78-145"><strong>Felosztási százalék</strong></span><span class="sxs-lookup"><span data-stu-id="fdc78-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="fdc78-146"><strong>Felosztás prioritása</strong></span><span class="sxs-lookup"><span data-stu-id="fdc78-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdc78-147">A költségeket csak egy finanszírozási forráshoz kívánja felosztani, amíg a pénzösszegei ki nem merülnek, ezután a költségeket a második finanszírozási forráshoz osztja fel, amíg a pénzösszegei ki nem merülnek, majd végül a fennmaradó költségeket egy harmadik finanszírozási forráshoz osztja fel.</span><span class="sxs-lookup"><span data-stu-id="fdc78-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="fdc78-148">1. finanszírozási forrás</span><span class="sxs-lookup"><span data-stu-id="fdc78-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="fdc78-149">2. finanszírozási forrás</span><span class="sxs-lookup"><span data-stu-id="fdc78-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="fdc78-150">3. finanszírozási forrás</span><span class="sxs-lookup"><span data-stu-id="fdc78-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fdc78-151">100%</span><span class="sxs-lookup"><span data-stu-id="fdc78-151">100%</span></span></li>
<li><span data-ttu-id="fdc78-152">100%</span><span class="sxs-lookup"><span data-stu-id="fdc78-152">100%</span></span></li>
<li><span data-ttu-id="fdc78-153">100%</span><span class="sxs-lookup"><span data-stu-id="fdc78-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fdc78-154">0</span><span class="sxs-lookup"><span data-stu-id="fdc78-154">1</span></span></li>
<li><span data-ttu-id="fdc78-155">2</span><span class="sxs-lookup"><span data-stu-id="fdc78-155">2</span></span></li>
<li><span data-ttu-id="fdc78-156">3</span><span class="sxs-lookup"><span data-stu-id="fdc78-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdc78-157">A költségek 75 százalékát egy finanszírozási forráshoz, 25 százalékát pedig egy második finanszírozási forráshoz kívánja felosztani.</span><span class="sxs-lookup"><span data-stu-id="fdc78-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="fdc78-158">Ha a finanszírozási források bármelyike kimerül, a fennmaradó költségeket egy harmadik finanszírozási forrásból kívánja fizetni.</span><span class="sxs-lookup"><span data-stu-id="fdc78-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="fdc78-159">1. finanszírozási forrás</span><span class="sxs-lookup"><span data-stu-id="fdc78-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="fdc78-160">2. finanszírozási forrás</span><span class="sxs-lookup"><span data-stu-id="fdc78-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="fdc78-161">3. finanszírozási forrás</span><span class="sxs-lookup"><span data-stu-id="fdc78-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fdc78-162">75%</span><span class="sxs-lookup"><span data-stu-id="fdc78-162">75%</span></span></li>
<li><span data-ttu-id="fdc78-163">25%</span><span class="sxs-lookup"><span data-stu-id="fdc78-163">25%</span></span></li>
<li><span data-ttu-id="fdc78-164">100%</span><span class="sxs-lookup"><span data-stu-id="fdc78-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fdc78-165">0</span><span class="sxs-lookup"><span data-stu-id="fdc78-165">1</span></span></li>
<li><span data-ttu-id="fdc78-166">0</span><span class="sxs-lookup"><span data-stu-id="fdc78-166">1</span></span></li>
<li><span data-ttu-id="fdc78-167">2</span><span class="sxs-lookup"><span data-stu-id="fdc78-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdc78-168">A költségek 75 százalékát egy finanszírozási forráshoz, 25 százalékát pedig egy második finanszírozási forráshoz kívánja felosztani.</span><span class="sxs-lookup"><span data-stu-id="fdc78-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="fdc78-169">Ha a finanszírozási források bármelyike kimerül, a fennmaradó költségeket egy harmadik finanszírozási forrás és egy negyedik finanszírozási forrás között kívánja felosztani.</span><span class="sxs-lookup"><span data-stu-id="fdc78-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="fdc78-170">1. finanszírozási forrás</span><span class="sxs-lookup"><span data-stu-id="fdc78-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="fdc78-171">2. finanszírozási forrás</span><span class="sxs-lookup"><span data-stu-id="fdc78-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="fdc78-172">3. finanszírozási forrás</span><span class="sxs-lookup"><span data-stu-id="fdc78-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="fdc78-173">4. finanszírozási forrás</span><span class="sxs-lookup"><span data-stu-id="fdc78-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fdc78-174">75%</span><span class="sxs-lookup"><span data-stu-id="fdc78-174">75%</span></span></li>
<li><span data-ttu-id="fdc78-175">25%</span><span class="sxs-lookup"><span data-stu-id="fdc78-175">25%</span></span></li>
<li><span data-ttu-id="fdc78-176">50%</span><span class="sxs-lookup"><span data-stu-id="fdc78-176">50%</span></span></li>
<li><span data-ttu-id="fdc78-177">50%</span><span class="sxs-lookup"><span data-stu-id="fdc78-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fdc78-178">0</span><span class="sxs-lookup"><span data-stu-id="fdc78-178">1</span></span></li>
<li><span data-ttu-id="fdc78-179">0</span><span class="sxs-lookup"><span data-stu-id="fdc78-179">1</span></span></li>
<li><span data-ttu-id="fdc78-180">2</span><span class="sxs-lookup"><span data-stu-id="fdc78-180">2</span></span></li>
<li><span data-ttu-id="fdc78-181">2</span><span class="sxs-lookup"><span data-stu-id="fdc78-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdc78-182">A költségek 25 százalékát egy finanszírozási forráshoz, a maradékot pedig egy második finanszírozási forráshoz kívánja felosztani.</span><span class="sxs-lookup"><span data-stu-id="fdc78-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="fdc78-183">1. finanszírozási forrás</span><span class="sxs-lookup"><span data-stu-id="fdc78-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="fdc78-184">2. finanszírozási forrás</span><span class="sxs-lookup"><span data-stu-id="fdc78-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fdc78-185">25%</span><span class="sxs-lookup"><span data-stu-id="fdc78-185">25%</span></span></li>
<li><span data-ttu-id="fdc78-186">100%</span><span class="sxs-lookup"><span data-stu-id="fdc78-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fdc78-187">0</span><span class="sxs-lookup"><span data-stu-id="fdc78-187">1</span></span></li>
<li><span data-ttu-id="fdc78-188">2</span><span class="sxs-lookup"><span data-stu-id="fdc78-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="fdc78-189">Példa: Több finanszírozási forrás (összetett)</span><span class="sxs-lookup"><span data-stu-id="fdc78-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="fdc78-190">Három finanszírozási forrással rendelkezik, amelyeket a következő sorrendben szeretné használni:</span><span class="sxs-lookup"><span data-stu-id="fdc78-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="fdc78-191">A 2. finanszírozási forrást és a 3. finanszírozási forrást egyenlően használja, amíg a 2. finanszírozási forrást ki nem merül.</span><span class="sxs-lookup"><span data-stu-id="fdc78-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="fdc78-192">Folytatja a 3. finanszírozási forrás használatát, amíg az ki nem merül.</span><span class="sxs-lookup"><span data-stu-id="fdc78-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="fdc78-193">Az 1. finanszírozási forrást használja, miután a 3. finanszírozási forrást kimerül.</span><span class="sxs-lookup"><span data-stu-id="fdc78-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="fdc78-194">Ennek a célnak a teljesítéséhez az alábbiakat kell végrehajtania:</span><span class="sxs-lookup"><span data-stu-id="fdc78-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="fdc78-195">Finanszírozási korlátokat kell beállítania a 2. finanszírozási forrás és a 3. finanszírozási forrás számára a megfelelő összegekkel.</span><span class="sxs-lookup"><span data-stu-id="fdc78-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="fdc78-196">Hozz létre a következő finanszírozási szabályt::</span><span class="sxs-lookup"><span data-stu-id="fdc78-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="fdc78-197">1. szabály (1. prioritás): Ossza fel a tranzakciók 50 százalékát a 2. finanszírozási forráshoz, és 50 százalékát a 3. finanszírozási forráshoz.</span><span class="sxs-lookup"><span data-stu-id="fdc78-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="fdc78-198">2. szabály (2. prioritás): Ossza fel a tranzakciók 100 százalékát a 3. finanszírozási forráshoz.</span><span class="sxs-lookup"><span data-stu-id="fdc78-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="fdc78-199">3. szabály (3. prioritás): Ossza fel a tranzakciók 100 százalékát az 1. finanszírozási forráshoz.</span><span class="sxs-lookup"><span data-stu-id="fdc78-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="fdc78-200">Ez a beállítás azért működik, mert a rendszer ellenőrzi a tranzakciókat a szabályok és a korlátozások alapján, hogy ezek közül bármelyik a tranzakcióra vonatkozik-e.</span><span class="sxs-lookup"><span data-stu-id="fdc78-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="fdc78-201">Ha a tranzakcióra nem érvényesek konkrét szabályok vagy korlátozások, a Minden tranzakció szabály érvényes.</span><span class="sxs-lookup"><span data-stu-id="fdc78-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="fdc78-202">A Minden tranzakció szabály minden tranzakcióra érvényes.</span><span class="sxs-lookup"><span data-stu-id="fdc78-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="fdc78-203">Ha a rendszer egy olyan szabályt talál, amely megfelel egy tranzakciónak, akkor először a szabályban lefoglalt százalékértéket alkalmazza, de csak azután, hogy az egyezések esetében ellenőrizte a beállított korlátokat.</span><span class="sxs-lookup"><span data-stu-id="fdc78-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="fdc78-204">Ha a költségek elérik a korlátot, és a finanszírozási forrás pénzösszegei kimerültek, a finanszírozási korlátozáshoz kapcsolódó finanszírozási szabály figyelmen kívül marad, és a program ellenőrzi a következő vonatkozó szabályt.</span><span class="sxs-lookup"><span data-stu-id="fdc78-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="fdc78-205">Bizonyos esetekben a tranzakciónak csak egy része osztható fel egy szabály értelmében.</span><span class="sxs-lookup"><span data-stu-id="fdc78-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="fdc78-206">Ez azért fordulhat elő, mert a tranzakció felosztásakor a költség eléri a korlátot.</span><span class="sxs-lookup"><span data-stu-id="fdc78-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="fdc78-207">Ebben az esetben csak bizonyos összeg kerül felosztásra az adott szabály szerint, például 50 százalék az egyes finanszírozási forrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="fdc78-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="fdc78-208">Ez az az eset az 1. szabályban, amelyet a fejezet korábban ismertet.</span><span class="sxs-lookup"><span data-stu-id="fdc78-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="fdc78-209">A maradékot a program a sorban következő szabály szerint osztja fel.</span><span class="sxs-lookup"><span data-stu-id="fdc78-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="fdc78-210">A következő táblázat részletesebben megvizsgálja ezt a forgatókönyvet.</span><span class="sxs-lookup"><span data-stu-id="fdc78-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fdc78-211"><strong>Fókusz</strong></span><span class="sxs-lookup"><span data-stu-id="fdc78-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="fdc78-212"><strong>Részletek</strong></span><span class="sxs-lookup"><span data-stu-id="fdc78-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdc78-213">Finanszírozási szabályok</span><span class="sxs-lookup"><span data-stu-id="fdc78-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="fdc78-214">1. szabály (1. prioritás): Minden tranzakció.</span><span class="sxs-lookup"><span data-stu-id="fdc78-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="fdc78-215">Felosztás a 2. finanszírozási forrásra 50%-ban és a 3 finanszírozási forrásra 50%-ban.</span><span class="sxs-lookup"><span data-stu-id="fdc78-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="fdc78-216">2. szabály (2. prioritás): Minden tranzakció.</span><span class="sxs-lookup"><span data-stu-id="fdc78-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="fdc78-217">Felosztás a 3. finanszírozási forrásra 100%-ban.</span><span class="sxs-lookup"><span data-stu-id="fdc78-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="fdc78-218">3. szabály (2. prioritás): Minden tranzakció.</span><span class="sxs-lookup"><span data-stu-id="fdc78-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="fdc78-219">Felosztás az 1. finanszírozási forrásra 100%-ban.</span><span class="sxs-lookup"><span data-stu-id="fdc78-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdc78-220">Finanszírozási korlátozások</span><span class="sxs-lookup"><span data-stu-id="fdc78-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="fdc78-221">1. finanszírozási forrás korlátja = 10 000,00</span><span class="sxs-lookup"><span data-stu-id="fdc78-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="fdc78-222">2. finanszírozási forrás korlátja = 500,00</span><span class="sxs-lookup"><span data-stu-id="fdc78-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="fdc78-223">3. finanszírozási forrás korlátja = 750,00</span><span class="sxs-lookup"><span data-stu-id="fdc78-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdc78-224">1. tranzakció</span><span class="sxs-lookup"><span data-stu-id="fdc78-224">Transaction 1</span></span></td>
<td><span data-ttu-id="fdc78-225"><strong>Tranzakció összege:</strong> 100,00<strong>Finanszírozás:</strong> A tranzakció csak az 1. szabály szerint kerül kifizetésre, mert a tranzakció teljes mértékben ki van fizetve az 1. szabály alkalmazása után.</span><span class="sxs-lookup"><span data-stu-id="fdc78-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="fdc78-226">A tranzakciót egyformán finanszírozza a 2. finanszírozási forrás és a 3. finanszírozási forrás.</span><span class="sxs-lookup"><span data-stu-id="fdc78-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="fdc78-227">2. finanszírozási forrás: 50,00</span><span class="sxs-lookup"><span data-stu-id="fdc78-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="fdc78-228">3. finanszírozási forrás: 50,00</span><span class="sxs-lookup"><span data-stu-id="fdc78-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdc78-229">2. tranzakció</span><span class="sxs-lookup"><span data-stu-id="fdc78-229">Transaction 2</span></span></td>
<td><span data-ttu-id="fdc78-230"><strong>Tranzakció összege:</strong> 5000,00<strong>Finanszírozás:</strong> A tranzakció mindhárom szabály szerint kerül kifizetésre.</span><span class="sxs-lookup"><span data-stu-id="fdc78-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="fdc78-231"><strong>1. szabály</strong>
</span><span class="sxs-lookup"><span data-stu-id="fdc78-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="fdc78-232">2. finanszírozási forrás: 450,00</span><span class="sxs-lookup"><span data-stu-id="fdc78-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="fdc78-233">3. finanszírozási forrás: 450,00</span><span class="sxs-lookup"><span data-stu-id="fdc78-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="fdc78-234">
<strong>2. szabály</strong>
</span><span class="sxs-lookup"><span data-stu-id="fdc78-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="fdc78-235">3. finanszírozási forrás: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="fdc78-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="fdc78-236">
<strong>3. szabály</strong>
</span><span class="sxs-lookup"><span data-stu-id="fdc78-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="fdc78-237">1. finanszírozási forrás: 3850,00 (= 5000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="fdc78-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdc78-238">Az egyes finanszírozási forrásokhoz szétosztott teljes pénzösszeg</span><span class="sxs-lookup"><span data-stu-id="fdc78-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="fdc78-239">1. finanszírozási forrás: 3850,00</span><span class="sxs-lookup"><span data-stu-id="fdc78-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="fdc78-240">2. finanszírozási forrás: 500,00</span><span class="sxs-lookup"><span data-stu-id="fdc78-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="fdc78-241">3. finanszírozási forrás: 750,00</span><span class="sxs-lookup"><span data-stu-id="fdc78-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="fdc78-242">Számlázási szabályok</span><span class="sxs-lookup"><span data-stu-id="fdc78-242">Billing rules</span></span>
<span data-ttu-id="fdc78-243">Amikor az ügyféllel egyeztet egy projektszerződést, meghatározhatja, hogyan és mikor számlázhatja a projekten végzett munkát az ügyfélnek.</span><span class="sxs-lookup"><span data-stu-id="fdc78-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="fdc78-244">A projektszerződés és a projekt beállítása után megadhatja a projekt számlázási szabályait.</span><span class="sxs-lookup"><span data-stu-id="fdc78-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="fdc78-245">A számlázási szabályok a projektszerződésben megadott feltételeken alapulnak.</span><span class="sxs-lookup"><span data-stu-id="fdc78-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="fdc78-246">A létrehozható számlázási szabályok a projektszerződés feltételeitől és a projekttípustól (például Idő és anyag vagy a Rögzített ár) függenek, amelyeket a számlázási szabályhoz társít.</span><span class="sxs-lookup"><span data-stu-id="fdc78-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="fdc78-247">A projektszerződéshez több számlázási szabály is létrehozható.</span><span class="sxs-lookup"><span data-stu-id="fdc78-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="fdc78-248">Számlázási szabályt hozzárendelhet több olyan projekthez, amelyek ugyanahhoz a projektszerződéshez vannak társítva, és hasonló számlázási feltételekkel rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="fdc78-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="fdc78-249">A következő típusú számlázási szabályokat állíthatja be:</span><span class="sxs-lookup"><span data-stu-id="fdc78-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="fdc78-250">**Szállítási egység** – Az ügyfélnek egy szállítási egység teljesítésekor számláz.</span><span class="sxs-lookup"><span data-stu-id="fdc78-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="fdc78-251">A szállítási egységeket a szerződésben definiálja.</span><span class="sxs-lookup"><span data-stu-id="fdc78-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="fdc78-252">**Előrehaladás** – Az ügyfélnek a projekt megadott százalékának teljesítése után számláz.</span><span class="sxs-lookup"><span data-stu-id="fdc78-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="fdc78-253">Beállíthat egy számlázási szabályt, amely automatikusan kiszámítja a befejezett munka százalékos arányát, vagy manuálisam kiszámíthatja a befejezett munka százalékos arányát, valamint az ügyfélnek számlázandó összeget.</span><span class="sxs-lookup"><span data-stu-id="fdc78-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="fdc78-254">**Mérföldkő** – A mérföldkő elérésekor a projekt mérföldkövének teljes összege kerül számlázásra az ügyfélnek.</span><span class="sxs-lookup"><span data-stu-id="fdc78-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="fdc78-255">**Díj** – Az ügyfélnek a szolgáltatásainak díja, valamint egy kezelési díj kerül kiszámlázásra, amely jellemzően a szolgáltatások költségének adott százaléka.</span><span class="sxs-lookup"><span data-stu-id="fdc78-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="fdc78-256">**Idő és anyag** – A projektben használt idő és anyagok értéke kerül számlázásra az ügyfélnek.</span><span class="sxs-lookup"><span data-stu-id="fdc78-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="fdc78-257">Minden számlázásiszabály-típus esetében megadhat egy visszatartási százalékot, amely levonásra kerül az ügyfelek számláiból, amíg a projekt elér egy megállapodás szerinti fázist.</span><span class="sxs-lookup"><span data-stu-id="fdc78-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="fdc78-258">A fizetési visszatartási százalék a projektszerződésben van megadva.</span><span class="sxs-lookup"><span data-stu-id="fdc78-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="fdc78-259">Az összeget a rendszer az ügyfélszámla sorainak teljes értékéből számítja ki és kivonja ki.</span><span class="sxs-lookup"><span data-stu-id="fdc78-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="fdc78-260">Az **Idő és anyag** és a **Folyamatban lévő** számlázási szabályok esetében a felszámítható kategóriákat is hozzárendelhet.</span><span class="sxs-lookup"><span data-stu-id="fdc78-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="fdc78-261">A felszámítható kategóriák jelzik azokat a tranzakciókat, amelyeket szerepeltetni kell az ügyfelek számláján.</span><span class="sxs-lookup"><span data-stu-id="fdc78-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="fdc78-262">Amikor készen áll az ügyfél felé történő számlázásra, a program a számlázási szabályok alapján számítja ki a projektre vonatkozó számla összegét, és létrehoz egy projektszámla-javaslatot.</span><span class="sxs-lookup"><span data-stu-id="fdc78-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="fdc78-263">A következő szakaszok példákat tartalmaznak, amelyek bemutatják, hogyan állíthatók be és kezelhetők a projektek számlázási szabályai.</span><span class="sxs-lookup"><span data-stu-id="fdc78-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="fdc78-264">Példa: A leszállított egységek számán alapuló számlázási szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="fdc78-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="fdc78-265">A szervezete olyan megállapodást köt, amely összesen öt képzés alkalmat biztosít az ügyfél alkalmazottainak, képzési alkalmanként 10 000 költség ellenében.</span><span class="sxs-lookup"><span data-stu-id="fdc78-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="fdc78-266">Minden képzési alkalom után számláz az ügyfélnek.</span><span class="sxs-lookup"><span data-stu-id="fdc78-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="fdc78-267">A szerződés számlázási szabályainak beállításakor a következő értékek használhatók:</span><span class="sxs-lookup"><span data-stu-id="fdc78-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="fdc78-268">A szállítási egység egy képzési alkalom.</span><span class="sxs-lookup"><span data-stu-id="fdc78-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="fdc78-269">Az egységár 10 000 képzési alkalmanként.</span><span class="sxs-lookup"><span data-stu-id="fdc78-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="fdc78-270">Az egységek teljes száma öt képzési alkalom.</span><span class="sxs-lookup"><span data-stu-id="fdc78-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="fdc78-271">Amikor befejezte az egyik képzési alkalmat, a 10 000 összegű számlát hoz létre a leszállított első egységre vonatkozóan, és elküldi a számlát az üygfélnek.</span><span class="sxs-lookup"><span data-stu-id="fdc78-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="fdc78-272">Példa: A projekt készültségének meghatározott százalékán alapuló számlázási szabály létrehozása (manuális számítás)</span><span class="sxs-lookup"><span data-stu-id="fdc78-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="fdc78-273">A szervezete, egy szoftvertanácsadó vállalat megállapodást köt az ügyféllel, hogy kifejleszti az ügyfél által fejlesztett termék egy részét.</span><span class="sxs-lookup"><span data-stu-id="fdc78-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="fdc78-274">A szervezete vállalja, hogy hat hónap alatt szállítja le a szoftver kódját.</span><span class="sxs-lookup"><span data-stu-id="fdc78-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="fdc78-275">Az ügyfél vállalja, hogy a munkáért összesen 100 000-et fizet a szervezetlnek.</span><span class="sxs-lookup"><span data-stu-id="fdc78-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="fdc78-276">Számlázási szabályt hoz létre, amely az ügyfelet a projektből a szerződésben meghatározott százalékban elkészült munkamennyiség alapján számlázza.</span><span class="sxs-lookup"><span data-stu-id="fdc78-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="fdc78-277">Az első hónap végén találkozik az ügyféllel, hogy megállapítsa a befejezett munka százalékos arányát.</span><span class="sxs-lookup"><span data-stu-id="fdc78-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="fdc78-278">Miután az ügyféllel áttekinti a projektet, úgy döntenek, hogy a projekt 15 százaléka készült el.</span><span class="sxs-lookup"><span data-stu-id="fdc78-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="fdc78-279">Létrehoz egy 15 000 (a teljes 100 000-es összeg 15%-a) összegű számlát, és elküldi az ügyfélnek.</span><span class="sxs-lookup"><span data-stu-id="fdc78-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="fdc78-280">Példa: A projekt készültségének meghatározott százalékán alapuló számlázási szabály létrehozása (automatikus számítás)</span><span class="sxs-lookup"><span data-stu-id="fdc78-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="fdc78-281">Szervezete, egy szoftverfejlesztő cég vállalja, hogy kidolgoz egy bérszámfejtési csomagot egy ügyfél számára 30 000-ért.</span><span class="sxs-lookup"><span data-stu-id="fdc78-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="fdc78-282">Az ügyfél vállalja, hogy a munkáért az elkészült munka százalékos aránya alapján fizet.</span><span class="sxs-lookup"><span data-stu-id="fdc78-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="fdc78-283">Úgy becsüli, hogy a projekt költségei 20 000-et tesznek ki.</span><span class="sxs-lookup"><span data-stu-id="fdc78-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="fdc78-284">A projektszerződés meghatározza a számlázási folyamatban használt munkakategóriákat.</span><span class="sxs-lookup"><span data-stu-id="fdc78-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="fdc78-285">Olyan számlázási szabályokat kell beállítani, amelyek automatikusan kiszámítják a számlaösszegeket az egyes kategóriákhoz tartozó befejezett munkamennyiségek százalékos arányai alapján.</span><span class="sxs-lookup"><span data-stu-id="fdc78-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="fdc78-286">Minden egyes kategóriához beállít egy költségvetést:</span><span class="sxs-lookup"><span data-stu-id="fdc78-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="fdc78-287">**Fejlesztés** – 15 000 költség és 20 000 árbevétel</span><span class="sxs-lookup"><span data-stu-id="fdc78-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="fdc78-288">**Telepítés** – 5000 költség és 10 000 árbevétel</span><span class="sxs-lookup"><span data-stu-id="fdc78-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="fdc78-289">Amikor első alkalommal hoz létre egy ügyfélszámlát, a rendszer automatikusan kiszámítja a számla összegét az alábbi adatok alapján:</span><span class="sxs-lookup"><span data-stu-id="fdc78-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="fdc78-290">Egy hónap elteltével a projekt munkatársa elküldi a projekthez tartozó munkaidő-nyilvántartást.</span><span class="sxs-lookup"><span data-stu-id="fdc78-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="fdc78-291">A dolgozói órák ára 5000 a fejlesztés és 1000 a telepítés esetében.</span><span class="sxs-lookup"><span data-stu-id="fdc78-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="fdc78-292">A fejlesztési munka 33 százaléka készült el (5000 tényleges költség/15 000 költségvetési költség), a telepítési munkának pedig 20%-a készült el (1000 tényleges költség/5000 költségvetési költség).</span><span class="sxs-lookup"><span data-stu-id="fdc78-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="fdc78-293">A rendszer automatikusan kiszámítja a 8667 összeget (20 000 33 százaléka + 10 000 20 százaléka).</span><span class="sxs-lookup"><span data-stu-id="fdc78-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="fdc78-294">Létrehoz egy 8667 összegű számlát, és elküldi az ügyfélnek.</span><span class="sxs-lookup"><span data-stu-id="fdc78-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="fdc78-295">Példa: Megállapodás szerinti mérföldköveken alapuló számlázási szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="fdc78-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="fdc78-296">A szervezete, egy menedzsmenttanácsadó cég vállalja, hogy az ügyfél által értékesíteni tervezett termékre vonatkozóan piackutatást végez.</span><span class="sxs-lookup"><span data-stu-id="fdc78-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="fdc78-297">Az ügyfél vállalja, hogy a szolgáltatásait márciusi kezdettel három hónapig igénybe veszi, és beleegyezik, hogy a szervezetének 50 000-et fizet.</span><span class="sxs-lookup"><span data-stu-id="fdc78-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="fdc78-298">A projekthez három mérföldkő tartozik:</span><span class="sxs-lookup"><span data-stu-id="fdc78-298">The project has three milestones:</span></span>

-   <span data-ttu-id="fdc78-299">1. mérföldkő: Fogyasztói adatok gyűjtése – Március 31.út 31</span><span class="sxs-lookup"><span data-stu-id="fdc78-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="fdc78-300">2. mérföldkő: Fogyasztói adatok elemzése – Április 30.</span><span class="sxs-lookup"><span data-stu-id="fdc78-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="fdc78-301">3. mérföldkő: Termék életképességére vonatkozó javaslat bemutatása – Május 31.</span><span class="sxs-lookup"><span data-stu-id="fdc78-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="fdc78-302">Az ügyfél vállalja, hogy kifizet a szervezetének 10 000-et az első mérföldkő, 20 000-et a második mérföldkő, és 20 000-et a harmadik mérföldkő eléréséért.</span><span class="sxs-lookup"><span data-stu-id="fdc78-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="fdc78-303">A projektszerződés rögzítésekor beleegyezik, hogy az ügyfélnek a teljesített mérföldkövek alapján számláz.</span><span class="sxs-lookup"><span data-stu-id="fdc78-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="fdc78-304">A számlázási szabály összeállítása a következő lépéseket tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="fdc78-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="fdc78-305">A projekt mérföldköveinek megadása.</span><span class="sxs-lookup"><span data-stu-id="fdc78-305">Define the project milestones.</span></span>
-   <span data-ttu-id="fdc78-306">Az ügyfél felé számlázandó összeg meghatározása az egyes mérföldkövek teljesítésekor.</span><span class="sxs-lookup"><span data-stu-id="fdc78-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="fdc78-307">Amikor az első mérföldkő március 31-én elkészül, akkor megjelöli befejezettként a mérföldkövet, majd létrehoz egy számlát 10 000 összeggel, és elküldi az ügyfélnek.</span><span class="sxs-lookup"><span data-stu-id="fdc78-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="fdc78-308">A mérföldkőhöz tartozó számla csak akkor hozható létre, ha a mérföldkő befejezettként van megjelölve.</span><span class="sxs-lookup"><span data-stu-id="fdc78-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="fdc78-309">Példa: Szolgáltatási és kezelési díjon alapuló számlázási szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="fdc78-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="fdc78-310">A szervezete, egy menedzsment-tanácsadó cég vállalja, hogy piackutatást hajt végre az ügyfél, egy kiskereskedelmi vállalat által fejlesztett termék életképességével kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="fdc78-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="fdc78-311">A szerződés feltételei meghatározzák, hogy a három legjobb menedzsment-tanácsadója szolgáltatásait fogja biztosítani, akik idő és anyag alapon hajtják végre a kutatást.</span><span class="sxs-lookup"><span data-stu-id="fdc78-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="fdc78-312">Az ügyfél beleegyezik, hogy a projekt esetében felszámított tanácsadási órákért 100 egységet fizet, valamint 10 százalék kezelési díjat.</span><span class="sxs-lookup"><span data-stu-id="fdc78-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="fdc78-313">A projektszerződés megkötésekor hozzon létre egy számlázási szabályt, amely 10 százalékos kezelési költséget ad hozzá a projektre felszámolt tanácsadási órákhoz.</span><span class="sxs-lookup"><span data-stu-id="fdc78-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="fdc78-314">Amikor számlát hoz létre az ügyfélnek, az ügyfél 10 százalékos kezelési díjról és a tanácsadási órák költségéről kap számlát.</span><span class="sxs-lookup"><span data-stu-id="fdc78-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="fdc78-315">Ha például a három tanácsadó a projektben összesen 200 órát dolgozott, a 22 000 összegű számlát a következő számítás alapján hozza létre:</span><span class="sxs-lookup"><span data-stu-id="fdc78-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="fdc78-316">200 óra, óránként 100 egység áron = 20 000</span><span class="sxs-lookup"><span data-stu-id="fdc78-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="fdc78-317">10 százalékos kezelési díj = 2000</span><span class="sxs-lookup"><span data-stu-id="fdc78-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="fdc78-318">Teljes számlázott mennyiség = 22 000</span><span class="sxs-lookup"><span data-stu-id="fdc78-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="fdc78-319">Ha egy ügyfél esetében a díjak adókötelesek, és kiválaszt egy áfacsoportot a projektszerződésben, akkor az áfacsoport automatikusan megadásra kerül a díjak számlázási szabályaiban.</span><span class="sxs-lookup"><span data-stu-id="fdc78-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="fdc78-320">Példa: Számlázási szabály létrehozása az idő és az anyagok értékéhez</span><span class="sxs-lookup"><span data-stu-id="fdc78-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="fdc78-321">A szervezete, egy szoftvertanácsadó cég vállalja, hogy öt műszaki tanácsadót biztosít az ügyfele szoftverfejlesztési projektjén végzett munkára a következő hat hónapra.</span><span class="sxs-lookup"><span data-stu-id="fdc78-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="fdc78-322">Az ügyfél beleegyezik, hogy minden tanácsadói órára 150-et fizet, valamint az irodaszerek költségét.</span><span class="sxs-lookup"><span data-stu-id="fdc78-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="fdc78-323">A szervezete minden hónap végén számlát küld az ügyfélnek.</span><span class="sxs-lookup"><span data-stu-id="fdc78-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="fdc78-324">A projektszerződés beállításakor vállalja, hogy az ügyfélnek havonta állít ki számlát a projekthez felhasznált időre és az anyagokra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="fdc78-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="fdc78-325">A következő információkat tartalmazó számlázási szabályt hoz létre:</span><span class="sxs-lookup"><span data-stu-id="fdc78-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="fdc78-326">A szerződés időszaka hat hónap.</span><span class="sxs-lookup"><span data-stu-id="fdc78-326">The contract period is six months.</span></span>
-   <span data-ttu-id="fdc78-327">A tanácsadási időt óránként 150-es áron számítja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="fdc78-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="fdc78-328">Az irodaszerek számlázása költségen történik, és a projekt teljes költsége nem haladhatja meg a 10 000 értéket.</span><span class="sxs-lookup"><span data-stu-id="fdc78-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="fdc78-329">A projekt során minden naptári hónap végén létre kell hoznia egy vevői számlát.</span><span class="sxs-lookup"><span data-stu-id="fdc78-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="fdc78-330">Az első hónapban összesen 800 órát rögzítenek a projekten dolgozó tanácsadók.</span><span class="sxs-lookup"><span data-stu-id="fdc78-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="fdc78-331">A projektre terhelt irodaszerek ára 2000.</span><span class="sxs-lookup"><span data-stu-id="fdc78-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="fdc78-332">Ezért a hónap végén létrehoz egy 122 000 összegű számlát, amelyhez 800 órát számít fel 150-es óránkénti áron, valamint az irodai kellékanyagok esetében 2000-et.</span><span class="sxs-lookup"><span data-stu-id="fdc78-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]