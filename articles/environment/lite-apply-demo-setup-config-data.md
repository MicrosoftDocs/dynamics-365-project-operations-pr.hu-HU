---
title: Bemutató beállítások és konfigurációs adatok alkalmazása – Lite
description: Ez a témakör a bemutató beállítás és a konfigurációs adatok Project Operations rendszerben való alkalmazásáról tartalmaz tájékoztatást.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 762b0cf317d442565a033f56033a53a5b5cc435c
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089122"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="f0a29-103">Bemutató beállítások és konfigurációs adatok alkalmazása a Project Operations alkalmazáshoz – Lite</span><span class="sxs-lookup"><span data-stu-id="f0a29-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="f0a29-104">_\*\*Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="f0a29-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="f0a29-105">Előfeltételek</span><span class="sxs-lookup"><span data-stu-id="f0a29-105">Prerequisites</span></span>

<span data-ttu-id="f0a29-106">A konfiguráció megkezdése előtt rendelkeznie kell egy Common Data Service (CDS) környezettel, amelyet a Dynamics 365 Project Operations alkalmazáshoz létesítettek.</span><span class="sxs-lookup"><span data-stu-id="f0a29-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="f0a29-107">Útmutatások</span><span class="sxs-lookup"><span data-stu-id="f0a29-107">Instructions</span></span>

1. <span data-ttu-id="f0a29-108">Töltse le a [fő adatcsomagot](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="f0a29-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="f0a29-109">Keresse meg a *ProjOpsDemoDataSetupAndMaster - Integrated CMT* mappát, és futtassa a végrehajtható *DataMigrationUtility* fájlt.</span><span class="sxs-lookup"><span data-stu-id="f0a29-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="f0a29-110">A Common Data Service konfigurációáttelepítő (CMT) varázsló 1. oldalán válassza az **Adatok importálása** lehetőséget, majd válassza a **Folytatás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f0a29-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Konfiguráció-áttelepítés](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="f0a29-112">A CMT varázsló 2. oldalán jelölje ki a **Microsoft 365** lehetőséget a **Telepítési típus** értékeként.</span><span class="sxs-lookup"><span data-stu-id="f0a29-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="f0a29-113">Jelölje be az **Elérhető szervezetek listájának megjelenítése** és a **Speciális megjelenítése** jelölőnégyzeteket.</span><span class="sxs-lookup"><span data-stu-id="f0a29-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="f0a29-114">Válassza ki a bérlő régióját, adja meg a hitelesítő adatait, majd válassza a **Bejelentkezés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f0a29-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Konfiguráció bejelentkezés](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="f0a29-116">A 3. oldalon, a bérlő szervezeteinek listájából válassza ki azt a szervezetet, amelybe importálni szeretné a bemutató adatokat, és válassza a **Bejelentkezés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f0a29-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="f0a29-117">A 4. oldalon jelölje ki a *MasterAndSetupData* zip-fájlt a kicsomagolt *ProjOpsDemoDataSetupAndMaster - Integrated CMT* mappából.</span><span class="sxs-lookup"><span data-stu-id="f0a29-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

   ![Zip-fájl](./media/3ZipFile.png)

   ![Jelöljön ki fájlt](./media/4SelectAFile.png)

9. <span data-ttu-id="f0a29-120">A zip-fájl kijelölése után válassza az **Adatok importálása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f0a29-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Adatok beolvasása](./media/5ImportData.png)

10. <span data-ttu-id="f0a29-122">Az Importálás a hálózat sebességétől függően körülbelül két-tíz percig tart.</span><span class="sxs-lookup"><span data-stu-id="f0a29-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="f0a29-123">Az befejeződése után lépjen ki a CMT varázslóból.</span><span class="sxs-lookup"><span data-stu-id="f0a29-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="f0a29-124">Ellenőrizze a szervezet adatait a következő 20 entitásban:</span><span class="sxs-lookup"><span data-stu-id="f0a29-124">Check your organization for data in the following 20 entities:</span></span>

    -   <span data-ttu-id="f0a29-125">Pénznem</span><span class="sxs-lookup"><span data-stu-id="f0a29-125">Currency</span></span>
    -   <span data-ttu-id="f0a29-126">Fiók</span><span class="sxs-lookup"><span data-stu-id="f0a29-126">Account</span></span>
    -   <span data-ttu-id="f0a29-127">Szervezeti egység</span><span class="sxs-lookup"><span data-stu-id="f0a29-127">Organizational Unit</span></span>
    -   <span data-ttu-id="f0a29-128">KAPCSOLATTARTÓ</span><span class="sxs-lookup"><span data-stu-id="f0a29-128">Contact</span></span>
    -   <span data-ttu-id="f0a29-129">Kiszerelés</span><span class="sxs-lookup"><span data-stu-id="f0a29-129">Unit</span></span>
    -   <span data-ttu-id="f0a29-130">Egységcsoport</span><span class="sxs-lookup"><span data-stu-id="f0a29-130">Unit Group</span></span>
    -   <span data-ttu-id="f0a29-131">Árlista</span><span class="sxs-lookup"><span data-stu-id="f0a29-131">Price List</span></span>
    -   <span data-ttu-id="f0a29-132">Projektparaméter árlistája</span><span class="sxs-lookup"><span data-stu-id="f0a29-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="f0a29-133">Számlázási gyakoriság</span><span class="sxs-lookup"><span data-stu-id="f0a29-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="f0a29-134">Lefoglalható erőforrás kategóriája</span><span class="sxs-lookup"><span data-stu-id="f0a29-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="f0a29-135">Tranzakció kategóriája</span><span class="sxs-lookup"><span data-stu-id="f0a29-135">Transaction Category</span></span>
    -   <span data-ttu-id="f0a29-136">Költségkategória</span><span class="sxs-lookup"><span data-stu-id="f0a29-136">Expense Category</span></span>
    -   <span data-ttu-id="f0a29-137">Szerepkörár</span><span class="sxs-lookup"><span data-stu-id="f0a29-137">Role Price</span></span>
    -   <span data-ttu-id="f0a29-138">Tranzakciókategória ára</span><span class="sxs-lookup"><span data-stu-id="f0a29-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="f0a29-139">Jellemző</span><span class="sxs-lookup"><span data-stu-id="f0a29-139">Characteristic</span></span>
    -   <span data-ttu-id="f0a29-140">Lefoglalható erőforrás</span><span class="sxs-lookup"><span data-stu-id="f0a29-140">Bookable Resource</span></span>
    -   <span data-ttu-id="f0a29-141">Lefoglalható erőforrás kategóriatársítása</span><span class="sxs-lookup"><span data-stu-id="f0a29-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="f0a29-142">Lefoglalható erőforrás jellemzője</span><span class="sxs-lookup"><span data-stu-id="f0a29-142">Bookable Resource Characteristic</span></span>

    ![Importálás befejezése](./media/6CompleteImport.png)
