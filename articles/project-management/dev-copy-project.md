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
ms.openlocfilehash: 87696b41db20e9ec70270c850d9acfe05df8cd84
ms.sourcegitcommit: d5004acb6f1c257b30063c873896fdea92191e3b
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/22/2021
ms.locfileid: "5045012"
---
# <a name="develop-project-templates-with-copy-project"></a>Projektsablonok fejlesztése a Projekt másolása lehetőséggel

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations támogatja a projektek másolását és a hozzárendelések visszaállítását a szerepkört képviselő általános erőforrásokhoz. Az ügyfelek ezzel a funkcióval alap projektsablonokat hozhatnak létre.

Ha a **Projekt másolása** lehetőséget választja, akkor a program frissíti a célprojekt állapotát. Az **Állapot oka** használatával megállapíthatja, hogy a másolási művelet befejeződött-e. Ha a **Projekt másolása** lehetőséget választja , akkor a projekt kezdési dátumát is frissíti az aktuális kezdési dátumra, ha a cél projekt entitásban nem észlelhető a céldátum.

## <a name="copy-project-custom-action"></a>Projekt másolása egyéni művelet 

### <a name="name"></a>Adatfolyam neve 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Bemeneti paraméterek
Három bemeneti paraméter van:

| Paraméter          | Típus szerint   | Értékek                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | Sztring | **{"removeNamedResources":true}** vagy **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Entitásreferencia | Forrásprojekt |
| Cél             | Entitásreferencia | Célprojekt |


- **{"clearTeamsAndAssignments":true}** : Az alapértelmezett viselkedés a Projekthez webre, és eltávolítja az összes hozzárendelést és csoporttagot.
- **{"removeNamedResources":true}** A Project Operations alapértelmezett viselkedése, és a hozzárendeléseket visszaállítja az általános erőforrásokra.

További alapértelmezett műveletek [Web API-műveletek használata](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Másolandó mezők meghatározása 
A művelet meghívásakor a **Projekt másolása** megnézi a **Projektoszlopok másolása** projektnézetet, ennek segítségével határozza meg, hogy mely mezőket másolja a projekt másolásakor.


### <a name="example"></a>Példa
A következő példa bemutatja, hogyan hívja a **CopyProject** egyéni műveletet a **removeNamedResources** paraméterkészlettel.
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