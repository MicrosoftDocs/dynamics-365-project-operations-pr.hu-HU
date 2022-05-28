---
title: Újdonságok vagy változások a Project Service Automation 39-es frissítési kiadásának V3 változatában
description: Ez a témakör a Microsoft Dynamics 365 Project Service Automation Update Release 39, V3 verzióban elérhető funkciókat és javításokat sorolja fel.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.openlocfilehash: 1d198f9ad9144f5cc2f533fa9603e1f1a181c8b6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588739"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Újdonságok vagy változások a Project Service Automation 39-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3 39-os frissítési kiadásában. Ez a verzió A V3.10.60.170 buildszámmal rendelkezik, és általában 2022 januárjában önfrissítéssel érhető el.

## <a name="update-release-39"></a>39-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.

**Általános**

- Számos fejlesztés történt az arab fordítás webhelytérképén.

**Projektmenedzsment**

- Hiba lép fel, ha a projektmenedzsert olyan felhasználóra módosítja, aki már csapattag a projektben.

**Értékesítés**

- A Projektszerződés árlistájának **tulajdonosa** helytelenül jelenik meg az árlista automatikus létrehozásakor. 
- Az árlista dátumhatékonyságát a program nem tartja tiszteletben, ha az árlista a projektparaméterre van alkalmazva.
- Előfordulhat, hogy az összehúzó egység nem rendelkezik a megfelelő alapértelmezett értékkel két különálló ajánlat szerkesztésekor.
