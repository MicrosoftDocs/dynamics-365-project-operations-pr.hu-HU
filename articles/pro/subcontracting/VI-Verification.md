---
title: A szállítói számlák ellenőrzése jóváhagyott tényadatokkal
description: Ez a cikk ismerteti, hogyan teszi lehetővé a Microsoft Dynamics 365 Project Operations projektvezetők számára a szállítói számlákat ellenőrzését a jóváhagyott tényadatokkal, miután az alvállalkozók elvégezték a munkát és rögzítették az időt a kiadásokat és az anyagokat, amelyeket a projektcsoporttagok felhasználtak.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 67e0a0143fa354ca9a87bfac5fbbd6306a97811c
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522950"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>A szállítói számlák ellenőrzése jóváhagyott tényadatokkal

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Microsoft Dynamics 365 Project Operations segítségével a projektmenedzserek a következőképpen ellenőrizhetik a szállítói számlasorokat:

- Használhatják a szállítói számlasorok **Ellenőrzési állapot** mezőjét.
- Ha a szállító számlasorai egy alvállalkozói sorra hivatkoznak, akkor az alvállalkozói tevékenység költség tényadatai az adott szállítói számlasorhoz vannak társítva. Ez a hivatkozás a költség tényadatai és a szállító számlasorokhoz történő egyeztetésével jön létre.

    > [!NOTE]
    > Annak ellenére, hogy az ellenőrzés állapota nyomon követhető az alvállalkozói szerződésre nem hivatkozó szállítói számlasorokhoz is, a költség tényadatait nem lehet az adott szállítói számlasorokhoz kapcsolni.

## <a name="verification-status"></a>Ellenőrzés állapota

A szállítói számlasor **Ellenőrzési állapot** mezője az ellenőrzés állapotát jelzi. A következő állapotok támogatottak:

1. Nem kezdődött el
2. Folyamatban
3. Teljesítés

A **Nincs elkezdve** ellenőrzési állapotú szállítóiszámla-sorokat lehet szerkeszteni.

A **Folyamatban** ellenőrzési állapotú szállítóiszámla-sorokat már nem lehet szerkeszteni. Az alvállalkozói szerződésre hivatkozó szállítói számlasorok ellenőrzési állapota automatikusan **Folyamatban** állapotúra van állítva, amint az első költség-tényadat megfeleltetve lett a szállítói számlasornak.

A **Kész** ellenőrzési állapotú szállítóiszámla-sorokat már nem lehet szerkeszteni. Ha egy szállítói számla összes sorának ez az ellenőrzési állapota, a szállítói számlát meg lehet erősíteni.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Aktuális költségek egyeztetése szállítói számlasorokkal

A költség-tényadatok egyeztetése segíti a szállítói számlasor ellenőrzési folyamatát. A költség tényadatainak egy szállítói számlasorhoz való egyeztetéshez hajtsa végre a következő lépéseket.

1. Nyissa meg a szállítói számlasort, és válassza a **Nem egyeztetett tényleges költségek** lapot. A rács azokat a tényleges költségeket jeleníti meg, amelyek a szállító számlasorával azonos alvállalkozói sorra hivatkoznak.
2. Jelöljön ki egy vagy több tényleges költséget, majd válassza a rács feletti eszköztár **Egyeztetés** gombját. A rendszer ellenőrzi, hogy a kiválasztott tényleges költségek egyeztethetőek-e. Az ellenőrzés után a tényleges költéségek össze vannak kapcsolva a szállítói számlasorral.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>A tényleges költségek szállítói számlasorokhoz való kapcsolásához használt ellenőrzési feltételek

Az egyeztetési folyamat során csak akkor lehet kapcsolatot létrehozni a tényleges költség és a szállítói számlasor között, ha mindkét alábbi feltétel teljesül:

- A **Korrekció állapota** mezőnek üresnek kell lennie minden egyes kiválasztott tényleges költséghez. Más szavakkal, a tényleges költségek nem lettek lecserélve más tényleges költségekkel a jóváhagyási, visszavonási vagy korrekciós napló foyamata során.
- A következő mezők értékei egyeztetve vannak a szállítói számlasor és a kiválasztott tényleges költség között. Ha valamelyik mező nincs beállítva a szállító számlasoron, akkor az nem lesz figyelembe véve az egyeztetéshez.

    - Projektszerződés
    - Projektszerződéssor
    - Tranzakcióosztály
    - Project
    - Feladatok
    - Erőforrás-kategória
    - Tranzakció kategóriája
    - Termék
    - Alvállalkozóiszerződés-sor
    - Lefoglalható erőforrás

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Aktuális költségek és a szállítóiszámla-sor egyeztetésének megszüntetése

A tényleges költségek egyeztetésének megszüntetése is segíthet egy szállítói számla ellenőrzési folyamatában, hiszen lehetővé teszi a korábban létrehozott hivatkozások eltávolítását. Csak a **Folyamatban** ellenőrzési állapotú szállítóiszámla-sorokat kapcsán lehet a tényleges költségek egyeztetését megszűntetni. A költség tényadatainak egy szállítói számlasorhoz való egyeztetésének megszüntetéséhez hajtsa végre a következő lépéseket.

1. Nyissa meg a szállítói számlasort, és válassza az **Egyeztetett tényleges költségek** lapot. A rács azokat a tényleges költségeket jeleníti meg, amelyek a szállító számlasorra hivatkoznak.
2. Jelöljön ki egy vagy több tényleges költséget, majd válassza a rács feletti eszköztár **Leválasztás** gombját.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
