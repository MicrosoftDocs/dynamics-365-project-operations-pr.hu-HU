---
title: Költségházirendek beállítása
description: Meghatározhatók olyan költségszabályzatok, amelyeket a dolgozóknak be kell tartaniuk a költségjelentések és az utazási igénylések megadásakor és elküldésekor a Microsoft Dynamics 365 Finance szolgáltatásban.
author: suvaidya
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa4f628a918e6e099a723ed05994f63d6ad847f5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005749"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="b6b71-103">Költségházirendek beállítása</span><span class="sxs-lookup"><span data-stu-id="b6b71-103">Set up expense policies</span></span>

<span data-ttu-id="b6b71-104">Meghatározhatók olyan szabályzatok, amelyeket a dolgozóknak be kell tartaniuk a költségjelentések és az utazási igénylések megadásakor és elküldésekor.</span><span class="sxs-lookup"><span data-stu-id="b6b71-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="b6b71-105">A költségszabályzatokkal hatékonyan kezelheti a költségeket.</span><span class="sxs-lookup"><span data-stu-id="b6b71-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="b6b71-106">Beállíthat például egy szabályzatot egy New York Cityben lévő szálloda kiadásaihoz, amely előírja, hogy az éjszakánkénti költség nem haladhatja meg a 250 USD-t.</span><span class="sxs-lookup"><span data-stu-id="b6b71-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="b6b71-107">Ha egy dolgozó olyan költségjelentést vagy utazási igénylést nyújt be, ahol a szobaár meghaladja ezt az összeget, a rendszer értesíti a</span><span class="sxs-lookup"><span data-stu-id="b6b71-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="b6b71-108">dolgozót, hogy túllépte a költségre vonatkozó szabályzatban szereplő összeget.</span><span class="sxs-lookup"><span data-stu-id="b6b71-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="b6b71-109">A szabályzat meghatározásakor állíthatja be,</span><span class="sxs-lookup"><span data-stu-id="b6b71-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="b6b71-110">hogy a dolgozó milyen üzenetet kapjon.</span><span class="sxs-lookup"><span data-stu-id="b6b71-110">define the policy.</span></span>      
        
<span data-ttu-id="b6b71-111">Háromféle szabályzat hozható létre:</span><span class="sxs-lookup"><span data-stu-id="b6b71-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="b6b71-112">Figyelmeztetés: A dolgozó beküldheti a költségjelentést vagy az utazási igénylést, de a rendszer minden jóváhagyó számára megjelöli a költséget</span><span class="sxs-lookup"><span data-stu-id="b6b71-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="b6b71-113">a későbbi jelentéskészítéshez.</span><span class="sxs-lookup"><span data-stu-id="b6b71-113">for later reporting.</span></span>        

- <span data-ttu-id="b6b71-114">Hiba: A dolgozónak a költségjelentés vagy az utazási igénylés elküldése előtt úgy kell módosítania a költséget, hogy megfeleljen a szabályzatnak.</span><span class="sxs-lookup"><span data-stu-id="b6b71-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="b6b71-115">Indoklás: A dolgozónak vagy a vezetőnek a költségjelentés vagy az utazási igénylés elküldése előtt indokolnia kell, hogy miért lépte túl a szabályzatban szereplő összeget.</span><span class="sxs-lookup"><span data-stu-id="b6b71-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="b6b71-116">Szabályzatra vonatkozó tippek</span><span class="sxs-lookup"><span data-stu-id="b6b71-116">Policy tips</span></span>
<span data-ttu-id="b6b71-117">Az alábbiakban néhány olyan javaslatot talál, amely segíthet a költségkezelés új szabályzatainak létrehozásában.</span><span class="sxs-lookup"><span data-stu-id="b6b71-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="b6b71-118">A szabályzatok az adott napon lépnek hatályba, és a költség dátuma után létrehozott szabályzat nem érvényes az adott költségek esetén.</span><span class="sxs-lookup"><span data-stu-id="b6b71-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="b6b71-119">Ha például egy új házirendet hoz létre ma, hogy kikényszerítse a $50 maximális étkezési költséget, akkor a tegnap bevitt összes költséget nem kell ellenőrizni ezzel a házirenddel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="b6b71-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="b6b71-120">Ha tételezhető költségkategóriára vonatkozó szabályzatot hoz létre, érdemes lehet feltételt hozzáadni a költségsor típusához.</span><span class="sxs-lookup"><span data-stu-id="b6b71-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="b6b71-121">Előfordulhat, hogy bizonyos szabályzatok, például a kötelező nyugta, nem feltétlenül hasznos a részletezett sorokhoz, és csak a fejlécsorra vagy egy nem részletezett sorra alkalmazhatók.</span><span class="sxs-lookup"><span data-stu-id="b6b71-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="b6b71-122">A költségkezelési szabályzatokat a rendszer alapértelmezés szerint a forrásentitáshoz képest értékeli ki.</span><span class="sxs-lookup"><span data-stu-id="b6b71-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="b6b71-123">Vállalatközi forgatókönyvek esetén beállíthatja, hogy a szabályzatot a célentitáshoz (átvevő entitás) képest értékelje a rendszer.</span><span class="sxs-lookup"><span data-stu-id="b6b71-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="b6b71-124">Ha a célentitáshoz szeretne szabályzatokat futtatni, kapcsolja be a „Költségszabályzat értékelése az átvevő jogi személyhez képest” szolgáltatást a **Funkciókezelés** munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="b6b71-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="b6b71-125">Mikor kell értékelni a szabályzatokat?</span><span class="sxs-lookup"><span data-stu-id="b6b71-125">When to evaluate policies</span></span>

<span data-ttu-id="b6b71-126">A költségkezelési paraméterek között kiválaszthatja, hogy a program csak egy sor mentésekor vagy a költségjelentés elküldésekor értékelje ki a költségkezelési szabályzatokat.</span><span class="sxs-lookup"><span data-stu-id="b6b71-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="b6b71-127">Ha a sorok mentésekor történő kiértékelést választja, akkor ez biztosítja, hogy a felhasználók korábban minden olyan részletet láthatnak, amit tenniük kell a költségjelentés végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="b6b71-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="b6b71-128">Ellenkező esetben késleltetheti a szabályzat kiértékelését, és időt takaríthat meg, ha a befejezést követően, a beküldéskor kerül sor a munkafolyamat ellenőrzésére.</span><span class="sxs-lookup"><span data-stu-id="b6b71-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]