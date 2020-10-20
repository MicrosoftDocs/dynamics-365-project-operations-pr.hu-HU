---
title: Terjesztések egy költségjelentésen
description: Ha kiadásokat ad meg egy költségjelentésen, akkor a szervezeten belül eloszthatja őket több projekt, jogi entitás vagy partner között.
author: suvaidya
manager: AnnBe
ms.date: 10/10/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a1fa7383e7715fe57380de0a006ccc4e020bb5a5
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908220"
---
# <a name="distributions-on-an-expense-report"></a><span data-ttu-id="1d7f5-103">Terjesztések egy költségjelentésen</span><span class="sxs-lookup"><span data-stu-id="1d7f5-103">Distributions on an expense report</span></span>

<span data-ttu-id="1d7f5-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="1d7f5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1d7f5-105">Ha kiadásokat ad meg egy költségjelentésen, akkor a szervezeten belül eloszthatja őket több projekt, pénzügyi részleg vagy partner között.</span><span class="sxs-lookup"><span data-stu-id="1d7f5-105">When you enter expenses on an expense report, you can distribute them across multiple projects, financial dimensions, or accounts in your organization.</span></span>

<span data-ttu-id="1d7f5-106">Például Nancy, a Fabrikam értékesítési képviselője Koppenhágából Frankfurtba utazott.</span><span class="sxs-lookup"><span data-stu-id="1d7f5-106">For example, Nancy, a Fabrikam sales representative, traveled from Copenhagen to Frankfurt.</span></span> <span data-ttu-id="1d7f5-107">Nancy Frankfurtban találkozott két szervezettel, hogy különálló projekteket vitassanak meg az egyes szervezetekkel.</span><span class="sxs-lookup"><span data-stu-id="1d7f5-107">In Frankfurt, Nancy met with two organizations to discuss separate projects for each organization.</span></span> <span data-ttu-id="1d7f5-108">Nancy hét munkanapot töltött az A szervezettel dolgozva az A projekten, és három napot töltött a B szervezettel dolgozva a B projekten.</span><span class="sxs-lookup"><span data-stu-id="1d7f5-108">Nancy spent seven business days working with organization A on project A, and three business days working with organization B on project B.</span></span>

<span data-ttu-id="1d7f5-109">Mivel Nancy frankfurti tartózkodása alatt két külön projekten dolgozott, amikor belép a költségjelentésbe, az egyes projekteknek megfelelő módon osztja el a kiadásokat.</span><span class="sxs-lookup"><span data-stu-id="1d7f5-109">Because Nancy worked on two separate projects while was in Frankfurt, when she enters the expense report, Nancy distributes the expenses as appropriate for each project.</span></span> <span data-ttu-id="1d7f5-110">A következő táblázat azt mutatja be, hogyan osztja el Nancy a kiadásokat.</span><span class="sxs-lookup"><span data-stu-id="1d7f5-110">The following table shows how Nancy distributed the expenses.</span></span>

| <span data-ttu-id="1d7f5-111">Költségtípus</span><span class="sxs-lookup"><span data-stu-id="1d7f5-111">Expense type</span></span> | <span data-ttu-id="1d7f5-112">Kiadás teljes összege</span><span class="sxs-lookup"><span data-stu-id="1d7f5-112">Total expense amount</span></span> | <span data-ttu-id="1d7f5-113">A projekthez elosztott összeg</span><span class="sxs-lookup"><span data-stu-id="1d7f5-113">Amount distributed to project A</span></span> | <span data-ttu-id="1d7f5-114">B projekthez elosztott összeg</span><span class="sxs-lookup"><span data-stu-id="1d7f5-114">Amount distributed to project B</span></span> |
|--------------|----------------------|---------------------------------|---------------------------------|
| <span data-ttu-id="1d7f5-115">Vonat viteldíja</span><span class="sxs-lookup"><span data-stu-id="1d7f5-115">Train fare</span></span>   | <span data-ttu-id="1d7f5-116">578 DKK</span><span class="sxs-lookup"><span data-stu-id="1d7f5-116">DKK 578</span></span>              | <span data-ttu-id="1d7f5-117">405 DKK</span><span class="sxs-lookup"><span data-stu-id="1d7f5-117">DKK 405</span></span>                         | <span data-ttu-id="1d7f5-118">173 DKK</span><span class="sxs-lookup"><span data-stu-id="1d7f5-118">DKK 173</span></span>                         |
| <span data-ttu-id="1d7f5-119">Szálloda</span><span class="sxs-lookup"><span data-stu-id="1d7f5-119">Hotel</span></span>        | <span data-ttu-id="1d7f5-120">725 EUR</span><span class="sxs-lookup"><span data-stu-id="1d7f5-120">EUR 725</span></span>              | <span data-ttu-id="1d7f5-121">557 EUR</span><span class="sxs-lookup"><span data-stu-id="1d7f5-121">EUR 557</span></span>                         | <span data-ttu-id="1d7f5-122">168 EUR</span><span class="sxs-lookup"><span data-stu-id="1d7f5-122">EUR 168</span></span>                         |
| <span data-ttu-id="1d7f5-123">Étkezések</span><span class="sxs-lookup"><span data-stu-id="1d7f5-123">Meals</span></span>        | <span data-ttu-id="1d7f5-124">346 EUR</span><span class="sxs-lookup"><span data-stu-id="1d7f5-124">EUR 346</span></span>              | <span data-ttu-id="1d7f5-125">284 EUR</span><span class="sxs-lookup"><span data-stu-id="1d7f5-125">EUR 284</span></span>                         | <span data-ttu-id="1d7f5-126">62 EUR</span><span class="sxs-lookup"><span data-stu-id="1d7f5-126">EUR 62</span></span>                          |
