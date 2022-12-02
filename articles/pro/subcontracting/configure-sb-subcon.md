---
title: Ütemezési tábla konfigurálása a szerződéses alkalmazottak és az alvállalkozói szerződésben rögzített kapacitás megjelenítéséhez
description: Ez a cikk azt mutatja be, hogyan konfigurálható az ütemezési tábla a Microsoft Dynamics 365 Project Operations alkalmazásban, hogy megjelenítse az alvállalkozói erőforráskapacitást a projekterőforrás-követelmények személyzethez rendelése során.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 355691b63f437de789afab499369afcdf87e6d3d
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262219"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Ütemezési tábla konfigurálása a szerződéses alkalmazottak és az alvállalkozói szerződésben rögzített kapacitás megjelenítéséhez 

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations ütemezési tábláján kétféleképpen kereshet erőforrásokat:

- Általános erőforrás-keresés bármilyen projektalapú erőforrás-követelmény környezete nélkül.
- Követelményspecifikus erőforrás-keresés, ahol a projektkövetelmény biztosítja a javasolt erőforrások környezetét.

Ha értesítenie kell az ütemezési táblát az alvállalkozók erőforrás-kapacitásról és a szerződéses alkalmazottakról, akkor módosítania kell az Ütemezési tábla beállításait. Ezek a frissítések a következők: 
- Az ütemezési tábla beállításainak frissítése az általános erőforrás-kereséshez.
- Az ütemezési tábla beállításainak frissítése a követelmény alapú erőforrás-kereséshez.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Az ütemezési tábla beállításainak frissítése az általános erőforrás-kereséshez
### <a name="update-filters-for-general-resource-search"></a>Az általános erőforrás-keresés szűrőinek frissítése
Egy erőforrás keresésekor az ütemezési táblán elérhető szűrőket frissíteni kell, hogy külső erőforrásokra is kereshessen a következők bármelyikének vagy mindegyikének a megadásával:
  - A dolgozó típusa, hogy a látható erőforrások a szerződéses alkalmazottak vagy az alkalmazottak-e.
  - A szállító vállalat, amelyhez a erőforrásnak tartoznia kell.
  - Adott alvállalkozói szerződéshez vagy alvállalkozói sorhoz tartozó erőforrások.
    
### <a name="update-retrieve-resource-query"></a>Erőforrás-lekérés lekérdezés frissítése
A kereséshez használt lekérdezést is frissíteni kell, hogy használja ezeket a további szűrőattribútumokat. Az általános erőforrások keresés konfigurációjának frissítéséhez az ütemezési táblán használja a következő lépéseket:  
1. Nyissa meg az **Ütemezési tábla beállításait** egy adott ütemezési táblához.
2. Nyissa meg az **Általános beállítások** lapot, és görgessen az **Egyéb beállítások** részhez.
3. Az ebben a szakaszban található beállítások listájában frissítse a **Szűrő elrendezést** beállítást **Alapértelmezett szűrőelrendezés a Project Operations Lite szolgáltatáshoz** értékre.
4. Frissítse az **Erőforrás-beszerzési lekérdezés** beállítást **Alapértelmezett lekérési erőforrásokra vonatkozó lekérdezés a Project Operations Lite szolgáltatáshoz** értékre.

![Az ütemezési tábla beállításainak frissítése az általános erőforrás-kereséshez](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Az ütemezési tábla beállításainak frissítése a követelmény alapú erőforrás-kereséshez
### <a name="update-filters-for-requirement-specific-resource-search"></a>Az követelményspecifikus erőforrás-keresés szűrőinek frissítése 
Egy erőforrás keresésekor az ütemezési táblán elérhető szűrőket frissíteni kell, hogy külső erőforrásokra is kereshessen a következők bármelyikének vagy mindegyikének a megadásával:
 - A dolgozó típusa, hogy a látható erőforrások a szerződéses alkalmazottak vagy az alkalmazottak-e.
 - A szállító vállalat, amelyhez a erőforrásnak tartoznia kell.
 - Adott alvállalkozói szerződéshez vagy alvállalkozói sorhoz tartozó erőforrások.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Az erőforrás lekérése lekérdezés frissítése követelményspecifikus erőforrás-kereséshez 
A kereséshez használt lekérdezést is frissíteni kell, hogy használja ezeket a további szűrőattribútumokat. A követelményalapú erőforráskeresés konfigurációjának frissítéséhez az ütemezési táblán használja a következő lépéseket:

1. Nyissa meg az **Ütemezési tábla beállításait** az adott ütemezési táblához, majd válassza az **Alapértelmezett beállítások megnyitása** lehetőséget a követelményspecifikus keresés beállításainak megnyitásához.
2. Nyissa meg az **Általános beállítások** lapot, és görgessen az **Egyéb beállítások** részhez.
3. Az ebben a szakaszban található beállítások listájában frissítse a **Szűrő elrendezést** beállítást **Alapértelmezett szűrőelrendezés a Project Operations Lite szolgáltatáshoz** értékre.
4. Frissítse az **Erőforrás-beszerzési lekérdezés** beállítást **Alapértelmezett lekérési erőforrásokra vonatkozó lekérdezés a Project Operations Lite szolgáltatáshoz** értékre.
5. Nyissa meg az **Ütemezési típusok** lapot, és menjen a **Projekt** szakaszba.
6. A **Projekt** beállításai alatt frissítse az **Ütemezési segéd – Erőforrás-beszerzési lekérdezés** beállítást **Alapértelmezett lekérési erőforrásokra vonatkozó lekérdezés a Project Operations Lite szolgáltatáshoz** értékre és az **Ütemezési segéd – korlátozásbeszerzési lekérdezés** beállítást **Alapértelmezett lekérési korlátokra vonatkozó lekérdezés a Project Operations Lite szolgáltatáshoz** értékre.

![Az ütemezési tábla beállításainak frissítése a követelmény alapú erőforrás-kereséshez](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
