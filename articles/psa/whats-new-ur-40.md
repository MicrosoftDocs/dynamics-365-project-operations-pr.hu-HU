---
title: Újdonságok vagy változások a Project Service Automation 40-es frissítési kiadásának V3 változatában
description: Ez a cikk a 40-es kiadás V3-as verziójában Microsoft Dynamics 365 Project Service Automation elérhető funkciókat és javításokat sorolja fel.
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

Ez a cikk azokat a szolgáltatásokat és javításokat sorolja fel, amelyek a Project Service Automation 40-es kiadásának 3.-as verziójához újak vagy módosultak. Ennek a verziónak a build száma V3.10.61.61, és általánosan elérhető egy önálló frissítésben 2022 februárjában.

## <a name="update-release-40"></a>40-ös frissítési kiadás

### <a name="features"></a>Funkciók
A Project Service Automationről a Project Operations - Lite-ra való frissítés 1. fázisa 2022 februárjában jelenik meg minden ügyfél számára. A jogosultság ellenőrzéséhez lásd: [Frissítés a Project Service Automationről a Project Operationsre](upgrade-project-operations-non-stocked.md). Ha az alkalmazás nem jelenik meg a példányban a Felügyeleti központban, forduljon az Power Platform ügyfélszolgálathoz, és kérje meg, hogy engedélyezze a járatot a környezetekben. A kérelemnek tartalmaznia kell azon környezeti azonosítók listáját, ahol a járatot engedélyezni kell.

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.

**Idő és költség**
- Egy jegyzetbejegyzés hiányzik, ha egy időbevitelt elutasítanak vagy törölnek. 

**Értékesítés**

- Ha a költség- vagy értékesítési becsléseket beépített beépülő modulokkal frissíti, helytelenül küldhet olyan JSON-adatcsomagokat, amelyek nem érvényesek a felhasználói felületen kívül.
- Ha a gyorsnézettel frissíti az árajánlatsorokat, aktiválhatja az idézőjeleket.
