---
title: Újdonságok vagy változások a Project Service Automation 25-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 25-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: aabee3fe755e33d2c0f01a96b6f53a68957bc041
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143754"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Újdonságok vagy változások a Project Service Automation 25-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy módosultak a Project Service Automation V3 verzió 25-ös frissítéskiadásnál Ez a verzió a V 3.10.43.76 buildszámmal rendelkezik, és 2020 októberében általánosan elérhető egy önkiszolgáló frissítéssel.

## <a name="update-release-25"></a>25-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

**Idő és költség**

A következő probléma ki lett javítva:

- Időbejegyzés-diagram további adatokat mutatott a túl nagy beolvasott intervallum esetén.

**Erőforráskezelés**

A következő probléma ki lett javítva:

- Hozzáadtunk egy további Package Deployer-kódot, amellyel a Universal Resource Scheduling javítás kihagyható, ha létezik magasabb verziójú javítás.

**Projektmenedzsment**

A következő problémák kerültek kijavításra:

- Javítottuk a kerekítési és árfolyam-eltéréseket, amelyek helytelen tervezett költséget eredményeztek a projektkövetési rácsban.
- Támogatja a **projekt** űrlapon két vagy több reagáló rács megjelenítését.
- Ellenőrzést adtunk hozzá, hogy foglalkozzunk a feladat naptári záró dátum utáni hozzáadási képességével, amely sikertelen erőforrás-hozzárendeléshez vezet.
- Javított hibakezelés a következőkből előállított null hivatkozás-kivétel kezelésére:

    - **PreValidateProjectTeamMemberCreate** beépülő modul
    - **PreValidateProjectTaskCreate**, ha társított projekt nélkül jön létre a Projektfeladat
    - **PreProjectTeamMemberCreate** beépülő modul
    - **PostProjectTeamMemberDelete** beépülő modul
    - **PreValidateProjectTaskDelete** beépülő modul

**Sales**

A következő problémák kerültek kijavításra:

- Javított hibakezelés a következőből létrehozott nulla hivatkozású kivételek kezelésére: **Projekt másolása: becslések HelperResource kezelése**.
- **Nem számlázásra kész** az **idő- és anyagelszámolású számlázási lemaradás** esetén nem törli a számlázási állapotot.
- Javítottuk a helytelenül címkézett **Árak** gombokat a **Szerepkörárak** és **Katalóguscikkek** lapon.
