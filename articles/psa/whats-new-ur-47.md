---
title: Újdonságok vagy változások a Project Service Automation 47-es frissítési kiadásának V3 változatában
description: Ez a cikk a Microsoft Dynamics 365 Project Service Automation Update Release 47, V3 verzióban elérhető funkciókat és javításokat sorolja fel.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477281"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Újdonságok vagy változások a Project Service Automation 47-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a cikk felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3 45-os frissítési kiadásában. Ennek a verziónak a buldszáma V3.10.78.8, és általánosan elérhető 2022. júliusában önálló frissítésen keresztül.

## <a name="update-release-47"></a>47-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.

**Erőforráskezelés**
- Az ellenőrzés frissült, annak biztosítására, hogy a felhasználók ne válthassanak ki nullreferencia kivételt, amikor **Foglalható erőforrás** nélkül próbálnak meg létrehozni egy projektcsoport-tagot.
