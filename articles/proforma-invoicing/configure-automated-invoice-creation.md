---
title: Automatikus számla létrehozásának konfigurálása
description: Ez a témakör a rendszer számlák automatikus létrehozásához történő konfigurálásáról tartalmaz információkat.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898129"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="c7bc5-103">Automatikus számla létrehozásának konfigurálása</span><span class="sxs-lookup"><span data-stu-id="c7bc5-103">Configure automated invoice creation</span></span>

<span data-ttu-id="c7bc5-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="c7bc5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c7bc5-105">Ha automatikus számla futtatását szeretnó konfigurálni a Project Operations alkalmazásban, hajtsa végre a következő lépéseket.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="c7bc5-106">Lépjen a **Beállítások** \> **Kötegelt feladatok** menüpontra.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="c7bc5-107">Hozzon létre egy kötegelt feladatot, és adja neki a **Project operations számlák létrehozása** nevet.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="c7bc5-108">A kötegelt feladat nevének tartalmaznia kell a „számlák létrehozása” kifejezést.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="c7bc5-109">A **Feladat típusa** mezőben válassza a **Nincs** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="c7bc5-110">Alapértelmezés szerint a **Napi gyakoriság** és az **Aktív** opciók értéke **Igen**.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="c7bc5-111">Válassza a **Munkamenet futtatása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-111">Select **Run Workflow**.</span></span> <span data-ttu-id="c7bc5-112">A **Rekord keresése** párbeszédpanelen három munkafolyamatot láthat:</span><span class="sxs-lookup"><span data-stu-id="c7bc5-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="c7bc5-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="c7bc5-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="c7bc5-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="c7bc5-114">ProcessRunner</span></span>
    - <span data-ttu-id="c7bc5-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="c7bc5-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="c7bc5-116">Válassza a **ProcessRunCaller** elemet, majd a **Hozzáadás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="c7bc5-117">A következő párbeszédpanelen válassza az **OK** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="c7bc5-118">Az **Alvás** munkafolyamatot egy **Folyamat** munkafolyamat követi.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="c7bc5-119">Az 5. lépésben a **ProcessRunner** lehetőséget is választhatja.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="c7bc5-120">Ezt követően, ha az **OK** lehetőséget választja, a **Folyamat** munkafolyamatot egy **Alvás** munkafolyamat követi.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="c7bc5-121">A **ProcessRunCaller** és a **ProcessRunner** munkafolyamatok számlákat hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="c7bc5-122">**A ProcessRunCaller** munkafolyamat meghívja a **ProcessRunner** munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="c7bc5-123">A **ProcessRunner** az a munkafolyamat, amely ténylegesen létrehozza a számlákat.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="c7bc5-124">Végighalad az összes szerződési soron, amelyhez számlákat kell létrehozni, és számlákat hoz létre ezekre a sorokhoz.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="c7bc5-125">Azon szerződési sorok meghatározásához, amelyekhez számlákat kell létrehozni, a feladat megvizsgálja a szerződési sorok számlafuttatási dátumait.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="c7bc5-126">Ha az adott szerződéshez tartozó szerződési sorok egyazon számlafuttatási dátummal rendelkeznek, a tranzakciók egyetlen számlába kerülnek egyesítésre, amely két számlasorral fog rendelkezni.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="c7bc5-127">Ha nincsenek tranzakciók a számlák létrehozására, akkor a feladat kihagyja a számla létrehozását.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="c7bc5-128">Miután a **ProcessRunner** munkafolyamat futtatása befejeződött, meghívja a **ProcessRunCaller** munkafolyamatot, megadja a befejezési időt, és bezáródik.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="c7bc5-129">A **ProcessRunCaller** ezután elindít egy időzítőt, amely a megadott befejezési időtől kezdve 24 órán át működik.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="c7bc5-130">Az időzítő végén a **ProcessRunCaller** bezáródik.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="c7bc5-131">A számlák létrehozására szolgáló kötegelt folyamat feladat ismétlődő feladat.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="c7bc5-132">Ha ezt a kötegelt folyamatot többször futtatja, akkor a feladatból több példány jön létre, és hibákat okoz.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="c7bc5-133">Ezért a kötegelt folyamatot csak egyszer kell elindítania, és csak akkor kell újraindítania, ha az leáll.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="c7bc5-134">A kötegelt számlázás csak a számlázási ütemezések szerint konfigurált projektek szerződéssoraihoz fut.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="c7bc5-135">A rögzített árú számlázási móddal rendelkező szerződéssornál a mérföldkövek konfigurálása szükséges.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="c7bc5-136">Az idő-és anyagelszámolású számlázási móddal rendelkező projekt-szerződéssorok esetében el kell végezni a dátum alapú számlázási ütemezés beállítását.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="c7bc5-137">Ugyanez érvényes a projektalapú szerződéssor esetében is.</span><span class="sxs-lookup"><span data-stu-id="c7bc5-137">The same applies to a project-based contract line.</span></span>     
