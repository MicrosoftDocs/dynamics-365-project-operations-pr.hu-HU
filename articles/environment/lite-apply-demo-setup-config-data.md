---
title: Bemutató beállítások és konfigurációs adatok alkalmazása
description: Ez a témakör a bemutató beállítás és a konfigurációs adatok Project Operations rendszerben való alkalmazásáról tartalmaz tájékoztatást.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4077957"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="4d1a0-103">A bemutató beállítás és a konfigurációs adatok alkalmazása a Project Operations Lite Lite telepítés – ajánlattól proforma számlázásig alkalmazásra</span><span class="sxs-lookup"><span data-stu-id="4d1a0-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="4d1a0-104">_\*\*Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="4d1a0-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="4d1a0-105">Töltse le a [fő adatcsomagot](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="4d1a0-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="4d1a0-106">Keresse meg a *ProjOpsDemoDataSetupAndMaster - Integrated CMT* mappát, és futtassa a végrehajtható *DataMigrationUtility* fájlt.</span><span class="sxs-lookup"><span data-stu-id="4d1a0-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="4d1a0-107">A Common Data Service konfigurációáttelepítő (CMT) varázsló 1. oldalán válassza az **Adatok importálása** lehetőséget, majd válassza a **Folytatás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="4d1a0-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfiguráció-áttelepítés](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="4d1a0-109">A CMT varázsló 2. oldalán jelölje ki a **Microsoft 365** lehetőséget a **Telepítési típus** értékeként.</span><span class="sxs-lookup"><span data-stu-id="4d1a0-109">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="4d1a0-110">Jelölje be az **Elérhető szervezetek listájának megjelenítése** és a **Speciális megjelenítése** jelölőnégyzeteket.</span><span class="sxs-lookup"><span data-stu-id="4d1a0-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="4d1a0-111">Válassza ki a bérlő régióját, adja meg a hitelesítő adatait, majd válassza a **Bejelentkezés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="4d1a0-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Konfiguráció bejelentkezés](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="4d1a0-113">A 3. oldalon, a bérlő szervezeteinek listájából válassza ki azt a szervezetet, amelybe importálni szeretné a bemutató adatokat, és válassza a **Bejelentkezés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="4d1a0-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="4d1a0-114">A 4. oldalon jelölje ki a *MasterAndSetupData* zip-fájlt a kicsomagolt *ProjOpsDemoDataSetupAndMaster - Integrated CMT* mappából.</span><span class="sxs-lookup"><span data-stu-id="4d1a0-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Zip-fájl](./media/3ZipFile.png)

![Jelöljön ki fájlt](./media/4SelectAFile.png)

9. <span data-ttu-id="4d1a0-117">A zip-fájl kijelölése után válassza az **Adatok importálása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="4d1a0-117">After the zip file is selected, select **Import Data**.</span></span>

![Adatok beolvasása](./media/5ImportData.png)

10. <span data-ttu-id="4d1a0-119">Az Importálás a hálózat sebességétől függően körülbelül két-tíz percig tart.</span><span class="sxs-lookup"><span data-stu-id="4d1a0-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="4d1a0-120">Az befejeződése után lépjen ki a CMT varázslóból.</span><span class="sxs-lookup"><span data-stu-id="4d1a0-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="4d1a0-121">Ellenőrizze a szervezet adatait a következő 20 entitásban:</span><span class="sxs-lookup"><span data-stu-id="4d1a0-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="4d1a0-122">Pénznem</span><span class="sxs-lookup"><span data-stu-id="4d1a0-122">Currency</span></span>
- <span data-ttu-id="4d1a0-123">Szervezeti egység</span><span class="sxs-lookup"><span data-stu-id="4d1a0-123">Organizational Unit</span></span>
- <span data-ttu-id="4d1a0-124">KAPCSOLATTARTÓ</span><span class="sxs-lookup"><span data-stu-id="4d1a0-124">Contact</span></span>
- <span data-ttu-id="4d1a0-125">Adócsoport</span><span class="sxs-lookup"><span data-stu-id="4d1a0-125">Tax Group</span></span>
- <span data-ttu-id="4d1a0-126">Ügyfélcsoport</span><span class="sxs-lookup"><span data-stu-id="4d1a0-126">Customer Group</span></span>
- <span data-ttu-id="4d1a0-127">Kiszerelés</span><span class="sxs-lookup"><span data-stu-id="4d1a0-127">Unit</span></span>
- <span data-ttu-id="4d1a0-128">Egységcsoport</span><span class="sxs-lookup"><span data-stu-id="4d1a0-128">Unit Group</span></span>
- <span data-ttu-id="4d1a0-129">Árlista</span><span class="sxs-lookup"><span data-stu-id="4d1a0-129">Price List</span></span>
- <span data-ttu-id="4d1a0-130">Projektparaméter árlistája</span><span class="sxs-lookup"><span data-stu-id="4d1a0-130">Project Parameter Price List</span></span>
- <span data-ttu-id="4d1a0-131">Számlázási gyakoriság</span><span class="sxs-lookup"><span data-stu-id="4d1a0-131">Invoice Frequency</span></span>
- <span data-ttu-id="4d1a0-132">Számlázási gyakoriság részletei</span><span class="sxs-lookup"><span data-stu-id="4d1a0-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="4d1a0-133">Lefoglalható erőforrás kategóriája</span><span class="sxs-lookup"><span data-stu-id="4d1a0-133">Bookable Resource Category</span></span>
- <span data-ttu-id="4d1a0-134">Tranzakció kategóriája</span><span class="sxs-lookup"><span data-stu-id="4d1a0-134">Transaction Category</span></span>
- <span data-ttu-id="4d1a0-135">Költségkategória</span><span class="sxs-lookup"><span data-stu-id="4d1a0-135">Expense Category</span></span>
- <span data-ttu-id="4d1a0-136">Szerepkörár</span><span class="sxs-lookup"><span data-stu-id="4d1a0-136">Role Price</span></span>
- <span data-ttu-id="4d1a0-137">Tranzakciókategória ára</span><span class="sxs-lookup"><span data-stu-id="4d1a0-137">Transaction Category Price</span></span>
- <span data-ttu-id="4d1a0-138">Jellemző</span><span class="sxs-lookup"><span data-stu-id="4d1a0-138">Characteristic</span></span>
- <span data-ttu-id="4d1a0-139">Lefoglalható erőforrás</span><span class="sxs-lookup"><span data-stu-id="4d1a0-139">Bookable Resource</span></span>
- <span data-ttu-id="4d1a0-140">Lefoglalható erőforrás kategóriatársítása</span><span class="sxs-lookup"><span data-stu-id="4d1a0-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="4d1a0-141">Lefoglalható erőforrás jellemzője</span><span class="sxs-lookup"><span data-stu-id="4d1a0-141">Bookable Resource Characteristic</span></span>

![Importálás befejezése](./media/6CompleteImport.png)
