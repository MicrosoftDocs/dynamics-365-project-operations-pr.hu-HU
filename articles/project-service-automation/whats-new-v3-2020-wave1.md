---
title: Újdonságok és változások a Project Service Automation 3. verziójában – 2020 1. hullám
description: Ez a témakör információkat nyújt arról, hogy milyen újdonságok és változások vannak a Project Service Automation 3. verziójában – 2020. 1. hullám.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752221"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Újdonságok és változások a Project Service Automation 3-as verziójában – 2020 1. hullám
A témakör bemutatja a legfontosabb frissítés szempontjait a Project Service Automation (PSA) 3. x 2020 1. hullám legújabb verziójára történő átállás során.

## <a name="time-entry"></a>Időbejegyzés
Az időbevitel élménye bővítve lett, hogy az időbevitel több ügyfél-forgatókönyvre is kiterjedjen. Ez magában foglalja a bejegyzéstípusok hozzáadását is, amelyek adott viselkedést váltanak ki a **Időbevitel beállításai** mezőséma névben, amely **Időforrás** néven jelenik meg.

### <a name="upgrade-consideration"></a>Frissítéssel kapcsolatos megjegyzések
A szolgáltatás támogatásához a PSA-ban lévő szerepkörök frissítve lettek, hogy új jogosultságokat tartalmazzanak. Ezek a jogosultságok olvasási hozzáférést biztosítanak az új **Időbevitel beállításai** entitásnak.

Az időpontot naplózó felhasználóknak a meglévő szerepkörökön kívül meg kell adni az **Időbeviteli felhasználó** felhasználói szerepkört is. Ez a szerepkör tartalmazza az új funkciókat, és gondoskodik arról, hogy az időbejegyzés továbbra is működjön.

### <a name="currently-extended-time-entry-changes"></a>Jelenleg meghosszabbított időbejegyzés-változások
Hogy ez a lehető legkevésbé befolyásolja az időbejegyzést jelenleg használó felhasználókat, ez a szerepkörmódosítás az egyetlen alapvető feltétele az időbejegyzés további használatának. Ha egyéni nézeteket vagy különálló időbeviteli élményeket hozott létre, akkor az **Időbevitel beállítása** mezőket a megfelelő PSA-értékre kell állítania.
