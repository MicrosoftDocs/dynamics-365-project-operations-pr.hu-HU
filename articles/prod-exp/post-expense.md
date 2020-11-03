---
title: Költségjelentés közzététele
description: Ez a témakör ismerteti, hogyan lehet költségjelentést könyvelni a főkönyvbe.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d008ef8dd55550431fbb9e329cd7d9428a08831
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078238"
---
# <a name="post-an-expense-report"></a><span data-ttu-id="19bcf-103">Költségjelentés közzététele</span><span class="sxs-lookup"><span data-stu-id="19bcf-103">Post an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19bcf-104">A költségjelentés jóváhagyása és a főkönyvi naplóba történő átadása után elküldhető a főkönyvbe.</span><span class="sxs-lookup"><span data-stu-id="19bcf-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="19bcf-105">A költségjelentés elküldésekor a rendszer azonosítja az áfa visszaigénylésére jogosult kiadásokat.</span><span class="sxs-lookup"><span data-stu-id="19bcf-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="19bcf-106">Az ÁFA-kifizetések ellenőrzésének és visszaigénylésének feladata a költségjelentés ellenőrzéséért felelős alkalmazotthoz van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="19bcf-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="19bcf-107">Ha egy költségjelentés költségeit az alkalmazottat foglalkoztató vállalattól eltérő vállalatnak számítják felé, akkor ellenőriznie kell mind a vállalatot, amelynek a kiadásokkal tartoznak, és a vállalatot, amely a kiadásokkal tartozik.</span><span class="sxs-lookup"><span data-stu-id="19bcf-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="19bcf-108">Például a költségjelentést elküldő alkalmazott a DAT vállalatnál dolgozik, de a DIR vállalatnak számított fel egy kiadást.</span><span class="sxs-lookup"><span data-stu-id="19bcf-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="19bcf-109">Ebben az esetben a DAT az a vállalat, amely a költséggel tartozik, és a DIR az a vállalat, amelynek a költséggel tartoznak.</span><span class="sxs-lookup"><span data-stu-id="19bcf-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="19bcf-110">A naplósorok ellenőrzése után a költségsorokat a főkönyvbe könyvelheti.</span><span class="sxs-lookup"><span data-stu-id="19bcf-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="19bcf-111">A költségjelentés elküldéséhez a **Jóváhagyott költségjelentések** oldalon válassza ki a költségjelentést, majd a Művelet panelen válassza a **Küldés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="19bcf-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="19bcf-112">Az összes költségjelentés egyszerre is elküldhető a listából.</span><span class="sxs-lookup"><span data-stu-id="19bcf-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="19bcf-113">Jelölje ki az összes költségjelentést, majd válassza a **Küldés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="19bcf-113">Select all the expense reports, and then select **Post**.</span></span>
