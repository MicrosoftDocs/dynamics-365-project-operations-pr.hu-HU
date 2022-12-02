---
title: Újdonságok 2022. júniusában – Project Operations egyszerű telepítés
description: Ez a cikk a Microsoft Dynamics 365 Project Operations könnyű telepítés 2022. júniusi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8313288ecf7ff1350cd82c62d3d0c291d8a3ded4
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031196"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Újdonságok 2022. júniusában – Project Operations egyszerű telepítés

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a cikk a következő Microsoft Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations egy 4.43.0.77 vagy 4.43.0.119 verziójú Dataverse-környezetben

## <a name="quality-updates"></a>Minőségi frissítések

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Alvállalkozásba adás | 2708885. | Javítottuk a hibaüzenetet, amely akkor jelenik meg, amikor a felhasználó létrehoz egy foglalható erőforrás fejlécrekordot, ahol egyetlen foglalható erőforrás sincs kitöltve. |
| Projekttervezés és nyomon követés | 2629441. | Kijavítottuk a munkafolyamat triggerlogikáját, hogy megakadályozza a végtelen ciklust a projektfeladatok frissítésekor. |
| Idő és költség | 2641209. | A hozzárendelések/foglalások időbejegyzéseinek importja esetén meg kell tartani a foglalható erőforrás-hivatkozást. |
| Projekttervezés és nyomon követés | 2651148. | A projektdokumentum fejlécét védeni kell.|
| Projekttervezés és nyomon követés | 2653145. | További ellenőrzések garantálják, hogy ne lehessen olyan projektrekordot létrehozni, amelynek a neve érvénytelen karaktereket tartalmaz. |
| Idő és költség | 2654710. | Javította a szűrést a **Jóváhagyások** oldalon. |
| Számlázás és árképzés | 2667805. | A hozzáadott ellenőrzésekkel megakadályozható, hogy a számlázott tényleges értékesítések akkor is létrejönnek, ha nem léteznek a mögöttes nem számlázott tényleges értékesítések. |
| Számlázás és árképzés | 2668378. | A hozzáadott érvényesítések segítségével megakadályozható, hogy egyéni árképzési dimenziót ne lehessen hozzáadni logikai név és mezőnév nincs megadva. |
| Idő és költség | 2700428. | Javítva lett a jóváhagyási logika, hogy a projekt más jóváhagyási készletei akkor is feldolgozhatók legyenek, ha a az egyik jóváhagyás készlet a rendszerfeladatokban elakadt. |
