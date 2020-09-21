---
title: A projekt szakaszai
description: Ez a témakör információkat nyújt a projekt szakaszairól.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752200"
---
# <a name="project-stages"></a><span data-ttu-id="9ecb3-103">A projekt szakaszai</span><span class="sxs-lookup"><span data-stu-id="9ecb3-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9ecb3-104">A Projekt szakaszai frissítésre kerülnek, hogy tükrözzék a projekt előrehaladásának állapotát.</span><span class="sxs-lookup"><span data-stu-id="9ecb3-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="9ecb3-105">Az alapértelmezett üzleti folyamat automatikusan frissíti a projekt egyes szakaszait, míg másokat a projektmenedzser manuálisan frissít.</span><span class="sxs-lookup"><span data-stu-id="9ecb3-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="9ecb3-106">Az alapértelmezett BPF a következő szakaszokat határozza meg:</span><span class="sxs-lookup"><span data-stu-id="9ecb3-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="9ecb3-107">Új</span><span class="sxs-lookup"><span data-stu-id="9ecb3-107">New</span></span>
- <span data-ttu-id="9ecb3-108">Ajánlat</span><span class="sxs-lookup"><span data-stu-id="9ecb3-108">Quote</span></span>
- <span data-ttu-id="9ecb3-109">Terv</span><span class="sxs-lookup"><span data-stu-id="9ecb3-109">Plan</span></span>
- <span data-ttu-id="9ecb3-110">Kiszállítás</span><span class="sxs-lookup"><span data-stu-id="9ecb3-110">Deliver</span></span>
- <span data-ttu-id="9ecb3-111">Teljes</span><span class="sxs-lookup"><span data-stu-id="9ecb3-111">Complete</span></span>
- <span data-ttu-id="9ecb3-112">Bezárás</span><span class="sxs-lookup"><span data-stu-id="9ecb3-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="9ecb3-113">Új</span><span class="sxs-lookup"><span data-stu-id="9ecb3-113">New</span></span>

<span data-ttu-id="9ecb3-114">Amikor létrehoz egy projektet, a projekt állapotát **Új**-ra állítja.</span><span class="sxs-lookup"><span data-stu-id="9ecb3-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="9ecb3-115">Ha a projektet sablonból hozták létre, akkor lehet, hogy van ütemezése, becslése és a csapat adatai.</span><span class="sxs-lookup"><span data-stu-id="9ecb3-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="9ecb3-116">Egyébként ez csak a projekt vázlata, és a fennmaradó komponenseket be kell adni.</span><span class="sxs-lookup"><span data-stu-id="9ecb3-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="9ecb3-117">Ajánlat</span><span class="sxs-lookup"><span data-stu-id="9ecb3-117">Quote</span></span>

<span data-ttu-id="9ecb3-118">Ha egy projektet árajánlattal társít, vagy amikor projektet árajánlatból készít, akkor a projekt állapotát **Árajánlat**-ra állítja , és a becsült kezdési és befejezési dátumot frissítik.</span><span class="sxs-lookup"><span data-stu-id="9ecb3-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="9ecb3-119">Amíg a projekt **Ajánlat** szakaszban van, az **Értékesítés** lap a **Projektentitás** oldalon az árajánlat részleteit mutatja.</span><span class="sxs-lookup"><span data-stu-id="9ecb3-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="9ecb3-120">Terv</span><span class="sxs-lookup"><span data-stu-id="9ecb3-120">Plan</span></span>

<span data-ttu-id="9ecb3-121">Ha nyer egy projekthez társított ajánlatot, és a projektet a **Szerződés** szakaszba váltják, a projekt szakasza **Terv**-re frissül.</span><span class="sxs-lookup"><span data-stu-id="9ecb3-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="9ecb3-122">Amíg a projekt a **Terv** szakaszban van, a **Projektentitás** oldal a szerződés részleteit mutatja.</span><span class="sxs-lookup"><span data-stu-id="9ecb3-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="9ecb3-123">Kiszállítás</span><span class="sxs-lookup"><span data-stu-id="9ecb3-123">Deliver</span></span>

<span data-ttu-id="9ecb3-124">Amikor a projektterv elkészült, és készen áll a projekt elindítására, a projektmenedzsernek frissítenie kell a projekt szakaszát a **Teljesítés** elemre, hogy megmutatja, hogy a projekt elindult.</span><span class="sxs-lookup"><span data-stu-id="9ecb3-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="9ecb3-125">Teljes</span><span class="sxs-lookup"><span data-stu-id="9ecb3-125">Complete</span></span> 

<span data-ttu-id="9ecb3-126">Amikor a projekt munkája befejeződött, a projektmenedzser frissítheti a szakaszt a **Kész** értékre.</span><span class="sxs-lookup"><span data-stu-id="9ecb3-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="9ecb3-127">A projekt szakaszának a **Teljes** értékre történő frissítésével a projektmenedzser kijelenti , hogy a munka 100%-ban befejeződött, de a projektet nyitva tartják, hogy minden függőben lévő idő- vagy költségbejegyzés rögzíthető legyen.</span><span class="sxs-lookup"><span data-stu-id="9ecb3-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="9ecb3-128">Bezárás</span><span class="sxs-lookup"><span data-stu-id="9ecb3-128">Close</span></span>

<span data-ttu-id="9ecb3-129">Amikor az összes tranzakciót rögzítik a projektnél, a projektmenedzser frissítheti a szakaszt a **Bezárás** értékre.</span><span class="sxs-lookup"><span data-stu-id="9ecb3-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="9ecb3-130">Ezen a ponton nem lehet tranzakciókat rögzíteni, és a projektet csak olvashatóvá állítják be.</span><span class="sxs-lookup"><span data-stu-id="9ecb3-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
