---
title: Újdonságok vagy változások a Project Service Automation 43-es frissítési kiadásának V3 változatában
description: Ez a témakör a Microsoft Dynamics 365 Project Service Automation Update Release 43, V3 verzióban elérhető funkciókat és javításokat sorolja fel.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.openlocfilehash: fcf18a24b3bc354a16a415368063133743e79696
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710155"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Újdonságok vagy változások a Project Service Automation 43-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x készülékkel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3 43-os frissítési kiadásában. A verzió build száma V3.10.74.200, és általánosan elérhető lesz önálló frissítésként 2022 májusában.

## <a name="update-release-43"></a>43-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.


**Idő és költség**

- Ha időbejegyzéseket importál foglalásokból vagy erőforrás-hozzárendelésekből, a kapcsolódó könyvelhető erőforrásra való hivatkozás nem marad fenn.
- Ha az időbeviteli rács teljes képernyőre bővül, a rácson való navigálás a tabulátorbillentyűvel nem működik.
- Egy másik felhasználó által létrehozott időbejegyzés elküldésekor a Program helytelenül tölti ki a **Beküldött** időpont mezőt az időlapot létrehozó felhasználóval.
