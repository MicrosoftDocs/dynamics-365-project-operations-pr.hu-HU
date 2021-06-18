---
title: Projekt-erőforrások beállítása
description: Ez a témakör információkat nyújt a projekterőforrások beállításáról vagy kéréséről.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49e0ca6254518079d2e01d92ac2e31d119468c4b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997694"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="c97ac-103">Projekt-erőforrások beállítása</span><span class="sxs-lookup"><span data-stu-id="c97ac-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c97ac-104">Be kell állítania egy naptárat, és társítania kell azt egy alkalmazotthoz vagy egy dolgozóhoz.</span><span class="sxs-lookup"><span data-stu-id="c97ac-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="c97ac-105">A naptár a projekt és a projekt számára fenntartott erőforrások munkaidejének ütemezésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="c97ac-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="c97ac-106">A naptár beállítása során a projektmenedzserek az erőforrás-optimalizálás részeként az erőforrásszintek beállítását is elvégezhetik.</span><span class="sxs-lookup"><span data-stu-id="c97ac-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="c97ac-107">A naptár ütemezése alapján a korlátozások alkalmazhatók az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="c97ac-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="c97ac-108">Beállíthat egy naptárat a **Naptárak** oldalon.</span><span class="sxs-lookup"><span data-stu-id="c97ac-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="c97ac-109">Amikor egy dolgozót projekterőforrásként állít be, kiválaszthatja azokat a dolgozókat, akik annál a vállalatnál dolgoznak, amelyhez az erőforrásokat beállítja.</span><span class="sxs-lookup"><span data-stu-id="c97ac-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="c97ac-110">Másik lehetőségként kiválaszthat dolgozókat a szervezete más vállalataitól is.</span><span class="sxs-lookup"><span data-stu-id="c97ac-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="c97ac-111">Ezek a dolgozók vállalatközi erőforrásként is ismertek.</span><span class="sxs-lookup"><span data-stu-id="c97ac-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="c97ac-112">A következő eljárások azt ismertetik, hogyan állítható be a dolgozó projekterőforrásként a vállalatánál, és hogyan állítható be egy vállalatközi projekterőforrás.</span><span class="sxs-lookup"><span data-stu-id="c97ac-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="c97ac-113">Alkalmazott beállítása projekterőforrásként</span><span class="sxs-lookup"><span data-stu-id="c97ac-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="c97ac-114">A **Dolgozók** oldalon található **Dolgozók** listában jelölje ki a projekterőforrásként hozzáadni kívánt munkatársat, és nyissa meg a munkabejegyzést.</span><span class="sxs-lookup"><span data-stu-id="c97ac-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="c97ac-115">A Művelet panelen válassza a **Projekt** &gt; **Beállítás** &gt; **Projektbeállítás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c97ac-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="c97ac-116">Jelöljön ki egy naptárt, majd zárja be az oldalt.</span><span class="sxs-lookup"><span data-stu-id="c97ac-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="c97ac-117">Az erőforrás alapértelmezett projektjeit az előzetes hozzárendelés típusaként is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="c97ac-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="c97ac-118">Az előzetes hozzárendelések akkor is használhatók, ha az erőforrás-menedzser vagy a projektmenedzser előre tudja, hogy mely projekteken fog az erőforrás dolgozni.</span><span class="sxs-lookup"><span data-stu-id="c97ac-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="c97ac-119">Az előzetes hozzárendelések a projektszponzor vagy ügyfél kérésén is alapulhatnak.</span><span class="sxs-lookup"><span data-stu-id="c97ac-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="c97ac-120">Projekt előzetes hozzárendeléséhez a **Projektek hozzárendelése** oldalon a **Projektek** lap **Hátralévő projektek** listájában válassza ki a megfelelő projektet.</span><span class="sxs-lookup"><span data-stu-id="c97ac-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="c97ac-121">Vállalatközi erőforrás beállítása</span><span class="sxs-lookup"><span data-stu-id="c97ac-121">Set up an intercompany resource</span></span>

<span data-ttu-id="c97ac-122">Ha a munkatársat vállalatközi erőforrásként állítja be, akkor a kölcsönadó vállalatnál és a kölcsönvevő vállalatnál is el kell végeznie a beállítást.</span><span class="sxs-lookup"><span data-stu-id="c97ac-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="c97ac-123">A kölcsönadó vállalatnál</span><span class="sxs-lookup"><span data-stu-id="c97ac-123">In the lending company</span></span>

1. <span data-ttu-id="c97ac-124">A Pénzügy területen ellenőrizze, hogy a kölcsönző vállalat ki van-e jelölve, majd végezze el az előző, „Alkalmazott beállítása projekterőforrásként” című részben leírt eljárást.</span><span class="sxs-lookup"><span data-stu-id="c97ac-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="c97ac-125">A **Vállalatközi könyvelés** oldalon válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c97ac-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="c97ac-126">A **Jogi entitás azonosítója** mezőben válassza ki a kölcsönadó vállalatot.</span><span class="sxs-lookup"><span data-stu-id="c97ac-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="c97ac-127">Töltse ki megfelelően a hátralévő mezőket, majd válassza a **Mentés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c97ac-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="c97ac-128">Az **Transzferár** oldalon válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c97ac-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="c97ac-129">A **Kölcsönbe vevő jogi személy** mezőben válassza ki a megfelelő vállalatot.</span><span class="sxs-lookup"><span data-stu-id="c97ac-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="c97ac-130">Ha csak az ennek a szakasznak a kezdetén létrehozott erőforrást kívánja kölcsönadni a kölcsönvevő vállalatnak, az **Erőforrás** mezőben jelölje ki a létrehozott erőforrás nevét.</span><span class="sxs-lookup"><span data-stu-id="c97ac-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="c97ac-131">Ha a kölcsönadó vállalat összes erőforrását elérhetővé szeretné hozni a kölcsönvevő vállalat számára, akkor hagyja üresen az **Erőforrás** mezőt.</span><span class="sxs-lookup"><span data-stu-id="c97ac-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="c97ac-132">A **Projektmenedzsment és könyvelési paraméterek** oldal **Vállalatközi** lapján állítsa a **Vállalatközi erőforrás-ütemezés és az időnyilvántartások engedélyezése** beállítást **Igen** értékre.</span><span class="sxs-lookup"><span data-stu-id="c97ac-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="c97ac-133">A kölcsönvevő vállalatnál</span><span class="sxs-lookup"><span data-stu-id="c97ac-133">In the borrowing company</span></span>

- <span data-ttu-id="c97ac-134">Az **Erőforrások listája** oldalon a keresési szűrőben írja be a kölcsönadó vállalathoz létrehozott erőforrás nevét annak ellenőrzéséhez, hogy a név szerepel-e a kölcsönvevő vállalathoz tartozó erőforráslistában.</span><span class="sxs-lookup"><span data-stu-id="c97ac-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="c97ac-135">Projekt erőforrásaira vonatkozó kérelmek</span><span class="sxs-lookup"><span data-stu-id="c97ac-135">Request project resources</span></span>
<span data-ttu-id="c97ac-136">A projektek erőforrás-ütemezésére vonatkozó funkció csak az erőforrás-menedzserek számára teszi lehetővé a munkatársakkal ellátott erőforrások elosztását aktivitásokra vagy projektekre.</span><span class="sxs-lookup"><span data-stu-id="c97ac-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="c97ac-137">A szolgáltatás engedélyezéséhez hajtsa végre az alábbi műveleteket, vagy ellenőrizze, hogy befejeződtek-e:</span><span class="sxs-lookup"><span data-stu-id="c97ac-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="c97ac-138">Számsorozatok beállítása.</span><span class="sxs-lookup"><span data-stu-id="c97ac-138">Set up number sequences.</span></span>
- <span data-ttu-id="c97ac-139">Projektmenedzsment és könyvelés munkafolyamatok beállítása.</span><span class="sxs-lookup"><span data-stu-id="c97ac-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="c97ac-140">Erőforrás-igénylési munkafolyamatok engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="c97ac-140">Enable resource request workflows.</span></span>

<span data-ttu-id="c97ac-141">Az előző feladatok befejezését követően az alábbi műveleteket hajthatja végre szükségletei szerint:</span><span class="sxs-lookup"><span data-stu-id="c97ac-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="c97ac-142">Erőforrás-kérelmek létrehozása egy ideiglenesen lefoglalt, munkatársakkal ellátott erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="c97ac-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="c97ac-143">Erőforráskérelmek felügyelete.</span><span class="sxs-lookup"><span data-stu-id="c97ac-143">Monitor resource requests.</span></span>
- <span data-ttu-id="c97ac-144">Erőforrás-kérelmek teljesítése.</span><span class="sxs-lookup"><span data-stu-id="c97ac-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="c97ac-145">Munkatársakkal ellátott erőforrás kérelmezése a WBS-ből.</span><span class="sxs-lookup"><span data-stu-id="c97ac-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="c97ac-146">Erőforrások foglalása egy projekthez egy munkatársakkal ellátott erőforrásra vonatkozó kérelem nélkül.</span><span class="sxs-lookup"><span data-stu-id="c97ac-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]