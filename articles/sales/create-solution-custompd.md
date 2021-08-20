---
title: Megoldás létrehozása egyéni árképzési dimenziókhoz
description: Ez a témakör az árazási dimenziókhoz tartozó megoldások létrehozásáról nyújt információt.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 753f0c4496bafd43d7e4a399cedeb355c2163c7ce56d932b2c786d5f2e672b6b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992209"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Megoldás létrehozása egyéni árképzési dimenziókhoz

 _**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_ 

>[!IMPORTANT]
>Az egyéni árképzésidimenzió-változásoknak külön megoldásban kell lenniük. Ez a fontos gyakorlati tanács rugalmasságot biztosít a változtatások frissítéséhez vagy eltávolításához szükség szerint, segítséget nyújt munkájának újbóli felhasználásában, és megkönnyíti a módosítások másik példányra való átvitelét. Miután elvégezte az összes szükséges módosítást, exportálja a megoldást **Felügyelt** megoldásként, majd importálja azt más példányokra az újbóli felhasználása céljából.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Megoldás létrehozása egyéni árképzési dimenziókhoz

1.  Válassza a **Beállítások** > **Megoldások** opciót, majd az **Új** lehetőséget.
2.  Nevezze el a megoldást, *<your organization name> árképzési dimenzióka*.
3. Írja be a további szükséges információt, majd kattintson a **Mentés** gombra.

  ![Egyéni árképzési megoldás létrehozása.](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Adja hozzá az összes szükséges entitást és a kapcsolódó komponenseket az árképzési dimenzió megoldáshoz

Adja hozzá a következő Project Service-entitásokat az árképzési megoldáshoz, hogy fontos sémamódosításokat hajtson végre az árképzési megoldásban. Miután befejezte ezt az eljárást, az entitások felismerik az új árképzési dimenziókat.

1.  Válassz a **Beállítások** > **Megoldások** elemez, majd kattintson duplán a **<*szervezet neve*> árazási dimenziók** elemre.
2.  A Solution Explorerben a bal oldali navigációs panelen válassza a **Meglévő hozzáadása** > **Entitások** elemet.
3.  A **Megoldás összetevői** párbeszédpanelen válassza ki a következő entitásokat:
 
   - **Tényadat**
   - **Lefoglalható erőforrás**
   - **Becsléssor**
   - **Projektfeladat**
   - **Számlasor részletei**
   - **Naplósor**
   - **Projektszerződés sorának részletei**
   - **Projektcsoporttag**
   - **Árajánlatsor részletei**
   - **Szerepkörárrés**
   - **Szerepkörár**
   - **Időbejegyzés**
 
   ![Adjon hozzá meglévő entitásokat az árképzési dimenzió megoldáshoz.](./media/Existing-entities-to-PD-solution.png)
 
 4. Tekintse át az egyes entitások hozzáadott összetevőit és az egyes entitások entitáseszközeinek végleges listáját. 

   >[!NOTE]
   > Minden kiválasztott entitás tartalmazzon minden űrlapot és nézetet.

  ![Hozzáadott entitások.](./media/solution-component-selection.png)


5.  Amikor a rendszer kéri, hogy a kijelölt entitások függő entitásait is adja hozzá, válassza a **Nem adom hozzá a szükséges összetevőket** lehetőséget.

    ![Függő entitásokkal együtt.](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]