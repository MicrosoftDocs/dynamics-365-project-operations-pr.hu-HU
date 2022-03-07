---
title: Újdonságok vagy változások a Project Service Automation 27-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 27-os frissítési kiadásában.
author: ruhercul
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
ms.openlocfilehash: ee7bbe888a982e3554ba524c67442437c9be9183a5ee0940ccc3261b4a4992e7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985054"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Újdonságok vagy változások a Project Service Automation 27-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 27-es frissítési kiadásában. Ennek a verziónak a build száma V3.10.45.98, és általánosan elérhető egy önálló frissítésben 2021. januárjában.

## <a name="update-release-27"></a>27-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

**Általános**

A következő problémák kerültek kijavításra:

- A Project Service Automation beépülő moduljai által létrehozott naplók nincsenek automatikus törlésre állítva.
- Az automatikus frissítés sikertelen, mert a Project Service Automation megoldás örökölt null NavBarArea és cím elemet tartalmaz.

**Idő és költség**

A következő problémák kerültek kijavításra:

- Az **Időbejegyzés** rács helytelen adatokat jelenít meg az **Időzónától független** dátum viselkedéséhez.
- Az **Időbejegyzés** rács helytelen időt hoz létre az **Időzónától független** dátum viselkedéséhez.
- A tevékenység keresése nem korlátozódik a kijelölt projektre az **Időbejegyzés szerkesztése** lapon.
- A projekten kívüli időbejegyzések időjóváhagyása a projekt jóváhagyójának keresésekor blokkolja a rendszert.
- A Tényadatok helyes bejegyzései helytelen hibaüzenetet jelenítenek meg.
- Ha egy feladat null értéket tartalmaz a tényleges költségnél, és a projekt összesítései frissülnek, a következő hiba történik: „Az adott kulcs nem létezik a szótárban”.
- Bizonyos esetekben a **Projektbecslés** fülön lévő **Csoportosítás** szűrők nem jelenítik meg a költségbecsléseket.
- A **Nyári időszámítás** időintervalluma nem megfelelő az időbejegyzések esetében.

**Projektmenedzsment**

A következő problémák kerültek kijavításra:

- A gyorsítótárazási fejlesztések, amelyek növelik a **Projekt** oldal betöltésével kapcsolatos teljesítményt.
- Egy elavult üzleti szabály megakadályozza a projektfeladatok elvégzését.
- A Microsoft Project bővítménykontúrok nem tartják tiszteletben a bővítmény naptárát, ami helytelen erőforrás-követelményeket eredményez.
- A projektek sablonokból történő létrehozása helytelenül állítja be a hozzárendelési dátumokat, és megakadályozza az erőforrás-követelmények létrehozását.
- A felhasználó nem tudja elérni a **Kategória**, **Leírás**, **Állapot** lehetőségeket a billentyűzet használatával.
- A projekt tényleges értékesítési értékei nem tartalmaznak díj- és anyagértékesítési értékeket.
- A tényleges értékesítések és a tényleges költségek összesítése helytelenül és különböző árfolyamokkal történik.
- Az **Alapértelmezett munkaóra sablon** leírása félrevezető.
- A feladat behúzása addig nem távolítja el a **Kategória** parancsot a felhasználói felületen, amíg nem frissül.
- Az ellenőrzés kihagyása annak biztosítása érdekében, hogy a projekt a befejezési dátumon belül teljesüljön, nem engedélyezett.

**Sales**

A következő problémák kerültek kijavításra:

- A projekt ajánlatsorán null hivatkozási kivétel jön létre, mert az **Importálás projektbecslésből** akkor látható, ha a projekt nincs kiválasztva.
- Az „Objektumhivatkozás nincs objektumpéldányra állítva” hibaüzenet akkor jelenik meg, amikor egy ajánlatot **Megnyert** állapotban zárnak le.
- A korrekció állapota a tényleges sztornírozás során nincs megadva a projekt szerződéssorról történő leválasztása közben.
- Ha a Dynamics 365 Field Service és a Project Service Automation egyaránt telepítve van, a **Zárolási díjszabás** és az **Aktuális díjszabás használata** beállítás nem jelenik meg egyszerre a **Számla** lapon.
- A japán nyelv esetében nincs más naptáralapú oldalakkal konzisztens fordítás.
- Az **Aktiválás** és **Inaktiválás** el lett távolítva a Project Service Automation **Árlistatársítás** entitásaiból.


[!INCLUDE[footer-include](../includes/footer-banner.md)]