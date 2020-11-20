---
title: Projekt frissítése
description: Ez a témakör a projektek Project Operationsben való frissítéséről nyújt tájékoztatást.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8bcbc6c5a62d252398d541649647fbad49006a0c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131436"
---
# <a name="update-a-project"></a><span data-ttu-id="8f8f5-103">Projekt frissítése</span><span class="sxs-lookup"><span data-stu-id="8f8f5-103">Update a project</span></span>

<span data-ttu-id="8f8f5-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="8f8f5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8f8f5-105">Az alábbiakban található egy összefoglaló a mezőkről, amelyek a létrehozást követően frissíthetők a projekten, és a frissítésre vonatkozó esetleges következmények.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="8f8f5-106">Projekt részletei mezők</span><span class="sxs-lookup"><span data-stu-id="8f8f5-106">Project detail fields</span></span>

- <span data-ttu-id="8f8f5-107">**Név**: A projekt címe.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="8f8f5-108">**Leírás**: A projekt áttekintése.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="8f8f5-109">**Ügyfél**: Az a vállalat, amelynek a projekt szállításra került.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="8f8f5-110">**Naptársablon**: A projekt munkaideje.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="8f8f5-111">A mező módosítása után a program újraszámítja a teljes ütemezést.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="8f8f5-112">**Pénznem**: A projekt pénzneme.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="8f8f5-113">Ez a mező a szerződő részlegben definiált pénznem alapján veszi fel az alapértelmezett értékét.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="8f8f5-114">A szerződő részleg frissítésekor a mező frissítése is megtörténik.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="8f8f5-115">**Szerződő részleg**: Az a szervezeti egység, amely azt a vállalatot vagy részleget reprezentálja, amely elsősorban felelős az értékesítés megnyeréséért és a munka és szolgáltatások ügyfélnek történő leszállításáért.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="8f8f5-116">**Projektvezető**: A projektcsapat azon tagja, akinek joga van az időbejegyzések és a kiadások áttekintésére és jóváhagyására.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="8f8f5-117">Becslés mezők</span><span class="sxs-lookup"><span data-stu-id="8f8f5-117">Estimate fields</span></span>

- <span data-ttu-id="8f8f5-118">**Becsült kezdő dátum**: A projekt kezdésének dátuma.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="8f8f5-119">A mező frissítésekor a projektben szereplő feladatok az új kezdő dátumnak megfelelően mozdulnak el.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="8f8f5-120">**Befejezési dátum**: A projekt ütemezett befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="8f8f5-121">**Erőfeszítés**: A projekt becsült erőfeszítése.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="8f8f5-122">Amikor feladatokat ad hozzá a projekthez, ez a mező többé nem szerkeszthető.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="8f8f5-123">**Becsült munkaköltség**: A projekt becsült munkaköltsége.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="8f8f5-124">Amikor munkaköltségeket ad hozzá a projekthez, ez a mező többé nem szerkeszthető.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="8f8f5-125">**Becsült kiadások**: A projekt becsült kiadásai.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="8f8f5-126">Amikor kiadásokat ad hozzá a projekthez, ez a mező többé nem szerkeszthető.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="8f8f5-127">A projekt tényleges mezői</span><span class="sxs-lookup"><span data-stu-id="8f8f5-127">Project actual fields</span></span>
- <span data-ttu-id="8f8f5-128">**Tényleges kezdés**: A projekt elkezdésének dátuma.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="8f8f5-129">**Tényleges befejezés**: Frissíteni kell a projekt befejezésekor.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="8f8f5-130">Projektállapot-mezők</span><span class="sxs-lookup"><span data-stu-id="8f8f5-130">Project status fields</span></span>

- <span data-ttu-id="8f8f5-131">**A projekt általános állapota**: A projektmenedzser által megadott általános projektegészségi állapot.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="8f8f5-132">**Megjegyzés**: A projektmenedzser által megadott aktuális állapotra vonatkozó leírás.</span><span class="sxs-lookup"><span data-stu-id="8f8f5-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>

