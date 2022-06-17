---
title: Újdonságok vagy változások a Project Service Automation 43-es frissítési kiadásának V3 változatában
description: Ez a cikk a 43-as kiadás V3-as verziójában Microsoft Dynamics 365 Project Service Automation elérhető funkciókat és javításokat sorolja fel.
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
ms.openlocfilehash: b12cfda08f1ea1fc441782003130be445a437f7c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915325"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Újdonságok vagy változások a Project Service Automation 43-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a cikk azokat a szolgáltatásokat és javításokat sorolja fel, amelyek a Project Service Automation 43-as, V3-as kiadásának újdonságai vagy módosításai. A verzió build száma V3.10.74.200, és általánosan elérhető lesz önálló frissítésként 2022 májusában.

## <a name="update-release-43"></a>43-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.


**Idő és költség**

- Amikor időbejegyzéseket importál foglalásokból vagy erőforrás-hozzárendelésekből, a kapcsolódó foglalható erőforrásra való hivatkozás nem marad meg.
- Ha az időbeviteli rács teljes képernyősre van kibontva, a tab billentyűvel való navigálás a rácsban nem működik.
- Egy másik felhasználó által létrehozott időbevitel elküldésekor a **Beküldés dátuma** mező helytelenül lesz feltöltve azzal a felhasználóval, aki létrehozta az időlapot.
