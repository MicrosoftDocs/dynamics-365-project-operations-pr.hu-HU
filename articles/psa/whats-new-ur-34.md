---
title: Újdonságok vagy változások a Project Service Automation 34-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 34-os frissítési kiadásában.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: 528d4f8d108720cb9c912cea1c0d5f37e3716eec
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323284"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Újdonságok vagy változások a Project Service Automation 34-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 34-es frissítési kiadásában. Ennek a verziónak a buldszáma V3.10.55.38, és általánosan elérhető 2021. júliusában önálló frissítésen keresztül.

## <a name="update-release-34"></a>34-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások
A következő problémák kerültek kijavításra.

**Általános**

- A közzétevő által vezérelt frissítések nem aktiválják az új, modern jóváhagyási munkafolyamatot.
- Hiányzik a **Célállapot** és **Művelettípus** attribútum a **Jóváhagyáskészlet** főoldalán.

**Idő és költség**

- A modern jóváhagyási folyamat segítségével nem lehet jóváhagyni visszahívási kérést.
- A heti bejegyzések másolása nem működik, ha a felhasználóhoz nem kapcsolódó bejegyzéseket másol.

**Projekt tervezése**

- Az erőforrások hozzárendelési feladatai sérültek a Microsoft Project asztali bővítményből történő importáláskor.

**Erőforrás-kezelés**

- Ha egy projektet teszt közzé a Microsoft Project asztali ügyfélprogram bővítményéből, a meglévő követelmények záró dátuma megváltozik.
- A tizedesjegyek pontossága meghaladja a két tizedesjegyet a foglalások kiterjesztése megerősítő párbeszédpanelen.

**Értékesítés**

- Ha egy meglévő termékkel termékalapú sort ad hozzá egy projektszerződéshez, megjelenik egy **kulcs nem található a szótárban** kivétel.
- Az érdeklődők nem minősítőek, ha egy megrendeléstípust egy érdeklődőből lehetőségre leképeznek.
