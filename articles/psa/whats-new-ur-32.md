---
title: Újdonságok vagy változások a Project Service Automation 32-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 32-os frissítési kiadásában.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 023e51e834060a35d2d7e3469d34297192e38ba11c12a2c4f57424213aba44ba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994864"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Újdonságok vagy változások a Project Service Automation 32-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 32-es frissítési kiadásában. A verzió build száma V3.10.53.108, és általánosan elérhető lesz önálló frissítésként 2021 júniusában.

## <a name="update-release-32"></a>32-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

#### <a name="general"></a>Általános

- Ha egy nagyobb frissítés sikertelen, csak az alkalmazás fő belépési pontjait kell zárolni annak érdekében, hogy a megosztott entitások továbbra is elérhetők legyenek.

#### <a name="time-and-expense"></a>Idő és költség

A következő problémák kerültek kijavításra:

- A **TimeEntalbumImportResourceAsignment** nem tartja karban az erőforrás-hozzárendelési szelet kezdő és a záró időpontját.
- Ha kiválasztja a **Bejegyzés megnyitása** az **Időbejegyzés** lehetőséget az Időbevitel rácson, előfordulhat, hogy más űrlapokat nem lehet kijelölni.
- Amikor időbejegyzések hozzárendelését importálja, az ügyfélkód lekérdezése hosszú URL-címet generálhat, amely meghiúsul a lekérdezésben.
- Az **Időbevitel** rácsban, miután egy értéket törölnek a cellából, a fókusz nem marad a rácsban.
- Az **Elutasítás** gomb el lett távolítva a modern jóváhagyások **Jóváhagyások feldolgozása** nézetéből.
- Az időbevitel tömeges jóváhagyásának stabilitását és teljesítményét befolyásolják a holtpontok és az, hogy nem elehet megefelelően kezelni a testreszabásokat, amelyek az **Időbevitel** bejegyzéshez kapcsolódnak.

#### <a name="project-planning"></a>Projekttervezés

- Null referencia kivétel jön létre olyan projekt frissítésekkor, amelyek értéke null értéket tartalmaz a **Szerződésszerződéses egység** mezőben.
- A **Projekt végösszegeinek frissítése** nem megfelelően számítja ki a fennmaradó költséget és a projekt hátralévő értékesítését.
- A redundáns árképzési számítások hatással vannak az erőforrás-hozzárendelések frissítéséhez kapcsolódó teljesítményre.

#### <a name="resource-management"></a>Erőforráskezelés

A következő probléma ki lett javítva:

- Ha egy lefoglalható erőforrás naptárkapacitása 1-nél több, a Project Service Automation helytelenül 0 (nulla) értékként ismeri fel a kapacitást. Éppen ezért végtelen ciklus fordul elő az ütemezési nézetben.

#### <a name="sales"></a>Értékesítés

A következő problémák kerültek kijavításra:

- Egyéni tranzakciótípusú naplósor létrehozásakor a következő null hivatkozási kivétel jön létre: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Az olyan szerepkörök és kategóriák, amelyek inaktiválva vannak az árajánlat másolása előtt, ne adja hozzá a számlázható szerepkörökhöz és kategóriákhoz az újonnan másolt árajánlatban.
- A dokumentum dátuma és a könyvelési dátum nem igazodik a számlasor olyan részleteihez tartozó kezdő dátumhoz, amely közvetlenül a számlatervezeten jön létre.
- A null hivatkozási kivételek olyan helyzetekben jönnek létre, amelyek a szerepkörök és kategóriák inaktiválásával kapcsolatosak az árajánlat másolása előtt.
- A **Projektek** lapon az **Árak frissítése** művelet nem frissíti a költségbecsléseket és az anyagbecsléseket.
