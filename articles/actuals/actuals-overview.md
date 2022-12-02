---
title: Tényadatok
description: Ez a cikk a Microsoft Dynamics 365 Project Operations tényadatokkal való munkára vonatkozó információit mutatja be.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924801"
---
# <a name="actuals"></a>Tények

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű központi telepítés – proforma számlázás_

A tényleges adatok a projekt felülvizsgált és jóváhagyott pénzügyi és ütemezési előrehaladását jelentik. Az idő-, költség-, anyagfelhasználási tételek, valamint a naplótételek és számlák jóváhagyásával jönnek létre.

> [!IMPORTANT]
> A tényadatokat nem szabad szerkeszteni vagy törölni a rendszerből. Máskülönben a pénzügyi integritást, valamint az egyéb pénzügyi és könyvelési rendszerekkel való integrációt ez negatívan érinti. A Microsoft Dynamics 365 Project Operations lehetővé teszi, hogy a projektek üzleti folyamatának különböző pontjaina tényadatok visszavonását és cseréjét a szerkesztéshez.

## <a name="recording-actuals-based-on-project-events"></a>Tényadatok rögzítése projektesemények alapján

A Project Operations tényadatokként rögzíti a projektegyüttműködés életciklusa során bekövetkező pénzügyi tranzakciókat. A tényadatok különböző eseményeken való létrehozása az életciklus során attól függően változik, hogy a projektaktivitása idő- és anyag alapú számlázási modellt vagy a rögzített árú számlázási modellt használja-e, és hogy az értékesítés előtti fázisban van-e, vagy egy belső projekt.

A következő cikkek ismertetik a különböző események a Tényadatok táblára gyakorolt hatásait:

- [A tényadatok hatásai idő és anyagalapú együttműködésben](ActualsonTM.md)
- [A tényadatok hatásai rögzített árú együttműködésben](ActualonFP.md)
- [A tényadatok hatása egy együttműködés értékesítés előtti fázisában](ActualonPreSales.md)
- [A tényadatok hatása egy belső projektben](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
