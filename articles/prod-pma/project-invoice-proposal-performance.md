---
title: Projektszámla-javaslatok teljesítménye
description: Ez témakör a projektszámla-javaslatok teljesítményfejlesztéséről nyújt tájékoztatást.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269793"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="53fef-103">Projektszámla-javaslatok teljesítménye</span><span class="sxs-lookup"><span data-stu-id="53fef-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53fef-104">Új számlajavaslat létrehozásakor a projektek és alprojektek számának növekedésével teljesítményproblémák merülhetnek fel.</span><span class="sxs-lookup"><span data-stu-id="53fef-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="53fef-105">A teljesítmény javítása érdekében rendelkezésre áll egy funkció, amely csökkenti a könyvelt projekttranzakciókra vonatkozó új számlajavaslat létrehozásához szükséges időt.</span><span class="sxs-lookup"><span data-stu-id="53fef-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="53fef-106">Projektszámla-javaslatok teljesítményjavításának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="53fef-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="53fef-107">A projektszámla-javaslat teljesítményjavítási funkció engedélyezéséhez végezze el az alábbi lépéseket.</span><span class="sxs-lookup"><span data-stu-id="53fef-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="53fef-108">Menjen a **Funkciókezelés** > **Összes** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="53fef-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="53fef-109">A szolgáltatáslistában keresse meg a **Projektszámla-javaslatok teljesítményjavítása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="53fef-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="53fef-110">Válassza ki az **Engedélyezés most** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="53fef-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="53fef-111">Frissítse böngészőjét, majd hozzon létre egy új számlajavaslatot.</span><span class="sxs-lookup"><span data-stu-id="53fef-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="53fef-112">Projektszámla-javaslatok teljesítményjavításának kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="53fef-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="53fef-113">A projektszámla-javaslat teljesítményjavítási funkció kikapcsolásához végezze el az alábbi lépéseket.</span><span class="sxs-lookup"><span data-stu-id="53fef-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="53fef-114">Menjen a **Funkciókezelés** > **Összes** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="53fef-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="53fef-115">A szolgáltatáslistában keresse meg a **Projektszámla-javaslatok teljesítményjavítása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="53fef-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="53fef-116">Válassza ki a **Letiltás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="53fef-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="53fef-117">Frissítse a böngészőjét.</span><span class="sxs-lookup"><span data-stu-id="53fef-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="53fef-118">A számlajavaslat teljesítménye nem alkalmazható a számlázási szabályok engedélyezésekor.</span><span class="sxs-lookup"><span data-stu-id="53fef-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="53fef-119">A számlajavaslatok léterhozásának folyamata során az alfeladatok száma a számlázható tranzakciókkal rendelkező szerződések számától függően maximális számra osztja fel a feladatokat, függetlenül attól, hogy mit adott meg.</span><span class="sxs-lookup"><span data-stu-id="53fef-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="53fef-120">Ha például **3**-as számot adja meg a számlajavaslat kötegben való létrehozásához szükséges alfeladatokhoz, és csak két olyan szerződés van, amely számlázható tranzakciókat tartalmaz, csak két alfeladat jön létre.</span><span class="sxs-lookup"><span data-stu-id="53fef-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
