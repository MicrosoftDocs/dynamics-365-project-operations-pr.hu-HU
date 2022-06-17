---
title: Ütemezési tábla konfigurálása a szerződéses alkalmazottak és az alvállalkozói szerződésben rögzített kapacitás megjelenítéséhez
description: Ez a cikk azt ismerteti, hogyan konfigurálhatja az Ütemezési táblát a Microsoftban Dynamics 365 Project Operations úgy, hogy az alvállalkozói erőforrás-kapacitást jelenítse meg a projekterőforrás-követelmények személyzete során.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b965fd5011a575354f50c47081be198ab43248f9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919833"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Ütemezési tábla konfigurálása a szerződéses alkalmazottak és az alvállalkozói szerződésben rögzített kapacitás megjelenítéséhez 

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations ütemezési táblája kétféleképpen használható erőforrások kereséséhez:

- Általános erőforrás-keresés az adott projektalapú erőforrás-követelmény kontextusa nélkül.
- Követelményspecifikus erőforrás-keresés, ahol a projektkövetelmény biztosítja a javasolt erőforrások kontextusát.

Ahhoz, hogy értesítse az ütemezési táblát az alvállalkozói erőforrás-kapacitásról és a szerződéses dolgozókról, frissítenie kell az Ütemezési tábla beállításait. Ezek a frissítések a következők: 
- Frissítse az ütemezési tábla beállításait az általános erőforrás-kereséshez.
- Frissítse az Ütemezési tábla beállításait a követelményalapú erőforrás-kereséshez.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Az ütemezési tábla beállításainak frissítése az általános erőforrás-kereséshez
### <a name="update-filters-for-general-resource-search"></a>Szűrők frissítése az általános erőforrás-kereséshez
Erőforrás keresésekor frissíteni kell az ütemezési táblán elérhető szűrőket, hogy külső erőforrásokat is kereshessen az alábbiak bármelyikének vagy mindegyikének megadásával:
  - Dolgozó típusa, függetlenül attól, hogy a megjelenített erőforrások szerződéses alkalmazottaknak vagy alkalmazottaknak kell-e lenniük.
  - Szállítóvállalat, amelyhez az erőforrásnak tartoznia kell.
  - Egy adott alvállalkozói vagy alvállalkozói vonalhoz tartozó erőforrások.
    
### <a name="update-retrieve-resource-query"></a>Erőforrás-lekérdezés lekérésének frissítése
A kereséshez használt lekérdezést is frissíteni kell, hogy ezeket a további szűrőattribútumokat használja. A következő lépésekkel frissítheti az ütemezési tábla konfigurációját az általános erőforrás-kereséshez:  
1. Nyissa meg **az Ütemezési tábla beállításainak** ütemezése egy adott ütemezési táblához.
2. Nyissa meg az **Általános beállítások** lapot, és görgessen az Egyéb beállítások **részhez**.
3. Az ebben a szakaszban található beállítások listájában frissítse a Szűrőelrendezést **a** **Project Operations Lite** alapértelmezett szűrőelrendezésére.
4. Frissítse **az Erőforrások lekérése lekérdezést** az **erőforrások alapértelmezett lekérése lekérdezésre a Project Operations Lite-hez**.

![Az ütemezési tábla beállításainak frissítése az általános erőforrás-kereséshez](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Ütemezési tábla beállításainak frissítése a követelményalapú erőforrás-kereséshez
### <a name="update-filters-for-requirement-specific-resource-search"></a>Szűrők frissítése a követelményspecifikus erőforrás-kereséshez 
Erőforrás keresésekor frissíteni kell az ütemezési táblán elérhető szűrőket, hogy külső erőforrásokat is kereshessen az alábbiak bármelyikének vagy mindegyikének megadásával:
 - Dolgozó típusa, függetlenül attól, hogy a megjelenített erőforrások szerződéses alkalmazottaknak vagy alkalmazottaknak kell-e lenniük.
 - Szállítóvállalat, amelyhez az erőforrásnak tartoznia kell.
 - Egy adott alvállalkozói vagy alvállalkozói vonalhoz tartozó erőforrások.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Erőforrás-lekérdezés frissítése a követelményspecifikus erőforrás-kereséshez 
A kereséshez használt lekérdezést is frissíteni kell, hogy ezeket a további szűrőattribútumokat használja. A következő lépésekkel frissítheti az ütemezési tábla konfigurációját a követelményalapú erőforrás-kereséshez:

1. Nyissa meg **az Ütemezési tábla beállításainak** ütemezése egy adott ütemezési táblához, majd válassza az Alapértelmezett beállítások **megnyitása lehetőséget** a követelményspecifikus keresés beállításainak megnyitásához.
2. Nyissa meg az **Általános beállítások** lapot, és görgessen az Egyéb beállítások **részhez**.
3. Az ebben a szakaszban található beállítások listájában frissítse a Szűrőelrendezést **a** **Project Operations Lite** alapértelmezett szűrőelrendezésére.
4. Frissítse **az Erőforrások lekérése lekérdezést** az **erőforrások alapértelmezett lekérése lekérdezésre a Project Operations Lite-hez**.
5. Nyissa meg az **Ütemezéstípusok** lapot, és lépjen a Projekt **elemre**.
6. A Project beállításai alatt frissítse az Ütemezési segéd erőforrások lekérése lekérdezését **az** erőforrások alapértelmezett lekérése lekérdezésre **a Project Operations Lite-hez, és frissítse** az ütemezési segéd lekérési kényszerek lekérdezését **az** **alapértelmezett lekérési kényszerek lekérdezésére a Project Operations Lite-hez**.**·**

![Ütemezési tábla beállításainak frissítése a követelményalapú erőforrás-kereséshez](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
