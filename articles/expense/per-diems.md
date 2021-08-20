---
title: Napidíjak
description: Ez a témakör a költségkezelésben használt napidíjszabályokról nyújt tájékoztatást.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 192164094231fa2da47806cd9c2ccaba8321c83a1464fc8724fa0d0a7618660f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986404"
---
# <a name="per-diems"></a>Napidíjak

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_


A napidíj olyan juttatás, amelyet a munka céljából utazó munkavállalónak fizetnek. A Költségkezelésben létrehoz napidíjszabályokat különböző utazási helyzetekhez. A napidíj az évszaktól, az utazás helyétől vagy mindkettőtől függhet. Amikor napidíjat hoz létre, megadhatja, hogy a napidíj bizonyos százalékát visszatartsák, ha egy dolgozó ingyenes étkezést vagy szolgáltatásokat kap. Beállíthatja azt a minimális és maximális óraszámot is, amelyre a napidíj a dolgozó utazása esetében vonatkozhat.

## <a name="configuration"></a>Konfigurálás 

1. A napidíjhelyek hozzáadásához nyissa meg a **Beállítás** > **Számítások és kódok** > **Napidíjhelyek** lehetőséget.
2. A fent hozzáadott helyek mindegyikéhez válassza ki a napidíj mértékét és a pénznemet, amely egy adott kezdő és záró dátum között érvényes a szálloda, az étkezés és az egyéb költségek esetében. A napidíj és a pénznemek a **Beállítás** > **Számítások és kódok** > **Napidíjak** alatt állíthatók be.
3. A **Napidíjhelyek** oldalon konfigurálja a napidíjszinteket. A napidíjszintek lehetővé teszik a napidíj százalékos felosztásának meghatározását a szállodai, étkezési és egyéb költségek esetében. 
4. A reggeli, ebéd vagy vacsora esetében érvényes étkezési százalékos csökkentés megadásához frissítse a mezőket a **Költségkezelési paraméterek** oldalon, a **Napidíj** lapon. 
    
## <a name="submit-expenses-using-per-diem"></a>Kiadások beküldése napidíj használatával
A kiadások napidíjak használatával történő elküldéséhez használja a **Napidíj** költségkategóriát költségjelentés létrehozásakor. Adja meg a **Napidíj kezdő dátuma**, a **Napidíj záró dátuma** és a **Napidíjhely** értékét. Az összeget a kiválasztott hely napidíjmértékei alapján számítják ki, az étkezési csökkentés pedig a napidíjszintek alapján kerül kiszámításra.


[!INCLUDE[footer-include](../includes/footer-banner.md)]