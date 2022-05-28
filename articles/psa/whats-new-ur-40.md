---
title: Újdonságok vagy változások a Project Service Automation 40-es frissítési kiadásának V3 változatában
description: Ez a témakör a Microsoft Dynamics 365 Project Service Automation Update Release 40, V3 verzióban elérhető funkciókat és javításokat sorolja fel.
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
ms.openlocfilehash: 25f375ce648eb7d233f6433739832caee351830d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588647"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Újdonságok vagy változások a Project Service Automation 40-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3 40-os frissítési kiadásában. Ennek a verziónak a build száma V3.10.61.61, és általánosan elérhető egy önálló frissítésben 2022 februárjában.

## <a name="update-release-40"></a>40-ös frissítési kiadás

### <a name="features"></a>Funkciók
A Project Service Automation-ről a Project Operations - Lite-ra történő frissítés 1. fázisa 2022 februárjában jelenik meg minden ügyfél számára. A jogosultság ellenőrzéséhez olvassa el a Frissítés a projektszolgáltatás automatizálásáról a projektműveletekre című [témakört](upgrade-project-operations-non-stocked.md). Ha az alkalmazás nem jelenik meg a példányban az Admin Centerben, lépjen kapcsolatba az Power Platform ügyfélszolgálattal, és kérje, hogy engedélyezze a járatot a környezetekben. A kérésnek tartalmaznia kell azoknak a környezeti azonosítóknak a listáját, amelyekben engedélyezni kell a járatot.

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.

**Idő és költség**
- Egy megjegyzésbejegyzés hiányzik, ha egy időbejegyzést elutasítanak vagy visszavonnak. 

**Értékesítés**

- Ha a költség- vagy értékesítési becsléseket beépített beépülő modulokkal frissíti, helytelenül küldhet olyan JSON-hasznos adatokat, amelyek nem érvényesek a felhasználói felületen kívül.
- Ha az ajánlatsorokat a gyorsnézettel frissíti, aktiválhatja az ajánlatokat.
