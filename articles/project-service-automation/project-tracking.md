---
title: A projekt haladása és költségfogyasztása
description: Ez a témakör a projekt előrehaladásának és a költségfelhasználásnak a nyomon követéséről nyújt információkat.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752284"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="57187-103">A projekt haladása és költségfogyasztása</span><span class="sxs-lookup"><span data-stu-id="57187-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="57187-104">Az előrehaladás ütemtervéhez viszonyított nyomon követésének szükségessége iparáganként eltérő.</span><span class="sxs-lookup"><span data-stu-id="57187-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="57187-105">Egyes iparágak granulált szinten követik el, mások viszont magasabb szinten követnek nyomot.</span><span class="sxs-lookup"><span data-stu-id="57187-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="57187-106">Ez a témakör bemutatja, hogyan kell ütemezni a szervezet követelményeit.</span><span class="sxs-lookup"><span data-stu-id="57187-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="57187-107">Erőfeszítések nyomon követésének megtekintése</span><span class="sxs-lookup"><span data-stu-id="57187-107">Effort tracking view</span></span>

<span data-ttu-id="57187-108">Az **Erőfeszítés követése** nézet követi a feladatok előrehaladását az ütemtervben.</span><span class="sxs-lookup"><span data-stu-id="57187-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="57187-109">Összehasonlítja a tényleges erőfeszítési órákat, amelyeket egy feladatra költöttek, az adott feladatra tervezett erőfeszítési órákkal.</span><span class="sxs-lookup"><span data-stu-id="57187-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="57187-110">A PSA a következő képleteket használja a követési mutatók kiszámításához:</span><span class="sxs-lookup"><span data-stu-id="57187-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="57187-111">Haladás százaléka = az eddig elköltött tényleges erőfeszítés ÷ a feladathoz tervezett erőfeszítés</span><span class="sxs-lookup"><span data-stu-id="57187-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="57187-112">Teljes becslés (ETC) = Tervezett erőfeszítés - A ténylegesen elvégzett erőfeszítés eddig</span><span class="sxs-lookup"><span data-stu-id="57187-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="57187-113">Teljes becslés (EAC) = fennmaradó erőfeszítés + az eddig elköltött tényleges erőfeszítés</span><span class="sxs-lookup"><span data-stu-id="57187-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="57187-114">Tervezett erőfeszítés szórása = Tervezett erőfeszítés - EAC</span><span class="sxs-lookup"><span data-stu-id="57187-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="57187-115">A PSA a feladat erőfeszítés-varianciájának előrejelzését mutatja.</span><span class="sxs-lookup"><span data-stu-id="57187-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="57187-116">Ha az EAC meghaladja a tervezett erőfeszítéseket, akkor a feladat várhatóan több időt vesz igénybe, mint az eredetileg tervezték.</span><span class="sxs-lookup"><span data-stu-id="57187-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="57187-117">Ezért elmarad az ütemtervtől.</span><span class="sxs-lookup"><span data-stu-id="57187-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="57187-118">Ha az EAC kevesebb, mint a tervezett erőfeszítés, akkor a feladat várhatóan kevesebb időt vesz igénybe, mint az eredetileg tervezték.</span><span class="sxs-lookup"><span data-stu-id="57187-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="57187-119">Ezért még hamarabb van.</span><span class="sxs-lookup"><span data-stu-id="57187-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="57187-120">Az erőfeszítés újratervezése</span><span class="sxs-lookup"><span data-stu-id="57187-120">Re-projecting effort</span></span>

<span data-ttu-id="57187-121">Általában a projektmenedzser felülvizsgálja a feladat eredeti becsléseit.</span><span class="sxs-lookup"><span data-stu-id="57187-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="57187-122">A projekt újratervezése a projekt menedzserének a becslésről alkotott felfogása, a projekt jelenlegi helyzetére tekintettel.</span><span class="sxs-lookup"><span data-stu-id="57187-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="57187-123">Nem javasoljuk azonban, hogy a projektvezetők megváltoztassák az alapszintet, mivel a projekt alapvonala a megállapított igazságforrást képviseli a projekt ütemterve és költségbecslése szempontjából, és a projekt összes érdekeltje egyetértett azzal.</span><span class="sxs-lookup"><span data-stu-id="57187-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="57187-124">Kétféle módon lehet egy projektmenedzser újraprogramozni a feladatokat:</span><span class="sxs-lookup"><span data-stu-id="57187-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="57187-125">Helyezze felül az alapértelmezett ETC-t egy új becsléssel a feladat tényleges hátralévő erőfeszítéseiről.</span><span class="sxs-lookup"><span data-stu-id="57187-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="57187-126">A feladat valódi előrehaladásának új becslésével felülbírálja az alapértelmezett haladási százalékot.</span><span class="sxs-lookup"><span data-stu-id="57187-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="57187-127">Ezeknek a megközelítéseknek a segítségével át kell számítani a feladat ETC-jét, EAC-ját és az előrehaladási százalékot, valamint a feladatra várható erőfeszítési varianciát.</span><span class="sxs-lookup"><span data-stu-id="57187-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="57187-128">Az EAC, az ETC-t és az összefoglaló feladatok előrehaladási százalékát szintén újraszámolják, és új előrejelzést adnak az erőkifejtés szórására.</span><span class="sxs-lookup"><span data-stu-id="57187-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="57187-129">Az erőfeszítések újratervezése az összefoglaló feladatok során</span><span class="sxs-lookup"><span data-stu-id="57187-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="57187-130">Az összefoglaló vagy a tároló feladatokra tett erőfeszítések újratervezhetők.</span><span class="sxs-lookup"><span data-stu-id="57187-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="57187-131">Függetlenül attól, hogy a felhasználó újraprogramozza-e a fennmaradó erőfeszítést vagy az összefoglaló feladatok előrehaladási százalékát, a következő számítási sorozat kezdődik:</span><span class="sxs-lookup"><span data-stu-id="57187-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="57187-132">Kiszámítják az EAC, ETC és a feladat előrehaladási százalékát.</span><span class="sxs-lookup"><span data-stu-id="57187-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="57187-133">Az új EAC eloszlik a gyermek feladataival azonos arányban, mint az eredeti EAC volt a feladatnál.</span><span class="sxs-lookup"><span data-stu-id="57187-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="57187-134">Kiszámítjuk az új EAC-t az egyes feladatok mindegyikétől egészen a levélcsomóponti feladatokig.</span><span class="sxs-lookup"><span data-stu-id="57187-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="57187-135">Az érintett gyermek feladatait a levélcsomópontokig az ETC-vel és az előrehaladási százalékkal újraszámolják az EAC-érték alapján.</span><span class="sxs-lookup"><span data-stu-id="57187-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="57187-136">Ez új előrejelzést eredményez a feladat erőfeszítési variációja szempontjából.</span><span class="sxs-lookup"><span data-stu-id="57187-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="57187-137">Az összesítő feladatok EAC-ját egészen a gyökércsomópontig újraszámolják.</span><span class="sxs-lookup"><span data-stu-id="57187-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="57187-138">Költségkövetési nézet</span><span class="sxs-lookup"><span data-stu-id="57187-138">Cost tracking view</span></span> 

<span data-ttu-id="57187-139">A **Költségkövetés** nézet összehasonlítja a feladat tényleges költségeit a feladat tervezett költségével.</span><span class="sxs-lookup"><span data-stu-id="57187-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="57187-140">Ez a nézet csak a munkaköltségeket mutatja, és nem tartalmazza a költségbecslésekből származó költségeket.</span><span class="sxs-lookup"><span data-stu-id="57187-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="57187-141">A PSA a következő képleteket használja a követési mutatók kiszámításához:</span><span class="sxs-lookup"><span data-stu-id="57187-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="57187-142">A felhasznált költség százalékos aránya = a mai napig ténylegesen elköltött költség ÷ A feladat tervezett költsége</span><span class="sxs-lookup"><span data-stu-id="57187-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="57187-143">Teljes költség (CTC) = Tervezett költség - a mai napig ténylegesen elköltött költség</span><span class="sxs-lookup"><span data-stu-id="57187-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="57187-144">EAC = CTC + a mai napig töltött tényleges költség</span><span class="sxs-lookup"><span data-stu-id="57187-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="57187-145">Tervezett költség szórás = Tervezett költség - EAC</span><span class="sxs-lookup"><span data-stu-id="57187-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="57187-146">A feladaton látható a költségváltozás vetülete.</span><span class="sxs-lookup"><span data-stu-id="57187-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="57187-147">Ha az EAC meghaladja a tervezett költségeket, akkor a feladat várhatóan többet fog fizetni, mint az eredetileg tervezték.</span><span class="sxs-lookup"><span data-stu-id="57187-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="57187-148">Ezért a költségvetés fölé emelkedik.</span><span class="sxs-lookup"><span data-stu-id="57187-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="57187-149">Ha az EAC kevesebb, mint a tervezett költség, akkor a feladat várhatóan kevesebbre kerül, mint az eredetileg tervezték.</span><span class="sxs-lookup"><span data-stu-id="57187-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="57187-150">Ezért a költségvetés keretein belül növekszik.</span><span class="sxs-lookup"><span data-stu-id="57187-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="57187-151">A projektvezető költségeinek újratervezése</span><span class="sxs-lookup"><span data-stu-id="57187-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="57187-152">Az erőfeszítés újratervezésekor a CTC, az EAC, a felhasznált költségek százalékos arányát és a várható költségváltozást mind a **Költségkövetés** nézetben újraszámolják.</span><span class="sxs-lookup"><span data-stu-id="57187-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="57187-153">A projekt állapotának összefoglalása</span><span class="sxs-lookup"><span data-stu-id="57187-153">Project status summary</span></span>

<span data-ttu-id="57187-154">A követési adatok az **Erőfeszítés követése** és **Költség nyomon követése** nézetekben a projekt gyökércsomópontjában, az összefoglaló feladatokban és a levélcsomópontok feladatainak szintjén mutatják az előrehaladást és a költségfelhasználást.</span><span class="sxs-lookup"><span data-stu-id="57187-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="57187-155">Az **Állapot** szakasz a **Projekt entitás** oldalon a projekt szintű állapotának összefoglalását mutatja.</span><span class="sxs-lookup"><span data-stu-id="57187-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="57187-156">Állapot-összefoglaló mezők</span><span class="sxs-lookup"><span data-stu-id="57187-156">Status summary fields</span></span>

<span data-ttu-id="57187-157">Az **Általános projekt állapota** mező egy szerkeszthető mező, amely a projekt általános állapotát mutatja.</span><span class="sxs-lookup"><span data-stu-id="57187-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="57187-158">Színkódolást használ, például a zöld, a sárga és a vörös, hogy jelezze a növekvő kockázatot.</span><span class="sxs-lookup"><span data-stu-id="57187-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="57187-159">A **Megjegyzések** mezőben a projektmenedzser konkrét megjegyzéseket fűzhet az állapothoz.</span><span class="sxs-lookup"><span data-stu-id="57187-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="57187-160">A **Állapot frissítése** mező nem szerkeszthető, és ez az érték időbélyeg, amely jelzi, ha az állapot utolsó frissítése.</span><span class="sxs-lookup"><span data-stu-id="57187-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="57187-161">Az **Ütemezés teljesítménye** és **Költség teljesítése** mezőket a követési dátumtól kezdve állítják be.</span><span class="sxs-lookup"><span data-stu-id="57187-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="57187-162">Ha a gyökércsomópont ütemezése és költségvarianciája az **Erőfeszítés követése** nézetben pozitív, akkor ezeket a mezőket **Ahead** értékre állíthatja.</span><span class="sxs-lookup"><span data-stu-id="57187-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="57187-163">Ha a gyökércsomópont ütemezése és költségeltérése negatív, akkor ezeket állíthatja **Mögött** értékre.</span><span class="sxs-lookup"><span data-stu-id="57187-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
