---
title: Hitelkártya-integráció beállítása
description: Ez témakör ismerteti, hogyan dolgozzon a költségekkel kapcsolatos hitelkártya-tranzakciókkal.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3555e894e206c2aafb30b0df1e52efadd69b0713
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001822"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="17f08-103">Hitelkártya-integráció beállítása</span><span class="sxs-lookup"><span data-stu-id="17f08-103">Set up credit card integration</span></span>

<span data-ttu-id="17f08-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="17f08-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="17f08-105">A költséggel kapcsolatos hitelkártya-tranzakciók úgy is beállíthatók, hogy a rendszer ismétlődően, ütemezés szerint, automatikusan importálja őket.</span><span class="sxs-lookup"><span data-stu-id="17f08-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="17f08-106">Szükség esetén manuálisan is importálhatja a tranzakciókat.</span><span class="sxs-lookup"><span data-stu-id="17f08-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="17f08-107">A hitelkártya-tranzakciók importálása a hitelkártya-tranzakciók adatentitáson keresztül történik.</span><span class="sxs-lookup"><span data-stu-id="17f08-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="17f08-108">Hitelkártya-tranzakciók importálása</span><span class="sxs-lookup"><span data-stu-id="17f08-108">Import credit card transactions</span></span>

<span data-ttu-id="17f08-109">Hitelkártya-tranzakciók importálása esetén kövesse az alábbi lépéseket:</span><span class="sxs-lookup"><span data-stu-id="17f08-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="17f08-110">A **Hitelkártya-tranzakciók** oldalon válassza a **Tranzakciók importálása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="17f08-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="17f08-111">Ha első alkalommal használja az adatkezelési funkciót, a folytatás előtt a rendszernek frissítenie kell az adatentitások listáját.</span><span class="sxs-lookup"><span data-stu-id="17f08-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="17f08-112">A **Név** mezőbe írja be az importálási feladat egyedi leírását.</span><span class="sxs-lookup"><span data-stu-id="17f08-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="17f08-113">A **Forrás adatformátuma** mezőben válassza ki az importálandó hitelkártya-tranzakciókat tartalmazó fájl formátumát.</span><span class="sxs-lookup"><span data-stu-id="17f08-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="17f08-114">Válassza a **Feltöltés** lehetőséget, majd keresse meg és jelölje ki az importálandó fájlt.</span><span class="sxs-lookup"><span data-stu-id="17f08-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="17f08-115">A fájl feltöltése után érvényesítse a hitelkártya-tranzakciós fájl és a hitelkártya-tranzakciók adatentitáshoz tartozó oszlopok leképezését a csempe **Leképezés megtekintése** hivatkozásával.</span><span class="sxs-lookup"><span data-stu-id="17f08-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="17f08-116">Ha vannak leképezési hibák, vagy ha módosítania kell a leképezést, akkor a szükséges módosításokat a **Leképezés vizualizációja** vagy a **Leképezés részletei** lapon adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="17f08-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="17f08-117">A hitelkártya-tranzakciók automatizálásához válassza az **Ismétlődő feladat létrehozása adatokhoz** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="17f08-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="17f08-118">Ezután beállíthatja azt az ismétlődést, amely meghatározza, hogy milyen gyakran kerüljön sor a hitelkártya-tranzakciók importálására.</span><span class="sxs-lookup"><span data-stu-id="17f08-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="17f08-119">Ha végzett, válassza az **OK** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="17f08-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="17f08-120">Ha azonnal szeretné importálni a kijelölt fájlt, válassza az **Importálás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="17f08-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="17f08-121">Ha az importálás során hibák történnek, megtekintheti a végrehajtási naplót vagy az előkészítési adatokat a sikeres importálás érdekében javítható hibák megtekintéséhez.</span><span class="sxs-lookup"><span data-stu-id="17f08-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="17f08-122">Ha egynél több fájlformátumot kell importálnia, minden formátumtípushoz külön importálási feladatokat kell létrehoznia.</span><span class="sxs-lookup"><span data-stu-id="17f08-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="17f08-123">Lezárt alkalmazottakhoz tartozó hitelkártya-tranzakciók ismételt hozzárendelése</span><span class="sxs-lookup"><span data-stu-id="17f08-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="17f08-124">Ha egy alkalmazott rekordját lezárják, az alkalmazott Active Directory Domain Services-fiókja (AD DS) le lesz tiltva.</span><span class="sxs-lookup"><span data-stu-id="17f08-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="17f08-125">Előfordulhat azonban, hogy vannak olyan aktív hitelkártya-tranzakciók, amelyeket továbbra is ki kell fizetni, és meg kell téríteni.</span><span class="sxs-lookup"><span data-stu-id="17f08-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="17f08-126">A **Hitelkártya-tranzakciók** lapon újra hozzárendelheti az alkalmazottat minden olyan hitelkártya-tranzakcióhoz, ahonnan a társított alkalmazottat eltávolították.</span><span class="sxs-lookup"><span data-stu-id="17f08-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="17f08-127">Jelöljön ki egy vagy több hitelkártya-tranzakciót, majd válassza a **Tranzakciók ismételt hozzárendelése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="17f08-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="17f08-128">Ezután kiválaszthat egy másik alkalmazottat, akit hozzá szeretne rendelni a hitelkártya-tranzakciókhoz.</span><span class="sxs-lookup"><span data-stu-id="17f08-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="17f08-129">A hitelkártya-tranzakciók újbóli hozzárendelése után ezeket a tranzakciókat a rendszer kiválaszthatja a költségjelentésekhez, és kifizethetők a visszatérítések a a költségjelentés szokásos folyamatán keresztül.</span><span class="sxs-lookup"><span data-stu-id="17f08-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="17f08-130">Hitelkártya-tranzakciók törlése</span><span class="sxs-lookup"><span data-stu-id="17f08-130">Delete credit card transactions</span></span> 

<span data-ttu-id="17f08-131">Előfordulhat, hogy a hitelkártya-tranzakciók importálása után bizonyos tranzakciókat törölni kell.</span><span class="sxs-lookup"><span data-stu-id="17f08-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="17f08-132">Ennek az lehet az oka, hogy a tranzakciók ismétlődnek, vagy mert az adatok nem pontosak.</span><span class="sxs-lookup"><span data-stu-id="17f08-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="17f08-133">A rendszergazdák a **„Hitelkártya-tranzakciók törlése”** funkcióval kiválaszthatják és törölhetik azokat a hitelkártya-tranzakciókat, amelyek **nem kapcsolódnak** költségjelentéshez.</span><span class="sxs-lookup"><span data-stu-id="17f08-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="17f08-134">Menjen az **Időszakos feladatok** > **Hitelkártya-tranzakciók törlése** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="17f08-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="17f08-135">Válassza a **Szűrés** lehetőséget, és adjon meg adatokat a felvenni kívánt rekordok azonosításához.</span><span class="sxs-lookup"><span data-stu-id="17f08-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="17f08-136">A rekordok törléséhez válassza az **OK** elemet.</span><span class="sxs-lookup"><span data-stu-id="17f08-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
