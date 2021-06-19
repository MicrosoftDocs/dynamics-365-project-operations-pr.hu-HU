---
title: Költségbejegyzés (Lite)
description: Ez a témakör a költségbejegyzések Lite telepítésben történő használatának módjával kapcsolatos információkat tartalmaz.
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e75a61c25be06a9db121e8165e8ccd25d4719d08
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002194"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="1d283-103">Költségbejegyzés (Lite)</span><span class="sxs-lookup"><span data-stu-id="1d283-103">Expense entry (lite)</span></span>

<span data-ttu-id="1d283-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="1d283-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1d283-105">Az alapszintű vagy a Lite költségkezelés az egyszerű kiadások rögzítésének képessége.</span><span class="sxs-lookup"><span data-stu-id="1d283-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="1d283-106">A projektek költségeit rögzítheti egy projekthez, majd a projekt jóváhagyója áttekinti és jóváhagyja azokat.</span><span class="sxs-lookup"><span data-stu-id="1d283-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="1d283-107">A Dynamics 365 Project Operations költségképeségeivel kapcsolatos további információk a következő témakörben találhatók: [Költségek áttekintése](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1d283-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="1d283-108">Alapköltség rögzítése</span><span class="sxs-lookup"><span data-stu-id="1d283-108">Capture a basic expense</span></span>

<span data-ttu-id="1d283-109">A költségeket rögzítheti, így elküldheti azokat a jóváhagyónak.</span><span class="sxs-lookup"><span data-stu-id="1d283-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="1d283-110">Lépjen a **Kiadások** pontra, és válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1d283-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="1d283-111">Az **Új kiadás** lapon adja meg a szükséges költséginformációkat, majd kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="1d283-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="1d283-112">Alapköltség elküldése</span><span class="sxs-lookup"><span data-stu-id="1d283-112">Submit a basic expense</span></span>

<span data-ttu-id="1d283-113">Miután befejezte az összes kiadás rögzítését, és készen áll a jóváhagyásra, el kell küldenie azokat.</span><span class="sxs-lookup"><span data-stu-id="1d283-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="1d283-114">Lépjen a **Kiadások** pontra, és válasszon egy kiadást.</span><span class="sxs-lookup"><span data-stu-id="1d283-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="1d283-115">Másik lehetőségként jelölje ki az összes kiadást a fejlécen lévő jelölőnégyzet használatával.</span><span class="sxs-lookup"><span data-stu-id="1d283-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="1d283-116">Válassza a **Küldés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1d283-116">Select **Submit**.</span></span> <span data-ttu-id="1d283-117">A rendszer feldolgozza a kijelölt bejegyzéseket, majd létrehozza a költségjóváhagyási kérelmeket.</span><span class="sxs-lookup"><span data-stu-id="1d283-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="add-an-attachment"></a><span data-ttu-id="1d283-118">Melléklet hozzáadása</span><span class="sxs-lookup"><span data-stu-id="1d283-118">Add an attachment</span></span>

<span data-ttu-id="1d283-119">Előfordulhat, hogy a jóváhagyónak további dokumentációt kell biztosítania az Ön költségére vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="1d283-119">You may have to provide the approver with additional documentation about your expense.</span></span> <span data-ttu-id="1d283-120">A költségbejegyzése idővonalában elismervényt csatolhat.</span><span class="sxs-lookup"><span data-stu-id="1d283-120">You can attach a receipt in the timeline of the expense entry.</span></span> <span data-ttu-id="1d283-121">Válassza a **Szerkesztés** lehetőséget, majd az **Idősor** szakaszban jelölje ki a gemkapocs ikont a nyugta csatolásához.</span><span class="sxs-lookup"><span data-stu-id="1d283-121">Select **Edit** and in the **Timeline** section, and then select the paperclip icon to attach your receipt.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="1d283-122">Alapköltség visszahívása</span><span class="sxs-lookup"><span data-stu-id="1d283-122">Recall a basic expense</span></span>

<span data-ttu-id="1d283-123">Amikor tévedésből küld el egy kiadást, visszahívhatja azt.</span><span class="sxs-lookup"><span data-stu-id="1d283-123">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="1d283-124">A költségbejegyzés visszahívásához szükséges idő a jóváhagyási fázisától függ.</span><span class="sxs-lookup"><span data-stu-id="1d283-124">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="1d283-125">Ha a jóváhagyó még nem hagyta jóvá a bejegyzést, akkor a visszahívás azonnal megtörténhet.</span><span class="sxs-lookup"><span data-stu-id="1d283-125">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="1d283-126">Ha azonban a bejegyzést már jóváhagyták, a jóváhagyónak jóvá kell hagynia a visszahívást, és vissza kell fordítania a tranzakciókat.</span><span class="sxs-lookup"><span data-stu-id="1d283-126">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="1d283-127">Nyissa meg a **Kiadások** pontot, majd a kiadások listájában válassza ki a visszahívni kívánt kiadást.</span><span class="sxs-lookup"><span data-stu-id="1d283-127">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="1d283-128">Válassza az **Előhívás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1d283-128">Select **Recall**.</span></span> <span data-ttu-id="1d283-129">Ha a költségbejegyzést még nem hagyták jóvá, a rendszer azonnal visszahívja.</span><span class="sxs-lookup"><span data-stu-id="1d283-129">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="1d283-130">Ha a költségbejegyzést már jóváhagyták, a rendszer egy visszahívási kérést hoz létre, amely értesíti a jóváhagyót, hogy sztornírozza a kiadást.</span><span class="sxs-lookup"><span data-stu-id="1d283-130">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="1d283-131">A jóváhagyó ezután megerősíti, hogy a sztornírozás megtehető, és a tétel visszakerül a rendszerbe.</span><span class="sxs-lookup"><span data-stu-id="1d283-131">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="1d283-132">Alapköltség törlése</span><span class="sxs-lookup"><span data-stu-id="1d283-132">Delete a basic expense</span></span>

<span data-ttu-id="1d283-133">A még el nem küldött kiadások törölhetők.</span><span class="sxs-lookup"><span data-stu-id="1d283-133">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="1d283-134">Ha már elküldött kiadást szeretne törölni, akkor először vissza kell hívnia.</span><span class="sxs-lookup"><span data-stu-id="1d283-134">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="1d283-135">Kapcsolódó információk</span><span class="sxs-lookup"><span data-stu-id="1d283-135">See also</span></span>

- [<span data-ttu-id="1d283-136">Jóváhagyások áttekintése</span><span class="sxs-lookup"><span data-stu-id="1d283-136">Approvals overview</span></span>](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]