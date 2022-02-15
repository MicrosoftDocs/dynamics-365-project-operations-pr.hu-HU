---
title: Újdonságok vagy változások a Project Service Automation 37-es frissítési kiadásának V3 változatában
description: Ez a témakör a Microsoft Dynamics 365 Project Service Automation Update Release 37, V3 verzióban elérhető funkciókat és javításokat sorolja fel.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: 7bd00ccbb09fb43f7d7c3e0fef888a4e9dfcc752
ms.sourcegitcommit: f888e9c6e0290608abb915aa599ae9629b0efd3e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/01/2021
ms.locfileid: "7727608"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Újdonságok vagy változások a Project Service Automation 37-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3 37-os frissítési kiadásában. Ennek a verziónak a buildszáma V3.10.58.120, és általában 2021 novemberében önfrissítéssel érhető el.

## <a name="update-release-37"></a>37-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.

**Idő és költség**
- A felhasználók a cella törlésével nem törölhetik az időbejegyzést.
- A **Saját sikertelen jóváhagyás** nézet csak **Elküldött** állapotú projekt-jóváhagyásokat tartalmazza.

**Projektmenedzsment**
- A felhasználók null hivatkozási kivételt kapnak a projekt Microsoft asztali bővítményben való megnyitásakor, ha a projekt csoporttagja üres.
- A **Projektfeladat** lapon nincs **Mentés** gomb, így a felhasználók nem menthetik a feladatrekordok módosításait.
- A felhasználók nem törölhetnek olyan projektet, amely **Megnyert** állapotú ajánlathoz feladatot társít.

**Értékesítés**
- A Program a **Projekt** lapon a **Pénznem** mezőt a módosított sablon pénznemének megfelelően frissíti.
- A több pénznemmel is rendelkező feladatok esetén helytelenül számítja ki a rendszer a költségeket.