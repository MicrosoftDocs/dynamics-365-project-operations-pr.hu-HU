---
title: Újdonságok vagy változások a Project Service Automation 13-es frissítési kiadásának V3 változatában
description: Ez a témakör információkat nyújt arról, hogy milyen újdonságok és változások vannak a Project Service Automation 13-ös frissítési kiadásának V3 verziójában.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 435b70255dd0053a496362c9ced9e742cfcca843
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078052"
---
# <a name="project-service-automation-update-release-13-v3"></a>Project Service Automation 13-es frissítési kiadás, V3
Örömmel jelentjük be a Dynamics 365 Project Service Automation (PSA) alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez nyissa meg a megoldások oldalt. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 13-es frissítési kiadásában. Ennek a verziónak a build száma V 3.10.3.18, és a következő ütemezés szerint érhető el:

- **Általános elérhetőség (Önálló frissítés):** 2019. november
- **Automatikus frissítés:** 2019. december


## <a name="update-release-13"></a>13-ös frissítési kiadás 

### <a name="bug-fixes"></a>Hibajavítások

- Idő és költség

     - Javítva: A **Költség-jóváhagyás** lapon a keresési funkció nem működik, ha költség célja alapján keres.

- Erőforráskezelés

     - Javítva: Az egyeztetésben szereplő frissítve lettek, hogy jobbra igazítottak legyenek.
     - Javítva: A megnevezett erőforrások nem rendelhetők hozzá a feladatokhoz az **Ütemezés** lapon.

- Projektmenedzsment

     - Javítva: Null hivatkozás kivétel csoporttag hozzárendelésekor, amikor a **TransactionType** esetében hiányzik a beállítási információ az **Egység** és **DefaultGroup** esetében.

- Sales

     - Javítva: A duplikált tranzakciótípus-rekordok hibát adnak vissza a szerepkör árrekordjai létrehozása során.
     - Javítva : Extra gombok láthatók az **Új lehetőség** , **Ajánlat** , **Rendelési sor** és **Termék hozzáadása** a Lehetőségek, Ajánlatok, Termékrendelések, és a projektlapú Sorok alrács parancsaiban.


