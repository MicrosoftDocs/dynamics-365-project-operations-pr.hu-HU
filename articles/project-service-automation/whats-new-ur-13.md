---
title: Újdonságok a Project Service Automation 13-es frissítési kiadásának V3 változatában
description: Ez a témakör információkat nyújt arról, hogy milyen újdonságok és változások vannak a Project Service Automation 13-ös frissítési kiadásának V3 verziójában.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752225"
---
# <a name="project-service-automation-v3-update-release-13"></a>Project Service Automation V3, 13-ös frissítési kiadás
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
     - Javítva : Extra gombok láthatók az **Új lehetőség** , **Ajánlat**, **Rendelési sor** és **Termék hozzáadása** a Lehetőségek, Ajánlatok, Termékrendelések, és a projektlapú Sorok alrács parancsaiban.


