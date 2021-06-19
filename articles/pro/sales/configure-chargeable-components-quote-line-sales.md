---
title: Az árajánlatsor számlázható összetevőinek konfigurálása
description: Ez a témakör a számlázható és nem számlázható összetevők beállításával kapcsolatban tartalmaz tájékoztatást a projekt alapú árajánlatok soraiban.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003769"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="4c311-103">Az árajánlatsor felszámítható összetevőinek konfigurálása</span><span class="sxs-lookup"><span data-stu-id="4c311-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="4c311-104">_**A következőre vonatkozik:** Egyszerű központi telepítés – proforma számlázás, Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="4c311-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4c311-105">A projektalapú ajánlati sor rendelkezhet *mellékelt* összetevőkkel és a *felszámítható* összetevőkkel.</span><span class="sxs-lookup"><span data-stu-id="4c311-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="4c311-106">A mellékelt összetevők a következőkre vonatkoznak:</span><span class="sxs-lookup"><span data-stu-id="4c311-106">Included components are subject to:</span></span>

  - <span data-ttu-id="4c311-107">Számlázási mód és ügyfél felosztások</span><span class="sxs-lookup"><span data-stu-id="4c311-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="4c311-108">Nem meghaladandó korlátok</span><span class="sxs-lookup"><span data-stu-id="4c311-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="4c311-109">A projekt alapú ajánlatsor által meghatározott számlázási gyakorisági beállításai</span><span class="sxs-lookup"><span data-stu-id="4c311-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="4c311-110">A befoglalt összetevők egy részhalmaza a **Számlázási típus** mező segítségével állítható terhelhetőre.</span><span class="sxs-lookup"><span data-stu-id="4c311-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="4c311-111">A **Számlázási típus** mező olyan értékkészlet, amely az ajánlatsorok környezetében az alábbi értékeket teszi lehetővé:</span><span class="sxs-lookup"><span data-stu-id="4c311-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="4c311-112">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-112">Chargeable</span></span>
  - <span data-ttu-id="4c311-113">Fel nem számítható</span><span class="sxs-lookup"><span data-stu-id="4c311-113">Non-chargeable</span></span>

<span data-ttu-id="4c311-114">A felszámítható összetevők a feladatokon, szerepkörökön és tranzakciós kategóriákon határozhatók meg.</span><span class="sxs-lookup"><span data-stu-id="4c311-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="4c311-115">A felszámíthatóság az ajánlatsor feladataihoz van definiálva, és a sorban szereplő összes tranzakciós osztályra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="4c311-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="4c311-116">Ha a szerződéssor **Feladatok belefoglalása** mezője üres, vagy a **Teljes projekt** értékre van állítva, a **Felszámítható feladatok** lap nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="4c311-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="4c311-117">Az ajánlatsor szerepkörei meghatározott felszámíthatóság csak az **Idő** tranzakciós osztályra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="4c311-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="4c311-118">Ha az **Idő belefoglalása** mező **Nem** értékre van állítva, a **Felszámítható szerepkörök** lap nem lesz elérhető.</span><span class="sxs-lookup"><span data-stu-id="4c311-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="4c311-119">Az ajánlati sor tranzakciós kategóriái meghatározott felszámíthatóság csak az **Költség** tranzakciós osztályra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="4c311-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="4c311-120">Ha a **Költségek belefoglalása** mező **Nem** értékre van állítva, a **Számlázható kategóriák** lap nem lesz elérhető.</span><span class="sxs-lookup"><span data-stu-id="4c311-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="4c311-121">Projekttevékenység frissítése felszámítható vagy nem felszámítható értékre</span><span class="sxs-lookup"><span data-stu-id="4c311-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="4c311-122">A projekttevékenység egy projektalapú ajánlatsor kontextusában felszámítható vagy nem felszámítható lehet, így a következő beállításokat lehet használni.</span><span class="sxs-lookup"><span data-stu-id="4c311-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="4c311-123">Ha egy projekten alapuló ajánlati sor **Időt** és a **T1** feladatot tartalmazza, akkor a feladat számlázhatóként lesz az ajánlati sorhoz rendelve.</span><span class="sxs-lookup"><span data-stu-id="4c311-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="4c311-124">Ha van egy második ajánlatsor , amely **Költségeket** tartalmaz , akkor a **T1** feladatot a szerződéssorok között nem felszámíthatóként társíthatja.</span><span class="sxs-lookup"><span data-stu-id="4c311-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="4c311-125">Az eredmény az, hogy a feladathoz rögzített összes idő felszámítható, és a feladathoz rendelt minden költség nem felszámítható.</span><span class="sxs-lookup"><span data-stu-id="4c311-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="4c311-126">A feladatok számlázási típusa a projektalapú ajánlatsor **Számlázható feladatok** lapján állítható be az **Ajánlatisor-feladatok** alrács **Számlázási típus** mezőjének frissítésével.</span><span class="sxs-lookup"><span data-stu-id="4c311-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="4c311-127">Másik lehetőségként frissítheti a projekttevékenységek számlázási típusát a **Számlázási típus** mezőben, a projekt számlázási beállítása alrácsán, amely a feladathoz társított ajánlati sorokat mutatja.</span><span class="sxs-lookup"><span data-stu-id="4c311-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="4c311-128">Szerepkör frissítése felszámítható vagy nem felszámítható értékre</span><span class="sxs-lookup"><span data-stu-id="4c311-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="4c311-129">A szerepkör egy adott, projekten alapuló ajánlati sor környezetében számlázható vagy nem számlázható lehet.</span><span class="sxs-lookup"><span data-stu-id="4c311-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="4c311-130">A szerepkör számlázási típusa a projektalapú ajánlatsor **Számlázható szerepkörök** lapján állítható be az **Számlázható szerepkörök** alrács **Számlázási típus** mezőjének frissítésével.</span><span class="sxs-lookup"><span data-stu-id="4c311-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="4c311-131">Tranzakciókategória frissítése felszámítható vagy nem felszámítható értékre</span><span class="sxs-lookup"><span data-stu-id="4c311-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="4c311-132">Egy tranzakciós kategória egy adott ajánlatsoron felszámítható vagy nem felszámítható lehet.</span><span class="sxs-lookup"><span data-stu-id="4c311-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="4c311-133">A tranzakció számlázási típusa a projektalapú ajánlatsor **Számlázható kategóriák** lapján állítható be az **Számlázható szerepkörök** alrács **Számlázási kategóriák** mezőjének frissítésével.</span><span class="sxs-lookup"><span data-stu-id="4c311-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="4c311-134">A számlázhatóság feloldása</span><span class="sxs-lookup"><span data-stu-id="4c311-134">Resolve chargeability</span></span>
<span data-ttu-id="4c311-135">Az időre létrehozott becslés vagy tényadat csak akkor tekinthető felszámíthatónak, ha:</span><span class="sxs-lookup"><span data-stu-id="4c311-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="4c311-136">Az **Idő** szerepel az árajánlatsorban.</span><span class="sxs-lookup"><span data-stu-id="4c311-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="4c311-137">A **Szerepkör** az árajánlatsorban felszámíthatóként van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="4c311-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="4c311-138">A **Hozzáadott feladatok** érték **Kijelölt feladatok** elemre van állítva az árajánlatsoron.</span><span class="sxs-lookup"><span data-stu-id="4c311-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="4c311-139">Ha ez a három dolog teljesül, akkor a **Feladat** felszámíthatóként konfigurálható.</span><span class="sxs-lookup"><span data-stu-id="4c311-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="4c311-140">A költségre létrehozott becslés vagy tényadat csak akkor tekinthető felszámíthatónak, ha:</span><span class="sxs-lookup"><span data-stu-id="4c311-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="4c311-141">A **Költség** szerepel az árajánlatsorban.</span><span class="sxs-lookup"><span data-stu-id="4c311-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="4c311-142">A **Tranzakciókategória** az árajánlatsorban felszámíthatóként van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="4c311-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="4c311-143">A **Hozzáadott feladatok** érték **Kijelölt feladatok** elemre van állítva az árajánlatsoron.</span><span class="sxs-lookup"><span data-stu-id="4c311-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="4c311-144">Ha ez a három dolog teljesül, akkor a **Feladat** felszámíthatóként konfigurálható.</span><span class="sxs-lookup"><span data-stu-id="4c311-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="4c311-145">Az anyagra létrehozott becslés vagy tényadat csak akkor tekinthető felszámíthatónak, ha:</span><span class="sxs-lookup"><span data-stu-id="4c311-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="4c311-146">Az **Anyag** szerepel az árajánlatsorban.</span><span class="sxs-lookup"><span data-stu-id="4c311-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="4c311-147">A **Hozzáadott feladatok** érték **Kijelölt feladatok** elemre van állítva az árajánlatsoron.</span><span class="sxs-lookup"><span data-stu-id="4c311-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="4c311-148">Ha ez a két dolog teljesül, akkor a **Feladatot** felszámíthatóként kell konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="4c311-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="4c311-149">
                    <strong>Időt tartalmaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="4c311-150">
                    <strong>Költséget tartalmaz</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="4c311-151">
                    <strong>Anyagokkal együtt</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="4c311-152">
                    <strong>Hozzáadott feladatok</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4c311-153">
                    <strong>Szerepkör</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="4c311-154">
                    <strong>Kategória</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4c311-155">
                    <strong>Feladatok</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="4c311-156">
                    <strong>Felszámolhatósági hatás</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4c311-157">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4c311-158">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4c311-159">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4c311-160">Teljes projekt</span><span class="sxs-lookup"><span data-stu-id="4c311-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4c311-161">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4c311-162">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4c311-163">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="4c311-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4c311-164">Számlázás egy tényleges Időhöz: Számlázható</span><span class="sxs-lookup"><span data-stu-id="4c311-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4c311-165">Számlázás típusa egy tényleges kiadáshoz: Számlázható</span><span class="sxs-lookup"><span data-stu-id="4c311-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4c311-166">Számlázási típus a tényanyagon: Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4c311-167">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4c311-168">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4c311-169">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4c311-170">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="4c311-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4c311-171">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4c311-172">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4c311-173">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4c311-174">Számlázás egy tényleges Időhöz: Számlázható</span><span class="sxs-lookup"><span data-stu-id="4c311-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4c311-175">Számlázás típusa egy tényleges kiadáshoz: Számlázható</span><span class="sxs-lookup"><span data-stu-id="4c311-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4c311-176">Számlázási típus a tényanyagon: Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4c311-177">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4c311-178">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4c311-179">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4c311-180">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="4c311-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4c311-181">
                    <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4c311-182">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4c311-183">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4c311-184">Számlázás egy tényleges Időhöz: <strong>Fel nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4c311-185">Számlázás típusa egy tényleges kiadáshoz: Számlázható</span><span class="sxs-lookup"><span data-stu-id="4c311-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4c311-186">Számlázási típus a tényanyagon: Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4c311-187">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4c311-188">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4c311-189">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4c311-190">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="4c311-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4c311-191">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4c311-192">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4c311-193">
                    <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4c311-194">Számlázás egy tényleges Időhöz: <strong>Fel nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4c311-195">Számlázás típusa egy tényleges költséghez: <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4c311-196">Számlázás típusa egy tényleges adathoz: <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4c311-197">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4c311-198">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4c311-199">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4c311-200">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="4c311-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4c311-201">
                    <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4c311-202">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4c311-203">
                    <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4c311-204">Számlázás egy tényleges Időhöz: <strong>Fel nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4c311-205">Számlázás típusa egy tényleges költséghez: <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4c311-206">Számlázás típusa egy tényleges adathoz: <strong> Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4c311-207">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4c311-208">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4c311-209">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4c311-210">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="4c311-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4c311-211">
                    <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="4c311-212">
                    <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4c311-213">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4c311-214">Számlázás egy tényleges Időhöz: <strong>Fel nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4c311-215">Számlázás típusa egy tényleges költséghez: <strong> Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4c311-216">Számlázási típus a tényanyagon: Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="4c311-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4c311-218">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4c311-219">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4c311-220">Teljes projekt</span><span class="sxs-lookup"><span data-stu-id="4c311-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4c311-221">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="4c311-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="4c311-222">
                    <strong>Felszámítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4c311-223">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="4c311-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4c311-224">Számlázás egy tényleges időhöz: <strong>Nem érhető el</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4c311-225">Számlázás típusa egy tényleges kiadáshoz: Számlázható</span><span class="sxs-lookup"><span data-stu-id="4c311-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4c311-226">Számlázási típus a tényanyagon: Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="4c311-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4c311-228">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4c311-229">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4c311-230">Teljes projekt</span><span class="sxs-lookup"><span data-stu-id="4c311-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4c311-231">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="4c311-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="4c311-232">
                    <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4c311-233">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="4c311-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4c311-234">Számlázás egy tényleges időhöz: <strong>Nem érhető el</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4c311-235">Számlázás típusa egy tényleges költséghez: <strong> Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4c311-236">Számlázási típus a tényanyagon: Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4c311-237">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="4c311-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4c311-239">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4c311-240">Teljes projekt</span><span class="sxs-lookup"><span data-stu-id="4c311-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4c311-241">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4c311-242">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="4c311-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4c311-243">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="4c311-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4c311-244">Számlázás egy tényleges Időhöz: Számlázható</span><span class="sxs-lookup"><span data-stu-id="4c311-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4c311-245">Számlázás típusa egy tényleges költséghez: <strong>Nem érhető el</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4c311-246">Számlázási típus a tényanyagon: Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4c311-247">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="4c311-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4c311-249">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4c311-250">Teljes projekt</span><span class="sxs-lookup"><span data-stu-id="4c311-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4c311-251">
                    <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4c311-252">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="4c311-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4c311-253">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="4c311-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4c311-254">Számlázás egy tényleges Időhöz: <strong>Fel nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="4c311-255">Számlázás típusa egy tényleges költséghez: <strong>Nem érhető el</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4c311-256">Számlázási típus a tényanyagon: Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4c311-257">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4c311-258">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="4c311-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4c311-260">Teljes projekt</span><span class="sxs-lookup"><span data-stu-id="4c311-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4c311-261">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4c311-262">Felszámítható</span><span class="sxs-lookup"><span data-stu-id="4c311-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4c311-263">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="4c311-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4c311-264">Számlázás egy tényleges Időhöz: Számlázható</span><span class="sxs-lookup"><span data-stu-id="4c311-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4c311-265">Számlázás típusa egy tényleges kiadáshoz: Számlázható</span><span class="sxs-lookup"><span data-stu-id="4c311-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4c311-266">Számlázás típusa egy tényleges anyaghoz: <strong>Nem érhető el</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4c311-267">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4c311-268">Igen</span><span class="sxs-lookup"><span data-stu-id="4c311-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="4c311-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4c311-270">Teljes projekt</span><span class="sxs-lookup"><span data-stu-id="4c311-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4c311-271">
                    <strong>Nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="4c311-272">
                    <strong>Nem számlázható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4c311-273">Nem állítható be</span><span class="sxs-lookup"><span data-stu-id="4c311-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4c311-274">Számlázás egy tényleges Időhöz: <strong>Fel nem számítható</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="4c311-275">Számlázás típusa egy tényleges költséghez:<strong> Nem számítható </strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="4c311-276">Számlázás típusa egy tényleges anyaghoz:<strong> Nem érhető el</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c311-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
