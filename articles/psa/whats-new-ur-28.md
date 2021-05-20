---
title: Újdonságok vagy változások a Project Service Automation 28-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 28-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2d5e8c629f8108ed039948ca70842c9d8afebfa6
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948689"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Újdonságok vagy változások a Project Service Automation 28-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy módosultak a Project Service Automation V3 verzió 28-es frissítéskiadásnál. Ez a verzió a V3.10.46.32 buildszámmal rendelkezik, és 2021 januárjában általánosan elérhető egy önkiszolgáló frissítéssel.

## <a name="update-release-28"></a>28-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

**Idő és költség**

A következő problémák kerültek kijavításra:

- A felhasználók a **Tömeges szerkesztés** segítségével frissíthetik a jóváhagyott és elküldött időbejegyzéseket.

**Projektmenedzsment**

A következő problémák kerültek kijavításra:

- Azokban az esetekben, amikor a tevékenység GUID-azonosítóját számként értelmezi, a tevékenységek nem nyithatók meg szerkesztésre **Munkalebontási struktúra** lap menüszalagján található **Tevékenység szerkesztése** használatával.

**Sales**

A következő problémák kerültek kijavításra:

- Egy nulla hivatkozási kivétel jön létre a **GetEstimatesForProject** beépülő modul meghívásakor.
- A mérföldkő rácson **Számlakészként megjelölés** csak részben frissíti az attribútumokat, kivéve a frissített **InvoiceStatus** attribútumot.



[!INCLUDE[footer-include](../includes/footer-banner.md)]