---
title: A Feladat rácson való munka hibaelhárítása
description: A témakör a Feladat rácson való munkavégzéshez szükséges hibaelhárítási információkat írja le.
author: ruhercul
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a15a4752de7537b3f60d5ee3269c846257a1fe4a
ms.sourcegitcommit: 72fa1f09fe406805f7009fc68e2f3eeeb9b7d5fc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/09/2021
ms.locfileid: "6213403"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="8d976-103">A Feladat rácson való munka hibaelhárítása</span><span class="sxs-lookup"><span data-stu-id="8d976-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="8d976-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="8d976-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8d976-105">A témakör azt ismerteti, hogyan tudja kijavítani a költségkezelés során esetleg felmerülő problémákat.</span><span class="sxs-lookup"><span data-stu-id="8d976-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="8d976-106">Cookie-k engedélyezése</span><span class="sxs-lookup"><span data-stu-id="8d976-106">Enable cookies</span></span>

<span data-ttu-id="8d976-107">A Project Operations szolgáltatáshoz engedélyezni kell a külső gyártótól származó cookie-kat annak érdekében, hogy a munkalebontási struktúra elérhető legyen.</span><span class="sxs-lookup"><span data-stu-id="8d976-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="8d976-108">Ha a külső gyártótól származó cookie-k nincsenek engedélyezve, a feladatok megjelenítése helyett egy üres oldal jelenik meg, amikor a **Projekt** lapon kijelöli a **Feladatok** fület.</span><span class="sxs-lookup"><span data-stu-id="8d976-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Üres fül jelenik meg, ha a külső gyártótól származó cookie-k nincsenek engedélyezve](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="8d976-110">Megoldás</span><span class="sxs-lookup"><span data-stu-id="8d976-110">Workaround</span></span>
<span data-ttu-id="8d976-111">A következő eljárások ismertetik, hogyan lehet frissíteni a böngésző beállítását a külső cookie-k engedélyezéséhez – Microsoft Edge vagy Google Chrome böngészőknél.</span><span class="sxs-lookup"><span data-stu-id="8d976-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="8d976-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8d976-112">Microsoft Edge</span></span>

1. <span data-ttu-id="8d976-113">Nyissa meg az Edge böngészőt.</span><span class="sxs-lookup"><span data-stu-id="8d976-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="8d976-114">A jobb felső sarokban válassza a **három pont** (...), majd a **Beállítások** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8d976-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="8d976-115">A **Cookie-k és a webjogosultságok** lehetőség alatt válassza a **Cookie-k és a webhelyadatok** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8d976-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="8d976-116">Kapcsolja ki a **Külső gyártótól származó cookie-k blokkolása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8d976-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="8d976-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="8d976-117">Google Chrome</span></span>

1. <span data-ttu-id="8d976-118">Nyissa meg a Chrome böngészőt.</span><span class="sxs-lookup"><span data-stu-id="8d976-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="8d976-119">Kattintson a jobb felső sarokban levő három függőleges pontra, és válassza a **Beállítások** elemet.</span><span class="sxs-lookup"><span data-stu-id="8d976-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="8d976-120">Az **Adatvédelem és a biztonság** lehetőség alatt válassza a **Cookie-k és a egyéb webhelyadatok** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8d976-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="8d976-121">Válassza a **Minden cookie engedélyezése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="8d976-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d976-122">Ha letiltja a harmadik fél cookie-kat, akkor az egyéb webhelyekről származó cookie-kat és webhelyadatokat letiltja a rendszer, még abban az esetben is, ha a webhely engedélyezett a kivételek listáján.</span><span class="sxs-lookup"><span data-stu-id="8d976-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="8d976-123">PEX-végpont</span><span class="sxs-lookup"><span data-stu-id="8d976-123">PEX Endpoint</span></span>

<span data-ttu-id="8d976-124">A Project Operations szolgáltatáshoz szükséges, hogy a projektparaméter a PEX végpontra hivatkozzon.</span><span class="sxs-lookup"><span data-stu-id="8d976-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="8d976-125">A végpontnak kommunikálnia kell a munkalebontási struktúra megjelenítéséhez használt szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="8d976-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="8d976-126">Ha a paraméter nincs engedélyezve, a következő hibaüzenet jelenik meg: „A projektparaméter érvénytelen”.</span><span class="sxs-lookup"><span data-stu-id="8d976-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="8d976-127">Megoldás</span><span class="sxs-lookup"><span data-stu-id="8d976-127">Workaround</span></span>
 ![A projektparaméteren lévő PEX végpont mező](media/projectparameter.png)

1. <span data-ttu-id="8d976-129">Adja hozzá a **PEX végpont** mezőt a **Projektparaméterek** laphoz.</span><span class="sxs-lookup"><span data-stu-id="8d976-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="8d976-130">Frissítse a mezőt a következő értékkel: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="8d976-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`</span></span>
3. <span data-ttu-id="8d976-131">Távolítsa el a mezőt a **Projektparaméterek** oldalról.</span><span class="sxs-lookup"><span data-stu-id="8d976-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="8d976-132">Webes projekt jogosultságai</span><span class="sxs-lookup"><span data-stu-id="8d976-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="8d976-133">A Project Operations egy külső ütemezési szolgáltatásra támaszkodik.</span><span class="sxs-lookup"><span data-stu-id="8d976-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="8d976-134">A szolgáltatáshoz a felhasználónak több szerepkörrel kell rendelkeznie ahhoz, hogy elolvashassa és írhasson a munkalebontási struktúrához kapcsolódó entitásokhoz.</span><span class="sxs-lookup"><span data-stu-id="8d976-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="8d976-135">Ezekhez az entitásokhoz kapcsolódnak projektfeladatok, erőforrás-hozzárendelések és feladatfüggőségek.</span><span class="sxs-lookup"><span data-stu-id="8d976-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="8d976-136">Ha egy felhasználó a **Feladatok** fül megnyitásakor nem tudja leképezni a munkalebontási struktúrát, annak valószínűleg az az oka, hogy a Project Operations projektje még nincs engedélyezve.</span><span class="sxs-lookup"><span data-stu-id="8d976-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="8d976-137">A felhasználónak egy biztonsági szerepkör hibát vagy egy hozzáférésmegtagadási hibát kell kapnia.</span><span class="sxs-lookup"><span data-stu-id="8d976-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="8d976-138">Megoldás</span><span class="sxs-lookup"><span data-stu-id="8d976-138">Workaround</span></span>

1. <span data-ttu-id="8d976-139">Menjen a **Beállítások > Biztonság > Felhasználók > Alkalmazásfelhasználók** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="8d976-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Alkalmazásolvasó](media/applicationuser.jpg)
   
2. <span data-ttu-id="8d976-141">Kattintson duplán az alkalmazás felhasználói bejegyzésére a következő jóváhagyásához:</span><span class="sxs-lookup"><span data-stu-id="8d976-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="8d976-142">A felhasználó hozzáféréssel rendelkezik a projekthez.</span><span class="sxs-lookup"><span data-stu-id="8d976-142">The user has access to the project.</span></span> <span data-ttu-id="8d976-143">Az ellenőrzés általában annak biztosításával történik, hogy a felhasználó **Projektmenedzser** biztonsági szerepkörrel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="8d976-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="8d976-144">A Microsoft Project alkalmazás felhasználója létezik, és megfelelően van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="8d976-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="8d976-145">Ha ez a felhasználó nem létezik, létrehozhat egy új felhasználói rekordot.</span><span class="sxs-lookup"><span data-stu-id="8d976-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="8d976-146">**Új felhasználó** kijelölése.</span><span class="sxs-lookup"><span data-stu-id="8d976-146">Select **New Users**.</span></span> <span data-ttu-id="8d976-147">Módosítsa a bejegyzési űrlapot **Alkalmazás felhasználó** lehetőségre, majd adja meg az **Alkalmazásazonosító** értékét.</span><span class="sxs-lookup"><span data-stu-id="8d976-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Alkalmazás felhasználó részletei](media/applicationuserdetails.jpg)

4. <span data-ttu-id="8d976-149">Ellenőrizze, hogy a felhasználóhoz a megfelelő licenc van-e hozzárendelve, és hogy a szolgáltatás engedélyezve van-e a licenc szolgáltatási terveiben.</span><span class="sxs-lookup"><span data-stu-id="8d976-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="8d976-150">Ellenőrizze, hogy a felhasználó meg tudja-e nyitni a project.microsoft.com webhelyet.</span><span class="sxs-lookup"><span data-stu-id="8d976-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="8d976-151">Ellenőrizze a projekt paraméterein keresztül, hogy a rendszer a megfelelő projektvégpontra mutat-e.</span><span class="sxs-lookup"><span data-stu-id="8d976-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="8d976-152">Ellenőrizze, hogy létrejött-e a projektalkalmazás felhasználója.</span><span class="sxs-lookup"><span data-stu-id="8d976-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="8d976-153">A következő biztonsági szerepköröket alkalmazza a felhasználóra:</span><span class="sxs-lookup"><span data-stu-id="8d976-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="8d976-154">Dataverse-felhasználó</span><span class="sxs-lookup"><span data-stu-id="8d976-154">Dataverse User</span></span>
  - <span data-ttu-id="8d976-155">A Project Operations rendszer</span><span class="sxs-lookup"><span data-stu-id="8d976-155">Project Operations System</span></span>
  - <span data-ttu-id="8d976-156">Projektrendszer</span><span class="sxs-lookup"><span data-stu-id="8d976-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="8d976-157">Hiba a munkalebontási struktúra frissítésekor</span><span class="sxs-lookup"><span data-stu-id="8d976-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="8d976-158">Ha egy vagy több frissítést eszközölnek a munkalebontási struktúrában, akkor a változtatások sikertelenek lesznek, és nem kerülnek mentésre.</span><span class="sxs-lookup"><span data-stu-id="8d976-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="8d976-159">Hiba történik az ütemezési rácsban, és „A legutóbbi módosításait nem lehet menteni” üzenetet fog kapni.</span><span class="sxs-lookup"><span data-stu-id="8d976-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="8d976-160">Megoldás</span><span class="sxs-lookup"><span data-stu-id="8d976-160">Workaround</span></span>

1. <span data-ttu-id="8d976-161">Ellenőrizze, hogy a felhasználóhoz a megfelelő licenc van-e hozzárendelve, és hogy a szolgáltatás engedélyezve van-e a licenc szolgáltatási terveiben.</span><span class="sxs-lookup"><span data-stu-id="8d976-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="8d976-162">Ellenőrizze, hogy a felhasználó meg tudja-e nyitni a project.microsoft.com webhelyet.</span><span class="sxs-lookup"><span data-stu-id="8d976-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="8d976-163">Ellenőrizze, hogy a rendszer a megfelelő projektvégpontra mutat-e.</span><span class="sxs-lookup"><span data-stu-id="8d976-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="8d976-164">Ellenőrizze, hogy létrejött-e a Projektalkalmazás felhasználója.</span><span class="sxs-lookup"><span data-stu-id="8d976-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="8d976-165">A következő biztonsági szerepköröket alkalmazza a felhasználóra:</span><span class="sxs-lookup"><span data-stu-id="8d976-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="8d976-166">Dataverse felhasználó vagy Alapfelhasználó</span><span class="sxs-lookup"><span data-stu-id="8d976-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="8d976-167">A Project Operations rendszer</span><span class="sxs-lookup"><span data-stu-id="8d976-167">Project Operations System</span></span>
  - <span data-ttu-id="8d976-168">Projektrendszer</span><span class="sxs-lookup"><span data-stu-id="8d976-168">Project System</span></span>
  - <span data-ttu-id="8d976-169">A Project Operations kettős írási rendszere (Ez a szerepkör akkor szükséges, ha Project Operations erőforrását/nem készleten alapuló forgatókönyvét telepíti.)</span><span class="sxs-lookup"><span data-stu-id="8d976-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
