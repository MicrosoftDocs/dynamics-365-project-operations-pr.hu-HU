---
title: Újdonságok vagy változások a Project Service Automation 40-es frissítési kiadásának V3 változatában
description: Ez a cikk a Microsoft Dynamics 365 Project Service Automation Update Release 40, V3 verzióban elérhető funkciókat és javításokat sorolja fel.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912795"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Újdonságok vagy változások a Project Service Automation 40-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a cikk felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3 40-os frissítési kiadásában. Ennek a verziónak a build száma V3.10.61.61, és általánosan elérhető egy önálló frissítésben 2022 februárjában.

## <a name="update-release-40"></a>40-ös frissítési kiadás

### <a name="features"></a>Funkciók
A Project Service Automation és a Project Operations – Lite közötti frissítés 1. fázisa 2022 februárjában minden ügyfél számára elérhető lesz. A jogosultság ellenőrzéséhez tekintse meg a [Frissítés a Project Service Automation szolgáltatásról Project Operations – Lite szolgáltatásra](upgrade-project-operations-non-stocked.md) című cikket. Ha az alkalmazás nem jelenik meg a példányán a Power Platform felügyeleti központban, forduljon a támogatáshoz, és kérje a tesztelés engedélyezését a környezet számára. Kérésének tartalmaznia kell azon környezetazonosítók listáját, ahol engedélyezni kell a tesztelést.

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.

**Idő és költség**
- Egy jegyzetbejegyzés akkor hiányzik, amikor egy időbejegyzést elutasítanak vagy visszavonnak. 

**Értékesítés**

- Ha gyári beépülő modulokon frissíti a költség- vagy értékesítésibecsléseket, helytelenül engedélyezve lesz Önnek a JSON hasznos adatok küldése, amelyek a felhasználói felületen kívül nem érvényesek.
- Ha a betekintő nézet használatával frissíti az árajánlatsorokat, akkor az árajánlatok aktiválása engedélyezett Önnek.
