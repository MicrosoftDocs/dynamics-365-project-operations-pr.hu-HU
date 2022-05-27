---
title: Újdonságok és változások a Project Service Automation 3. verziójában – 2020 1. hullám
description: Ez a témakör információkat nyújt arról, hogy milyen újdonságok és változások vannak a Project Service Automation 3. verziójában – 2020. 1. hullám.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
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
ms.openlocfilehash: 073b70b4ae02d943eb0794b51e888815ee16f438
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577883"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Újdonságok és változások a Project Service Automation 3-as verziójában – 2020 1. hullám

[!include [banner](../includes/psa-now-project-operations.md)]

A témakör bemutatja a legfontosabb frissítés szempontjait a Project Service Automation (PSA) 3. x 2020 1. hullám legújabb verziójára történő átállás során.

## <a name="time-entry"></a>Időbejegyzés
Az időbevitel élménye bővítve lett, hogy az időbevitel több ügyfél-forgatókönyvre is kiterjedjen. Ez magában foglalja a bejegyzéstípusok hozzáadását is, amelyek adott viselkedést váltanak ki a **Időbevitel beállításai** mezőséma névben, amely **Időforrás** néven jelenik meg. A funkció támogatása érdekében új megoldást adtunk hozzá, amelynek neve: Idő, költség, állapotkezelés és jóváhagyások (TESA).

### <a name="upgrade-consideration"></a>Frissítéssel kapcsolatos megjegyzések
A szolgáltatás támogatásához a PSA-ban lévő szerepkörök frissítve lettek, hogy új jogosultságokat tartalmazzanak. Ezek a jogosultságok olvasási hozzáférést biztosítanak az új **Időbevitel beállításai** entitásnak.

Az időpontot naplózó felhasználóknak a meglévő szerepkörökön kívül meg kell adni az **Időbeviteli felhasználó** felhasználói szerepkört is. Ez a szerepkör tartalmazza az új funkciókat, és gondoskodik arról, hogy az időbejegyzés továbbra is működjön.

Emellett ha bármilyen egyéni alkalmazás-modullal rendelkezik, amely tartalmazza az időbejegyzés entitás összes űrlapját, akkor a modulból el kell távolítania a **TESA időbejegyzés gyorslétrehozási űrlapját**.

### <a name="currently-extended-time-entry-changes"></a>Jelenleg meghosszabbított időbejegyzés-változások
Hogy ez a lehető legkevésbé befolyásolja az időbejegyzést jelenleg használó felhasználókat, ez a szerepkörmódosítás az egyetlen alapvető feltétele az időbejegyzés további használatának. Ha egyéni nézeteket vagy különálló időbeviteli élményeket hozott létre, akkor az **Időbevitel beállítása** mezőket a megfelelő PSA-értékre kell állítania.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
