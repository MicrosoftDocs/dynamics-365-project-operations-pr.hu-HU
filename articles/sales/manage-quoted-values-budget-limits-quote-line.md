---
title: Projekt árajánlatsorok áttekintése
description: Ez témakör az árajánlatsorok projektmunkához történő használatáról nyújt tájékoztatást.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: c585bbc55119e678a4f75f5dfe8966a436db1a34
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368074"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="62096-103">Projekt árajánlatsorok áttekintése</span><span class="sxs-lookup"><span data-stu-id="62096-103">Project quote lines overview</span></span>

<span data-ttu-id="62096-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="62096-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="62096-105">A projektalapú ajánlati sorok úgy vannak kialakítva, hogy elősegítsék az aktivitásra vonatkozó projektmunka becslését.</span><span class="sxs-lookup"><span data-stu-id="62096-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="62096-106">A projektalapú ajánlatsor felépítése a projektbecslésekhez a következő fogalmakkal bővül:</span><span class="sxs-lookup"><span data-stu-id="62096-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="62096-107">Számlázási mód</span><span class="sxs-lookup"><span data-stu-id="62096-107">Billing Method</span></span>
- <span data-ttu-id="62096-108">Projektleképezés</span><span class="sxs-lookup"><span data-stu-id="62096-108">Project Mapping</span></span>
- <span data-ttu-id="62096-109">Szerepeltetett tranzakciós osztályok</span><span class="sxs-lookup"><span data-stu-id="62096-109">Included Transaction classes</span></span>
- <span data-ttu-id="62096-110">Nem meghaladandó korlát</span><span class="sxs-lookup"><span data-stu-id="62096-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="62096-111">Felszámíthatósági beállítás</span><span class="sxs-lookup"><span data-stu-id="62096-111">Chargeability setup</span></span>
- <span data-ttu-id="62096-112">Becslés az ajánlati sor részleteinek használatával</span><span class="sxs-lookup"><span data-stu-id="62096-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="62096-113">Árajánlatsor ügyfelei</span><span class="sxs-lookup"><span data-stu-id="62096-113">Quote line Customers</span></span>

<span data-ttu-id="62096-114">A következő táblázat a projektalapú árajánlatsor **Általános** lapján található mezőkre vonatkozó információkat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="62096-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="62096-115">Ezek a mezők segítséget nyújtanak a projektmunka részletes, jól felépített becslési alapjainak kialakításában.</span><span class="sxs-lookup"><span data-stu-id="62096-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="62096-116">**Mező**</span><span class="sxs-lookup"><span data-stu-id="62096-116">**Field**</span></span> | <span data-ttu-id="62096-117">**Leírás**</span><span class="sxs-lookup"><span data-stu-id="62096-117">**Description**</span></span> | <span data-ttu-id="62096-118">**Alsóbb rétegbeli hatás**</span><span class="sxs-lookup"><span data-stu-id="62096-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="62096-119">Adatfolyam neve</span><span class="sxs-lookup"><span data-stu-id="62096-119">Name</span></span> | <span data-ttu-id="62096-120">Az árajánlatsor neve, amely segít azonosítani a becslés alatt álló ajánlat elkülönített összetevőjét.</span><span class="sxs-lookup"><span data-stu-id="62096-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="62096-121">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="62096-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62096-122">Számlázási mód</span><span class="sxs-lookup"><span data-stu-id="62096-122">Billing Method</span></span> | <span data-ttu-id="62096-123">A lehetőségből létrehozott árajánlaton ezt az értéket a rendszer a lehetőség sor megfelelő mezőjéből másolja át.</span><span class="sxs-lookup"><span data-stu-id="62096-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="62096-124">Ez a mező a Dynamics 365 Project Operations által támogatott két fő szerződési modellt tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="62096-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="62096-125">- Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="62096-125">- Fixed price</span></span></br><span data-ttu-id="62096-126">- Idő és anyag</span><span class="sxs-lookup"><span data-stu-id="62096-126">- Time and material.</span></span>| <span data-ttu-id="62096-127">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="62096-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62096-128">Project</span><span class="sxs-lookup"><span data-stu-id="62096-128">Project</span></span> | <span data-ttu-id="62096-129">Ezzel a nem kötelező mezővel azonosíthatja azt a projektet, amelyet a program az adott tevékenységgel kapcsolatos munkára fog használni.</span><span class="sxs-lookup"><span data-stu-id="62096-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="62096-130">Amikor egy projektet egy ajánlati sorhoz rendelnek, az segítséget nyújt a felszámítható feladatok beállításában, valamint a projekten alapuló becslést hoz árajánlatsori részletekként az árajánlatsorba.</span><span class="sxs-lookup"><span data-stu-id="62096-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="62096-131">Ha egy projekt nincs leképezve projektalapú árajánlatsorra, a becslést kézzel kell létrehozni az egyes árajánlati sorok részleteinek létrehozásával.</span><span class="sxs-lookup"><span data-stu-id="62096-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="62096-132">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="62096-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62096-133">Idővel együtt</span><span class="sxs-lookup"><span data-stu-id="62096-133">Include Time</span></span> | <span data-ttu-id="62096-134">Az **Igen**/**Nem** jelző azt jelzi, hogy a kiválasztott projekten az időtranzakciók és a munkaerőköltségek szerepelni fognak-e az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="62096-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="62096-135">A **Nem** érték azt jelzi, hogy az időtranzakciók és a munkaerőköltségek nem fognak szerepelni az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="62096-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="62096-136">Az **Igen** érték azt jelzi, hogy az időtranzakciók és a munkaerőköltségek szerepelni fognak az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="62096-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="62096-137">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="62096-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62096-138">Költséggel együtt</span><span class="sxs-lookup"><span data-stu-id="62096-138">Include Expense</span></span> | <span data-ttu-id="62096-139">Az **Igen**/**Nem** jelző azt jelzi, hogy a kiválasztott projekten a kiadási költségek szerepelni fognak-e az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="62096-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="62096-140">A **Nem** érték azt jelzi, hogy a kiadási költségek nem fognak szerepelni az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="62096-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="62096-141">Az **Igen** érték azt jelzi, hogy a kiadási költségek szerepelni fognak az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="62096-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="62096-142">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="62096-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62096-143">Díjjal együtt</span><span class="sxs-lookup"><span data-stu-id="62096-143">Include Fee</span></span> | <span data-ttu-id="62096-144">Az **Igen**/**Nem** jelző azt jelzi, hogy a kiválasztott projekten a díjak szerepelni fognak-e az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="62096-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="62096-145">A **Nem** érték azt jelzi, hogy a díjak nem fognak szerepelni az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="62096-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="62096-146">Az **Igen** érték azt jelzi, hogy a díjak szerepelni fognak az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="62096-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="62096-147">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="62096-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62096-148">Megajánlott összeg</span><span class="sxs-lookup"><span data-stu-id="62096-148">Quoted Amount</span></span> | <span data-ttu-id="62096-149">Ez az összeg jelenik meg árajánlatként az ügyfélnek az összes előrejelzett munka esetében a projektalapú árajánlatsoron.</span><span class="sxs-lookup"><span data-stu-id="62096-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="62096-150">A lehetőségből létrehozott árajánlaton ezt az értéket a rendszer a lehetőség sor **Ügyfél költségvetése** mezőjéből másolja át.</span><span class="sxs-lookup"><span data-stu-id="62096-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="62096-151">Ha a projektalapú árajánlatsor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és az árajánlatsor részleteiben szereplő összegből kerül összesítésre.</span><span class="sxs-lookup"><span data-stu-id="62096-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="62096-152">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="62096-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62096-153">Becsült adó</span><span class="sxs-lookup"><span data-stu-id="62096-153">Estimated Tax</span></span> | <span data-ttu-id="62096-154">Ez egy szerkeszthető mező, amellyel a felhasználó hozzáadhatja a becsült adót az árajánlatsorhoz.</span><span class="sxs-lookup"><span data-stu-id="62096-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="62096-155">Ha a projektalapú árajánlatsor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és az árajánlatsor részleteiben szereplő adóösszegből kerül összesítésre.</span><span class="sxs-lookup"><span data-stu-id="62096-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="62096-156">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="62096-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62096-157">Árajánlat összege adózás után</span><span class="sxs-lookup"><span data-stu-id="62096-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="62096-158">Ez a mező az árajánlatsor adózás utáni összege, amely csak olvasható.</span><span class="sxs-lookup"><span data-stu-id="62096-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="62096-159">Az ebben a mezőben szereplő összeget a program *Árajánlat összege + adó* képlettel számítja ki.</span><span class="sxs-lookup"><span data-stu-id="62096-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="62096-160">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="62096-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62096-161">Nem meghaladandó korlát</span><span class="sxs-lookup"><span data-stu-id="62096-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="62096-162">Ez a mező szerkeszthető, és csak azokban a projektalapú árajánlatsorokban érhető el, amelyek **Idő és anyag** számlázási móddal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="62096-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="62096-163">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="62096-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62096-164">Ügyfél költségvetése</span><span class="sxs-lookup"><span data-stu-id="62096-164">Customer Budget</span></span> | <span data-ttu-id="62096-165">A mező szerkeszthető, és a rendszer a lehetőség sor megfelelő mezőjéből másolja át, ha az árajánlat egy lehetőségből lett létrehozva.</span><span class="sxs-lookup"><span data-stu-id="62096-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="62096-166">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="62096-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="62096-167">A projektalapú árajánlatsorok Általános lapján található mezőkre vonatkozó ellenőrzési szabályok</span><span class="sxs-lookup"><span data-stu-id="62096-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="62096-168">**1. szabály**: A kijelölt projekt bizonyos tranzakciós osztályai csak az árajánlat egy projektalapú árajánlatsorában szerepelhetnek.</span><span class="sxs-lookup"><span data-stu-id="62096-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="62096-169">**2. szabály**: Ha a lehetőség több árajánlattal rendelkezik, akkor különböző árajánlatokból származó ajánlati sorok szerepelhetnek, amelyek ugyanarra a projektre hivatkoznak, és ugyanazt a tranzakciós osztályt tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="62096-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="62096-170">**3. szabály**: Ha az ajánlatok nem ugyanahhoz a lehetőséghez tartoznak, akkor nem tartalmazhatják ugyanazokat a projekt- és tranzakciós osztályokat.</span><span class="sxs-lookup"><span data-stu-id="62096-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="62096-171">
                    <strong>Lehetőség</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62096-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="62096-172">
                    <strong>Ajánlat</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62096-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="62096-173">
                    <strong>Árajánlatsor</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62096-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="62096-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62096-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="62096-175">
                    <strong>Idővel együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62096-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="62096-176">
                    <strong>Költséggel együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62096-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="62096-177">
                    <strong>Ezzel együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62096-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="62096-178">
                    <strong>Díj</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62096-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="62096-179">
                    <strong>Érvényes/nem érvényes</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62096-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="62096-180">
                    <strong>Ok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62096-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="62096-181">L1</span><span class="sxs-lookup"><span data-stu-id="62096-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62096-182">N1</span><span class="sxs-lookup"><span data-stu-id="62096-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-183">ÁS1</span><span class="sxs-lookup"><span data-stu-id="62096-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-184">I1</span><span class="sxs-lookup"><span data-stu-id="62096-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-185">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-186">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-187">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="62096-188">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="62096-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="62096-189">Az 1. szabály megsértése.</span><span class="sxs-lookup"><span data-stu-id="62096-189">Violation of Rule #1.</span></span> <span data-ttu-id="62096-190">A P1 projektre vonatkozó időt, költséget és díjat mindkét árajánlatsor (ÁS1 és ÁS2) tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="62096-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="62096-191">L1</span><span class="sxs-lookup"><span data-stu-id="62096-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62096-192">N1</span><span class="sxs-lookup"><span data-stu-id="62096-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-193">ÁS2</span><span class="sxs-lookup"><span data-stu-id="62096-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-194">I1</span><span class="sxs-lookup"><span data-stu-id="62096-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-195">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-196">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-197">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-197">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="62096-198">L1</span><span class="sxs-lookup"><span data-stu-id="62096-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62096-199">N1</span><span class="sxs-lookup"><span data-stu-id="62096-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-200">ÁS1</span><span class="sxs-lookup"><span data-stu-id="62096-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-201">I1</span><span class="sxs-lookup"><span data-stu-id="62096-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-202">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-203">Nincs</span><span class="sxs-lookup"><span data-stu-id="62096-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-204">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="62096-205">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="62096-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="62096-206">Az 1. szabály megsértése.</span><span class="sxs-lookup"><span data-stu-id="62096-206">Violation of Rule #1.</span></span> <span data-ttu-id="62096-207">A P1 projektre vonatkozó időt és díjakat mindkét árajánlatsor (ÁS1 és ÁS2) tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="62096-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="62096-208">L1</span><span class="sxs-lookup"><span data-stu-id="62096-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62096-209">N1</span><span class="sxs-lookup"><span data-stu-id="62096-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-210">ÁS2</span><span class="sxs-lookup"><span data-stu-id="62096-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-211">I1</span><span class="sxs-lookup"><span data-stu-id="62096-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-212">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-213">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-214">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-214">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="62096-215">L1</span><span class="sxs-lookup"><span data-stu-id="62096-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62096-216">N1</span><span class="sxs-lookup"><span data-stu-id="62096-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-217">ÁS1</span><span class="sxs-lookup"><span data-stu-id="62096-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-218">I1</span><span class="sxs-lookup"><span data-stu-id="62096-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-219">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-220">Nincs</span><span class="sxs-lookup"><span data-stu-id="62096-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-221">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="62096-222">Érvényes</span><span class="sxs-lookup"><span data-stu-id="62096-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="62096-223">A P1 projektre vonatkozó időt és díjat az ÁS1 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="62096-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="62096-224">A P1 projektre vonatkozó költséget az ÁS2 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="62096-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="62096-225">Az egyes árajánlatsorokban szereplő elemek között nincs átfedés, így az érvényes.</span><span class="sxs-lookup"><span data-stu-id="62096-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="62096-226">L1</span><span class="sxs-lookup"><span data-stu-id="62096-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62096-227">N1</span><span class="sxs-lookup"><span data-stu-id="62096-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-228">ÁS2</span><span class="sxs-lookup"><span data-stu-id="62096-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-229">I1</span><span class="sxs-lookup"><span data-stu-id="62096-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-230">Nincs</span><span class="sxs-lookup"><span data-stu-id="62096-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-231">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-232">Nincs</span><span class="sxs-lookup"><span data-stu-id="62096-232">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="62096-233">L1</span><span class="sxs-lookup"><span data-stu-id="62096-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62096-234">N1</span><span class="sxs-lookup"><span data-stu-id="62096-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-235">ÁS1</span><span class="sxs-lookup"><span data-stu-id="62096-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-236">I1</span><span class="sxs-lookup"><span data-stu-id="62096-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-237">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-238">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-239">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="62096-240">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="62096-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="62096-241">A fenti 1. szabály megsértése</span><span class="sxs-lookup"><span data-stu-id="62096-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="62096-242">Az Á1 tartalmazza a teljes P1 projektre vonatkozó időt, költségeket és díjakat.</span><span class="sxs-lookup"><span data-stu-id="62096-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="62096-243">Az ÁS2 tartalmazza a teljes P1 teljes projektre vonatkozó időt, költségeket és díjakat, és átfedésben van az Á1-ben szereplő elemekkel.</span><span class="sxs-lookup"><span data-stu-id="62096-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="62096-244">L1</span><span class="sxs-lookup"><span data-stu-id="62096-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62096-245">N1</span><span class="sxs-lookup"><span data-stu-id="62096-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-246">ÁS2</span><span class="sxs-lookup"><span data-stu-id="62096-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-247">I1</span><span class="sxs-lookup"><span data-stu-id="62096-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-248">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-249">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-250">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-250">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="62096-251">L1</span><span class="sxs-lookup"><span data-stu-id="62096-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62096-252">N1</span><span class="sxs-lookup"><span data-stu-id="62096-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-253">ÁS1</span><span class="sxs-lookup"><span data-stu-id="62096-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-254">I1</span><span class="sxs-lookup"><span data-stu-id="62096-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-255">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-256">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-257">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="62096-258">Érvényes</span><span class="sxs-lookup"><span data-stu-id="62096-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="62096-259">A 2. szabály alapján az Á1 és Á2 két árajánlat ugyanarra a lehetőségre, így mindkettő becsülheti egy projekt ugyanazon összetevőit.</span><span class="sxs-lookup"><span data-stu-id="62096-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="62096-260">L1</span><span class="sxs-lookup"><span data-stu-id="62096-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62096-261">N2</span><span class="sxs-lookup"><span data-stu-id="62096-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-262">ÁS1 az Á2-n:</span><span class="sxs-lookup"><span data-stu-id="62096-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-263">I1</span><span class="sxs-lookup"><span data-stu-id="62096-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-264">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-265">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-266">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-266">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="62096-267">L1</span><span class="sxs-lookup"><span data-stu-id="62096-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62096-268">N1</span><span class="sxs-lookup"><span data-stu-id="62096-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-269">ÁS1</span><span class="sxs-lookup"><span data-stu-id="62096-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-270">I1</span><span class="sxs-lookup"><span data-stu-id="62096-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-271">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-272">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-273">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="62096-274">Érvényes</span><span class="sxs-lookup"><span data-stu-id="62096-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="62096-275">A 3. szabály alapján az Á1 és Á2 két árajánlat különböző lehetőségekre, így nem becsülhetik ugyanazon projekt azonos összetevőit.</span><span class="sxs-lookup"><span data-stu-id="62096-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="62096-276">L2</span><span class="sxs-lookup"><span data-stu-id="62096-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62096-277">N1</span><span class="sxs-lookup"><span data-stu-id="62096-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-278">ÁS1</span><span class="sxs-lookup"><span data-stu-id="62096-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-279">I1</span><span class="sxs-lookup"><span data-stu-id="62096-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-280">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62096-281">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62096-282">Igen</span><span class="sxs-lookup"><span data-stu-id="62096-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="62096-283">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="62096-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
