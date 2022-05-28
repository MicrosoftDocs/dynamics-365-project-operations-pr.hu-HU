---
title: Az erőforrások számlázható kihasználtságának megtekintése
description: Ez a témakör információkat nyújt az erőforrás-kihasználtsági nézetről.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 0f6240a3337eb78496570ddfabc85d431e61d640
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595639"
---
# <a name="view-chargeable-utilization-for-resources"></a>Az erőforrások számlázható kihasználtságának megtekintése

[!include [banner](../includes/psa-now-project-operations.md)]
 
A **Project Service Erőforrás-kihasználtság** oldal **Kihasználtsági nézete** az egyes foglalható erőforrások számlázható kihasználtságát jeleníti meg. Mivel a nézet az ütemezési táblán alapul, így számos funkció azonos.

> ![Képernyőkép: Erőforrás-kihasználtság nézet.](media/FAQ-utilization-1.png)
 

A számlázható kihasználtság számítása a következőképpen történik:

   Számlázható kihasználtság = (számlázható tényleges óra)/(erőforrás kapacitása)

A cellák a kiválasztott időszakra (nap, hét vagy hónap) számított számlázható kihasználtságot jelentik.

A színek minden cella esetében az erőforrás számlázható kihasználtságát jelenítik meg a cél számlázható kihasználtsághoz képest. 

A cél kihasználtság az erőforrás alapértelmezett szerepkörén vagy az egyes erőforrásokon állítható be. A számítás először az adott személynél keresi a célt, majd az erőforrás alapértelmezett szerepkörén.

## <a name="set-target-on-a-resource"></a>Állítson be célt egy erőforráson

1. Lépjen a **Források** \> **Források** oldalra. 
2. Válasszon egy erőforrást a rekord megnyitásához. 
3. A **Project Service** lapon beállíthatja az erőforrás cél kihasználtságát.

> ![A Project Service lapjának használata a cél kihasználtság megadásához – képernyőkép.](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Állítsa be a cél kihasználtságot egy szerepkörön

1. Lépjen az **Erőforrások** \> **Erőforrás-szerepkörök** oldalra. 
2. Válasszon ki egy szerepkört, és nyissa meg a rekordot. 
3. A cél kihasználtság beállítása a szerepkörhöz.

> ![Az Erőforrás-szerepkörök használata a cél kihasználtság megadásához – képernyőkép.](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Számítsa ki az erőforrás számlázható kihasználtságát.

Az erőforrás számlázható kihasználtságának kiszámításához el kell végeznie a szükséges konfigurációs lépéseket. 

### <a name="set-default-role-for-individual-resource"></a>Állítsa be az alapértelmezett szerepet az egyes erőforrásokhoz

Elsőként a cél kihasználtságot kell beállítani az egyes erőforrásokon vagy erőforrás-szerepkörökön. Ha erőforrás-szerepköröket használ a célokhoz, minden egyes erőforrásnak egy alapértelmezett szerepkörrel kell rendelkeznie. 

1. Ennek beállításához lépjen az **Erőforrások** \> **Erőforrások** oldalra. 
2. Válasszon ki egy erőforrást, nyissa meg a rekordot, majd válassza ki a **Project Service** fület. 
3. Az **Erőforrás-szerepkör** rácsban ellenőrizze, hogy egy szerep tartozik az erőforráshoz, és az **Alapértelmezett** beállítás **Igen** értékű-e.
 
### <a name="change-billing-type-for-resource-role"></a>Módosítsa az erőforrás-szerepkör számlázási típusát.

Az erőforrás-szerepköröket úgy kell beállítani, hogy a számlázási típus **Számlázható** legyen. 

1. Lépjen az **Erőforrások** \> **Erőforrás-szerepkörök** oldalra. 
2. Nyissa meg a frissíteni kívánt rekordot, majd állítsa be a számlázási típus alapértelmezett állapotát **Számlázható** értékre.

### <a name="set-working-hours-for-resource-role"></a>Állítsa be a munkaórákat az erőforrás-szerepkörhöz
 
Az erőforrásnak munkaórákkal kell rendelkeznie a kapacitásszámításhoz. 

1. Lépjen a **Források** \> **Források** oldalra. 
2. Válasszon egy erőforrást a rekord megnyitásához, majd válassza ki a **Munkaórák megjelenítése** lehetőséget. 
3. Tömegesen is frissítheti az erőforrásokat, az **Erőforráslista** nézetből a **Munkaórasablon** alkalmazásával.

## <a name="troubleshooting-chargeable-actual-hours"></a>Számlázható tényleges órák hibaelhárítása

A ténylegesen fizetendő órák a **Tényadatok** entitásból származnak. A **számlázható** típusú tényleges órák részei a kiszámításnak, és emiatt rendelkeznie kell olyan projektekkel, ahol tényleges órák számlázhatók.

Ha nem látható számlázható kihasználtság, az alábbi néhány dolgot ellenőrizheti:

- Az erőforrás kapacitásánál vannak munkaórák.
- Az erőforrásnak van vagy egyedileg meghatározott kihasználtsági célja, vagy egy alapértelmezett szerepkör van hozzárendelve. A szerepkörhöz meg van határozva kihasználtsági cél.
- A tényleges órák rendelkeznek **számlázható** számlázási típussal arra az időszakra, amelyre kihasználtsági számítás elvégzése várható. Ellenőrizze a következőket, ha azt látja, hogy a tényleges órák számlázási típusa eltér a számlázhatótól:

  - A tényleges órákhoz használt szerepkör alapértelmezett számlázási típusa eltér a számlázhatótól.
  - A projekt mögöttes projekt szerződéssorán levő szerepkör nem számlázhatóra van beállítva.
  - A projektnek nincs hozzárendelt szerződéssora.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
