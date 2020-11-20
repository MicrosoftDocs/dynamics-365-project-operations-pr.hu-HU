---
title: Készség- és jártassági modellek
description: Ez a témakör a készségek és a jártassági modellek használatáról nyújt információkat.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 92735262ebc4b48dd1143af57349d77e1fe3061c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124191"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="02de0-103">Készség- és jártassági modellek</span><span class="sxs-lookup"><span data-stu-id="02de0-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="02de0-104">A készségek olyan erőforrás-jellemzők, amelyek jelen vannak a Dynamics 365 Project Service Automation és ha van, a Dynamics 365 Field Service rendszerben is.</span><span class="sxs-lookup"><span data-stu-id="02de0-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="02de0-105">A Project Service Automation készségeinek tárolásához menjen az **Erőforrások** \> **Erőforrás-készségek** oldalra.</span><span class="sxs-lookup"><span data-stu-id="02de0-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Erőforrás képességei](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="02de0-107">Használjon jártassági modelleket az erőforrások értékeléséhez</span><span class="sxs-lookup"><span data-stu-id="02de0-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="02de0-108">Az erőforrás-készségeket a jártassági modellek osztályozzák.</span><span class="sxs-lookup"><span data-stu-id="02de0-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="02de0-109">Az egyes értékelések jártassági modellben vannak.</span><span class="sxs-lookup"><span data-stu-id="02de0-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="02de0-110">Jártassági modell létrehozásához lépjen a **Erőforrások** \> **Jóléti modellek** elemre , majd válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="02de0-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="02de0-111">Az új besorolási modellben adja meg a minimális besorolási értéket, a maximális besorolási értéket és az osztályozandó entitást.</span><span class="sxs-lookup"><span data-stu-id="02de0-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="02de0-112">Az **Értékelési értékek** alrácson meghatározhatja a különböző minősítési értékeket, a minimumtól a maximumig.</span><span class="sxs-lookup"><span data-stu-id="02de0-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Meghatározott minimális és maximális besorolás](media/Resource-Management-image85.png)

<span data-ttu-id="02de0-114">Ezek a minősítési értékek megjelennek az **Erőforrásigény**, **Ütemezési tábla** és **Ütemezési asszisztens** szűrőkön.</span><span class="sxs-lookup"><span data-stu-id="02de0-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
