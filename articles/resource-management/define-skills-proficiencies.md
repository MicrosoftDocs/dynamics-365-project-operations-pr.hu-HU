---
title: Képességek és jártasságok meghatározása
description: Ez a témakör az erőforrások értékelésére szolgáló jártassági modellek beállításáról nyújt információkat.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 24538ed1d610a0cae4c2badc0fd33c2f738a8338
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078036"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="6901e-103">Képességek és jártasságok meghatározása</span><span class="sxs-lookup"><span data-stu-id="6901e-103">Define skills and proficiencies</span></span>

<span data-ttu-id="6901e-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="6901e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6901e-105">A készségek a Dynamics 365 Project Operations és – ha jelen van – a Dynamics 365 Field Service között megosztott erőforrás-jellemzők.</span><span class="sxs-lookup"><span data-stu-id="6901e-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="6901e-106">A Project Operations készségeinek karbantartásához lépjen az **Erőforrások** \> **Erőforrás-készségek** részre.</span><span class="sxs-lookup"><span data-stu-id="6901e-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="6901e-107">Használjon jártassági modelleket az erőforrások értékeléséhez</span><span class="sxs-lookup"><span data-stu-id="6901e-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="6901e-108">Az erőforrás-készségeket a jártassági modellek osztályozzák.</span><span class="sxs-lookup"><span data-stu-id="6901e-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="6901e-109">Az egyes értékelések jártassági modellben vannak.</span><span class="sxs-lookup"><span data-stu-id="6901e-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="6901e-110">Jártassági modell létrehozásához lépjen a **Erőforrások** \> **Jóléti modellek** elemre , majd válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="6901e-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="6901e-111">Az új besorolási modellben adja meg a minimális besorolási értéket, a maximális besorolási értéket és az osztályozandó entitást.</span><span class="sxs-lookup"><span data-stu-id="6901e-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="6901e-112">Az **Értékelési értékek** alhálózatban meghatározhatja a különböző minősítési értékeket, a minimumtól a maximumig.</span><span class="sxs-lookup"><span data-stu-id="6901e-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="6901e-113">Ezek a minősítési értékek megjelennek az **Erőforrásigény** , **Ütemezési tábla** és **Ütemezési asszisztens** szűrőkön.</span><span class="sxs-lookup"><span data-stu-id="6901e-113">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>
