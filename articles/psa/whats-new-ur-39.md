---
title: Újdonságok vagy változások a Project Service Automation 39-es frissítési kiadásának V3 változatában
description: Ez a cikk a Microsoft Dynamics 365 Project Service Automation Update Release 39, V3 verzióban elérhető funkciókat és javításokat sorolja fel.
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

Ez a cikk felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3 39-os frissítési kiadásában. Ennek a verziónak a build száma V3.10.60.170, és általánosan elérhető egy önálló frissítésben 2022. januárjában.

## <a name="update-release-39"></a>39-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.

**Általános**

- Arab fordításhoz számos továbbfejlesztés történt az oldaltérképen.

**Projektmenedzsment**

- Hiba történik, ha a projektvezetőt olyan felhasználóra módosítja a projekten, aki már csoporttag a projekten.

**Értékesítés**

- Helytelen a **Projekt szerződés árlista** tulajdonosa az árlista automatikus létrehozásakor. 
- Nincs figyelembe véve az árlista érvényességi dátuma amikor az árlistát alkalmazza a projektparaméterre.
- Előfordulhat, hogy két külön árajánlat szerkesztése során a szerződő egység nem a megfelelő alapértelmezett értéket használja.
