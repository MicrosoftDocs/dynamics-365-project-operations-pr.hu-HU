---
title: Egyéni mezők és entitások létrehozása árazási dimenzióként
description: Ez a témakör az egyéni értékkészletek és entitások létrehozását ismerteti.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2000f7e710267560fe2bd52b0e33024617d108ea
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898264"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Egyéni mezők és entitások létrehozása árazási dimenzióként

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Ha egyéni értékkészletet vagy entitást szeretne létrehozni, hajtsa végre az alábbi lépéseket.

> [!IMPORTANT]
> Javasoljuk, hogy minden egyéni árképzési dimenziót külön megoldásban hajtson végre. Ez a fontos gyakorlati tanács rugalmasságot biztosít a jövőben a változtatások frissítéséhez vagy eltávolításához szükség szerint, segítséget nyújt munkájának újbóli felhasználásában, és megkönnyíti a módosítások másik példányra való átvitelét. Miután elvégezte az összes szükséges módosítást, exportálja a megoldást **Felügyelt megoldásként**, majd importálja azt más példányokra az árképzési beállítások újbóli felhasználása céljából.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Egyéni megoldás létrehozása árképzési dimenziókra
1. Új megoldás létrehozásához lépjen a **Beállítások** > **Megoldások** részre, és válassza az **Új** lehetőséget. 
2. Nevezze el a megoldást, (**\<your organization name> árképzési dimenziók**), írja be a további szükséges információkat, majd kattintson a **Mentés** gombra.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Egyéni mezők és értékkészletek létrehozása az árképzési dimenzió megoldásban

Az árképzési dimenzió lehet értékkészlet vagy entitás. Mindkettőt létre kell hozni az árképzési megoldásban. Az eljárás lépései ismertetik az entitás alapú dimenziók és az értékkészlet-alapú dimenziók létrehozását.

### <a name="entity-based-dimensions"></a>Entitásalapú dimenziók

1. Lépjen a **Beállítások** > **Megoldások** részre, és kattintson duplán a(z) **\<your organization name> árképzési dimenzióira**.
2. A Solution Explorerben a bal oldali navigációs panelen válassza az **Entitások** elemet.
3. Válassza az **Új** lehetőséget, és hozzon létre egy **Standard cím** nevű új entitást. 
4. Írja be a további szükséges információt, majd kattintson a **Mentés** gombra.


### <a name="option-set-based-dimensions"></a>Értékkészlet-alapú dimenziók 
Két értékkészlet-alapú dimenziót hozhat létre. Használja az **Erőforrás munkahelye** elemet az **Otthon** végzett munka és a **Helyszíni** munka árának nyomon követéséhez, és használja az **Erőforrás munkaideje** elemet a **Rendszeres** és a **Túlóra** értékekkel, hogy jelöléssel láthassa el az elkészült munkát.


1. Lépjen a **Beállítások** > **Megoldások** részre, és kattintson duplán a(z) **\<your organization name> árképzési dimenzióira**. 
2. A Solution Explorerben a bal oldali navigációs panelen válassza az **Értékkészletek** elemet. 
3. Új értékkészlet létrehozásához kattintson az **Új** elemre, majd írja be a további szükséges információkat, majd kattintson a **Mentés** gombra.

## <a name="create-data-for-entity-based-dimensions"></a>Adatok létrehozása entitásalapú dimenziókhoz

Entitásalapú dimenziókhoz manuálisan vagy Microsoft Excel importálással vagy szolgáltatáshívások használatával hozhat létre adatokat. Az eljárás lépéseinek követésévek hozhat létre két szabványos címet: a **Szabványos cím** entitásalapú dimenzióból származó **Rendszermérnök** és **Vezető rendszermérnök**. Ha a létrehozni kívánt adat kis méretű, a következő példához hasonlóan használhat szabványos űrlapot.

1. Válassza az **Irányított keresés** lehetőséget, válassza ki az entitás **Normál címét**, majd válassza az **Eredmények** lehetőséget. A **Szabványos cím** összes sora megjelenik.
2. Válassza az **Új** lehetőséget, és a **Név** mezőbe írja be a „Rendszermérnök” elemet, majd kattintson a **Mentés** gombra.
3. Az űrlap bezárása. 
4. Ismételje meg az 1–3. lépést egy újabb szabványos cím létrehozásához a „Vezető rendszermérnök” esetében.

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Adja hozzá az összes szükséges entitást és a kapcsolódó komponenseket az árképzési dimenzió megoldáshoz.
A következő entitásokat kell hozzáadnia az árképzési megoldáshoz. Az eljárás lépéseit követve végezzen el néhány fontos sémaváltoztatást az árképzési megoldásban, hogy az entitások megismerjék az új árképzési dimenziókat.

1. Válassza a **Beállítások** > **Megoldások** lehetőséget, és kattintson duplán a(z) **\<your organization name> árazási dimenzióira**. 
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


> [!NOTE]
> Ügyeljen arra, hogy minden kiválasztott entitás tartalmazzon minden űrlapot és nézetet.

4. Amikor a rendszer felkéri a függő entitás fent megadott entitásokhoz való felvételére, kattintson a **Nem** elemre.

