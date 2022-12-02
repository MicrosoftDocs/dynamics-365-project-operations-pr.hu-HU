---
title: Pénznemeltérés hiba
description: Ez a cikk a bizonyos bejegyzéstípusok mentésekor jelentkező a pénznemeltérés hibával kapcsolatos hibaelhárítási információikat biztosít.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5b0973a340dec8e68f326803d75bea9803e19791
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914727"
---
# <a name="currency-mismatch-error"></a>Pénznemeltérés hiba 

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Egy projekt, szerződés, árajánlat vagy foglalható erőforrás mentésekor a **A tulajdonosként megadott vállalat pénzneme nem egyezik meg a szerződő egység pénznemével. A folytatáshoz válasszon másik vállalatot vagy szerződő egységet a projektszerződéshez** hiba jelenthet meg. Ez azért van így, mert a rekord szerződő egységének pénzneme nem egyezik meg a tulajdonos vállalat pénznemével.


## <a name="resolution"></a>Felbontás

A probléma megkerüléséhez tegye a következőket:
- Ellenőrizze a rekordhoz tartozó a szerződő egység pénznemét. A pénznem a szervezeti egység rekordjának megnyitása után az **Általános** lapon található **Pénznem** mezőben láthatja.
- A tulajdonos vállalat pénznemének ellenőrzése. A pénznem a vállalat rekordjában a **Kapcsolódó** > **Főkönyvek** menüben láthatja. Kattintson duplán a vállalathoz társított főkönyvi rekordra, és ellenőrizze a **Könyvelési pénznem** mezőben az **Általános** lapon.

Ha a szerződő egységben és a főkönyvi rekordban beállított pénznem nem egyezik, módosítsa a konfigurációt, vagy válasszon más értékeket a bejegyzés mentésekor. A rendszer megköveteli, hogy ezek a bejegyzések megegyezzenek a megfelelő vállalatközi számlázási folyamatok biztosításához. Az vállalatközi konfigurációkról további tudnivalókat a [Vállalatközi tranzakciók létrehozása](../../project-accounting/create-intercompany-transactions.md) szakasz tartalmaz.

Ha a vállalati rekordhoz nincs hozzárendelve főkönyvi bejegyzés, ez azt jelzi, hogy a környezet beállításakor hiányzik egy konfiguráció. A konfigurációt a rendszergazdának kell kijavítania. A rendszergazdának meg kell nyitnia a **Kettős írási konfigurációkat**, és le kell állítania és újra kell indítania **Főkönyvek kettős írású leképezését** a leképezés kezdeti szinkronizálásával és az előfeltételekkel. További információért lásd: [Project Operations kettős írásos térképverziók](../../environment/resource-dual-write-maps.md).
