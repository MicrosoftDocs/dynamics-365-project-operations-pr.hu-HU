---
title: Egyéni mezők és entitások létrehozása
description: A témakör ismerteti, hogyan hozhatók létre értékkészlet-halmazok és entitások saját megoldásban a Power Apps platformon.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: b9e32c8871a8986ba827f742baf4e4d5cd9dd235
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144866"
---
# <a name="create-custom-fields-and-entities"></a>Egyéni mezők és entitások létrehozása 

[!include [banner](../includes/psa-now-project-operations.md)]

Hajtsa végre az alábbi lépéseket minden olyan alkalommal, amikor egyéni értékkészletet vagy entitást szeretne létrehozni a Power Apps platformon.  
A témakör eljárásait a Project Service Automation (PSA) webfelületének használatával kell elvégezni.

> [!IMPORTANT]
> Javasoljuk, hogy minden egyéni árképzési dimenziót külön megoldásban hajtson végre. Ez a fontos gyakorlati tanács rugalmasságot biztosít a jövőben a változtatások frissítéséhez vagy eltávolításához szükség szerint, segítséget nyújt munkájának újbóli felhasználásában, és megkönnyíti a módosítások másik példányra való átvitelét. Miután elvégezte az összes szükséges módosítást, exportálja a megoldást **Felügyelt megoldásként**, majd importálja azt más példányokra az árképzési beállítások újbóli felhasználása céljából.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Egyéni mezők és értékkészletek létrehozása az árképzési dimenzió megoldásban

Az árképzési dimenzió lehet értékkészlet vagy entitás. Mindkettőt létre kell hozni az árképzési megoldásban. Az eljárás lépései ismertetik az entitás alapú dimenziók és az értékkészlet-alapú dimenziók létrehozását.

### <a name="entity-based-dimensions"></a>Entitásalapú dimenziók

1. A PSA-ban válassza ki a **Beállítások** > **Megoldások** lehetőséget, és kattintson duplán a(z) **\<your organization name> árazási dimenzióira**.
2. A Solution Explorerben a bal oldali navigációs panelen válassza az **Entitások** elemet.
3. Kattintson az **Új** elemre, és hozzon létre egy új entitást, melynek neve: **Standard cím**. Írja be a további szükséges információkat, majd kattintson a **Mentés** gombra.

> ![A standard című entitás meghatározása](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Értékkészlet-alapú dimenziók 
Két értékkészlet-alapú dimenziót hozhat létre. Használja az **Erőforrás munkahelye** elemet az **Otthon** végzett munka és a **Helyszíni** munka árának nyomon követéséhez, és használja az **Erőforrás munkaideje** elemet a **Rendszeres** és a **Túlóra** értékekkel, hogy jelöléssel láthassa el az elkészült munkát.


1. A PSA-ban válassza a **Beállítások** > **Megoldások** lehetőséget, és kattintson duplán a(z) **\<your organization name> árazási dimenzióira**. 
2. A Solution Explorerben a bal oldali navigációs panelen válassza az **Értékkészletek** elemet. 
3. Új értékkészlet létrehozásához kattintson az **Új** elemre, majd írja be a további szükséges információkat, majd kattintson a **Mentés** gombra.

> ![Erőforrás munkahelye nevű értékkészlet-alapú árképzési dimenzió ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Erőforrás munkaideje nevű értékkészlet-alapú árképzési dimenzió ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Adatok létrehozása entitásalapú dimenziókhoz

Entitásalapú dimenziókhoz manuálisan vagy Microsoft Excel importálással vagy szolgáltatáshívások használatával hozhat létre adatokat. Az eljárás lépéseinek követésévek hozhat létre két szabványos címet: a **Szabványos cím** entitásalapú dimenzióból származó **Rendszermérnök** és **Vezető rendszermérnök**. Ha a létrehozni kívánt adat kis méretű, a következő példához hasonlóan használhat szabványos űrlapot.

1. A PSA-ban kattintson a **Speciális keresés** elemre. Válassza ki a **Szabványos cím** entitást, majd kattintson az **Eredmények** elemre. A **Szabványos cím** összes sora megjelenik.
2. Kattintson az **Új** elemre. A **Név** mezőbe írja be a „Rendszermérnök” elemet, majd kattintson a **Mentés** elemre.
3. Zárja be az űrlapot. 
4. Ismételje meg az 1–3. lépést egy újabb szabványos cím létrehozásához a „Vezető rendszermérnök” esetében.

> ![Mintaadatok a szabványos cím entitáshoz ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]