---
title: Projektalapú árajánlatsorok áttekintése
description: Ez a témakör a projektalapú ajánlatsorok projektmunkához való használatáról tartalmaz tájékoztatást.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369874"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="42113-103">Projektalapú árajánlatsorok áttekintése</span><span class="sxs-lookup"><span data-stu-id="42113-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="42113-104">_**A következőre vonatkozik:** Egyszerű központi telepítés – proforma számlázás, Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="42113-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="42113-105">A projektalapú ajánlati sorok úgy vannak kialakítva, hogy elősegítsék az aktivitásra vonatkozó projektmunka becslését.</span><span class="sxs-lookup"><span data-stu-id="42113-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="42113-106">A projektalapú ajánlatsor felépítése a projektbecslésekhez a következő fogalmakkal bővül:</span><span class="sxs-lookup"><span data-stu-id="42113-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="42113-107">Számlázási mód</span><span class="sxs-lookup"><span data-stu-id="42113-107">Billing Method</span></span>
- <span data-ttu-id="42113-108">Projekt és feladatleképezés</span><span class="sxs-lookup"><span data-stu-id="42113-108">Project and Task Mapping</span></span>
- <span data-ttu-id="42113-109">Szerepeltetett tranzakciós osztályok</span><span class="sxs-lookup"><span data-stu-id="42113-109">Included Transaction classes</span></span>
- <span data-ttu-id="42113-110">Nem meghaladandó korlát</span><span class="sxs-lookup"><span data-stu-id="42113-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="42113-111">Felszámíthatósági beállítás</span><span class="sxs-lookup"><span data-stu-id="42113-111">Chargeability setup</span></span>
- <span data-ttu-id="42113-112">Becslés az ajánlati sor részleteinek használatával</span><span class="sxs-lookup"><span data-stu-id="42113-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="42113-113">Árajánlatsor ügyfelei</span><span class="sxs-lookup"><span data-stu-id="42113-113">Quote line Customers</span></span>

<span data-ttu-id="42113-114">A következő táblázat a projektalapú árajánlatsor **Általános** lapján található mezőkre vonatkozó információkat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="42113-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="42113-115">Ezek a mezők segítséget nyújtanak a projektmunka részletes, jól felépített becslési alapjainak kialakításában.</span><span class="sxs-lookup"><span data-stu-id="42113-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="42113-116">**Mező**</span><span class="sxs-lookup"><span data-stu-id="42113-116">**Field**</span></span> | <span data-ttu-id="42113-117">**Leírás**</span><span class="sxs-lookup"><span data-stu-id="42113-117">**Description**</span></span> | <span data-ttu-id="42113-118">**Alsóbb rétegbeli hatás**</span><span class="sxs-lookup"><span data-stu-id="42113-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="42113-119">Adatfolyam neve</span><span class="sxs-lookup"><span data-stu-id="42113-119">Name</span></span> | <span data-ttu-id="42113-120">Az árajánlatsor neve, amely segít azonosítani a becsült árajánlat különálló összetevőjét.</span><span class="sxs-lookup"><span data-stu-id="42113-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="42113-121">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="42113-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="42113-122">Számlázási mód</span><span class="sxs-lookup"><span data-stu-id="42113-122">Billing Method</span></span> | <span data-ttu-id="42113-123">A lehetőségből létrehozott árajánlaton ezt az értéket a rendszer a lehetőség sor megfelelő mezőjéből másolja át.</span><span class="sxs-lookup"><span data-stu-id="42113-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="42113-124">Ez a mező a Dynamics 365 Project Operations által támogatott két fő szerződési modellt tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="42113-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="42113-125">- Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="42113-125">- Fixed price</span></span></br><span data-ttu-id="42113-126">- Idő és anyag</span><span class="sxs-lookup"><span data-stu-id="42113-126">- Time and material.</span></span>| <span data-ttu-id="42113-127">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="42113-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="42113-128">Project</span><span class="sxs-lookup"><span data-stu-id="42113-128">Project</span></span> | <span data-ttu-id="42113-129">Ezzel a nem kötelező mezővel azonosíthatja azt a projektet, amelyet a program az adott tevékenységgel kapcsolatos munkára fog használni.</span><span class="sxs-lookup"><span data-stu-id="42113-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="42113-130">Amikor egy projektet egy ajánlati sorhoz rendelnek, az segítséget nyújt a felszámítható feladatok beállításában, valamint a projekten alapuló becslést hoz árajánlatsori részletekként az árajánlatsorba.</span><span class="sxs-lookup"><span data-stu-id="42113-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="42113-131">Ha egy projekt nincs leképezve projektalapú árajánlatsorra, a becslést kézzel kell létrehozni az egyes árajánlati sorok részleteinek létrehozásával.</span><span class="sxs-lookup"><span data-stu-id="42113-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="42113-132">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="42113-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="42113-133">Hozzáadott feladatok</span><span class="sxs-lookup"><span data-stu-id="42113-133">Included Tasks</span></span> | <span data-ttu-id="42113-134">Azt jelzi, hogy az árajánlatsor a kijelölt projekt összes vagy néhány projektfeladatához kerül-e felhasználásra.</span><span class="sxs-lookup"><span data-stu-id="42113-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="42113-135">Ez a mező az alábbi értékekkel rendelkezhet:</span><span class="sxs-lookup"><span data-stu-id="42113-135">This field has the following possible values:</span></span></br><span data-ttu-id="42113-136">- Összes projektfeladat</span><span class="sxs-lookup"><span data-stu-id="42113-136">- All project tasks</span></span></br><span data-ttu-id="42113-137">- Csak a kiválasztott projektfeladatok</span><span class="sxs-lookup"><span data-stu-id="42113-137">- Selected project tasks only</span></span></br><span data-ttu-id="42113-138">Ebben a mezőben az üres érték az **Összes projektfeladat** beállításnak felel meg.</span><span class="sxs-lookup"><span data-stu-id="42113-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="42113-139">Ha a **Csak kijelölt projektfeladatok** van kiválasztva a projektoldalon, akkor a **Feleadatszámlázási beállítás** fülön kiválaszthatja azokat a feladatokat, amelyek ehhez az árajánlatsorhoz társítják őket.</span><span class="sxs-lookup"><span data-stu-id="42113-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="42113-140">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="42113-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="42113-141">Idővel együtt</span><span class="sxs-lookup"><span data-stu-id="42113-141">Include Time</span></span> | <span data-ttu-id="42113-142">Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt időtranzakciói vagy munkaköltségei szerepelnek-e az árajánlatsor becslésében.</span><span class="sxs-lookup"><span data-stu-id="42113-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="42113-143">A **Nem** érték azt jelzi, hogy az időtranzakciók és a munkaerőköltségek nem fognak szerepelni az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="42113-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="42113-144">Az **Igen** érték azt jelzi, hogy az időtranzakciók és a munkaerőköltségek szerepelni fognak az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="42113-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="42113-145">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="42113-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="42113-146">Költséggel együtt</span><span class="sxs-lookup"><span data-stu-id="42113-146">Include Expense</span></span> | <span data-ttu-id="42113-147">Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt önköltségei szerepelnek-e az árajánlatsor becslésében.</span><span class="sxs-lookup"><span data-stu-id="42113-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="42113-148">A **Nem** érték azt jelzi, hogy a kiadási költségek nem fognak szerepelni az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="42113-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="42113-149">Az **Igen** érték azt jelzi, hogy a kiadási költségek szerepelni fognak az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="42113-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="42113-150">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="42113-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="42113-151">Anyaggal együtt</span><span class="sxs-lookup"><span data-stu-id="42113-151">Include Material</span></span> | <span data-ttu-id="42113-152">Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt anyagköltségei szerepelnek-e az árajánlatsor becslésében.</span><span class="sxs-lookup"><span data-stu-id="42113-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="42113-153">A **Nem** érték azt jelzi, hogy az anyagköltségek nem szerepelnek az árajánlatsor becslésében.</span><span class="sxs-lookup"><span data-stu-id="42113-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="42113-154">Az **Igen** érték azt jelzi, hogy az anyagköltségek szerepelnek az árajánlatsor becslésében.</span><span class="sxs-lookup"><span data-stu-id="42113-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="42113-155">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="42113-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="42113-156">Díjjal együtt</span><span class="sxs-lookup"><span data-stu-id="42113-156">Include Fee</span></span> | <span data-ttu-id="42113-157">Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt díjai szerepelnek-e az árajánlatsor becslésében.</span><span class="sxs-lookup"><span data-stu-id="42113-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="42113-158">A **Nem** érték azt jelzi, hogy a díjak nem fognak szerepelni az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="42113-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="42113-159">Az **Igen** érték azt jelzi, hogy a díjak szerepelni fognak az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="42113-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="42113-160">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="42113-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="42113-161">Megajánlott összeg</span><span class="sxs-lookup"><span data-stu-id="42113-161">Quoted Amount</span></span> | <span data-ttu-id="42113-162">Ez az az összeg, amelyet az ügyfélnek a projektalapú árajánlatsorban előre jelzett összes munkára ki fognak számlázni.</span><span class="sxs-lookup"><span data-stu-id="42113-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="42113-163">A lehetőségből létrehozott árajánlaton ezt az értéket a rendszer a lehetőség sor **Ügyfél költségvetése** mezőjéből másolja át.</span><span class="sxs-lookup"><span data-stu-id="42113-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="42113-164">Ha a projektalapú árajánlatsor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és az árajánlatsor részleteiben szereplő összegből kerül összesítésre.</span><span class="sxs-lookup"><span data-stu-id="42113-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="42113-165">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="42113-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="42113-166">Becsült adó</span><span class="sxs-lookup"><span data-stu-id="42113-166">Estimated Tax</span></span> | <span data-ttu-id="42113-167">Ez egy szerkeszthető mező, amellyel a felhasználó hozzáadhatja a becsült adót az árajánlatsorhoz.</span><span class="sxs-lookup"><span data-stu-id="42113-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="42113-168">Ha a projektalapú árajánlatsor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és az árajánlatsor részleteiben szereplő adóösszegből kerül összesítésre.</span><span class="sxs-lookup"><span data-stu-id="42113-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="42113-169">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="42113-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="42113-170">Árajánlat összege adózás után</span><span class="sxs-lookup"><span data-stu-id="42113-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="42113-171">Ez a mező az árajánlatsor adózás utáni összege, amely csak olvasható.</span><span class="sxs-lookup"><span data-stu-id="42113-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="42113-172">Az ebben a mezőben szereplő összeget a program *Árajánlat összege + adó* képlettel számítja ki.</span><span class="sxs-lookup"><span data-stu-id="42113-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="42113-173">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="42113-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="42113-174">Nem meghaladandó korlát</span><span class="sxs-lookup"><span data-stu-id="42113-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="42113-175">Ez a mező szerkeszthető, és csak azokban a projektalapú árajánlatsorokban érhető el, amelyek **Idő és anyag** számlázási móddal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="42113-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="42113-176">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="42113-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="42113-177">Ügyfél költségvetése</span><span class="sxs-lookup"><span data-stu-id="42113-177">Customer Budget</span></span> | <span data-ttu-id="42113-178">A mező szerkeszthető, és a rendszer a lehetőség sor megfelelő mezőjéből másolja át, ha az árajánlat egy lehetőségből lett létrehozva.</span><span class="sxs-lookup"><span data-stu-id="42113-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="42113-179">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="42113-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="42113-180">A projektalapú árajánlatsorok Általános lapján található mezőkre vonatkozó ellenőrzési szabályok</span><span class="sxs-lookup"><span data-stu-id="42113-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="42113-181">**1. szabály**: Ha a **Hozzáadott feladatok** mező üres, vagy ha az **Összes projektfeladat** értékre van beállítva, a projektet tartalmazza az árajánlatsor.</span><span class="sxs-lookup"><span data-stu-id="42113-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="42113-182">**2. szabály**: Ha a **Hozzáadott feladatok** mező üres, vagy ha az **Összes projektfeladat** értékre van beállítva, a projekt és egy bizonyos tranzakciós osztály csak az árajánlat egy projektalapú árajánlatsorában szerepelhet.</span><span class="sxs-lookup"><span data-stu-id="42113-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="42113-183">**3. szabály**: Ha a **Hozzáadott feladatok** mező a **Csak a kiválasztott projektfeladatok** értékre van beállítva, a projekt és egy bizonyos tranzakciós osztály az árajánlat több projektalapú árajánlatsorában szerepelhet.</span><span class="sxs-lookup"><span data-stu-id="42113-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="42113-184">**4. szabály**: Ha a lehetőség több árajánlattal rendelkezik, akkor különböző árajánlatokból származó ajánlati sorok szerepelhetnek, amelyek ugyanarra a projektre hivatkoznak, és ugyanazt a tranzakciós osztályt tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="42113-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="42113-185">**5. szabály**: Ha az ajánlatok nem ugyanahhoz a lehetőséghez tartoznak, akkor nem tartalmazhatják ugyanazokat a projekt- és tranzakciós osztályokat.</span><span class="sxs-lookup"><span data-stu-id="42113-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="42113-186">
                    <strong>Lehetőség</strong>
                </span><span class="sxs-lookup"><span data-stu-id="42113-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="42113-187">
                    <strong>Ajánlat</strong>
                </span><span class="sxs-lookup"><span data-stu-id="42113-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="42113-188">
                    <strong>Árajánlatsor</strong>
                </span><span class="sxs-lookup"><span data-stu-id="42113-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="42113-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="42113-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="42113-190">
                    <strong>Hozzáadott feladatok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="42113-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="42113-191">
                    <strong>Idővel együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="42113-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="42113-192">
                    <strong>Költséggel együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="42113-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="42113-193">
                    <strong>Anyaggal együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="42113-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="42113-194">
                    <strong>Tartalmazás</strong>
                </span><span class="sxs-lookup"><span data-stu-id="42113-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="42113-195">
                    <strong>Díj</strong>
                </span><span class="sxs-lookup"><span data-stu-id="42113-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="42113-196">
                    <strong>Érvényes/nem érvényes</strong>
                </span><span class="sxs-lookup"><span data-stu-id="42113-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="42113-197">
                    <strong>Ok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="42113-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="42113-198">L1</span><span class="sxs-lookup"><span data-stu-id="42113-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="42113-199">N1</span><span class="sxs-lookup"><span data-stu-id="42113-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="42113-200">ÁS1</span><span class="sxs-lookup"><span data-stu-id="42113-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-201">I1</span><span class="sxs-lookup"><span data-stu-id="42113-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="42113-202">Üres</span><span class="sxs-lookup"><span data-stu-id="42113-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="42113-203">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="42113-204">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="42113-205">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-206">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42113-207">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="42113-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42113-208">Az 2. szabály megsértése.</span><span class="sxs-lookup"><span data-stu-id="42113-208">Violation of Rule #2.</span></span> <span data-ttu-id="42113-209">A P1 projektre vonatkozó időt, költséget és díjat az ÁS1 és ÁS2 árajánlatsor tartalmazza</span><span class="sxs-lookup"><span data-stu-id="42113-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="42113-210">L1</span><span class="sxs-lookup"><span data-stu-id="42113-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="42113-211">N1</span><span class="sxs-lookup"><span data-stu-id="42113-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="42113-212">ÁS2</span><span class="sxs-lookup"><span data-stu-id="42113-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-213">I1</span><span class="sxs-lookup"><span data-stu-id="42113-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="42113-214">Üres</span><span class="sxs-lookup"><span data-stu-id="42113-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="42113-215">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="42113-216">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="42113-217">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-218">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="42113-219">L1</span><span class="sxs-lookup"><span data-stu-id="42113-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="42113-220">N1</span><span class="sxs-lookup"><span data-stu-id="42113-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="42113-221">ÁS1</span><span class="sxs-lookup"><span data-stu-id="42113-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-222">I1</span><span class="sxs-lookup"><span data-stu-id="42113-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="42113-223">Üres</span><span class="sxs-lookup"><span data-stu-id="42113-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="42113-224">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="42113-225">No</span><span class="sxs-lookup"><span data-stu-id="42113-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="42113-226">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-227">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42113-228">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="42113-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42113-229">Az 2. szabály megsértése.</span><span class="sxs-lookup"><span data-stu-id="42113-229">Violation of Rule #2.</span></span> <span data-ttu-id="42113-230">A P1 projektre vonatkozó időt, anyagot és díjat az ÁS1 és ÁS2 árajánlatsor tartalmazza</span><span class="sxs-lookup"><span data-stu-id="42113-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="42113-231">L1</span><span class="sxs-lookup"><span data-stu-id="42113-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="42113-232">N1</span><span class="sxs-lookup"><span data-stu-id="42113-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="42113-233">ÁS2</span><span class="sxs-lookup"><span data-stu-id="42113-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-234">I1</span><span class="sxs-lookup"><span data-stu-id="42113-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="42113-235">Üres</span><span class="sxs-lookup"><span data-stu-id="42113-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="42113-236">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="42113-237">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="42113-238">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-239">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="42113-240">L1</span><span class="sxs-lookup"><span data-stu-id="42113-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="42113-241">N1</span><span class="sxs-lookup"><span data-stu-id="42113-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="42113-242">ÁS1</span><span class="sxs-lookup"><span data-stu-id="42113-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-243">I1</span><span class="sxs-lookup"><span data-stu-id="42113-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="42113-244">Üres</span><span class="sxs-lookup"><span data-stu-id="42113-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="42113-245">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="42113-246">No</span><span class="sxs-lookup"><span data-stu-id="42113-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="42113-247">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-248">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42113-249">Érvényes</span><span class="sxs-lookup"><span data-stu-id="42113-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42113-250">A P1 projektre vonatkozó időt, anyagot és díjat az ÁS1 árajánlatsor tartalmazza</span><span class="sxs-lookup"><span data-stu-id="42113-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="42113-251">A P1 projektre vonatkozó költséget az ÁS2 tartalmazza</span><span class="sxs-lookup"><span data-stu-id="42113-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="42113-252">Nincs átfedés abban, hogy miket tartalmaznak az egyes árajánlatsorok, így ez érvényes.</span><span class="sxs-lookup"><span data-stu-id="42113-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="42113-253">L1</span><span class="sxs-lookup"><span data-stu-id="42113-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="42113-254">N1</span><span class="sxs-lookup"><span data-stu-id="42113-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="42113-255">ÁS2</span><span class="sxs-lookup"><span data-stu-id="42113-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-256">I1</span><span class="sxs-lookup"><span data-stu-id="42113-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="42113-257">Üres</span><span class="sxs-lookup"><span data-stu-id="42113-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="42113-258">No</span><span class="sxs-lookup"><span data-stu-id="42113-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="42113-259">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="42113-260">No</span><span class="sxs-lookup"><span data-stu-id="42113-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-261">No</span><span class="sxs-lookup"><span data-stu-id="42113-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="42113-262">L1</span><span class="sxs-lookup"><span data-stu-id="42113-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="42113-263">N1</span><span class="sxs-lookup"><span data-stu-id="42113-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="42113-264">ÁS1</span><span class="sxs-lookup"><span data-stu-id="42113-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-265">I1</span><span class="sxs-lookup"><span data-stu-id="42113-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="42113-266">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="42113-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="42113-267">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="42113-268">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="42113-269">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-270">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42113-271">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="42113-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42113-272">A 2. szabály megsértése</span><span class="sxs-lookup"><span data-stu-id="42113-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="42113-273">A Q1 tartalmazza a P1 projekttel kapcsolatos feladatok egy részhalmazának idejét, anyagát, költségeit és díjait</span><span class="sxs-lookup"><span data-stu-id="42113-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="42113-274">A QL2 tartalmazza az egész P1 projektre vonatkozó időt, költségeket és díjakat, ezért átfedésben van a Q1 sorral.</span><span class="sxs-lookup"><span data-stu-id="42113-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="42113-275">L1</span><span class="sxs-lookup"><span data-stu-id="42113-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="42113-276">N1</span><span class="sxs-lookup"><span data-stu-id="42113-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="42113-277">ÁS2</span><span class="sxs-lookup"><span data-stu-id="42113-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-278">I1</span><span class="sxs-lookup"><span data-stu-id="42113-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="42113-279">Üres</span><span class="sxs-lookup"><span data-stu-id="42113-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="42113-280">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="42113-281">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="42113-282">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-283">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="42113-284">L1</span><span class="sxs-lookup"><span data-stu-id="42113-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="42113-285">N1</span><span class="sxs-lookup"><span data-stu-id="42113-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="42113-286">ÁS1</span><span class="sxs-lookup"><span data-stu-id="42113-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-287">I1</span><span class="sxs-lookup"><span data-stu-id="42113-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="42113-288">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="42113-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="42113-289">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="42113-290">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="42113-291">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-292">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42113-293">Érvényes</span><span class="sxs-lookup"><span data-stu-id="42113-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42113-294">A 3. szabály szerint</span><span class="sxs-lookup"><span data-stu-id="42113-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="42113-295">a Q1 tartalmazza a P1 projekttel kapcsolatos feladatok egy részhalmazának idejét, anyagát, költségeit és díjait.</span><span class="sxs-lookup"><span data-stu-id="42113-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="42113-296">A QL2 tartalmazza a P1 projekttel kapcsolatos feladatok egy részhalmazának idejét, anyagát, költségeit és díjait.</span><span class="sxs-lookup"><span data-stu-id="42113-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="42113-297">Az egyetlen további ellenőrzés a QL1-es feladatok részhalmaza körül van, amely eltér a QL2-es feladatok részhalmazától, így biztosítva, hogy nincs átfedés.</span><span class="sxs-lookup"><span data-stu-id="42113-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="42113-298">Ezt a rendszer hajtja végre a feladatok társításakor.</span><span class="sxs-lookup"><span data-stu-id="42113-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="42113-299">L1</span><span class="sxs-lookup"><span data-stu-id="42113-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="42113-300">N1</span><span class="sxs-lookup"><span data-stu-id="42113-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="42113-301">ÁS2</span><span class="sxs-lookup"><span data-stu-id="42113-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-302">I1</span><span class="sxs-lookup"><span data-stu-id="42113-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="42113-303">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="42113-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="42113-304">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="42113-305">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="42113-306">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-307">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="42113-308">L1</span><span class="sxs-lookup"><span data-stu-id="42113-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="42113-309">N1</span><span class="sxs-lookup"><span data-stu-id="42113-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="42113-310">ÁS1</span><span class="sxs-lookup"><span data-stu-id="42113-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-311">I1</span><span class="sxs-lookup"><span data-stu-id="42113-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="42113-312">Összes projektfeladat vagy üres</span><span class="sxs-lookup"><span data-stu-id="42113-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="42113-313">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="42113-314">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="42113-315">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-316">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42113-317">Érvényes</span><span class="sxs-lookup"><span data-stu-id="42113-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42113-318">Az 5. szabály szerint a, Q1 és Q2 két árajánlat ugyanarra a lehetőségre, így mindkettő megbecsülheti a projekt ugyanazon összetevőit.</span><span class="sxs-lookup"><span data-stu-id="42113-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="42113-319">L1</span><span class="sxs-lookup"><span data-stu-id="42113-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="42113-320">N2</span><span class="sxs-lookup"><span data-stu-id="42113-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="42113-321">ÁS1</span><span class="sxs-lookup"><span data-stu-id="42113-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-322">I1</span><span class="sxs-lookup"><span data-stu-id="42113-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="42113-323">Összes projektfeladat vagy üres</span><span class="sxs-lookup"><span data-stu-id="42113-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="42113-324">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="42113-325">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="42113-326">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-327">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="42113-328">L1</span><span class="sxs-lookup"><span data-stu-id="42113-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="42113-329">N1</span><span class="sxs-lookup"><span data-stu-id="42113-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="42113-330">ÁS1</span><span class="sxs-lookup"><span data-stu-id="42113-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-331">I1</span><span class="sxs-lookup"><span data-stu-id="42113-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="42113-332">Összes projektfeladat vagy üres</span><span class="sxs-lookup"><span data-stu-id="42113-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="42113-333">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="42113-334">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="42113-335">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-336">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42113-337">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="42113-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42113-338">A 4. szabály szerint a, Q1 és Q2 két árajánlat különböző lehetőségekre, így nem becsülheti meg mindkettő a projekt ugyanazon összetevőit.</span><span class="sxs-lookup"><span data-stu-id="42113-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="42113-339">L2</span><span class="sxs-lookup"><span data-stu-id="42113-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="42113-340">N1</span><span class="sxs-lookup"><span data-stu-id="42113-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="42113-341">ÁS1</span><span class="sxs-lookup"><span data-stu-id="42113-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-342">I1</span><span class="sxs-lookup"><span data-stu-id="42113-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="42113-343">Összes projektfeladat vagy üres</span><span class="sxs-lookup"><span data-stu-id="42113-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="42113-344">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="42113-345">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="42113-346">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="42113-347">Igen</span><span class="sxs-lookup"><span data-stu-id="42113-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
