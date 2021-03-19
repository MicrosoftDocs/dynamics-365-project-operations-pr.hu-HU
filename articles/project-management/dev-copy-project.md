---
title: Projektsablonok fejlesztése a Projekt másolása lehetőséggel
description: Ez a témakör információt nyújt arról, hogyan hozhat létre projektsablonokat a Projekt másolása egyéni művelettel.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 27847575e2d6ec9af77d24f756b13d3aeb0efea7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286926"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="2bbb9-103">Projektsablonok fejlesztése a Projekt másolása lehetőséggel</span><span class="sxs-lookup"><span data-stu-id="2bbb9-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="2bbb9-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="2bbb9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2bbb9-105">Dynamics 365 Project Operations támogatja a projektek másolását és a hozzárendelések visszaállítását a szerepkört képviselő általános erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="2bbb9-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="2bbb9-106">Az ügyfelek ezzel a funkcióval alap projektsablonokat hozhatnak létre.</span><span class="sxs-lookup"><span data-stu-id="2bbb9-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="2bbb9-107">Ha a **Projekt másolása** lehetőséget választja, akkor a program frissíti a célprojekt állapotát.</span><span class="sxs-lookup"><span data-stu-id="2bbb9-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="2bbb9-108">Az **Állapot oka** használatával megállapíthatja, hogy a másolási művelet befejeződött-e.</span><span class="sxs-lookup"><span data-stu-id="2bbb9-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="2bbb9-109">Ha a **Projekt másolása** lehetőséget választja , akkor a projekt kezdési dátumát is frissíti az aktuális kezdési dátumra, ha a cél projekt entitásban nem észlelhető a céldátum.</span><span class="sxs-lookup"><span data-stu-id="2bbb9-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="2bbb9-110">Projekt másolása egyéni művelet</span><span class="sxs-lookup"><span data-stu-id="2bbb9-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="2bbb9-111">Adatfolyam neve</span><span class="sxs-lookup"><span data-stu-id="2bbb9-111">Name</span></span> 

<span data-ttu-id="2bbb9-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="2bbb9-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="2bbb9-113">Bemeneti paraméterek</span><span class="sxs-lookup"><span data-stu-id="2bbb9-113">Input parameters</span></span>
<span data-ttu-id="2bbb9-114">Három bemeneti paraméter van:</span><span class="sxs-lookup"><span data-stu-id="2bbb9-114">There are three input parameters:</span></span>

| <span data-ttu-id="2bbb9-115">Paraméter</span><span class="sxs-lookup"><span data-stu-id="2bbb9-115">Parameter</span></span>          | <span data-ttu-id="2bbb9-116">Típus szerint</span><span class="sxs-lookup"><span data-stu-id="2bbb9-116">Type</span></span>   | <span data-ttu-id="2bbb9-117">Értékek</span><span class="sxs-lookup"><span data-stu-id="2bbb9-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="2bbb9-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="2bbb9-118">ProjectCopyOption</span></span>  | <span data-ttu-id="2bbb9-119">Sztring</span><span class="sxs-lookup"><span data-stu-id="2bbb9-119">String</span></span> | <span data-ttu-id="2bbb9-120">**{"removeNamedResources":true}** vagy **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="2bbb9-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="2bbb9-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="2bbb9-121">SourceProject</span></span>      | <span data-ttu-id="2bbb9-122">Entitásreferencia</span><span class="sxs-lookup"><span data-stu-id="2bbb9-122">Entity Reference</span></span> | <span data-ttu-id="2bbb9-123">Forrásprojekt</span><span class="sxs-lookup"><span data-stu-id="2bbb9-123">Source Project</span></span> |
| <span data-ttu-id="2bbb9-124">Cél</span><span class="sxs-lookup"><span data-stu-id="2bbb9-124">Target</span></span>             | <span data-ttu-id="2bbb9-125">Entitásreferencia</span><span class="sxs-lookup"><span data-stu-id="2bbb9-125">Entity Reference</span></span> | <span data-ttu-id="2bbb9-126">Célprojekt</span><span class="sxs-lookup"><span data-stu-id="2bbb9-126">Target Project</span></span> |


- <span data-ttu-id="2bbb9-127">**{"clearTeamsAndAssignments":true}** : Az alapértelmezett viselkedés a Projekthez webre, és eltávolítja az összes hozzárendelést és csoporttagot.</span><span class="sxs-lookup"><span data-stu-id="2bbb9-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="2bbb9-128">**{"removeNamedResources":true}** A Project Operations alapértelmezett viselkedése, és a hozzárendeléseket visszaállítja az általános erőforrásokra.</span><span class="sxs-lookup"><span data-stu-id="2bbb9-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="2bbb9-129">További alapértelmezett műveletek [Web API-műveletek használata](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="2bbb9-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="2bbb9-130">Másolandó mezők meghatározása</span><span class="sxs-lookup"><span data-stu-id="2bbb9-130">Specify fields to copy</span></span> 
<span data-ttu-id="2bbb9-131">A művelet meghívásakor a **Projekt másolása** megnézi a **Projektoszlopok másolása** projektnézetet, ennek segítségével határozza meg, hogy mely mezőket másolja a projekt másolásakor.</span><span class="sxs-lookup"><span data-stu-id="2bbb9-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="2bbb9-132">Példa</span><span class="sxs-lookup"><span data-stu-id="2bbb9-132">Example</span></span>
<span data-ttu-id="2bbb9-133">A következő példa bemutatja, hogyan hívja a **CopyProject** egyéni műveletet a **removeNamedResources** paraméterkészlettel.</span><span class="sxs-lookup"><span data-stu-id="2bbb9-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]