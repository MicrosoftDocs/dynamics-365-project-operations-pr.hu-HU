---
title: Árlisták inaktiválása
description: Ez témakör ismerteti a fel nem használt vagy régi árlisták inaktiválását vagy eltávolítását.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701940"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="89132-103">Árlisták inaktiválása</span><span class="sxs-lookup"><span data-stu-id="89132-103">Deactivate price lists</span></span> 

<span data-ttu-id="89132-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="89132-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="89132-105">A régi vagy nem használt árlisták Dynamics 365 Project Operations-ből törénő eltávolításához két lépést kell tennie.</span><span class="sxs-lookup"><span data-stu-id="89132-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="89132-106">Az árlista eltávolítása vagy törlése az adott oldalakról.</span><span class="sxs-lookup"><span data-stu-id="89132-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="89132-107">Inaktiválja vagy törölje az árlistát az **Árlisták** lap Aktív árlistáiból.</span><span class="sxs-lookup"><span data-stu-id="89132-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="89132-108">Az árlista teljes eltávolításához mindkét lépést végre kell hajtania.</span><span class="sxs-lookup"><span data-stu-id="89132-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="89132-109">Csak a 2. lépés végrehajtása – azaz az árlista Akítv árlisták nézetéből való közvetlen törlése vagy inaktiválása – nem elegendő.</span><span class="sxs-lookup"><span data-stu-id="89132-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="89132-110">Az árlista hozzárendelését is törölnie kell az 1. lépésben említett összes helyről.</span><span class="sxs-lookup"><span data-stu-id="89132-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="89132-111">Az árlista törlése az adott oldalakról</span><span class="sxs-lookup"><span data-stu-id="89132-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="89132-112">Ha árlistát szeretne törölni a Project Operations alkalmazásból, akkor nyissa meg az alábbi oldalakat:</span><span class="sxs-lookup"><span data-stu-id="89132-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="89132-113">**Projektparaméterek** oldal > **Árlisták** fül</span><span class="sxs-lookup"><span data-stu-id="89132-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="89132-114">**Szervezeti egység** lap > **Árlisták** rács</span><span class="sxs-lookup"><span data-stu-id="89132-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="89132-115">**Partner** oldal > **Projektárlisták** rács</span><span class="sxs-lookup"><span data-stu-id="89132-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="89132-116">**Projektárajánlatok** lap > **Projektárlisták** rács: Ez az összes aktív projektárajánlatra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="89132-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="89132-117">**Projektszerződések** lap > **Projektárlisták** rács: Ez az összes aktív projektszerződésre vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="89132-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="89132-118">Minden oldalhoz ki kell választania a törölni kívánt árlistát, majd a **Törlés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="89132-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="89132-119">Törölje vagy inaktiváljs az árlistát az Árlisták oldalról</span><span class="sxs-lookup"><span data-stu-id="89132-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="89132-120">Ha törölni szeretne egy árlistát az aktív árlistákból, menjen az **Értékesítés** > **Ügyfelek** > **Árlisták** lapra.</span><span class="sxs-lookup"><span data-stu-id="89132-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="89132-121">Válassza ki a törölni kívánt árlistákat, majd kattintson a **Törlés** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="89132-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="89132-122">Ha az árlista bármely meglévő tranzakcióra hivatkozik, akkor nem fogja tudni törölni.</span><span class="sxs-lookup"><span data-stu-id="89132-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="89132-123">Ha ez történik, inaktiválhatja az árlistát, hogy az ne jelenjen meg egyetlen nézetben sem.</span><span class="sxs-lookup"><span data-stu-id="89132-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="89132-124">Az árlista inaktiválásához jelölje ki újra az árlistát, majd válassza az **Inaktiválás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="89132-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
