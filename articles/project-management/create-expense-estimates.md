---
title: Költség becslések
description: Ez a témakör a projektalapú kiadások definiálásával vagy becslésével kapcsolatban tartalmaz tájékoztatást.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908230"
---
# <a name="expense-estimates"></a>Költség becslések
_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az erőforrásalapú becslések meghatározásával együtt a Dynamics 365 Project Operations lehetővé teszi, hogy a projektmenedzserek az egyes projektek projektalapú kiadásait definiálják. Minden egyes költségtétel hozzárendelhető egy adott projektfeladathoz vagy költségkategóriához. A költségkategóriák általában szervezeti szinten vannak meghatározva. Az egyes kiadások kategóriáinak árazását általában a következő hierarchia határozza meg:

- Cég
- Ügyfél
- Árajánlat/szerződés

Hajtsa végre a következő lépéseket a projektkiadások megtekintéséhez, hozzáadásához és törléséhez.

1. Nyissa meg a **Projektek** elemet, és jelölje ki a kezelni kívánt projektet.
2. Válassza ki a **Projektbecslések** lapot, és tekintse meg a projektek kiadásainak listáját.
3. Kiadás hozzáadásához válassza az **Új kiadás** lehetőséget. Másik lehetőségként jelölje ki a törlendő kiadást, majd válassza a **Kiadás törlése** lehetőséget.

Minden egyes költségsori tételhez a következő attribútumok vannak definiálva:

- **Kategória**: A projekttel kapcsolatban felmerült összes kiadás leírására szolgáló közös csoportosítások.
- **Kezdő dátum**: A kiadás várható felmerülésének dátuma.
- **Mennyiség**: Egy adott kategóriához tartozó kiadási tételek becsült száma.
- **Egység önköltségi ára**: A kiadás költségének kiszámításához használt egységár.
- **Egység értékesítési ára**: A kiadás értékesítési árának kiszámításához használt egységár.

