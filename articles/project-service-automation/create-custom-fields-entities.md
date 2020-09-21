---
title: Egyéni mezők és entitások létrehozása
description: A témakör ismerteti, hogyan hozhatók létre értékkészlet-halmazok és entitások saját megoldásban a Power Apps platformon.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752291"
---
# <a name="create-custom-fields-and-entities"></a>Egyéni mezők és entitások létrehozása 

Hajtsa végre az alábbi lépéseket minden olyan alkalommal, amikor egyéni értékkészletet vagy entitást szeretne létrehozni a Power Apps platformon.  
A témakör eljárásait a Project Service Automation (PSA) webfelületének használatával kell elvégezni.

> [!IMPORTANT]
> Javasoljuk, hogy minden egyéni árképzési dimenziót külön megoldásban hajtson végre. Ez a fontos gyakorlati tanács rugalmasságot biztosít a jövőben a változtatások frissítéséhez vagy eltávolításához szükség szerint, segítséget nyújt munkájának újbóli felhasználásában, és megkönnyíti a módosítások másik példányra való átvitelét. Miután elvégezte az összes szükséges módosítást, exportálja a megoldást **Felügyelt megoldásként**, majd importálja azt más példányokra az árképzési beállítások újbóli felhasználása céljából.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Egyéni megoldás létrehozása árképzési dimenziókra
1. A PSA-ban kattintson a **Beállítások** > **Megoldások** lehetőségre, majd az **Új** lehetőségre új megoldás létrehozásához. 
2. Nevezze el a megoldást, **\<a szervezet neve> árképzési dimenziók**, írja be a további szükséges információkat, majd kattintson a **Mentés** gombra.

> ![Egyéni megoldás létrehozása árképzési dimenziókra](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Egyéni mezők és értékkészletek létrehozása az árképzési dimenzió megoldásban

Az árképzési dimenzió lehet értékkészlet vagy entitás. Mindkettőt létre kell hozni az árképzési megoldásban. Az eljárás lépései ismertetik az entitás alapú dimenziók és az értékkészlet-alapú dimenziók létrehozását.

### <a name="entity-based-dimensions"></a>Entitásalapú dimenziók

1. A PSA-ban kattintson a **Beállítások** > **Megoldások** elemre, majd kattintson duplán a **\<szervezet neve> árazási dimenziók** elemre.
2. A Solution Explorerben a bal oldali navigációs panelen válassza az **Entitások** elemet.
3. Kattintson az **Új** elemre, és hozzon létre egy új entitást, melynek neve: **Standard cím**. Írja be a további szükséges információkat, majd kattintson a **Mentés** gombra.

> ![A standard című entitás meghatározása](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Értékkészlet-alapú dimenziók 
Két értékkészlet-alapú dimenziót hozhat létre. Használja az **Erőforrás munkahelye** elemet az **Otthon** végzett munka és a **Helyszíni** munka árának nyomon követéséhez, és használja az **Erőforrás munkaideje** elemet a **Rendszeres** és a **Túlóra** értékekkel, hogy jelöléssel láthassa el az elkészült munkát.


1. A PSA-ban kattintson a **Beállítások** > **Megoldások** elemre, majd kattintson duplán a **\<szervezet neve> árképzési dimenziók** elemre. 
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

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Adja hozzá az összes szükséges PSA-entitást és kapcsolódó komponenseket az árképzési dimenzió megoldáshoz.
A következő Project Service entitásokat kell hozzáadnia az árképzési megoldáshoz. Az eljárás lépéseit követve végezzen el néhány fontos sémaváltoztatást az árképzési megoldásban, hogy az entitások megismerjék az új árképzési dimenziókat.

1. A PSA-ban kattintson a **Beállítások** > **Megoldások** elemre, majd kattintson duplán a **\<szervezet neve> árazási dimenziók** elemre. 
2. A Solution Explorerben a bal oldali navigációs panelen válassza a **Meglévő hozzáadása** > **Entitások** elemet.
3. A **Megoldás összetevői** párbeszédpanelen válassza ki a következő entitásokat:

- Tény
- Lefoglalható erőforrás
- Becsléssor
- Számlasor részletei
- Naplósor
- Projektszerződés sorának részletei
- Projektcsoporttag
- Árajánlatsor részletei
- Szerepkörárrés
- Szerepkörár 
- Időbejegyzés 

> ![Adjon hozzá meglévő elemeket az árképzési dimenzió megoldáshoz](media/Existing-entities-to-PD-solution.png)

> ![Megoldás-összetevők kiválasztása](media/Dimension-Components.png)

> [!NOTE]
> Ügyeljen arra, hogy minden kiválasztott entitás tartalmazzon minden űrlapot és nézetet.

4. Amikor a rendszer felkéri függő entitásának felvételére a fentebb kiválasztott entitásokhoz, kattintson a **Nem** elemre.

> ![Ne adja hozzá az összes kapcsolódó komponenst](media/Do-not-include-required.png)


