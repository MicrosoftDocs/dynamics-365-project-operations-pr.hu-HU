---
title: Az Ütemezési tábla konfigurálása a szerződéses dolgozók és az alvállalkozói kapacitás megjelenítéséhez
description: Ez a témakör azt ismerteti, hogyan konfigurálhatja a Microsoft Schedule Board programtáblát Dynamics 365 Project Operations úgy, hogy az alvállalkozói erőforrás-kapacitást megjelenítse a projekterőforrás-követelmények kezelésekor.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d645dee741a45dcb0219e4e4f58a329b7b873e10
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903032"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Az Ütemezési tábla konfigurálása a szerződéses dolgozók és az alvállalkozói kapacitás megjelenítéséhez 

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Schedule Board Dynamics 365 Project Operations kétféleképpen használható erőforrások keresésére:

- Általános erőforrás-keresés adott projektalapú erőforrás-követelmény környezete nélkül.
- Követelményspecifikus erőforrás-keresés, ahol a projektkövetelmény biztosítja a javasolt erőforrások kontextusát.

Az alvállalkozói erőforrás-kapacitásról és a szerződéses dolgozókról szóló ütemezési táblának értesítéséhez frissítéseket kell végrehajtania az Ütemezési tábla beállításaiban. Ezek a frissítések a következők: 
- Az ütemezési tábla beállításainak frissítése az általános erőforrás-kereséshez.
- Az ütemezési tábla beállításainak frissítése a követelményalapú erőforrás-kereséshez.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Ütemezési tábla beállításainak frissítése az általános erőforrás-kereséshez
### <a name="update-filters-for-general-resource-search"></a>Szűrők frissítése az általános erőforrás-kereséshez
Erőforrás keresésekor frissíteni kell az ütemezési táblán elérhető szűrőket, hogy külső erőforrásokat is megkeressen az alábbiak bármelyikének vagy mindegyikének megadásával:
  - Dolgozó típusa, függetlenül attól, hogy a megjelenített erőforrásoknak szerződéses munkavállalóknak vagy alkalmazottaknak kell-e lenniük.
  - Szállítói vállalat, amelyhez egy erőforrásnak tartoznia kell.
  - Egy adott alvállalkozói vagy alvállalkozói vonalhoz tartozó erőforrások.
    
### <a name="update-retrieve-resource-query"></a>Erőforrás-lekérdezés lekérésének frissítése
A kereséshez használt lekérdezést is frissíteni kell a további szűrőattribútumok használatához. Az alábbi lépésekkel frissítheti az ütemezési tábla konfigurációját az általános erőforrás-kereséshez:  
1. Nyissa meg **az Ütemezési tábla beállításait** egy adott ütemezési táblához.
2. Nyissa meg az **Általános beállítások** lapot, és görgessen az **Egyéb beállítások lapra**.
3. Az ebben a szakaszban található beállítások listájában frissítse a **Szűrőelrendezést** a Project Operations **Lite alapértelmezett szűrőelrendezésére.**
4. Frissítse **az Erőforrások lekérése** lekérdezést a Project Operations **Lite alapértelmezett erőforrás-lekérdezésére.**

![Ütemezési tábla beállításainak frissítése az általános erőforrás-kereséshez](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Ütemezési tábla beállításainak frissítése a követelményalapú erőforrás-kereséshez
### <a name="update-filters-for-requirement-specific-resource-search"></a>Szűrők frissítése a követelményspecifikus erőforrás-kereséshez 
Erőforrás keresésekor frissíteni kell az ütemezési táblán elérhető szűrőket, hogy külső erőforrásokat is megkeressen az alábbiak bármelyikének vagy mindegyikének megadásával:
 - Dolgozó típusa, függetlenül attól, hogy a megjelenített erőforrásoknak szerződéses munkavállalóknak vagy alkalmazottaknak kell-e lenniük.
 - Szállítói vállalat, amelyhez egy erőforrásnak tartoznia kell.
 - Egy adott alvállalkozói vagy alvállalkozói vonalhoz tartozó erőforrások.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Erőforrás-lekérdezés frissítése a követelményspecifikus erőforrás-kereséshez 
A kereséshez használt lekérdezést is frissíteni kell a további szűrőattribútumok használatához. Az alábbi lépésekkel frissítheti az Ütemezési tábla konfigurációját a követelményalapú erőforrás-kereséshez:

1. Nyissa meg **az Ütemezési tábla beállításait** egy adott ütemezési táblához, majd válassza az Alapértelmezett beállítások megnyitása lehetőséget **a** követelményspecifikus keresés beállításainak megnyitásához.
2. Nyissa meg az **Általános beállítások** lapot, és görgessen az **Egyéb beállítások lapra**.
3. Az ebben a szakaszban található beállítások listájában frissítse a **Szűrőelrendezést** a Project Operations **Lite alapértelmezett szűrőelrendezésére.**
4. Frissítse **az Erőforrások lekérése** lekérdezést a Project Operations **Lite alapértelmezett erőforrás-lekérdezésére.**
5. Nyissa meg az **Ütemezéstípusok** lapot, és lépjen a **Project** elemre.
6. A Project beállításai alatt frissítse **az** **Ütemezési segéd erőforrások lekérdezésének ütemezése lekérését** a Project Operations **Lite alapértelmezett erőforrás-lekérdezésére,** és frissítse az **Ütemezési segéd lekérési kényszerek lekérdezését** a Project Operations **Lite alapértelmezett lekérési** lekérdezésére.

![Ütemezési tábla beállításainak frissítése a követelményalapú erőforrás-kereséshez](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
