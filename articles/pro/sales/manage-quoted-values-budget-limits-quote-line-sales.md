---
title: Projektalapú árajánlatsorok áttekintése
description: Ez a témakör a projektalapú ajánlatsorok projektmunkához való használatáról tartalmaz tájékoztatást.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32337b05f09ef7c5b84fdff9870744d6367e2693
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994859"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="7c68a-103">Projektalapú árajánlatsorok áttekintése</span><span class="sxs-lookup"><span data-stu-id="7c68a-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="7c68a-104">_**A következőre vonatkozik:** Egyszerű központi telepítés – proforma számlázás, Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="7c68a-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7c68a-105">A projektalapú ajánlati sorok úgy vannak kialakítva, hogy elősegítsék az aktivitásra vonatkozó projektmunka becslését.</span><span class="sxs-lookup"><span data-stu-id="7c68a-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="7c68a-106">A projektalapú ajánlatsor felépítése a projektbecslésekhez a következő fogalmakkal bővül:</span><span class="sxs-lookup"><span data-stu-id="7c68a-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="7c68a-107">Számlázási mód</span><span class="sxs-lookup"><span data-stu-id="7c68a-107">Billing Method</span></span>
- <span data-ttu-id="7c68a-108">Projekt és feladatleképezés</span><span class="sxs-lookup"><span data-stu-id="7c68a-108">Project and Task Mapping</span></span>
- <span data-ttu-id="7c68a-109">Szerepeltetett tranzakciós osztályok</span><span class="sxs-lookup"><span data-stu-id="7c68a-109">Included Transaction classes</span></span>
- <span data-ttu-id="7c68a-110">Nem meghaladandó korlát</span><span class="sxs-lookup"><span data-stu-id="7c68a-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="7c68a-111">Felszámíthatósági beállítás</span><span class="sxs-lookup"><span data-stu-id="7c68a-111">Chargeability setup</span></span>
- <span data-ttu-id="7c68a-112">Becslés az ajánlati sor részleteinek használatával</span><span class="sxs-lookup"><span data-stu-id="7c68a-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="7c68a-113">Árajánlatsor ügyfelei</span><span class="sxs-lookup"><span data-stu-id="7c68a-113">Quote line Customers</span></span>

<span data-ttu-id="7c68a-114">A következő táblázat a projektalapú árajánlatsor **Általános** lapján található mezőkre vonatkozó információkat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="7c68a-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="7c68a-115">Ezek a mezők segítséget nyújtanak a projektmunka részletes, jól felépített becslési alapjainak kialakításában.</span><span class="sxs-lookup"><span data-stu-id="7c68a-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="7c68a-116">**Mező**</span><span class="sxs-lookup"><span data-stu-id="7c68a-116">**Field**</span></span> | <span data-ttu-id="7c68a-117">**Leírás**</span><span class="sxs-lookup"><span data-stu-id="7c68a-117">**Description**</span></span> | <span data-ttu-id="7c68a-118">**Alsóbb rétegbeli hatás**</span><span class="sxs-lookup"><span data-stu-id="7c68a-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="7c68a-119">Adatfolyam neve</span><span class="sxs-lookup"><span data-stu-id="7c68a-119">Name</span></span> | <span data-ttu-id="7c68a-120">Az árajánlatsor neve, amely segít azonosítani a becsült árajánlat különálló összetevőjét.</span><span class="sxs-lookup"><span data-stu-id="7c68a-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="7c68a-121">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="7c68a-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7c68a-122">Számlázási mód</span><span class="sxs-lookup"><span data-stu-id="7c68a-122">Billing Method</span></span> | <span data-ttu-id="7c68a-123">A lehetőségből létrehozott árajánlaton ezt az értéket a rendszer a lehetőség sor megfelelő mezőjéből másolja át.</span><span class="sxs-lookup"><span data-stu-id="7c68a-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="7c68a-124">Ez a mező a Dynamics 365 Project Operations által támogatott két fő szerződési modellt tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="7c68a-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="7c68a-125">- Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="7c68a-125">- Fixed price</span></span></br><span data-ttu-id="7c68a-126">- Idő és anyag</span><span class="sxs-lookup"><span data-stu-id="7c68a-126">- Time and material.</span></span>| <span data-ttu-id="7c68a-127">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="7c68a-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7c68a-128">Project</span><span class="sxs-lookup"><span data-stu-id="7c68a-128">Project</span></span> | <span data-ttu-id="7c68a-129">Ezzel a nem kötelező mezővel azonosíthatja azt a projektet, amelyet a program az adott tevékenységgel kapcsolatos munkára fog használni.</span><span class="sxs-lookup"><span data-stu-id="7c68a-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="7c68a-130">Amikor egy projektet egy ajánlati sorhoz rendelnek, az segítséget nyújt a felszámítható feladatok beállításában, valamint a projekten alapuló becslést hoz árajánlatsori részletekként az árajánlatsorba.</span><span class="sxs-lookup"><span data-stu-id="7c68a-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="7c68a-131">Ha egy projekt nincs leképezve projektalapú árajánlatsorra, a becslést kézzel kell létrehozni az egyes árajánlati sorok részleteinek létrehozásával.</span><span class="sxs-lookup"><span data-stu-id="7c68a-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="7c68a-132">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="7c68a-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="7c68a-133">Hozzáadott feladatok</span><span class="sxs-lookup"><span data-stu-id="7c68a-133">Included Tasks</span></span> | <span data-ttu-id="7c68a-134">Azt jelzi, hogy az árajánlatsor a kijelölt projekt összes vagy néhány projektfeladatához kerül-e felhasználásra.</span><span class="sxs-lookup"><span data-stu-id="7c68a-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="7c68a-135">Ez a mező az alábbi értékekkel rendelkezhet:</span><span class="sxs-lookup"><span data-stu-id="7c68a-135">This field has the following possible values:</span></span></br><span data-ttu-id="7c68a-136">- Összes projektfeladat</span><span class="sxs-lookup"><span data-stu-id="7c68a-136">- All project tasks</span></span></br><span data-ttu-id="7c68a-137">- Csak a kiválasztott projektfeladatok</span><span class="sxs-lookup"><span data-stu-id="7c68a-137">- Selected project tasks only</span></span></br><span data-ttu-id="7c68a-138">Ebben a mezőben az üres érték az **Összes projektfeladat** beállításnak felel meg.</span><span class="sxs-lookup"><span data-stu-id="7c68a-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="7c68a-139">Ha a **Csak kijelölt projektfeladatok** van kiválasztva a projektoldalon, akkor a **Feleadatszámlázási beállítás** fülön kiválaszthatja azokat a feladatokat, amelyek ehhez az árajánlatsorhoz társítják őket.</span><span class="sxs-lookup"><span data-stu-id="7c68a-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="7c68a-140">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="7c68a-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7c68a-141">Idővel együtt</span><span class="sxs-lookup"><span data-stu-id="7c68a-141">Include Time</span></span> | <span data-ttu-id="7c68a-142">Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt időtranzakciói vagy munkaköltségei szerepelnek-e az árajánlatsor becslésében.</span><span class="sxs-lookup"><span data-stu-id="7c68a-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="7c68a-143">A **Nem** érték azt jelzi, hogy az időtranzakciók és a munkaerőköltségek nem fognak szerepelni az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="7c68a-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="7c68a-144">Az **Igen** érték azt jelzi, hogy az időtranzakciók és a munkaerőköltségek szerepelni fognak az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="7c68a-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="7c68a-145">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="7c68a-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7c68a-146">Költséggel együtt</span><span class="sxs-lookup"><span data-stu-id="7c68a-146">Include Expense</span></span> | <span data-ttu-id="7c68a-147">Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt önköltségei szerepelnek-e az árajánlatsor becslésében.</span><span class="sxs-lookup"><span data-stu-id="7c68a-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="7c68a-148">A **Nem** érték azt jelzi, hogy a kiadási költségek nem fognak szerepelni az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="7c68a-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="7c68a-149">Az **Igen** érték azt jelzi, hogy a kiadási költségek szerepelni fognak az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="7c68a-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="7c68a-150">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="7c68a-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7c68a-151">Anyaggal együtt</span><span class="sxs-lookup"><span data-stu-id="7c68a-151">Include Material</span></span> | <span data-ttu-id="7c68a-152">Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt anyagköltségei szerepelnek-e az árajánlatsor becslésében.</span><span class="sxs-lookup"><span data-stu-id="7c68a-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="7c68a-153">A **Nem** érték azt jelzi, hogy az anyagköltségek nem szerepelnek az árajánlatsor becslésében.</span><span class="sxs-lookup"><span data-stu-id="7c68a-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="7c68a-154">Az **Igen** érték azt jelzi, hogy az anyagköltségek szerepelnek az árajánlatsor becslésében.</span><span class="sxs-lookup"><span data-stu-id="7c68a-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="7c68a-155">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="7c68a-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7c68a-156">Díjjal együtt</span><span class="sxs-lookup"><span data-stu-id="7c68a-156">Include Fee</span></span> | <span data-ttu-id="7c68a-157">Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt díjai szerepelnek-e az árajánlatsor becslésében.</span><span class="sxs-lookup"><span data-stu-id="7c68a-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="7c68a-158">A **Nem** érték azt jelzi, hogy a díjak nem fognak szerepelni az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="7c68a-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="7c68a-159">Az **Igen** érték azt jelzi, hogy a díjak szerepelni fognak az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="7c68a-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="7c68a-160">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="7c68a-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7c68a-161">Megajánlott összeg</span><span class="sxs-lookup"><span data-stu-id="7c68a-161">Quoted Amount</span></span> | <span data-ttu-id="7c68a-162">Ez az az összeg, amelyet az ügyfélnek a projektalapú árajánlatsorban előre jelzett összes munkára ki fognak számlázni.</span><span class="sxs-lookup"><span data-stu-id="7c68a-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="7c68a-163">A lehetőségből létrehozott árajánlaton ezt az értéket a rendszer a lehetőség sor **Ügyfél költségvetése** mezőjéből másolja át.</span><span class="sxs-lookup"><span data-stu-id="7c68a-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="7c68a-164">Ha a projektalapú árajánlatsor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és az árajánlatsor részleteiben szereplő összegből kerül összesítésre.</span><span class="sxs-lookup"><span data-stu-id="7c68a-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="7c68a-165">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="7c68a-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7c68a-166">Becsült adó</span><span class="sxs-lookup"><span data-stu-id="7c68a-166">Estimated Tax</span></span> | <span data-ttu-id="7c68a-167">Ez egy szerkeszthető mező, amellyel a felhasználó hozzáadhatja a becsült adót az árajánlatsorhoz.</span><span class="sxs-lookup"><span data-stu-id="7c68a-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="7c68a-168">Ha a projektalapú árajánlatsor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és az árajánlatsor részleteiben szereplő adóösszegből kerül összesítésre.</span><span class="sxs-lookup"><span data-stu-id="7c68a-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="7c68a-169">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="7c68a-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7c68a-170">Árajánlat összege adózás után</span><span class="sxs-lookup"><span data-stu-id="7c68a-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="7c68a-171">Ez a mező az árajánlatsor adózás utáni összege, amely csak olvasható.</span><span class="sxs-lookup"><span data-stu-id="7c68a-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="7c68a-172">Az ebben a mezőben szereplő összeget a program *Árajánlat összege + adó* képlettel számítja ki.</span><span class="sxs-lookup"><span data-stu-id="7c68a-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="7c68a-173">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="7c68a-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7c68a-174">Nem meghaladandó korlát</span><span class="sxs-lookup"><span data-stu-id="7c68a-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="7c68a-175">Ez a mező szerkeszthető, és csak azokban a projektalapú árajánlatsorokban érhető el, amelyek **Idő és anyag** számlázási móddal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="7c68a-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="7c68a-176">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="7c68a-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7c68a-177">Ügyfél költségvetése</span><span class="sxs-lookup"><span data-stu-id="7c68a-177">Customer Budget</span></span> | <span data-ttu-id="7c68a-178">A mező szerkeszthető, és a rendszer a lehetőség sor megfelelő mezőjéből másolja át, ha az árajánlat egy lehetőségből lett létrehozva.</span><span class="sxs-lookup"><span data-stu-id="7c68a-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="7c68a-179">Ez az érték az árajánlat megnyerésekor az árajánlatsorból létrehozott projektszerződéssorba lesz átmásolva.</span><span class="sxs-lookup"><span data-stu-id="7c68a-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="7c68a-180">A projektalapú árajánlatsorok Általános lapján található mezőkre vonatkozó ellenőrzési szabályok</span><span class="sxs-lookup"><span data-stu-id="7c68a-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="7c68a-181">**1. szabály**: Ha a **Hozzáadott feladatok** mező üres, vagy ha az **Összes projektfeladat** értékre van beállítva, a projektet tartalmazza az árajánlatsor.</span><span class="sxs-lookup"><span data-stu-id="7c68a-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="7c68a-182">**2. szabály**: Ha a **Hozzáadott feladatok** mező üres, vagy ha az **Összes projektfeladat** értékre van beállítva, a projekt és egy bizonyos tranzakciós osztály csak az árajánlat egy projektalapú árajánlatsorában szerepelhet.</span><span class="sxs-lookup"><span data-stu-id="7c68a-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="7c68a-183">**3. szabály**: Ha a **Hozzáadott feladatok** mező a **Csak a kiválasztott projektfeladatok** értékre van beállítva, a projekt és egy bizonyos tranzakciós osztály az árajánlat több projektalapú árajánlatsorában szerepelhet.</span><span class="sxs-lookup"><span data-stu-id="7c68a-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="7c68a-184">**4. szabály**: Ha a lehetőség több árajánlattal rendelkezik, akkor különböző árajánlatokból származó ajánlati sorok szerepelhetnek, amelyek ugyanarra a projektre hivatkoznak, és ugyanazt a tranzakciós osztályt tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="7c68a-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="7c68a-185">**5. szabály**: Ha az ajánlatok nem ugyanahhoz a lehetőséghez tartoznak, akkor nem tartalmazhatják ugyanazokat a projekt- és tranzakciós osztályokat.</span><span class="sxs-lookup"><span data-stu-id="7c68a-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="7c68a-186">
                    <strong>Lehetőség</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7c68a-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="7c68a-187">
                    <strong>Ajánlat</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7c68a-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="7c68a-188">
                    <strong>Árajánlatsor</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7c68a-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="7c68a-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7c68a-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="7c68a-190">
                    <strong>Hozzáadott feladatok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7c68a-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="7c68a-191">
                    <strong>Idővel együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7c68a-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="7c68a-192">
                    <strong>Költséggel együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7c68a-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="7c68a-193">
                    <strong>Anyaggal együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7c68a-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="7c68a-194">
                    <strong>Tartalmazás</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7c68a-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="7c68a-195">
                    <strong>Díj</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7c68a-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="7c68a-196">
                    <strong>Érvényes/nem érvényes</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7c68a-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="7c68a-197">
                    <strong>Ok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7c68a-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="7c68a-198">L1</span><span class="sxs-lookup"><span data-stu-id="7c68a-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="7c68a-199">N1</span><span class="sxs-lookup"><span data-stu-id="7c68a-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="7c68a-200">ÁS1</span><span class="sxs-lookup"><span data-stu-id="7c68a-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-201">I1</span><span class="sxs-lookup"><span data-stu-id="7c68a-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="7c68a-202">Üres</span><span class="sxs-lookup"><span data-stu-id="7c68a-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="7c68a-203">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="7c68a-204">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="7c68a-205">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-206">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7c68a-207">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="7c68a-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7c68a-208">Az 2. szabály megsértése.</span><span class="sxs-lookup"><span data-stu-id="7c68a-208">Violation of Rule #2.</span></span> <span data-ttu-id="7c68a-209">A P1 projektre vonatkozó időt, költséget és díjat az ÁS1 és ÁS2 árajánlatsor tartalmazza</span><span class="sxs-lookup"><span data-stu-id="7c68a-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="7c68a-210">L1</span><span class="sxs-lookup"><span data-stu-id="7c68a-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="7c68a-211">N1</span><span class="sxs-lookup"><span data-stu-id="7c68a-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="7c68a-212">ÁS2</span><span class="sxs-lookup"><span data-stu-id="7c68a-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-213">I1</span><span class="sxs-lookup"><span data-stu-id="7c68a-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="7c68a-214">Üres</span><span class="sxs-lookup"><span data-stu-id="7c68a-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="7c68a-215">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="7c68a-216">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="7c68a-217">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-218">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-218">Yes</span></span> </p>
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
<span data-ttu-id="7c68a-219">L1</span><span class="sxs-lookup"><span data-stu-id="7c68a-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="7c68a-220">N1</span><span class="sxs-lookup"><span data-stu-id="7c68a-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="7c68a-221">ÁS1</span><span class="sxs-lookup"><span data-stu-id="7c68a-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-222">I1</span><span class="sxs-lookup"><span data-stu-id="7c68a-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="7c68a-223">Üres</span><span class="sxs-lookup"><span data-stu-id="7c68a-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="7c68a-224">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="7c68a-225">No</span><span class="sxs-lookup"><span data-stu-id="7c68a-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="7c68a-226">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-227">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7c68a-228">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="7c68a-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7c68a-229">Az 2. szabály megsértése.</span><span class="sxs-lookup"><span data-stu-id="7c68a-229">Violation of Rule #2.</span></span> <span data-ttu-id="7c68a-230">A P1 projektre vonatkozó időt, anyagot és díjat az ÁS1 és ÁS2 árajánlatsor tartalmazza</span><span class="sxs-lookup"><span data-stu-id="7c68a-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="7c68a-231">L1</span><span class="sxs-lookup"><span data-stu-id="7c68a-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="7c68a-232">N1</span><span class="sxs-lookup"><span data-stu-id="7c68a-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="7c68a-233">ÁS2</span><span class="sxs-lookup"><span data-stu-id="7c68a-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-234">I1</span><span class="sxs-lookup"><span data-stu-id="7c68a-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="7c68a-235">Üres</span><span class="sxs-lookup"><span data-stu-id="7c68a-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="7c68a-236">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="7c68a-237">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="7c68a-238">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-239">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-239">Yes</span></span> </p>
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
<span data-ttu-id="7c68a-240">L1</span><span class="sxs-lookup"><span data-stu-id="7c68a-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="7c68a-241">N1</span><span class="sxs-lookup"><span data-stu-id="7c68a-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="7c68a-242">ÁS1</span><span class="sxs-lookup"><span data-stu-id="7c68a-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-243">I1</span><span class="sxs-lookup"><span data-stu-id="7c68a-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="7c68a-244">Üres</span><span class="sxs-lookup"><span data-stu-id="7c68a-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="7c68a-245">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="7c68a-246">No</span><span class="sxs-lookup"><span data-stu-id="7c68a-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="7c68a-247">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-248">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7c68a-249">Érvényes</span><span class="sxs-lookup"><span data-stu-id="7c68a-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7c68a-250">A P1 projektre vonatkozó időt, anyagot és díjat az ÁS1 árajánlatsor tartalmazza</span><span class="sxs-lookup"><span data-stu-id="7c68a-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="7c68a-251">A P1 projektre vonatkozó költséget az ÁS2 tartalmazza</span><span class="sxs-lookup"><span data-stu-id="7c68a-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="7c68a-252">Nincs átfedés abban, hogy miket tartalmaznak az egyes árajánlatsorok, így ez érvényes.</span><span class="sxs-lookup"><span data-stu-id="7c68a-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="7c68a-253">L1</span><span class="sxs-lookup"><span data-stu-id="7c68a-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="7c68a-254">N1</span><span class="sxs-lookup"><span data-stu-id="7c68a-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="7c68a-255">ÁS2</span><span class="sxs-lookup"><span data-stu-id="7c68a-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-256">I1</span><span class="sxs-lookup"><span data-stu-id="7c68a-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="7c68a-257">Üres</span><span class="sxs-lookup"><span data-stu-id="7c68a-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="7c68a-258">No</span><span class="sxs-lookup"><span data-stu-id="7c68a-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="7c68a-259">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="7c68a-260">No</span><span class="sxs-lookup"><span data-stu-id="7c68a-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-261">No</span><span class="sxs-lookup"><span data-stu-id="7c68a-261">No</span></span> </p>
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
<span data-ttu-id="7c68a-262">L1</span><span class="sxs-lookup"><span data-stu-id="7c68a-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="7c68a-263">N1</span><span class="sxs-lookup"><span data-stu-id="7c68a-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="7c68a-264">ÁS1</span><span class="sxs-lookup"><span data-stu-id="7c68a-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-265">I1</span><span class="sxs-lookup"><span data-stu-id="7c68a-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="7c68a-266">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="7c68a-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="7c68a-267">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="7c68a-268">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="7c68a-269">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-270">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7c68a-271">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="7c68a-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7c68a-272">A 2. szabály megsértése</span><span class="sxs-lookup"><span data-stu-id="7c68a-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="7c68a-273">A Q1 tartalmazza a P1 projekttel kapcsolatos feladatok egy részhalmazának idejét, anyagát, költségeit és díjait</span><span class="sxs-lookup"><span data-stu-id="7c68a-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="7c68a-274">A QL2 tartalmazza az egész P1 projektre vonatkozó időt, költségeket és díjakat, ezért átfedésben van a Q1 sorral.</span><span class="sxs-lookup"><span data-stu-id="7c68a-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="7c68a-275">L1</span><span class="sxs-lookup"><span data-stu-id="7c68a-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="7c68a-276">N1</span><span class="sxs-lookup"><span data-stu-id="7c68a-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="7c68a-277">ÁS2</span><span class="sxs-lookup"><span data-stu-id="7c68a-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-278">I1</span><span class="sxs-lookup"><span data-stu-id="7c68a-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="7c68a-279">Üres</span><span class="sxs-lookup"><span data-stu-id="7c68a-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="7c68a-280">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="7c68a-281">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="7c68a-282">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-283">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-283">Yes</span></span> </p>
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
<span data-ttu-id="7c68a-284">L1</span><span class="sxs-lookup"><span data-stu-id="7c68a-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="7c68a-285">N1</span><span class="sxs-lookup"><span data-stu-id="7c68a-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="7c68a-286">ÁS1</span><span class="sxs-lookup"><span data-stu-id="7c68a-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-287">I1</span><span class="sxs-lookup"><span data-stu-id="7c68a-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="7c68a-288">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="7c68a-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="7c68a-289">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="7c68a-290">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="7c68a-291">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-292">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7c68a-293">Érvényes</span><span class="sxs-lookup"><span data-stu-id="7c68a-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7c68a-294">A 3. szabály szerint</span><span class="sxs-lookup"><span data-stu-id="7c68a-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="7c68a-295">a Q1 tartalmazza a P1 projekttel kapcsolatos feladatok egy részhalmazának idejét, anyagát, költségeit és díjait.</span><span class="sxs-lookup"><span data-stu-id="7c68a-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="7c68a-296">A QL2 tartalmazza a P1 projekttel kapcsolatos feladatok egy részhalmazának idejét, anyagát, költségeit és díjait.</span><span class="sxs-lookup"><span data-stu-id="7c68a-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="7c68a-297">Az egyetlen további ellenőrzés a QL1-es feladatok részhalmaza körül van, amely eltér a QL2-es feladatok részhalmazától, így biztosítva, hogy nincs átfedés.</span><span class="sxs-lookup"><span data-stu-id="7c68a-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="7c68a-298">Ezt a rendszer hajtja végre a feladatok társításakor.</span><span class="sxs-lookup"><span data-stu-id="7c68a-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="7c68a-299">L1</span><span class="sxs-lookup"><span data-stu-id="7c68a-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="7c68a-300">N1</span><span class="sxs-lookup"><span data-stu-id="7c68a-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="7c68a-301">ÁS2</span><span class="sxs-lookup"><span data-stu-id="7c68a-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-302">I1</span><span class="sxs-lookup"><span data-stu-id="7c68a-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="7c68a-303">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="7c68a-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="7c68a-304">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="7c68a-305">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="7c68a-306">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-307">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-307">Yes</span></span> </p>
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
<span data-ttu-id="7c68a-308">L1</span><span class="sxs-lookup"><span data-stu-id="7c68a-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="7c68a-309">N1</span><span class="sxs-lookup"><span data-stu-id="7c68a-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="7c68a-310">ÁS1</span><span class="sxs-lookup"><span data-stu-id="7c68a-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-311">I1</span><span class="sxs-lookup"><span data-stu-id="7c68a-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="7c68a-312">Összes projektfeladat vagy üres</span><span class="sxs-lookup"><span data-stu-id="7c68a-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="7c68a-313">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="7c68a-314">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="7c68a-315">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-316">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7c68a-317">Érvényes</span><span class="sxs-lookup"><span data-stu-id="7c68a-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7c68a-318">Az 5. szabály szerint a, Q1 és Q2 két árajánlat ugyanarra a lehetőségre, így mindkettő megbecsülheti a projekt ugyanazon összetevőit.</span><span class="sxs-lookup"><span data-stu-id="7c68a-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="7c68a-319">L1</span><span class="sxs-lookup"><span data-stu-id="7c68a-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="7c68a-320">N2</span><span class="sxs-lookup"><span data-stu-id="7c68a-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="7c68a-321">ÁS1</span><span class="sxs-lookup"><span data-stu-id="7c68a-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-322">I1</span><span class="sxs-lookup"><span data-stu-id="7c68a-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="7c68a-323">Összes projektfeladat vagy üres</span><span class="sxs-lookup"><span data-stu-id="7c68a-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="7c68a-324">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="7c68a-325">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="7c68a-326">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-327">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-327">Yes</span></span> </p>
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
<span data-ttu-id="7c68a-328">L1</span><span class="sxs-lookup"><span data-stu-id="7c68a-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="7c68a-329">N1</span><span class="sxs-lookup"><span data-stu-id="7c68a-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="7c68a-330">ÁS1</span><span class="sxs-lookup"><span data-stu-id="7c68a-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-331">I1</span><span class="sxs-lookup"><span data-stu-id="7c68a-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="7c68a-332">Összes projektfeladat vagy üres</span><span class="sxs-lookup"><span data-stu-id="7c68a-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="7c68a-333">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="7c68a-334">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="7c68a-335">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-336">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7c68a-337">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="7c68a-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7c68a-338">A 4. szabály szerint a, Q1 és Q2 két árajánlat különböző lehetőségekre, így nem becsülheti meg mindkettő a projekt ugyanazon összetevőit.</span><span class="sxs-lookup"><span data-stu-id="7c68a-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="7c68a-339">L2</span><span class="sxs-lookup"><span data-stu-id="7c68a-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="7c68a-340">N1</span><span class="sxs-lookup"><span data-stu-id="7c68a-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="7c68a-341">ÁS1</span><span class="sxs-lookup"><span data-stu-id="7c68a-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-342">I1</span><span class="sxs-lookup"><span data-stu-id="7c68a-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="7c68a-343">Összes projektfeladat vagy üres</span><span class="sxs-lookup"><span data-stu-id="7c68a-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="7c68a-344">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="7c68a-345">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="7c68a-346">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7c68a-347">Igen</span><span class="sxs-lookup"><span data-stu-id="7c68a-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
