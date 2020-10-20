---
title: Projektalapú árajánlatsor becslése
description: Ez a témakör azt ismerteti, hogyan lehet becslést létrehozni egy projektalapú árajánlatsorban.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 65aee7238781ac90f603e57c6d9b0b92cabd6644
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966799"
---
# <a name="estimating-a-project-based-quote-line"></a><span data-ttu-id="c9001-103">Projektalapú árajánlatsor becslése</span><span class="sxs-lookup"><span data-stu-id="c9001-103">Estimating a project-based quote line</span></span>

<span data-ttu-id="c9001-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="c9001-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c9001-105">A projektalapú árajánlatsor olyan részletekkel rendelkezik, amelyek segítenek az árajánlatsor elkészítésére fordított munka költségének és potenciális bevételének becslésében.</span><span class="sxs-lookup"><span data-stu-id="c9001-105">A project-based quote line has details that help with estimating the cost and potential revenue of the work involved to deliver the quote line.</span></span>

<span data-ttu-id="c9001-106">A projektalapú árajánlatsor becsléséhez válassza ki a projektalapú árajánlatsoron az **Árajánlatsor részletei** lapot. A becsléseket kétféleképpen lehet létrehozni egy projektalapú árajánlatsorban:</span><span class="sxs-lookup"><span data-stu-id="c9001-106">To estimate a project-based quote line, on the project-based quote line, select the **Quote Line Detail** tab. There are two ways to create an estimate on a project-based quote line:</span></span>

- <span data-ttu-id="c9001-107">A becslés manuális létrehozása közvetlenül az árajánlatsorban az árajánlatsor részleteinek használatával</span><span class="sxs-lookup"><span data-stu-id="c9001-107">Manually create the estimate directly on the quote line using quote line details</span></span> 
- <span data-ttu-id="c9001-108">Hozzon létre egy projektet és egy projekttervet, majd társítsa a projektet és a feladatokat a projekten az árajánlatsorhoz.</span><span class="sxs-lookup"><span data-stu-id="c9001-108">Create a project and a project plan, and then associate the project and tasks on the project to the quote line.</span></span> <span data-ttu-id="c9001-109">A projektterv becsült értékének az árajánlatsorba való importálásának folyamata a megadott adatok alapján engedélyezve lesz.</span><span class="sxs-lookup"><span data-stu-id="c9001-109">The process to import the estimates on the project plan into the quote line based on the information you provided will be enabled.</span></span>

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a><span data-ttu-id="c9001-110">Projektbecslések létrehozása közvetlenül egy projektalapú árajánlatsoron</span><span class="sxs-lookup"><span data-stu-id="c9001-110">Create estimates directly on a project-based quote line</span></span>

<span data-ttu-id="c9001-111">Ha egy projektalapú árajánlatsor becslését szeretné létrehozni, akkor válassza ki az **Árajánlatsor részletei** lapot. Az ezen a lapon létrehozott sor összesíti az árajánlatsorhoz tartozó ajánlati értéket.</span><span class="sxs-lookup"><span data-stu-id="c9001-111">To create an estimate on a project-based quote line, select the **Quote Line Detail** tab. The line item that you create on this tab will summarize the quoted value for this quote line.</span></span> 

<span data-ttu-id="c9001-112">Az árajánlatsor részleteinek létrehozásához válassza az **+ Új árajánlatsor-részlet** lehetőséget az **Árajánlatsor részletei** alrácson.</span><span class="sxs-lookup"><span data-stu-id="c9001-112">To create quote line details, select **+ New quote line detail** on the **Quote Line Details** sub-grid.</span></span> <span data-ttu-id="c9001-113">Megnyílik egy gyorslétrehozási csúszka.</span><span class="sxs-lookup"><span data-stu-id="c9001-113">A quick create slider will open.</span></span> <span data-ttu-id="c9001-114">Az **Árajánlatsor** űrlap következő mezői:</span><span class="sxs-lookup"><span data-stu-id="c9001-114">The following fields on the **Quote Line** form:</span></span>

| <span data-ttu-id="c9001-115">**Mező**</span><span class="sxs-lookup"><span data-stu-id="c9001-115">**Field**</span></span> | <span data-ttu-id="c9001-116">**Hely**</span><span class="sxs-lookup"><span data-stu-id="c9001-116">**Location**</span></span> | <span data-ttu-id="c9001-117">**Relevancia, cél és útmutatás**</span><span class="sxs-lookup"><span data-stu-id="c9001-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="c9001-118">**Alsóbb rétegbeli hatás**</span><span class="sxs-lookup"><span data-stu-id="c9001-118">**Downstream impact**</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="c9001-119">Adatfolyam leírása</span><span class="sxs-lookup"><span data-stu-id="c9001-119">Description</span></span> | <span data-ttu-id="c9001-120">Gyorslétrehozás</span><span class="sxs-lookup"><span data-stu-id="c9001-120">Quick create</span></span> | <span data-ttu-id="c9001-121">Egy adott becslés leírása.</span><span class="sxs-lookup"><span data-stu-id="c9001-121">A description of the specific estimate.</span></span> | <span data-ttu-id="c9001-122">Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be.</span><span class="sxs-lookup"><span data-stu-id="c9001-122">This field defaults to the related quote line detail for cost that is automatically created.</span></span> |
| <span data-ttu-id="c9001-123">Tranzakció osztálya</span><span class="sxs-lookup"><span data-stu-id="c9001-123">Transaction Class</span></span> | <span data-ttu-id="c9001-124">Gyorslétrehozás</span><span class="sxs-lookup"><span data-stu-id="c9001-124">Quick create</span></span> | <span data-ttu-id="c9001-125">Ez a legördülő lista a projektalapú árajánlatsor **Általános** lapján szereplő tranzakciós osztályokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c9001-125">This drop-down list provides the transaction classes that are included on the **General** tab of project-based quote line.</span></span>  | <span data-ttu-id="c9001-126">Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be.</span><span class="sxs-lookup"><span data-stu-id="c9001-126">This field defaults to the related quote line detail for cost that is automatically created.</span></span> |
| <span data-ttu-id="c9001-127">Szerepkör</span><span class="sxs-lookup"><span data-stu-id="c9001-127">Role</span></span> | <span data-ttu-id="c9001-128">Gyorslétrehozás</span><span class="sxs-lookup"><span data-stu-id="c9001-128">Quick create</span></span> | <span data-ttu-id="c9001-129">Az a személy, aki ezt a munkát végrehajtja, vagy akinél ez a kiadás felmerül.</span><span class="sxs-lookup"><span data-stu-id="c9001-129">The person that will perform this work or incur this expense.</span></span> | <span data-ttu-id="c9001-130">Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be.</span><span class="sxs-lookup"><span data-stu-id="c9001-130">This field defaults to the related quote line detail for cost that is automatically created.</span></span> |
| <span data-ttu-id="c9001-131">Kategória</span><span class="sxs-lookup"><span data-stu-id="c9001-131">Category</span></span> | <span data-ttu-id="c9001-132">Gyorslétrehozás</span><span class="sxs-lookup"><span data-stu-id="c9001-132">Quick create</span></span> | <span data-ttu-id="c9001-133">A munka vagy kiadás kategóriája.</span><span class="sxs-lookup"><span data-stu-id="c9001-133">Category of the work or expense.</span></span> | <span data-ttu-id="c9001-134">Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be.</span><span class="sxs-lookup"><span data-stu-id="c9001-134">This field defaults to the related quote line detail for cost that is automatically created.</span></span> |
| <span data-ttu-id="c9001-135">Kezdő dátum</span><span class="sxs-lookup"><span data-stu-id="c9001-135">Start Date</span></span> | <span data-ttu-id="c9001-136">Gyorslétrehozás</span><span class="sxs-lookup"><span data-stu-id="c9001-136">Quick create</span></span> | <span data-ttu-id="c9001-137">A munka kezdő dátuma.</span><span class="sxs-lookup"><span data-stu-id="c9001-137">Start date of the work.</span></span> | <span data-ttu-id="c9001-138">Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be.</span><span class="sxs-lookup"><span data-stu-id="c9001-138">This field defaults to the related quote line detail for cost that is automatically created.</span></span> |
| <span data-ttu-id="c9001-139">Befejező dátum</span><span class="sxs-lookup"><span data-stu-id="c9001-139">End Date</span></span> | <span data-ttu-id="c9001-140">Gyorslétrehozás</span><span class="sxs-lookup"><span data-stu-id="c9001-140">Quick create</span></span> | <span data-ttu-id="c9001-141">A munka záró dátuma.</span><span class="sxs-lookup"><span data-stu-id="c9001-141">End date of the work.</span></span> | <span data-ttu-id="c9001-142">Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be.</span><span class="sxs-lookup"><span data-stu-id="c9001-142">This field defaults to the related quote line detail for cost that is automatically created.</span></span> |
| <span data-ttu-id="c9001-143">Erőforrás-kezelő részleg</span><span class="sxs-lookup"><span data-stu-id="c9001-143">Resourcing Unit</span></span> | <span data-ttu-id="c9001-144">Gyorslétrehozás</span><span class="sxs-lookup"><span data-stu-id="c9001-144">Quick create</span></span> | <span data-ttu-id="c9001-145">A beszerzési egység, amelynél felmerül ez a költség, és biztosítja az erőforrást az azon végzett munkához.</span><span class="sxs-lookup"><span data-stu-id="c9001-145">Resourcing unit that will incur this cost and provide the resource to work on it.</span></span> | <span data-ttu-id="c9001-146">Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be.</span><span class="sxs-lookup"><span data-stu-id="c9001-146">This field defaults to the related quote line detail for cost that is automatically created.</span></span> <span data-ttu-id="c9001-147">Ez a mező az önköltségi ár beolvasása esetén is használatos.</span><span class="sxs-lookup"><span data-stu-id="c9001-147">This field is also used in cost price retrieval.</span></span> |
| <span data-ttu-id="c9001-148">Egységütemezés</span><span class="sxs-lookup"><span data-stu-id="c9001-148">Unit schedule</span></span> | <span data-ttu-id="c9001-149">Gyorslétrehozás</span><span class="sxs-lookup"><span data-stu-id="c9001-149">Quick create</span></span> | <span data-ttu-id="c9001-150">A munka vagy kiadás egységcsoportja.</span><span class="sxs-lookup"><span data-stu-id="c9001-150">Unit group of the work or expense.</span></span> <span data-ttu-id="c9001-151">Az egységek egy egységütemezéshez vagy egységcsoporthoz tartoznak.</span><span class="sxs-lookup"><span data-stu-id="c9001-151">Units belong to a unit schedule or a group of units.</span></span> <span data-ttu-id="c9001-152">Például a mérföldek és kilométerek távolságot leíró egységek egy csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="c9001-152">For example, Miles and KMs are units that belong to a group of units that describes distance.</span></span> | <span data-ttu-id="c9001-153">Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be.</span><span class="sxs-lookup"><span data-stu-id="c9001-153">This field defaults to the related quote line detail for cost that is automatically created.</span></span> |
| <span data-ttu-id="c9001-154">Kiszerelés</span><span class="sxs-lookup"><span data-stu-id="c9001-154">Unit</span></span> | <span data-ttu-id="c9001-155">Gyorslétrehozás</span><span class="sxs-lookup"><span data-stu-id="c9001-155">Quick create</span></span> | <span data-ttu-id="c9001-156">A munka vagy kiadás egysége.</span><span class="sxs-lookup"><span data-stu-id="c9001-156">Unit of the work or expense.</span></span> | <span data-ttu-id="c9001-157">Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be.</span><span class="sxs-lookup"><span data-stu-id="c9001-157">This field defaults to the related quote line detail for cost that is automatically created.</span></span> |
| <span data-ttu-id="c9001-158">Mennyiség</span><span class="sxs-lookup"><span data-stu-id="c9001-158">Quantity</span></span> | <span data-ttu-id="c9001-159">Gyorslétrehozás</span><span class="sxs-lookup"><span data-stu-id="c9001-159">Quick create</span></span> | <span data-ttu-id="c9001-160">A munka vagy kiadás mennyisége.</span><span class="sxs-lookup"><span data-stu-id="c9001-160">Quantity of work or expense</span></span> | <span data-ttu-id="c9001-161">Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be.</span><span class="sxs-lookup"><span data-stu-id="c9001-161">This field defaults to the related quote line detail for cost that is automatically created.</span></span> |
| <span data-ttu-id="c9001-162">Egységár</span><span class="sxs-lookup"><span data-stu-id="c9001-162">Unit price</span></span> | <span data-ttu-id="c9001-163">Gyorslétrehozás</span><span class="sxs-lookup"><span data-stu-id="c9001-163">Quick create</span></span> | <span data-ttu-id="c9001-164">A költségkategóriára vonatkozó munkát végrehajtó szerepkör számlázási ára vagy az értékesítési ár.</span><span class="sxs-lookup"><span data-stu-id="c9001-164">Bill rate of the role that is performing the work or the Sales price of the expense category.</span></span> <span data-ttu-id="c9001-165">Ez a mező alapértelmezés szerint arra az időre áll be, amely a szerepkör és az erőforrásbiztosító egység kombinációja alapján kezdő dátumként érvényes a projekt árlistájában.</span><span class="sxs-lookup"><span data-stu-id="c9001-165">This field defaults for Time based on the role and resourcing unit combination on the project price list that is effective for the start date.</span></span> <span data-ttu-id="c9001-166">A kiadások esetében ez a mező alapértelmezés szerint a kezdő dátumnál érvényben lévő, a projekt árlistájában szereplő tranzakciós kategóriához tartozó árból kerül beállításra.</span><span class="sxs-lookup"><span data-stu-id="c9001-166">For expenses, this field defaults from the price setup for the transaction category in the project price list that is effective for the start date.</span></span> <span data-ttu-id="c9001-167">Ha a tranzakciós kategória árképzési módja nem egységár, nincs alapértelmezett érték, és ez a mező üresen marad.</span><span class="sxs-lookup"><span data-stu-id="c9001-167">If the pricing method for the transaction category is not price-per-unit, there is no default, and this field is left blank.</span></span> | <span data-ttu-id="c9001-168">A költségkategóriára vonatkozó munkát végrehajtó szerepkör költségára vagy az egységár.</span><span class="sxs-lookup"><span data-stu-id="c9001-168">Cost rate of the role that is performing the work or the cost-per-unit of the expense category.</span></span> <span data-ttu-id="c9001-169">Ez a mező alapértelmezés szerint arra az időre áll be, amely a szerepkör és az erőforrásbiztosító egység kombinációja alapján kezdő dátumként érvényes az árajánlat árlistájához tartozó szerződő egység áránál.</span><span class="sxs-lookup"><span data-stu-id="c9001-169">This field defaults for Time based on the role and resourcing unit combination on the price of the Contracting unit of the Quote price list that is effective for the start date.</span></span> <span data-ttu-id="c9001-170">A kiadások esetében ez a mező alapértelmezés szerint a kezdő dátumnál érvényben lévő, a szerződő egység költség-árlistájában szereplő tranzakciós kategóriához tartozó árból kerül beállításra.</span><span class="sxs-lookup"><span data-stu-id="c9001-170">For expenses, this field defaults from the price setup for the transaction category in the cost price list of Contracting unit that is effective for the start date.</span></span> <span data-ttu-id="c9001-171">Ha a tranzakciós kategória árképzési módja nem egységár, nincs alapértelmezett érték, és ez a mező üresen marad.</span><span class="sxs-lookup"><span data-stu-id="c9001-171">If the pricing method for the transaction category is not price-per-unit, there is no default and this field is left blank.</span></span> |
| <span data-ttu-id="c9001-172">Becsült adó</span><span class="sxs-lookup"><span data-stu-id="c9001-172">Estimated Tax</span></span> | <span data-ttu-id="c9001-173">Gyorslétrehozás</span><span class="sxs-lookup"><span data-stu-id="c9001-173">Quick create</span></span> | <span data-ttu-id="c9001-174">A munkára vagy kiadásra vonatkozó becsült adót kézzel is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="c9001-174">You can manually enter the estimated tax for this work or expense.</span></span> | <span data-ttu-id="c9001-175">Ennek a mezőnek nincs későbbi hatása.</span><span class="sxs-lookup"><span data-stu-id="c9001-175">There is no downstream impact of this field.</span></span> |
| <span data-ttu-id="c9001-176">Mennyiség</span><span class="sxs-lookup"><span data-stu-id="c9001-176">Amount</span></span> | <span data-ttu-id="c9001-177">Gyorslétrehozás</span><span class="sxs-lookup"><span data-stu-id="c9001-177">Quick create</span></span> | <span data-ttu-id="c9001-178">Az adatokat manuálisan is beviheti ebbe a mezőbe, ha a **Mennyiség** és az **Ár** mező üresen marad.</span><span class="sxs-lookup"><span data-stu-id="c9001-178">You can manually input information into this field if the **Quantity** and **Price** fields are left blank.</span></span> <span data-ttu-id="c9001-179">Ha ezek a mezők nem üresek, akkor ez a mező írásvédett lesz, és számítása a következőképp történik (Mennyiség \* Egységár) + Adó.</span><span class="sxs-lookup"><span data-stu-id="c9001-179">If these fields are not blank, this field becomes read-only and is calculated as (Quantity \* Unit price) + Tax.</span></span> | <span data-ttu-id="c9001-180">Ennek a mezőnek nincs későbbi hatása.</span><span class="sxs-lookup"><span data-stu-id="c9001-180">There is no downstream impact of this field.</span></span> |

## <a name="update-prices-on-quote-line-details"></a><span data-ttu-id="c9001-181">Árak frissítése az árajánlatsor részleteiben</span><span class="sxs-lookup"><span data-stu-id="c9001-181">Update prices on quote line details</span></span>

<span data-ttu-id="c9001-182">Ha megváltoztatta az árakat az árajánlathoz mellékelt projektárlistán vagy a szerződési egység önköltségiár-listáján, akkor az **Árajánlat** oldalon az **Újraszámolás** lehetőségre kattinthat, és az egyes árajánlatsor-részletekben szereplő árakat frissítheti, hogy azok tükrözzék ezt a változást.</span><span class="sxs-lookup"><span data-stu-id="c9001-182">If you have changed prices on the project price list that is attached to the quote, or on cost price list of the contracting unit, you can select **Recalculate** on the **Quote** page, to refresh the prices on the individual quote line details to reflect this change.</span></span> <span data-ttu-id="c9001-183">Amikor az **Újraszámolás** lehetőséget választja, egy figyelmeztetés jelenik meg, hogy az árajánlatban szereplő összes árajánlatsor árajánlatsor-részleteihez tartozó árak alaphelyzetbe kerülnek.</span><span class="sxs-lookup"><span data-stu-id="c9001-183">When you select **Recalculate**, a warning occurs that informs you that prices on quote line details for all quote lines on this quote will be reset.</span></span> <span data-ttu-id="c9001-184">Válassza az **Igen** lehetőséget, ha az mind az értékesítés, mind a költség árajánlatsor-részletek árait frissíteni szeretné.</span><span class="sxs-lookup"><span data-stu-id="c9001-184">Select **Yes**, to refresh prices for both sales and cost quote line details.</span></span>

## <a name="access-quote-line-details-for-cost"></a><span data-ttu-id="c9001-185">A költség árajánlatsor-részleteinek elérése</span><span class="sxs-lookup"><span data-stu-id="c9001-185">Access quote line details for cost</span></span>

<span data-ttu-id="c9001-186">Az **Árajánlatsor részletei** lapon jelöljön ki egy sort a rácsban, hogy engedélyezze az alrács eszköztárának bizonyos műveleteit.</span><span class="sxs-lookup"><span data-stu-id="c9001-186">On the **Quote Line Details** tab, select a row in the grid to enable some actions on the toolbar of the sub-grid.</span></span> <span data-ttu-id="c9001-187">Az alrács eszköztár első művelete, amikor az árajánlatsor részletei be van jelölve, a **Költség részleteinek megnyitása**.</span><span class="sxs-lookup"><span data-stu-id="c9001-187">The first action on the sub-grid tool bar when a quote line detail is selected is **Open Cost Detail**.</span></span> <span data-ttu-id="c9001-188">Válassza a **Költség részleteinek megnyitása** lehetőséget az árajánlatsorhoz kapcsolódó költségarány és -összeg megtekintéséhez.</span><span class="sxs-lookup"><span data-stu-id="c9001-188">Select **Open Cost Detail** to see the related cost rate and amount for this quote line.</span></span>

> [!NOTE]
> <span data-ttu-id="c9001-189">Az erőforrásbiztosító egység, mennyiség, dátumok, szerep vagy kategória értékek módosítása a költség árajánlatsor-részletein módosítani fogja az értékesítések árajánlatsor-részleteinek megfelelő értékét.</span><span class="sxs-lookup"><span data-stu-id="c9001-189">Changing the resourcing unit, quantity, dates, role, or category values on the quote line detail for cost will change the corresponding values on the quote line details for sales.</span></span>
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a><span data-ttu-id="c9001-190">Az költség és értékesítések ajánlatsor-részleteinek pénzneme</span><span class="sxs-lookup"><span data-stu-id="c9001-190">Currency on quote line details for cost and sales</span></span>

<span data-ttu-id="c9001-191">Az értékesítések árajánlatsor-részleteinek pénzneme az árajánlatsor-részlet kezdő dátuma esetében érvényes projektárlistából veszi az alapértelmezett értékét.</span><span class="sxs-lookup"><span data-stu-id="c9001-191">Currency on the quote line detail for sales defaults from the project price list that is effective for the start date of the quote line detail.</span></span>

<span data-ttu-id="c9001-192">A költség árajánlatsor-részleteinek pénzneme az költség árajánlatsor-részletének kezdő dátuma esetében érvényes árajánlat szerződési egységének árlistájából veszi az alapértelmezett értékét.</span><span class="sxs-lookup"><span data-stu-id="c9001-192">Currency on the quote line detail for cost defaults from the price list of the contracting unit of the quote that is effective for the start date of the quote line detail for cost.</span></span>

<span data-ttu-id="c9001-193">A jövedelmezőségi számítások átváltják a költség és értékesítések árajánlatsor-részleteiben szereplő összeget a környezet alappénznemére az árajánlat teljes becsült hasznának jelentéséhez.</span><span class="sxs-lookup"><span data-stu-id="c9001-193">Profitability calculations convert the amount on quote line details for cost and sales into the base currency of the environment to report the overall estimated margin on the quote.</span></span>

<span data-ttu-id="c9001-194">Ennek következtében a pénznemek kerekítési hibái és a nyereségek módosulhatnak a tényleges átváltási árfolyamok hiánya miatt.</span><span class="sxs-lookup"><span data-stu-id="c9001-194">This could result in currency rounding errors and changing margins because of the lack of date effective exchange rates.</span></span> <span data-ttu-id="c9001-195">Ezeket a számításokat a projektárajánlatok esetében csak közelítésként használja és nem a tényleges törvényi vagy egyéb jelentéskészítéshez, amely nagyobb kerekítési pontosságot vagy az átváltási árfolyamok érvényességének ismeretét követeli meg.</span><span class="sxs-lookup"><span data-stu-id="c9001-195">Use these calculations on Project quotes only as approximations and not actual statutory or other reporting that requires higher precision of rounding and awareness of date effectivity for exchange rates.</span></span>