---
title: Újdonságok vagy változások a Project Service Automation 26-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 26-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 669b3ca4601bdac483db4e1d7f55a8bf5b3d9661
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948827"
---
# <a name="project-service-automation-update-release-26-v3"></a>Project Service Automation 26-es frissítési kiadás, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3 26-os frissítési kiadásában. A Build száma V 3.10.44.59, és általánosan elérhető egy önálló frissítésként 2020 decemberében.

## <a name="update-release-26"></a>26-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

**Idő és költség**

A következő problémák kerültek kijavításra:

- A felhasználók egy jóváhagyott/elküldött időbejegyzésen módosíthatják a feladatot.
- Az időbejegyzés mentésekor az „Objektumhivatkozás nincs beállítva” hibaüzenet jelenik meg.
- Az erőforrás-hozzárendelések importálásának időrekordjainak nem megfelelő DateTime értékekkel rendelkező időbejegyzéseket hoz létre.
- Ha a Project Service Automation és a Field Service alkalmazás egyaránt telepítve van, az **Új** gomb kétszer jelenik meg a parancssávon a Field Service alkalmazás időbejegyzéseihez.
- Az **Egység engedélyezése** és az **Egységcsoport** cellái frissítései immár működnek **Költségbecslések** rácson.
- **Az időtételmódosítás frissítése** űrlap tartalmaz **Idősort**.
- A projekten kívüli időbejegyzések időjóváhagyása a projekt jóváhagyói szerepkörének keresésekor blokkolja a rendszert.

**Erőforráskezelés**

A következő problémák kerültek kijavításra:

- Hozzáadott érvényesítés a **PostProjectCreate** beépülő modulban amely ellenőrzi az elsődleges követelményt, mielőtt létrehozna egyet.
- A **Projektcsapat tagja** gyors létrehozási űrlap egy null referencia kivételt ad, ha a mezőket eltávolítja az űrlapról.
- 12 órás követelmények létrehozása egy évre vonatkozóan sikertelen lesz.
- Javított hibaüzenet null hivatkozás kivétel az erőforrásszükséglet létrehozása során.

**Projektmenedzsment**

A következő problémák kerültek kijavításra:

- Javított érvényesítés a **PreProjectUpdate** beépülő modulban létrejött null hivatkozásra vonatkozó kivételek kezelésére.
- A Microsoft Project Desktop bővítmény által közzétett projektek a törlik a nem hozzárendelt megbízásokat.
- Az új ellenőrzés hozzáadva, ha **PreValidateProjectTaskUpdate** nulla hivatkozás kivétele miatt a projekthivatkozás érvénytelen.
- A Csapattagok rácsa nem jeleníti meg a csapattagok rekordjainak különböző hozzárendeléseit.
- Hozzáadva egy új ellenőrzés és hibaüzenetek a **PreProjectTaskDelete** beépülő modul nullhivatkozás kivétele miatt.

**Sales**

A következő problémák kerültek kijavításra:

- Ha egy projekten alapuló sort egy ajánlatban vagy szerződésben választ ki, akkor a **Javaslat** gomb csak akkor látható, ha egy termékalapú sort választ ki egy meglévő termékhez.
- A **Create_Product** jogosultság le lett választva a **Create_ProjectContract** jogosultságról.
- Egy számlasor törlése nullahivatkozás hibát okoz **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice** elemnél.


[!INCLUDE[footer-include](../includes/footer-banner.md)]