---
title: Újdonságok vagy változások a Project Service Automation 31-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 31-os frissítési kiadásában.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2e5fce003c25f9c5911e5a01fb4ec3e19c06c078e00b054472699a522b9cd070
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002154"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Újdonságok vagy változások a Project Service Automation 31-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 31-es frissítési kiadásában. A verzió build száma V3.10.52.77, és általánosan elérhető lesz önálló frissítésként 2021 májusában.

## <a name="update-release-31"></a>31-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

**Idő és költség**

A következő problémák kerültek kijavításra:

- Az Időbevitel vezérlő parancsgombjai a **Foglalható erőforrás** lapon érthetetlenek voltak.
- A **Project.SetTrackingFields** null referencia kivételt generált egy időbejegyzés jóváhagyásakor.

**Erőforráskezelés**

A következő problémák kerültek kijavításra:

- A **Csapattag létrehozása** nem jeleníti meg helyesen a foglalási beállítások metaadatainak beállítását a **Foglalások alapértelmezett lekötött állapota** esetében.
- A PSA 1.X verzióról 3.X verzióra való frissítés esetén a frissítési folyamat sikertelen lesz az **UpgradeResourceRequirements** elemben.


**Értékesítés**

A következő problémák kerültek kijavításra:

- A tényleges bevétel a nyomkövetési táblázatban a projekt pénznemére váltja át az összegeket.
- A pénznem alapértelmezett beállítása olyan helyzetekben, amikor a szervezet alappénzneme eltér a projektpénznemtől, árajánlatsorok és szerződéssorok létrehozásakor.
- **A függőben lévő javításra vonatkozó** érvényesítési lekérdezés nem szűri le a projekteket.
- A hátralévő értékesítések helytelen számítása történik egy projekten.
- A kapcsolattartón alapuló ajánlatok nem sikerülnek, ha árlista nélkül jön létre.
- Ha a **Számla megerősítése** lehetőséget választja, akkor nem jelenik meg a feldolgozásléptető.
- Ha a **Számla létrehozása** lehetőséget választja, akkor nem jelenik meg a feldolgozásléptető
- Az ajánlat elvesztettként való lezárása nem törli a foglalásokat.







