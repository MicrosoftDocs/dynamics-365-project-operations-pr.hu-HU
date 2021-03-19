---
title: Vállalatközi költségek
description: Ez témakör tájékoztatást nyújt arról, hogyan lehet a vállalatközi kiadások használatával a dolgozók kiadásait ahhoz a jogi entitáshoz hozzárendelni, amelynél a munkát végrehajtották.
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
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271536"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="676b5-103">Vállalatközi költségek</span><span class="sxs-lookup"><span data-stu-id="676b5-103">Intercompany expenses</span></span>

<span data-ttu-id="676b5-104">A szervezet egyik jogi személye által alkalmazott munkavállaló végezhet munkát egy másik, ugyanabban a szervezetben lévő jogi entitásnál.</span><span class="sxs-lookup"><span data-stu-id="676b5-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="676b5-105">A vállalatközi kiadások használatával a dolgozók kiadásait ahhoz a jogi entitáshoz tudja hozzárendelni, amelynél a munkát végrehajtották.</span><span class="sxs-lookup"><span data-stu-id="676b5-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="676b5-106">A munkavállalót foglalkoztató jogi személy az úgynevezett kölcsönadó jogi entitás.</span><span class="sxs-lookup"><span data-stu-id="676b5-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="676b5-107">Az a jogi személy, amelyhez a munkavállaló a költségeket generálja a kölcsönbevevő jogi személy.</span><span class="sxs-lookup"><span data-stu-id="676b5-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="676b5-108">Ahhoz, hogy egy dolgozó létrehozza és elküldje a vállalatközi költségeket, engedélyeznie kell a vállalatközi költségsorokat.</span><span class="sxs-lookup"><span data-stu-id="676b5-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="676b5-109">A kölcsönadó jogi entitás **Költségkezelési paraméterek** lapján válassza a **Vállalatközi költségsorok engedélyezése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="676b5-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="676b5-110">Vállalatközi kiadások adójának feladása</span><span class="sxs-lookup"><span data-stu-id="676b5-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="676b5-111">Ahhoz, hogy a költségjelentésben a kölcsönkérő (cél) jogi entitás helyett a kölcsönadóhoz (forrás) tartozó adócsoportokat használjon, engedélyeznie kell a funkciót a Főkönyvi áfa beállításban.</span><span class="sxs-lookup"><span data-stu-id="676b5-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="676b5-112">Ha a **Vállalatközi jogi entitás adójának feladása** paraméter **Forrás** lehetőségre van állítva, és az **Áfa adózási szabályok alkalmazása** beállítás **Nem** értékre van állítva, a kölcsönadó entitás adókombinációját használja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="676b5-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="676b5-113">Ha ugyanazt a paramétert a **Cél** értékre állítja , a rendszer a kölcsönvevő jogi személyhez tartozó adózási kombinációt használja.</span><span class="sxs-lookup"><span data-stu-id="676b5-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="676b5-114">Az Egyesült államokbeli jogi entitások esetében, ha a paraméter beállítása **Forrás**, a rendszernek az **ÁFA-kinnlévőség** mezőt is be kell állítania az új **Főkönyvi feladási csoportok** lapon.</span><span class="sxs-lookup"><span data-stu-id="676b5-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="676b5-115">A könyvelési motor az ebből a mezőből származó információkat az adózáshoz kapcsolódó könyvelési bejegyzéshez használja.</span><span class="sxs-lookup"><span data-stu-id="676b5-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="676b5-116">A viselkedés összhangban van a projekttel vagy anélkül feladott költségelszámolási sorokkal.</span><span class="sxs-lookup"><span data-stu-id="676b5-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]