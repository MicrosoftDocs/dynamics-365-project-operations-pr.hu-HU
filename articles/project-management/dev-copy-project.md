---
title: Projektsablonok fejlesztése a Projekt másolása lehetőséggel
description: Ez a témakör információt nyújt arról, hogyan hozhat létre projektsablonokat a Projekt másolása egyéni művelettel.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131616"
---
# <a name="develop-project-templates-with-copy-project"></a>Projektsablonok fejlesztése a Projekt másolása lehetőséggel

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations támogatja a projekt másolásának képességét és a hozzárendelések visszaállítását a szerepkört képviselő általános erőforrásokhoz. Az ügyfelek ezzel a funkcióval alap projektsablonokat hozhatnak létre.

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