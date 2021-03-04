---
title: Egyéni mezők és entitások létrehozása árazási dimenzióként
description: Ez a témakör az egyéni értékkészletek és entitások létrehozását ismerteti.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642816"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Egyéni mezők és entitások létrehozása árazási dimenzióként

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Hajtsa végre az alábbi lépéseket, amikor egyéni értékkészletet vagy entitást szeretne létrehozni, hogy azt árazási dimenzióként használja. További információkért lásd: [Árazási dimenziók áttekintése](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Javasoljuk, hogy minden egyéni árképzési dimenziót külön megoldásban hajtson végre. Ez a fontos gyakorlati tanács rugalmasságot biztosít a jövőben a szükséges változtatások frissítéséhez vagy eltávolításához. Ez a művelet a munkájának újbóli felhasználását is segíti, és megkönnyíti a változtatások egy másik példányra történő portolását, miután elvégezte az összes szükséges változtatást, exportálja ezt a megoldást **Felügyelt megoldásként**, és importálja más példányokra az árképzési beállítások újbóli felhasználása céljából.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Egyéni mezők és értékkészletek létrehozása az árképzési dimenzió megoldásban

Az árképzési dimenzió lehet értékkészlet vagy entitás. Mindkettőt létre kell hozni az árképzési megoldásban. Az eljárás lépései ismertetik az entitás alapú dimenziók és az értékkészlet-alapú dimenziók létrehozását.

### <a name="entity-based-dimensions"></a>Entitásalapú dimenziók
Az entitásalapú dimenziók létrehozásához tegye a következőket:

1. Lépjen a **Beállítások** > **Megoldások** részre, és kattintson duplán a(z) **\<your organization name> árképzési dimenzióira**.
2. A Megoldástallózóban a bal oldali navigációs panelen válassza az **Entitások** elemet.
3. Válassza az **Új** lehetőséget, és hozzon létre egy **Standard cím** nevű új entitást. 
4. Írja be a további szükséges információt, majd kattintson a **Mentés** gombra.

> ![A standard című entitás meghatározása](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Értékkészlet-alapú dimenziók 
Két értékkészlet-alapú dimenziót hozhat létre. 

- Az **Erőforrás-munkaterület** segítségével nyomon követheti az **Otthoni** munka és a **Helyszíni** munkavégzés árát. 
- Az **Erőforrások munkaóráit** használja a **Normál** és a **Túlóra** értékkel , ha a munka befejezésekor a felárat kell alkalmazni.

A következő ábra az **Erőforrás munkavégzési helyének** dimenzióját jeleníti meg. 

> ![Erőforrás munkahelye nevű értékkészlet-alapú árképzési dimenzió](media/Option-set-PD-called-Resource-Work-Location.png)

A következő ábra az **Erőforrás munkaóráinak** dimenzióját jeleníti meg. 

> ![Erőforrás munkaideje nevű értékkészlet-alapú árképzési dimenzió](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Lépjen a **Beállítások** > **Megoldások** részre, és kattintson duplán a(z) **\<your organization name> árképzési dimenzióira**. 
2. A Solution Explorerben a bal oldali navigációs panelen válassza az **Értékkészletek** elemet. 
3. Új értékkészlet létrehozásához kattintson az **Új** elemre, majd írja be a további szükséges információkat, majd kattintson a **Mentés** gombra.

## <a name="create-data-for-entity-based-dimensions"></a>Adatok létrehozása entitásalapú dimenziókhoz

Entitásalapú dimenziókhoz manuálisan vagy Microsoft Excel importálással vagy szolgáltatáshívások használatával hozhat létre adatokat. Az eljárás lépéseinek követésévek hozhat létre két szabványos címet: a **Szabványos cím** entitásalapú dimenzióból származó **Rendszermérnök** és **Vezető rendszermérnök**. Ha a létrehozni kívánt adat kis méretű, a következő példához hasonlóan használhat szabványos űrlapot.

1. Válassza az **Irányított keresés** lehetőséget.
2. Válassza ki a **Szabványos cím** entitást, majd válassza az **Eredmények** elemet. A **Szabványos cím** összes sora megjelenik.
3. Válassza az **Új** lehetőséget, és a **Név** mezőbe írja be a „Rendszermérnök” elemet, majd kattintson a **Mentés** gombra.
4. Zárja be a lapot. 
5. Ismételje meg az 1–3. lépést egy újabb szabványos cím létrehozásához a „Vezető rendszermérnök” esetében.

> ![Mintaadatok a szabványos cím entitáshoz](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]