---
title: Újdonságok vagy változások a Project Service Automation 14-es frissítési kiadásának V3 változatában
description: Ez a témakör információkat nyújt arról, hogy milyen újdonságok és változások vannak a Project Service Automation 14-es frissítési kiadásának V3 verziójában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: f9347741d8dae2c9a810bb5b3a32d4d6c0a628ed
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147161"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation 14-es frissítési kiadás, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Örömmel jelentjük be a Dynamics 365 Project Service Automation (PSA) alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez nyissa meg a megoldások oldalt. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a PSA V3. 14-ös frissítési kiadásában. Ennek a verziónak a build száma V 3.10.4.21, és a következő ütemezés szerint érhető el:

- **Általános elérhetőség (Önálló frissítés):** 2020. január
- **Automatikus frissítés:** 2020. február

## <a name="update-release-14"></a>14-ös frissítési kiadás

### <a name="enhancements"></a>Fejlesztések

- Sales

     - Az **Ajánlati sor részletei** mezőből származó egyéni mezőértékeket a program átmásolja a **Projektszerződés sorainak részletei** elemhez, amikor az ajánlatot **Lezárva megnyertként** értékre frissíti a rendszer.
     - A megerősített projektek állapota lehet **Lezárva elvesztettként**.

- Erőforráskezelés

     - A foglalások kibővítésekor a rendszer egy megerősítő párbeszédpanellel kéri a felhasználókat a foglalási eredmények összesítésére, és egy hivatkozást kínál a foglalások karbantartásához.


### <a name="bug-fixes"></a>Hibajavítások

- Idő és költség

     - Javítva: A felhasználói élmény javítása, amikor a felhasználó nem jelölt ki semmilyen helyesbítendő bejegyzést.

- Erőforráskezelés

     - Javítva: Egy erőforrás többszöri foglalása túlcsordulást okoz a foglalt erőforrás nevében.

- Sales

     - Javítva: A teljes értékesítési ár nincs kiszámítva addig, amíg a felhasználó nem ad meg önköltségi árat költségbecslésekhez egy projektben.
     - Javítva: Az ajánlat lezárása **Megnyert** állapottal sikertelen, ha a társított szerződés nem **Vázlat** állapotú.



[!INCLUDE[footer-include](../includes/footer-banner.md)]