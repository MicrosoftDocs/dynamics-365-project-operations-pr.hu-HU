---
title: Projektfázisok
description: Ez a témakör a Microsoft Dynamics Project Operations projektszakaszairól nyújt információt.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a5c695e0cd39f8a222e719cc6c9ffe984fe80b07
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286791"
---
# <a name="project-stages"></a><span data-ttu-id="fa407-103">Projektfázisok</span><span class="sxs-lookup"><span data-stu-id="fa407-103">Project stages</span></span>

<span data-ttu-id="fa407-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="fa407-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fa407-105">Az Projekt szakaszainak célja, hogy tükrözzék a projekt előrehaladásának állapotát.</span><span class="sxs-lookup"><span data-stu-id="fa407-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="fa407-106">A testreszabások segítségével automatikusan frissítheti a fázisokat az üzleti folyamatok, a Power Automate, illetve a beépülőmodul-bővítmények használatával.</span><span class="sxs-lookup"><span data-stu-id="fa407-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="fa407-107">Az alapértelmezett üzleti folyamat a következő szakaszokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="fa407-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="fa407-108">Új</span><span class="sxs-lookup"><span data-stu-id="fa407-108">New</span></span>
- <span data-ttu-id="fa407-109">Ajánlat</span><span class="sxs-lookup"><span data-stu-id="fa407-109">Quote</span></span>
- <span data-ttu-id="fa407-110">Csomag</span><span class="sxs-lookup"><span data-stu-id="fa407-110">Plan</span></span>
- <span data-ttu-id="fa407-111">Kiszállítás</span><span class="sxs-lookup"><span data-stu-id="fa407-111">Deliver</span></span>
- <span data-ttu-id="fa407-112">Befejeződött</span><span class="sxs-lookup"><span data-stu-id="fa407-112">Complete</span></span>
- <span data-ttu-id="fa407-113">Bezárás</span><span class="sxs-lookup"><span data-stu-id="fa407-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="fa407-114">Új</span><span class="sxs-lookup"><span data-stu-id="fa407-114">New</span></span>

<span data-ttu-id="fa407-115">Amikor létrehoz egy projektet, a projekt állapotát **Új**-ra állítja.</span><span class="sxs-lookup"><span data-stu-id="fa407-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="fa407-116">Ha a projektet sablonból hozták létre, akkor lehet, hogy van ütemezése, becslése és a csapat adatai.</span><span class="sxs-lookup"><span data-stu-id="fa407-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="fa407-117">Egyébként ez a projekt vázlata, és a fennmaradó komponenseket be kell adni.</span><span class="sxs-lookup"><span data-stu-id="fa407-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="fa407-118">Ajánlat</span><span class="sxs-lookup"><span data-stu-id="fa407-118">Quote</span></span>

<span data-ttu-id="fa407-119">Ha egy projektet árajánlattal társít, vagy amikor projektet árajánlatból készít, akkor a projekt állapotát **Árajánlat**-ra állítja , és a becsült kezdési és befejezési dátumot frissítik.</span><span class="sxs-lookup"><span data-stu-id="fa407-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="fa407-120">Amíg a projekt **Ajánlat** szakaszban van, az **Értékesítés** lap a **Projektentitás** oldalon az árajánlat részleteit mutatja.</span><span class="sxs-lookup"><span data-stu-id="fa407-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="fa407-121">Terv</span><span class="sxs-lookup"><span data-stu-id="fa407-121">Plan</span></span>

<span data-ttu-id="fa407-122">Ha nyer egy projekthez társított ajánlatot, és a projektet a **Szerződés** szakaszba váltják, a projekt szakasza **Terv**-re frissül.</span><span class="sxs-lookup"><span data-stu-id="fa407-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="fa407-123">Amíg a projekt a **Terv** szakaszban van, a **Projektentitás** oldal a szerződés részleteit mutatja.</span><span class="sxs-lookup"><span data-stu-id="fa407-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="fa407-124">Kiszállítás</span><span class="sxs-lookup"><span data-stu-id="fa407-124">Deliver</span></span>

<span data-ttu-id="fa407-125">Amikor a projektterv elkészült, és készen áll a projekt elindítására, a projektmenedzsernek frissítenie kell a projekt szakaszát a **Teljesítés** elemre, hogy megmutatja, hogy a projekt elindult.</span><span class="sxs-lookup"><span data-stu-id="fa407-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="fa407-126">Teljes</span><span class="sxs-lookup"><span data-stu-id="fa407-126">Complete</span></span> 

<span data-ttu-id="fa407-127">Amikor a projekt munkája befejeződött, a projektmenedzser frissítheti a szakaszt a **Kész** értékre.</span><span class="sxs-lookup"><span data-stu-id="fa407-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="fa407-128">A projekt szakaszának a **Teljes** értékre történő frissítésével a projektmenedzser kijelenti , hogy a munka 100%-ban befejeződött, de a projektet nyitva tartják, hogy minden függőben lévő idő- vagy költségbejegyzés rögzíthető legyen.</span><span class="sxs-lookup"><span data-stu-id="fa407-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="fa407-129">Bezárás</span><span class="sxs-lookup"><span data-stu-id="fa407-129">Close</span></span>

<span data-ttu-id="fa407-130">Amikor az összes tranzakciót rögzítik a projektnél, a projektmenedzser frissítheti a szakaszt a **Bezárás** értékre.</span><span class="sxs-lookup"><span data-stu-id="fa407-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="fa407-131">Ezen a ponton nem lehet tranzakciókat rögzíteni, és a projektet csak olvashatóvá állítják be.</span><span class="sxs-lookup"><span data-stu-id="fa407-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]