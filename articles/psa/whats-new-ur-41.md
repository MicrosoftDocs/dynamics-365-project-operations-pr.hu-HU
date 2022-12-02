---
title: Újdonságok vagy változások a Project Service Automation 41-es frissítési kiadásának V3 változatában
description: Ez a cikk a Microsoft Dynamics 365 Project Service Automation Update Release 41, V3 verzióban elérhető funkciókat és javításokat sorolja fel.
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930551"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Újdonságok vagy változások a Project Service Automation 41-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a cikk felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3 41-os frissítési kiadásában. Ennek a verziónak a build száma V3.10.62.162, és általánosan elérhető egy önálló frissítésben 2022 márciusában.

## <a name="update-release-41"></a>41-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.

**Projektmenedzsment**
- Amikor az asztali bővítményből létrehozott projekten alapuló sablonból kísérel meg projektet létrehozni, a következő hibaüzenet jelenik meg: „Az erőforrás-hozzárendelés tervezett munka mezőjének ellenőrzése: Az egyes erőforrás hozzárendelési időszeletek záró dátuma nem lehet korábbi a kezdő dátumnál”.

**Idő és költség**
- Amikor megpróbál törölni egy időbejegyzést, a következő hibaüzenet jelenik meg: „Váratlan hiba történik az ISV-kódból”.

**Értékesítés**
- Ha egy rögzített árú mérföldkőhöz számlát hoz létre, a rendszer nem tölti ki a **Leírás** és a **Külső leírás** mezőket. 
