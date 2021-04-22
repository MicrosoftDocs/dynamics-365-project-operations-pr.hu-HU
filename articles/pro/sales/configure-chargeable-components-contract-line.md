---
title: A projektalapú szerződéssor felszámítható összetevőinek konfigurálása
description: Ez a témakör tájékoztatást nyújt arról, hogyan lehet a felszámítható összetevőket felvenni a Project Operations szerződéssoraiba.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858476"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="33a5b-103">A projektalapú szerződéssor felszámítható összetevőinek konfigurálása</span><span class="sxs-lookup"><span data-stu-id="33a5b-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="33a5b-104">_**A következőre vonatkozik:** Egyszerű központi telepítés – proforma számlázás, Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="33a5b-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="33a5b-105">A projektalapú szerződéssor rendelkezik *mellékelt* összetevőkkel és a *felszámítható* összetevőkkel.</span><span class="sxs-lookup"><span data-stu-id="33a5b-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="33a5b-106">A mellékelt összetevők olyan összetevők, amelyek a következőkhöz kapcsolódnak:</span><span class="sxs-lookup"><span data-stu-id="33a5b-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="33a5b-107">Számlázási mód és ügyfél felosztások</span><span class="sxs-lookup"><span data-stu-id="33a5b-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="33a5b-108">Nem meghaladandó korlátok</span><span class="sxs-lookup"><span data-stu-id="33a5b-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="33a5b-109">A projekt alapú szerződéssor által meghatározott számlázási gyakorisági beállításai</span><span class="sxs-lookup"><span data-stu-id="33a5b-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="33a5b-110">A befoglalt összetevők egy részhalmaza a **Számlázási típus** mező segítségével állítható terhelhetőre.</span><span class="sxs-lookup"><span data-stu-id="33a5b-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="33a5b-111">A **Számlázási típus** mező olyan értékkészlet, amely a szerződéssorok környezetében az alábbi értékeket teszi lehetővé:</span><span class="sxs-lookup"><span data-stu-id="33a5b-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="33a5b-112">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-112">Chargeable</span></span>
  - <span data-ttu-id="33a5b-113">Fel nem számítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-113">Non-chargeable</span></span>

<span data-ttu-id="33a5b-114">A felszámítható összetevők a feladatokon, szerepkörökön és tranzakciós kategóriákon határozhatók meg.</span><span class="sxs-lookup"><span data-stu-id="33a5b-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="33a5b-115">A felszámíthatóság a projekt szerződéssor feladataihoz van definiálva, és a sorban szereplő összes tranzakciós osztályra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="33a5b-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="33a5b-116">Ha a szerződéssor **Feladatok belefoglalása** mezője üres, vagy a **Teljes projekt** értékre van állítva, a **Felszámítható feladatok** lap nem lesz elérhető.</span><span class="sxs-lookup"><span data-stu-id="33a5b-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="33a5b-117">A Project szerződéssor szerepkörei meghatározott felszámíthatóság csak az **Idő** tranzakciós osztályra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="33a5b-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="33a5b-118">Ha a szerződéssor **Idő belefoglalása** mezője **Nem** értékre van állítva, a **Felszámítható feladatok** lap nem lesz elérhető.</span><span class="sxs-lookup"><span data-stu-id="33a5b-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="33a5b-119">A Project szerződéssor tranzakciós kategóriái meghatározott felszámíthatóság csak az **Költség** tranzakciós osztályra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="33a5b-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="33a5b-120">Ha a szerződéssor **Kiadások belefoglalása** mezője **Nem** értékre van állítva, a **Felszámítható kategóriák** lap nem lesz elérhető.</span><span class="sxs-lookup"><span data-stu-id="33a5b-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="33a5b-121">Projekttevékenység frissítése felszámítható vagy nem felszámítható értékre</span><span class="sxs-lookup"><span data-stu-id="33a5b-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="33a5b-122">A projekttevékenység egy adott szerződéssor felszámítható vagy nem felszámítható lehet, így a következő beállításokat lehet használni:</span><span class="sxs-lookup"><span data-stu-id="33a5b-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="33a5b-123">Ha egy projekten alapuló szerződéssor **Idő** típusú, és egy bizonyos feladatot tartalmaz, akkor a **T1** a felszámíthatóként van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="33a5b-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="33a5b-124">Ha van egy második szerződéssor , amely **Költséget** tartalmaz , akkor a T1 feladatot a szerződéssorok között nem felszámíthatóként társíthatja.</span><span class="sxs-lookup"><span data-stu-id="33a5b-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="33a5b-125">Az eredmény az, hogy a feladathoz rögzített összes idő felszámítható, és minden költség nem felszámítható.</span><span class="sxs-lookup"><span data-stu-id="33a5b-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="33a5b-126">A feladatok számlázási típusa a szerződéssor **Számlázható feladatok** lapján állítható be a szerződéssor-feladatok alrács **Számlázási típus** mezőjének frissítésével.</span><span class="sxs-lookup"><span data-stu-id="33a5b-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="33a5b-127">Másik lehetőségként frissítheti a **Számlázási típus** mezőt, a projekt számlázási beállítása alrácsán, amely a feladathoz társított szerződéssorokat mutatja.</span><span class="sxs-lookup"><span data-stu-id="33a5b-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="33a5b-128">Szerepkör frissítése felszámítható vagy nem felszámítható értékre</span><span class="sxs-lookup"><span data-stu-id="33a5b-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="33a5b-129">Egy szerepkör egy adott szerződéssoron felszámítható vagy nem felszámítható lehet.</span><span class="sxs-lookup"><span data-stu-id="33a5b-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="33a5b-130">A szerepkör számlázási típusa a szerződéssor **Számlázható szerepkörök** lapján állítható be.</span><span class="sxs-lookup"><span data-stu-id="33a5b-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="33a5b-131">Ehhez frissítse a **Számlázható szerepkörök** alrács **Számlázási típus** mezőjét.</span><span class="sxs-lookup"><span data-stu-id="33a5b-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="33a5b-132">Tranzakciókategória frissítése felszámítható vagy nem felszámítható értékre</span><span class="sxs-lookup"><span data-stu-id="33a5b-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="33a5b-133">Egy tranzakciós kategória egy adott szerződéssoron felszámítható vagy nem felszámítható lehet.</span><span class="sxs-lookup"><span data-stu-id="33a5b-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="33a5b-134">A tranzakció számlázási típusa a projektalapú szerződéssor **Számlázható kategóriák** lapján állítható be.</span><span class="sxs-lookup"><span data-stu-id="33a5b-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="33a5b-135">Ehhez frissítse a **Számlázható kategóriák** alrács **Számlázási típus** mezőjét.</span><span class="sxs-lookup"><span data-stu-id="33a5b-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="33a5b-136">A számlázhatóság feloldása</span><span class="sxs-lookup"><span data-stu-id="33a5b-136">Resolve chargeability</span></span>

<span data-ttu-id="33a5b-137">Az időre létrehozott becslés vagy tényadat csak akkor tekinthető felszámíthatónak, ha:</span><span class="sxs-lookup"><span data-stu-id="33a5b-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="33a5b-138">Az **Idő** szerepel a szerződéssorban.</span><span class="sxs-lookup"><span data-stu-id="33a5b-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="33a5b-139">A **Szerepkör** a szerződéssorban felszámíthatóként van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="33a5b-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="33a5b-140">A **Hozzáadott feladatok** érték **Kijelölt feladatok** elemre van állítva a szerződéssoron.</span><span class="sxs-lookup"><span data-stu-id="33a5b-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="33a5b-141">Ha ez a három dolog teljesül, akkor a feladat felszámíthatóként konfigurálható.</span><span class="sxs-lookup"><span data-stu-id="33a5b-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="33a5b-142">A költségre létrehozott becslés vagy tényadat csak akkor tekinthető felszámíthatónak, ha:</span><span class="sxs-lookup"><span data-stu-id="33a5b-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="33a5b-143">A **Költség** szerepel a szerződéssorban</span><span class="sxs-lookup"><span data-stu-id="33a5b-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="33a5b-144">A **Tranzakciókategória** a szerződéssorban felszámíthatóként van konfigurálva</span><span class="sxs-lookup"><span data-stu-id="33a5b-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="33a5b-145">A **Hozzáadott feladatok** érték **Kijelölt feladat** elemre van állítva a szerződéssoron</span><span class="sxs-lookup"><span data-stu-id="33a5b-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="33a5b-146">Ha ez a három dolog teljesül, akkor a **Feladat** felszámíthatóként konfigurálható.</span><span class="sxs-lookup"><span data-stu-id="33a5b-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="33a5b-147">Az anyagra létrehozott becslés vagy tényadat csak akkor tekinthető felszámíthatónak, ha:</span><span class="sxs-lookup"><span data-stu-id="33a5b-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="33a5b-148">Az **Anyagok** szerepel a szerződéssorban</span><span class="sxs-lookup"><span data-stu-id="33a5b-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="33a5b-149">A **Hozzáadott feladatok** érték **Kijelölt feladatok** elemre van állítva a szerződéssoron</span><span class="sxs-lookup"><span data-stu-id="33a5b-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="33a5b-150">Ha ez a két dolog teljesül, akkor a **Feladat** felszámíthatóként konfigurálható.</span><span class="sxs-lookup"><span data-stu-id="33a5b-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="33a5b-151">
                    <strong>Időt tartalmaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="33a5b-152">
                    <strong>Költséget tartalmaz</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="33a5b-153">
                    <strong>Anyagokkal együtt</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="33a5b-154">
                    <strong>Hozzáadott feladatok</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="33a5b-155">
                    <strong>Szerepkör</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="33a5b-156">
                    <strong>Kategória</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="33a5b-157">
                    <strong>Feladatok</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="33a5b-158">
                    <strong>Felszámolhatósági hatás</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="33a5b-159">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="33a5b-160">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="33a5b-161">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="33a5b-162">Teljes projekt</span><span class="sxs-lookup"><span data-stu-id="33a5b-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="33a5b-163">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="33a5b-164">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="33a5b-165">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="33a5b-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="33a5b-166">Számlázás egy tényleges Időhöz: <strong>Számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="33a5b-167">Számlázás típusa egy tényleges kiadáshoz: <strong>Számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="33a5b-168">Számlázási típus a tényanyagon: <strong>Számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="33a5b-169">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="33a5b-170">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="33a5b-171">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="33a5b-172">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="33a5b-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="33a5b-173">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="33a5b-174">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="33a5b-175">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="33a5b-176">Számlázás egy tényleges Időhöz: <strong>Számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="33a5b-177">Számlázás típusa egy tényleges kiadáshoz: <strong>Számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="33a5b-178">Számlázási típus a tényanyagon: <strong>Számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="33a5b-179">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="33a5b-180">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="33a5b-181">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="33a5b-182">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="33a5b-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="33a5b-183">
                    <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="33a5b-184">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="33a5b-185">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="33a5b-186">Számlázás egy tényleges Időhöz: <strong>Fel nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="33a5b-187">Számlázás típusa egy tényleges kiadáshoz: Számlázható</span><span class="sxs-lookup"><span data-stu-id="33a5b-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="33a5b-188">Számlázási típus a tényanyagon: Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="33a5b-189">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="33a5b-190">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="33a5b-191">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="33a5b-192">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="33a5b-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="33a5b-193">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="33a5b-194">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="33a5b-195">
                    <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="33a5b-196">Számlázás egy tényleges Időhöz: <strong>Fel nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="33a5b-197">Számlázás típusa egy tényleges költséghez: <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="33a5b-198">Számlázás típusa egy tényleges adathoz: <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="33a5b-199">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="33a5b-200">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="33a5b-201">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="33a5b-202">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="33a5b-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="33a5b-203">
                    <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="33a5b-204">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="33a5b-205">
                    <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="33a5b-206">Számlázás egy tényleges Időhöz: <strong>Fel nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="33a5b-207">Számlázás típusa egy tényleges költséghez: <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="33a5b-208">Számlázás típusa egy tényleges adathoz: <strong> Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="33a5b-209">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="33a5b-210">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="33a5b-211">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="33a5b-212">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="33a5b-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="33a5b-213">
                    <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="33a5b-214">
                    <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="33a5b-215">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="33a5b-216">Számlázás egy tényleges Időhöz: <strong>Fel nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="33a5b-217">Számlázás típusa egy tényleges költséghez: <strong> Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="33a5b-218">Számlázási típus a tényanyagon: Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="33a5b-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="33a5b-220">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="33a5b-221">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="33a5b-222">Teljes projekt</span><span class="sxs-lookup"><span data-stu-id="33a5b-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="33a5b-223">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="33a5b-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="33a5b-224">
                    <strong>Felszámítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="33a5b-225">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="33a5b-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="33a5b-226">Számlázás egy tényleges időhöz: <strong>Nem érhető el</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="33a5b-227">Számlázás típusa egy tényleges kiadáshoz: Számlázható</span><span class="sxs-lookup"><span data-stu-id="33a5b-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="33a5b-228">Számlázási típus a tényanyagon: Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="33a5b-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="33a5b-230">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="33a5b-231">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="33a5b-232">Teljes projekt</span><span class="sxs-lookup"><span data-stu-id="33a5b-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="33a5b-233">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="33a5b-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="33a5b-234">
                    <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="33a5b-235">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="33a5b-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="33a5b-236">Számlázás egy tényleges időhöz: <strong>Nem érhető el</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="33a5b-237">Számlázás típusa egy tényleges költséghez: <strong> Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="33a5b-238">Számlázási típus a tényanyagon: Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="33a5b-239">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="33a5b-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="33a5b-241">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="33a5b-242">Teljes projekt</span><span class="sxs-lookup"><span data-stu-id="33a5b-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="33a5b-243">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="33a5b-244">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="33a5b-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="33a5b-245">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="33a5b-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="33a5b-246">Számlázás egy tényleges Időhöz: Számlázható</span><span class="sxs-lookup"><span data-stu-id="33a5b-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="33a5b-247">Számlázás típusa egy tényleges költséghez: <strong>Nem érhető el</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="33a5b-248">Számlázási típus a tényanyagon: Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="33a5b-249">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="33a5b-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="33a5b-251">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="33a5b-252">Teljes projekt</span><span class="sxs-lookup"><span data-stu-id="33a5b-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="33a5b-253">
                    <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="33a5b-254">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="33a5b-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="33a5b-255">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="33a5b-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="33a5b-256">Számlázás egy tényleges Időhöz: <strong>Fel nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="33a5b-257">Számlázás típusa egy tényleges költséghez: <strong>Nem érhető el</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="33a5b-258">Számlázási típus a tényanyagon: Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="33a5b-259">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="33a5b-260">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="33a5b-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="33a5b-262">Teljes projekt</span><span class="sxs-lookup"><span data-stu-id="33a5b-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="33a5b-263">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="33a5b-264">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="33a5b-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="33a5b-265">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="33a5b-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="33a5b-266">Számlázás egy tényleges Időhöz: Számlázható</span><span class="sxs-lookup"><span data-stu-id="33a5b-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="33a5b-267">Számlázás típusa egy tényleges kiadáshoz: Számlázható</span><span class="sxs-lookup"><span data-stu-id="33a5b-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="33a5b-268">Számlázás típusa egy tényleges anyaghoz: <strong>Nem érhető el</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="33a5b-269">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="33a5b-270">Igen</span><span class="sxs-lookup"><span data-stu-id="33a5b-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="33a5b-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="33a5b-272">Teljes projekt</span><span class="sxs-lookup"><span data-stu-id="33a5b-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="33a5b-273">
                    <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="33a5b-274">
                    <strong>Nem számlázható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="33a5b-275">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="33a5b-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="33a5b-276">Számlázás egy tényleges Időhöz: <strong>Fel nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="33a5b-277">Számlázás típusa egy tényleges költséghez:<strong> Nem számítható </strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="33a5b-278">Számlázás típusa egy tényleges anyaghoz:<strong> Nem érhető el</strong>
                </span><span class="sxs-lookup"><span data-stu-id="33a5b-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
