---
title: Projektalapú árajánlatsorok (Pro)
description: Ez a témakör a projektalapú ajánlatsorok projektmunkához való használatáról tartalmaz tájékoztatást. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078022"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="350e9-104">Projektalapú árajánlatsorok (Pro)</span><span class="sxs-lookup"><span data-stu-id="350e9-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="350e9-105">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="350e9-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="350e9-106">A projektalapú ajánlati sorok úgy vannak kialakítva, hogy elősegítsék az aktivitásra vonatkozó projektmunka becslését.</span><span class="sxs-lookup"><span data-stu-id="350e9-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="350e9-107">A projektalapú ajánlatsor felépítése a projektbecslésekhez a következő fogalmakkal bővül:</span><span class="sxs-lookup"><span data-stu-id="350e9-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="350e9-108">Számlázási mód</span><span class="sxs-lookup"><span data-stu-id="350e9-108">Billing Method</span></span>
- <span data-ttu-id="350e9-109">Projekt és feladatleképezés</span><span class="sxs-lookup"><span data-stu-id="350e9-109">Project and Task Mapping</span></span>
- <span data-ttu-id="350e9-110">Szerepeltetett tranzakciós osztályok</span><span class="sxs-lookup"><span data-stu-id="350e9-110">Included Transaction classes</span></span>
- <span data-ttu-id="350e9-111">Nem meghaladandó korlát</span><span class="sxs-lookup"><span data-stu-id="350e9-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="350e9-112">Felszámíthatósági beállítás</span><span class="sxs-lookup"><span data-stu-id="350e9-112">Chargeability setup</span></span>
- <span data-ttu-id="350e9-113">Becslés az ajánlati sor részleteinek használatával</span><span class="sxs-lookup"><span data-stu-id="350e9-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="350e9-114">Árajánlatsor ügyfelei</span><span class="sxs-lookup"><span data-stu-id="350e9-114">Quote line Customers</span></span>

<span data-ttu-id="350e9-115">A következő táblázat a projektalapú árajánlatsor **Általános** lapján található mezőkre vonatkozó információkat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="350e9-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="350e9-116">Ezek a mezők segítséget nyújtanak a projektmunka részletes, jól felépített becslési alapjainak kialakításában.</span><span class="sxs-lookup"><span data-stu-id="350e9-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="350e9-117">**Mező**</span><span class="sxs-lookup"><span data-stu-id="350e9-117">**Field**</span></span> | <span data-ttu-id="350e9-118">**Relevancia, cél és útmutatás**</span><span class="sxs-lookup"><span data-stu-id="350e9-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="350e9-119">**Alsóbb rétegbeli hatás**</span><span class="sxs-lookup"><span data-stu-id="350e9-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="350e9-120">Adatfolyam neve</span><span class="sxs-lookup"><span data-stu-id="350e9-120">Name</span></span> | <span data-ttu-id="350e9-121">Az árajánlatsor neve, amely segít azonosítani a becslés alatt álló ajánlat elkülönített összetevőjét.</span><span class="sxs-lookup"><span data-stu-id="350e9-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="350e9-122">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="350e9-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="350e9-123">Számlázási mód</span><span class="sxs-lookup"><span data-stu-id="350e9-123">Billing Method</span></span> | <span data-ttu-id="350e9-124">A lehetőségből létrehozott árajánlaton ezt az értéket a rendszer a lehetőség sor megfelelő mezőjéből másolja át.</span><span class="sxs-lookup"><span data-stu-id="350e9-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="350e9-125">Ez a mező a Dynamics 365 Project Operations által támogatott két fő szerződési modellt tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="350e9-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="350e9-126">- Rögzített ár</span><span class="sxs-lookup"><span data-stu-id="350e9-126">- Fixed price</span></span></br><span data-ttu-id="350e9-127">- Idő és anyag</span><span class="sxs-lookup"><span data-stu-id="350e9-127">- Time and material.</span></span>| <span data-ttu-id="350e9-128">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="350e9-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="350e9-129">Project</span><span class="sxs-lookup"><span data-stu-id="350e9-129">Project</span></span> | <span data-ttu-id="350e9-130">Ezzel a nem kötelező mezővel azonosíthatja azt a projektet, amelyet a program az adott tevékenységgel kapcsolatos munkára fog használni.</span><span class="sxs-lookup"><span data-stu-id="350e9-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="350e9-131">Amikor egy projektet egy ajánlati sorhoz rendelnek, az segítséget nyújt a felszámítható feladatok beállításában, valamint a projekten alapuló becslést hoz árajánlatsori részletekként az árajánlatsorba.</span><span class="sxs-lookup"><span data-stu-id="350e9-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="350e9-132">Ha egy projekt nincs leképezve projektalapú árajánlatsorra, a becslést kézzel kell létrehozni az egyes árajánlati sorok részleteinek létrehozásával.</span><span class="sxs-lookup"><span data-stu-id="350e9-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="350e9-133">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="350e9-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="350e9-134">Hozzáadott feladatok</span><span class="sxs-lookup"><span data-stu-id="350e9-134">Included Tasks</span></span> | <span data-ttu-id="350e9-135">Azt jelzi, hogy az árajánlatsor a kijelölt projekt összes vagy néhány projektfeladatához kerül-e felhasználásra.</span><span class="sxs-lookup"><span data-stu-id="350e9-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="350e9-136">Ez a mező az alábbi értékekkel rendelkezhet:</span><span class="sxs-lookup"><span data-stu-id="350e9-136">This field has the following possible values:</span></span></br><span data-ttu-id="350e9-137">- Összes projektfeladat</span><span class="sxs-lookup"><span data-stu-id="350e9-137">- All project tasks</span></span></br><span data-ttu-id="350e9-138">- Csak a kiválasztott projektfeladatok</span><span class="sxs-lookup"><span data-stu-id="350e9-138">- Selected project tasks only</span></span></br><span data-ttu-id="350e9-139">Ebben a mezőben az üres érték az **Összes projektfeladat** beállításnak felel meg.</span><span class="sxs-lookup"><span data-stu-id="350e9-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="350e9-140">Ha a **Csak a kiválasztott projektfeladatok** van bejelölve, akkor a projektoldalon, a **Feladat számlázási beállítása** lap lehetővé teszi, hogy konkrét feladatokat jelöljön ki, amelyeket ehhez az árajánlatsorhoz társít.</span><span class="sxs-lookup"><span data-stu-id="350e9-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="350e9-141">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="350e9-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="350e9-142">Idővel együtt</span><span class="sxs-lookup"><span data-stu-id="350e9-142">Include Time</span></span> | <span data-ttu-id="350e9-143">Az **Igen**/**Nem** jelző azt jelzi, hogy a kiválasztott projekten az időtranzakciók és a munkaerőköltségek szerepelni fognak-e az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="350e9-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="350e9-144">A **Nem** érték azt jelzi, hogy az időtranzakciók és a munkaerőköltségek nem fognak szerepelni az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="350e9-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="350e9-145">Az **Igen** érték azt jelzi, hogy az időtranzakciók és a munkaerőköltségek szerepelni fognak az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="350e9-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="350e9-146">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="350e9-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="350e9-147">Költséggel együtt</span><span class="sxs-lookup"><span data-stu-id="350e9-147">Include Expense</span></span> | <span data-ttu-id="350e9-148">Az **Igen**/**Nem** jelző azt jelzi, hogy a kiválasztott projekten a kiadási költségek szerepelni fognak-e az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="350e9-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="350e9-149">A **Nem** érték azt jelzi, hogy a kiadási költségek nem fognak szerepelni az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="350e9-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="350e9-150">Az **Igen** érték azt jelzi, hogy a kiadási költségek szerepelni fognak az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="350e9-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="350e9-151">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="350e9-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="350e9-152">Díjjal együtt</span><span class="sxs-lookup"><span data-stu-id="350e9-152">Include Fee</span></span> | <span data-ttu-id="350e9-153">Az **Igen**/**Nem** jelző azt jelzi, hogy a kiválasztott projekten a díjak szerepelni fognak-e az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="350e9-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="350e9-154">A **Nem** érték azt jelzi, hogy a díjak nem fognak szerepelni az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="350e9-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="350e9-155">Az **Igen** érték azt jelzi, hogy a díjak szerepelni fognak az árajánlatsorban szereplő becslésben.</span><span class="sxs-lookup"><span data-stu-id="350e9-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="350e9-156">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="350e9-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="350e9-157">Megajánlott összeg</span><span class="sxs-lookup"><span data-stu-id="350e9-157">Quoted Amount</span></span> | <span data-ttu-id="350e9-158">Ez az összeg jelenik meg árajánlatként az ügyfélnek az összes előrejelzett munka esetében a projektalapú árajánlatsoron.</span><span class="sxs-lookup"><span data-stu-id="350e9-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="350e9-159">A lehetőségből létrehozott árajánlaton ezt az értéket a rendszer a lehetőség sor **Ügyfél költségvetése** mezőjéből másolja át.</span><span class="sxs-lookup"><span data-stu-id="350e9-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="350e9-160">Ha a projektalapú árajánlatsor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és az árajánlatsor részleteiben szereplő összegből kerül összesítésre.</span><span class="sxs-lookup"><span data-stu-id="350e9-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="350e9-161">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="350e9-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="350e9-162">Becsült adó</span><span class="sxs-lookup"><span data-stu-id="350e9-162">Estimated Tax</span></span> | <span data-ttu-id="350e9-163">Ez egy szerkeszthető mező, amellyel a felhasználó hozzáadhatja a becsült adót az árajánlatsorhoz.</span><span class="sxs-lookup"><span data-stu-id="350e9-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="350e9-164">Ha a projektalapú árajánlatsor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és az árajánlatsor részleteiben szereplő adóösszegből kerül összesítésre.</span><span class="sxs-lookup"><span data-stu-id="350e9-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="350e9-165">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="350e9-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="350e9-166">Árajánlat összege adózás után</span><span class="sxs-lookup"><span data-stu-id="350e9-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="350e9-167">Ez a mező az árajánlatsor adózás utáni összege, amely csak olvasható.</span><span class="sxs-lookup"><span data-stu-id="350e9-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="350e9-168">Az ebben a mezőben szereplő összeget a program *Árajánlat összege + adó* képlettel számítja ki.</span><span class="sxs-lookup"><span data-stu-id="350e9-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="350e9-169">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="350e9-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="350e9-170">Nem meghaladandó korlát</span><span class="sxs-lookup"><span data-stu-id="350e9-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="350e9-171">Ez a mező szerkeszthető, és csak azokban a projektalapú árajánlatsorokban érhető el, amelyek **Idő és anyag** számlázási móddal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="350e9-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="350e9-172">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="350e9-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="350e9-173">Ügyfél költségvetése</span><span class="sxs-lookup"><span data-stu-id="350e9-173">Customer Budget</span></span> | <span data-ttu-id="350e9-174">A mező szerkeszthető, és a rendszer a lehetőség sor megfelelő mezőjéből másolja át, ha az árajánlat egy lehetőségből lett létrehozva.</span><span class="sxs-lookup"><span data-stu-id="350e9-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="350e9-175">A program az ebből az árajánlatból létrehozott projektszerződéssorba másolja ezt a mezőt az árajánlat megnyerése után.</span><span class="sxs-lookup"><span data-stu-id="350e9-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="350e9-176">A projektalapú árajánlatsorok Általános lapján található mezőkre vonatkozó ellenőrzési szabályok</span><span class="sxs-lookup"><span data-stu-id="350e9-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="350e9-177">**1. szabály** : Ha a **Hozzáadott feladatok** mező üres, vagy ha az **Összes projektfeladat** értékre van beállítva, a projektet tartalmazza az árajánlatsor.</span><span class="sxs-lookup"><span data-stu-id="350e9-177">**Rule 1** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project is included in the quote line.</span></span>

<span data-ttu-id="350e9-178">**2. szabály** : Ha a **Hozzáadott feladatok** mező üres, vagy ha az **Összes projektfeladat** értékre van beállítva, a projekt és egy bizonyos tranzakciós osztály csak az árajánlat egy projektalapú árajánlatsorában szerepelhet.</span><span class="sxs-lookup"><span data-stu-id="350e9-178">**Rule 2** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="350e9-179">**3. szabály** : Ha a **Hozzáadott feladatok** mező a **Csak a kiválasztott projektfeladatok** értékre van beállítva, a projekt és egy bizonyos tranzakciós osztály az árajánlat több projektalapú árajánlatsorában szerepelhet.</span><span class="sxs-lookup"><span data-stu-id="350e9-179">**Rule 3** : If the **Included Tasks** field is set to **Selected project tasks only** , a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="350e9-180">**4. szabály** : Ha a lehetőség több árajánlattal rendelkezik, akkor különböző árajánlatokból származó ajánlati sorok szerepelhetnek, amelyek ugyanarra a projektre hivatkoznak, és ugyanazt a tranzakciós osztályt tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="350e9-180">**Rule 4** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="350e9-181">**5. szabály** : Ha az ajánlatok nem ugyanahhoz a lehetőséghez tartoznak, akkor nem tartalmazhatják ugyanazokat a projekt- és tranzakciós osztályokat.</span><span class="sxs-lookup"><span data-stu-id="350e9-181">**Rule 5** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="350e9-182">
                    <strong>Lehetőség</strong>
                </span><span class="sxs-lookup"><span data-stu-id="350e9-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="350e9-183">
                    <strong>Ajánlat</strong>
                </span><span class="sxs-lookup"><span data-stu-id="350e9-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="350e9-184">
                    <strong>Árajánlatsor</strong>
                </span><span class="sxs-lookup"><span data-stu-id="350e9-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="350e9-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="350e9-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="350e9-186">
                    <strong>Hozzáadott feladatok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="350e9-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="350e9-187">
                    <strong>Idővel együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="350e9-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="350e9-188">
                    <strong>Költséggel együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="350e9-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="350e9-189">
                    <strong>Ezzel együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="350e9-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="350e9-190">
                    <strong>Díj</strong>
                </span><span class="sxs-lookup"><span data-stu-id="350e9-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="350e9-191">
                    <strong>Érvényes/nem érvényes</strong>
                </span><span class="sxs-lookup"><span data-stu-id="350e9-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="350e9-192">
                    <strong>Ok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="350e9-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="350e9-193">L1</span><span class="sxs-lookup"><span data-stu-id="350e9-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="350e9-194">N1</span><span class="sxs-lookup"><span data-stu-id="350e9-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-195">ÁS1</span><span class="sxs-lookup"><span data-stu-id="350e9-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-196">I1</span><span class="sxs-lookup"><span data-stu-id="350e9-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="350e9-197">Üres</span><span class="sxs-lookup"><span data-stu-id="350e9-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-198">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-199">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-200">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="350e9-201">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="350e9-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="350e9-202">Az 2. szabály megsértése.</span><span class="sxs-lookup"><span data-stu-id="350e9-202">Violation of Rule #2.</span></span> <span data-ttu-id="350e9-203">A P1 projektre vonatkozó időt, költséget és díjat az ÁS1 és ÁS2 árajánlatsor tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="350e9-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="350e9-204">L1</span><span class="sxs-lookup"><span data-stu-id="350e9-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="350e9-205">N1</span><span class="sxs-lookup"><span data-stu-id="350e9-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-206">ÁS2</span><span class="sxs-lookup"><span data-stu-id="350e9-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-207">I1</span><span class="sxs-lookup"><span data-stu-id="350e9-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="350e9-208">Üres</span><span class="sxs-lookup"><span data-stu-id="350e9-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-209">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-210">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-211">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-211">Yes</span></span> </p>
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
<span data-ttu-id="350e9-212">L1</span><span class="sxs-lookup"><span data-stu-id="350e9-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="350e9-213">N1</span><span class="sxs-lookup"><span data-stu-id="350e9-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-214">ÁS1</span><span class="sxs-lookup"><span data-stu-id="350e9-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-215">I1</span><span class="sxs-lookup"><span data-stu-id="350e9-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="350e9-216">Üres</span><span class="sxs-lookup"><span data-stu-id="350e9-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-217">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-218">Nincs</span><span class="sxs-lookup"><span data-stu-id="350e9-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-219">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="350e9-220">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="350e9-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="350e9-221">Az 2. szabály megsértése.</span><span class="sxs-lookup"><span data-stu-id="350e9-221">Violation of Rule #2.</span></span> <span data-ttu-id="350e9-222">A P1 projektre vonatkozó időt és díjakat az ÁS1 és ÁS2 árajánlatsor tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="350e9-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="350e9-223">L1</span><span class="sxs-lookup"><span data-stu-id="350e9-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="350e9-224">N1</span><span class="sxs-lookup"><span data-stu-id="350e9-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-225">ÁS2</span><span class="sxs-lookup"><span data-stu-id="350e9-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-226">I1</span><span class="sxs-lookup"><span data-stu-id="350e9-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="350e9-227">Üres</span><span class="sxs-lookup"><span data-stu-id="350e9-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-228">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-229">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-230">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-230">Yes</span></span> </p>
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
<span data-ttu-id="350e9-231">L1</span><span class="sxs-lookup"><span data-stu-id="350e9-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="350e9-232">N1</span><span class="sxs-lookup"><span data-stu-id="350e9-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-233">ÁS1</span><span class="sxs-lookup"><span data-stu-id="350e9-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-234">I1</span><span class="sxs-lookup"><span data-stu-id="350e9-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="350e9-235">Üres</span><span class="sxs-lookup"><span data-stu-id="350e9-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-236">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-237">Nincs</span><span class="sxs-lookup"><span data-stu-id="350e9-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-238">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="350e9-239">Érvényes</span><span class="sxs-lookup"><span data-stu-id="350e9-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="350e9-240">A P1 projektre vonatkozó időt és díjakat az ÁS1 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="350e9-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="350e9-241">A P1 projektre vonatkozó költséget az ÁS2 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="350e9-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="350e9-242">Az egyes árajánlatsorokban szereplő elemek között nincs átfedés, így az érvényes.</span><span class="sxs-lookup"><span data-stu-id="350e9-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="350e9-243">L1</span><span class="sxs-lookup"><span data-stu-id="350e9-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="350e9-244">N1</span><span class="sxs-lookup"><span data-stu-id="350e9-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-245">ÁS2</span><span class="sxs-lookup"><span data-stu-id="350e9-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-246">I1</span><span class="sxs-lookup"><span data-stu-id="350e9-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="350e9-247">Üres</span><span class="sxs-lookup"><span data-stu-id="350e9-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-248">Nincs</span><span class="sxs-lookup"><span data-stu-id="350e9-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-249">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-250">Nincs</span><span class="sxs-lookup"><span data-stu-id="350e9-250">No</span></span> </p>
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
<span data-ttu-id="350e9-251">L1</span><span class="sxs-lookup"><span data-stu-id="350e9-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="350e9-252">N1</span><span class="sxs-lookup"><span data-stu-id="350e9-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-253">ÁS1</span><span class="sxs-lookup"><span data-stu-id="350e9-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-254">I1</span><span class="sxs-lookup"><span data-stu-id="350e9-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="350e9-255">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="350e9-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-256">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-257">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-258">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="350e9-259">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="350e9-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="350e9-260">A fenti 2. szabály megsértése</span><span class="sxs-lookup"><span data-stu-id="350e9-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="350e9-261">Az Á1 tartalmazza az időt, a költségeket és a díjakat a P1 projekthez kapcsolódó feladatok egy részhalmazán.</span><span class="sxs-lookup"><span data-stu-id="350e9-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="350e9-262">Az ÁS2 tartalmazza a teljes P1 teljes projektre vonatkozó időt, költségeket és díjakat, és átfedésben van az Á1-ben szereplő elemekkel.</span><span class="sxs-lookup"><span data-stu-id="350e9-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="350e9-263">L1</span><span class="sxs-lookup"><span data-stu-id="350e9-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="350e9-264">N1</span><span class="sxs-lookup"><span data-stu-id="350e9-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-265">ÁS2</span><span class="sxs-lookup"><span data-stu-id="350e9-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-266">I1</span><span class="sxs-lookup"><span data-stu-id="350e9-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="350e9-267">Üres</span><span class="sxs-lookup"><span data-stu-id="350e9-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-268">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-269">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-270">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-270">Yes</span></span> </p>
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
<span data-ttu-id="350e9-271">L1</span><span class="sxs-lookup"><span data-stu-id="350e9-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="350e9-272">N1</span><span class="sxs-lookup"><span data-stu-id="350e9-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-273">ÁS1</span><span class="sxs-lookup"><span data-stu-id="350e9-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-274">I1</span><span class="sxs-lookup"><span data-stu-id="350e9-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="350e9-275">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="350e9-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-276">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-277">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-278">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="350e9-279">Érvényes</span><span class="sxs-lookup"><span data-stu-id="350e9-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="350e9-280">A fenti 3. szabály alapján,</span><span class="sxs-lookup"><span data-stu-id="350e9-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="350e9-281">Az Á1 tartalmazza az időt, a költségeket és a díjakat a P1 projekthez kapcsolódó feladatok egy részhalmazán.</span><span class="sxs-lookup"><span data-stu-id="350e9-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="350e9-282">Az ÁS2 tartalmazza az időt, a költségeket és a díjakat a P1 projekthez kapcsolódó feladatok egy részhalmazán.</span><span class="sxs-lookup"><span data-stu-id="350e9-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="350e9-283">Az egyetlen további érvényesítés az ÁS1 feladatainak csak azon részhalmazára vonatkozik, amelyek eltérnek az ÁS2 feladatainak részhalmaztól.</span><span class="sxs-lookup"><span data-stu-id="350e9-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="350e9-284">Ezzel biztosítható, hogy nincsenek átfedések.</span><span class="sxs-lookup"><span data-stu-id="350e9-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="350e9-285">Ezt a rendszer hajtja végre a feladatok társításakor.</span><span class="sxs-lookup"><span data-stu-id="350e9-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="350e9-286">L1</span><span class="sxs-lookup"><span data-stu-id="350e9-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="350e9-287">N1</span><span class="sxs-lookup"><span data-stu-id="350e9-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-288">ÁS2</span><span class="sxs-lookup"><span data-stu-id="350e9-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-289">I1</span><span class="sxs-lookup"><span data-stu-id="350e9-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="350e9-290">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="350e9-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-291">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-292">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-293">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-293">Yes</span></span> </p>
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
<span data-ttu-id="350e9-294">L1</span><span class="sxs-lookup"><span data-stu-id="350e9-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="350e9-295">N1</span><span class="sxs-lookup"><span data-stu-id="350e9-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-296">ÁS1</span><span class="sxs-lookup"><span data-stu-id="350e9-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-297">I1</span><span class="sxs-lookup"><span data-stu-id="350e9-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="350e9-298">Összes projektfeladat vagy üres</span><span class="sxs-lookup"><span data-stu-id="350e9-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-299">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-300">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-301">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="350e9-302">Érvényes</span><span class="sxs-lookup"><span data-stu-id="350e9-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="350e9-303">A 5. szabály alapján az Á1 és Á2 két árajánlat ugyanarra a lehetőségre, így mindkettő becsülheti egy projekt ugyanazon összetevőit.</span><span class="sxs-lookup"><span data-stu-id="350e9-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="350e9-304">L1</span><span class="sxs-lookup"><span data-stu-id="350e9-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="350e9-305">N2</span><span class="sxs-lookup"><span data-stu-id="350e9-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-306">ÁS1</span><span class="sxs-lookup"><span data-stu-id="350e9-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-307">I1</span><span class="sxs-lookup"><span data-stu-id="350e9-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="350e9-308">Összes projektfeladat vagy üres</span><span class="sxs-lookup"><span data-stu-id="350e9-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-309">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-310">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-311">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-311">Yes</span></span> </p>
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
<span data-ttu-id="350e9-312">L1</span><span class="sxs-lookup"><span data-stu-id="350e9-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="350e9-313">N1</span><span class="sxs-lookup"><span data-stu-id="350e9-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-314">ÁS1</span><span class="sxs-lookup"><span data-stu-id="350e9-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-315">I1</span><span class="sxs-lookup"><span data-stu-id="350e9-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="350e9-316">Összes projektfeladat vagy üres</span><span class="sxs-lookup"><span data-stu-id="350e9-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-317">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-318">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-319">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="350e9-320">Érvényes</span><span class="sxs-lookup"><span data-stu-id="350e9-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="350e9-321">A 4. szabály alapján az Á1 és Á2 két árajánlat különböző lehetőségekre, így nem becsülhetik ugyanazon projekt azonos összetevőit.</span><span class="sxs-lookup"><span data-stu-id="350e9-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="350e9-322">L2</span><span class="sxs-lookup"><span data-stu-id="350e9-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="350e9-323">N1</span><span class="sxs-lookup"><span data-stu-id="350e9-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-324">ÁS1</span><span class="sxs-lookup"><span data-stu-id="350e9-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-325">I1</span><span class="sxs-lookup"><span data-stu-id="350e9-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="350e9-326">Összes projektfeladat vagy üres</span><span class="sxs-lookup"><span data-stu-id="350e9-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-327">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="350e9-328">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="350e9-329">Igen</span><span class="sxs-lookup"><span data-stu-id="350e9-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="350e9-330">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="350e9-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

