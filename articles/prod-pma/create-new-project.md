---
title: Új projekt létrehozása
description: Ez a témakör információt nyújt egy új projekt létrehozásáról.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006244"
---
# <a name="create-a-new-project"></a><span data-ttu-id="2f485-103">Új projekt létrehozása</span><span class="sxs-lookup"><span data-stu-id="2f485-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f485-104">A következő lépések elvégzésével hozhat létre új projektet.</span><span class="sxs-lookup"><span data-stu-id="2f485-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="2f485-105">A **Projektmenedzsment** oldalon válassza az **Új projekt** lehetőséget, és adja meg a következő értékeket:</span><span class="sxs-lookup"><span data-stu-id="2f485-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="2f485-106">**Projekttípus:** Idő és anyag</span><span class="sxs-lookup"><span data-stu-id="2f485-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="2f485-107">**Projekt neve:** XYZ frissítés 2. fázis</span><span class="sxs-lookup"><span data-stu-id="2f485-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="2f485-108">**Projektcsoport:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="2f485-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="2f485-109">**Projektszerződés azonosítója:** 00000002</span><span class="sxs-lookup"><span data-stu-id="2f485-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="2f485-110">Válassza a **Projekt létrehozása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2f485-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="2f485-111">Erőforrás hozzárendelése egy projekthez</span><span class="sxs-lookup"><span data-stu-id="2f485-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="2f485-112">A **Dolgozók** oldalon található **Dolgozók** listában jelölje ki annak a dolgozónak a rekordját, akihez korábban kompetenciákat hozott létre, és nyissa meg a dolgozó rekordját.</span><span class="sxs-lookup"><span data-stu-id="2f485-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="2f485-113">A Művelet panelen a **Projekt** lap **Beállítás** csoportjában válassza a **Projektek hozzárendelése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2f485-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="2f485-114">Az **Erőforrás-ellenőrzés projekt-hozzárendelései** oldal **Projektek** lapjának **Projekt hozzáadása a kijelölt projektekhez** mezőjében szűrjön az **XYZ frissítés 2. fázis** projektre.</span><span class="sxs-lookup"><span data-stu-id="2f485-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="2f485-115">A **Fennmaradó projektek** panelen válasszon ki egy projektet, majd válassza a nyíl gombot, majd adja hozzá a **Kijelölt projektek** panelhez.</span><span class="sxs-lookup"><span data-stu-id="2f485-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="2f485-116">Szükség szerint az erőforrásokhoz is hozzárendelhet kategóriákat.</span><span class="sxs-lookup"><span data-stu-id="2f485-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="2f485-117">A kategória típusa vagy **Költség** vagy **Bevétel**.</span><span class="sxs-lookup"><span data-stu-id="2f485-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="2f485-118">A kategória típusát a szervezete határozza meg.</span><span class="sxs-lookup"><span data-stu-id="2f485-118">The category type is determined by your organization.</span></span> <span data-ttu-id="2f485-119">Ha egy erőforráshoz egyetlen kategória sincs hozzárendelve, akkor a Pénzügy az alapértelmezett kategóriát keresi ki a költség és a bevétel óránkénti ára esetében.</span><span class="sxs-lookup"><span data-stu-id="2f485-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="2f485-120">A projekt erőforrás- és szerepkörjellemzőinek beállítása</span><span class="sxs-lookup"><span data-stu-id="2f485-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="2f485-121">A projektmenedzser a projekterőforrások biztosításának funkciójával létrehozhatja a projekthez szükséges erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="2f485-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="2f485-122">A szerepkörök használhatók, ha a megerősített erőforrások még nem ismertek az erőforrások lefoglalása esetén.</span><span class="sxs-lookup"><span data-stu-id="2f485-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="2f485-123">A szerepkörök ideiglenesen lefoglalhatók fenntartott erőforrásként, így folytathatja a projektek tervezési fázisait.</span><span class="sxs-lookup"><span data-stu-id="2f485-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="2f485-124">[![Példa szerepkörre](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="2f485-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="2f485-125">**Szituáció:** A Contoso céget egy idő és anyag alapú projekttel bízták meg, amelyhez tartozik egy jóváhagyott projektcharterrel.</span><span class="sxs-lookup"><span data-stu-id="2f485-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="2f485-126">A junior projektmenedzser még dolgozik a projekt hatókörének befejezésén.</span><span class="sxs-lookup"><span data-stu-id="2f485-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="2f485-127">Az erőforrás-kezelő jelenleg azonosítja azokat az erőforrásokat, amelyek az új projekt munkájához lefoglalásra kerülnek.</span><span class="sxs-lookup"><span data-stu-id="2f485-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="2f485-128">A projekt kritikus jellegéből adódóan a projekt szponzora az egyik szerepkörként a Senior projektmenedzsert kérelmezte.</span><span class="sxs-lookup"><span data-stu-id="2f485-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="2f485-129">Az erőforrás-menedzsernek meg kell szereznie az új erőforrást, és meg kell adnia a szerepkört a rendszerben abban az esetben, ha a junior projektmenedzsernek erőforrásadatokra van szüksége a projekttervezés során.</span><span class="sxs-lookup"><span data-stu-id="2f485-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="2f485-130">A következő lépések azt mutatják, hogy az erőforrás-menedzser hogyan állíthatja be a Senior projektmenedzseri szerepkört, és társíthatja hozzá az erőforrás-jellemzőket.</span><span class="sxs-lookup"><span data-stu-id="2f485-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="2f485-131">Később a szerepkör használható a szükséges erőforrás-kompetenciáknak megfelelő, rendelkezésre álló erőforrások keresésére.</span><span class="sxs-lookup"><span data-stu-id="2f485-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="2f485-132">A **Szerepek beállítása** oldalon válassza az **Új** lehetőséget, és adja meg a következő értékeket:</span><span class="sxs-lookup"><span data-stu-id="2f485-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="2f485-133">**Szerepkör-azonosító:** Senior projektmenedzser</span><span class="sxs-lookup"><span data-stu-id="2f485-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="2f485-134">**Leírás:** Senior projektmenedzser</span><span class="sxs-lookup"><span data-stu-id="2f485-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="2f485-135">Válassza a **Létrehozás** parancsot.</span><span class="sxs-lookup"><span data-stu-id="2f485-135">Select **Create**.</span></span>
3. <span data-ttu-id="2f485-136">Válassza ki a **Senior projektmenedzser** szerepkört, majd válassza a **Tulajdonságok konfigurálása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2f485-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="2f485-137">A **Jellemzők típusa** mezőben válassza a **Készség** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2f485-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="2f485-138">A **Rendelkezésre álló jellemzők** mezőben adja meg a keresendő készséget.</span><span class="sxs-lookup"><span data-stu-id="2f485-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="2f485-139">A **Jellemzők típusa** mezőben válassza a **Tanúsítvány** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2f485-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="2f485-140">A **Rendelkezésre álló jellemzők** mezőben adja meg a keresendő tanúsítványtípust.</span><span class="sxs-lookup"><span data-stu-id="2f485-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="2f485-141">Projekterőforrás hozzárendelése egy projekthez</span><span class="sxs-lookup"><span data-stu-id="2f485-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="2f485-142">A **Minden projekt** oldalon jelölje ki az **XYZ frissítés 2. fázis** projektet.</span><span class="sxs-lookup"><span data-stu-id="2f485-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="2f485-143">A **Projektcsapat és ütemezés** lapon válassza a **Hozzáadás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2f485-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="2f485-144">A **Szerepkör** mezőben jelölje ki a **Csapattag** elemet.</span><span class="sxs-lookup"><span data-stu-id="2f485-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="2f485-145">Válassza a **Foglalás a naptárból** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2f485-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="2f485-146">Az **Erőforrás elérhetősége** oldalon válassza a **Nézet beállításai** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2f485-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="2f485-147">A **Nézet beállításainak módosítása** oldalon adja meg a következő értékeket:</span><span class="sxs-lookup"><span data-stu-id="2f485-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="2f485-148">**Dátumtartomány nézetének formátuma:** Nap</span><span class="sxs-lookup"><span data-stu-id="2f485-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="2f485-149">**Rendelkezésre állási leírások megjelenítése:** Igen</span><span class="sxs-lookup"><span data-stu-id="2f485-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="2f485-150">**Hátralévő kapacitás megjelenítése:** Igen</span><span class="sxs-lookup"><span data-stu-id="2f485-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="2f485-151">Válasszon ki egy erőforrást az erőforrások listájából.</span><span class="sxs-lookup"><span data-stu-id="2f485-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="2f485-152">Válassza **Végleges foglalás** és a **Teljes kapacitás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2f485-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="2f485-153">Rendeljen egy erőforrást az alapértelmezett szerephez</span><span class="sxs-lookup"><span data-stu-id="2f485-153">Assign a resource to a default role</span></span>

<span data-ttu-id="2f485-154">Segítségként a projekt- vagy erőforrás-menedzserek tovább fúrhatnak le az erőforrásokon, amelyek egy projekthez vannak lefoglalva.</span><span class="sxs-lookup"><span data-stu-id="2f485-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="2f485-155">Az alapértelmezett szerepkör társítható meglévő erőforráshoz vagy újonnan megszerzett erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="2f485-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="2f485-156">Amikor például Dániel felvették, megfelelő tapasztalattal és készségekkel rendelkezett az üzleti elemző szerepkör betöltésére.</span><span class="sxs-lookup"><span data-stu-id="2f485-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="2f485-157">Az erőforrás-menedzser ezt a szerepkört rendelte Dánielhez alapértelmezett szerepkörként.</span><span class="sxs-lookup"><span data-stu-id="2f485-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="2f485-158">Ezért az erőforrás-menedzser hozzáadta Dánielt a projekteken végzett munkához rendelkezésre álló üzleti elemzők készletéhez.</span><span class="sxs-lookup"><span data-stu-id="2f485-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="2f485-159">Az erőforrás-foglalás során a projektmenedzserek szűrhetik a projektek számára elérhető szerepkör-erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="2f485-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="2f485-160">Ezeket az információkat felhasználhatják feltételként, amikor a többfeltételű döntési döntéselemzést hajtanak végre az erőforrás-teljesítés során.</span><span class="sxs-lookup"><span data-stu-id="2f485-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="2f485-161">Emellett más erőforrás-jellemzőket is hozzáadhatnak a szűrőhöz, hogy olyan erőforrásokat keressenek, amelyek meghatározott készségekkel, oktatással és tapasztalattal rendelkeznek egy adott projekthez.</span><span class="sxs-lookup"><span data-stu-id="2f485-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="2f485-162">**Forgatókönyv:** Egy jóváhagyott projekt elindult, és a Senior projektmenedzser szerepe a projekt tervezési fázisában tervezett erőforrásként lett lefoglalva.</span><span class="sxs-lookup"><span data-stu-id="2f485-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="2f485-163">Az erőforrás-menedzser most már megszerezte az erőforrást a Senior projektmenedzseri szerepkör betöltéséhez.</span><span class="sxs-lookup"><span data-stu-id="2f485-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="2f485-164">Az **Erőforrások listája** oldalon válassza a **Kovács Dániel** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2f485-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="2f485-165">Az **Erőforrás szerepköre** oldalon válassza az **Új** lehetőséget, és adja meg a következő értékeket:</span><span class="sxs-lookup"><span data-stu-id="2f485-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="2f485-166">**Hatályos:** Adja meg az aktuális dátumot.</span><span class="sxs-lookup"><span data-stu-id="2f485-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="2f485-167">**Lejárat:** Adja meg a **Soha** értéket.</span><span class="sxs-lookup"><span data-stu-id="2f485-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="2f485-168">**Szerepkör:** Adja meg a **Senior projektmenedzser** értéket.</span><span class="sxs-lookup"><span data-stu-id="2f485-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="2f485-169">Válassza a **Mentés** lehetőséget, és zárja be az oldalt.</span><span class="sxs-lookup"><span data-stu-id="2f485-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="2f485-170">A **Kompetenciák** lapon adja hozzá a **ProjectMgmt** készséget és a **PMP** tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="2f485-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]