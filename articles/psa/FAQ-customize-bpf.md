---
title: Hogyan szabható testre a Projektfázisok üzleti folyamat?
description: A Projektfázisok üzleti folyamat testreszabásánek áttekintése.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2dccc33088cd9e49e7ffe609f9d9754ef33a5dba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078278"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="44075-103">Hogyan szabható testre a Projektfázisok üzleti folyamat?</span><span class="sxs-lookup"><span data-stu-id="44075-103">How do I customize the Project Stages business process flow?</span></span>
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="44075-104">Van egy ismert korlátozása a Project Service alkalmazás korábbi verzióiban, amely szerint a Projektfázisok üzleti folyamat fázisneveinek pontosan egyezniük a várt angol nevekkel ( **Quote** , **Plan** , **Close** ).</span><span class="sxs-lookup"><span data-stu-id="44075-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names ( **Quote** , **Plan** , **Close** ).</span></span> <span data-ttu-id="44075-105">Ellenkező esetben az üzleti logika, amely a fázisok angol nevén alapul, nem működik megfelelően.</span><span class="sxs-lookup"><span data-stu-id="44075-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="44075-106">Ezért nem láthatók a megszokott, a projektűrlapon elérhető műveletek, például a **Folyamatváltás** vagy a **Folyamat szerkesztése** , és az üzleti folyamat testreszabás nem javasolt.</span><span class="sxs-lookup"><span data-stu-id="44075-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="44075-107">Ezt a korlátozást a 2.4.5.48 és újabb verziókat már feloldottuk.</span><span class="sxs-lookup"><span data-stu-id="44075-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="44075-108">Ebben a cikkben javasolt megoldások találhatók, ha testre kell szabnia az alapértelmezett üzleti folyamatot a korábbi verziókban.</span><span class="sxs-lookup"><span data-stu-id="44075-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="44075-109">Az üzleti logika az angol fázisnevekkel való pontos egyezést követel meg</span><span class="sxs-lookup"><span data-stu-id="44075-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="44075-110">A Projektfázisok üzleti folyamatban üzleti logikát tartalmaz, amely az alkalmazásban az alábbi viselkedéseket váltja ki:</span><span class="sxs-lookup"><span data-stu-id="44075-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="44075-111">Amikor a projekt társítva van egy ajánlattal, a kód a **Quote** fázisra állítja be az üzleti folyamatot.</span><span class="sxs-lookup"><span data-stu-id="44075-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="44075-112">Amikor a projekt társítva van egy szerződéssel, a kód a **Plan** fázisra állítja be az üzleti folyamatot.</span><span class="sxs-lookup"><span data-stu-id="44075-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="44075-113">Ha az üzleti folyamat eljut a **Close** fázisig, a projektrekordot inktiválja.</span><span class="sxs-lookup"><span data-stu-id="44075-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="44075-114">A projekt inaktiválásakor a projektűrlap és a munkalebontási struktúra (WBS) csak olvasható beállítású lesz, megtörténik az elnevezett erőforrások foglalásainak elengedése, és bármilyen kapcsolódó árlisták inaktiválva lesznek.</span><span class="sxs-lookup"><span data-stu-id="44075-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="44075-115">Az üzleti logika az angol nevekre támaszkodik a projektfázisok esetében.</span><span class="sxs-lookup"><span data-stu-id="44075-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="44075-116">Az angol fázisnevektől való függőség a fő ok, amiért a Projektfázisok üzleti folyamat testreszabása nem javasolt, valamint ezért nem láthatók a gyakran használt üzletifolyamat-műveleteket, mint a **Folyamatváltás** vagy a **Folyamat szerkesztése** a projektentitáson.</span><span class="sxs-lookup"><span data-stu-id="44075-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="44075-117">Mi történik, ha a fázisnevek nem egyeznek meg az angol nevekkel?</span><span class="sxs-lookup"><span data-stu-id="44075-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="44075-118">A Project Service alkalmazás 1.x verziójában a 8.2 platformon, ha a fázisok neve az üzleti folyamatban nem egyezik meg pontosan az angol fázisnevekkel, a rendszer átugorja azt az üzleti logikát, amely a megfelelő fázisra állítja az ajánlatokat vagy a szerződéseket, vagy amely bezárja a projektet.</span><span class="sxs-lookup"><span data-stu-id="44075-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="44075-119">Hibaüzenet nem jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="44075-119">No error messages are displayed.</span></span> <span data-ttu-id="44075-120">Ezért úgy tűnik, hogy testreszabható a Projektfázisok üzleti folyamat.</span><span class="sxs-lookup"><span data-stu-id="44075-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="44075-121">Azonban nem fognak működni az automatikus folyamatok az ajánlatok, a szerződések és a projektzárás esetében.</span><span class="sxs-lookup"><span data-stu-id="44075-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="44075-122">A Project Service alkalmazás 2.4.4.30 vagy korábbi verzióban a 9.0 platformon, jelentős architekturális változás történt az üzleti folyamatokban, amely az üzleti folyamat üzleti logikájának újraírását tette szükségessé.</span><span class="sxs-lookup"><span data-stu-id="44075-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="44075-123">Ennek következtében, ha a fázisnevek nem egyeznek meg a várt angol nevekkel, hibaüzenetet kap.</span><span class="sxs-lookup"><span data-stu-id="44075-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="44075-124">Ezért ha testre szeretné szabni a projektentitáshoz a Projektfázisok üzleti folyamatot, csak hozzáadhat teljesen új fázisokat az alapértelmezett üzleti folyamathoz a projektentitáshoz, miközben változatlanul tartja meg az **Ajánlat** , **Terv** és **Bezárás** fázisokat.</span><span class="sxs-lookup"><span data-stu-id="44075-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote** , **Plan** , and **Close** stages as-is.</span></span> <span data-ttu-id="44075-125">Ez a korlátozás biztosítja, hogy nem kap hibákat az üzleti logikától, amely az üzleti folyamatban az angol fázisnevekre számít.</span><span class="sxs-lookup"><span data-stu-id="44075-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="44075-126">A 2.4.5.48 és újabb verziókban az üzleti logika, amelyről ebben a cikkben szó van, kikerült a projektentitás alapértelmezett üzleti folyamatából.</span><span class="sxs-lookup"><span data-stu-id="44075-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="44075-127">A frissítés arra, vagy az újabb verziókra, lehetővé teszi majd az alapértelmezett üzleti folyamat lecserélését egy sajátra.</span><span class="sxs-lookup"><span data-stu-id="44075-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="44075-128">Megkerülő megoldások a korábbi verziók esetén</span><span class="sxs-lookup"><span data-stu-id="44075-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="44075-129">Ha a frissítés nem lehetséges, testreszabhatja a Projektfázisok üzleti folyamatot az alábbi két módon a projektentitáshoz:</span><span class="sxs-lookup"><span data-stu-id="44075-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="44075-130">Adjon hozzá további fázisokat az alapértelmezett konfigurációhoz, miközben megtartja az angol fázisneveket az **Ajánlat** , a **Terv** és a **Bezárás** esetében.</span><span class="sxs-lookup"><span data-stu-id="44075-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote** , **Plan** , and **Close**.</span></span>


![Fázisok hozzáadása az alapértelmezett konfigurációhoz képernyőkép](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="44075-132">Hozzon létre saját üzleti folyamatot, és legyen ez az elsődleges üzleti folyamat a projektentitáshoz, ami lehetővé teszi bármilyen kívánt fázisnév használatát.</span><span class="sxs-lookup"><span data-stu-id="44075-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="44075-133">Azonban ha ugyanazokat a szabványos projektfázisokat is használni kívánja – **Ajánlat** , **Terv** és **Bezárás** – néhány testreszabást kell végrehajtani.</span><span class="sxs-lookup"><span data-stu-id="44075-133">However, if you want to use the same standard project stages **Quote** , **Plan** , and **Close** , you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="44075-134">A bonyolultabb logika a projektzárás, amely továbbra is kiváltható csak a projektbejegyzés inaktiválásával.</span><span class="sxs-lookup"><span data-stu-id="44075-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![BPF testreszabása](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="44075-136">További szempontok a Project Service alkalmazás 2.4.4.30 vagy korábbi verzió esetében a 9.0 platformon</span><span class="sxs-lookup"><span data-stu-id="44075-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="44075-137">A Project Service 2.4.4.30 vagy korábbi verziói esetében a 9.0 platformon, az egyéni üzleti folyamatban a **Fázis neve** mező annál a projektentitásnál, amely a **Projekt fázis szerint** diagramon és a projektlistanézetekben van használatban nem frissül, mert hozzá van kapcsolva az alapértelmezett Projektfázisok üzleti folyamathoz.</span><span class="sxs-lookup"><span data-stu-id="44075-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="44075-138">A probléma a következő lépések végrehajtásával oldható meg:</span><span class="sxs-lookup"><span data-stu-id="44075-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="44075-139">Adja hozzá egy egyéni mezőt, amely az aktuális üzletifolyamat-fázist rögzíti, és amely frissül, ahogy a felhasználó végighalad az egyéni üzleti folyamaton.</span><span class="sxs-lookup"><span data-stu-id="44075-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="44075-140">Módosítsa a **Projekt fázis szerint** diagramot, hogy az egyéni mezőt használja az alapértelmezett beállítás helyett.</span><span class="sxs-lookup"><span data-stu-id="44075-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="44075-141">Lépések saját üzleti folyamat létrehozásához a projektentitáshoz</span><span class="sxs-lookup"><span data-stu-id="44075-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="44075-142">Saját üzleti folyamat létrehozásához a projektentitáshoz tegye a következőt:</span><span class="sxs-lookup"><span data-stu-id="44075-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="44075-143">Válassza a **Beállítások** > **Folyamatközpont** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="44075-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="44075-144">A Projektfázisok üzleti folyamatot ne másolja le, mert ezzel a Project Service üzleti logikáját is lemásolná.</span><span class="sxs-lookup"><span data-stu-id="44075-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Folyamat létrehozása](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="44075-146">A Folyamattervező segítségével hozza létre a kívánt fázisneveket.</span><span class="sxs-lookup"><span data-stu-id="44075-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="44075-147">Ha szeretné az alapértelmezett fázisok funkcióit az **Ajánlat** , **Terv** és **Bezárás** esetében, akkor kell létrehozni ezt az egyéni üzleti folyamat fázisnevei alapján.</span><span class="sxs-lookup"><span data-stu-id="44075-147">If you want the same functionality as the default stages for **Quote** , **Plan** , and **Close** , you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![BPF testreszabásához használt Folyamattervező képernyőképe](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="44075-149">Kattintson a Folyamattervezőben a **Megrendelési folyamat** elemre, hogy az egyéni üzleti folyamatot tegye az elsődleges üzleti folyamattá a projektentitásba azzal, hogy áthelyezi a Projektfázisok üzleti folyamat fölé, a lista tetejére.</span><span class="sxs-lookup"><span data-stu-id="44075-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="44075-150">Megrendelési folyamat használata – képernyőkép</span><span class="sxs-lookup"><span data-stu-id="44075-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="44075-151">A következő lépések a Project Service alkalmazás 2.4.4.30 vagy korábbi verziójára vonatkoznak a 9.0 platformon</span><span class="sxs-lookup"><span data-stu-id="44075-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="44075-152">Adjon hozzá egy új egyéni mezőt a projektentitáshoz az fázisok rögzítésére az egyéni üzleti folyamatban.</span><span class="sxs-lookup"><span data-stu-id="44075-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="44075-153">Üzleti logikát (beépülő modul vagy munkafolyamat) kell hozzáadnia, hogy a mező frissüljön az egyéni üzleti folyamat fázisának+ frissítésekor.</span><span class="sxs-lookup"><span data-stu-id="44075-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Képernyőkép: projektentitás testreszabása](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="44075-155">Módosítsa a **Projekt fázis szerint** diagramot, hogy az új egyéni mezőt használja a fázisokhoz.</span><span class="sxs-lookup"><span data-stu-id="44075-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Képernyőkép: Projekt fázis szerint diagram használata](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="44075-157">Módosítsa az összes érintett nézetet a projektentitáshoz, hogy tartalmazza az új egyéni mezőt a fázisokhoz.</span><span class="sxs-lookup"><span data-stu-id="44075-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Képernyőkép: projektentitáson nézetek módosítása](media/FAQ-Customize-BPF-8-720.png)

