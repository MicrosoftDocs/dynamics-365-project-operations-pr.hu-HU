---
title: Konfigurációs adatok beállítása és alkalmazása a Common Data Service szolgáltatásban
description: Ez a témakör a beállításról és a konfigurációs adatok Project Operations rendszerben való alkalmazásáról tartalmaz tájékoztatást.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642231"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="f4607-103">Konfigurációs adatok beállítása és alkalmazása a Common Data Service szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="f4607-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="f4607-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="f4607-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="f4607-105">Előfeltételek</span><span class="sxs-lookup"><span data-stu-id="f4607-105">Prerequisites</span></span>

<span data-ttu-id="f4607-106">Az adatok Common Data Service (CDS) felületén történő konfigurálásának megkezdése előtt a következő előfeltételeknek kell teljesülnie:</span><span class="sxs-lookup"><span data-stu-id="f4607-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="f4607-107">CDS-környezet és Dynamics 365 Finance-környezet kiépítése a Project Operationshoz.</span><span class="sxs-lookup"><span data-stu-id="f4607-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="f4607-108">A jogi személy adatait meg kell osztani a Dynamics 365 Finance-ből a CDS-környezetbe.</span><span class="sxs-lookup"><span data-stu-id="f4607-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="f4607-109">Ez azt jelenti, hogy a **vállalat** entitás a CDS-ben a következő vállalati rekordokkal rendelkezik:</span><span class="sxs-lookup"><span data-stu-id="f4607-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="f4607-110">THPM</span><span class="sxs-lookup"><span data-stu-id="f4607-110">THPM</span></span>
  - <span data-ttu-id="f4607-111">USPM</span><span class="sxs-lookup"><span data-stu-id="f4607-111">USPM</span></span>
  - <span data-ttu-id="f4607-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="f4607-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="f4607-113">Beállítási és konfigurációs adatok telepítése</span><span class="sxs-lookup"><span data-stu-id="f4607-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="f4607-114">Töltse le, oldja fel, és csomagolja ki a [Beállítási és konfigurációs adatcsomagot](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="f4607-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="f4607-115">Keresse meg a kibontott mappát, és futtassa a végrehajtható *DataMigrationUtility* fájlt.</span><span class="sxs-lookup"><span data-stu-id="f4607-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="f4607-116">A Common Data Service konfigurációáttelepítő (CMT) varázsló 1. oldalán válassza az **Adatok importálása** lehetőséget, majd válassza a **Folytatás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f4607-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfiguráció-áttelepítés](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="f4607-118">A CMT varázsló 2. oldalán jelölje ki a **Microsoft 365** lehetőséget a **Telepítési típus** értékeként.</span><span class="sxs-lookup"><span data-stu-id="f4607-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="f4607-119">Jelölje be az **Elérhető szervezetek listájának megjelenítése** és a **Speciális megjelenítése** jelölőnégyzeteket.</span><span class="sxs-lookup"><span data-stu-id="f4607-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="f4607-120">Válassza ki a bérlő régióját, adja meg a hitelesítő adatait, majd válassza a **Bejelentkezés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f4607-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Konfiguráció bejelentkezés](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="f4607-122">A 3. oldalon, a bérlő szervezeteinek listájából válassza ki azt a szervezetet, amelybe importálni szeretné a bemutató adatokat, és válassza a **Bejelentkezés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f4607-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="f4607-123">A 4. oldalon jelölje ki a *SampleSetupAndConfigData* zip-fájlt a kicsomagolt mappából.</span><span class="sxs-lookup"><span data-stu-id="f4607-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Zip-fájl kiválasztása](./media/3ZipFile.png)

![Jelöljön ki fájlt](./media/4SelectAFile.png)

9. <span data-ttu-id="f4607-126">A zip-fájl kijelölése után válassza az **Adatok importálása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f4607-126">After the zip file is selected, select **Import Data**.</span></span>

![Adatok beolvasása](./media/5ImportData.png)

10. <span data-ttu-id="f4607-128">Az Importálás a hálózat sebességétől függően körülbelül két-tíz percig tart.</span><span class="sxs-lookup"><span data-stu-id="f4607-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="f4607-129">Az importálás befejeződése után lépjen ki a CMT varázslóból.</span><span class="sxs-lookup"><span data-stu-id="f4607-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="f4607-130">Ellenőrizze a szervezet adatait a következő 19 entitásban:</span><span class="sxs-lookup"><span data-stu-id="f4607-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="f4607-131">Pénznem</span><span class="sxs-lookup"><span data-stu-id="f4607-131">Currency</span></span>
  - <span data-ttu-id="f4607-132">Szervezeti egység</span><span class="sxs-lookup"><span data-stu-id="f4607-132">Organizational Unit</span></span>
  - <span data-ttu-id="f4607-133">KAPCSOLATTARTÓ</span><span class="sxs-lookup"><span data-stu-id="f4607-133">Contact</span></span>
  - <span data-ttu-id="f4607-134">Adócsoport</span><span class="sxs-lookup"><span data-stu-id="f4607-134">Tax Group</span></span>
  - <span data-ttu-id="f4607-135">Ügyfélcsoport</span><span class="sxs-lookup"><span data-stu-id="f4607-135">Customer Group</span></span>
  - <span data-ttu-id="f4607-136">Kiszerelés</span><span class="sxs-lookup"><span data-stu-id="f4607-136">Unit</span></span>
  - <span data-ttu-id="f4607-137">Egységcsoport</span><span class="sxs-lookup"><span data-stu-id="f4607-137">Unit Group</span></span>
  - <span data-ttu-id="f4607-138">Árlista</span><span class="sxs-lookup"><span data-stu-id="f4607-138">Price List</span></span>
  - <span data-ttu-id="f4607-139">Projektparaméter árlistája</span><span class="sxs-lookup"><span data-stu-id="f4607-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="f4607-140">Számlázási gyakoriság</span><span class="sxs-lookup"><span data-stu-id="f4607-140">Invoice Frequency</span></span>
  - <span data-ttu-id="f4607-141">Lefoglalható erőforrás kategóriája</span><span class="sxs-lookup"><span data-stu-id="f4607-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="f4607-142">Tranzakció kategóriája</span><span class="sxs-lookup"><span data-stu-id="f4607-142">Transaction Category</span></span>
  - <span data-ttu-id="f4607-143">Költségkategória</span><span class="sxs-lookup"><span data-stu-id="f4607-143">Expense Category</span></span>
  - <span data-ttu-id="f4607-144">Szerepkörár</span><span class="sxs-lookup"><span data-stu-id="f4607-144">Role Price</span></span>
  - <span data-ttu-id="f4607-145">Tranzakciókategória ára</span><span class="sxs-lookup"><span data-stu-id="f4607-145">Transaction Category Price</span></span>
  - <span data-ttu-id="f4607-146">Jellemző</span><span class="sxs-lookup"><span data-stu-id="f4607-146">Characteristic</span></span>
  - <span data-ttu-id="f4607-147">Lefoglalható erőforrás</span><span class="sxs-lookup"><span data-stu-id="f4607-147">Bookable Resource</span></span>
  - <span data-ttu-id="f4607-148">Lefoglalható erőforrás kategóriatársítása</span><span class="sxs-lookup"><span data-stu-id="f4607-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="f4607-149">Lefoglalható erőforrás jellemzője</span><span class="sxs-lookup"><span data-stu-id="f4607-149">Bookable Resource Characteristic</span></span>

![Importálás befejezése](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="f4607-151">A Project Operations-konfigurációk frissítése</span><span class="sxs-lookup"><span data-stu-id="f4607-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="f4607-152">Navigáljon a CE-környezethez.</span><span class="sxs-lookup"><span data-stu-id="f4607-152">Navigate to the CE environment.</span></span> <span data-ttu-id="f4607-153">Ezt megtalálhatja a [Power Platform felügyeleti központ](https://admin.powerplatform.microsoft.com/environments) megnyitásával, a környezet kiválasztásával és a **Környezet megnyitása** lehetőség kiválasztásával.</span><span class="sxs-lookup"><span data-stu-id="f4607-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Környezet megnyitása](./media/7OpenEnvironment.png)

2. <span data-ttu-id="f4607-155">Nyissa meg a **Projektek** > **Erőforrások** részt, és válassza az **Új** lehetőséget foglalható erőforrás létrehozásához a felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="f4607-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Lefoglalható erőforrások](./media/8BookableResources.png)

3. <span data-ttu-id="f4607-157">Az **Általános** lapon válassza ki a rendszergazdai felhasználót.</span><span class="sxs-lookup"><span data-stu-id="f4607-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="f4607-158">Ellenőrizze, hogy az időzóna megegyezik-e az Ön által használt időzónával.</span><span class="sxs-lookup"><span data-stu-id="f4607-158">Verify that the time zone matches the one you are in.</span></span> 

![Új foglalható erőforrás](./media/9NewBookableResource.png)

4. <span data-ttu-id="f4607-160">Az **Ütemezés** lap **Vállalat** mezőjében válassza ki az **USPM** vállalatot, majd válassza a **Mentés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f4607-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Ütemezés lap](./media/10SchedulingTab.png)

5. <span data-ttu-id="f4607-162">Válassza a **Munkaórák** lapot.</span><span class="sxs-lookup"><span data-stu-id="f4607-162">Select the **Work hours** tab.</span></span>  

![Munkaórák](./media/11WorkHours.png)

6. <span data-ttu-id="f4607-164">Kattintson duplán a naptár tetszőleges értékére, és válassza a **Szerkesztés** > **Minden esemény a sorozatban** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f4607-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Munkanaptár](./media/12WorkCalendar.png)

7. <span data-ttu-id="f4607-166">Módosítsa a munkaidőt nyolc (8) órás munkanapra, a hétvégék munkavégzés nélküli napokra történő megjelölésével, és győződjön meg arról, hogy az időzóna megfelel az Ön időzónájának.</span><span class="sxs-lookup"><span data-stu-id="f4607-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="f4607-167">Válassza a **Mentés és bezárás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f4607-167">Select **Save and close**.</span></span>

![Naptár frissítése](./media/13UpdateCalendar.png)

9. <span data-ttu-id="f4607-169">Nyissa meg a **Beállítások** > **Naptársablonok** részt, és válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f4607-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Naptársablonok](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="f4607-171">Adja meg a nevet, jelölje ki a létrehozott sablonerőforrást, majd válassza a **Mentés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f4607-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Naptársablon mentése](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="f4607-173">Nyissa meg a **Paraméterek** részt és kattintson duplán a rekordra.</span><span class="sxs-lookup"><span data-stu-id="f4607-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projektparaméterek](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="f4607-175">Frissítse a következő mezőket:</span><span class="sxs-lookup"><span data-stu-id="f4607-175">Update the following fields:</span></span>

 - <span data-ttu-id="f4607-176">**Alapértelmezett vállalat**: USPM</span><span class="sxs-lookup"><span data-stu-id="f4607-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="f4607-177">**Alapértelmezett szervezeti egység** : Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="f4607-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="f4607-178">**Számlázási gyakoriság**: Hetedik és utolsó nap</span><span class="sxs-lookup"><span data-stu-id="f4607-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="f4607-179">**Munkaidősablon**: Váltson a létrehozott sablonra.</span><span class="sxs-lookup"><span data-stu-id="f4607-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="f4607-180">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="f4607-180">Select **Save**.</span></span> 

![Frissített projektparaméterek](./media/17UpdatedProjectParameters.png)
