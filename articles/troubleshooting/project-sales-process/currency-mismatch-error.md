---
title: Pénznem eltérési hiba
description: Ez a témakör hibaelhárítási információkat nyújt egy pénznem eltérési hibájáról, amely bizonyos rekordtípusok mentésekor következik be.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 52e33ad3728e1a393e8c7e3ca4e0a4b506d0b774
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903685"
---
# <a name="currency-mismatch-error"></a>Pénznem eltérési hiba 

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Projekt, szerződés, ajánlat vagy foglalható erőforrás mentésekor előfordulhat, hogy a hiba jelenik meg: **A vállalati pénznem birtoklása nem egyezik meg a szerződő egység pénznemével. Válasszon másik tulajdonban vagy szerződéses egységet a folytatáshoz**. Ennek az az oka, hogy a rekordhoz kötött egység pénzneme és a tulajdonló vállalati pénznem között eltérés van.


## <a name="resolution"></a>Felbontás

A probléma megkerülésére tegye a következőket:
- Ellenőrizze a rekordhoz a szerződő egység pénznemét. A pénznemet a szervezeti egységrekord megnyitásával és a Pénznem mezőben az Általános lapon található érték ellenőrzésével **tekintheti** **meg**.
- Ellenőrizze a tulajdonló vállalat pénznemét. A pénznemet a **vállalati rekord Kapcsolódó főkönyvei című** > **témakörben tekintheti** meg. Kattintson duplán a vállalathoz társított főkönyvi rekordra, és ellenőrizze a **Könyvelés** **pénzneme mezőben a Általános lapon található** értéket.

Ha a szerződő egységben beállított pénznem és a főkönyvi rekord nem egyezik, módosítsa a konfigurációt, vagy válasszon különböző értékeket a rekord mentésekor. A rendszer megköveteli, hogy ezeknek a rekordoknak egyezzenek a helyes vállalatközi számlázási folyamatok biztosítása érdekében. A vállalatközi konfigurációkról további információt a Vállalatközi tranzakciók létrehozása című témakörben [talál](../../project-accounting/create-intercompany-transactions.md).

Ha a vállalati rekord nem rendelkezik társított főkönyvi rekordtal, ez azt jelzi, hogy a környezet beállításakor hiányzik a konfiguráció. A konfigurációt a rendszergazdának kell kijavítania. A rendszergazdának kettős írású konfigurációkra kell lépnie, és le kell **állítania** és újra kell **indítania a főkönyvek kettős írási** térképét a térkép kezdeti szinkronizálásával és előfeltételeivel. További információért lásd: [Project Operations kettős írásos térképverziók](../../environment/resource-dual-write-maps.md).
