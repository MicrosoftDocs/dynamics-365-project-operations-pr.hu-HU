---
title: Pénznem eltérése hiba
description: Ez a témakör hibaelhárítási információkat tartalmaz egy adott bejegyzéstípus mentésekor fellépő pénznembeli eltérési hibáról.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bb54a121f0dc22f1c0ea88ada9c922c1d4c6544
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589751"
---
# <a name="currency-mismatch-error"></a>Pénznem eltérése hiba 

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Projekt, szerződés, ajánlat vagy könyvelhető erőforrás mentésekor előfordulhat, hogy a hiba jelenik meg, **a vállalat pénznemének birtoklása nem egyezik meg az összehúzódási egység pénznemével. Válassza ki a másik tulajdonosi társaságot vagy ajánlatkérőt a folytatáshoz**. Ennek az az oka, hogy a rekord szerződési egység pénzneme és a tulajdonos vállalat pénzneme között pénzneme nem egyezik.


## <a name="resolution"></a>Felbontás

A probléma megoldásához tegye a következőket:
- Ellenőrizze a rekord szerződési egységének pénznemét. A pénznemet a szervezeti egység rekordjának megnyitásával és a Pénznem **mező Általános** lapján **található** érték ellenőrzésével tekintheti meg.
- Ellenőrizze a tulajdonos vállalat pénznemét. A pénznemet a vállalati rekord kapcsolódó **főkönyvei** > **címmel** tekintheti meg. Kattintson duplán a vállalathoz társított főkönyvi rekordra, és ellenőrizze az értéket a **Könyvelés pénzneme** mező Általános **lapján**.

Ha az összehúzó egységben és a főkönyvi rekordban beállított pénznem nem egyezik meg, módosítsa a konfigurációt, vagy válasszon különböző értékeket a rekord mentésekor. A rendszer megköveteli, hogy ezek a rekordok megfeleljenek a helyes vállalatközi számlázási folyamatok biztosításához. A vállalatközi konfigurációkról további információt a Vállalatközi tranzakciók [létrehozása című témakörben talál](../../project-accounting/create-intercompany-transactions.md).

Ha a vállalati rekordhoz nincs társított főkönyvi rekord, ez azt jelzi, hogy a környezet beállításakor hiányzik a konfiguráció. A konfigurációt a rendszergazdának ki kell javítania. A rendszergazdának át kell lépnie a kettős írási **konfigurációkra**, és le kell állítania és újra kell indítania **a Ledgers kettős írási térképet** a térkép kezdeti szinkronizálásával és előfeltételeivel. További információért lásd: [Project Operations kettős írásos térképverziók](../../environment/resource-dual-write-maps.md).
