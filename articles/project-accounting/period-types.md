---
title: Időszaktípusok
description: Ez a témakör információt nyújt az időszaktípusok beállításáról a bevételbecsléshez.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07cc9cde5fab10accb1fd6efede58926918f614c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013489"
---
# <a name="period-types"></a><span data-ttu-id="994d2-103">Időszaktípusok</span><span class="sxs-lookup"><span data-stu-id="994d2-103">Period types</span></span>

<span data-ttu-id="994d2-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="994d2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="994d2-105">Az időszak típusa határozza meg, hogy milyen gyakran kerüljön sor bevétel becslésére a projekthez.</span><span class="sxs-lookup"><span data-stu-id="994d2-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="994d2-106">Ez a témakör információt nyújt az időszaktípusok beállításáról a bevételbecsléshez.</span><span class="sxs-lookup"><span data-stu-id="994d2-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="994d2-107">Időszaktípusok létrehozása és használata</span><span class="sxs-lookup"><span data-stu-id="994d2-107">Create and work with period types</span></span>
<span data-ttu-id="994d2-108">Az időszaktípusok létrehozásához és használatához hajtsa végre a következő lépéseket:</span><span class="sxs-lookup"><span data-stu-id="994d2-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="994d2-109">A Dynamics 365 Finance környezetében nyissa meg a **Projektvezetés és könyvelés** > **Beállítások** > **Becslések** > **Időszaktípusok** elemet.</span><span class="sxs-lookup"><span data-stu-id="994d2-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="994d2-110">Új időszaktípus létrehozásához válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="994d2-110">Select **New** to create new period type.</span></span> <span data-ttu-id="994d2-111">Adjon meg egy nevet és egy leírást.</span><span class="sxs-lookup"><span data-stu-id="994d2-111">Enter a name and description.</span></span>
3. <span data-ttu-id="994d2-112">Válasszon egy értéket a **Gyakoriság** mezőben:</span><span class="sxs-lookup"><span data-stu-id="994d2-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="994d2-113">Ha **Hetente**, **Kéthetente**, **Félhavonta**, **Havonta**, **Naponta**, **Negyedévente** vagy **Évente** lehetőséget választja rendszer a naptárat használja az időszakok generálásához.</span><span class="sxs-lookup"><span data-stu-id="994d2-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="994d2-114">Ha a **Főkönyvi időszak** lehetőséget választja, akkor a Főkönyv konfigurációjának főkönyvi időszakait fogja használni a rendszer az időszakok generálásához.</span><span class="sxs-lookup"><span data-stu-id="994d2-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="994d2-115">Ha a **Korlátlan** lehetőséget választja , akkor egyéni időszakokat is megadhat.</span><span class="sxs-lookup"><span data-stu-id="994d2-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="994d2-116">Válassza ki az időszak típusú rekordot, majd válassza az **Időszakok generálása** lehetőséget az időszak típushoz tartozó időszakok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="994d2-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="994d2-117">A kiválasztott időszaki gyakoriság alapján lehet, hogy meg kell adni a kezdési dátumot vagy a létrehozni kívánt időszakok számát.</span><span class="sxs-lookup"><span data-stu-id="994d2-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="994d2-118">A létrehozott **Időszakok** véleményezésére szolgáló időszakok kiválasztása.</span><span class="sxs-lookup"><span data-stu-id="994d2-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]