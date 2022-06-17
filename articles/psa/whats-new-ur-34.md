---
title: Újdonságok vagy változások a Project Service Automation 34-es frissítési kiadásának V3 változatában
description: Ez a cikk a Project Service Automation 34-es, V3-as kiadásában elérhető funkciókat és javításokat sorolja fel.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: e47a5442f285952c165a2d30e337a362a6b065dd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928665"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Újdonságok vagy változások a Project Service Automation 34-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a cikk a Project Service Automation V3 3. verziójának 34. kiadásának újdonságaival és fejlesztéseivel kapcsolatos szolgáltatásokat és javításokat sorolja fel. Ennek a verziónak a buldszáma V3.10.55.38, és általánosan elérhető 2021. júliusában önálló frissítésen keresztül.

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
