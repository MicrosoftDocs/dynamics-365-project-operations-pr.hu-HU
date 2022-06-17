---
title: Újdonságok 2022. júniusában – Project Operations egyszerű telepítés
description: Ez a cikk a Microsoft Dynamics 365 Project Operations Lite központi telepítésének 2022. júniusi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2d773603abef7ab45d4d1c298e5553e57893294d
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959620"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Újdonságok 2022. júniusában – Project Operations egyszerű telepítés

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a cikk a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Project Operations egy Dataverse környezeti verzióban 4.43.0.77

## <a name="quality-updates"></a>Minőségi frissítések

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Alvállalkozói | 2708885 | Kijavítottuk a hibaüzenetet, amely akkor jelenik meg, amikor egy felhasználó lefoglalható erőforrás-foglalási fejlécrekordot hozott létre, amelyben nincs kitöltve foglalható erőforrás. |
| Projekttervezés és nyomon követés | 2629441 | Kijavítottuk a munkafolyamatot kiváltó logikát, hogy megakadályozza a végtelen hurkot a projekttevékenységek frissítésekor. |
| Idő és költség | 2641209 | A hozzárendelésekből/foglalásokból származó időbeviteli importálásoknak meg kell őrizniük a foglalható erőforrás-referenciát. |
| Projekttervezés és nyomon követés | 2651148 | A projektdokumentum fejlécét meg kell őrizni.|
| Projekttervezés és nyomon követés | 2653145 | Hozzáadott ellenőrzések annak biztosítására, hogy ne lehessen olyan projektrekordot létrehozni, amelynek nevében nem érvényes karakterek szerepelnek. |
| Idő és költség | 2654710 | Kijavítottuk a szűrést a **Jóváhagyások** lapon. |
| Számlázás és árképzés | 2667805 | Hozzáadott ellenőrzések, amelyek segítenek megakadályozni a számlázott értékesítési tényleges adatok létrehozását, ha a számlázatlan értékesítési tényleges adatok nem léteznek. |
| Számlázás és árképzés | 2668378 | Hozzáadott ellenőrzések, amelyek segítenek megakadályozni az egyéni árképzési dimenziók hozzáadását, kivéve, ha a rendszer kitölti a logikai nevet és a mező nevét. |
| Idő és költség | 2700428 | Továbbfejlesztettük a jóváhagyási logikát, hogy a projekt más jóváhagyási készletei akkor is feldolgozhatók legyenek, ha az egyik jóváhagyási készlet elakadt a rendszerfeladatokban. |
