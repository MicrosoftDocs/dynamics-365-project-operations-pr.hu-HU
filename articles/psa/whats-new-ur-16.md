---
title: Újdonságok vagy változások a Project Service Automation 16-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 16-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 882ee6c25e5d88db22e051254c7fd82dc787ab73
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143636"
---
# <a name="project-service-automation-update-release-16-v3"></a>Project Service Automation 16-os frissítési kiadás, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.  Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra. További információ: [Előnyben részesített telepítése, frissítése](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).
Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a PSA V3. 16-ös frissítési kiadásában. Ennek a verziónak a build száma V3.10.6.34, és általánosan elérhető egy önálló frissítésben 2020. januárjában.


## <a name="update-release-16"></a>16-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

-   Idő és költség

    -   Javítva: A felhasználók, akik törölt idő- vagy költségbejegyzéseket küldenek be jóváhagyásra mostantól ehhez kapcsolódó hibaüzenetet kapnak.

-   Projektmenedzsment

    -   Javítva: A sablonokban a csapattagokhoz definiált erőforrásegységek figyelembe lesznek véve a sablonokban, és alkalmazva lesznek az új projektre.

    -   Javítva: Bejegyzések tulajdonjogának újbóli hozzárendelésének továbbfejlesztett kezelése.

    -   Javítva A másolás alatt álló projektek másolása az összes másolási művelet befejezéséig nem engedélyezett.

-   Erőforráskezelés

    -   Javítva: A foglalások meghosszabbítása mostantól helyesen kezeli a rövid időtartamokat, és a továbbiakban nem hoz létre nulla órákat a meghosszabbított foglalásokhoz.

    -   Javítva: Az egyeztetési nézet immár megjelenítésre kerül, ha a projekt időzónája +5:30 GMT és a felhasználó időzónája eltérő.

-   Sales

    -   Javítva: Egy szerződéssorhoz társított projekt eltávolítása és egy új projekt társítása esetén az új projektben szereplő tényadat-bejegyzések nem lettek újra kiértékelve a szerződéssorhoz definiált számlázási és árképzési szabályok alapján. Ez ebben a kiadásban ez javítva lett. A projekthez újonnan társított árképzési és tényadat-bejegyzések a szerződéssor árazási és számlázási szabályai alapján vissza lesznek állítva, és helyesen lesznek létrehozva. A megszüntetett hozzárendelésű projekt tényadat-bejegyzései ennek megfelelően újra lesznek értékelve, és újra létre lesznek hozva.

    -   Javítva: A rendszer további ellenőrzést kapott a becslési sor **Összeg** mezőjéhez így biztosítva, hogy a nulla értékek ne maradjanak meg.

    -   Javítva: Ha a tényadatokat frissítették egy projekten, akkor a program a projekt fő űrlapjára megjelenik egy frissítés gomb, hogy a felhasználók újra szinkronizálhassák a tényadatokat.

    -   Javítva: Amikor a felhasználók 2.X verzióról a 3.X verzóra a NULL projektnévértű projektek megengedettek.



[!INCLUDE[footer-include](../includes/footer-banner.md)]