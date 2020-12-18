---
title: Projekt értékesítési árlistáinak felülbírálása
description: Ez a témakör az egyéni értékesítési árlisták létrehozásával kapcsolatban tartalmaz tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: af9baca540d89f4e5e616bdfdd6111bef29abe28
ms.sourcegitcommit: 656a9d03f260c29e988e2ff05b6e07ae0365d6d0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672234"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="2252c-103">Projekt értékesítési árlistáinak felülbírálása</span><span class="sxs-lookup"><span data-stu-id="2252c-103">Override project sales price lists</span></span>

<span data-ttu-id="2252c-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="2252c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="2252c-105">Az ügyfélre jellemző projektárlisták</span><span class="sxs-lookup"><span data-stu-id="2252c-105">Customer-specific project price lists</span></span>

<span data-ttu-id="2252c-106">Az ügyfél-specifikus árakra vonatkozó megállapodások projektárlisták formájában állíthatók be a Dynamics 365 Project Operations egy partnerrekordján.</span><span class="sxs-lookup"><span data-stu-id="2252c-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="2252c-107">Ha egy ügyfélhez tartozó projektárlistát szeretne létrehozni, akkor nyissa meg a partnerrekordot az **értékesítés** területen.</span><span class="sxs-lookup"><span data-stu-id="2252c-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="2252c-108">Nyissa meg a **Partnerek** listaoldalt.</span><span class="sxs-lookup"><span data-stu-id="2252c-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="2252c-109">Keresse meg és kattintson duplán egy ügyfélrekordra a **partner** részletező lap megnyitásához.</span><span class="sxs-lookup"><span data-stu-id="2252c-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="2252c-110">A **Projektárlisták** lapon válassza a **+ új projektárlista** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2252c-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="2252c-111">Az **új projektárlista** lapon válasszon ki egy árlistát a legördülő listából.</span><span class="sxs-lookup"><span data-stu-id="2252c-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="2252c-112">Csak azok az árlisták szerepelnek a rendszerben, amelyek esetében a környezet értéke **értékesítés**, és amelynek pénzneme megegyezik a partner pénznemével.</span><span class="sxs-lookup"><span data-stu-id="2252c-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="2252c-113">Nevezze el a társítást, majd válassza a **Mentés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2252c-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="2252c-114">Az ügyfélre jellemző projektárlista létrejön.</span><span class="sxs-lookup"><span data-stu-id="2252c-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="2252c-115">Ezt az árlistát fogja használni a rendszer az ügyfélhez létrehozott projektárajánlatok vagy szerződések alapértelmezett projektáraihoz, ahol az árajánlat vagy a projektszerződés létrehozott dátuma az árlista érvényességi időszakába esik.</span><span class="sxs-lookup"><span data-stu-id="2252c-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="2252c-116">Egyéni árazás a projektárajánlatoknál</span><span class="sxs-lookup"><span data-stu-id="2252c-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="2252c-117">A projektárajánlatoknál a projekt árazása kiindulhat az ügyféltől származó alapértelmezett standard árlistával, vagy a projektparaméterekből.</span><span class="sxs-lookup"><span data-stu-id="2252c-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="2252c-118">Ha egy adott árajánlaton belül egyéni árazásra van szüksége a projekthez kapcsolódó munkára vonatkozóan, akkor a projektárlistákhoz társított entitásból kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="2252c-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="2252c-119">Hajtsa végre az alábbi lépéseket az árajánlat-specifikus projektek árazásának beállításához.</span><span class="sxs-lookup"><span data-stu-id="2252c-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="2252c-120">Nyissa meg a projektárajánlatot, és válassza ki a **projektárlisták** lapot.</span><span class="sxs-lookup"><span data-stu-id="2252c-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="2252c-121">Az alrácsban válassza az **Egyéni árképzés létrehozása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2252c-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="2252c-122">Az árajánlathoz csatolt összes projektárlistát az program az új árlisták listájába másolja.</span><span class="sxs-lookup"><span data-stu-id="2252c-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="2252c-123">Az új árlisták neve tükrözi az árajánlat nevét, amely a dátum- és időbélyegzőt tartalmazza az árlisták létrehozásának időpontjával.</span><span class="sxs-lookup"><span data-stu-id="2252c-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="2252c-124">Használhatja ezeket az árlistákat, és frissítheti a munka (szerepkörár) és költség (kategória ára) árait.</span><span class="sxs-lookup"><span data-stu-id="2252c-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="2252c-125">Ezek az árak csak erre a projektárajánlatra vonatkoznak.</span><span class="sxs-lookup"><span data-stu-id="2252c-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="2252c-126">Projektszerződés árlistái</span><span class="sxs-lookup"><span data-stu-id="2252c-126">Price lists on a project contract</span></span>

<span data-ttu-id="2252c-127">A Projektszerződésekben a projektek árazása mindig alapértelmezés szerint egyéni árlistaként szerepel a szerződés nevével és a létrehozott dátum- és időbélyegzővel, amelyet a rendszer a névhez fűzött.</span><span class="sxs-lookup"><span data-stu-id="2252c-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="2252c-128">Ez akkor is igaz, ha a szerződés az árajánlat megnyerése után jött létre, vagy ha a szerződés a semmiből jött létre.</span><span class="sxs-lookup"><span data-stu-id="2252c-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="2252c-129">Ha szükséges, eltávolíthatja ezt a társítást az egyéni árlistához, és ehelyett társíthat egy normál árlistát a projektszerződéshez.</span><span class="sxs-lookup"><span data-stu-id="2252c-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="2252c-130">Ha normál árlistát rendel az árajánlathoz vagy a szerződéshez tartozó projektárlistákhoz, akkor az árlista árain végrehajtott változtatások hatással vannak az árlistát használó összes ajánlatra és szerződésre.</span><span class="sxs-lookup"><span data-stu-id="2252c-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>
