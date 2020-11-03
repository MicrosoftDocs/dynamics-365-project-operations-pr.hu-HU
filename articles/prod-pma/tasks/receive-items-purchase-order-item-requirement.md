---
title: Cikkek bevételezése a cikkszükségletből származó beszerzési rendelésen
description: Ez a témakör ismerteti, hogyan lehet cikkeket bevételezni egy cikkszükségletből származó beszerzési rendelésen.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078259"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="9f0bf-103">Cikkek bevételezése a cikkszükségletből származó beszerzési rendelésen</span><span class="sxs-lookup"><span data-stu-id="9f0bf-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9f0bf-104">Ez a témakör ismerteti, hogyan lehet cikkeket bevételezni egy cikkszükségletből származó beszerzési rendelésen.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="9f0bf-105">Cikktranzakció helyett egy cikkszükségletet használva megtervezheti a szállítást éppen a cikk tényleges felhasználása előtt, létrehozhat egy beszerzési rendelést, belefoglalhatja a cikket egy megállapodási keretrendszerbe, és belefoglalhatja a cikkszükségletet a gyártási tervezésbe.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="9f0bf-106">Ez a feladat a USSI adatkészletet használja.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="9f0bf-107">Az ablaktáblában kattintson a **Modulok > Projektvezetés és könyvelés > Projektek > Minden projekt** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="9f0bf-108">A listában válassza ki a hivatkozást a kívánt sorban.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="9f0bf-109">A Művelet panelen válassza a **Terv** elemet.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="9f0bf-110">Válassza a **Cikkszükségletek** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="9f0bf-111">Válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-111">Select **New**.</span></span>
6. <span data-ttu-id="9f0bf-112">Az új sorban adjon meg vagy jelöljön ki egy értéket a **Cikkszám** mezőben.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="9f0bf-113">Írjon be egy számot a **Mennyiség** mezőbe.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="9f0bf-114">Válassza a **Mentés** parancsot.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-114">Select **Save**.</span></span>
9. <span data-ttu-id="9f0bf-115">A Művelet panelen válassza a **Kezelés** elemet.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="9f0bf-116">Válassza a **Funkciók** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-116">Select **Functions**.</span></span>
11. <span data-ttu-id="9f0bf-117">Válassza a **Megrendelés létrehozása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="9f0bf-118">Kattintson az **Összes belefoglalása** jelölőnégyzetre.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="9f0bf-119">Adjon meg vagy jelöljön ki egy értéket a **Partnerfiók** mezőben.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="9f0bf-120">Kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-120">Select **OK**.</span></span>
15. <span data-ttu-id="9f0bf-121">A Navigáció ablaktáblán nyissa meg a következőt: **Modulok > Kötelezettségek > Megrendelések > Minden megrendelés**.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="9f0bf-122">A listában válassza ki a hivatkozást a kívánt sorban.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="9f0bf-123">A Művelet panelen válassza a **Beszerzés** elemet.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="9f0bf-124">Válassza a **Megerősítés** elemet.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="9f0bf-125">A Művelet panelen válassza a **Bevételezés** elemet.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="9f0bf-126">Válassza a **Termékbizonylat** elemet.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="9f0bf-127">A **Termékbizonylat** mezőbe írjon be egy értéket.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="9f0bf-128">Kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="9f0bf-128">Select **OK**.</span></span>

