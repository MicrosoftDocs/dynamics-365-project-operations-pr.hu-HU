---
title: Munkavégzés személyes kiadásokkal egy költségjelentésen
description: A témakör tájékoztatást nyújt arról, hogyan kell használni az üzleti céllal utazó alkalmazottak személyes kiadásait.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025687"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="3208a-103">Munkavégzés személyes kiadásokkal egy költségjelentésen</span><span class="sxs-lookup"><span data-stu-id="3208a-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="3208a-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="3208a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3208a-105">Üzleti út közben az alkalmazottak személyes költségeket számolhatnak fel a vállalati hitelkártyájuknak.</span><span class="sxs-lookup"><span data-stu-id="3208a-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="3208a-106">Ha még nincs megadva folyamat a személyes kiadások kezeléséhez, a költségjelentés jóváhagyási folyamata megszakadhat, amikor egy alkalmazott elküldi a tételes költségjelentését.</span><span class="sxs-lookup"><span data-stu-id="3208a-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="3208a-107">Az alkalmazottak személyes kiadásait kétféleképpen kezelheti:</span><span class="sxs-lookup"><span data-stu-id="3208a-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="3208a-108">**Alkalmazott által fizetendő**: A szervezet nem fizeti ki a személyes költségeket, amelyek megjelennek a vállalati hitelkártya számláján.</span><span class="sxs-lookup"><span data-stu-id="3208a-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="3208a-109">Ehelyett az alkalmazott közvetlenül a hitelkártya szállítójának fizeti a költségeket.</span><span class="sxs-lookup"><span data-stu-id="3208a-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="3208a-110">**Vállalat által fizetendő**: A vállalat fizeti a vállalati hitelkártya teljes költségét, majd a személyes kiadások összegével megterheli a dolgozó fiókját.</span><span class="sxs-lookup"><span data-stu-id="3208a-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="3208a-111">Megadhatja, hogy a szervezet milyen módszert használ a **költségkezelési paraméterek** lapon.</span><span class="sxs-lookup"><span data-stu-id="3208a-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="3208a-112">Költség felsosztása engedélyezése, ha a személyes összeg mező értéke meg van adva</span><span class="sxs-lookup"><span data-stu-id="3208a-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="3208a-113">A **Költség felosztásának engedélyezése, ha a személyes összeg mező értéke meg van adva** csak azon költségjelentésekre vonatkozik, amelyek sorszintű munkafolyamattal vannak jóváhagyva.</span><span class="sxs-lookup"><span data-stu-id="3208a-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="3208a-114">A jelentések jóváhagyása a **Költségjelentések feldolgozása** > **Hozzám rendelt költségjelentések** > **Költségjelentések megnyitása** helyen lehetséges.</span><span class="sxs-lookup"><span data-stu-id="3208a-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="3208a-115">A funkció engedélyezéséhez válassza a **Munkaterületek** > **Funkciókezelés** lehetőséget, válassza a **Költségek felosztásának engedélyezése, ha a személyes összeg mező értéke meg van adva** lehetőséget, majd válassza az **Engedélyezés most** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="3208a-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="3208a-116">Ha a szolgáltatás engedélyezve van, akkor a szolgáltatást használó költségsorok a jelentés elküldésekor két sort generálnak.</span><span class="sxs-lookup"><span data-stu-id="3208a-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="3208a-117">Két sor jön létre, így a jóváhagyó külön-külön jóváhagyhatja a sorokat.</span><span class="sxs-lookup"><span data-stu-id="3208a-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
