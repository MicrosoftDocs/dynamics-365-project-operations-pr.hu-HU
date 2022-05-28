---
title: Újdonságok vagy változások a Project Service Automation 41-es frissítési kiadásának V3 változatában
description: Ez a témakör a Microsoft Dynamics 365 Project Service Automation Update Release 41, V3 verzióban elérhető funkciókat és javításokat sorolja fel.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 649d8bca36fda0a09dc7230ee4d742cadb32f3b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580919"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Újdonságok vagy változások a Project Service Automation 41-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3 41-os frissítési kiadásában. Ez a verzió buildszáma V3.10.62.162, és általában 2022 márciusában önfrissítéssel érhető el.

## <a name="update-release-41"></a>41-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.

**Projektmenedzsment**
- Amikor olyan sablonból próbál projektet létrehozni, amely az asztali bővítményből létrehozott projekten alapul, a következő hibaüzenet jelenik meg: "Erőforrás-hozzárendelés tervezett munkamező-érvényesítése: Minden erőforrás-hozzárendelési időszelet befejezési dátuma nem lehet korábbi, mint a kezdési dátum".

**Idő és költség**
- Amikor megpróbál törölni egy időbejegyzést, a következő hibaüzenet jelenik meg: "Váratlan hiba következik be az ISV-kódból".

**Értékesítés**
- Ha számlát hoz létre egy rögzített árú mérföldkőhöz, a Leírás **és** a **Külső leírás** mező nem lesz kitöltve. 
