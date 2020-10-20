---
title: Beállítási és konfigurációs adatok alkalmazása a Project Operations szolgáltatáshoz használható Common Data Service rendszerben
description: Ez a témakör a beállításról és a konfigurációs adatok Project Operations rendszerben való alkalmazásáról tartalmaz tájékoztatást.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948910"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="f397b-103">Beállítási és konfigurációs adatok alkalmazása a Project Operations szolgáltatáshoz használható Common Data Service rendszerben</span><span class="sxs-lookup"><span data-stu-id="f397b-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="f397b-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="f397b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="f397b-105">Beállítási és konfigurációs adatok telepítése</span><span class="sxs-lookup"><span data-stu-id="f397b-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="f397b-106">Töltse le, oldja fel, és csomagolja ki a [Beállítási és konfigurációs adatcsomagot](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="f397b-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="f397b-107">Keresse meg a kibontott mappát, és futtassa a végrehajtható *DataMigrationUtility* fájlt.</span><span class="sxs-lookup"><span data-stu-id="f397b-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="f397b-108">A Common Data Service konfigurációáttelepítő (CMT) varázsló 1. oldalán válassza az **Adatok importálása** lehetőséget, majd válassza a **Folytatás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f397b-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfiguráció-áttelepítés](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="f397b-110">A CMT varázsló 2. oldalán jelölje ki az **Office 365** lehetőséget a **Telepítési típus** értékeként.</span><span class="sxs-lookup"><span data-stu-id="f397b-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="f397b-111">Jelölje be az **Elérhető szervezetek listájának megjelenítése** és a **Speciális megjelenítése** jelölőnégyzeteket.</span><span class="sxs-lookup"><span data-stu-id="f397b-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="f397b-112">Válassza ki a bérlő régióját, adja meg a hitelesítő adatait, majd válassza a **Bejelentkezés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f397b-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Konfiguráció bejelentkezés](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="f397b-114">A 3. oldalon, a bérlő szervezeteinek listájából válassza ki azt a szervezetet, amelybe importálni szeretné a bemutató adatokat, és válassza a **Bejelentkezés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f397b-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="f397b-115">A 4. oldalon jelölje ki a *SampleSetupAndConfigData* zip-fájlt a kicsomagolt mappából.</span><span class="sxs-lookup"><span data-stu-id="f397b-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Zip-fájl kiválasztása](./media/3ZipFile.png)

![Jelöljön ki fájlt](./media/4SelectAFile.png)

9. <span data-ttu-id="f397b-118">A zip-fájl kijelölése után válassza az **Adatok importálása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f397b-118">After the zip file is selected, select **Import Data**.</span></span>

![Adatok beolvasása](./media/5ImportData.png)

10. <span data-ttu-id="f397b-120">Az Importálás a hálózat sebességétől függően körülbelül két-tíz percig tart.</span><span class="sxs-lookup"><span data-stu-id="f397b-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="f397b-121">Az importálás befejeződése után lépjen ki a CMT varázslóból.</span><span class="sxs-lookup"><span data-stu-id="f397b-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="f397b-122">Ellenőrizze a szervezet adatait a következő 19 entitásban:</span><span class="sxs-lookup"><span data-stu-id="f397b-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="f397b-123">Pénznem</span><span class="sxs-lookup"><span data-stu-id="f397b-123">Currency</span></span>
  - <span data-ttu-id="f397b-124">Szervezeti egység</span><span class="sxs-lookup"><span data-stu-id="f397b-124">Organizational Unit</span></span>
  - <span data-ttu-id="f397b-125">KAPCSOLATTARTÓ</span><span class="sxs-lookup"><span data-stu-id="f397b-125">Contact</span></span>
  - <span data-ttu-id="f397b-126">Adócsoport</span><span class="sxs-lookup"><span data-stu-id="f397b-126">Tax Group</span></span>
  - <span data-ttu-id="f397b-127">Ügyfélcsoport</span><span class="sxs-lookup"><span data-stu-id="f397b-127">Customer Group</span></span>
  - <span data-ttu-id="f397b-128">Kiszerelés</span><span class="sxs-lookup"><span data-stu-id="f397b-128">Unit</span></span>
  - <span data-ttu-id="f397b-129">Egységcsoport</span><span class="sxs-lookup"><span data-stu-id="f397b-129">Unit Group</span></span>
  - <span data-ttu-id="f397b-130">Árlista</span><span class="sxs-lookup"><span data-stu-id="f397b-130">Price List</span></span>
  - <span data-ttu-id="f397b-131">Projektparaméter árlistája</span><span class="sxs-lookup"><span data-stu-id="f397b-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="f397b-132">Számlázási gyakoriság</span><span class="sxs-lookup"><span data-stu-id="f397b-132">Invoice Frequency</span></span>
  - <span data-ttu-id="f397b-133">Lefoglalható erőforrás kategóriája</span><span class="sxs-lookup"><span data-stu-id="f397b-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="f397b-134">Tranzakció kategóriája</span><span class="sxs-lookup"><span data-stu-id="f397b-134">Transaction Category</span></span>
  - <span data-ttu-id="f397b-135">Költségkategória</span><span class="sxs-lookup"><span data-stu-id="f397b-135">Expense Category</span></span>
  - <span data-ttu-id="f397b-136">Szerepkörár</span><span class="sxs-lookup"><span data-stu-id="f397b-136">Role Price</span></span>
  - <span data-ttu-id="f397b-137">Tranzakciókategória ára</span><span class="sxs-lookup"><span data-stu-id="f397b-137">Transaction Category Price</span></span>
  - <span data-ttu-id="f397b-138">Jellemző</span><span class="sxs-lookup"><span data-stu-id="f397b-138">Characteristic</span></span>
  - <span data-ttu-id="f397b-139">Lefoglalható erőforrás</span><span class="sxs-lookup"><span data-stu-id="f397b-139">Bookable Resource</span></span>
  - <span data-ttu-id="f397b-140">Lefoglalható erőforrás kategóriatársítása</span><span class="sxs-lookup"><span data-stu-id="f397b-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="f397b-141">Lefoglalható erőforrás jellemzője</span><span class="sxs-lookup"><span data-stu-id="f397b-141">Bookable Resource Characteristic</span></span>

![Importálás befejezése](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="f397b-143">A Project Operations-konfigurációk frissítése</span><span class="sxs-lookup"><span data-stu-id="f397b-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="f397b-144">Navigáljon a CE-környezethez.</span><span class="sxs-lookup"><span data-stu-id="f397b-144">Navigate to the CE environment.</span></span> <span data-ttu-id="f397b-145">Ezt megtalálhatja a [Power Platform felügyeleti központ](https://admin.powerplatform.microsoft.com/environments) megnyitásával, a környezet kiválasztásával és a **Környezet megnyitása** lehetőség kiválasztásával.</span><span class="sxs-lookup"><span data-stu-id="f397b-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Környezet megnyitása](./media/7OpenEnvironment.png)

2. <span data-ttu-id="f397b-147">Nyissa meg a **Projektek** > **Erőforrások** részt, és válassza az **Új** lehetőséget foglalható erőforrás létrehozásához a felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="f397b-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Lefoglalható erőforrások](./media/8BookableResources.png)

3. <span data-ttu-id="f397b-149">Az **Általános** lapon válassza ki a rendszergazdai felhasználót.</span><span class="sxs-lookup"><span data-stu-id="f397b-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="f397b-150">Ellenőrizze, hogy az időzóna megegyezik-e az Ön által használt időzónával.</span><span class="sxs-lookup"><span data-stu-id="f397b-150">Verify that the time zone matches the one you are in.</span></span> 

![Új foglalható erőforrás](./media/9NewBookableResource.png)

4. <span data-ttu-id="f397b-152">Az **Ütemezés** lap **Vállalat** mezőjében válassza ki az **USPM** vállalatot, majd válassza a **Mentés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f397b-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Ütemezés lap](./media/10SchedulingTab.png)

5. <span data-ttu-id="f397b-154">Válassza a **Munkaórák** lapot.</span><span class="sxs-lookup"><span data-stu-id="f397b-154">Select the **Work hours** tab.</span></span>  

![Munkaórák](./media/11WorkHours.png)

6. <span data-ttu-id="f397b-156">Kattintson duplán a naptár tetszőleges értékére, és válassza a **Szerkesztés** > **Minden esemény a sorozatban** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f397b-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Munkanaptár](./media/12WorkCalendar.png)

7. <span data-ttu-id="f397b-158">Módosítsa a munkaidőt nyolc (8) órás munkanapra, a hétvégék munkavégzés nélküli napokra történő megjelölésével, és győződjön meg arról, hogy az időzóna megfelel az Ön időzónájának.</span><span class="sxs-lookup"><span data-stu-id="f397b-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="f397b-159">Válassza a **Mentés és bezárás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f397b-159">Select **Save and close**.</span></span>

![Naptár frissítése](./media/13UpdateCalendar.png)

9. <span data-ttu-id="f397b-161">Nyissa meg a **Beállítások** > **Naptársablonok** részt, és válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f397b-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Naptársablonok](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="f397b-163">Adja meg a nevet, jelölje ki a létrehozott sablonerőforrást, majd válassza a **Mentés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f397b-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Naptársablon mentése](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="f397b-165">Nyissa meg a **Paraméterek** részt és kattintson duplán a rekordra.</span><span class="sxs-lookup"><span data-stu-id="f397b-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projektparaméterek](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="f397b-167">Frissítse a következő mezőket:</span><span class="sxs-lookup"><span data-stu-id="f397b-167">Update the following fields:</span></span>

 - <span data-ttu-id="f397b-168">**Alapértelmezett vállalat**: USPM</span><span class="sxs-lookup"><span data-stu-id="f397b-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="f397b-169">**Alapértelmezett szervezeti egység** : Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="f397b-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="f397b-170">**Számlázási gyakoriság**: Hetedik és utolsó nap</span><span class="sxs-lookup"><span data-stu-id="f397b-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="f397b-171">**Munkaidősablon**: Váltson a létrehozott sablonra.</span><span class="sxs-lookup"><span data-stu-id="f397b-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="f397b-172">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="f397b-172">Select **Save**.</span></span> 

![Frissített projektparaméterek](./media/17UpdatedProjectParameters.png)
