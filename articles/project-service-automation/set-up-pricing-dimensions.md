---
title: Állítson be egyéni mezőket árazási dimenziókként
description: Ez a témakör az egyedi árazási dimenziók beállításáról nyújt információkat.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: d5f59779-a6ed-4854-ab82-2810dace288f
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 8f19254acfc7f03ed7ccca95ed7e2b94cc199d3b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752196"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a><span data-ttu-id="194ac-103">Állítson be egyéni mezőket árazási dimenziókként</span><span class="sxs-lookup"><span data-stu-id="194ac-103">Set up custom fields as pricing dimensions</span></span> 

<span data-ttu-id="194ac-104">Ez a témakör feltételezi, hogy először elvégezte a következő eljárásokat: [Egyéni mezők és entitások létrehozása](create-custom-fields-entities.md) és [Egyéni mezők hozzáadása az ár a telepítést és tranzakciós szervezetek](field-references.md).</span><span class="sxs-lookup"><span data-stu-id="194ac-104">Before you begin, this topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md) and [Add custom fields to price setup and transactional entities](field-references.md).</span></span> <span data-ttu-id="194ac-105">Ha még nem fejezte be ezeket az eljárásokat, menjen vissza, és fejezze be őket, majd térjen vissza ehhez a témához.</span><span class="sxs-lookup"><span data-stu-id="194ac-105">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span> 

<span data-ttu-id="194ac-106">Ez a témakör az egyedi árazási dimenziók beállításáról nyújt információkat.</span><span class="sxs-lookup"><span data-stu-id="194ac-106">This topic provides information about setting up custom pricing dimensions.</span></span> <span data-ttu-id="194ac-107">A Project Service webes felületén, a **Paraméterek** oldalon, az **Összeg alapú árképzési dimenziók** lapon megjelennek az árazási dimenziók entitásaiban szereplő rekordok.</span><span class="sxs-lookup"><span data-stu-id="194ac-107">In the Project Service web interface, on the **Parameters** page, the **Amount-Based Pricing Dimensions** tab shows the records in the pricing dimension entities.</span></span> <span data-ttu-id="194ac-108">Alapértelmezés szerint a Project Service telepítése 2 sort hoz létre a fül rácsában:</span><span class="sxs-lookup"><span data-stu-id="194ac-108">By default, Project Service installation creates 2 rows in the grid on this tab:</span></span>

- <span data-ttu-id="194ac-109">**msdyn_resourcecategory** (Szerepkör)</span><span class="sxs-lookup"><span data-stu-id="194ac-109">**msdyn_resourcecategory** (Role)</span></span>
- <span data-ttu-id="194ac-110">**msdyn_OrganizationalUnit** (Szervezeti egység)</span><span class="sxs-lookup"><span data-stu-id="194ac-110">**msdyn_OrganizationalUnit** (Organizational Unit)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="194ac-111">Ne törölje ezeket a sorokat.</span><span class="sxs-lookup"><span data-stu-id="194ac-111">Do not delete these rows.</span></span> <span data-ttu-id="194ac-112">Azonban, ha nincs rájuk szükség, akkor azokat nem kell alkalmazni egy adott helyzetben a **Költségre alkalmazandó**, **Értékesítésre alkalmazandó** és **Vásárlásra alkalmazandó** paraméterek **Nem** értékre állításával.</span><span class="sxs-lookup"><span data-stu-id="194ac-112">However, if you do not need them, you can make them not applicable in a specific context by setting **Applicable to Cost**, **Applicable to Sales**, and **Applicable to Purchase** all to **No**.</span></span> <span data-ttu-id="194ac-113">Ha ezeket az attribútumértékeket **Nem**-re állítja, akkor ugyanaz a hatása, ha nem rendelkezik mezővel, mint árképzési dimenzióval.</span><span class="sxs-lookup"><span data-stu-id="194ac-113">Setting these attribute values to **No** has the same effect of not having the field as a pricing dimension.</span></span>

<span data-ttu-id="194ac-114">Ahhoz, hogy egy mező árképzési dimenzióvá váljon, a következőknek kell lennie:</span><span class="sxs-lookup"><span data-stu-id="194ac-114">For a field to become a pricing dimension, it must be:</span></span>

- <span data-ttu-id="194ac-115">Mezőként lett létrehozva a **Szerepkörát** és **Szerepkör felár** entitásokban.</span><span class="sxs-lookup"><span data-stu-id="194ac-115">Created as a field in the **Role Price** and **Role Price markup** entities.</span></span> <span data-ttu-id="194ac-116">További információkért lásd: [Egyéni mezők hozzáadása az árbeállításhoz és a tranzakciós entitásokhoz](field-references.md).</span><span class="sxs-lookup"><span data-stu-id="194ac-116">For more information on how to do this, see [Add custom fields to price setup and transactional entities](field-references.md).</span></span>
- <span data-ttu-id="194ac-117">Sorként jön létre az **Árazási dimenzió** táblázatban.</span><span class="sxs-lookup"><span data-stu-id="194ac-117">Created as a row in the **Pricing Dimension** table.</span></span> <span data-ttu-id="194ac-118">Például adjon hozzá árképzési dimenziós sorokat a következő ábra szerint.</span><span class="sxs-lookup"><span data-stu-id="194ac-118">For example, add pricing dimension rows as shown in the following graphic.</span></span> 

![Összeg alapú árképzési dimenziós sorok](media/Amt-based-PD.png)

<span data-ttu-id="194ac-120">Vegye figyelembe, hogy az erőforrás-munkaidőt (**msdyn_resourceworkhours**) feláralapú dimenzióként adták hozzá, és a **Feláron alapuló árképzési dimenzió** lapon a rácshoz adták.</span><span class="sxs-lookup"><span data-stu-id="194ac-120">Notice that Resource Work hours (**msdyn_resourceworkhours**) has been added as a markup-based dimension and has been added to the grid on the **Markup Based Pricing Dimension** tab.</span></span>

![Feláralapú árképzési dimenziós sorok](media/Markup-based-PD.png)

> [!IMPORTANT]
> <span data-ttu-id="194ac-122">A táblázat árazási dimenziós adatainak bármilyen megváltozása, létező vagy új, csak a gyorsítótár frissítése után kerül továbbításra a Project Service árazási üzleti logikájába.</span><span class="sxs-lookup"><span data-stu-id="194ac-122">Any change to pricing dimension data in this table, existing or new, is propagated to the Project Service pricing business logic only after the cache is refreshed.</span></span> <span data-ttu-id="194ac-123">A gyorsítótár frissítési ideje akár 10 percet is igénybe vehet.</span><span class="sxs-lookup"><span data-stu-id="194ac-123">The cache refresh time may take up to 10 minutes.</span></span> <span data-ttu-id="194ac-124">Várja meg, amíg az ár alapértelmezett logikájában bekövetkező változások megjelennek, amelyeknek az árképzési dimenzió adatainak megváltozásából kell következniük.</span><span class="sxs-lookup"><span data-stu-id="194ac-124">Allow that length of time to see the changes in price defaulting logic that must result from changes to the Pricing Dimension data.</span></span>


## <a name="attributes-of-the-pricing-dimensions-table"></a><span data-ttu-id="194ac-125">Az Árképzési dimenziók táblázat attribútumai</span><span class="sxs-lookup"><span data-stu-id="194ac-125">Attributes of the Pricing Dimensions table</span></span>
<span data-ttu-id="194ac-126">A következő szakaszok információkat tartalmaznak az **Árazási dimenziók** táblázat különböző attribútumairól.</span><span class="sxs-lookup"><span data-stu-id="194ac-126">The following sections provide information about the different attributes in the **Pricing Dimensions** table.</span></span>

### <a name="pricing-dimension-name"></a><span data-ttu-id="194ac-127">Árképzési dimenzió neve</span><span class="sxs-lookup"><span data-stu-id="194ac-127">Pricing Dimension Name</span></span>
<span data-ttu-id="194ac-128">Ennek az értéknek pontosan meg kell egyeznie a mezőséma nevével, amelyet a **Szerepkörár** táblázathoz adunk az egyedi árazási dimenziókhoz.</span><span class="sxs-lookup"><span data-stu-id="194ac-128">This value should be the exact same as the schema name of the field that is added to the **Role Price** table for custom pricing dimensions.</span></span> <span data-ttu-id="194ac-129">A mezőknek a **Szerepkörár** táblájához történő hozzáadásával kapcsolatos további információkért lásd: [Egyéni mezők hozzáadása az árbeállításhoz és tranzakciós entitásokhoz](field-references.md).</span><span class="sxs-lookup"><span data-stu-id="194ac-129">For more information about adding fields to the **Role Price** table, see [Add custom fields to price setup and transactional entities](field-references.md).</span></span>

### <a name="type-of-dimension"></a><span data-ttu-id="194ac-130">A dimenzió típusa</span><span class="sxs-lookup"><span data-stu-id="194ac-130">Type of dimension</span></span>
<span data-ttu-id="194ac-131">Az árképzési dimenzióknak két típusa létezik:</span><span class="sxs-lookup"><span data-stu-id="194ac-131">There are two types of pricing dimensions:</span></span>
  
  - <span data-ttu-id="194ac-132">**Összegalapú dimenziók**: A bemeneti kontextus dimenzióértékei illeszkednek a dimenziós értékekhez a **Szerepkörár** sorban, és az ár/költség alapértelmezés szerint közvetlenül a **Szerepkörár** táblázatból származik.</span><span class="sxs-lookup"><span data-stu-id="194ac-132">**Amount-based dimensions**: The dimension values from the input context are matched to the dimension values on **Role Price** line and the price/cost is defaulted directly from the **Role Price** table.</span></span>
  - <span data-ttu-id="194ac-133">**Feláron alapuló dimenziók** : Ezek olyan dimenziók, amelyekben a Project Service a következő háromlépcsős eljárást fogja alkalmazni az ár/költség megszerzésére</span><span class="sxs-lookup"><span data-stu-id="194ac-133">**Markup-based dimensions**: These are dimensions where Project Service will adopt the following 3-step process to get the price/cost</span></span>
 
    1. <span data-ttu-id="194ac-134">A Project Service összeegyezteti a nem jelölésen alapuló dimenziós értékeket a bemeneti környezetből a Szerepkörár sorba az alapkamat megszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="194ac-134">Project Service matches the non-markup-based dimension values from the input context to the Role Price line to get the base rate.</span></span>
    2. <span data-ttu-id="194ac-135">A Project Service az összes dimenziós értéket egyezteti a bemeneti környezetből a **Szerepkörár** sorig, hogy megkapja a felárszázalékot.</span><span class="sxs-lookup"><span data-stu-id="194ac-135">Project Service matches all of the dimension values from the input context to the **Role Price Markup** line to get a markup percentage.</span></span>
    3. <span data-ttu-id="194ac-136">A Project Service a második lépéstől a jelölési százalékot az alapvető kamatlábakhoz használja, amelyeket az első lépésben a **Szerepkörár** táblázatból nyert, hogy elérje a végső árat/költségeket.</span><span class="sxs-lookup"><span data-stu-id="194ac-136">Project Service applies the markup percentage from the second step to the base rate obtained from the **Role Price** table in the first step to arrive at final price/cost.</span></span>
   
   <span data-ttu-id="194ac-137">Az alábbi táblázat szemlélteti az árkülönbözetek kiszámítását.</span><span class="sxs-lookup"><span data-stu-id="194ac-137">The following table illustrates the calculation of price markups.</span></span>
  
| <span data-ttu-id="194ac-138">Szerepkör</span><span class="sxs-lookup"><span data-stu-id="194ac-138">Role</span></span>        | <span data-ttu-id="194ac-139">Szerv. egység</span><span class="sxs-lookup"><span data-stu-id="194ac-139">Org Unit</span></span>    |<span data-ttu-id="194ac-140">Munka helye</span><span class="sxs-lookup"><span data-stu-id="194ac-140">Work Location</span></span>      |<span data-ttu-id="194ac-141">Normál cím</span><span class="sxs-lookup"><span data-stu-id="194ac-141">Standard Title</span></span>      |<span data-ttu-id="194ac-142">Erőforrás-munkaidő</span><span class="sxs-lookup"><span data-stu-id="194ac-142">Resource Work Hours</span></span>      |  <span data-ttu-id="194ac-143">Felár</span><span class="sxs-lookup"><span data-stu-id="194ac-143">Mark Up</span></span>|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | <span data-ttu-id="194ac-144">Contoso India</span><span class="sxs-lookup"><span data-stu-id="194ac-144">Contoso India</span></span>|<span data-ttu-id="194ac-145">Telephely</span><span class="sxs-lookup"><span data-stu-id="194ac-145">Onsite</span></span>            |                    |<span data-ttu-id="194ac-146">Túlóra</span><span class="sxs-lookup"><span data-stu-id="194ac-146">Overtime</span></span>                 |<span data-ttu-id="194ac-147">15</span><span class="sxs-lookup"><span data-stu-id="194ac-147">15</span></span>     |
|             | <span data-ttu-id="194ac-148">Contoso India</span><span class="sxs-lookup"><span data-stu-id="194ac-148">Contoso India</span></span>|<span data-ttu-id="194ac-149">Helyi</span><span class="sxs-lookup"><span data-stu-id="194ac-149">Local</span></span>             |                    |<span data-ttu-id="194ac-150">Túlóra</span><span class="sxs-lookup"><span data-stu-id="194ac-150">Overtime</span></span>                 |<span data-ttu-id="194ac-151">10</span><span class="sxs-lookup"><span data-stu-id="194ac-151">10</span></span>     |
|             | <span data-ttu-id="194ac-152">Contoso USA</span><span class="sxs-lookup"><span data-stu-id="194ac-152">Contoso US</span></span>   |<span data-ttu-id="194ac-153">Helyi</span><span class="sxs-lookup"><span data-stu-id="194ac-153">Local</span></span>             |                    |<span data-ttu-id="194ac-154">Túlóra</span><span class="sxs-lookup"><span data-stu-id="194ac-154">Overtime</span></span>                 |<span data-ttu-id="194ac-155">20</span><span class="sxs-lookup"><span data-stu-id="194ac-155">20</span></span>     |


<span data-ttu-id="194ac-156">Ha a Contoso India erőforrása, amelynek alapára 100 USD, működik a helyszínen, és napi 8 órát szokásos időt és 2 órát túlórát jelent az időbeíráskor, a Project Service árazási motor 8 órán keresztül 100-as alapárat fog használni rögzíteni 800 USD.</span><span class="sxs-lookup"><span data-stu-id="194ac-156">If a resource from Contoso India whose base rate is 100 USD is working onsite, and they log 8 hours of Regular time and 2 hours of overtime on the time entry, the Project Service pricing engine will use the base rate of 100 for the 8 hours to record 800 USD.</span></span> <span data-ttu-id="194ac-157">A 2 órás túlórára 15%-os felárat kell alkalmazni a 100-as alapárra, hogy 115 USD egységárhoz jussanak, és a teljes költség 230 USD lesz.</span><span class="sxs-lookup"><span data-stu-id="194ac-157">For the 2 hours overtime, a markup of 15% will be applied to the base rate of 100 to get a unit price of 115 USD and will record a total cost of 230 USD.</span></span>

### <a name="applicable-to-cost"></a><span data-ttu-id="194ac-158">Költségre alkalmazható</span><span class="sxs-lookup"><span data-stu-id="194ac-158">Applicable to Cost</span></span> 
<span data-ttu-id="194ac-159">Ha ezt **Igen**-re állítja , ez azt jelzi, hogy a bemeneti kontextus dimenzióértékét kell használni a **Szerepkörár**és **Szerepkör felár** összeegyeztetéséhez, amikor a költségeket és a felárarányokat lekérdezi.</span><span class="sxs-lookup"><span data-stu-id="194ac-159">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the cost and markup rates.</span></span>

### <a name="applicable-to-sales"></a><span data-ttu-id="194ac-160">Értékesítésre alkalmazható</span><span class="sxs-lookup"><span data-stu-id="194ac-160">Applicable to Sales</span></span>
<span data-ttu-id="194ac-161">Ha ez az **Igen**-re van állítva, akkor ez azt jelzi, hogy a bemeneti kontextusban szereplő dimenzióértéket kell használni a **Szerepkörát** és **Szerepkör felár** összeegyeztetéséhez a számla és a felárarány lekérésekor.</span><span class="sxs-lookup"><span data-stu-id="194ac-161">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the bill and markup rates.</span></span>

### <a name="applicable-to-purchase"></a><span data-ttu-id="194ac-162">Vásárlásra alkalmazható</span><span class="sxs-lookup"><span data-stu-id="194ac-162">Applicable to Purchase</span></span>
<span data-ttu-id="194ac-163">Ha ezt **Igen**-re állítja, ez azt jelzi, hogy a bemeneti kontextus dimenzióértékét kell használni a **Szerepkörát** és **Szerepkör felár** összeegyeztetéséhez a vételár lekérdezésekor.</span><span class="sxs-lookup"><span data-stu-id="194ac-163">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the purchase price.</span></span> <span data-ttu-id="194ac-164">A Project Service jelenleg nem támogatja az alvállalkozási forgatókönyveket, ezért ezt a mezőt nem használja.</span><span class="sxs-lookup"><span data-stu-id="194ac-164">Currently Project Service does not support subcontracting scenarios, so this field is not used.</span></span> 

### <a name="priority"></a><span data-ttu-id="194ac-165">Prioritás</span><span class="sxs-lookup"><span data-stu-id="194ac-165">Priority</span></span>
<span data-ttu-id="194ac-166">A dimenzió prioritásának meghatározása segít a Project Service árazásában abban az esetben is, ha nem talál pontos egyezést a bemeneti dimenziók értékei és a **Szerepkörát** vagy a **Szerep felár** táblázatok értékei között.</span><span class="sxs-lookup"><span data-stu-id="194ac-166">Setting the dimension priority helps Project Service pricing produce a price even when it can't find an exact match between the input dimension values and the values from the **Role Price** or **Role Price Markup** tables.</span></span> <span data-ttu-id="194ac-167">Ebben a forgatókönyvben a Project Service null értékeket fog használni a páratlan dimenziós értékekhez, a súlyok fontossági sorrendben történő megmérésével.</span><span class="sxs-lookup"><span data-stu-id="194ac-167">In this scenario, Project Service will use null values for unmatched dimension values by weighing the dimensions in order of their priority.</span></span>

- <span data-ttu-id="194ac-168">**Költségprioritás**: A dimenzió költség prioritásának értéke jelzi annak dimenzióját, amikor összeegyeztetik a költségárakkal.</span><span class="sxs-lookup"><span data-stu-id="194ac-168">**Cost Priority**: The value of a dimension's cost priority will indicate the weight of that dimension when matching against the setup of cost prices.</span></span> <span data-ttu-id="194ac-169">A **Költségprioritás** értékének egyedinek kell lennie, a **Költségre alkalmazható** dimenziókban.</span><span class="sxs-lookup"><span data-stu-id="194ac-169">The value of **Cost Priority** must be unique across dimensions that are **Applicable to Cost**.</span></span>
- <span data-ttu-id="194ac-170">**Értékesítési prioritás**: A dimenzió eladási prioritása értéke jelzi ennek a dimenziónak a súlyát, amikor egyeztetik az eladási árak vagy a számlázási tarifák beállításával.</span><span class="sxs-lookup"><span data-stu-id="194ac-170">**Sales Priority**: The value of dimension's sales priority will indicate the weight of that dimension when matching against the setup of sales prices or bill rates.</span></span> <span data-ttu-id="194ac-171">Az **Értékesítési prioritás** értékének egyedinek kell lennie, az **Értékesítésre alkalmazható** dimenziókban.</span><span class="sxs-lookup"><span data-stu-id="194ac-171">The value of **Sales Priority** must be unique across dimensions that are **Applicable to Sales**.</span></span>