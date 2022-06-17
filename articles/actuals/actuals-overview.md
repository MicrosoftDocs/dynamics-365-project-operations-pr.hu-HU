---
title: Tényadatok
description: Ez a cikk arról nyújt tájékoztatást, hogyan dolgozhat a tényleges adatokkal a Microsoftban Dynamics 365 Project Operations.
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

A tényleges adatok a projekt felülvizsgált és jóváhagyott pénzügyi és ütemezési előrehaladását jelentik. Ezek akkor jönnek létre, amikor az idő-, költség- és anyaghasználati bejegyzéseket, naplóbejegyzéseket és számlákat jóváhagyják.

> [!IMPORTANT]
> A tényleges adatokat nem szabad szerkeszteni vagy törölni a rendszerből. Ellenkező esetben hátrányosan érintheti a pénzügyi integritást és a más pénzügyi és számviteli rendszerekkel való integrációt. A Microsoft Dynamics 365 Project Operations lehetővé teszi, hogy a tényleges adatok megfordításával és cseréjével szerkessze a tényleges adatokat a projektek üzleti folyamatának életciklusának különböző pontjain.

## <a name="recording-actuals-based-on-project-events"></a>Tényadatok rögzítése projektesemények alapján

A Project Operations a projekt elköteleződési életciklusa során bekövetkező pénzügyi tranzakciókat ténylegesként rögzíti. A tényleges adatok létrehozása az életciklus különböző eseményein attól függően változik, hogy a projekt elköteleződése az idő- és anyagszámlázási modellt vagy a rögzített árú számlázási modellt használja-e, és hogy az értékesítés előtti szakaszban van-e, vagy belső projektről van-e szó.

A következő cikkek ismertetik a Tényleges adatok táblázatra gyakorolt hatást a különböző változatok különböző eseményeinél:

- [A tényleges hatás egy adott időben és az anyagok bevonása](ActualsonTM.md)
- [Tényleges hatás rögzített ármegállapításban](ActualonFP.md)
- [Tényleges hatás az elköteleződés értékesítés előtti szakaszában](ActualonPreSales.md)
- [A belső projekt tényleges hatása](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
