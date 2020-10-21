---
title: Összetett egységek kezelése, például felhasználónként vagy havonta, termékalapú árajánlatsoroknál
description: Ez a témakör az összetett egységek kezeléséről tartalmaz tájékoztatást a termékalapú árajánlatsorok esetében.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 741230e69302138cce8f7379f520f7178e1c80af
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965806"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a>Összetett egységek kezelése, például felhasználónként vagy havonta, termékalapú árajánlatsoroknál

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Dynamics 365 Project Operations mennyiségi tényezőket alkalmaz az előfizetésen alapuló termékek értékesítésének támogatására. Az előfizetésen alapuló termékek esetében az árajánlat vagy a projektszerződés sorában szereplő mennyiséget a felhasználói/hónap számában fejezik ki.

Az előfizetési szoftver ára általában a katalógusban kerül tárolásra havi felhasználónkénti árként. Az értékesítési folyamat során az árajánlatsorban a felhasználónkénti havi ár általában az IT-értékesítési ügynökkel való egyeztetés után és az általa megadott árengedménnyel születik meg. Minden egyes ügyletnek eltérő felhasználói száma és előfizetési hónapjai vannak. Az árajánlatsor kiszámításához használt mennyiség a felhasználók számának és az előfizetési hónapoknak a szorzata.

Az ilyen típusú értékesítés támogatása érdekében a Project Operations bevezette a mennyiségi tényezők fogalmát. A mennyiségi tényezők a Dynamics 365 termékattribútumaira támaszkodnak. Amikor egy adott termék tulajdonságait konfigurálja, a Project Operations lehetővé teszi, hogy mennyiségi tényezőként jelölje meg ezen tulajdonságok egy részhalmazát vagy az összes tulajdonságot.

A Project Operations ellenőrzi, hogy csak a numerikus vagy a numerikus adattípusú termékjellemzőket jelölte-e meg mennyiségi tényezőként. Ha mennyiségi tényezőket tartalmazó terméket ad hozzá egy árajánlatsorhoz, a **Mennyiség** mező írásvédett lesz. Miután megadta azon terméktulajdonságok értékeit, amelyek mennyiségi tényezők, a Project Operations kiszámítja az árajánlatsor mennyiségét.

Például a Dynamics 365 Sales a következő tulajdonságokkal rendelkezik:

- **Felhasználók száma**: A felhasználók száma
- **Hónapok száma**: Az előfizetési hónapok száma
- **Termék cikkszáma**

A **Felhasználók száma** és a **Hónapok száma** tulajdonságok megjelölhetők mennyiségi tényezőként a terméksor tulajdonságainak szerkesztésével.

Ha mennyiségi tényezőket szeretne létrehozni a termék tulajdonságaiból, hajtsa végre a következő lépéseket:

1. A Project Operations bal oldali ablaktáblájában nyissa meg az **Értékesítés** > **Termékek** menüpontot.
2. Nyissa meg azt a terméket, amelyre vonatkozóan mennyiségi tényezőket kell konfigurálnia. Győződjön meg róla, hogy a termékhez már konfigurálva vannak tulajdonságok.
3. A termékre vonatkozó **Projektinformációk** oldalon jelölje ki a **Mennyiségi tényezők** lapot.
4. Az alrácsban válassza az **+ Új mezőszámítás** elemet.
5. Adja meg a mennyiségi tényező nevét, és jelölje ki a mezőszámításra leképezhető megfelelő tulajdonságértéket.
6. Az űrlap mentése és bezárása. Ismételje meg ezeket a lépéseket minden olyan tulajdonságra vonatkozóan, amelyet a termékalapú árajánlatsor mennyiségének a kiszámításához használni szeretne.

Ha egy termékhez termékalapú árajánlatsort hoz létre, az árajánlatsor mennyisége zárolva lesz. A mennyiséget az adott árajánlatsorhoz tartozó tulajdonságértékek szorzatával számítja ki a program.
