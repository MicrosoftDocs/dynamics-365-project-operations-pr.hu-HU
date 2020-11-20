---
title: Bonyolult egységek kezelése termékalapú szerződéssorokhoz - lite
description: Ez az témakör az előfizetéses termékek értékesítésének támogatásával kapcsolatos információkat tartalmaz.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177379"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Bonyolult egységek kezelése termékalapú szerződéssorokhoz - lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Dynamics 365 Project Operations mennyiségi tényezőket alkalmaz az előfizetésen alapuló termékek értékesítésének támogatására. Az előfizetésen alapuló termékek esetében a szerződés vagy a projektszerződés sorában szereplő mennyiséget a felhasználói-hónap számában fejezik ki.

Általában az előfizetési szoftver ára általában a katalógusban kerül tárolásra havi felhasználónkénti árként. Az értékesítési folyamat során a szerződéssorban a felhasználónkénti havi ár általában az értékesítési ügynökkel való egyeztetés után és az általa megadott árengedménnyel születik meg. Minden egyes ügyletnek eltérő felhasználói száma és előfizetési hónapjai vannak. A szerződéssor összegének kiszámításához használt mennyiség a felhasználók számának és az előfizetési hónapoknak a szorzata.

Az ilyen típusú értékesítés támogatása érdekében a Project Operations támogatja a *mennyiségi tényezők* fogalmát. A mennyiségi tényezők a termékattribútumokra támaszkodnak. Amikor egy adott termék tulajdonságait konfigurálja, mennyiségi tényezőként jelölheti meg ezen tulajdonságok egy részhalmazát vagy az összes tulajdonságot.

A Project Operations ellenőrzi, hogy csak a numerikus vagy a numerikus adattípusú termékjellemzőket jelölte-e meg mennyiségi tényezőként. Amikor beállított mennyiség tényezőkkel rendelkező terméket vesz fel egy szerződéssorba, a **Mennyiség** mező írásvédett lesz. Miután megadta a terméktulajdonságok értékeit, amelyek mennyiségi tényezők, a Project Operations kiszámítja az szerződéssor mennyiségét.

Például a Dynamics 365 Sales a következő tulajdonságokkal rendelkezik:

- **Felhasználók száma**: A felhasználók száma.
- **Hónapok száma**: Az előfizetési hónapok száma.
- **Termék termékváltozata**: A raktározási egység (SKU) a termékhez.

A **Felhasználók száma** és a **Hónapok száma** tulajdonságok megjelölhetők mennyiségi tényezőként a terméksor tulajdonságainak szerkesztésével.

Ha mennyiségi tényezőket szeretne létrehozni a termék tulajdonságaiból, hajtsa végre az alábbi lépéseket.

1. A **Project Operations** alkalmazásban válassza az **Értékesítés-termékek** lehetőséget.
2. Nyissa meg azt a terméket, amelyre vonatkozóan meg kell adnia a mennyiségi tényezőket. Ügyeljen arra, hogy a termékhez a tulajdonságok már be legyenek beállítva..
3. A **Projektinformációk** lapon válassza a **Mennyiségi tényezők** lapot.
4. Az alrácsban válassza az **+ Új mezőszámítás** elemet.
5. Adja meg a **Mennyiségi tényező** nevét, és jelölje ki a mezőszámításra leképezhető megfelelő tulajdonságértéket.
6. Az űrlap mentése és bezárása.
7. Ismételje meg a 2–6 lépéseket az összes olyan tulajdonságra vonatkozóan, amelyek együttesen alkotják a termék alapú szerződéssor mennyiségét.

A beállított mennyiségi tényezőkkel, amikor a felhasználó létrehoz egy szerződéssor ehhez a termékhez, a szerződéssor mennyisége zárolva van. A mennyiséget a program az adott szerződéssor tulajdonságértékeinek szorzataként számítja ki.
