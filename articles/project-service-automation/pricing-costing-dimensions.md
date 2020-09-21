---
title: Árképzés és költségdimenziók kezdőlap
description: Ez a témakör áttekintést nyújt az árképzési dimenziókról.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752207"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="3a289-103">Árképzés és költségdimenziók kezdőlap</span><span class="sxs-lookup"><span data-stu-id="3a289-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="3a289-104">Az árképzéshez és a költségek meghatározásához az emberi erőforrásokban felhasznált dimenziók két kategóriába sorolhatók:</span><span class="sxs-lookup"><span data-stu-id="3a289-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="3a289-105">Személyek</span><span class="sxs-lookup"><span data-stu-id="3a289-105">People</span></span>
- <span data-ttu-id="3a289-106">Tervezett munka</span><span class="sxs-lookup"><span data-stu-id="3a289-106">Planned work</span></span>

<span data-ttu-id="3a289-107">Emiatt kétféle árképzési dimenzió érhető el a Project Service Automation (PSA) szolgáltatásban:</span><span class="sxs-lookup"><span data-stu-id="3a289-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="3a289-108">**Értékkészletek** – Dimenziók, amelyek értékek készletének rögzített jegyzékei.</span><span class="sxs-lookup"><span data-stu-id="3a289-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="3a289-109">**Entitásalapú értékek** – Dimenziók, amelyek különböző értékkészletek lehetnek.</span><span class="sxs-lookup"><span data-stu-id="3a289-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="3a289-110">Árképzési dimenziók</span><span class="sxs-lookup"><span data-stu-id="3a289-110">Pricing dimensions</span></span>

<span data-ttu-id="3a289-111">A PSA alapértelmezett árképzési dimenziókkal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="3a289-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="3a289-112">Megnézheti ezeket a **Project Service** > **Paraméterek** részére lépve.</span><span class="sxs-lookup"><span data-stu-id="3a289-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="3a289-113">A paraméterrekordban az **Összegalapú árképzési dimenziók** fülön ellenőrizze, hogy a **msdyn_resourcecategory** szerepkör és a **msdyn_organizationalunit** erőforrásbiztosító szervezeti egység rendelkezik **Értékesítésre vonatkozó** és **Költségre vonatkozó** mezőkkel, és hogy ezek beállítása **Igen** legyen.</span><span class="sxs-lookup"><span data-stu-id="3a289-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="3a289-114">Ez lehetővé teszi az egyes szerepkörök és szervezeti egységkombinációk árának és költségének beállítását.</span><span class="sxs-lookup"><span data-stu-id="3a289-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Képernyőkép a Project Service paramétereiről az „Értékesítésre vonatkozó” mező kiemelésével](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="3a289-116">Ha a PSA 3. verzióját megelőzően használta a használatra kész szerepköröket és szervezeti egységeket árképzési dimenziókként, akkor nem lesz észlelhető változás.</span><span class="sxs-lookup"><span data-stu-id="3a289-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="3a289-117">Továbbra is használhatja a Project Service szolgáltatást a megszokott módon.</span><span class="sxs-lookup"><span data-stu-id="3a289-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="3a289-118">Ha további attribútumok használatával szükséges árakat vagy költségeket fizetnie az erőforrásokért, testreszabott mezőket, entitásokat és dimenziókat hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="3a289-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="3a289-119">További információt a következő témakörökben talál, azonban vegye figyelembe, hogy az eljárásokat az alábbiakban felsorolt sorrendben kell elvégeznie:</span><span class="sxs-lookup"><span data-stu-id="3a289-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="3a289-120">Egyéni mezők és entitások létrehozása</span><span class="sxs-lookup"><span data-stu-id="3a289-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="3a289-121">Egyéni mezők hozzáadása az árbeállításhoz és a tranzakciós entitásokhoz</span><span class="sxs-lookup"><span data-stu-id="3a289-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="3a289-122">Egyéni mezők beállítása árképzési dimenziókként</span><span class="sxs-lookup"><span data-stu-id="3a289-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="3a289-123">Bővítményattribútumok frissítése új árképzési dimenziók felvételéhez</span><span class="sxs-lookup"><span data-stu-id="3a289-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="3a289-124">Az emberi erőforrás munkaidejének árképzése</span><span class="sxs-lookup"><span data-stu-id="3a289-124">Pricing human resource time</span></span>
<span data-ttu-id="3a289-125">Az, hogy a szervezet milyen módon képez árat a humán erőforrás munkaidejére gyakran fontos stratégiai szempont, amely közvetlenül befolyásolja a szervezet jövedelmezőségét.</span><span class="sxs-lookup"><span data-stu-id="3a289-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="3a289-126">Dolgozzon együtt a pénzügyi csapatokkal és a gyakorlati vezetőkkel, amikor a szervezet készen áll arra, hogy meghatározza, hogyan kívánja beállítani a számla- és költségmértéket az emberi erőforrás munkaidejére vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="3a289-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="3a289-127">Az árképzés egyéb szempontjai között szerepel, hogy újra kell-e használni olyan mezőket vagy entitásokat, amelyek jelenleg nem árképzési dimenziók, ugyanakkor a szervezetben érvényes árképzési dimenzióként alkalmazandók.</span><span class="sxs-lookup"><span data-stu-id="3a289-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="3a289-128">Az olyan mezők, mint a **Tranzakciós kategória** (**msdyn_transactioncategory**) és a **Lefoglalható erőforrás** (**bookableresource**) példák a jelöltdimenziókra.</span><span class="sxs-lookup"><span data-stu-id="3a289-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="3a289-129">Azt is meg kell fontolnia, hogy árképzési dimenzió tábla vagy értékkészlet legyen-e.</span><span class="sxs-lookup"><span data-stu-id="3a289-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="3a289-130">Ha egy dimenzió értékének olyan változásait látja előre, amelyek meghaladják a 10-et vagy 12-őt, és további attribútumokra van szüksége ezekhez az értékekhez, akkor érdemesebb entitást létrehoznia, mint értékkészletet.</span><span class="sxs-lookup"><span data-stu-id="3a289-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="3a289-131">Az értékkészlet fenntartásához, például az értékek hozzáadásához vagy eltávolításához, rendszergazda vagy fejlesztő szükséges, míg új sorok hozzáadását a táblához a legtöbb felhasználó megteheti.</span><span class="sxs-lookup"><span data-stu-id="3a289-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="3a289-132">A következő példa azt a számlamértéket mutatja, amelyet azon szerepkör és erőforrásbiztosító szervezeti egység alapján állítanak fel, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="3a289-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="3a289-133">A költség mértéke általában a munkavállaló fizetési sávjától és attól a szervezeti egységtől függ, amelyhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="3a289-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="3a289-134">Ebben a példában a számlázási és költségtáblázatok a következőképpen alakulnak.</span><span class="sxs-lookup"><span data-stu-id="3a289-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="3a289-135">**Számlaminta**</span><span class="sxs-lookup"><span data-stu-id="3a289-135">**Sample bill rates**</span></span>

| <span data-ttu-id="3a289-136">Szerepkör</span><span class="sxs-lookup"><span data-stu-id="3a289-136">Role</span></span>        | <span data-ttu-id="3a289-137">Szerv. egység</span><span class="sxs-lookup"><span data-stu-id="3a289-137">Org Unit</span></span>    |<span data-ttu-id="3a289-138">Egység</span><span class="sxs-lookup"><span data-stu-id="3a289-138">Unit</span></span>      |<span data-ttu-id="3a289-139">Ár</span><span class="sxs-lookup"><span data-stu-id="3a289-139">Price</span></span>      |<span data-ttu-id="3a289-140">Pénznem</span><span class="sxs-lookup"><span data-stu-id="3a289-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="3a289-141">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="3a289-141">Developer</span></span>   | <span data-ttu-id="3a289-142">Contoso USA</span><span class="sxs-lookup"><span data-stu-id="3a289-142">Contoso US</span></span>  |<span data-ttu-id="3a289-143">Hour</span><span class="sxs-lookup"><span data-stu-id="3a289-143">Hour</span></span> | <span data-ttu-id="3a289-144">200</span><span class="sxs-lookup"><span data-stu-id="3a289-144">200</span></span>|<span data-ttu-id="3a289-145">USD</span><span class="sxs-lookup"><span data-stu-id="3a289-145">USD</span></span>     |
| <span data-ttu-id="3a289-146">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="3a289-146">Developer</span></span>   | <span data-ttu-id="3a289-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="3a289-147">Contoso India</span></span> |<span data-ttu-id="3a289-148">Hour</span><span class="sxs-lookup"><span data-stu-id="3a289-148">Hour</span></span>|   <span data-ttu-id="3a289-149">112</span><span class="sxs-lookup"><span data-stu-id="3a289-149">112</span></span>|<span data-ttu-id="3a289-150">USD</span><span class="sxs-lookup"><span data-stu-id="3a289-150">USD</span></span>     |


<span data-ttu-id="3a289-151">**Költségminta**</span><span class="sxs-lookup"><span data-stu-id="3a289-151">**Sample cost rates**</span></span>

| <span data-ttu-id="3a289-152">Fizetési sáv</span><span class="sxs-lookup"><span data-stu-id="3a289-152">Salary Band</span></span>     | <span data-ttu-id="3a289-153">Szerv. egység</span><span class="sxs-lookup"><span data-stu-id="3a289-153">Org Unit</span></span>    |<span data-ttu-id="3a289-154">Egység</span><span class="sxs-lookup"><span data-stu-id="3a289-154">Unit</span></span>      |<span data-ttu-id="3a289-155">Ár</span><span class="sxs-lookup"><span data-stu-id="3a289-155">Price</span></span>      |<span data-ttu-id="3a289-156">Pénznem</span><span class="sxs-lookup"><span data-stu-id="3a289-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="3a289-157">Cégem_Sáv1</span><span class="sxs-lookup"><span data-stu-id="3a289-157">My company_Band1</span></span> | <span data-ttu-id="3a289-158">Contoso USA</span><span class="sxs-lookup"><span data-stu-id="3a289-158">Contoso US</span></span>  |<span data-ttu-id="3a289-159">Hour</span><span class="sxs-lookup"><span data-stu-id="3a289-159">Hour</span></span> | <span data-ttu-id="3a289-160">145</span><span class="sxs-lookup"><span data-stu-id="3a289-160">145</span></span>|<span data-ttu-id="3a289-161">USD</span><span class="sxs-lookup"><span data-stu-id="3a289-161">USD</span></span>     |
| <span data-ttu-id="3a289-162">Cégem_Sáv2</span><span class="sxs-lookup"><span data-stu-id="3a289-162">My company_Band2</span></span> | <span data-ttu-id="3a289-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="3a289-163">Contoso India</span></span> |<span data-ttu-id="3a289-164">Hour</span><span class="sxs-lookup"><span data-stu-id="3a289-164">Hour</span></span>|   <span data-ttu-id="3a289-165">67</span><span class="sxs-lookup"><span data-stu-id="3a289-165">67</span></span>|<span data-ttu-id="3a289-166">USD</span><span class="sxs-lookup"><span data-stu-id="3a289-166">USD</span></span>     |
