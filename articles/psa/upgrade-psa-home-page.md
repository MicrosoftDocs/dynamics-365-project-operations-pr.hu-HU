---
title: A kezdőlap frissítése
description: Ez a témakör azt mutatja, hogy hol találja a fontos információkat az új és módosult funkciókról a Dynamics 365 Project Service Automation rendszerben, és a folyamatot a legújabb verzióra történő frissítéshez.
ms.prod: ''
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8fc820d8fa0e421cdc963f391133e7311de96982
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368524"
---
# <a name="upgrade-home-page"></a>A kezdőlap frissítése

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Frissítés a PSA 2.x vagy 1.x verziójáról a 3.x verzióra

### <a name="new-instances"></a>Új példányok

2019. május 17-től, amikor egy új példány létesítésekor a Project Service Automation van kiválasztva, az alapértelmezés szerint a 3.x verzió kerül telepítésre.

### <a name="existing-instances"></a>Meglévő példányok

Korábban azoknak az ügyfeleknek, akiknek PSA 2.x verziója volt, és frissíteniük kellett a 3.x verzióra, amely a PSA Unified Client Interface (UCI) verziója, fel kellett venniük a kapcsolatot a Microsoft ügyfélszolgálattal, és meg kellett adniuk a részleteket a saját példányukról, hogy a támogatás lehetővé tegye a példány frissítését a 3.x verzióra. 2020. március 1-jétől azoknak az ügyfeleknek, akiknek PSA 2.x példánya van, és frissíteniük kell a 3.x verzióra, a példányaikat közvetlenül az Adminisztrátor portálról frissíthetik példányaikat, és ne kell felvenniük a kapcsolatot a Microsoft ügyfélszolgálattal.  

> [!NOTE]
> A PSA 3.x verziója jelentős változtatásokat tartalmaz. A továbbfejlesztett felhasználói élmény biztosítása érdekében az egységes interfész keretére épült. Az átalakított alkalmazás következetes, egységes felhasználói felületet (UI) biztosít, és reagáló tervezési elveket követ az optimális megtekintéshez bármilyen képernyőméretben vagy eszközön. Az alkalmazás egészében más változások is történtek. Néhány megváltozott terület magában foglalja az árazást, az erőforrások, az idő, a költségek és a jóváhagyások elrendelését és hozzárendelését.

A frissítési folyamat megkezdése előtt javasoljuk, hogy hajtsa végre a következő feladatokat:

- Ellenőrizze, hogy a Dynamics 365 Field Service és a Project Service Automation telepítve vannak-e az azonosított példányon. Ha mindkét megoldás telepítve van, akkor a példa rendszeres használatának folytatása előtt terveznie kell mindkettő frissítését.
- Gondosan olvassa át a következő témákat. A verziók közötti változások ismerete és megértése segít a frissítési folyamatban. Ezek a témák információkat tartalmaznak a PSA jelentős változásairól, valamint a 3.x verzióra történő frissítés megfontolásairól és ajánlásairól.

    - [Újdonságok és változások a Project Service Automation 3. verziójában](whats-new-changed-v3.md)
    - [Frissítési szempontok - A Project Service Automation 2.x vagy 1.x verziója a 3. verzióra](upgrade-v3.md)

- Frissítse a sandbox példányát a megvalósításban bekövetkező változások értékeléséhez, mielőtt frissítené a termelési példányt.

Miután áttekintette a korábban említett témákat, és készen áll a PSA 3.x vagy UCI-alapú verzióra való frissítésre, kérje a Microsoft támogatását, hogy a frissítést elérhetővé tegye az adminisztrációs központból. Kérésében adja meg a példány részleteit.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>A PSA régebbi verziói (PSA 2.x verzió) egy újonnan létrehozott példányban

2019. május 17-től minden új példányon UCI lesz az alapértelmezett ügyfél. A változáshoz való hozzáigazításhoz a PSA 3.x és a Field Service 8.x verziója alapértelmezés szerint lesz biztosítva, mivel ezeket a verziókat úgy tervezték, hogy az UCI klienssel működjenek.

2020. március 1-jétől a Dynamics PSA ügyfelei a továbbiakban nem hozhatnak létre új környezetet a PSA régebbi verzióival, például a PSA 2.x-es vagy régebbi verzióival. Minden új környezet csak a PSA 3.X verziójában hozható létre.

> [!NOTE]
> A legjobb élmény érdekében, ha a Field Service és a PSA alkalmazások régebbi verzióit használja, keresse meg a **Rendszerbeállítások** oldalt és a mezőnél használja a **Csak az új egységes interfész használata (ajánlott)** mezőt, válassza a **Nem** lehetőséget, mivel ezek a verziók nem úgy vannak megtervezve, hogy megfelelően letöltsék az UCI-t. Az UCI kikapcsolása után a régi web kliens használatával megnyithatja és futtathatja a Field Service és a PSA ezeket a verzióit. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]