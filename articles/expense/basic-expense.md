---
title: Költségbejegyzés (Lite)
description: Ez a témakör a költségbejegyzések Lite telepítésben történő használatának módjával kapcsolatos információkat tartalmaz.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4077976"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="0af36-103">Költségbejegyzés (Lite)</span><span class="sxs-lookup"><span data-stu-id="0af36-103">Expense entry (lite)</span></span>

<span data-ttu-id="0af36-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="0af36-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0af36-105">Az alapszintű vagy a Lite költségkezelés az egyszerű kiadások rögzítésének képessége.</span><span class="sxs-lookup"><span data-stu-id="0af36-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="0af36-106">A projektek költségeit rögzítheti egy projekthez, majd a projekt jóváhagyója áttekinti és jóváhagyja azokat.</span><span class="sxs-lookup"><span data-stu-id="0af36-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="0af36-107">A Dynamics 365 Project Operations költségre vonatkozó képességeivel kapcsolatos további információkért lásd: [Költség áttekintése](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0af36-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="0af36-108">Alapköltség rögzítése</span><span class="sxs-lookup"><span data-stu-id="0af36-108">Capture a basic expense</span></span>

<span data-ttu-id="0af36-109">A költségeket rögzítheti, így elküldheti azokat a jóváhagyónak.</span><span class="sxs-lookup"><span data-stu-id="0af36-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="0af36-110">Lépjen a **Kiadások** pontra, és válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="0af36-110">Go to **Expenses** , and select **New**.</span></span>
2. <span data-ttu-id="0af36-111">Az **Új kiadás** lapon adja meg a szükséges költséginformációkat, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="0af36-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="0af36-112">Alapköltség elküldése</span><span class="sxs-lookup"><span data-stu-id="0af36-112">Submit a basic expense</span></span>

<span data-ttu-id="0af36-113">Miután befejezte az összes kiadás rögzítését, és készen áll a jóváhagyásra, el kell küldenie azokat.</span><span class="sxs-lookup"><span data-stu-id="0af36-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="0af36-114">Lépjen a **Kiadások** pontra, és válasszon egy kiadást.</span><span class="sxs-lookup"><span data-stu-id="0af36-114">Go to **Expenses** , and select an expense.</span></span> <span data-ttu-id="0af36-115">Másik lehetőségként jelölje ki az összes kiadást a fejlécen lévő jelölőnégyzet használatával.</span><span class="sxs-lookup"><span data-stu-id="0af36-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="0af36-116">Válassza a **Küldés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="0af36-116">Select **Submit**.</span></span> <span data-ttu-id="0af36-117">A rendszer feldolgozza a kijelölt bejegyzéseket, majd létrehozza a költségjóváhagyási kérelmeket.</span><span class="sxs-lookup"><span data-stu-id="0af36-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="0af36-118">Alapköltség visszahívása</span><span class="sxs-lookup"><span data-stu-id="0af36-118">Recall a basic expense</span></span>

<span data-ttu-id="0af36-119">Amikor tévedésből küld el egy kiadást, visszahívhatja azt.</span><span class="sxs-lookup"><span data-stu-id="0af36-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="0af36-120">A költségbejegyzés visszahívásához szükséges idő a jóváhagyási fázisától függ.</span><span class="sxs-lookup"><span data-stu-id="0af36-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="0af36-121">Ha a jóváhagyó még nem hagyta jóvá a bejegyzést, akkor a visszahívás azonnal megtörténhet.</span><span class="sxs-lookup"><span data-stu-id="0af36-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="0af36-122">Ha azonban a bejegyzést már jóváhagyták, a jóváhagyónak jóvá kell hagynia a visszahívást, és vissza kell fordítania a tranzakciókat.</span><span class="sxs-lookup"><span data-stu-id="0af36-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="0af36-123">Nyissa meg a **Kiadások** pontot, majd a kiadások listájában válassza ki a visszahívni kívánt kiadást.</span><span class="sxs-lookup"><span data-stu-id="0af36-123">Go to **Expenses** , and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="0af36-124">Válassza az **Előhívás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="0af36-124">Select **Recall**.</span></span> <span data-ttu-id="0af36-125">Ha a költségbejegyzést még nem hagyták jóvá, a rendszer azonnal visszahívja.</span><span class="sxs-lookup"><span data-stu-id="0af36-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="0af36-126">Ha a költségbejegyzést már jóváhagyták, a rendszer egy visszahívási kérést hoz létre, amely értesíti a jóváhagyót, hogy sztornírozza a kiadást.</span><span class="sxs-lookup"><span data-stu-id="0af36-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="0af36-127">A jóváhagyó ezután megerősíti, hogy a sztornírozás megtehető, és a tétel visszakerül a rendszerbe.</span><span class="sxs-lookup"><span data-stu-id="0af36-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="0af36-128">Alapköltség törlése</span><span class="sxs-lookup"><span data-stu-id="0af36-128">Delete a basic expense</span></span>

<span data-ttu-id="0af36-129">A még el nem küldött kiadások törölhetők.</span><span class="sxs-lookup"><span data-stu-id="0af36-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="0af36-130">Ha már elküldött kiadást szeretne törölni, akkor először vissza kell hívnia.</span><span class="sxs-lookup"><span data-stu-id="0af36-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="0af36-131">Kapcsolódó információk</span><span class="sxs-lookup"><span data-stu-id="0af36-131">See also</span></span>

- [<span data-ttu-id="0af36-132">Jóváhagyások áttekintése</span><span class="sxs-lookup"><span data-stu-id="0af36-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
