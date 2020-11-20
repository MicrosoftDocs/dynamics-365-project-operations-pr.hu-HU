---
title: Utazási kérelmek
description: Ez a témakör az utazási kérelmekről tartalmaz információkat.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 46a678ac4486c99f11d74dbac07dedd08364cb2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123741"
---
# <a name="travel-requisitions"></a><span data-ttu-id="4a740-103">Utazási kérelmek</span><span class="sxs-lookup"><span data-stu-id="4a740-103">Travel requisitions</span></span>

<span data-ttu-id="4a740-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="4a740-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4a740-105">Az utazási kérelem felsorolja az utazás céljából felmerülő költségeket.</span><span class="sxs-lookup"><span data-stu-id="4a740-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="4a740-106">Az utazási kérelmet be kell nyújtani áttekintésre, és felhasználható a kiadások engedélyezésére.</span><span class="sxs-lookup"><span data-stu-id="4a740-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="4a740-107">Előfordulhat, hogy utazási kérelmet kell benyújtania, mielőtt felszámíthatna bármilyen kiadást a szervezet felé.</span><span class="sxs-lookup"><span data-stu-id="4a740-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="4a740-108">Ez a követelmény érvényes, függetlenül attól, hogy a vállalat hitelkártyájára terheli a felmerülő kiadásokat, készpénzelőlegként kapott készpénzt költ, vagy a szervezet által visszatérítendő, saját pénzből fedezett kiadások merültek fel.</span><span class="sxs-lookup"><span data-stu-id="4a740-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="4a740-109">Az utazási kérelmek és házirendek használhatók a szervezeti kiadások kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="4a740-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="4a740-110">Ha például a szervezet olyan rögzített árú projekten dolgozik, amelyhez utazás szükséges, a projektcsoporttagok utazási költségeinek a projekt költségvetéséhez kell illeszkednie.</span><span class="sxs-lookup"><span data-stu-id="4a740-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="4a740-111">Ha megköveteli, hogy az utazási költségeket a felszámításuk előtt jóvá kell hagyni, a szervezet segíthet annak biztosításában, hogy a projekt a költségvetésen belül maradjon.</span><span class="sxs-lookup"><span data-stu-id="4a740-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="4a740-112">Konfigurálás</span><span class="sxs-lookup"><span data-stu-id="4a740-112">Configuration</span></span> 

<span data-ttu-id="4a740-113">Az utazási kérelmek a „kötelezőként” állíthatók be, ha engedélyezi „Az utazás előzetes engedélyezése kötelező” paramétert a Költségkezelés paraméterei részben.</span><span class="sxs-lookup"><span data-stu-id="4a740-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="4a740-114">Utazási kérelem létrehozása és elküldése</span><span class="sxs-lookup"><span data-stu-id="4a740-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="4a740-115">Válassza a **Saját kiadások: Utazási kérelem** lehetőséget, és válassza az **Új utazási kérelem** elemet.</span><span class="sxs-lookup"><span data-stu-id="4a740-115">Go to **My expenses: Travel Requisition**, and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="4a740-116">Adja meg a kérelem célját és úti célját.</span><span class="sxs-lookup"><span data-stu-id="4a740-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="4a740-117">Az **Utazás leírása** mezőben adja meg a további adatokat.</span><span class="sxs-lookup"><span data-stu-id="4a740-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="4a740-118">Az egyes várt kiadások, például a repülés, az étkezés vagy az autókölcsönzés esetén hozzon létre egy költségsortételt.</span><span class="sxs-lookup"><span data-stu-id="4a740-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="4a740-119">Adja meg a becsült dátumot, a becsült összeget és az egyes kiadások pénznemét.</span><span class="sxs-lookup"><span data-stu-id="4a740-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="4a740-120">Amikor befejezte a várható kiadások hozzáadását, válassza a **Mentés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="4a740-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="4a740-121">Amikor készen áll az utazási kérelem elküldésére, válassza a **Munkafolyamat** > **Küldés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="4a740-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="4a740-122">A jóváhagyott utazási kérelmeket a **Saját kiadások: Utazási kérelem** alatt tekintheti meg.</span><span class="sxs-lookup"><span data-stu-id="4a740-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="4a740-123">Rendelkezésre álló utazási kérelmek megtekintése</span><span class="sxs-lookup"><span data-stu-id="4a740-123">View available travel requisitions</span></span>

<span data-ttu-id="4a740-124">Az összes jóváhagyott utazási kérelmeket a **Saját kiadások: Utazási kérelmek** alatt tekintheti meg.</span><span class="sxs-lookup"><span data-stu-id="4a740-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="4a740-125">Utazási kérelmek jóváhagyása</span><span class="sxs-lookup"><span data-stu-id="4a740-125">Approve travel requisitions</span></span>

<span data-ttu-id="4a740-126">Válassza ki a jóváhagyni kívánt utazási kérelmet, majd jelölje ki a **Munkafolyamat** > **Jóváhagyás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="4a740-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="4a740-127">Költségjelentés elküldése a jóváhagyott utazási kérelem használatával</span><span class="sxs-lookup"><span data-stu-id="4a740-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="4a740-128">Hozzon létre egy új költségjelentést, és a költségjelentés fejlécében és a jóváhagyott utazási kérelmek listájából válassza a **Leképezés utazási kérelemre** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="4a740-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="4a740-129">Az **Utazási kérelem összege** mező automatikusan frissül a költségjelentés fejlécében.</span><span class="sxs-lookup"><span data-stu-id="4a740-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="4a740-130">Vegyen fel minden utazással kapcsolatban felmerült költséget.</span><span class="sxs-lookup"><span data-stu-id="4a740-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="4a740-131">Ha az **Előre engedélyezett** mező engedélyezve van, akkor a program frissíti az adott költségkategóriához tartozó egyeztetett összeget és engedélyezett összeget.</span><span class="sxs-lookup"><span data-stu-id="4a740-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="4a740-132">Ha egy költségjelentést jóváhagyott utazási kérelemhez képez hozzá, a tranzakció összege nem lehet nagyobb, mint az engedélyezett összeg.</span><span class="sxs-lookup"><span data-stu-id="4a740-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 
