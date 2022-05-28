---
title: Projektsablonok fejlesztése a Projekt másolása lehetőséggel
description: Ez a témakör információt nyújt arról, hogyan hozhat létre projektsablonokat a Projekt másolása egyéni művelettel.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 72aa2db7c717eeab85ada448c673bf702087baeb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590901"
---
# <a name="develop-project-templates-with-copy-project"></a>Projektsablonok fejlesztése a Projekt másolása lehetőséggel

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Dynamics 365 Project Operations támogatja a projektek másolását és a hozzárendelések visszaállítását a szerepkört képviselő általános erőforrásokhoz. Az ügyfelek ezzel a funkcióval alap projektsablonokat hozhatnak létre.

Ha a **Projekt másolása** lehetőséget választja, akkor a program frissíti a célprojekt állapotát. Az **Állapot oka** használatával megállapíthatja, hogy a másolási művelet befejeződött-e. Ha a **Projekt másolása** lehetőséget választja , akkor a projekt kezdési dátumát is frissíti az aktuális kezdési dátumra, ha a cél projekt entitásban nem észlelhető a céldátum.

## <a name="copy-project-custom-action"></a>Projekt másolása egyéni művelet

### <a name="name"></a>Name 

msdyn\_ CopyProjectV3

### <a name="input-parameters"></a>Bemeneti paraméterek

Három bemeneti paraméter van:

- **ReplaceNamedResources** vagy **ClearTeamsAndAssignments** – Csak az egyik beállítást adja meg. Ne állítsa be mindkettőt.

    - **\{"ReplaceNamedResources":true\}** – A Project Operations alapértelmezett viselkedése. A rendszer lecseréli a megnevezett erőforrásokat az általános erőforrásokra.
    - **\{"ClearTeamsAndAssignments":true\}** – A Project for the Web alapértelmezett viselkedése. Minden feladat és csapattag eltávolításra kerül.

- **SourceProject** – a forrásprojekt entitáshivatkozása, amelyből másolni szeretne. Ez a paraméter nem lehet null értékű.
- **Cél** – a másolás célprojekt entitáshivatkozása. Ez a paraméter nem lehet null értékű.

Az alábbi táblázat összefoglalja a három paramétert.

| Paraméter                | Type             | Érték                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Boolean          | **Igaz** vagy **hamis** |
| ClearTeamsAndAssignments | Boolean          | **Igaz** vagy **hamis** |
| SourceProject            | Entitásreferencia | A forrásprojekt    |
| Target                   | Entitásreferencia | A célprojekt    |

A műveletek alapértelmezett beállításairól a Webes API-műveletek [használata című témakörben olvashat bővebben](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Érvényesítés

A következő érvényesítések történnek.

1. Null ellenőrzi és lekéri a forrás- és célprojekteket, hogy megerősítse mindkét projekt létezését a szervezetben.
2. A rendszer a következő feltételek ellenőrzésével ellenőrzi, hogy a célprojekt érvényes-e másolásra:

    - A projektben nincs korábbi tevékenység (beleértve a **Tevékenységek** lap kiválasztását is), és a projekt újonnan jön létre.
    - Nincs korábbi másolat, nincs importálás kérve ehhez a projekthez, és a projekt állapota **nem sikerült**.

3. A művelet nem HTTP használatával hívható meg.

## <a name="specify-fields-to-copy"></a>Másolandó mezők meghatározása

A művelet meghívásakor a **Projekt másolása** megnézi a **Projektoszlopok másolása** projektnézetet, ennek segítségével határozza meg, hogy mely mezőket másolja a projekt másolásakor.

### <a name="example"></a>Példa

Az alábbi példa bemutatja, hogyan hívható meg a **CopyProjectV3** egyéni művelet az **removeNamedResources** paraméterkészlettel.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

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
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
