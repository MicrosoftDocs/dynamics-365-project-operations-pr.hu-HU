---
title: Árazási dimenziók áttekintése
description: Ez a témakör a Dynamics 365 Project Operations árképzési dimenzióiról nyújt információkat.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898219"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="91a95-103">Árazási dimenziók áttekintése</span><span class="sxs-lookup"><span data-stu-id="91a95-103">Pricing dimensions overview</span></span>

<span data-ttu-id="91a95-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="91a95-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="91a95-105">Az árképzéshez és a költségek meghatározásához az emberi erőforrásokban felhasznált dimenziók két kategóriába sorolhatók:</span><span class="sxs-lookup"><span data-stu-id="91a95-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="91a95-106">Személyek</span><span class="sxs-lookup"><span data-stu-id="91a95-106">People</span></span>
- <span data-ttu-id="91a95-107">Tervezett munka</span><span class="sxs-lookup"><span data-stu-id="91a95-107">Planned work</span></span>

<span data-ttu-id="91a95-108">Emiatt kétféle árképzési dimenzió érhető el:</span><span class="sxs-lookup"><span data-stu-id="91a95-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="91a95-109">**Értékkészletek**: Azon dimenziók, amelyek értékcsoportok rögzített enumerálásai.</span><span class="sxs-lookup"><span data-stu-id="91a95-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="91a95-110">**Entitásalapú értékek**: Azon dimenziók, amelyek különböző értékcsoportok lehetnek.</span><span class="sxs-lookup"><span data-stu-id="91a95-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="91a95-111">Árazási dimenziók</span><span class="sxs-lookup"><span data-stu-id="91a95-111">Pricing dimensions</span></span>

<span data-ttu-id="91a95-112">A Dynamics 365 Project Operations szolgáltatás részét képezi az árképzési dimenziók alapértelmezett csoportja.</span><span class="sxs-lookup"><span data-stu-id="91a95-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="91a95-113">Ezek az árképzési dimenziók a **Project Operations** > **Paraméterek** részén tekinthetők meg.</span><span class="sxs-lookup"><span data-stu-id="91a95-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="91a95-114">A paraméterrekordban az **Összegalapú árképzési dimenziók** fülön ellenőrizze, hogy a **msdyn_resourcecategory** szerepkör és a **msdyn_organizationalunit** erőforrásbiztosító szervezeti egység rendelkezik **Értékesítésre vonatkozó** és **Költségre vonatkozó** mezőkkel, és hogy ezek beállítása **Igen** legyen.</span><span class="sxs-lookup"><span data-stu-id="91a95-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="91a95-115">Ha engedélyezi ezeket a mezőket, beállíthatja az egyes szerepkörök és szervezeti egységek kombinációjához tartozó árakat és költségeket.</span><span class="sxs-lookup"><span data-stu-id="91a95-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="91a95-116">Ha további attribútumok használatával szükséges árakat vagy költségeket fizetnie az erőforrásokért, testreszabott mezőket, entitásokat és dimenziókat hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="91a95-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="91a95-117">Az emberi erőforrás munkaidejének árképzése</span><span class="sxs-lookup"><span data-stu-id="91a95-117">Pricing human resource time</span></span>
<span data-ttu-id="91a95-118">Az, hogy a szervezet milyen módon képez árat a humán erőforrás munkaidejére gyakran fontos stratégiai szempont, amely közvetlenül befolyásolja a szervezet jövedelmezőségét.</span><span class="sxs-lookup"><span data-stu-id="91a95-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="91a95-119">Dolgozzon együtt a pénzügyi csapatokkal és a gyakorlati vezetőkkel, amikor a szervezet készen áll arra, hogy meghatározza, hogyan kívánja beállítani a számla- és költségmértéket az emberi erőforrás munkaidejére vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="91a95-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="91a95-120">Az árképzés egyéb szempontjai között szerepel, hogy újra kell-e használni olyan mezőket vagy entitásokat, amelyek jelenleg nem árképzési dimenziók, ugyanakkor a szervezetben érvényes árképzési dimenzióként alkalmazandók.</span><span class="sxs-lookup"><span data-stu-id="91a95-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="91a95-121">Az olyan mezők, mint a **Tranzakciós kategória** (**msdyn_transactioncategory**) és a **Lefoglalható erőforrás** (**bookableresource**) példák a jelöltdimenziókra.</span><span class="sxs-lookup"><span data-stu-id="91a95-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="91a95-122">Azt is gondolja át, hogy az árképzési dimenzió tábla vagy értékkészlet legyen-e.</span><span class="sxs-lookup"><span data-stu-id="91a95-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="91a95-123">Ha egy dimenzió értékének olyan változásait látja előre, amelyek meghaladják a 10-et vagy 12-őt, és további attribútumokra van szüksége ezekhez az értékekhez, akkor érdemesebb entitást létrehoznia, mint értékkészletet.</span><span class="sxs-lookup"><span data-stu-id="91a95-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="91a95-124">Az értékkészlet fenntartásához, például az értékek hozzáadásához vagy eltávolításához, rendszergazda vagy fejlesztő szükséges, míg új sorok hozzáadását a táblához a legtöbb felhasználó megteheti.</span><span class="sxs-lookup"><span data-stu-id="91a95-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="91a95-125">A következő példa azt a számlamértéket mutatja, amelyet azon szerepkör és erőforrásbiztosító szervezeti egység alapján állítanak fel, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="91a95-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="91a95-126">A költség mértéke általában a munkavállaló fizetési sávjától és attól a szervezeti egységtől függ, amelyhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="91a95-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="91a95-127">Ebben a példában a számlázási és költségtáblázatok a következőképpen alakulnak.</span><span class="sxs-lookup"><span data-stu-id="91a95-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="91a95-128">**Számlaminta**</span><span class="sxs-lookup"><span data-stu-id="91a95-128">**Sample bill rates**</span></span>

| <span data-ttu-id="91a95-129">Szerepkör</span><span class="sxs-lookup"><span data-stu-id="91a95-129">Role</span></span>        | <span data-ttu-id="91a95-130">Szerv. egység</span><span class="sxs-lookup"><span data-stu-id="91a95-130">Org Unit</span></span>    |<span data-ttu-id="91a95-131">Egység</span><span class="sxs-lookup"><span data-stu-id="91a95-131">Unit</span></span>      |<span data-ttu-id="91a95-132">Ár</span><span class="sxs-lookup"><span data-stu-id="91a95-132">Price</span></span>      |<span data-ttu-id="91a95-133">Pénznem</span><span class="sxs-lookup"><span data-stu-id="91a95-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="91a95-134">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="91a95-134">Developer</span></span>   | <span data-ttu-id="91a95-135">Contoso USA</span><span class="sxs-lookup"><span data-stu-id="91a95-135">Contoso US</span></span>  |<span data-ttu-id="91a95-136">Hour</span><span class="sxs-lookup"><span data-stu-id="91a95-136">Hour</span></span> | <span data-ttu-id="91a95-137">200</span><span class="sxs-lookup"><span data-stu-id="91a95-137">200</span></span>|<span data-ttu-id="91a95-138">USD</span><span class="sxs-lookup"><span data-stu-id="91a95-138">USD</span></span>     |
| <span data-ttu-id="91a95-139">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="91a95-139">Developer</span></span>   | <span data-ttu-id="91a95-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="91a95-140">Contoso India</span></span> |<span data-ttu-id="91a95-141">Hour</span><span class="sxs-lookup"><span data-stu-id="91a95-141">Hour</span></span>|   <span data-ttu-id="91a95-142">112</span><span class="sxs-lookup"><span data-stu-id="91a95-142">112</span></span>|<span data-ttu-id="91a95-143">USD</span><span class="sxs-lookup"><span data-stu-id="91a95-143">USD</span></span>     |


<span data-ttu-id="91a95-144">**Költségminta**</span><span class="sxs-lookup"><span data-stu-id="91a95-144">**Sample cost rates**</span></span>

| <span data-ttu-id="91a95-145">Fizetési sáv</span><span class="sxs-lookup"><span data-stu-id="91a95-145">Salary Band</span></span>     | <span data-ttu-id="91a95-146">Szerv. egység</span><span class="sxs-lookup"><span data-stu-id="91a95-146">Org Unit</span></span>    |<span data-ttu-id="91a95-147">Egység</span><span class="sxs-lookup"><span data-stu-id="91a95-147">Unit</span></span>      |<span data-ttu-id="91a95-148">Ár</span><span class="sxs-lookup"><span data-stu-id="91a95-148">Price</span></span>      |<span data-ttu-id="91a95-149">Pénznem</span><span class="sxs-lookup"><span data-stu-id="91a95-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="91a95-150">Cégem_Sáv1</span><span class="sxs-lookup"><span data-stu-id="91a95-150">My company_Band1</span></span> | <span data-ttu-id="91a95-151">Contoso USA</span><span class="sxs-lookup"><span data-stu-id="91a95-151">Contoso US</span></span>  |<span data-ttu-id="91a95-152">Hour</span><span class="sxs-lookup"><span data-stu-id="91a95-152">Hour</span></span> | <span data-ttu-id="91a95-153">145</span><span class="sxs-lookup"><span data-stu-id="91a95-153">145</span></span>|<span data-ttu-id="91a95-154">USD</span><span class="sxs-lookup"><span data-stu-id="91a95-154">USD</span></span>     |
| <span data-ttu-id="91a95-155">Cégem_Sáv2</span><span class="sxs-lookup"><span data-stu-id="91a95-155">My company_Band2</span></span> | <span data-ttu-id="91a95-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="91a95-156">Contoso India</span></span> |<span data-ttu-id="91a95-157">Hour</span><span class="sxs-lookup"><span data-stu-id="91a95-157">Hour</span></span>|   <span data-ttu-id="91a95-158">67</span><span class="sxs-lookup"><span data-stu-id="91a95-158">67</span></span>|<span data-ttu-id="91a95-159">USD</span><span class="sxs-lookup"><span data-stu-id="91a95-159">USD</span></span>     |
