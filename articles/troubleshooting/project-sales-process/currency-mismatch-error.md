---
title: Pénznemek eltérési hibája
description: Ez a cikk hibaelhárítási információkat tartalmaz egy pénznemeltéreltérési hibáról, amely adott rekordtípusok mentésekor következik be.
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
# <a name="currency-mismatch-error"></a>Pénznemek eltérési hibája 

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Projekt, szerződés, árajánlat vagy foglalható erőforrás mentésekor a következő hibaüzenet jelenhet meg: **A vállalat pénznemének birtoklása nem egyezik meg a szerződő egység pénznemével. A folytatáshoz válasszon másik tulajdonosi társaságot vagy szerződéses egységet**. Ennek az az oka, hogy devizaeltérés van a rekordra vonatkozó szerződéses egység pénzneme és a tulajdonos cég pénzneme között.


## <a name="resolution"></a>Felbontás

A probléma megoldásához tegye a következőket:
- Ellenőrizze a rekord szerződő egységének pénznemét. A pénznemet úgy tekintheti meg, hogy megnyitja a szervezeti egység rekordját, és ellenőrzi az értéket a **Pénznem** **mező Általános** lapján.
- Ellenőrizze a tulajdonos társaság pénznemét. A pénznemet **a Vállalati rekordban a Kapcsolódó** > **főkönyvek** menüpontban tekintheti meg. Kattintson duplán a vállalathoz társított főkönyvi rekordra, és ellenőrizze az értéket a **Könyvelési pénznem** mező Általános lapján.**·**

Ha a szerződő egységben beállított pénznem és a főkönyvi rekord nem egyezik, módosítsa a konfigurációt, vagy válasszon különböző értékeket a rekord mentésekor. A rendszer megköveteli, hogy ezek a rekordok egyezzenek a vállalatközi számlázási folyamatok megfelelő biztosítása érdekében. További információ a vállalatközi konfigurációkról: [Vállalatközi tranzakciók](../../project-accounting/create-intercompany-transactions.md) létrehozása.

Ha a vállalati rekordhoz nincs társított főkönyvi rekord, ez azt jelzi, hogy hiányzik a konfiguráció a környezet beállításakor. A konfigurációt a rendszergazdának ki kell javítania. A rendszergazdának a Kettős írás konfigurációkhoz **kell mennie,** és le kell állítania és újra kell indítania **a Főkönyvek kettős írású leképezését** a térkép kezdeti szinkronizálásával és annak előfeltételeivel. További információért lásd: [Project Operations kettős írásos térképverziók](../../environment/resource-dual-write-maps.md).
