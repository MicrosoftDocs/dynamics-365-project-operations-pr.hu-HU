---
title: Projektsablonok fejlesztése a Projekt másolása lehetőséggel
description: Ez a cikk információt nyújt arról, hogyan hozhat létre projektsablonokat a Projekt másolása egyéni művelettel.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923835"
---
# <a name="develop-project-templates-with-copy-project"></a>Projektsablonok fejlesztése a Projekt másolása lehetőséggel

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Dynamics 365 Project Operations támogatja a projektek másolását és a hozzárendelések visszaállítását a szerepkört képviselő általános erőforrásokhoz. Az ügyfelek ezzel a funkcióval alap projektsablonokat hozhatnak létre.

Ha a **Projekt másolása** lehetőséget választja, akkor a program frissíti a célprojekt állapotát. Az **Állapot oka** használatával megállapíthatja, hogy a másolási művelet befejeződött-e. Ha a **Projekt másolása** lehetőséget választja , akkor a projekt kezdési dátumát is frissíti az aktuális kezdési dátumra, ha a cél projekt entitásban nem észlelhető a céldátum.

## <a name="copy-project-custom-action"></a>Projekt másolása egyéni művelet

### <a name="name"></a>Name 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Bemeneti paraméterek

Három bemeneti paraméter van:

- **ReplaceNamedResources** vagy **ClearTeamsAndAssignments** – Csak az egyik lehetőséget állítsa be. Ne állítsa be mindkettőt

    - **\{"ReplaceNamedResources":true\}** – A Project Operations alapértelmezett viselkedése. Minden megnevezett erőforrás helyébe általános erőforrás lép.
    - **\{"ClearTeamsAndAssignments":true\}** – A Project for the Web alapértelmezett viselkedése. A rendszer minden hozzárendelést és csoporttagot eltávolít.

- **SourceProject** – A forrás projekt, amelyből másolni kell entitáshivatkozása. Ez a paraméter nem lehet null értékű.
- **Target** – A célprojekt, amelybe másolni kell entitáshivatkozása. Ez a paraméter nem lehet null értékű.

Az alábbi táblázat a három paraméter összefoglalását tartalmazza.

| Paraméter                | Type             | Érték                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Boolean          | **True** vagy **False** |
| ClearTeamsAndAssignments | Boolean          | **True** vagy **False** |
| SourceProject            | Entitásreferencia | A forrásprojekt    |
| Target                   | Entitásreferencia | A célprojekt    |

További alapértelmezett műveletek: [Web API-műveletek használata](/powerapps/developer/common-data-service/webapi/use-web-api-actions)

### <a name="validations"></a>Ellenőrzések

A következő ellenőrzések történnek.

1. A Null ellenőrzi és beolvassa a forrás- és a cél projekteket, hogy megerősítse mindkét projekt meglété a szervezetben.
2. A rendszer a következő feltételek ellenőrzésével ellenőrzi, hogy a cél projekt érvényes-e másolásra:

    - Nincs korábbi tevékenység a projektben (beleértve a **Feladatok** lap kiválasztását is), és a projekt frissen lett létrehozva.
    - Nincs korábbi példány, nem kért importálást a projekthez, és a projekt állapota nem **Sikertelen**.

3. A művelet nincs HTTP-vel meghívva.

## <a name="specify-fields-to-copy"></a>Másolandó mezők meghatározása

A művelet meghívásakor a **Projekt másolása** megnézi a **Projektoszlopok másolása** projektnézetet, ennek segítségével határozza meg, hogy mely mezőket másolja a projekt másolásakor.

### <a name="example"></a>Példa

A következő példa bemutatja, hogyan hívja a **CopyProjectV3** egyéni műveletet a **removeNamedResources** paraméterkészlettel.

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
