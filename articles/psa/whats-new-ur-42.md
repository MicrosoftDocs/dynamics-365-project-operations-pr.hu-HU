---
title: Újdonságok vagy változások a Project Service Automation 42-es frissítési kiadásának V3 változatában
description: Ez a témakör a Microsoft Dynamics 365 Project Service Automation Update Release 42, V3 verzióban elérhető funkciókat és javításokat sorolja fel.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589199"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Újdonságok vagy változások a Project Service Automation 42-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3 42-os frissítési kiadásában. Ez a verzió buildszáma V3.10.73.61, és általában 2022 áprilisában önfrissítéssel érhető el.

## <a name="update-release-42"></a>42-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.

**Idő és költség**

- Ha egy munkaidő-lapot elutasítanak, az elutasító felhasználót helytelenül rendszerként **azonosítják**.
- A bejegyzések importálásakor hiányzik az **Erőforráskategória** érték.
- A projekt jóváhagyói jóváhagyhatják a benyújtott projekteket, ha az engedélyük nincs kifejezetten Jóváhagyható értékre **állítva**.

**Értékesítés**

- Ha a tényleges adatok nem gyökérszintű tevékenységekbe vannak bejelentkezve, a tényleges költségek helytelenül összesítve vannak.
