---
title: Képességek és jártasságok meghatározása
description: Ez a témakör az erőforrások értékelésére szolgáló jártassági modellek beállításáról nyújt információkat.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: d1ef50a3aa297ef439b54d37de629414ca66c820
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279681"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="2891e-103">Képességek és jártasságok meghatározása</span><span class="sxs-lookup"><span data-stu-id="2891e-103">Define skills and proficiencies</span></span>

<span data-ttu-id="2891e-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="2891e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2891e-105">A készségek olyan erőforrás-jellemzők, amelyek jelen vannak a Dynamics 365 Project Operations és ha van, a Dynamics 365 Field Service rendszerben is.</span><span class="sxs-lookup"><span data-stu-id="2891e-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="2891e-106">A Project Operations készségeinek karbantartásához lépjen az **Erőforrások** \> **Erőforrás-készségek** részre.</span><span class="sxs-lookup"><span data-stu-id="2891e-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="2891e-107">Használjon jártassági modelleket az erőforrások értékeléséhez</span><span class="sxs-lookup"><span data-stu-id="2891e-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="2891e-108">Az erőforrás-készségeket a jártassági modellek osztályozzák.</span><span class="sxs-lookup"><span data-stu-id="2891e-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="2891e-109">Az egyes értékelések jártassági modellben vannak.</span><span class="sxs-lookup"><span data-stu-id="2891e-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="2891e-110">Jártassági modell létrehozásához lépjen a **Erőforrások** \> **Jóléti modellek** elemre , majd válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2891e-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="2891e-111">Az új besorolási modellben adja meg a minimális besorolási értéket, a maximális besorolási értéket és az osztályozandó entitást.</span><span class="sxs-lookup"><span data-stu-id="2891e-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="2891e-112">Az **Értékelési értékek** alrácson meghatározhatja a különböző minősítési értékeket, a minimumtól a maximumig.</span><span class="sxs-lookup"><span data-stu-id="2891e-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="2891e-113">Ezek a minősítési értékek megjelennek az **Erőforrásigény**, **Ütemezési tábla** és **Ütemezési asszisztens** szűrőkön.</span><span class="sxs-lookup"><span data-stu-id="2891e-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]