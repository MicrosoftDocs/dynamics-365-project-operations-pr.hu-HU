---
title: Költségkezelési munkafolyamatok beállítása
description: Beállíthat munkafolyamatot az utazásokkal és a költségekkel kapcsolatos dokumentumok ellenőrzésére és jóváhagyására.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0af23ed2cf172e4c90de72f5db389c349303c039
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078246"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="237e9-103">Költségkezelési munkafolyamatok beállítása</span><span class="sxs-lookup"><span data-stu-id="237e9-103">Set up Expense management workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="237e9-104">Beállíthat olyan munkafolyamatot, amely az utazásokkal és a költségekkel kapcsolatos dokumentumok ellenőrzésére és jóváhagyására szolgál.</span><span class="sxs-lookup"><span data-stu-id="237e9-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="237e9-105">A dokumentumok, amelyekhez definiálhatók munkafolyamatok a költségjelentések, az utazási igénylések és a készpénzelőleg igénylések.</span><span class="sxs-lookup"><span data-stu-id="237e9-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="237e9-106">A munkafolyamatok egy üzleti folyamatnak felelnek meg.</span><span class="sxs-lookup"><span data-stu-id="237e9-106">A workflow represents a business process.</span></span> <span data-ttu-id="237e9-107">Meghatározza, hogyan halad a dokumentum a rendszeren keresztül, és jelzi, hogy kinek kell elvégeznie a feladatot, vagy jóváhagynia a dokumentumot.</span><span class="sxs-lookup"><span data-stu-id="237e9-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="237e9-108">A munkafolyamatok használata több okból is hasznos a szervezetek számára:</span><span class="sxs-lookup"><span data-stu-id="237e9-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="237e9-109">**Egységes eljárások** – Meghatározható bizonyos dokumentumok (például a beszerzési igénylések vagy a költségelszámolások) jóváhagyási folyamata.</span><span class="sxs-lookup"><span data-stu-id="237e9-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="237e9-110">A munkafolyamatokkal biztosítható, hogy a dokumentumok feldolgozása és jóváhagyása egységes és hatékony legyen.</span><span class="sxs-lookup"><span data-stu-id="237e9-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="237e9-111">Folyamat láthatósága – Nyomon követheti egy adott munkafolyamat-példány állapotát, előzményeit és teljesítménymutatóit.</span><span class="sxs-lookup"><span data-stu-id="237e9-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="237e9-112">Így meghatározhatja, hogy szükség van-e a munkafolyamat hatékonyabbá tételére.</span><span class="sxs-lookup"><span data-stu-id="237e9-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="237e9-113">Központosított munkavégzési lista – A felhasználók megtekinthetik a központosított munkavégzési listákat, és láthatják a hozzájuk rendelt munkafolyamat-feladatokat és jóváhagyásokat.</span><span class="sxs-lookup"><span data-stu-id="237e9-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="237e9-114">**A létrehozható munkafolyamatok**</span><span class="sxs-lookup"><span data-stu-id="237e9-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="237e9-115">Az alábbi táblázat a **Költség** részen létrehozható munkafolyamatok típusait ismerteti.</span><span class="sxs-lookup"><span data-stu-id="237e9-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="237e9-116"><strong>Típus</strong></span><span class="sxs-lookup"><span data-stu-id="237e9-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="237e9-117"><strong>A típus használata</strong></span><span class="sxs-lookup"><span data-stu-id="237e9-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="237e9-118"><strong>Költségjelentés</strong></span><span class="sxs-lookup"><span data-stu-id="237e9-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="237e9-119">Jóváhagyási munkafolyamatok létrehozása költségjelentésekhez.</span><span class="sxs-lookup"><span data-stu-id="237e9-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="237e9-120"><strong>Költségjelentés automatikus közzététele</strong></span><span class="sxs-lookup"><span data-stu-id="237e9-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="237e9-121">Automatikus közzétételi munkafolyamatok létrehozása költségjelentésekhez.</span><span class="sxs-lookup"><span data-stu-id="237e9-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="237e9-122"><strong>Költségsorelem</strong></span><span class="sxs-lookup"><span data-stu-id="237e9-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="237e9-123">Jóváhagyási munkafolyamatok létrehozása a költségjelentések sorelemeihez.</span><span class="sxs-lookup"><span data-stu-id="237e9-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="237e9-124"><strong>Költségsorelem automatikus közzététele</strong></span><span class="sxs-lookup"><span data-stu-id="237e9-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="237e9-125">Automatikus közzétételi munkafolyamatok létrehozása a költségjelentések sorelemeihez.</span><span class="sxs-lookup"><span data-stu-id="237e9-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="237e9-126"><strong>Utazási kérelem</strong></span><span class="sxs-lookup"><span data-stu-id="237e9-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="237e9-127">Jóváhagyási munkafolyamatok létrehozása utazási kérelmekhez.</span><span class="sxs-lookup"><span data-stu-id="237e9-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="237e9-128"><strong>Készpénzelőleg kérése</strong></span><span class="sxs-lookup"><span data-stu-id="237e9-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="237e9-129">Jóváhagyási munkafolyamatok létrehozása készpénzelőleg kéréséhez.</span><span class="sxs-lookup"><span data-stu-id="237e9-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="237e9-130"><strong>ÁFA-visszaigénylés</strong></span><span class="sxs-lookup"><span data-stu-id="237e9-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="237e9-131">Jóváhagyási munkafolyamatok létrehozása ÁFA visszaigényléséhez.</span><span class="sxs-lookup"><span data-stu-id="237e9-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

