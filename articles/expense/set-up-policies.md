---
title: Költségszabályzatok definiálása
description: Meghatározhatók olyan költségszabályzatok, amelyeket a dolgozóknak be kell tartaniuk a költségjelentések és az utazási igénylések megadásakor és elküldésekor.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fa108db9aa0d2a22c35d2d046917ddae1f3842c1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001879"
---
# <a name="define-expense-policies"></a><span data-ttu-id="0ae6a-103">Költségszabályzatok definiálása</span><span class="sxs-lookup"><span data-stu-id="0ae6a-103">Define expense policies</span></span>

<span data-ttu-id="0ae6a-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="0ae6a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0ae6a-105">Meghatározhatók olyan szabályzatok, amelyeket a dolgozóknak be kell tartaniuk a költségjelentések és az utazási igénylések megadásakor és elküldésekor.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="0ae6a-106">A költségszabályzatokkal hatékonyan kezelheti a költségeket.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="0ae6a-107">Beállíthat például egy szabályzatot egy New York Cityben lévő szálloda kiadásaihoz, amely előírja, hogy az éjszakánkénti költség nem haladhatja meg a 250 USD-t.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="0ae6a-108">Ha egy dolgozó olyan költségjelentést vagy utazási igénylést nyújt be, ahol a szobaár meghaladja ezt az összeget, a rendszer értesíti a</span><span class="sxs-lookup"><span data-stu-id="0ae6a-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="0ae6a-109">dolgozót, hogy túllépte a költségre vonatkozó szabályzatban szereplő összeget.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="0ae6a-110">A szabályzat meghatározásakor állíthatja be,</span><span class="sxs-lookup"><span data-stu-id="0ae6a-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="0ae6a-111">hogy a dolgozó milyen üzenetet kapjon.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-111">define the policy.</span></span>      
        
<span data-ttu-id="0ae6a-112">Háromféle szabályzat hozható létre:</span><span class="sxs-lookup"><span data-stu-id="0ae6a-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="0ae6a-113">**Figyelmeztetés**: A dolgozó beküldheti a költségjelentést vagy az utazási igénylést, de a rendszer minden jóváhagyó számára megjelöli a költséget</span><span class="sxs-lookup"><span data-stu-id="0ae6a-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="0ae6a-114">a későbbi jelentéskészítéshez.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-114">for later reporting.</span></span>        

- <span data-ttu-id="0ae6a-115">**Hiba**: A dolgozónak a költségjelentés vagy az utazási igénylés elküldése előtt úgy kell módosítania a költséget, hogy megfeleljen a szabályzatnak.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="0ae6a-116">**Indoklás**: A dolgozónak vagy a vezetőnek a költségjelentés vagy az utazási igénylés elküldése előtt indokolnia kell, hogy miért lépte túl a szabályzatban szereplő összeget.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="0ae6a-117">Szabályzatra vonatkozó tippek</span><span class="sxs-lookup"><span data-stu-id="0ae6a-117">Policy tips</span></span>
<span data-ttu-id="0ae6a-118">Az alábbiakban néhány olyan javaslatot talál, amely segíthet a költségkezelés új szabályzatainak létrehozásában:</span><span class="sxs-lookup"><span data-stu-id="0ae6a-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="0ae6a-119">A szabályzatok az adott napon lépnek hatályba. Ez azt jelenti, hogy a költség dátuma után létrehozott szabályzat nem érvényes az adott költségek esetén.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="0ae6a-120">Olyan szabályzatot léptet például érvénybe, amely 50 USD értékben határozza meg a legmagasabb étkezési költséget.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="0ae6a-121">Az előző napon bevitt költségeket a szabályzat nem ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="0ae6a-122">Ha tételezhető költségkategóriára vonatkozó szabályzatot hoz létre, érdemes lehet feltételt hozzáadni a költségsor típusához.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="0ae6a-123">Bizonyos szabályzatok – például a nyugták köteleővé tétele – nem feltétlenül hasznosak tételezett sorok esetén.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="0ae6a-124">Ebben az esetben a szabályzatot csak a fejlécsorra vagy a nem tételezett sorokra alkalmazza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="0ae6a-125">A költségkezelési szabályzatokat a rendszer alapértelmezés szerint a forrásentitáshoz képest értékeli ki.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="0ae6a-126">Vállalatközi forgatókönyvek esetén beállíthatja, hogy a szabályzatot a célentitáshoz (átvevő entitás) képest értékelje a rendszer.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="0ae6a-127">Ha a célentitáshoz szeretne szabályzatokat futtatni, kapcsolja be a **Költségszabályzat értékelése az átvevő jogi személyhez képest** szolgáltatást a **Szolgáltatáskezelés** munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="0ae6a-128">Mikor kell értékelni a szabályzatokat?</span><span class="sxs-lookup"><span data-stu-id="0ae6a-128">When to evaluate policies</span></span>

<span data-ttu-id="0ae6a-129">A költségkezelési paraméterek között kiválaszthatja, hogy a program csak egy sor mentésekor vagy a költségjelentés elküldésekor értékelje ki a költségkezelési szabályzatokat.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="0ae6a-130">Ha a sorok mentésekor történő kiértékelést választja, akkor a felhasználók korábban minden olyan részletet láthatnak, amit tenniük kell a költségjelentés végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="0ae6a-131">Ellenkező esetben késleltetheti a szabályzat kiértékelését, és időt takaríthat meg, ha a befejezést követően, a beküldéskor ellenőrzi a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="0ae6a-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]