---
title: Projekttevékenységek szinkronizálása közvetlenül a Projektszolgáltatás automatizálásától a Pénzügyekig és műveletekig
description: Ez a témakör a projekttevékenységek közvetlen Microsoft Dynamics 365 Project Service Automation szinkronizálására használt sablont és mögöttes tevékenységet írja le Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 666e0d757969b32f16e08128d9f78a2ffe1e8357
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683313"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Projekttevékenységek szinkronizálása közvetlenül a Projektszolgáltatás automatizálásától a Pénzügyekig és műveletekig

[!include[banner](../includes/banner.md)]

Ez a témakör a projekttevékenységek közvetlen Dynamics 365 Project Service Automation szinkronizálására használt sablont és mögöttes tevékenységet írja le Dynamics 365 Finance.

> [!NOTE]
> - A projektfeladatok integrációja, a kiadási tranzakciók kategóriái, az órabecslések, a kiadásbecslések és a funkciók zárolása a 8.0 verzióban érhető el.
> - Ha az Enterprise Edition 7.3.0 verzióját használja, a KB 4132657 és a KB 4132660 telepítése után használhatja a sablonokat a projektfeladatok, a költségtranzakció-kategóriák, az órabecslések, a kiadásbecslések és a tényadatok integrálására, valamint a funkciók zárolásának konfigurálására. Ha vissza kell állítania a könyvelési feloszlásokat, ajánlott a KB 4131710 telepítése is.
> - A tényadatok integrációja a 8.0.1 vagy újabb verziókban érhető el.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Adatfolyam a Project Service Automation és a Finance között

A Project Service Automation és Finance közötti integrációs megoldás az adatintegrációs funkció segítségével szinkronizálja az adatokat a Project Service Automation és a Finance példányai között. Az adatintegrációs szolgáltatással elérhető integrációs sablon lehetővé teszi a projektfeladatok áramlását a Project Service Automation és a Finance között.

A következő ábra azt mutatja be, hogyan történik az adatok szinkronizálása a Project Service Automation és a Finance rendszer között.

[![Adatfolyam a Project Service Automation és a Finance közötti integrációhoz.](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Sablon és feladat

A sablon eléréséhez a Microsoft Power Apps felügyeleti központban válassza a **Projektek** lehetőséget, majd a jobb felső sarokban válassza az **Új projekt** lehetőséget a nyilvános sablonok kiválasztásához.

A következő sablon és a mögöttes feladat segítségével szinkronizálhatja a projektfeladatokat a Project Service Automation alkalmazásból a Finance rendszerbe:

- **A sablon neve az adatintegrációban:** Projektfeladatok (PSA – Fin és Ops)
- **A feladat neve a projektben:** Projektfeladatok

A projektfeladatok szinkronizálása előtt szinkronizálnia kell a projektszerződéseket és projekteket.

## <a name="entity-set"></a>Entitáskészlet

| Project Service Automation | Pénzügy                             |
|----------------------------|-------------------------------------|
| Projektfeladatok              | A projektfeladat integrációs entitása |

## <a name="entity-flow"></a>Entitásfolyam

A projektfeladatok a Project Service Automation alkalmazásban kezelhetők, és a program projekttevékenységekként szinkronizálja őket a Finance rendszerbe.

## <a name="prerequisites-and-mapping-setup"></a>Előfeltételek és leképezési beállítások

A projektfeladatok szinkronizálása előtt szinkronizálnia kell a projektszerződéseket és projekteket.

## <a name="power-query"></a>Power Query

Ha ez a feltétel teljesül, a Microsoft Power Query for Excel programot kell használni az adatok szűrésére:

- A projektfeladatban erőforrás-specifikus rekordok vannak.

Ha használnia Power Query kell, kövesse az alábbi iránymutatást:

- A Projektfeladatok (PSA – Fin és Ops) sablonja egy alapértelmezett szűrővel rendelkezik, amely kizárja a projektfeladat erőforrás-specifikus bejegyzéseit az **IsLineTask** szűrőjét **Hemis** értékre állítva. Ha saját sablont hoz létre, akkor ezt a szűrőt kell hozzáadnia.

## <a name="template-mapping-in-data-integration"></a>Sablonok leképezése az adatintegrációban

A következő ábra egy példát mutat be az adatintegrációban az sablonfeladatok leképezésére. A leképezés azokat a mezőinformációkat mutatja, amelyek a Project Service Automation alkalmazásból a Finance rendszerbe lesznek szinkronizálva.

[![Sablonok leképezése.](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]