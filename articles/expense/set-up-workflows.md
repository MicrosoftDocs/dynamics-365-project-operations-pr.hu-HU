---
title: Munkafolyamatok beállítása költségkezeléshez
description: Beállíthat olyan munkafolyamatot, amely az utazásokkal és a költségekkel kapcsolatos dokumentumok ellenőrzésére és jóváhagyására szolgál.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896554"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="cf505-103">Munkafolyamatok beállítása költségkezeléshez</span><span class="sxs-lookup"><span data-stu-id="cf505-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="cf505-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="cf505-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cf505-105">Beállíthat munkafolyamatot az utazásokkal és a költségekkel kapcsolatos dokumentumok ellenőrzésére és jóváhagyására.</span><span class="sxs-lookup"><span data-stu-id="cf505-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="cf505-106">Megadhat munkafolyamatokat a költségjelentések, az utazási igénylések és a készpénzelőleg igénylései számára.</span><span class="sxs-lookup"><span data-stu-id="cf505-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="cf505-107">A munkafolyamat olyan üzleti folyamat, amely meghatározza, hogy egy dokumentum hogy halad át a rendszeren.</span><span class="sxs-lookup"><span data-stu-id="cf505-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="cf505-108">A munkafolyamat azt is jelzi, hogy kinek kell elvégeznie egy feladatot, vagy jóváhagynia egy dokumentumot.</span><span class="sxs-lookup"><span data-stu-id="cf505-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="cf505-109">A munkafolyamatok használata több okból is hasznos a szervezetek számára:</span><span class="sxs-lookup"><span data-stu-id="cf505-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="cf505-110">**Egységes eljárások**: Meghatározható bizonyos dokumentumok (például a beszerzési igénylések vagy a költségelszámolások) jóváhagyási folyamata.</span><span class="sxs-lookup"><span data-stu-id="cf505-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="cf505-111">A munkafolyamatokkal biztosítható, hogy a dokumentumok feldolgozása és jóváhagyása egységes és hatékony legyen.</span><span class="sxs-lookup"><span data-stu-id="cf505-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="cf505-112">**Folyamat láthatósága**: Nyomon követheti egy adott munkafolyamat-példány állapotát, előzményeit és teljesítménymutatóit.</span><span class="sxs-lookup"><span data-stu-id="cf505-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="cf505-113">Így meghatározhatja, hogy szükség van-e a munkafolyamat hatékonyabbá tételére.</span><span class="sxs-lookup"><span data-stu-id="cf505-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="cf505-114">**Központosított munkavégzési lista**: A felhasználók megtekinthetik a központosított munkavégzési listákat, és láthatják a hozzájuk rendelt munkafolyamat-feladatokat és jóváhagyásokat.</span><span class="sxs-lookup"><span data-stu-id="cf505-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="cf505-115">Munkafolyamatok típusai</span><span class="sxs-lookup"><span data-stu-id="cf505-115">Workflow types</span></span>

<span data-ttu-id="cf505-116">Az alábbi táblázat a **Költségkezelés** részen létrehozható munkafolyamatok típusait ismerteti.</span><span class="sxs-lookup"><span data-stu-id="cf505-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="cf505-117"><strong>Típus</strong></span><span class="sxs-lookup"><span data-stu-id="cf505-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="cf505-118"><strong>A típus használata</strong></span><span class="sxs-lookup"><span data-stu-id="cf505-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="cf505-119"><strong>Költségjelentés automatikus jóváhagyása</strong></span><span class="sxs-lookup"><span data-stu-id="cf505-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="cf505-120">Jóváhagyási munkafolyamatok létrehozása költségjelentésekhez.</span><span class="sxs-lookup"><span data-stu-id="cf505-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="cf505-121"><strong>Költségjelentés automatikus közzététele</strong></span><span class="sxs-lookup"><span data-stu-id="cf505-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="cf505-122">Automatikus közzétételi munkafolyamatok létrehozása költségjelentésekhez.</span><span class="sxs-lookup"><span data-stu-id="cf505-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="cf505-123"><strong>Költségsorelem</strong></span><span class="sxs-lookup"><span data-stu-id="cf505-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="cf505-124">Jóváhagyási munkafolyamatok létrehozása a költségjelentések sorelemeihez.</span><span class="sxs-lookup"><span data-stu-id="cf505-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="cf505-125"><strong>Költségsorelem automatikus közzététele</strong></span><span class="sxs-lookup"><span data-stu-id="cf505-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="cf505-126">Automatikus közzétételi munkafolyamatok létrehozása a költségjelentések sorelemeihez.</span><span class="sxs-lookup"><span data-stu-id="cf505-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="cf505-127"><strong>Utazási kérelem</strong></span><span class="sxs-lookup"><span data-stu-id="cf505-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="cf505-128">Jóváhagyási munkafolyamatok létrehozása utazási kérelmekhez.</span><span class="sxs-lookup"><span data-stu-id="cf505-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="cf505-129"><strong>Készpénzelőleg kérése</strong></span><span class="sxs-lookup"><span data-stu-id="cf505-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="cf505-130">Jóváhagyási munkafolyamatok létrehozása készpénzelőleg kéréséhez.</span><span class="sxs-lookup"><span data-stu-id="cf505-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="cf505-131"><strong>ÁFA-visszaigénylés</strong></span><span class="sxs-lookup"><span data-stu-id="cf505-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="cf505-132">Jóváhagyási munkafolyamatok létrehozása ÁFA visszaigényléséhez.</span><span class="sxs-lookup"><span data-stu-id="cf505-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
