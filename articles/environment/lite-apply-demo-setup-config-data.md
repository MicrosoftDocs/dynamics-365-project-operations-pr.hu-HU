---
title: Bemutató beállítások és konfigurációs adatok alkalmazása – Lite
description: Ez a témakör a bemutató beállítás és a konfigurációs adatok Project Operations rendszerben való alkalmazásáról tartalmaz tájékoztatást.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401266"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="75ce4-103">Bemutató beállítások és konfigurációs adatok alkalmazása a Project Operations alkalmazáshoz – Lite</span><span class="sxs-lookup"><span data-stu-id="75ce4-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="75ce4-104">_\*\*Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="75ce4-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="75ce4-105">Előfeltételek</span><span class="sxs-lookup"><span data-stu-id="75ce4-105">Prerequisites</span></span>

<span data-ttu-id="75ce4-106">A konfiguráció megkezdése előtt rendelkeznie kell egy Common Data Service (CDS) környezettel, amelyet a Dynamics 365 Project Operations alkalmazáshoz létesítettek.</span><span class="sxs-lookup"><span data-stu-id="75ce4-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="75ce4-107">Útmutatások</span><span class="sxs-lookup"><span data-stu-id="75ce4-107">Instructions</span></span>

1. <span data-ttu-id="75ce4-108">Töltse le a [fő adatcsomagot](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="75ce4-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="75ce4-109">Keresse meg a *ProjOpsDemoDataSetupAndMaster - Integrated CMT* mappát, és futtassa a végrehajtható *DataMigrationUtility* fájlt.</span><span class="sxs-lookup"><span data-stu-id="75ce4-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="75ce4-110">A Common Data Service konfigurációáttelepítő (CMT) varázsló 1. oldalán válassza az **Adatok importálása** lehetőséget, majd válassza a **Folytatás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="75ce4-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfiguráció-áttelepítés](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="75ce4-112">A CMT varázsló 2. oldalán jelölje ki a **Microsoft 365** lehetőséget a **Telepítési típus** értékeként.</span><span class="sxs-lookup"><span data-stu-id="75ce4-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="75ce4-113">Jelölje be az **Elérhető szervezetek listájának megjelenítése** és a **Speciális megjelenítése** jelölőnégyzeteket.</span><span class="sxs-lookup"><span data-stu-id="75ce4-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="75ce4-114">Válassza ki a bérlő régióját, adja meg a hitelesítő adatait, majd válassza a **Bejelentkezés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="75ce4-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Konfiguráció bejelentkezés](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="75ce4-116">A 3. oldalon, a bérlő szervezeteinek listájából válassza ki azt a szervezetet, amelybe importálni szeretné a bemutató adatokat, és válassza a **Bejelentkezés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="75ce4-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="75ce4-117">A 4. oldalon jelölje ki a *MasterAndSetupData* zip-fájlt a kicsomagolt *ProjOpsDemoDataSetupAndMaster - Integrated CMT* mappából.</span><span class="sxs-lookup"><span data-stu-id="75ce4-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Zip-fájl](./media/3ZipFile.png)

![Jelöljön ki fájlt](./media/4SelectAFile.png)

9. <span data-ttu-id="75ce4-120">A zip-fájl kijelölése után válassza az **Adatok importálása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="75ce4-120">After the zip file is selected, select **Import Data**.</span></span>

![Adatok beolvasása](./media/5ImportData.png)

10. <span data-ttu-id="75ce4-122">Az Importálás a hálózat sebességétől függően körülbelül két-tíz percig tart.</span><span class="sxs-lookup"><span data-stu-id="75ce4-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="75ce4-123">Az befejeződése után lépjen ki a CMT varázslóból.</span><span class="sxs-lookup"><span data-stu-id="75ce4-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="75ce4-124">Ellenőrizze a szervezet adatait a következő 20 entitásban:</span><span class="sxs-lookup"><span data-stu-id="75ce4-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="75ce4-125">Pénznem</span><span class="sxs-lookup"><span data-stu-id="75ce4-125">Currency</span></span>
-   <span data-ttu-id="75ce4-126">Fiók</span><span class="sxs-lookup"><span data-stu-id="75ce4-126">Account</span></span>
-   <span data-ttu-id="75ce4-127">Szervezeti egység</span><span class="sxs-lookup"><span data-stu-id="75ce4-127">Organizational Unit</span></span>
-   <span data-ttu-id="75ce4-128">KAPCSOLATTARTÓ</span><span class="sxs-lookup"><span data-stu-id="75ce4-128">Contact</span></span>
-   <span data-ttu-id="75ce4-129">Adócsoport</span><span class="sxs-lookup"><span data-stu-id="75ce4-129">Tax Group</span></span>
-   <span data-ttu-id="75ce4-130">Ügyfélcsoport</span><span class="sxs-lookup"><span data-stu-id="75ce4-130">Customer Group</span></span>
-   <span data-ttu-id="75ce4-131">Kiszerelés</span><span class="sxs-lookup"><span data-stu-id="75ce4-131">Unit</span></span>
-   <span data-ttu-id="75ce4-132">Egységcsoport</span><span class="sxs-lookup"><span data-stu-id="75ce4-132">Unit Group</span></span>
-   <span data-ttu-id="75ce4-133">Árlista</span><span class="sxs-lookup"><span data-stu-id="75ce4-133">Price List</span></span>
-   <span data-ttu-id="75ce4-134">Projektparaméter árlistája</span><span class="sxs-lookup"><span data-stu-id="75ce4-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="75ce4-135">Számlázási gyakoriság</span><span class="sxs-lookup"><span data-stu-id="75ce4-135">Invoice Frequency</span></span>
-   <span data-ttu-id="75ce4-136">Lefoglalható erőforrás kategóriája</span><span class="sxs-lookup"><span data-stu-id="75ce4-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="75ce4-137">Tranzakció kategóriája</span><span class="sxs-lookup"><span data-stu-id="75ce4-137">Transaction Category</span></span>
-   <span data-ttu-id="75ce4-138">Költségkategória</span><span class="sxs-lookup"><span data-stu-id="75ce4-138">Expense Category</span></span>
-   <span data-ttu-id="75ce4-139">Szerepkörár</span><span class="sxs-lookup"><span data-stu-id="75ce4-139">Role Price</span></span>
-   <span data-ttu-id="75ce4-140">Tranzakciókategória ára</span><span class="sxs-lookup"><span data-stu-id="75ce4-140">Transaction Category Price</span></span>
-   <span data-ttu-id="75ce4-141">Jellemző</span><span class="sxs-lookup"><span data-stu-id="75ce4-141">Characteristic</span></span>
-   <span data-ttu-id="75ce4-142">Lefoglalható erőforrás</span><span class="sxs-lookup"><span data-stu-id="75ce4-142">Bookable Resource</span></span>
-   <span data-ttu-id="75ce4-143">Lefoglalható erőforrás kategóriatársítása</span><span class="sxs-lookup"><span data-stu-id="75ce4-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="75ce4-144">Lefoglalható erőforrás jellemzője</span><span class="sxs-lookup"><span data-stu-id="75ce4-144">Bookable Resource Characteristic</span></span>

![Importálás befejezése](./media/6CompleteImport.png)
