---
title: Újdonságok vagy változások a Project Service Automation 45-es frissítési kiadásának V3 változatában
description: Ez a cikk a 45-ös kiadás V3-as verziójában Microsoft Dynamics 365 Project Service Automation elérhető funkciókat és javításokat sorolja fel.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169179"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Újdonságok vagy változások a Project Service Automation 45-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a cikk azokat a funkciókat és javításokat sorolja fel, amelyek a Project Service Automation 45-ös, V3-as kiadásának újdonságai vagy módosításai. Ennek a verziónak a buldszáma V3.10.76.168, és általánosan elérhető 2022. júliusában önálló frissítésen keresztül.

## <a name="update-release-45"></a>45-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.

**Értékesítés**

- A felhasználók nem hozhatnak létre sikeresen számlákat, miután megpróbálnak számlát létrehozni rendezetlen értékesítések nélkül, ha az oldal ugyanazon példányát is megtekintik, és nem frissítik.

**Idő és költség**

- Ha a modern jóváhagyások engedélyezve vannak, és egy visszahívott projektjóváhagyást hagynak jóvá, a rekordszakasz helytelenül frissül **a Visszavont kérelemre**.
- Ha a Modern jóváhagyások engedélyezve van, és a Cloud Flows inaktív, a jóváhagyási folyamat nem sikeres, és a felhasználók beküldése vagy jóváhagyása nem kap értesítést.
