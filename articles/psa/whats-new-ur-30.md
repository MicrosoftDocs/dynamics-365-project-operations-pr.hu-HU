---
title: Újdonságok vagy változások a Project Service Automation 30-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 30-os frissítési kiadásában.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 07ca20425d05d1d638d9b2b8c3425562e39dd6627916794d1ad8441f00658459
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986989"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Újdonságok vagy változások a Project Service Automation 30-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution.md).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 30-es frissítési kiadásában. A verzió build száma V3.10.51.61, és általánosan elérhető lesz önálló frissítésként 2021 áprilisában.

## <a name="update-release-30"></a>30-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

**Idő és költség**

A következő problémák kerültek kijavításra:

- Hiba történik, ha időbejegyzést hoz létre és ment el a **Gyorslétrehozási** lapon, miközben a **Szerepkör** mező el van távolítva.
- Az Időbejegyzési szűrő nem a megfelelő szűrőoperátort alkalmazza.
- A másolt munkaidő-nyilvántartások nem jelennek meg automatikusan, amikor az időbejegyzés vezérlőjén a **Hét másolása** lehetőséget választja ki.

**Erőforráskezelés**

A következő problémák kerültek kijavításra:

- Ha meghosszabbít egy foglalást, akkor a kemény foglaláshoz rendelt foglalási állapot helytelen. A foglalás kiterjesztése tiszteletben tartja a foglalási beállítás metaadataiban **Lekötöttként** meghatározott foglalási állapotot.
- Ha nincs megadva érvényes foglalási állapot, a hibaüzenet nem lesz megfelelően lokalizálva.

**Projektmenedzsment**

A következő problémák kerültek kijavításra:

- A projektek nem hozhatók létre az egyik pénznemben, és nem tartalmazzák a kapcsolódó tevékenységeket egy másik pénznemben.

**Értékesítés**

A következő problémák kerültek kijavításra:

- Árlista másolásakor az árak nem frissülnek.
- Az árajánlat megnyertként való lezárása nem sikerül, ha a költségrészletnek van egy eredeti értéke.
- A **Projektfeladat** entitáson a **Becsült költség** át lett nevezve **Tervezett költség (Alap)** értékre.
- A számlák létrehozásakor vagy törlésekor null értékű hivatkozáskivétel jön létre.
