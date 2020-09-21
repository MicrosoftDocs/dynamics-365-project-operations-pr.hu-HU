---
title: Újdonságok a Project Service Automation 16-ös frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 16-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: b890a7b6-1664-4812-8732-fed77653cc05
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0f4c206fd5b7a36d940e966b28c2437525812a98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752222"
---
# <a name="project-service-automation-v3-update-release-16"></a>Project Service Automation V3, 16-ös frissítési kiadás
Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.

Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra. További információ: [Előnyben részesített telepítése, frissítése](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page). Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a PSA V3. 16-ös frissítési kiadásában. Ennek a verziónak a build száma V3.10.6.34, és általánosan elérhető egy önálló frissítésben 2020. januárjában.

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

