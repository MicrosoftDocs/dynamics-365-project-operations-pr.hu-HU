---
title: Projektek és feladatok leképezése egy projektalapú árajánlatsorba
description: Ez a témakör a projektek és feladatok projektalapú feladatsorra való leképezésével kapcsolatban tartalmaz tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 6b396ccf5e76230a42a2f933a3aaa5b8149790bb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/06/2020
ms.locfileid: "3964910"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="70eba-103">Projektek és feladatok leképezése egy projektalapú árajánlatsorba</span><span class="sxs-lookup"><span data-stu-id="70eba-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="70eba-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="70eba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="70eba-105">A projektalapú árajánlatsorokban leképezheti egy olyan projekt adott feladatait, amely már hozzá van rendelve egy árajánlatsorhoz.</span><span class="sxs-lookup"><span data-stu-id="70eba-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="70eba-106">Ha feladatokat képez le egy árajánlatsorba, akkor az árajánlatsorban megadott következő elemek csak az adott feladatokra vonatkoznak:</span><span class="sxs-lookup"><span data-stu-id="70eba-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="70eba-107">Számlázási mód</span><span class="sxs-lookup"><span data-stu-id="70eba-107">Billing method</span></span>
- <span data-ttu-id="70eba-108">Díjazhatósági lehetőségek</span><span class="sxs-lookup"><span data-stu-id="70eba-108">Chargeability options</span></span>
- <span data-ttu-id="70eba-109">Nem meghaladandó korlátok</span><span class="sxs-lookup"><span data-stu-id="70eba-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="70eba-110">Vevők</span><span class="sxs-lookup"><span data-stu-id="70eba-110">Customers</span></span>

<span data-ttu-id="70eba-111">Előfordulhat például, hogy a projektben az egyik fázis a rögzített áras, a többi fázis pedig idő- és anyagelszámolásos.</span><span class="sxs-lookup"><span data-stu-id="70eba-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="70eba-112">Ebben az esetben az első fázist és az összes alárendelt feladatát hozzárendelheti az adott fázishoz tartozó árajánlatsorhoz egy rögzített árú számlázási móddal.</span><span class="sxs-lookup"><span data-stu-id="70eba-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="70eba-113">Ezután az összes többi fázist hozzárendelheti az idő- és anyagalapú árajánlatsorhoz.</span><span class="sxs-lookup"><span data-stu-id="70eba-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="70eba-114">Feladatok hozzárendelése a projektalapú árajánlatsorokhoz</span><span class="sxs-lookup"><span data-stu-id="70eba-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="70eba-115">Hozzárendelhet feladatokat az árajánlatsorokhoz alábbi helyekről:</span><span class="sxs-lookup"><span data-stu-id="70eba-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="70eba-116">**Projekt** oldal > **Feladat számlázása** lap (optimális)</span><span class="sxs-lookup"><span data-stu-id="70eba-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="70eba-117">**Árajánlatsor** oldal > **Felszámítható feladatok** lap</span><span class="sxs-lookup"><span data-stu-id="70eba-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="70eba-118">A Projekt oldalról</span><span class="sxs-lookup"><span data-stu-id="70eba-118">From the Project page</span></span>

<span data-ttu-id="70eba-119">A **Projekt** oldal optimális felhasználói élményt nyújt a feladatok árajánlatsorokhoz való társításához.</span><span class="sxs-lookup"><span data-stu-id="70eba-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="70eba-120">Ezen az oldalon több feladatot is kijelölhet, és az összeset, valamint alárendelt feladatait hozzárendelheti a kijelölt árajánlatsorhoz.</span><span class="sxs-lookup"><span data-stu-id="70eba-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="70eba-121">A projektalapú árajánlatsor **Általános** lapján ellenőrizze, hogy a **Projekt** mező ki van-e töltve.</span><span class="sxs-lookup"><span data-stu-id="70eba-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="70eba-122">A **Hozzáadott feladatok** mezőben válassza ki a **Csak a kiválasztott feladatok** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="70eba-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="70eba-123">Mentse a projektalapú árajánlatsorokat.</span><span class="sxs-lookup"><span data-stu-id="70eba-123">Save the project-based quote line.</span></span> <span data-ttu-id="70eba-124">Az űrlap frissítésekor a **Felszámítható feladatok** lap jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="70eba-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="70eba-125">Az **Általános** lapon jelölje ki a projekthez tartozó hivatkozást a **Projekt** mezőben.</span><span class="sxs-lookup"><span data-stu-id="70eba-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="70eba-126">A **Projekt** oldalon lépjen a **Feladat számlázása** lapra.</span><span class="sxs-lookup"><span data-stu-id="70eba-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="70eba-127">A második rácson, amely a feladatspecifikus számlázási beállításra vonatkozik, válasszon ki egy vagy több feladatot, majd válassza az **Árajánlatsorok hozzárendelése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="70eba-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="70eba-128">A megjelenő párbeszédpanelen válasszon egy árajánlatsort, amely az árajánlat projektalapú árajánlatsorait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="70eba-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="70eba-129">A **Számlázási típus** mezőben adja meg, hogy ezek a feladatok felszámíthatók vagy nem felszámíthatók-e.</span><span class="sxs-lookup"><span data-stu-id="70eba-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="70eba-130">Jelölje be a jelölőnégyzetet, ha jelezni szeretné, hogy a hozzárendelésnek tartalmaznia kell a kiválasztott tevékenységek alárendelt feladatait.</span><span class="sxs-lookup"><span data-stu-id="70eba-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="70eba-131">A mező kiválasztásával hozzárendeli a kiválasztott feladatok alárendelt feladatait az árajánlatsorhoz.</span><span class="sxs-lookup"><span data-stu-id="70eba-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="70eba-132">Válassza az **OK** elemet a párbeszédpanel bezárásához.</span><span class="sxs-lookup"><span data-stu-id="70eba-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="70eba-133">Az Árajánlatsor oldalról</span><span class="sxs-lookup"><span data-stu-id="70eba-133">From the Quote line page</span></span>

<span data-ttu-id="70eba-134">A projektfeladatokat az árajánlatsorokhoz társíthatja a **Felszámítható feladatok** lapon, az **Árajánlatsor** oldalon.</span><span class="sxs-lookup"><span data-stu-id="70eba-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="70eba-135">A projektfeladatok árajánlatsorokhoz történő hozzárendelésére az optimális hely a **Projekt** oldal **Feladat számlázása** lapja.</span><span class="sxs-lookup"><span data-stu-id="70eba-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="70eba-136">Ha az **Árajánlatsor** oldal **Felszámítható feladatok** lapjáról rendel hozzá feladatokat, akkor manuálisan kell társítania az egyes projekteket.</span><span class="sxs-lookup"><span data-stu-id="70eba-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="70eba-137">A projektalapú árajánlatsor **Általános** lapján ellenőrizze, hogy a **Projekt** mezőben ki van-e választva egy projekt.</span><span class="sxs-lookup"><span data-stu-id="70eba-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="70eba-138">A **Hozzáadott feladatok** mezőben válassza ki a **Csak a kiválasztott feladatok** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="70eba-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="70eba-139">Mentse a projektalapú árajánlatsorokat.</span><span class="sxs-lookup"><span data-stu-id="70eba-139">Save the project-based quote line.</span></span> <span data-ttu-id="70eba-140">Az űrlap frissítésekor a **Felszámítható feladatok** lap jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="70eba-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="70eba-141">A **Felszámítható feladatok** lapon válassza az **Árajánlatsor-feladat hozzáadása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="70eba-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="70eba-142">Az **Árajánlatsor-feladat** oldalon, a **Feladatok** mezőben jelölje ki a feladatot, és a **Számlázás típusa** mezőben válassza a **Mentés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="70eba-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="70eba-143">Zárja be a lapot.</span><span class="sxs-lookup"><span data-stu-id="70eba-143">Close the page.</span></span> <span data-ttu-id="70eba-144">A kijelölt feladat most az árajánlatsorhoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="70eba-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="70eba-145">Feladatok projektalapú árajánlatsorokhoz való hozzárendelésének törlése</span><span class="sxs-lookup"><span data-stu-id="70eba-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="70eba-146">A Projekt oldalról</span><span class="sxs-lookup"><span data-stu-id="70eba-146">From the Project page</span></span>

<span data-ttu-id="70eba-147">Ez a módszer a legoptimálisabb felhasználói élményt nyújtja a feladatok árajánlatsorokhoz való társításának törléséhez.</span><span class="sxs-lookup"><span data-stu-id="70eba-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="70eba-148">Ezen az oldalon több feladatot is kijelölhet, és az összes, valamint alárendelt feladatainak hozzárendelését törölheti a kijelölt árajánlatsorról.</span><span class="sxs-lookup"><span data-stu-id="70eba-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="70eba-149">A projektalapú árajánlatsor **Általános** lapján, a **Projekt** mezőben válassza ki a projekt hivatkozását.</span><span class="sxs-lookup"><span data-stu-id="70eba-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="70eba-150">A **Projekt** oldalon lépjen a **Feladat számlázása** lapra.</span><span class="sxs-lookup"><span data-stu-id="70eba-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="70eba-151">A második rácson, amely a feladatspecifikus számlázási beállításra vonatkozik, válasszon ki egy vagy több feladatot, majd válassza az **Árajánlatsorok hozzárendelésének visszavonása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="70eba-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="70eba-152">A megjelenő párbeszédpanelen jelöljön ki egy árajánlatsort.</span><span class="sxs-lookup"><span data-stu-id="70eba-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="70eba-153">Jelölje be a jelölőnégyzetet, ha jelezni szeretné, hogy a hozzárendelésnek a kiválasztott tevékenységek alárendelt feladatairól is eltávolításra kell kerülnie.</span><span class="sxs-lookup"><span data-stu-id="70eba-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="70eba-154">A mező kiválasztásával továbbá visszavonhatja a kiválasztott feladatok alárendelt feladatait az árajánlatsorhoz való hozzárendelését.</span><span class="sxs-lookup"><span data-stu-id="70eba-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="70eba-155">Kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="70eba-155">Select **OK**.</span></span> <span data-ttu-id="70eba-156">Egy figyelmeztető üzenet arról tájékoztatja, hogy ha eltávolítja ezt a társítást, a feladathoz előzőleg rögzített tényleges adatokat a rendszer sztornírozhatja.</span><span class="sxs-lookup"><span data-stu-id="70eba-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="70eba-157">Válassza az **OK** lehetőséget a feladat és a projektalapú árajánlatsor közötti társítás eltávolításának folytatásához.</span><span class="sxs-lookup"><span data-stu-id="70eba-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="70eba-158">Az Árajánlatsor oldalról</span><span class="sxs-lookup"><span data-stu-id="70eba-158">From the Quote line page</span></span>

<span data-ttu-id="70eba-159">Visszavonhatja továbbá a projektfeladatok és az árajánlatsorok társítását a **Felszámítható feladatok** lapon, az **Árajánlatsor** oldalon.</span><span class="sxs-lookup"><span data-stu-id="70eba-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="70eba-160">A **Felszámítható feladatok** lapon válassza az **Árajánlatsor-feladat törlése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="70eba-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="70eba-161">Kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="70eba-161">Select **OK**.</span></span> <span data-ttu-id="70eba-162">Egy figyelmeztető üzenet arról tájékoztatja, hogy ha eltávolítja ezt a társítást, a feladathoz előzőleg rögzített tényleges adatokat a rendszer sztornírozhatja.</span><span class="sxs-lookup"><span data-stu-id="70eba-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="70eba-163">Válassza az **OK** lehetőséget a feladat és a projektalapú árajánlatsor közötti társítás eltávolításának folytatásához.</span><span class="sxs-lookup"><span data-stu-id="70eba-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="70eba-164">Ez az eljárás nem törli a feladatot a projektből.</span><span class="sxs-lookup"><span data-stu-id="70eba-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="70eba-165">Csak eltávolítja a feladat-hozzárendelést a projektalapú árajánlatsorból.</span><span class="sxs-lookup"><span data-stu-id="70eba-165">It only removes the task association from the project-based quote line.</span></span>
