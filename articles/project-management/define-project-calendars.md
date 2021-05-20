---
title: Projektnaptárak meghatározása
description: A témakör nyújt tájékoztatást arról, hogyan lehet naptári sablont alkalmazni a projekt ütemezésének nyomon követésére.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
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
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981303"
---
# <a name="define-project-calendars"></a><span data-ttu-id="d312f-103">Projektnaptárak meghatározása</span><span class="sxs-lookup"><span data-stu-id="d312f-103">Define project calendars</span></span>

<span data-ttu-id="d312f-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="d312f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d312f-105">Projekt létrehozásához és kezeléséhez naptársablont kell alkalmaznia a projektre.</span><span class="sxs-lookup"><span data-stu-id="d312f-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="d312f-106">A naptársablon a következő projektjellemzőket határozza meg:</span><span class="sxs-lookup"><span data-stu-id="d312f-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="d312f-107">Munkaidő, beleértve a kezdési és befejezési időt</span><span class="sxs-lookup"><span data-stu-id="d312f-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="d312f-108">Munkanapok</span><span class="sxs-lookup"><span data-stu-id="d312f-108">Working days</span></span>
- <span data-ttu-id="d312f-109">Naptárkivételek, például munkaszüneti napok</span><span class="sxs-lookup"><span data-stu-id="d312f-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="d312f-110">A projektre alkalmazott naptársablon a szervezet beállításaiban meghatározott naptársablon másolata.</span><span class="sxs-lookup"><span data-stu-id="d312f-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="d312f-111">Ha módosítja a naptársablont, ezek a módosítások nem kerülnek át a projekt munkaidejébe.</span><span class="sxs-lookup"><span data-stu-id="d312f-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="d312f-112">A projekt munkaidejének módosításához új sablont kell alkalmazni.</span><span class="sxs-lookup"><span data-stu-id="d312f-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="d312f-113">A szervezet naptársablonának létrehozásához két fő követelmény szükséges:</span><span class="sxs-lookup"><span data-stu-id="d312f-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="d312f-114">Új vagy meglévő foglalható erőforrással határozza meg a sablon kívánt munkaidejét.</span><span class="sxs-lookup"><span data-stu-id="d312f-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="d312f-115">Hozzon létre egy új naptársablont, és társítsa a sablont a foglalható erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="d312f-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="d312f-116">**A sablon munkaidejének meghatározása**</span><span class="sxs-lookup"><span data-stu-id="d312f-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="d312f-117">Lépjen a **Források** \> **Források** oldalra.</span><span class="sxs-lookup"><span data-stu-id="d312f-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="d312f-118">Hozzon létre egy új hivatkozást a naptársablonban, vagy jelöljön ki egy meglévő erőforrást.</span><span class="sxs-lookup"><span data-stu-id="d312f-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="d312f-119">Válassza ki az erőforrás **Munkaidő** lapját, és hajtsa végre a [Munkaidő beállítása erőforráshoz](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) felületen megjelenő utasításokat a naptárszabályok konfigurálásához.</span><span class="sxs-lookup"><span data-stu-id="d312f-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="d312f-120">**Új naptársablon létrehozása**</span><span class="sxs-lookup"><span data-stu-id="d312f-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="d312f-121">Lépjen a **Beállítások** \> **Naptársablon** pontra.</span><span class="sxs-lookup"><span data-stu-id="d312f-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="d312f-122">Válassza az **Új** lehetőséget, és adjon meg egy nevet, leírást és sablonerőforrást.</span><span class="sxs-lookup"><span data-stu-id="d312f-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="d312f-123">Ha egy erőforrásra hivatkozik egy naptársablonban, az erőforrás naptárának egy példánya a naptársablonhoz társul.</span><span class="sxs-lookup"><span data-stu-id="d312f-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="d312f-124">Ha módosítja a másolt sablon munkaidejét, akkor ezek a módosítások nem kerülnek át a projekt munkaidejébe.</span><span class="sxs-lookup"><span data-stu-id="d312f-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="d312f-125">Most már hozzárendelheti a munkasablont egy projekt naptársablonhoz.</span><span class="sxs-lookup"><span data-stu-id="d312f-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

