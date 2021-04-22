---
title: Projektalapú szerződéssorok áttekintése
description: Ez a témakör információkat nyújt a projektalapú szerződéssorok használatáról.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858161"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="d4ed4-103">Projektalapú szerződéssorok áttekintése</span><span class="sxs-lookup"><span data-stu-id="d4ed4-103">Project-based contract lines overview</span></span>

<span data-ttu-id="d4ed4-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="d4ed4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d4ed4-105">A Dynamics 365 Project Operations szerződéssorai úgy vannak kialakítva, hogy tárolják a becsléseket és számlázási megállapodásokat a projektmunka adott komponenseire egy aktivitásban.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="d4ed4-106">A projektalapú szerződéssorok felépítése a projektek becsült és számlázási helyzetére vonatkozóan a következő fogalmakkal bővül:</span><span class="sxs-lookup"><span data-stu-id="d4ed4-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="d4ed4-107">Számlázási mód</span><span class="sxs-lookup"><span data-stu-id="d4ed4-107">Billing method</span></span>
- <span data-ttu-id="d4ed4-108">Projekt és feladatleképezés</span><span class="sxs-lookup"><span data-stu-id="d4ed4-108">Project and task mapping</span></span>
- <span data-ttu-id="d4ed4-109">Szerepeltetett tranzakciós osztályok</span><span class="sxs-lookup"><span data-stu-id="d4ed4-109">Included transaction classes</span></span>
- <span data-ttu-id="d4ed4-110">Nem meghaladandó korlát</span><span class="sxs-lookup"><span data-stu-id="d4ed4-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="d4ed4-111">Felszámíthatósági beállítás</span><span class="sxs-lookup"><span data-stu-id="d4ed4-111">Chargeability setup</span></span>
- <span data-ttu-id="d4ed4-112">Becslések a szerződéssorok részleteinek használatával</span><span class="sxs-lookup"><span data-stu-id="d4ed4-112">Estimates using contract line details</span></span>
- <span data-ttu-id="d4ed4-113">Szerződéssor ügyfelei</span><span class="sxs-lookup"><span data-stu-id="d4ed4-113">Contract line customers</span></span>

<span data-ttu-id="d4ed4-114">A következő táblázat a projektalapú szerződéssorok **Általános** lapján található mezőket tartalmazza, amelyek segítenek részletes, mindenre kiterjedő becslési és számlázási megoldásokat beállítania projektalapú munkához.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="d4ed4-115">Mező</span><span class="sxs-lookup"><span data-stu-id="d4ed4-115">Field</span></span> | <span data-ttu-id="d4ed4-116">Adatfolyam leírása</span><span class="sxs-lookup"><span data-stu-id="d4ed4-116">Description</span></span> | <span data-ttu-id="d4ed4-117">Alsóbb rétegbeli hatás</span><span class="sxs-lookup"><span data-stu-id="d4ed4-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d4ed4-118">**Név**</span><span class="sxs-lookup"><span data-stu-id="d4ed4-118">**Name**</span></span> | <span data-ttu-id="d4ed4-119">A szerződéssor neve.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-119">Name of the contract line.</span></span> <span data-ttu-id="d4ed4-120">Ez azonosítja a becsült szerződés különálló összetevőjét.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="d4ed4-121">Az árajánlatból létrehozott projekt-szerződések esetén a program a projekt alapú árajánlati sor kapcsolódó értékéből másolja át az értéket.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="d4ed4-122">A számla létrehozásakor a név át lesz másolva a projekt számlasorra, amelye ebből a szerződéssorból lesz létrehozva.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="d4ed4-123">**Számlázási mód**</span><span class="sxs-lookup"><span data-stu-id="d4ed4-123">**Billing Method**</span></span> | <span data-ttu-id="d4ed4-124">Az árajánlatból létrehozott projekt-szerződésben a program a az ajánlatsor kapcsolódó mezőjéből másolja át az értéket.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="d4ed4-125">Ez egy értékkészlet, amely a Project Operations által támogatott két fő szerződőmodellt képviseli:</span><span class="sxs-lookup"><span data-stu-id="d4ed4-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="d4ed4-126">- **Rögzített ár**</span><span class="sxs-lookup"><span data-stu-id="d4ed4-126">- **Fixed Price**</span></span></br><span data-ttu-id="d4ed4-127">- **Idő és anyag**</span><span class="sxs-lookup"><span data-stu-id="d4ed4-127">- **Time and Material**</span></span> | <span data-ttu-id="d4ed4-128">A hivatkozott szerződéssor számlázási módja alapján a rendszer feldolgozza a tényleges tranzakciót.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="d4ed4-129">Ha a tényadat által hivatkozottszerződéssor idő-és anyagelszámolású számlázási módot tartalmaz, akkor a rendszer létrehozza a költség és a nem számlázott tényleges értékesítések bejegyzéseit.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="d4ed4-130">Ha a tényadat által hivatkozott szerződéssor rögzített árú számlázási móddal rendelkezik, akkor csak egy tényleges költség jön létre.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="d4ed4-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="d4ed4-131">**Project**</span></span> | <span data-ttu-id="d4ed4-132">Ezzel a mezővel azonosíthatja azt a projektet, amelyet az adott aktivitással kapcsolatos munkára fog használni.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="d4ed4-133">Ezt az értéket a **Hozzáadott feladatok** és a **Hozzáadott tranzakcióosztályok** együtt fogja használni a szerződéssor-hivatkozás feloldásához egy tényleges vagy becslési sorrekordon.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="d4ed4-134">**Hozzáadott feladatok**</span><span class="sxs-lookup"><span data-stu-id="d4ed4-134">**Included Tasks**</span></span> | <span data-ttu-id="d4ed4-135">Azt jelzi, hogy a szerződéssor tartalmazza-e a kijelölt projekt összes projekt-feladatát, vagy csak a feladatok egy részét.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="d4ed4-136">Ez egy értékkészlet, amelynek a következő lehetséges értékei vannak:</span><span class="sxs-lookup"><span data-stu-id="d4ed4-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="d4ed4-137">- **Összes projektfeladat**</span><span class="sxs-lookup"><span data-stu-id="d4ed4-137">- **All Project Tasks**</span></span></br><span data-ttu-id="d4ed4-138">- **Csak a kiválasztott projektfeladatok**.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="d4ed4-139">Az ebben a mezőben szereplő üres érték az **Összes projektfeladat** kijelölésével egyenlő.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="d4ed4-140">Ha a **Csak a kiválasztott feladatok** lehetőség van kiválasztva, akkor kijelölhet bizonyos feladatokat, és hozzárendelheti őket ehhez a szerződés sorhoz a **Projekt** lap **Feladat számlázási beállítása** lapján.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="d4ed4-141">Ezt az értéket a program a **Projekt** és **Hozzáadott tranzakciók** osztályokkal együtt használja, hogy feloldja a szerződéssor hivatkozását egy tényadaton vagy egy becsléssor-rekordon.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="d4ed4-142">**Idővel együtt**</span><span class="sxs-lookup"><span data-stu-id="d4ed4-142">**Include Time**</span></span> | <span data-ttu-id="d4ed4-143">Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt időtranzakciói vagy munkaköltségei szerepelnek-e a szerződéssoron.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="d4ed4-144">A **Nem** érték azt jelzi, hogy a kiválasztott projekthez tartozó időtranzakciók vagy munkaköltségek nem fognak szerepelni ebben a szerződéssorban.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="d4ed4-145">Az **Igen** érték azt jelzi, hogy fognak.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="d4ed4-146">Ez az érték a projekttel együtt egy tényleges vagy becslési sorrekord szerződéssor-hivatkozásának feloldására szolgál.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="d4ed4-147">**Költséggel együtt**</span><span class="sxs-lookup"><span data-stu-id="d4ed4-147">**Include Expense**</span></span> | <span data-ttu-id="d4ed4-148">Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt önköltségei szerepelnek-e a szerződéssorban.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="d4ed4-149">A **Nem** érték azt jelzi, hogy a kiválasztott projekthez tartozó önköltség nem fog szerepelni ebben a szerződéssorban.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="d4ed4-150">Az **Igen** érték azt jelzi, hogy fog.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="d4ed4-151">Ez az érték a projekttel együtt egy tényleges vagy becslési sorrekord szerződéssor-hivatkozásának feloldására szolgál.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="d4ed4-152">**Anyagokkal együtt**</span><span class="sxs-lookup"><span data-stu-id="d4ed4-152">**Include Materials**</span></span> | <span data-ttu-id="d4ed4-153">Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt anyagköltségei szerepelnek-e a szerződéssorban.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="d4ed4-154">A **Nem** érték azt jelzi, hogy az anyagköltségek nem szerepelnek a szerződéssorban.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="d4ed4-155">Az **Igen** érték azt jelzi, hogy fog.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="d4ed4-156">Ez az érték a projekttel együtt egy tényleges vagy becslési sorrekord szerződéssor-hivatkozásának feloldására szolgál.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="d4ed4-157">**Díjjal együtt**</span><span class="sxs-lookup"><span data-stu-id="d4ed4-157">**Include Fee**</span></span> | <span data-ttu-id="d4ed4-158">Az **Igen**/**Nem** érték azt jelzi, hogy a kiválasztott projekt díjai szerepelnek-e a szerződéssorban.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="d4ed4-159">A **Nem** érték azt jelzi, hogy a kiválasztott projekthez tartozó díjak nem fognak szerepelni ebben a szerződéssorban.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="d4ed4-160">Az **Igen** érték azt jelzi, hogy fognak.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="d4ed4-161">Ez az érték a projekttel együtt egy tényleges vagy becslési sorrekord szerződéssor-hivatkozásának feloldására szolgál.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="d4ed4-162">**Szerződésben rögzített összeg**</span><span class="sxs-lookup"><span data-stu-id="d4ed4-162">**Contracted Amount**</span></span> | <span data-ttu-id="d4ed4-163">Rögzített árú szerződéssor esetén ez az összeg egy megállapodott érték, ami számlázva lesz az ügyfélnek a szerződéssorhoz társított összes munkaösszetevőhöz.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="d4ed4-164">Idő és anyag szerződéssor esetén ez az összeg becsült érték arra vonatkozóan, ami számlázva lesz az ügyfélnek a szerződéssorhoz társított összes munkaösszetevőhöz.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="d4ed4-165">Árajánlatból létrehozott projekt-szerződésben a program a az ajánlatsor kapcsolódó mezőjéből másolja át az értéket.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="d4ed4-166">Ha egy projektalapú szerződéssor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és a program a szerződéssor részleteiben szereplő összegből összegzi.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="d4ed4-167">Ha a szerződéssorhoz tartoznak sorrészletek, akkor ez az érték módosítható a sor részleteiben szereplő összegek módosításával.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="d4ed4-168">Rögzített árú szerződéssor esetén ez az érték a periodikus számlázási mérföldkövek után fizetendő összeg generálására szolgál.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="d4ed4-169">**Becsült adó**</span><span class="sxs-lookup"><span data-stu-id="d4ed4-169">**Estimated Tax**</span></span> | <span data-ttu-id="d4ed4-170">A felhasználó módosíthatja ezt a mezőt, hogy a szerződéssor összegére vonatkozóan megadja a becsült adót.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="d4ed4-171">Ha egy projektalapú szerződéssor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és a program a szerződéssor részleteiben szereplő adóösszegből összegzi.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="d4ed4-172">Ha a szerződéssorhoz tartoznak sorrészletek, akkor ez az érték módosítható a sor részleteiben szereplő adóösszegek módosításával.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="d4ed4-173">Rögzített árú szerződéssor esetén ez az érték a periodikus számlázási mérföldkövekhez kapcsolódó adózás előtti összeg generálására szolgál.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="d4ed4-174">**Szerződésben rögzített összeg adózás után**</span><span class="sxs-lookup"><span data-stu-id="d4ed4-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="d4ed4-175">A szerződéssor összege adózás után.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-175">The contract line amount after tax.</span></span> <span data-ttu-id="d4ed4-176">Ez a mező csak olvasható, és számítása a következő: **Szerződött összeg + adó**.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="d4ed4-177">Rögzített árú szerződéssor esetén ez az érték a periodikus számlázási mérföldkövekhez kapcsolódó adó generálására szolgál.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="d4ed4-178">**Nem meghaladandó korlát**</span><span class="sxs-lookup"><span data-stu-id="d4ed4-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="d4ed4-179">A felhasználó szerkesztheti ezt a mezőt, és csak olyan projektalapú szerződéssorok esetén érhető el, amelyek számlázási módja idő és anyag értékre van beállítva.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="d4ed4-180">A felhasználó szerkesztheti ezt a mezőt.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-180">The user can edit this field.</span></span> <span data-ttu-id="d4ed4-181">Ha egy időhöz vagy anyaghoz tartozó tényadat erre a szerződéssorra hivatkozik, akkor tényadathoz tartozó összeg össze lesz vetve a szerződéssor nem túlléphető határértékével.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="d4ed4-182">Ez az értékelés a már elköltött és lekötött összegek figyelembe vételét követően fejeződik be.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="d4ed4-183">**Ügyfél költségvetése**</span><span class="sxs-lookup"><span data-stu-id="d4ed4-183">**Customer Budget**</span></span> | <span data-ttu-id="d4ed4-184">Ez a mező szerkeszthető, és árajánlatból létrehozott projekt-szerződésben a program a az ajánlatsor kapcsolódó mezőjéből másolja át az értéket.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="d4ed4-185">Ez a mező csak tájékoztatásra szolgál, és nincs későbbi jelentősége.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="d4ed4-186">A Projektalapú szerződéssorok Általános lapjának beállításaira vonatkozó ellenőrzési szabályok</span><span class="sxs-lookup"><span data-stu-id="d4ed4-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="d4ed4-187">1. szabály: Ha a **Hozzáadott feladatok** mező üres, vagy **Minden projekttevékenység** értékre van állítva , a projekt minden feladata szerepel a szerződéssoron.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="d4ed4-188">2. szabály: Ha a **Hozzáadott feladatok** mező üres, vagy kifejezetten **Minden projektfeladat** értékre van beállítva, egy projekt vagy egy adott tranzakciós osztály egy szerződésnek csak egy projektalapú szerződéssorán szerepelhet.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="d4ed4-189">3. szabály: Ha a **Hozzáadott feladatok** mező **Csak kiválasztott projektfeladatok** értékre van beállítva, egy projekt vagy egy adott tranzakciós osztály egy szerződésnek több projektalapú szerződéssorán szerepelhet.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="d4ed4-190">
                    <strong>Szerződés</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4ed4-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d4ed4-191">
                    <strong>Szerződéssor</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4ed4-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d4ed4-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4ed4-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="d4ed4-193">
                    <strong>Hozzáadott feladatok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4ed4-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d4ed4-194">
                    <strong>Idővel együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4ed4-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d4ed4-195">
                    <strong>Költséggel együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4ed4-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d4ed4-196">
                    <strong>Anyagokkal együtt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4ed4-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d4ed4-197">
                    <strong>Tartalmazás</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4ed4-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="d4ed4-198">
                    <strong>Díj</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4ed4-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="d4ed4-199">
                    <strong>Érvényes/nem érvényes</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4ed4-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="d4ed4-200">
                    <strong>Ok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4ed4-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d4ed4-201">C1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4ed4-202">CL1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-203">I1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4ed4-204">Üres</span><span class="sxs-lookup"><span data-stu-id="d4ed4-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-205">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-206">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-207">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-208">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4ed4-209">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="d4ed4-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4ed4-210">Az 2. szabály megsértése.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-210">Violation of Rule #2.</span></span> <span data-ttu-id="d4ed4-211">A P1 projektre vonatkozó időt, költséget, anyagokat és díjat az ÁS1 és ÁS2 szerződéssora is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d4ed4-212">C1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4ed4-213">CL2</span><span class="sxs-lookup"><span data-stu-id="d4ed4-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-214">I1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4ed4-215">Üres</span><span class="sxs-lookup"><span data-stu-id="d4ed4-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-216">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-217">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-218">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-219">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-219">Yes</span></span> </p>
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
<span data-ttu-id="d4ed4-220">C1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4ed4-221">CL1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-222">I1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4ed4-223">Üres</span><span class="sxs-lookup"><span data-stu-id="d4ed4-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-224">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-225">No</span><span class="sxs-lookup"><span data-stu-id="d4ed4-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-226">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-227">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4ed4-228">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="d4ed4-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4ed4-229">Az 2. szabály megsértése.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-229">Violation of Rule #2.</span></span> <span data-ttu-id="d4ed4-230">A P1 projektre vonatkozó időt, anyagokat és díjat az ÁS1 és ÁS2 szerződéssora is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d4ed4-231">C1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4ed4-232">CL2</span><span class="sxs-lookup"><span data-stu-id="d4ed4-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-233">I1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4ed4-234">Üres</span><span class="sxs-lookup"><span data-stu-id="d4ed4-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-235">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-236">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-237">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-238">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-238">Yes</span></span> </p>
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
<span data-ttu-id="d4ed4-239">C1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4ed4-240">CL1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-241">I1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4ed4-242">Üres</span><span class="sxs-lookup"><span data-stu-id="d4ed4-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-243">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-244">No</span><span class="sxs-lookup"><span data-stu-id="d4ed4-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-245">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-246">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4ed4-247">Érvényes</span><span class="sxs-lookup"><span data-stu-id="d4ed4-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4ed4-248">A P1 projektre vonatkozó időt, anyagokat és díjat az ÁS1 árajánlatsor tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="d4ed4-249">A P1 projektre vonatkozó költséget a CS2 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="d4ed4-250">Nincs átfedés abban, hogy miket tartalmaznak az egyes szerződéssorok, így ez érvényes.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d4ed4-251">C1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4ed4-252">CL2</span><span class="sxs-lookup"><span data-stu-id="d4ed4-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-253">I1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4ed4-254">Üres</span><span class="sxs-lookup"><span data-stu-id="d4ed4-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-255">No</span><span class="sxs-lookup"><span data-stu-id="d4ed4-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-256">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-257">No</span><span class="sxs-lookup"><span data-stu-id="d4ed4-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-258">No</span><span class="sxs-lookup"><span data-stu-id="d4ed4-258">No</span></span> </p>
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
<span data-ttu-id="d4ed4-259">C1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4ed4-260">CL1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-261">I1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4ed4-262">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="d4ed4-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-263">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-264">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-265">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-266">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4ed4-267">Nem érvényes</span><span class="sxs-lookup"><span data-stu-id="d4ed4-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4ed4-268">A 2. szabály megsértése</span><span class="sxs-lookup"><span data-stu-id="d4ed4-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="d4ed4-269">A C1 tartalmazza a P1 projekttel kapcsolatos feladatok egy részhalmazának idejét, anyagait, költségeit és díjait.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d4ed4-270">A CL2 tartalmazza az egész P1 projektre vonatkozó időt, anyagokat, költségeket és díjakat, ezért átfedésben van a C1 sorral.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d4ed4-271">C1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4ed4-272">CL2</span><span class="sxs-lookup"><span data-stu-id="d4ed4-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-273">I1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4ed4-274">Üres</span><span class="sxs-lookup"><span data-stu-id="d4ed4-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-275">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-276">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-277">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-278">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-278">Yes</span></span> </p>
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
<span data-ttu-id="d4ed4-279">C1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4ed4-280">CL1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-281">I1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4ed4-282">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="d4ed4-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-283">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-284">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-285">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-286">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4ed4-287">Érvényes</span><span class="sxs-lookup"><span data-stu-id="d4ed4-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d4ed4-288">A 3. szabály szerint</span><span class="sxs-lookup"><span data-stu-id="d4ed4-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="d4ed4-289">A C1 tartalmazza a P1 projekttel kapcsolatos feladatok egy részhalmazának idejét, költségeit, anyagait és díjait.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d4ed4-290">A CL2 tartalmazza a P1 projekttel kapcsolatos feladatok egy részhalmazának idejét, anyagait, költségeit és díjait.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d4ed4-291">Az egyetlen további ellenőrzés a CL1-es feladatok részhalmaza körül van, amely eltér a CL2-es feladatok részhalmazától, így biztosítva, hogy ne legyen semmilyen átfedés.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="d4ed4-292">Ezt a rendszer hajtja végre a feladatok társításakor.</span><span class="sxs-lookup"><span data-stu-id="d4ed4-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d4ed4-293">C1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4ed4-294">CL2</span><span class="sxs-lookup"><span data-stu-id="d4ed4-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-295">I1</span><span class="sxs-lookup"><span data-stu-id="d4ed4-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d4ed4-296">Csak a kiválasztott feladatok</span><span class="sxs-lookup"><span data-stu-id="d4ed4-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-297">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d4ed4-298">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-299">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d4ed4-300">Igen</span><span class="sxs-lookup"><span data-stu-id="d4ed4-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
