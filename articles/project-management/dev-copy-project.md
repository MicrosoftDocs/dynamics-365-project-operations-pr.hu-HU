---
title: Projektsablonok fejlesztése a Projekt másolása lehetőséggel
description: Ez a témakör információt nyújt arról, hogyan hozhat létre projektsablonokat a Projekt másolása egyéni művelettel.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078032"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="a47bb-103">Projektsablonok fejlesztése a Projekt másolása lehetőséggel</span><span class="sxs-lookup"><span data-stu-id="a47bb-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="a47bb-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="a47bb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a47bb-105">A Dynamics 365 Project Operations támogatja a projekt másolásának képességét és a hozzárendelések visszaállítását a szerepkört képviselő általános erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="a47bb-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="a47bb-106">Az ügyfelek ezzel a funkcióval alap projektsablonokat hozhatnak létre.</span><span class="sxs-lookup"><span data-stu-id="a47bb-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="a47bb-107">Ha a **Projekt másolása** lehetőséget választja, akkor a program frissíti a célprojekt állapotát.</span><span class="sxs-lookup"><span data-stu-id="a47bb-107">When you select **Copy Project** , the status of the target project is updated.</span></span> <span data-ttu-id="a47bb-108">Az **Állapot oka** használatával megállapíthatja, hogy a másolási művelet befejeződött-e.</span><span class="sxs-lookup"><span data-stu-id="a47bb-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="a47bb-109">Ha a **Projekt másolása** lehetőséget választja , akkor a projekt kezdési dátumát is frissíti az aktuális kezdési dátumra, ha a cél projekt entitásban nem észlelhető a céldátum.</span><span class="sxs-lookup"><span data-stu-id="a47bb-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="a47bb-110">Projekt másolása egyéni művelet</span><span class="sxs-lookup"><span data-stu-id="a47bb-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="a47bb-111">Adatfolyam neve</span><span class="sxs-lookup"><span data-stu-id="a47bb-111">Name</span></span> 

<span data-ttu-id="a47bb-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="a47bb-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="a47bb-113">Bemeneti paraméterek</span><span class="sxs-lookup"><span data-stu-id="a47bb-113">Input parameters</span></span>
<span data-ttu-id="a47bb-114">Három bemeneti paraméter van:</span><span class="sxs-lookup"><span data-stu-id="a47bb-114">There are three input parameters:</span></span>

| <span data-ttu-id="a47bb-115">Paraméter</span><span class="sxs-lookup"><span data-stu-id="a47bb-115">Parameter</span></span>          | <span data-ttu-id="a47bb-116">Típus szerint</span><span class="sxs-lookup"><span data-stu-id="a47bb-116">Type</span></span>   | <span data-ttu-id="a47bb-117">Értékek</span><span class="sxs-lookup"><span data-stu-id="a47bb-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="a47bb-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="a47bb-118">ProjectCopyOption</span></span>  | <span data-ttu-id="a47bb-119">Sztring</span><span class="sxs-lookup"><span data-stu-id="a47bb-119">String</span></span> | <span data-ttu-id="a47bb-120">**{"removeNamedResources":true}** vagy **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="a47bb-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="a47bb-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="a47bb-121">SourceProject</span></span>      | <span data-ttu-id="a47bb-122">Entitásreferencia</span><span class="sxs-lookup"><span data-stu-id="a47bb-122">Entity Reference</span></span> | <span data-ttu-id="a47bb-123">Forrásprojekt</span><span class="sxs-lookup"><span data-stu-id="a47bb-123">Source Project</span></span> |
| <span data-ttu-id="a47bb-124">Cél</span><span class="sxs-lookup"><span data-stu-id="a47bb-124">Target</span></span>             | <span data-ttu-id="a47bb-125">Entitásreferencia</span><span class="sxs-lookup"><span data-stu-id="a47bb-125">Entity Reference</span></span> | <span data-ttu-id="a47bb-126">Célprojekt</span><span class="sxs-lookup"><span data-stu-id="a47bb-126">Target Project</span></span> |


- <span data-ttu-id="a47bb-127">**{"clearTeamsAndAssignments":true}** : Az alapértelmezett viselkedés a Projekthez webre, és eltávolítja az összes hozzárendelést és csoporttagot.</span><span class="sxs-lookup"><span data-stu-id="a47bb-127">**{"clearTeamsAndAssignments":true}** : Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="a47bb-128">**{"removeNamedResources":true}** A Project Operations alapértelmezett viselkedése, és a hozzárendeléseket visszaállítja az általános erőforrásokra.</span><span class="sxs-lookup"><span data-stu-id="a47bb-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="a47bb-129">További alapértelmezett műveletek [Web API-műveletek használata](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="a47bb-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="a47bb-130">Másolandó mezők meghatározása</span><span class="sxs-lookup"><span data-stu-id="a47bb-130">Specify fields to copy</span></span> 
<span data-ttu-id="a47bb-131">A művelet meghívásakor a **Projekt másolása** megnézi a **Projektoszlopok másolása** projektnézetet, ennek segítségével határozza meg, hogy mely mezőket másolja a projekt másolásakor.</span><span class="sxs-lookup"><span data-stu-id="a47bb-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
