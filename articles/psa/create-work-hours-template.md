---
title: Munkaidősablon létrehozása
description: Ez a témakör ismerteti, hogyan hozható létre munkaidősablon a Project Service szolgáltatásban.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997199"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="23701-103">Munkaidősablon létrehozása (Project Service)</span><span class="sxs-lookup"><span data-stu-id="23701-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="23701-104">Projekt létrehozásához és kezeléséhez naptársablont kell alkalmaznia a projektre.</span><span class="sxs-lookup"><span data-stu-id="23701-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="23701-105">A naptársablon a következő projektjellemzőket határozza meg:</span><span class="sxs-lookup"><span data-stu-id="23701-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="23701-106">Munkaidő, beleértve a kezdési és befejezési időt</span><span class="sxs-lookup"><span data-stu-id="23701-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="23701-107">Munkanapok</span><span class="sxs-lookup"><span data-stu-id="23701-107">Working days</span></span>
- <span data-ttu-id="23701-108">Naptárkivételek, például munkaszüneti napok</span><span class="sxs-lookup"><span data-stu-id="23701-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="23701-109">A projektre alkalmazott naptársablon a szervezet beállításaiban meghatározott naptársablon másolata.</span><span class="sxs-lookup"><span data-stu-id="23701-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="23701-110">Ha módosítja a naptársablont, ezek a módosítások nem kerülnek át a projekt munkaidejébe.</span><span class="sxs-lookup"><span data-stu-id="23701-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="23701-111">A projekt munkaidejének módosításához új sablont kell alkalmazni.</span><span class="sxs-lookup"><span data-stu-id="23701-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="23701-112">A szervezet naptársablonának létrehozásához két fő követelmény szükséges:</span><span class="sxs-lookup"><span data-stu-id="23701-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="23701-113">Új vagy meglévő foglalható erőforrással határozza meg a sablon kívánt munkaidejét.</span><span class="sxs-lookup"><span data-stu-id="23701-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="23701-114">Hozzon létre egy új naptársablont, és társítsa a sablont a foglalható erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="23701-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="23701-115">**A sablon munkaidejének meghatározása**</span><span class="sxs-lookup"><span data-stu-id="23701-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="23701-116">Lépjen a **Források** \> **Források** oldalra.</span><span class="sxs-lookup"><span data-stu-id="23701-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="23701-117">Hozzon létre egy új hivatkozást a naptársablonban, vagy jelöljön ki egy meglévő erőforrást.</span><span class="sxs-lookup"><span data-stu-id="23701-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="23701-118">Válassza ki az erőforrás **Munkaidő** lapját, és hajtsa végre a [Munkaidő beállítása erőforráshoz](/dynamics365/field-service/set-work-hours-resource.md) felületen megjelenő utasításokat a naptárszabályok konfigurálásához.</span><span class="sxs-lookup"><span data-stu-id="23701-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="23701-119">**Új naptársablon létrehozása**</span><span class="sxs-lookup"><span data-stu-id="23701-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="23701-120">Lépjen a **Beállítások** \> **Naptársablon** pontra.</span><span class="sxs-lookup"><span data-stu-id="23701-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="23701-121">Válassza az **Új** lehetőséget, és adjon meg egy nevet, leírást és sablonerőforrást.</span><span class="sxs-lookup"><span data-stu-id="23701-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="23701-122">Ha egy erőforrásra hivatkozik egy naptársablonban, az erőforrás naptárának egy példánya a naptársablonhoz társul.</span><span class="sxs-lookup"><span data-stu-id="23701-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="23701-123">Ha módosítja a másolt sablon munkaidejét, akkor ezek a módosítások nem kerülnek át a projekt munkaidejébe.</span><span class="sxs-lookup"><span data-stu-id="23701-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="23701-124">Kapcsolódó információk</span><span class="sxs-lookup"><span data-stu-id="23701-124">See Also</span></span>  
 [<span data-ttu-id="23701-125">Erőforrások beállítása</span><span class="sxs-lookup"><span data-stu-id="23701-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
