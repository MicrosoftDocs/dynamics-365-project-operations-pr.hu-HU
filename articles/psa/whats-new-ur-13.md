---
title: Újdonságok vagy változások a Project Service Automation 13-es frissítési kiadásának V3 változatában
description: Ez a cikk információkat nyújt arról, hogy milyen újdonságok és változások vannak a Project Service Automation 13-ös frissítési kiadásának V3 verziójában.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: f4898391922f5ecbc99d78e49358ea749fe27b3f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930689"
---
# <a name="project-service-automation-update-release-13-v3"></a>Project Service Automation 13-es frissítési kiadás, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Örömmel jelentjük be a Dynamics 365 Project Service Automation (PSA) alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez nyissa meg a megoldások oldalt. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a cikk felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 13-es frissítési kiadásában. Ennek a verziónak a build száma V 3.10.3.18, és a következő ütemezés szerint érhető el:

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
     - Rögzített: Extra gombok az **Új lehetőség**, **Árajánlat**, **Rendelési sor** és **Termék hozzáadása** elemekhez láthatóvá válnak a Lehetőségek, Árajánlatok és Rendeléshez tartozó termékek parancsaiban, és a projektalapú Sorok részrácson.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
