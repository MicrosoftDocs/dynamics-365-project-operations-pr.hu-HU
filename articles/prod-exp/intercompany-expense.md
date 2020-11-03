---
title: Vállalatközi költségek
description: A szervezet egyik jogi személye által alkalmazott munkavállaló végezhet munkát egy másik, ugyanabban a szervezetben lévő jogi entitásnál. Ebben az esetben a vállalatközi költség funkciót használhatja a munkavállalói kiadások ahhoz a jogi entitáshoz való hozzárendeléséhez, amelynél a munkát végezték.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078243"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="cb6a7-104">Vállalatközi költségek</span><span class="sxs-lookup"><span data-stu-id="cb6a7-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb6a7-105">A szervezet egyik jogi személye által alkalmazott munkavállaló végezhet munkát egy másik, ugyanabban a szervezetben lévő jogi entitásnál.</span><span class="sxs-lookup"><span data-stu-id="cb6a7-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="cb6a7-106">Ebben az esetben a vállalatközi költség funkciót használhatja a munkavállalói kiadások ahhoz a jogi entitáshoz való hozzárendeléséhez, amelynél a munkát végezték.</span><span class="sxs-lookup"><span data-stu-id="cb6a7-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="cb6a7-107">A munkavállalót foglalkoztató jogi személy az úgynevezett kölcsönadó jogi entitás.</span><span class="sxs-lookup"><span data-stu-id="cb6a7-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="cb6a7-108">Az a jogi személy, amelyhez a munkavállaló a költségeket generálja a kölcsönbevevő jogi személy.</span><span class="sxs-lookup"><span data-stu-id="cb6a7-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="cb6a7-109">Mielőtt a dolgozó a másik jogi személy számára végzett munkára vonatkozóan költségeket hozzon létre és nyújtson be, a kölcsönadó jogi személynél a **Költség-kezelési paraméterek** lapon jelölje be a **Vállalatközi kiadási sorok engedélyezése** jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="cb6a7-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="cb6a7-110">Vállalatközi kiadások adójának feladása</span><span class="sxs-lookup"><span data-stu-id="cb6a7-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb6a7-111">Ha a kölcsönadó (forrás) jogi személyhez tartozó adócsoportokat kívánja használni a kölcsönbevevő (cél) jogi személy helyett, akkor ezt a főkönyvben kell beállítania.</span><span class="sxs-lookup"><span data-stu-id="cb6a7-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="cb6a7-112">Ha a **Vállalatközi adófeladás jogi személye** Főkönyvi paraméter beállítás **Forrás** és **Az ÁFA-adózási szabályok alkalmazása** értéke **Nem** a kölcsönadó jogi személyhez tartozó adózási kombinációt használja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="cb6a7-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="cb6a7-113">Ha ugyanazt a paramétert a **Cél** értékre állítja , a rendszer a kölcsönvevő jogi személyhez tartozó adózási kombinációt használja.</span><span class="sxs-lookup"><span data-stu-id="cb6a7-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="cb6a7-114">Az Egyesült államokbeli jogi entitások esetében, ha a paraméter beállítása **Forrás** , a rendszernek az **ÁFA-kinnlévőség** mezőt is be kell állítania az új **Főkönyvi feladási csoportok** lapon.</span><span class="sxs-lookup"><span data-stu-id="cb6a7-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="cb6a7-115">A könyvelési motor az ebből a mezőből származó információkat az adózáshoz kapcsolódó könyvelési bejegyzéshez használja.</span><span class="sxs-lookup"><span data-stu-id="cb6a7-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="cb6a7-116">A viselkedés összhangban van a projekttel vagy anélkül feladott költségelszámolási sorokkal.</span><span class="sxs-lookup"><span data-stu-id="cb6a7-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
