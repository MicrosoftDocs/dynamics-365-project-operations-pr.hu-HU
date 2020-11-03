---
title: Egyéni megoldások létrehozása árképzési dimenziókra
description: Ez a témakör ismerteti, hogyan lehet egyéni megoldást létrehozni egyéni árképzési dimenziók létrehozásakor.
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
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078101"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Egyéni megoldások létrehozása árképzési dimenziókra

> [!IMPORTANT]
> Az egyéni árképzésidimenzió-változásoknak külön megoldásban kell lenniük. Ez a fontos gyakorlati tanács rugalmasságot biztosít a jövőben a változtatások frissítéséhez vagy eltávolításához szükség szerint, segítséget nyújt munkájának újbóli felhasználásában, és megkönnyíti a módosítások másik példányra való átvitelét. Miután elvégezte az összes szükséges módosítást, exportálja a megoldást **Felügyelt megoldásként** , majd importálja azt más példányokra az árképzési beállítások újbóli felhasználása céljából.

1. Válassza a **Beállítások** > **Megoldások** opciót, majd az **Új** lehetőséget. 
2. Nevezze el a megoldást, ( **\<your organization name> árképzési dimenziók** ), írja be a további szükséges információkat, majd kattintson a **Mentés** gombra.

> ![Egyéni megoldás létrehozása árképzési dimenziókra](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Adja hozzá az összes szükséges entitást és a kapcsolódó komponenseket az árképzési dimenzió megoldáshoz
A következő Project Service entitásokat kell hozzáadnia az árképzési megoldáshoz. Az eljárás lépéseit követve végezzen el néhány fontos sémaváltoztatást az árképzési megoldásban, hogy az entitások megismerjék az új árképzési dimenziókat.

1. Válassza a **Beállítások** > **Megoldások** lehetőséget, és kattintson duplán a(z) **\<your organization name> árazási dimenzióira**. 
2. A Solution Explorerben a bal oldali navigációs panelen válassza a **Meglévő hozzáadása** > **Entitások** elemet.
3. A **Megoldás összetevői** párbeszédpanelen válassza ki a következő entitásokat:

- Tényadat
- Lefoglalható erőforrás
- Becsléssor
- Projektfeladat
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

4. Amikor a rendszer felkéri egy függő entitásnak a kiválasztott entitásokhoz való felvételére, kattintson a **Nem** elemre.

> ![Ne adja hozzá az összes kapcsolódó komponenst](media/Do-not-include-required.png)


