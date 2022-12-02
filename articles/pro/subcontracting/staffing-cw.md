---
title: Projekt felszerelése szerződéses alkalmazottakkal és az alvállalkozói szerződésben rögzített kapacitással
description: Ez a cikk ismerteti, hogyan lehet a projektkövetelményeket szerződéses dolgozók vagy alvállalkozói kapacitás használatával kiosztani a Microsoft Dynamics 365 Project Operations alkalmazásban.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 30e16efeed93ab4568eac57fb3ed46067a08524d
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522438"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Projekt felszerelése szerződéses alkalmazottakkal és az alvállalkozói szerződésben rögzített kapacitással

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A projekt általános csoporttagjai alkalmazottakat kioszthatók alkalmazottak vagy szerződéses munkavállalók számára. Ha egy projekten szerződéses dolgozókat alkalmaz, akkor a kiosztási lehetőségeket egy adott alvállalkozói sorhoz rendelt szerződéses dolgozókra korlátozhatja. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Munkatársak erőforrás-követelményeinek keresése adott alvállalkozói sorhoz tartozó szerződésen dolgozókkal

Munkatársak erőforrás-követelményeinek kereséséhez adott alvállalkozói sorhoz tartozó szerződésen dolgozókkal kövesse az alábbi lépéseket:

1. Hozzon létre egy általános projektcsoporttagot, aki alvállalkozói szerződésre és alvállalkozói sorra hivatkozik.
2. Hozzon létre erőforrás-követelményeket ehhez az általános projektcsoporttaghoz a projektcsoporttagok alrács **Követelmény létrehozása** gombjával.
3. Jelölje ki a csoporttag sorát, majd az alrácson válassza a **Foglalás** gombot. 
4. Ezzel megnyitja az ütemezési táblát a követelmény környezetében. Az egyéb attribútumokkal, például a dátumokkal, a szerepkörrel és a szervezeti egység mezőkkel együtt az Ütemezési tábla szűrői automatikusan ki vannak töltve is a szállító, alvállalkozói szerződés és alvállalkozói sor elemekkel is az erőforrás-követelményből.
5. A rendszer a szűrőfeltételeknek megfelelő erőforrásokat keres, és listázza azokat. 
6. Jelölje ki az egyik szűrt erőforrást, és foglalja le a követelményhez az erőforrást. 
7. Létrejön egy projektcsoporttag, és frissítve lesz alvállalkozói szerződéssel és alvállalkozói sor hivatkozásaival. A **Projektbecslések** részen az **Árak frissítése** lehetőséget választva láthatja az erőforrás-hozzárendelés frissített költségét. 

> [!NOTE]
> Ha az erőforrás több alvállalkozói sorhoz is hozzá van rendelve, akkor a projektcsoport tagjainak frissítése nem minden esetben lehetséges a foglalás során. Ha a rendszer nem tudja frissíteni a projektcsoporttagot egy alvállalkozói szerződéssel és egy alvállalkozói sorral, akkor nyissa meg a projektcsoporttag rekordját, és manuálisan frissítse ezeket a mezőket, hogy a pénzügyi költségbecslés pontosan tükrözze az alvállalkozó költségét.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Erőforráskövetelmények keresése és kiosztás bármely szerződéses dolgozónak

Erőforráskövetelmények kereséséhez és kiosztásához bármely szerződéses dolgozónak kövesse az alábbi lépéseket:

1. Általános projektcsoporttag létrehozása.
2. Hozzon létre erőforrás-követelményeket ehhez az általános projektcsoporttaghoz a projektcsoporttagok alrács **Követelmény létrehozása** gombjával.
3. Jelölje ki a csoporttag sorát, majd az alrácson válassza a **Foglalás** gombot. 
4. Ezzel megnyitja az ütemezési táblát a követelmény környezetében. Az egyéb attribútumokkal, például a dátumokkal, a szerepkörrel és a szervezeti egység mezőkkel együtt az Ütemezési tábla szűrői automatikusan ki vannak töltve is a szállító, alvállalkozói szerződés és alvállalkozói sor elemekkel is az erőforrás-követelményből. Mivel a követelményhez nem volt kitöltve alvállalkozói szerződés vagy alvállalkozói sor érték, ezek az attribútumok üresek lesznek a szűrőpanelen.
5. A rendszer a szűrőfeltételeknek megfelelő erőforrásokat keres, és listázza azokat.
6. A szűrőablak **Dolgozó típusa** mezőjét frissítse **Szerződés dolgozó** értékre, hogy a keresés csak a szerződéses alkalmazottakra legyen korlátozva. Frissítse a **Szállító** elemet a szűrőablakban egy szállító kiválasztásához, hogy a keresés csak egy adott szállító szerződéses dolgozóit mutassa.
7. Válasszon ki egy szerződés dolgozót a listából, és foglalja le a követelményhez szükséges erőforrást.
8. Létrejön egy projektcsoporttag. A projektcsoporttag azonban nem frissül az alvállalkozói szerződéssel vagy alvállalkozói sorral, ezért az erőforrások hozzárendelése nem az alvállalkozói árképzés alkalmazásával lesz költségelve. Manuálisan frissítse a projektcsoport tagjait egy alvállalkozói sorral, és menjen a **Projektbecslések** lapra, és válassza az **Árak frissítése** lehetőséget az erőforrás-hozzárendelés frissített költségének a megkereséséhez.

> [!NOTE]
> A Projekt csoport olyan tagjai, akiknél a **Dolgozó típusa** beállítása értéke **Szerződéses dolgozó**, de nem rendelkeznek alvállalkozói hivatkozással, **Érvénytelen** értékkel lesznek megjelölve a **Projektcsoporttagok** rácsban. Ha van ezzel az állapottal rendelkező projektcsoporttag, nyissa meg a projektcsoporttag rekordját, és frissítse manuálisan az alvállakozói szerződés és alvállalkozói sor mezőket, hogy a pénzügyi költségbecslés pontosan tükrözze az alvállalkozó költségét a **Becslések** lapon. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
