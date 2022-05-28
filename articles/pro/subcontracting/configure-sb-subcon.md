---
title: Ütemezési tábla konfigurálása a szerződéses alkalmazottak és az alvállalkozói szerződésben rögzített kapacitás megjelenítéséhez
description: Ez a témakör azt ismerteti, hogyan konfigurálható a Microsoft Dynamics 365 Project Operations Schedule Board szolgáltatása úgy, hogy az alvállalkozói erőforrás-kapacitást jelenítse meg a projekterőforrás-követelmények személyzete során.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6e382b33fafe91c8b96a91d033fe12b998114bdc
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587826"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Ütemezési tábla konfigurálása a szerződéses alkalmazottak és az alvállalkozói szerződésben rögzített kapacitás megjelenítéséhez 

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations Ütemezési táblája kétféle módon használható erőforrások keresésére:

- Általános erőforrás-keresés adott projektalapú erőforrásszükséglet környezete nélkül.
- Követelményspecifikus erőforrás-keresés, ahol a projektkövetelmény biztosítja a javasolt erőforrások környezetét.

Ha értesíteni szeretné az ütemező táblát az alvállalkozói erőforrás-kapacitásról és a szerződéses dolgozókról, frissítenie kell az ütemezési tábla beállításait. Ezek a frissítések a következők: 
- Az ütemezési tábla beállításainak frissítése az általános erőforrás-kereséshez.
- Az Ütemezési tábla beállításainak frissítése követelményalapú erőforrás-kereséshez.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Ütemezési tábla beállításainak frissítése általános erőforrás-kereséshez
### <a name="update-filters-for-general-resource-search"></a>Szűrők frissítése általános erőforrás-kereséshez
Erőforrás keresésekor frissíteni kell az ütemezési táblán elérhető szűrőket, hogy külső erőforrásokat is kereshessen az alábbiak bármelyikének vagy mindegyikének megadásával:
  - Dolgozó típusa, függetlenül attól, hogy a megjelenített erőforrásoknak szerződéses dolgozóknak vagy alkalmazottaknak kell-e lenniük.
  - Szállító vállalat, amelyhez az erőforrásnak tartoznia kell.
  - Adott alvállalkozói vagy alvállalkozói sorhoz tartozó erőforrások.
    
### <a name="update-retrieve-resource-query"></a>Erőforrás-lekérdezés lekérésének frissítése
A kereséshez használt lekérdezést is frissíteni kell a további szűrőattribútumok használatához. Az alábbi lépésekkel frissítheti az Ütemezési tábla konfigurációját az általános erőforrás-kereséshez:  
1. Nyissa meg **egy adott ütemezési tábla ütemezési táblájának beállításait**.
2. Nyissa meg az **Általános beállítások** lapot, és görgessen az Egyéb beállítások **lapra**.
3. Az ebben a szakaszban található beállítások listájában frissítse a Szűrőelrendezést alapértelmezett **szűrőelrendezésre** a Project Operations Lite **számára**.
4. Frissítse az Erőforrások lekérdezésének lekérése lekérdezést **az** **erőforrások alapértelmezett lekérésére a projektműveletek lite-jához**.

![Ütemezési tábla beállításainak frissítése általános erőforrás-kereséshez](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Ütemezési tábla beállításainak frissítése követelményalapú erőforrás-kereséshez
### <a name="update-filters-for-requirement-specific-resource-search"></a>Szűrők frissítése követelményspecifikus erőforrás-kereséshez 
Erőforrás keresésekor frissíteni kell az ütemezési táblán elérhető szűrőket, hogy külső erőforrásokat is kereshessen az alábbiak bármelyikének vagy mindegyikének megadásával:
 - Dolgozó típusa, függetlenül attól, hogy a megjelenített erőforrásoknak szerződéses dolgozóknak vagy alkalmazottaknak kell-e lenniük.
 - Szállító vállalat, amelyhez az erőforrásnak tartoznia kell.
 - Adott alvállalkozói vagy alvállalkozói sorhoz tartozó erőforrások.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Erőforrás-lekérdezés lekérésének frissítése követelményspecifikus erőforrás-kereséshez 
A kereséshez használt lekérdezést is frissíteni kell a további szűrőattribútumok használatához. Az alábbi lépésekkel frissítheti az Ütemezési tábla konfigurációját a követelményalapú erőforrás-kereséshez:

1. Nyissa meg **egy adott ütemezési tábla ütemezési táblájának beállításait**, majd válassza az Alapértelmezett beállítások **megnyitása lehetőséget** a követelményspecifikus keresés beállításainak megnyitásához.
2. Nyissa meg az **Általános beállítások** lapot, és görgessen az Egyéb beállítások **lapra**.
3. Az ebben a szakaszban található beállítások listájában frissítse a Szűrőelrendezést alapértelmezett **szűrőelrendezésre** a Project Operations Lite **számára**.
4. Frissítse az Erőforrások lekérdezésének lekérése lekérdezést **az** **erőforrások alapértelmezett lekérésére a projektműveletek lite-jához**.
5. Nyissa meg az **Ütemezési típusok** lapot, és nyissa meg a **Project elemet**.
6. A Project beállításai között frissítse **az Ütemezési segéd Erőforrás-lekérdezésének** lekérése alapértelmezett lekérési erőforrás-lekérdezést a Project Operations Lite-hoz **, és frissítse** az Ütemezési segéd lekérési megkötések **lekérdezését** **a Project Operations Lite** alapértelmezett lekérési megkötései lekérdezésére.**·**

![Ütemezési tábla beállításainak frissítése követelményalapú erőforrás-kereséshez](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
