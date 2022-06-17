---
title: Újdonságok vagy változások a Project Service Automation 28-es frissítési kiadásának V3 változatában
description: Ez a cikk a Project Service Automation 28-as, V3-as kiadásában elérhető szolgáltatásokat és javításokat sorolja fel.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 56a87bce55c560e541e20709b10d38b9512ffcee
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930597"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Újdonságok vagy változások a Project Service Automation 28-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a cikk azokat a funkciókat és javításokat sorolja fel, amelyek újak vagy módosultak a Project Service Automation V3, Update Release 28 ez a verzió buildszáma V3.10.46.32, és általánosan elérhető egy önfrissítéssel 2021 januárjában.

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
