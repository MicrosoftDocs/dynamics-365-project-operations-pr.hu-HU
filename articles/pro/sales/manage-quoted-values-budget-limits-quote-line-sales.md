---
title: Projektalapú árajánlatsorok áttekintése - Lite
description: Ez a témakör a projektalapú ajánlatsorok projektmunkához való használatáról tartalmaz tájékoztatást. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4865c06691fba09eacf5fe6449adfaf542444520
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272976"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="2add5-104">Projektalapú árajánlatsorok áttekintése - Lite</span><span class="sxs-lookup"><span data-stu-id="2add5-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="2add5-105">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="2add5-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2add5-106">A projektalapú ajánlati sorok úgy vannak kialakítva, hogy elősegítsék az aktivitásra vonatkozó projektmunka becslését.</span><span class="sxs-lookup"><span data-stu-id="2add5-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="2add5-107">A projektalapú ajánlatsor felépítése a projektbecslésekhez a következő fogalmakkal bővül:</span><span class="sxs-lookup"><span data-stu-id="2add5-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="2add5-108">Számlázási mód</span><span class="sxs-lookup"><span data-stu-id="2add5-108">Billing Method</span></span>
- <span data-ttu-id="2add5-109">Projekt és feladatleképezés</span><span class="sxs-lookup"><span data-stu-id="2add5-109">Project and Task Mapping</span></span>
- <span data-ttu-id="2add5-110">Szerepeltetett tranzakciós osztályok</span><span class="sxs-lookup"><span data-stu-id="2add5-110">Included Transaction classes</span></span>
- <span data-ttu-id="2add5-111">Nem meghaladandó korlát</span><span class="sxs-lookup"><span data-stu-id="2add5-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="2add5-112">Felszámíthatósági beállítás</span><span class="sxs-lookup"><span data-stu-id="2add5-112">Chargeability setup</span></span>
- <span data-ttu-id="2add5-113">Becslés az ajánlati sor részleteinek használatával</span><span class="sxs-lookup"><span data-stu-id="2add5-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="2add5-114">Árajánlatsor ügyfelei</span><span class="sxs-lookup"><span data-stu-id="2add5-114">Quote line Customers</span></span>

<span data-ttu-id="2add5-115">A következő táblázat a projektalapú árajánlatsor **Általános** lapján található mezőkre vonatkozó információkat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2add5-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="2add5-116">Ezek a mezők segítséget nyújtanak a projektmunka részletes, jól felépített becslési alapjainak kialakításában.</span><span class="sxs-lookup"><span data-stu-id="2add5-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="2add5-117">**Mező**</span><span class="sxs-lookup"><span data-stu-id="2add5-117">**Field**</span></span> | <span data-ttu-id="2add5-118">**Leírás**</span><span class="sxs-lookup"><span data-stu-id="2add5-118">**Description**</span></span> | <span data-ttu-id="2add5-119">**Alsóbb rétegbeli hatás**</span><span class="sxs-lookup"><span data-stu-id="2add5-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="2add5-120">Adatfolyam neve</span><span class="sxs-lookup"><span data-stu-id="2add5-120">Name</span></span> | <span data-ttu-id="2add5-121">Az árajánlatsor neve, amely segít azonosítani a becslés alatt álló ajánlat elkülönített összetevőjét.</span><span class="sxs-lookup"><span data-stu-id="2add5-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="2add5-122">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="2add5-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2add5-123">Számlázási mód</span><span class="sxs-lookup"><span data-stu-id="2add5-123">Billing Method</span></span> | <span data-ttu-id="2add5-124">A lehetőségből létrehozott árajánlaton ezt az értéket a rendszer a lehetőség sor megfelelő mezőjéből másolja át.</span><span class="sxs-lookup"><span data-stu-id="2add5-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="2add5-125">Ez a mező a Dynamics 365 Project Operations által támogatott két fő szerződési modellt tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="2add5-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="2add5-126">- Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="2add5-126">- Fixed price</span></span></br><span data-ttu-id="2add5-127">- Idő és anyag</span><span class="sxs-lookup"><span data-stu-id="2add5-127">- Time and material.</span></span>| <span data-ttu-id="2add5-128">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="2add5-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2add5-129">Project</span><span class="sxs-lookup"><span data-stu-id="2add5-129">Project</span></span> | <span data-ttu-id="2add5-130">Ezzel a nem kötelező mezővel azonosíthatja azt a projektet, amelyet a program az adott tevékenységgel kapcsolatos munkára fog használni.</span><span class="sxs-lookup"><span data-stu-id="2add5-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="2add5-131">Amikor egy projektet egy ajánlati sorhoz rendelnek, az segítséget nyújt a felszámítható feladatok beállításában, valamint a projekten alapuló becslést hoz árajánlatsori részletekként az árajánlatsorba.</span><span class="sxs-lookup"><span data-stu-id="2add5-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="2add5-132">Ha egy projekt nincs leképezve projektalapú árajánlatsorra, a becslést kézzel kell létrehozni az egyes árajánlati sorok részleteinek létrehozásával.</span><span class="sxs-lookup"><span data-stu-id="2add5-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="2add5-133">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="2add5-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="2add5-134">Hozzáadott feladatok</span><span class="sxs-lookup"><span data-stu-id="2add5-134">Included Tasks</span></span> | <span data-ttu-id="2add5-135">Azt jelzi, hogy az árajánlatsor a kijelölt projekt összes vagy néhány projektfeladatához kerül-e felhasználásra.</span><span class="sxs-lookup"><span data-stu-id="2add5-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="2add5-136">Ez a mező az alábbi értékekkel rendelkezhet:</span><span class="sxs-lookup"><span data-stu-id="2add5-136">This field has the following possible values:</span></span></br><span data-ttu-id="2add5-137">- Összes projektfeladat</span><span class="sxs-lookup"><span data-stu-id="2add5-137">- All project tasks</span></span></br><span data-ttu-id="2add5-138">- Csak a kiválasztott projektfeladatok</span><span class="sxs-lookup"><span data-stu-id="2add5-138">- Selected project tasks only</span></span></br><span data-ttu-id="2add5-139">Ebben a mezőben az üres érték az **Összes projektfeladat** beállításnak felel meg.</span><span class="sxs-lookup"><span data-stu-id="2add5-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="2add5-140">Ha a **Csak a kiválasztott projektfeladatok** van bejelölve, akkor a projektoldalon, a **Feladat számlázási beállítása** lap lehetővé teszi, hogy konkrét feladatokat jelöljön ki, amelyeket ehhez az árajánlatsorhoz társít.</span><span class="sxs-lookup"><span data-stu-id="2add5-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="2add5-141">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="2add5-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2add5-142">Idővel együtt</span><span class="sxs-lookup"><span data-stu-id="2add5-142">Include Time</span></span> | <span data-ttu-id="2add5-143">Az **Igen**/**Nem** jelző azt jelzi, hogy a kiválasztott projekten az időtranzakciók és a munkaerőköltségek szerepelni fognak-e az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="2add5-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="2add5-144">A **Nem** érték azt jelzi, hogy az időtranzakciók és a munkaerőköltségek nem fognak szerepelni az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="2add5-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="2add5-145">Az **Igen** érték azt jelzi, hogy az időtranzakciók és a munkaerőköltségek szerepelni fognak az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="2add5-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="2add5-146">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="2add5-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2add5-147">Költséggel együtt</span><span class="sxs-lookup"><span data-stu-id="2add5-147">Include Expense</span></span> | <span data-ttu-id="2add5-148">Az **Igen**/**Nem** jelző azt jelzi, hogy a kiválasztott projekten a kiadási költségek szerepelni fognak-e az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="2add5-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="2add5-149">A **Nem** érték azt jelzi, hogy a kiadási költségek nem fognak szerepelni az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="2add5-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="2add5-150">Az **Igen** érték azt jelzi, hogy a kiadási költségek szerepelni fognak az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="2add5-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="2add5-151">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="2add5-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2add5-152">Díjjal együtt</span><span class="sxs-lookup"><span data-stu-id="2add5-152">Include Fee</span></span> | <span data-ttu-id="2add5-153">Az **Igen**/**Nem** jelző azt jelzi, hogy a kiválasztott projekten a díjak szerepelni fognak-e az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="2add5-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="2add5-154">A **Nem** érték azt jelzi, hogy a díjak nem fognak szerepelni az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="2add5-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="2add5-155">Az **Igen** érték azt jelzi, hogy a díjak szerepelni fognak az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="2add5-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="2add5-156">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="2add5-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2add5-157">Megajánlott összeg</span><span class="sxs-lookup"><span data-stu-id="2add5-157">Quoted Amount</span></span> | <span data-ttu-id="2add5-158">Ez az összeg jelenik meg árajánlatként az ügyfélnek az összes előrejelzett munka esetében a projektalapú árajánlatsoron.</span><span class="sxs-lookup"><span data-stu-id="2add5-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="2add5-159">A lehetőségből létrehozott árajánlaton ezt az értéket a rendszer a lehetőség sor **Ügyfél költségvetése** mezőjéből másolja át.</span><span class="sxs-lookup"><span data-stu-id="2add5-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="2add5-160">Ha a projektalapú árajánlatsor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és az árajánlatsor részleteiben szereplő összegből kerül összesítésre.</span><span class="sxs-lookup"><span data-stu-id="2add5-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="2add5-161">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="2add5-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2add5-162">Becsült adó</span><span class="sxs-lookup"><span data-stu-id="2add5-162">Estimated Tax</span></span> | <span data-ttu-id="2add5-163">Ez egy szerkeszthető mező, amellyel a felhasználó hozzáadhatja a becsült adót az árajánlatsorhoz.</span><span class="sxs-lookup"><span data-stu-id="2add5-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="2add5-164">Ha a projektalapú árajánlatsor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és az árajánlatsor részleteiben szereplő adóösszegből kerül összesítésre.</span><span class="sxs-lookup"><span data-stu-id="2add5-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="2add5-165">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="2add5-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2add5-166">Árajánlat összege adózás után</span><span class="sxs-lookup"><span data-stu-id="2add5-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="2add5-167">Ez a mező az árajánlatsor adózás utáni összege, amely csak olvasható.</span><span class="sxs-lookup"><span data-stu-id="2add5-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="2add5-168">Az ebben a mezőben szereplő összeget a program *Árajánlat összege + adó* képlettel számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2add5-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="2add5-169">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="2add5-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2add5-170">Nem meghaladandó korlát</span><span class="sxs-lookup"><span data-stu-id="2add5-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="2add5-171">Ez a mező szerkeszthető, és csak azokban a projektalapú árajánlatsorokban érhető el, amelyek **Idő és anyag** számlázási móddal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="2add5-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="2add5-172">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="2add5-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2add5-173">Ügyfél költségvetése</span><span class="sxs-lookup"><span data-stu-id="2add5-173">Customer Budget</span></span> | <span data-ttu-id="2add5-174">A mező szerkeszthető, és a rendszer a lehetőség sor megfelelő mezőjéből másolja át, ha az árajánlat egy lehetőségből lett létrehozva.</span><span class="sxs-lookup"><span data-stu-id="2add5-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="2add5-175">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="2add5-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="2add5-176">A projektalapú árajánlatsorok Általános lapján található mezőkre vonatkozó ellenőrzési szabályok</span><span class="sxs-lookup"><span data-stu-id="2add5-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="2add5-177">**1. szabály**: Ha a **Hozzáadott feladatok** mező üres, vagy ha az **Összes projektfeladat** értékre van beállítva, a projektet tartalmazza az árajánlatsor.</span><span class="sxs-lookup"><span data-stu-id="2add5-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="2add5-178">**2. szabály**: Ha a **Hozzáadott feladatok** mező üres, vagy ha az **Összes projektfeladat** értékre van beállítva, a projekt és egy bizonyos tranzakciós osztály csak az árajánlat egy projektalapú árajánlatsorában szerepelhet.</span><span class="sxs-lookup"><span data-stu-id="2add5-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="2add5-179">**3. szabály**: Ha a **Hozzáadott feladatok** mező a **Csak a kiválasztott projektfeladatok** értékre van beállítva, a projekt és egy bizonyos tranzakciós osztály az árajánlat több projektalapú árajánlatsorában szerepelhet.</span><span class="sxs-lookup"><span data-stu-id="2add5-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="2add5-180">**4. szabály**: Ha a lehetőség több árajánlattal rendelkezik, akkor különböző árajánlatokból származó ajánlati sorok szerepelhetnek, amelyek ugyanarra a projektre hivatkoznak, és ugyanazt a tranzakciós osztályt tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="2add5-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="2add5-181">**5. szabály**: Ha az ajánlatok nem ugyanahhoz a lehetőséghez tartoznak, akkor nem tartalmazhatják ugyanazokat a projekt- és tranzakciós osztályokat.</span><span class="sxs-lookup"><span data-stu-id="2add5-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="2add5-182">
                    <strong>Lehetőség</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2add5-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="2add5-183">
                    <strong>Ajánlat</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2add5-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="2add5-184">
                    <strong>Árajánlatsor</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2add5-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="2add5-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2add5-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="2add5-186">
                    <strong>Hozzáadott feladatok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2add5-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="2add5-187">
                    <strong>Idővel együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2add5-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="2add5-188">
                    <strong>Költséggel együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2add5-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="2add5-189">
                    <strong>Ezzel együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2add5-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="2add5-190">
                    <strong>Díj</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2add5-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="2add5-191">
                    <strong>Érvényes/nem érvényes</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2add5-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="2add5-192">
                    <strong>Ok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2add5-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2add5-193">L1</span><span class="sxs-lookup"><span data-stu-id="2add5-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2add5-194">N1</span><span class="sxs-lookup"><span data-stu-id="2add5-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-195">ÁS1</span><span class="sxs-lookup"><span data-stu-id="2add5-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-196">I1</span><span class="sxs-lookup"><span data-stu-id="2add5-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2add5-197">Üres</span><span class="sxs-lookup"><span data-stu-id="2add5-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-198">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-199">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-200">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2add5-201">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="2add5-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2add5-202">Az 2. szabály megsértése.</span><span class="sxs-lookup"><span data-stu-id="2add5-202">Violation of Rule #2.</span></span> <span data-ttu-id="2add5-203">A P1 projektre vonatkozó időt, költséget és díjat az ÁS1 és ÁS2 árajánlatsor tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2add5-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2add5-204">L1</span><span class="sxs-lookup"><span data-stu-id="2add5-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2add5-205">N1</span><span class="sxs-lookup"><span data-stu-id="2add5-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-206">ÁS2</span><span class="sxs-lookup"><span data-stu-id="2add5-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-207">I1</span><span class="sxs-lookup"><span data-stu-id="2add5-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2add5-208">Üres</span><span class="sxs-lookup"><span data-stu-id="2add5-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-209">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-210">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-211">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-211">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="2add5-212">L1</span><span class="sxs-lookup"><span data-stu-id="2add5-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2add5-213">N1</span><span class="sxs-lookup"><span data-stu-id="2add5-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-214">ÁS1</span><span class="sxs-lookup"><span data-stu-id="2add5-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-215">I1</span><span class="sxs-lookup"><span data-stu-id="2add5-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2add5-216">Üres</span><span class="sxs-lookup"><span data-stu-id="2add5-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-217">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-218">Nincs</span><span class="sxs-lookup"><span data-stu-id="2add5-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-219">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2add5-220">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="2add5-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2add5-221">Az 2. szabály megsértése.</span><span class="sxs-lookup"><span data-stu-id="2add5-221">Violation of Rule #2.</span></span> <span data-ttu-id="2add5-222">A P1 projektre vonatkozó időt és díjakat az ÁS1 és ÁS2 árajánlatsor tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2add5-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2add5-223">L1</span><span class="sxs-lookup"><span data-stu-id="2add5-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2add5-224">N1</span><span class="sxs-lookup"><span data-stu-id="2add5-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-225">ÁS2</span><span class="sxs-lookup"><span data-stu-id="2add5-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-226">I1</span><span class="sxs-lookup"><span data-stu-id="2add5-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2add5-227">Üres</span><span class="sxs-lookup"><span data-stu-id="2add5-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-228">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-229">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-230">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-230">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2add5-231">L1</span><span class="sxs-lookup"><span data-stu-id="2add5-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2add5-232">N1</span><span class="sxs-lookup"><span data-stu-id="2add5-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-233">ÁS1</span><span class="sxs-lookup"><span data-stu-id="2add5-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-234">I1</span><span class="sxs-lookup"><span data-stu-id="2add5-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2add5-235">Üres</span><span class="sxs-lookup"><span data-stu-id="2add5-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-236">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-237">Nincs</span><span class="sxs-lookup"><span data-stu-id="2add5-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-238">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2add5-239">Érvényes</span><span class="sxs-lookup"><span data-stu-id="2add5-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="2add5-240">A P1 projektre vonatkozó időt és díjakat az ÁS1 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2add5-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="2add5-241">A P1 projektre vonatkozó költséget az ÁS2 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2add5-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="2add5-242">Az egyes árajánlatsorokban szereplő elemek között nincs átfedés, így az érvényes.</span><span class="sxs-lookup"><span data-stu-id="2add5-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2add5-243">L1</span><span class="sxs-lookup"><span data-stu-id="2add5-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2add5-244">N1</span><span class="sxs-lookup"><span data-stu-id="2add5-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-245">ÁS2</span><span class="sxs-lookup"><span data-stu-id="2add5-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-246">I1</span><span class="sxs-lookup"><span data-stu-id="2add5-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2add5-247">Üres</span><span class="sxs-lookup"><span data-stu-id="2add5-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-248">Nincs</span><span class="sxs-lookup"><span data-stu-id="2add5-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-249">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-250">Nincs</span><span class="sxs-lookup"><span data-stu-id="2add5-250">No</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="2add5-251">L1</span><span class="sxs-lookup"><span data-stu-id="2add5-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2add5-252">N1</span><span class="sxs-lookup"><span data-stu-id="2add5-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-253">ÁS1</span><span class="sxs-lookup"><span data-stu-id="2add5-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-254">I1</span><span class="sxs-lookup"><span data-stu-id="2add5-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2add5-255">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="2add5-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-256">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-257">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-258">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2add5-259">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="2add5-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2add5-260">A fenti 2. szabály megsértése</span><span class="sxs-lookup"><span data-stu-id="2add5-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="2add5-261">Az Á1 tartalmazza az időt, a költségeket és a díjakat a P1 projekthez kapcsolódó feladatok egy részhalmazán.</span><span class="sxs-lookup"><span data-stu-id="2add5-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="2add5-262">Az ÁS2 tartalmazza a teljes P1 teljes projektre vonatkozó időt, költségeket és díjakat, és átfedésben van az Á1-ben szereplő elemekkel.</span><span class="sxs-lookup"><span data-stu-id="2add5-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2add5-263">L1</span><span class="sxs-lookup"><span data-stu-id="2add5-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2add5-264">N1</span><span class="sxs-lookup"><span data-stu-id="2add5-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-265">ÁS2</span><span class="sxs-lookup"><span data-stu-id="2add5-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-266">I1</span><span class="sxs-lookup"><span data-stu-id="2add5-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2add5-267">Üres</span><span class="sxs-lookup"><span data-stu-id="2add5-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-268">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-269">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-270">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-270">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2add5-271">L1</span><span class="sxs-lookup"><span data-stu-id="2add5-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2add5-272">N1</span><span class="sxs-lookup"><span data-stu-id="2add5-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-273">ÁS1</span><span class="sxs-lookup"><span data-stu-id="2add5-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-274">I1</span><span class="sxs-lookup"><span data-stu-id="2add5-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2add5-275">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="2add5-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-276">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-277">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-278">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2add5-279">Érvényes</span><span class="sxs-lookup"><span data-stu-id="2add5-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2add5-280">A fenti 3. szabály alapján,</span><span class="sxs-lookup"><span data-stu-id="2add5-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="2add5-281">Az Á1 tartalmazza az időt, a költségeket és a díjakat a P1 projekthez kapcsolódó feladatok egy részhalmazán.</span><span class="sxs-lookup"><span data-stu-id="2add5-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="2add5-282">Az ÁS2 tartalmazza az időt, a költségeket és a díjakat a P1 projekthez kapcsolódó feladatok egy részhalmazán.</span><span class="sxs-lookup"><span data-stu-id="2add5-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="2add5-283">Az egyetlen további érvényesítés az ÁS1 feladatainak csak azon részhalmazára vonatkozik, amelyek eltérnek az ÁS2 feladatainak részhalmaztól.</span><span class="sxs-lookup"><span data-stu-id="2add5-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="2add5-284">Ezzel biztosítható, hogy nincsenek átfedések.</span><span class="sxs-lookup"><span data-stu-id="2add5-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="2add5-285">Ezt a rendszer hajtja végre a feladatok társításakor.</span><span class="sxs-lookup"><span data-stu-id="2add5-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2add5-286">L1</span><span class="sxs-lookup"><span data-stu-id="2add5-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2add5-287">N1</span><span class="sxs-lookup"><span data-stu-id="2add5-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-288">ÁS2</span><span class="sxs-lookup"><span data-stu-id="2add5-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-289">I1</span><span class="sxs-lookup"><span data-stu-id="2add5-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2add5-290">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="2add5-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-291">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-292">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-293">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-293">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="2add5-294">L1</span><span class="sxs-lookup"><span data-stu-id="2add5-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2add5-295">N1</span><span class="sxs-lookup"><span data-stu-id="2add5-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-296">ÁS1</span><span class="sxs-lookup"><span data-stu-id="2add5-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-297">I1</span><span class="sxs-lookup"><span data-stu-id="2add5-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2add5-298">Összes projektfeladat vagy üres</span><span class="sxs-lookup"><span data-stu-id="2add5-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-299">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-300">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-301">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="2add5-302">Érvényes</span><span class="sxs-lookup"><span data-stu-id="2add5-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2add5-303">A 5. szabály alapján az Á1 és Á2 két árajánlat ugyanarra a lehetőségre, így mindkettő becsülheti egy projekt ugyanazon összetevőit.</span><span class="sxs-lookup"><span data-stu-id="2add5-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2add5-304">L1</span><span class="sxs-lookup"><span data-stu-id="2add5-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2add5-305">N2</span><span class="sxs-lookup"><span data-stu-id="2add5-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-306">ÁS1</span><span class="sxs-lookup"><span data-stu-id="2add5-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-307">I1</span><span class="sxs-lookup"><span data-stu-id="2add5-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2add5-308">Összes projektfeladat vagy üres</span><span class="sxs-lookup"><span data-stu-id="2add5-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-309">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-310">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-311">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-311">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="2add5-312">L1</span><span class="sxs-lookup"><span data-stu-id="2add5-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2add5-313">N1</span><span class="sxs-lookup"><span data-stu-id="2add5-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-314">ÁS1</span><span class="sxs-lookup"><span data-stu-id="2add5-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-315">I1</span><span class="sxs-lookup"><span data-stu-id="2add5-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2add5-316">Összes projektfeladat vagy üres</span><span class="sxs-lookup"><span data-stu-id="2add5-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-317">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-318">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-319">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="2add5-320">Érvényes</span><span class="sxs-lookup"><span data-stu-id="2add5-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2add5-321">A 4. szabály alapján az Á1 és Á2 két árajánlat különböző lehetőségekre, így nem becsülhetik ugyanazon projekt azonos összetevőit.</span><span class="sxs-lookup"><span data-stu-id="2add5-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2add5-322">L2</span><span class="sxs-lookup"><span data-stu-id="2add5-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2add5-323">N1</span><span class="sxs-lookup"><span data-stu-id="2add5-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-324">ÁS1</span><span class="sxs-lookup"><span data-stu-id="2add5-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-325">I1</span><span class="sxs-lookup"><span data-stu-id="2add5-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2add5-326">Összes projektfeladat vagy üres</span><span class="sxs-lookup"><span data-stu-id="2add5-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-327">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2add5-328">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2add5-329">Igen</span><span class="sxs-lookup"><span data-stu-id="2add5-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="2add5-330">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="2add5-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]