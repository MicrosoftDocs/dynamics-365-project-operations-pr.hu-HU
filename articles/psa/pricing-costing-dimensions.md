---
title: Árképzés és költségdimenziók kezdőlap
description: Ez a témakör áttekintést nyújt az árképzési dimenziókról.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9a2e2f7ed394229bbc553af9e616a6f322857195
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009259"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="c1742-103">Árképzés és költségdimenziók kezdőlap</span><span class="sxs-lookup"><span data-stu-id="c1742-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c1742-104">A projektalapú szervezetekben a munkadíjak és a költségszámítás beállításához használt dimenziókat a következő attribútumok befolyásolják:</span><span class="sxs-lookup"><span data-stu-id="c1742-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="c1742-105">A saját tapasztalataik, szerepkörük vagy földrajzi elhelyezkedésük alapján hasonló munkát végző személyek</span><span class="sxs-lookup"><span data-stu-id="c1742-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="c1742-106">A munka összetettségéhez vagy napszakhoz hasonlóan elvégzendő munka</span><span class="sxs-lookup"><span data-stu-id="c1742-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="c1742-107">Tekintettel a munka ezen attribútumainak jellegzetességére és a munka végrehajtásához szükséges személyekre, a Project Service Automation rendszerben kétféle árazási dimenzióérték érhető el:</span><span class="sxs-lookup"><span data-stu-id="c1742-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="c1742-108">**Értékkészletek**: azon attribútumok, amelyek értékcsoportok rögzített felsorolásai.</span><span class="sxs-lookup"><span data-stu-id="c1742-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="c1742-109">**Entitásalapú értékek**: azon attribútumok, amelyek olyan különböző, de véges értékcsoportokat tartalmazhatnak, amelyek idővel változhatnak.</span><span class="sxs-lookup"><span data-stu-id="c1742-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="c1742-110">Árazási dimenziók</span><span class="sxs-lookup"><span data-stu-id="c1742-110">Pricing dimensions</span></span>

<span data-ttu-id="c1742-111">A PSA alapértelmezett árképzési dimenziókkal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="c1742-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="c1742-112">Megnézheti ezeket a **Project Service** > **Paraméterek** részére lépve.</span><span class="sxs-lookup"><span data-stu-id="c1742-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="c1742-113">A paraméterrekordban az **Összegalapú árképzési dimenziók** fülön ellenőrizze, hogy a **msdyn_resourcecategory** szerepkör és a **msdyn_organizationalunit** erőforrásbiztosító szervezeti egység rendelkezik **Értékesítésre vonatkozó** és **Költségre vonatkozó** mezőkkel, és hogy ezek beállítása **Igen** legyen.</span><span class="sxs-lookup"><span data-stu-id="c1742-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="c1742-114">Ez lehetővé teszi az egyes szerepkörök és szervezeti egységkombinációk árának és költségének beállítását.</span><span class="sxs-lookup"><span data-stu-id="c1742-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Képernyőkép a Project Service paramétereiről az „Értékesítésre vonatkozó” mező kiemelésével](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="c1742-116">Ha a PSA 3. verzióját megelőzően használta a használatra kész szerepköröket és szervezeti egységeket árképzési dimenziókként, akkor nem lesz észlelhető változás.</span><span class="sxs-lookup"><span data-stu-id="c1742-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="c1742-117">Továbbra is használhatja a Project Service szolgáltatást a megszokott módon.</span><span class="sxs-lookup"><span data-stu-id="c1742-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="c1742-118">Ha további attribútumok használatával szükséges árakat vagy költségeket fizetnie az erőforrásokért, testreszabott mezőket, entitásokat és dimenziókat hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="c1742-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="c1742-119">További információt a következő témakörökben talál, azonban vegye figyelembe, hogy az eljárásokat az alábbiakban felsorolt sorrendben kell elvégeznie:</span><span class="sxs-lookup"><span data-stu-id="c1742-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="c1742-120">Egyéni mezők és entitások létrehozása</span><span class="sxs-lookup"><span data-stu-id="c1742-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="c1742-121">Egyéni mezők hozzáadása az árbeállításhoz és a tranzakciós entitásokhoz</span><span class="sxs-lookup"><span data-stu-id="c1742-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="c1742-122">Egyéni mezők beállítása árazási dimenziókként </span><span class="sxs-lookup"><span data-stu-id="c1742-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="c1742-123">Bővítményattribútumok frissítése új árképzési dimenziók felvételéhez</span><span class="sxs-lookup"><span data-stu-id="c1742-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="c1742-124">Az emberi erőforrás munkaidejének árképzése</span><span class="sxs-lookup"><span data-stu-id="c1742-124">Pricing human resource time</span></span>
<span data-ttu-id="c1742-125">Az, hogy a szervezet milyen módon képez árat a humán erőforrás munkaidejére gyakran fontos stratégiai szempont, amely közvetlenül befolyásolja a szervezet jövedelmezőségét.</span><span class="sxs-lookup"><span data-stu-id="c1742-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="c1742-126">Dolgozzon együtt a pénzügyi csapatokkal és a gyakorlati vezetőkkel, amikor a szervezet készen áll arra, hogy meghatározza, hogyan kívánja beállítani a számla- és költségmértéket az emberi erőforrás munkaidejére vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="c1742-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="c1742-127">Az árképzés egyéb szempontjai között szerepel, hogy újra kell-e használni olyan mezőket vagy entitásokat, amelyek jelenleg nem árképzési dimenziók, ugyanakkor a szervezetben érvényes árképzési dimenzióként alkalmazandók.</span><span class="sxs-lookup"><span data-stu-id="c1742-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="c1742-128">Az olyan mezők, mint a **Tranzakciós kategória** (**msdyn_transactioncategory**) és a **Lefoglalható erőforrás** (**bookableresource**) példák a jelöltdimenziókra.</span><span class="sxs-lookup"><span data-stu-id="c1742-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="c1742-129">Azt is gondolja át, hogy az árképzési dimenzió tábla vagy értékkészlet legyen-e.</span><span class="sxs-lookup"><span data-stu-id="c1742-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="c1742-130">Ha egy dimenzió értékének olyan változásait látja előre, amelyek meghaladják a 10-es vagy 12-es értéket, és további attribútumokra van szüksége ezekhez az értékekhez, akkor érdemesebb entitást létrehoznia, nem pedig értékkészletet.</span><span class="sxs-lookup"><span data-stu-id="c1742-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="c1742-131">Az értékkészlet fenntartásához – például az értékek hozzáadásához vagy eltávolításához – rendszergazda vagy fejlesztő szükséges, míg új sorok hozzáadását a táblához a legtöbb üzleti felhasználó elvégezheti.</span><span class="sxs-lookup"><span data-stu-id="c1742-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="c1742-132">A következő példa azt a számlamértéket mutatja, amelyet azon szerepkör és erőforrásbiztosító szervezeti egység alapján állítanak fel, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="c1742-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="c1742-133">A költség mértéke általában a munkavállaló fizetési sávjától és attól a szervezeti egységtől függ, amelyhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="c1742-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="c1742-134">Ebben a példában a számlázási és költségtáblázatok a következőképpen alakulnak.</span><span class="sxs-lookup"><span data-stu-id="c1742-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="c1742-135">**Számlaminta**</span><span class="sxs-lookup"><span data-stu-id="c1742-135">**Sample bill rates**</span></span>

| <span data-ttu-id="c1742-136">Szerepkör</span><span class="sxs-lookup"><span data-stu-id="c1742-136">Role</span></span>        | <span data-ttu-id="c1742-137">Szerv. egység</span><span class="sxs-lookup"><span data-stu-id="c1742-137">Org Unit</span></span>    |<span data-ttu-id="c1742-138">Kiszerelés</span><span class="sxs-lookup"><span data-stu-id="c1742-138">Unit</span></span>      |<span data-ttu-id="c1742-139">Ár</span><span class="sxs-lookup"><span data-stu-id="c1742-139">Price</span></span>      |<span data-ttu-id="c1742-140">Pénznem</span><span class="sxs-lookup"><span data-stu-id="c1742-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="c1742-141">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="c1742-141">Developer</span></span>   | <span data-ttu-id="c1742-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="c1742-142">Contoso US</span></span>  |<span data-ttu-id="c1742-143">Óra</span><span class="sxs-lookup"><span data-stu-id="c1742-143">Hour</span></span> | <span data-ttu-id="c1742-144">200</span><span class="sxs-lookup"><span data-stu-id="c1742-144">200</span></span>|<span data-ttu-id="c1742-145">USD</span><span class="sxs-lookup"><span data-stu-id="c1742-145">USD</span></span>     |
| <span data-ttu-id="c1742-146">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="c1742-146">Developer</span></span>   | <span data-ttu-id="c1742-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="c1742-147">Contoso India</span></span> |<span data-ttu-id="c1742-148">Óra</span><span class="sxs-lookup"><span data-stu-id="c1742-148">Hour</span></span>|   <span data-ttu-id="c1742-149">112</span><span class="sxs-lookup"><span data-stu-id="c1742-149">112</span></span>|<span data-ttu-id="c1742-150">USD</span><span class="sxs-lookup"><span data-stu-id="c1742-150">USD</span></span>     |


<span data-ttu-id="c1742-151">**Költségminta**</span><span class="sxs-lookup"><span data-stu-id="c1742-151">**Sample cost rates**</span></span>

| <span data-ttu-id="c1742-152">Fizetési sáv</span><span class="sxs-lookup"><span data-stu-id="c1742-152">Salary Band</span></span>     | <span data-ttu-id="c1742-153">Szerv. egység</span><span class="sxs-lookup"><span data-stu-id="c1742-153">Org Unit</span></span>    |<span data-ttu-id="c1742-154">Kiszerelés</span><span class="sxs-lookup"><span data-stu-id="c1742-154">Unit</span></span>      |<span data-ttu-id="c1742-155">Ár</span><span class="sxs-lookup"><span data-stu-id="c1742-155">Price</span></span>      |<span data-ttu-id="c1742-156">Pénznem</span><span class="sxs-lookup"><span data-stu-id="c1742-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="c1742-157">Cégem_Sáv1</span><span class="sxs-lookup"><span data-stu-id="c1742-157">My company_Band1</span></span> | <span data-ttu-id="c1742-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="c1742-158">Contoso US</span></span>  |<span data-ttu-id="c1742-159">Óra</span><span class="sxs-lookup"><span data-stu-id="c1742-159">Hour</span></span> | <span data-ttu-id="c1742-160">145</span><span class="sxs-lookup"><span data-stu-id="c1742-160">145</span></span>|<span data-ttu-id="c1742-161">USD</span><span class="sxs-lookup"><span data-stu-id="c1742-161">USD</span></span>     |
| <span data-ttu-id="c1742-162">Cégem_Sáv2</span><span class="sxs-lookup"><span data-stu-id="c1742-162">My company_Band2</span></span> | <span data-ttu-id="c1742-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="c1742-163">Contoso India</span></span> |<span data-ttu-id="c1742-164">Óra</span><span class="sxs-lookup"><span data-stu-id="c1742-164">Hour</span></span>|   <span data-ttu-id="c1742-165">67</span><span class="sxs-lookup"><span data-stu-id="c1742-165">67</span></span>|<span data-ttu-id="c1742-166">USD</span><span class="sxs-lookup"><span data-stu-id="c1742-166">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]