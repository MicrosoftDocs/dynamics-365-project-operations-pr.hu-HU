---
title: Projektszámla-javaslatok teljesítménye
description: Ez témakör a projektszámla-javaslatok teljesítményfejlesztéséről nyújt tájékoztatást.
author: Yowelle
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 78c924cba8107471a5f8e6d6a38265890d32d72b
ms.sourcegitcommit: 2350c6f3728067a8298adde640e6fdd5984eb077
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573562"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="08f89-103">Projektszámla-javaslatok teljesítménye</span><span class="sxs-lookup"><span data-stu-id="08f89-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="08f89-104">Új számlajavaslat létrehozásakor a projektek és alprojektek számának növekedésével teljesítményproblémák merülhetnek fel.</span><span class="sxs-lookup"><span data-stu-id="08f89-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="08f89-105">A teljesítmény javítása érdekében rendelkezésre áll egy funkció, amely csökkenti a könyvelt projekttranzakciókra vonatkozó új számlajavaslat létrehozásához szükséges időt.</span><span class="sxs-lookup"><span data-stu-id="08f89-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="08f89-106">Projektszámla-javaslatok teljesítményjavításának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="08f89-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="08f89-107">A projektszámla-javaslat teljesítményjavítási funkció engedélyezéséhez végezze el az alábbi lépéseket.</span><span class="sxs-lookup"><span data-stu-id="08f89-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="08f89-108">Menjen a **Funkciókezelés** > **Összes** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="08f89-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="08f89-109">A szolgáltatáslistában keresse meg a **Projektszámla-javaslatok teljesítményjavítása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="08f89-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="08f89-110">Válassza ki az **Engedélyezés most** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="08f89-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="08f89-111">Frissítse böngészőjét, majd hozzon létre egy új számlajavaslatot.</span><span class="sxs-lookup"><span data-stu-id="08f89-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="08f89-112">Projektszámla-javaslatok teljesítményjavításának kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="08f89-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="08f89-113">A projektszámla-javaslat teljesítményjavítási funkció kikapcsolásához végezze el az alábbi lépéseket.</span><span class="sxs-lookup"><span data-stu-id="08f89-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="08f89-114">Menjen a **Funkciókezelés** > **Összes** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="08f89-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="08f89-115">A szolgáltatáslistában keresse meg a **Projektszámla-javaslatok teljesítményjavítása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="08f89-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="08f89-116">Válassza ki a **Letiltás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="08f89-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="08f89-117">Frissítse a böngészőjét.</span><span class="sxs-lookup"><span data-stu-id="08f89-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="08f89-118">A számlajavaslat teljesítménye nem alkalmazható, ha a számlázási szabályok engedélyezve vannak, vagy ha a kötegelt folyamatok futnak.</span><span class="sxs-lookup"><span data-stu-id="08f89-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
