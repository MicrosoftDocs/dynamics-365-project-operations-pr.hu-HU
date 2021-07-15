---
title: Projektalapú szerződéssorok áttekintése
description: Ez a témakör információkat nyújt a projektalapú szerződéssorok használatáról.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 22e8ff927c5ff6c3748a35031e7703e3fcfe0dab
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369919"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="d4c6e-103">Projektalapú szerződéssorok áttekintése</span><span class="sxs-lookup"><span data-stu-id="d4c6e-103">Project-based contract lines overview</span></span>

<span data-ttu-id="d4c6e-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="d4c6e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d4c6e-105">A Dynamics 365 Project Operations szerződéssorai úgy vannak kialakítva, hogy tárolják a becsléseket és számlázási megállapodásokat a projektmunka adott komponenseire egy aktivitásban.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="d4c6e-106">A projektalapú szerződéssorok felépítése a projektek becsült és számlázási helyzetére vonatkozóan a következő fogalmakkal bővül:</span><span class="sxs-lookup"><span data-stu-id="d4c6e-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="d4c6e-107">Számlázási mód</span><span class="sxs-lookup"><span data-stu-id="d4c6e-107">Billing method</span></span>
- <span data-ttu-id="d4c6e-108">Projekt és feladatleképezés</span><span class="sxs-lookup"><span data-stu-id="d4c6e-108">Project and task mapping</span></span>
- <span data-ttu-id="d4c6e-109">Szerepeltetett tranzakciós osztályok</span><span class="sxs-lookup"><span data-stu-id="d4c6e-109">Included transaction classes</span></span>
- <span data-ttu-id="d4c6e-110">Nem meghaladandó korlát</span><span class="sxs-lookup"><span data-stu-id="d4c6e-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="d4c6e-111">Felszámíthatósági beállítás</span><span class="sxs-lookup"><span data-stu-id="d4c6e-111">Chargeability setup</span></span>
- <span data-ttu-id="d4c6e-112">Becslések a szerződéssorok részleteinek használatával</span><span class="sxs-lookup"><span data-stu-id="d4c6e-112">Estimates using contract line details</span></span>
- <span data-ttu-id="d4c6e-113">Szerződéssor ügyfelei</span><span class="sxs-lookup"><span data-stu-id="d4c6e-113">Contract line customers</span></span>

<span data-ttu-id="d4c6e-114">A következő táblázat a projektalapú szerződéssorok **Általános** lapján található mezőket tartalmazza, amelyek segítenek részletes, mindenre kiterjedő becslési és számlázási megoldásokat beállítania projektalapú munkához.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="d4c6e-115">Mező</span><span class="sxs-lookup"><span data-stu-id="d4c6e-115">Field</span></span> | <span data-ttu-id="d4c6e-116">Adatfolyam leírása</span><span class="sxs-lookup"><span data-stu-id="d4c6e-116">Description</span></span> | <span data-ttu-id="d4c6e-117">Alsóbb rétegbeli hatás</span><span class="sxs-lookup"><span data-stu-id="d4c6e-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d4c6e-118">**Név**</span><span class="sxs-lookup"><span data-stu-id="d4c6e-118">**Name**</span></span> | <span data-ttu-id="d4c6e-119">A szerződéssor neve.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-119">Name of the contract line.</span></span> <span data-ttu-id="d4c6e-120">Ez azonosítja a becsült szerződés különálló összetevőjét.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="d4c6e-121">Az árajánlatból létrehozott projekt-szerződések esetén a program a projekt alapú árajánlati sor kapcsolódó értékéből másolja át az értéket.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="d4c6e-122">A számla létrehozásakor a név át lesz másolva a projekt számlasorra, amelye ebből a szerződéssorból lesz létrehozva.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="d4c6e-123">**Számlázási mód**</span><span class="sxs-lookup"><span data-stu-id="d4c6e-123">**Billing Method**</span></span> | <span data-ttu-id="d4c6e-124">Az árajánlatból létrehozott projekt-szerződésben a program a az ajánlatsor kapcsolódó mezőjéből másolja át az értéket.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="d4c6e-125">Ez egy értékkészlet, amely a Project Operations által támogatott két fő szerződőmodellt képviseli:</span><span class="sxs-lookup"><span data-stu-id="d4c6e-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="d4c6e-126">- **Rögzített ár**</span><span class="sxs-lookup"><span data-stu-id="d4c6e-126">- **Fixed Price**</span></span></br><span data-ttu-id="d4c6e-127">- **Idő és anyag**</span><span class="sxs-lookup"><span data-stu-id="d4c6e-127">- **Time and Material**</span></span> | <span data-ttu-id="d4c6e-128">A hivatkozott szerződéssor számlázási módja alapján a rendszer feldolgozza a tényleges tranzakciót.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="d4c6e-129">Ha a tényadat által hivatkozottszerződéssor idő-és anyagelszámolású számlázási módot tartalmaz, akkor a rendszer létrehozza a költség és a nem számlázott tényleges értékesítések bejegyzéseit.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="d4c6e-130">Ha a tényadat által hivatkozott szerződéssor rögzített árú számlázási móddal rendelkezik, akkor csak egy tényleges költség jön létre.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="d4c6e-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="d4c6e-131">**Project**</span></span> | <span data-ttu-id="d4c6e-132">Ezzel a mezővel azonosíthatja azt a projektet, amelyet az adott aktivitással kapcsolatos munkára fog használni.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="d4c6e-133">Ezt az értéket a **Hozzáadott feladatok** és a **Hozzáadott tranzakcióosztályok** együtt fogja használni a szerződéssor-hivatkozás feloldásához egy tényleges vagy becslési sorrekordon.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="d4c6e-134">**Hozzáadott feladatok**</span><span class="sxs-lookup"><span data-stu-id="d4c6e-134">**Included Tasks**</span></span> | <span data-ttu-id="d4c6e-135">Azt jelzi, hogy a szerződéssor tartalmazza-e a kijelölt projekt összes projekt-feladatát, vagy csak a feladatok egy részét.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="d4c6e-136">Ez egy értékkészlet, amelynek a következő lehetséges értékei vannak:</span><span class="sxs-lookup"><span data-stu-id="d4c6e-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="d4c6e-137">- **Összes projektfeladat**</span><span class="sxs-lookup"><span data-stu-id="d4c6e-137">- **All Project Tasks**</span></span></br><span data-ttu-id="d4c6e-138">- **Csak a kiválasztott projektfeladatok**.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="d4c6e-139">Az ebben a mezőben szereplő üres érték az **Összes projektfeladat** kijelölésével egyenlő.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="d4c6e-140">Ha a **Csak a kiválasztott feladatok** lehetőség van kiválasztva, akkor kijelölhet bizonyos feladatokat, és hozzárendelheti őket ehhez a szerződés sorhoz a **Projekt** lap **Feladat számlázási beállítása** lapján.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="d4c6e-141">Ezt az értéket a program a **Projekt** és **Hozzáadott tranzakciók** osztályokkal együtt használja, hogy feloldja a szerződéssor hivatkozását egy tényadaton vagy egy becsléssor-rekordon.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="d4c6e-142">**Idővel együtt**</span><span class="sxs-lookup"><span data-stu-id="d4c6e-142">**Include Time**</span></span> | <span data-ttu-id="d4c6e-143">Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt időtranzakciói vagy munkaköltségei szerepelnek-e a szerződéssoron.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="d4c6e-144">A **Nem** érték azt jelzi, hogy a kiválasztott projekthez tartozó időtranzakciók vagy munkaköltségek nem fognak szerepelni ebben a szerződéssorban.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="d4c6e-145">Az **Igen** érték azt jelzi, hogy fognak.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="d4c6e-146">Ez az érték a projekttel együtt egy tényleges vagy becslési sorrekord szerződéssor-hivatkozásának feloldására szolgál.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="d4c6e-147">**Költséggel együtt**</span><span class="sxs-lookup"><span data-stu-id="d4c6e-147">**Include Expense**</span></span> | <span data-ttu-id="d4c6e-148">Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt önköltségei szerepelnek-e a szerződéssorban.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="d4c6e-149">A **Nem** érték azt jelzi, hogy a kiválasztott projekthez tartozó önköltség nem fog szerepelni ebben a szerződéssorban.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="d4c6e-150">Az **Igen** érték azt jelzi, hogy fog.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="d4c6e-151">Ez az érték a projekttel együtt egy tényleges vagy becslési sorrekord szerződéssor-hivatkozásának feloldására szolgál.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="d4c6e-152">**Anyagokkal együtt**</span><span class="sxs-lookup"><span data-stu-id="d4c6e-152">**Include Materials**</span></span> | <span data-ttu-id="d4c6e-153">Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt anyagköltségei szerepelnek-e a szerződéssorban.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="d4c6e-154">A **Nem** érték azt jelzi, hogy az anyagköltségek nem szerepelnek a szerződéssorban.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="d4c6e-155">Az **Igen** érték azt jelzi, hogy fog.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="d4c6e-156">Ez az érték a projekttel együtt egy tényleges vagy becslési sorrekord szerződéssor-hivatkozásának feloldására szolgál.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="d4c6e-157">**Díjjal együtt**</span><span class="sxs-lookup"><span data-stu-id="d4c6e-157">**Include Fee**</span></span> | <span data-ttu-id="d4c6e-158">Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt díjai szerepelnek-e a szerződéssorban.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="d4c6e-159">A **Nem** érték azt jelzi, hogy a kiválasztott projekthez tartozó díjak nem fognak szerepelni ebben a szerződéssorban.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="d4c6e-160">Az **Igen** érték azt jelzi, hogy fognak.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="d4c6e-161">Ez az érték a projekttel együtt egy tényleges vagy becslési sorrekord szerződéssor-hivatkozásának feloldására szolgál.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="d4c6e-162">**Szerződésben rögzített összeg**</span><span class="sxs-lookup"><span data-stu-id="d4c6e-162">**Contracted Amount**</span></span> | <span data-ttu-id="d4c6e-163">Rögzített árú szerződéssor esetén ez az összeg egy megállapodott érték, ami számlázva lesz az ügyfélnek a szerződéssorhoz társított összes munkaösszetevőhöz.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="d4c6e-164">Idő és anyag szerződéssor esetén ez az összeg becsült érték arra vonatkozóan, ami számlázva lesz az ügyfélnek a szerződéssorhoz társított összes munkaösszetevőhöz.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="d4c6e-165">Árajánlatból létrehozott projekt-szerződésben a program a az ajánlatsor kapcsolódó mezőjéből másolja át az értéket.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="d4c6e-166">Ha egy projektalapú szerződéssor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és a program a szerződéssor részleteiben szereplő összegből összegzi.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="d4c6e-167">Ha a szerződéssorhoz tartoznak sorrészletek, akkor ez az érték módosítható a sor részleteiben szereplő összegek módosításával.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="d4c6e-168">Rögzített árú szerződéssor esetén ez az érték a periodikus számlázási mérföldkövek után fizetendő összeg generálására szolgál.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="d4c6e-169">**Becsült adó**</span><span class="sxs-lookup"><span data-stu-id="d4c6e-169">**Estimated Tax**</span></span> | <span data-ttu-id="d4c6e-170">A felhasználó módosíthatja ezt a mezőt, hogy a szerződéssor összegére vonatkozóan megadja a becsült adót.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="d4c6e-171">Ha egy projektalapú szerződéssor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és a program a szerződéssor részleteiben szereplő adóösszegből összegzi.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="d4c6e-172">Ha a szerződéssorhoz tartoznak sorrészletek, akkor ez az érték módosítható a sor részleteiben szereplő adóösszegek módosításával.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="d4c6e-173">Rögzített árú szerződéssor esetén ez az érték a periodikus számlázási mérföldkövekhez kapcsolódó adózás előtti összeg generálására szolgál.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="d4c6e-174">**Szerződésben rögzített összeg adózás után**</span><span class="sxs-lookup"><span data-stu-id="d4c6e-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="d4c6e-175">A szerződéssor összege adózás után.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-175">The contract line amount after tax.</span></span> <span data-ttu-id="d4c6e-176">Ez a mező csak olvasható, és számítása a következő: **Szerződött összeg + adó**.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="d4c6e-177">Rögzített árú szerződéssor esetén ez az érték a periodikus számlázási mérföldkövekhez kapcsolódó adó generálására szolgál.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="d4c6e-178">**Nem meghaladandó korlát**</span><span class="sxs-lookup"><span data-stu-id="d4c6e-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="d4c6e-179">A felhasználó szerkesztheti ezt a mezőt, és csak olyan projektalapú szerződéssorok esetén érhető el, amelyek számlázási módja idő és anyag értékre van beállítva.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="d4c6e-180">A felhasználó szerkesztheti ezt a mezőt.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-180">The user can edit this field.</span></span> <span data-ttu-id="d4c6e-181">Ha egy időhöz vagy anyaghoz tartozó tényadat erre a szerződéssorra hivatkozik, akkor tényadathoz tartozó összeg össze lesz vetve a szerződéssor nem túlléphető határértékével.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="d4c6e-182">Ez az értékelés a már elköltött és lekötött összegek figyelembe vételét követően fejeződik be.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="d4c6e-183">**Ügyfél költségvetése**</span><span class="sxs-lookup"><span data-stu-id="d4c6e-183">**Customer Budget**</span></span> | <span data-ttu-id="d4c6e-184">Ez a mező szerkeszthető, és árajánlatból létrehozott projekt-szerződésben a program a az ajánlatsor kapcsolódó mezőjéből másolja át az értéket.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="d4c6e-185">Ez a mező csak tájékoztatásra szolgál, és nincs későbbi jelentősége.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="d4c6e-186">A Projektalapú szerződéssorok Általános lapjának beállításaira vonatkozó ellenőrzési szabályok</span><span class="sxs-lookup"><span data-stu-id="d4c6e-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="d4c6e-187">1. szabály: Ha a **Hozzáadott feladatok** mező üres, vagy **Minden projekttevékenység** értékre van állítva , a projekt minden feladata szerepel a szerződéssoron.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="d4c6e-188">2. szabály: Ha a **Hozzáadott feladatok** mező üres, vagy kifejezetten **Minden projektfeladat** értékre van beállítva, egy projekt vagy egy adott tranzakciós osztály egy szerződésnek csak egy projektalapú szerződéssorán szerepelhet.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="d4c6e-189">3. szabály: Ha a **Hozzáadott feladatok** mező **Csak kiválasztott projektfeladatok** értékre van beállítva, egy projekt vagy egy adott tranzakciós osztály egy szerződésnek több projektalapú szerződéssorán szerepelhet.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="d4c6e-190">
                    <strong>Szerződés</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4c6e-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d4c6e-191">
                    <strong>Szerződéssor</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4c6e-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d4c6e-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4c6e-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="d4c6e-193">
                    <strong>Hozzáadott feladatok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4c6e-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d4c6e-194">
                    <strong>Idővel együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4c6e-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d4c6e-195">
                    <strong>Költséggel együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4c6e-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d4c6e-196">
                    <strong>Anyagokkal együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4c6e-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d4c6e-197">
                    <strong>Tartalmazás</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4c6e-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="d4c6e-198">
                    <strong>Díj</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4c6e-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="d4c6e-199">
                    <strong>Érvényes/nem érvényes</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4c6e-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="d4c6e-200">
                    <strong>Ok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4c6e-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d4c6e-201">C1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4c6e-202">CL1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-203">I1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4c6e-204">Üres</span><span class="sxs-lookup"><span data-stu-id="d4c6e-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-205">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-206">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-207">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-208">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4c6e-209">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="d4c6e-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4c6e-210">Az 2. szabály megsértése.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-210">Violation of Rule #2.</span></span> <span data-ttu-id="d4c6e-211">A P1 projektre vonatkozó időt, költséget, anyagokat és díjat az ÁS1 és ÁS2 szerződéssora is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d4c6e-212">C1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4c6e-213">CL2</span><span class="sxs-lookup"><span data-stu-id="d4c6e-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-214">I1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4c6e-215">Üres</span><span class="sxs-lookup"><span data-stu-id="d4c6e-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-216">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-217">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-218">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-219">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d4c6e-220">C1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4c6e-221">CL1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-222">I1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4c6e-223">Üres</span><span class="sxs-lookup"><span data-stu-id="d4c6e-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-224">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-225">No</span><span class="sxs-lookup"><span data-stu-id="d4c6e-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-226">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-227">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4c6e-228">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="d4c6e-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4c6e-229">Az 2. szabály megsértése.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-229">Violation of Rule #2.</span></span> <span data-ttu-id="d4c6e-230">A P1 projektre vonatkozó időt, anyagokat és díjat az ÁS1 és ÁS2 szerződéssora is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d4c6e-231">C1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4c6e-232">CL2</span><span class="sxs-lookup"><span data-stu-id="d4c6e-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-233">I1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4c6e-234">Üres</span><span class="sxs-lookup"><span data-stu-id="d4c6e-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-235">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-236">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-237">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-238">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d4c6e-239">C1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4c6e-240">CL1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-241">I1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4c6e-242">Üres</span><span class="sxs-lookup"><span data-stu-id="d4c6e-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-243">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-244">No</span><span class="sxs-lookup"><span data-stu-id="d4c6e-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-245">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-246">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4c6e-247">Érvényes</span><span class="sxs-lookup"><span data-stu-id="d4c6e-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4c6e-248">A P1 projektre vonatkozó időt, anyagokat és díjat az ÁS1 árajánlatsor tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="d4c6e-249">A P1 projektre vonatkozó költséget a CS2 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="d4c6e-250">Nincs átfedés abban, hogy miket tartalmaznak az egyes szerződéssorok, így ez érvényes.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d4c6e-251">C1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4c6e-252">CL2</span><span class="sxs-lookup"><span data-stu-id="d4c6e-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-253">I1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4c6e-254">Üres</span><span class="sxs-lookup"><span data-stu-id="d4c6e-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-255">No</span><span class="sxs-lookup"><span data-stu-id="d4c6e-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-256">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-257">No</span><span class="sxs-lookup"><span data-stu-id="d4c6e-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-258">No</span><span class="sxs-lookup"><span data-stu-id="d4c6e-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d4c6e-259">C1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4c6e-260">CL1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-261">I1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4c6e-262">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="d4c6e-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-263">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-264">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-265">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-266">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4c6e-267">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="d4c6e-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4c6e-268">A 2. szabály megsértése</span><span class="sxs-lookup"><span data-stu-id="d4c6e-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="d4c6e-269">A C1 tartalmazza a P1 projekttel kapcsolatos feladatok egy részhalmazának idejét, anyagait, költségeit és díjait.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d4c6e-270">A CL2 tartalmazza az egész P1 projektre vonatkozó időt, anyagokat, költségeket és díjakat, ezért átfedésben van a C1 sorral.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d4c6e-271">C1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4c6e-272">CL2</span><span class="sxs-lookup"><span data-stu-id="d4c6e-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-273">I1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4c6e-274">Üres</span><span class="sxs-lookup"><span data-stu-id="d4c6e-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-275">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-276">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-277">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-278">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d4c6e-279">C1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4c6e-280">CL1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-281">I1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4c6e-282">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="d4c6e-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-283">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-284">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-285">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-286">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4c6e-287">Érvényes</span><span class="sxs-lookup"><span data-stu-id="d4c6e-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4c6e-288">A 3. szabály szerint</span><span class="sxs-lookup"><span data-stu-id="d4c6e-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="d4c6e-289">A C1 tartalmazza a P1 projekttel kapcsolatos feladatok egy részhalmazának idejét, költségeit, anyagait és díjait.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d4c6e-290">A CL2 tartalmazza a P1 projekttel kapcsolatos feladatok egy részhalmazának idejét, anyagait, költségeit és díjait.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d4c6e-291">Az egyetlen további ellenőrzés a CL1-es feladatok részhalmaza körül van, amely eltér a CL2-es feladatok részhalmazától, így biztosítva, hogy ne legyen semmilyen átfedés.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="d4c6e-292">Ezt a rendszer hajtja végre a feladatok társításakor.</span><span class="sxs-lookup"><span data-stu-id="d4c6e-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d4c6e-293">C1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4c6e-294">CL2</span><span class="sxs-lookup"><span data-stu-id="d4c6e-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-295">I1</span><span class="sxs-lookup"><span data-stu-id="d4c6e-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4c6e-296">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="d4c6e-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-297">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4c6e-298">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-299">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4c6e-300">Igen</span><span class="sxs-lookup"><span data-stu-id="d4c6e-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
