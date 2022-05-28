---
title: Tényadatok
description: A témakör a Microsoft Dynamics 365 Project Operations tényadatokkal való munkára vonatkozó információit mutatja be.
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
ms.openlocfilehash: 3f0cb8c478e2ce6fba589d51d95649f53f62e883
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581287"
---
# <a name="actuals"></a>Tények

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű központi telepítés – proforma számlázás_

A tényleges adatok a projekt felülvizsgált és jóváhagyott pénzügyi és ütemezési előrehaladását jelentik. Ezek az idő-, költség- és anyagfelhasználási tételek, naplótételek és számlák jóváhagyásakor jönnek létre.

> [!IMPORTANT]
> A tényleges adatokat nem szabad szerkeszteni vagy törölni a rendszerből. Ellenkező esetben a pénzügyi integritást és az egyéb pénzügyi és számviteli rendszerekkel való bármilyen integrációt hátrányosan érintheti. A Microsoft Dynamics 365 Project Operations lehetővé teszi, hogy a tényleges adatok sztornírozásával és cseréjével szerkesztheti a tényleges adatokat a projektek üzleti folyamat életciklusának különböző pontjain.

## <a name="recording-actuals-based-on-project-events"></a>Tényadatok rögzítése projektesemények alapján

A Project Operations a projektmegbízási életciklus során bekövetkező pénzügyi tranzakciókat tényleges értékként rögzíti. A tényleges adatok létrehozása az életciklus különböző eseményein változó, attól függően, hogy a projekt elkötelezettsége az idő- és anyagszámlázási modellt vagy a rögzített árú számlázási modellt használja-e, és hogy az értékesítés előtti szakaszban van-e, vagy belső projekt.

A következő témakörök az Aktualitások táblára gyakorolt hatást ismertetik a különböző változatok különböző eseményein:

- [Aktualitások hatása egy időben és az anyagokban](ActualsonTM.md)
- [Tényleges hatás egy rögzített árú megbízásban](ActualonFP.md)
- [Tényleges hatások az eljegyzés értékesítés előtti szakaszában](ActualonPreSales.md)
- [A belső projekt tényleges hatása](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
