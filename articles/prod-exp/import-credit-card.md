---
title: Bankkártya-tranzakciók importálása és karbantartása
description: Ez a témakör a költséggel kapcsolatos hitelkártya-tranzakciók importálását és karbantartását ismerteti. Ezek a tranzakciók úgy állíthatók be, hogy ismétlődő ütemezésben automatikusan importálásra kerülnek, illetve szükség esetén kézzel is importálhatók.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 6cec15e436bc699e361577c970dd5845c6c68908
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078245"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="d5aa7-104">Bankkártya-tranzakciók importálása és karbantartása</span><span class="sxs-lookup"><span data-stu-id="d5aa7-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5aa7-105">A költséggel kapcsolatos hitelkártya-tranzakciók úgy is beállíthatók, hogy a rendszer ismétlődően, ütemezés szerint, automatikusan importálja őket.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="d5aa7-106">Szükség esetén manuálisan is importálhatja a tranzakciókat.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="d5aa7-107">A hitelkártya-tranzakciók importálása a Hitelkártya-tranzakciók adatentitáson keresztül történik.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="d5aa7-108">Az adatentitásokkal kapcsolatos további tudnivalókért lásd: [Adatentitások](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="d5aa7-108">For more information about data entities, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="d5aa7-109">Hitelkártya-tranzakciók importálása</span><span class="sxs-lookup"><span data-stu-id="d5aa7-109">Import credit card transactions</span></span>

1. <span data-ttu-id="d5aa7-110">A **Hitelkártya-tranzakciók** oldalon válassza a **Tranzakciók importálása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="d5aa7-111">Ha első alkalommal használja az adatkezelési funkciót, a folytatás előtt a rendszernek frissítenie kell az adatentitások listáját.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="d5aa7-112">A **Név** mezőben adja meg az importálási feladat egyedi leírását.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="d5aa7-113">A **Forrás adatformátuma** mezőben válassza ki az importálandó hitelkártya-tranzakciókat tartalmazó fájl formátumát.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="d5aa7-114">Válassza a **Feltöltés** lehetőséget, majd keresse meg és jelölje ki az importálandó fájlt.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-114">Select **Upload** , and then find and select the file to import.</span></span>
5. <span data-ttu-id="d5aa7-115">A fájl feltöltése után érvényesítse a hitelkártya-tranzakciós fájl és a hitelkártya-tranzakciók adatentitáshoz tartozó oszlopok leképezését a csempe **Leképezés megtekintése** hivatkozásával.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="d5aa7-116">Ha vannak leképezési hibák, vagy ha módosítania kell a leképezést, akkor a szükséges módosításokat a **Leképezés vizualizációja** vagy a **Leképezés részletei** lapon adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="d5aa7-117">A hitelkártya-tranzakciók automatizálásához válassza az **Ismétlődő feladat létrehozása adatokhoz** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="d5aa7-118">Ezután beállíthatja azt az ismétlődést, amely meghatározza, hogy milyen gyakran kerüljön sor a hitelkártya-tranzakciók importálására.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="d5aa7-119">Ha végzett, válassza az **OK** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="d5aa7-120">Ha azonnal szeretné importálni a kijelölt fájlt, válassza az **Importálás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="d5aa7-121">Ha az importálás során hiba történik, akkor a végrehajtási naplóban vagy az előkészítési adatok között tekintheti meg azokat a hibákat, amelyeket ki kell javítania, hogy az importálás sikeres legyen.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="d5aa7-122">Ha több fájlformátumot kell importálnia, akkor mindegyik formátumtípushoz külön importálási feladatot kell létrehoznia.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="d5aa7-123">Lezárt alkalmazottakhoz tartozó hitelkártya-tranzakciók ismételt hozzárendelése</span><span class="sxs-lookup"><span data-stu-id="d5aa7-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="d5aa7-124">Ha egy alkalmazott rekordját lezárják, az alkalmazott Active Directory Domain Services-fiókja (AD DS) le lesz tiltva.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="d5aa7-125">Előfordulhat azonban, hogy vannak olyan aktív hitelkártya-tranzakciók, amelyeket továbbra is ki kell fizetni, és meg kell téríteni.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="d5aa7-126">A **Hitelkártya-tranzakciók** oldalon újra hozzárendelheti az alkalmazottat az olyan hitelkártya-tranzakciók esetén, ahol a társított alkalmazott le van zárva.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="d5aa7-127">Jelöljön ki egy vagy több hitelkártya-tranzakciót, majd válassza a **Tranzakciók ismételt hozzárendelése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="d5aa7-128">Ezután kiválaszthat egy másik alkalmazottat, akit hozzá szeretne rendelni a hitelkártya-tranzakciókhoz.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="d5aa7-129">A hitelkártya-tranzakciók újbóli hozzárendelése után ezeket a tranzakciókat a rendszer kiválaszthatja a költségjelentésekhez, és kifizethetők a visszatérítések a a költségjelentés szokásos folyamatán keresztül.</span><span class="sxs-lookup"><span data-stu-id="d5aa7-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
