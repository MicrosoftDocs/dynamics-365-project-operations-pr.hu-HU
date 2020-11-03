---
title: Napidíjak
description: Ez a témakör a költségkezelésben használt napidíjszabályokról nyújt tájékoztatást.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4077966"
---
# <a name="per-diems"></a><span data-ttu-id="c292c-103">Napidíjak</span><span class="sxs-lookup"><span data-stu-id="c292c-103">Per diems</span></span>

<span data-ttu-id="c292c-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="c292c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="c292c-105">A napidíj olyan juttatás, amelyet a munka céljából utazó munkavállalónak fizetnek.</span><span class="sxs-lookup"><span data-stu-id="c292c-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="c292c-106">A Költségkezelésben létrehoz napidíjszabályokat különböző utazási helyzetekhez.</span><span class="sxs-lookup"><span data-stu-id="c292c-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="c292c-107">A napidíj az évszaktól, az utazás helyétől vagy mindkettőtől függhet.</span><span class="sxs-lookup"><span data-stu-id="c292c-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="c292c-108">Amikor napidíjat hoz létre, megadhatja, hogy a napidíj bizonyos százalékát visszatartsák, ha egy dolgozó ingyenes étkezést vagy szolgáltatásokat kap.</span><span class="sxs-lookup"><span data-stu-id="c292c-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="c292c-109">Beállíthatja azt a minimális és maximális óraszámot is, amelyre a napidíj a dolgozó utazása esetében vonatkozhat.</span><span class="sxs-lookup"><span data-stu-id="c292c-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="c292c-110">Konfigurálás</span><span class="sxs-lookup"><span data-stu-id="c292c-110">Configuration</span></span> 

1. <span data-ttu-id="c292c-111">A napidíjhelyek hozzáadásához nyissa meg a **Beállítás** > **Számítások és kódok** > **Napidíjhelyek** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c292c-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="c292c-112">A fent hozzáadott helyek mindegyikéhez válassza ki a napidíj mértékét és a pénznemet, amely egy adott kezdő és záró dátum között érvényes a szálloda, az étkezés és az egyéb költségek esetében.</span><span class="sxs-lookup"><span data-stu-id="c292c-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="c292c-113">A napidíj és a pénznemek a **Beállítás** > **Számítások és kódok** > **Napidíjak** alatt állíthatók be.</span><span class="sxs-lookup"><span data-stu-id="c292c-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="c292c-114">A **Napidíjhelyek** oldalon konfigurálja a napidíjszinteket.</span><span class="sxs-lookup"><span data-stu-id="c292c-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="c292c-115">A napidíjszintek lehetővé teszik a napidíj százalékos felosztásának meghatározását a szállodai, étkezési és egyéb költségek esetében.</span><span class="sxs-lookup"><span data-stu-id="c292c-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="c292c-116">A reggeli, ebéd vagy vacsora esetében érvényes étkezési százalékos csökkentés megadásához frissítse a mezőket a **Költségkezelési paraméterek** oldalon, a **Napidíj** lapon.</span><span class="sxs-lookup"><span data-stu-id="c292c-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="c292c-117">Kiadások beküldése napidíj használatával</span><span class="sxs-lookup"><span data-stu-id="c292c-117">Submit expenses using per diem</span></span>
<span data-ttu-id="c292c-118">A kiadások napidíjak használatával történő elküldéséhez használja a **Napidíj** költségkategóriát költségjelentés létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="c292c-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="c292c-119">Adja meg a **Napidíj kezdő dátuma** , a **Napidíj záró dátuma** és a **Napidíjhely** értékét.</span><span class="sxs-lookup"><span data-stu-id="c292c-119">Enter the **Per diem from date** , **Per diem to date** ,  and the **Per diem location**.</span></span> <span data-ttu-id="c292c-120">Az összeget a kiválasztott hely napidíjmértékei alapján számítják ki, az étkezési csökkentés pedig a napidíjszintek alapján kerül kiszámításra.</span><span class="sxs-lookup"><span data-stu-id="c292c-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
