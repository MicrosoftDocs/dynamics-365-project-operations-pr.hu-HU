---
title: Újdonságok vagy változások a Project Service Automation 42-es frissítési kiadásának V3 változatában
description: Ez a cikk a Microsoft Dynamics 365 Project Service Automation Update Release 42, V3 verzióban elérhető funkciókat és javításokat sorolja fel.
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
ms.openlocfilehash: e9911531e4acbd78db416f554c8d85c4f1fee1cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912718"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Újdonságok vagy változások a Project Service Automation 42-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a cikk felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3 42-os frissítési kiadásában. A verzió build száma V3.10.73.61, és általánosan elérhető lesz önálló frissítésként 2022 áprilisában.

## <a name="update-release-42"></a>42-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.

**Idő és költség**

- Elutasított időnyilvántartás esetén az elutasító felhasználó helytelenül **Rendszer** értékkel van azonosítva.
- Időbejegyzések importálásakor hiányzik az **Erőforráskategória** érték.
- A projekt jóváhagyók akkor is jóváhagyhatják a beküldött projekteket, ha az engedélyük nincs kifejezetten a **Jóváhagyhat** értékre állítva.

**Értékesítés**

- Nem gyökérszintű feladatokhoz való tényadatok naplózása esetén a tényleges költségeket nem megfelelően összesíti a rendszer.
