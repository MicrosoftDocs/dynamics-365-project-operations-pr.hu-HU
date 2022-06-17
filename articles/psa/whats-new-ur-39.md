---
title: Újdonságok vagy változások a Project Service Automation 39-es frissítési kiadásának V3 változatában
description: Ez a cikk a 39-es kiadás V3-as verziójában Microsoft Dynamics 365 Project Service Automation elérhető funkciókat és javításokat sorolja fel.
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
ms.openlocfilehash: d5b5938762d98acaead9e26c47bce07e0059faf6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922455"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Újdonságok vagy változások a Project Service Automation 39-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a cikk a Project Service Automation 39-es, V3-as kiadásának újdonságaival vagy módosításaival kapcsolatos szolgáltatásokat és javításokat sorolja fel. Ez a verzió buildszáma V3.10.60.170, és általánosan elérhető egy önfrissítéssel 2022 januárjában.

## <a name="update-release-39"></a>39-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.

**Általános**

- Számos fejlesztés történt az arab fordítás oldaltérképén.

**Projektmenedzsment**

- Hiba történik, ha egy projekt projektmenedzserét olyan felhasználóra módosítja, aki már csapattag a projektben.

**Értékesítés**

- A Projektszerződés árlistájának **tulajdonosa** helytelen, ha az árlista automatikusan létrejön. 
- Az árlista dátumhatékonyságát a rendszer nem veszi figyelembe, ha az árlistát alkalmazza a projektparaméterre.
- Előfordulhat, hogy a szerződő egység nem rendelkezik a megfelelő alapértelmezett értékkel két külön idézőjel szerkesztésekor.
