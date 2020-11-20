---
title: Projektfázistípusok
description: Ez a témakör információkat nyújt a projekt szakaszairól.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: aa423979a794b07a8bd27440f47a29480b74b518
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123061"
---
# <a name="project-stage-types"></a><span data-ttu-id="d7853-103">Projektfázistípusok</span><span class="sxs-lookup"><span data-stu-id="d7853-103">Project stage types</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d7853-104">Az Projekt szakaszainak célja, hogy tükrözzék a projekt előrehaladásának állapotát.</span><span class="sxs-lookup"><span data-stu-id="d7853-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="d7853-105">A testreszabások segítségével automatikusan frissítheti a fázisokat az üzleti folyamatok, a Power Automate, illetve a beépülőmodul-bővítmények használatával.</span><span class="sxs-lookup"><span data-stu-id="d7853-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="d7853-106">Az alapértelmezett BPF a következő szakaszokat határozza meg:</span><span class="sxs-lookup"><span data-stu-id="d7853-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="d7853-107">Új</span><span class="sxs-lookup"><span data-stu-id="d7853-107">New</span></span>
- <span data-ttu-id="d7853-108">Ajánlat</span><span class="sxs-lookup"><span data-stu-id="d7853-108">Quote</span></span>
- <span data-ttu-id="d7853-109">Terv</span><span class="sxs-lookup"><span data-stu-id="d7853-109">Plan</span></span>
- <span data-ttu-id="d7853-110">Kiszállítás</span><span class="sxs-lookup"><span data-stu-id="d7853-110">Deliver</span></span>
- <span data-ttu-id="d7853-111">Teljes</span><span class="sxs-lookup"><span data-stu-id="d7853-111">Complete</span></span>
- <span data-ttu-id="d7853-112">Bezárás</span><span class="sxs-lookup"><span data-stu-id="d7853-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="d7853-113">Új</span><span class="sxs-lookup"><span data-stu-id="d7853-113">New</span></span>

<span data-ttu-id="d7853-114">Amikor létrehoz egy projektet, a projekt állapotát **Új**-ra állítja.</span><span class="sxs-lookup"><span data-stu-id="d7853-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="d7853-115">Ha a projektet sablonból hozták létre, akkor lehet, hogy van ütemezése, becslése és a csapat adatai.</span><span class="sxs-lookup"><span data-stu-id="d7853-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="d7853-116">Egyébként ez csak a projekt vázlata, és a fennmaradó komponenseket be kell adni.</span><span class="sxs-lookup"><span data-stu-id="d7853-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="d7853-117">Ajánlat</span><span class="sxs-lookup"><span data-stu-id="d7853-117">Quote</span></span>

<span data-ttu-id="d7853-118">Ha egy projektet árajánlattal társít, vagy amikor projektet árajánlatból készít, akkor a projekt állapotát **Árajánlat**-ra állítja , és a becsült kezdési és befejezési dátumot frissítik.</span><span class="sxs-lookup"><span data-stu-id="d7853-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="d7853-119">Amíg a projekt **Ajánlat** szakaszban van, az **Értékesítés** lap a **Projektentitás** oldalon az árajánlat részleteit mutatja.</span><span class="sxs-lookup"><span data-stu-id="d7853-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="d7853-120">Terv</span><span class="sxs-lookup"><span data-stu-id="d7853-120">Plan</span></span>

<span data-ttu-id="d7853-121">Ha nyer egy projekthez társított ajánlatot, és a projektet a **Szerződés** szakaszba váltják, a projekt szakasza **Terv**-re frissül.</span><span class="sxs-lookup"><span data-stu-id="d7853-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="d7853-122">Amíg a projekt a **Terv** szakaszban van, a **Projektentitás** oldal a szerződés részleteit mutatja.</span><span class="sxs-lookup"><span data-stu-id="d7853-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="d7853-123">Kiszállítás</span><span class="sxs-lookup"><span data-stu-id="d7853-123">Deliver</span></span>

<span data-ttu-id="d7853-124">Amikor a projektterv elkészült, és készen áll a projekt elindítására, a projektmenedzsernek frissítenie kell a projekt szakaszát a **Teljesítés** elemre, hogy megmutatja, hogy a projekt elindult.</span><span class="sxs-lookup"><span data-stu-id="d7853-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="d7853-125">Teljes</span><span class="sxs-lookup"><span data-stu-id="d7853-125">Complete</span></span> 

<span data-ttu-id="d7853-126">Amikor a projekt munkája befejeződött, a projektmenedzser frissítheti a szakaszt a **Kész** értékre.</span><span class="sxs-lookup"><span data-stu-id="d7853-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="d7853-127">A projekt szakaszának a **Teljes** értékre történő frissítésével a projektmenedzser kijelenti , hogy a munka 100%-ban befejeződött, de a projektet nyitva tartják, hogy minden függőben lévő idő- vagy költségbejegyzés rögzíthető legyen.</span><span class="sxs-lookup"><span data-stu-id="d7853-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="d7853-128">Bezárás</span><span class="sxs-lookup"><span data-stu-id="d7853-128">Close</span></span>

<span data-ttu-id="d7853-129">Amikor az összes tranzakciót rögzítik a projektnél, a projektmenedzser frissítheti a szakaszt a **Bezárás** értékre.</span><span class="sxs-lookup"><span data-stu-id="d7853-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="d7853-130">Ezen a ponton nem lehet tranzakciókat rögzíteni, és a projektet csak olvashatóvá állítják be.</span><span class="sxs-lookup"><span data-stu-id="d7853-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
