---
title: Költségjelentések közzététele
description: Ez a témakör ismerteti a költségjelentések elküldésének módját.
author: suvaidya
ms.date: 09/09/2020
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
ms.openlocfilehash: acb26ef74c653a70134f13ab3c382f3c80a8ec14
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995219"
---
# <a name="post-expense-reports"></a><span data-ttu-id="75e6d-103">Költségjelentések közzététele</span><span class="sxs-lookup"><span data-stu-id="75e6d-103">Post expense reports</span></span>

<span data-ttu-id="75e6d-104">A költségjelentés jóváhagyása és a főkönyvi naplóba történő átadása után elküldhető.</span><span class="sxs-lookup"><span data-stu-id="75e6d-104">After an expense report has been approved and transferred to the general journal, it can be posted.</span></span> <span data-ttu-id="75e6d-105">A költségjelentés elküldésekor a rendszer azonosítja az áfa visszaigénylésére jogosult kiadásokat.</span><span class="sxs-lookup"><span data-stu-id="75e6d-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="75e6d-106">Az ÁFA-kifizetések ellenőrzésének és visszaigénylésének feladata a költségjelentés ellenőrzéséért felelős alkalmazotthoz van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="75e6d-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="75e6d-107">Ha egy költségjelentés költségeit az alkalmazottat foglalkoztató vállalattól eltérő vállalatnak számítják felé, akkor ellenőriznie kell mind a vállalatot, amelynek a kiadásokkal tartoznak, ás a vállalatot, amely a kiadásokkal tartozik.</span><span class="sxs-lookup"><span data-stu-id="75e6d-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify both the company that those expenses are owed to and the company that they are owed from.</span></span> <span data-ttu-id="75e6d-108">Például a költségjelentést elküldő alkalmazott a DAT vállalatnál dolgozik, de a DIR vállalatnak számított fel egy kiadást.</span><span class="sxs-lookup"><span data-stu-id="75e6d-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="75e6d-109">Ebben az esetben a DAT az a vállalat, amely a költséggel tartozik, és a DIR az a vállalat, amelynek a költséggel tartoznak.</span><span class="sxs-lookup"><span data-stu-id="75e6d-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="75e6d-110">A naplósorok ellenőrzése után a költségsorokat a főkönyvbe könyvelheti.</span><span class="sxs-lookup"><span data-stu-id="75e6d-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="75e6d-111">A költségjelentés elküldéséhez a **Jóváhagyott költségjelentések** oldalon válassza ki a költségjelentést, majd a Művelet panelen válassza a **Küldés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="75e6d-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="75e6d-112">Az összes költségjelentés egyszerre is elküldhető a listából.</span><span class="sxs-lookup"><span data-stu-id="75e6d-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="75e6d-113">Jelölje ki az összes költségjelentést, majd válassza a **Küldés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="75e6d-113">Select all the expense reports, and then select **Post**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]