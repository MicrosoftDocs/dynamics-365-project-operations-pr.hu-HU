---
title: Alvállalkozói szerződéses sorok forrásai
description: Ez a témakör elmagyarázza, hogyan lehet megadni a szállító által egy adott alvállalkozói szerződéssorhoz biztosított dedikált erőforrásokat az időre vonatkozóan.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323374"
---
# <a name="subcontract-line-resources"></a>Alvállalkozói szerződéses sorok forrásai

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Dynamics 365 Project Operations rendszerben a szállító megadhatja azokat az erőforrásokat, amelyeket az alvállalkozói szerződéssoron megvásárolt erőforrás-kapacitás időre történő ellátására használ.

## <a name="create-subcontract-line-resources"></a>Alvállalkozói sor erőforrásainak létrehozása

Az alvállalkozói sor erőforrásainak létrehozásához hajtsa végre a következő lépéseket.

1. A navigációs ablaktáblán válassza az **Alvállalkozói szerződések** elemet, és nyissa meg azt az alvállalkozói szerződést, amellyel dolgozni szeretne.
2. Nyissa meg az alvállalkozói szerződés azon sorát, amelyre vonatkozóan meg kívánja adni a szállítói erőforrásokat.
3. Az **Alvállalkozói szerződéssor erőforrásai** lapon, az alrácson válassza a **+ Új alvállalkozói szerződéssor erőforrása** lehetőséget.
4. Az **Új alvállalkozói szerződéssor mérföldkő** lapon adja meg a szükséges információkat, majd válassza a **Mentés és bezárás** lehetőséget.

A következő táblázat az alvállalkozói szerződéssor erőforrás mezőit ismerteti.

| Mező |  Ismertetés |
| ----- | ------------ |
| Lefoglalható erőforrás | Válassza ki a „Szerződéses munkavállaló” típusú foglalható erőforrást, amelyet az alvállalkozói soron erőforrásként kíván használni. Ha még nem hozott létre foglalható erőforrást a szerződéses munkavállaló számára, hagyja üresen ezt a mezőt. A rekord mentésekor létrejön egy foglalható erőforrás.  |
| Kapcsolat | Ha a **Foglalható erőforrás** mező üres, akkor az alvállalkozói sor erőforrását egy meglévő kapcsolatból hozhatja létre. A keresés segítségével megtekintheti a rendszerben lévő aktív kapcsolatok listáját. Válassza ki az alvállalkozó szállítójának kapcsolattartóját. A kiválasztott kapcsolat a rekord mentésekor érvényesítésre kerül. Ha a kiválasztott kapcsolat nem érvényes kapcsolat, a rekord nem kerül mentésre. Ha a kiválasztott kapcsolathoz nincs foglalható erőforrás, a rendszer az alvállalkozói sor erőforrásának létrehozása előtt létrehoz egy foglalható erőforrást a kiválasztott kapcsolathoz. |
| Felhasználó | Ha a **Foglalható erőforrás** mező üres, akkor egy aktív felhasználó kiválasztásával hozhat létre alvállalkozói sor erőforrást. A keresés segítségével megtekintheti a rendszerben lévő aktív felhasználók listáját. Ha nincs foglalható erőforrás a kiválasztott felhasználó számára, a rendszer létrehoz egy foglalható erőforrást a kiválasztott felhasználó számára, mielőtt az alvállalkozói sor erőforrása létrejönne. |
| Kezdő dátum | Az alvállalkozói megbízás kezdetének időpontja. Ha ez az erőforrás olyan időszakra van lefoglalva, amely az adott dátumtartomány előttre esik, figyelmeztetés jelenik meg. |
| Befejező dátum | Az alvállalkozói megbízás befejezésének időpontja. Ha ezt az erőforrást olyan időszakra foglalják le, amely ezen a dátumtartományon túlra esik, figyelmeztetés jelenik meg. |
| Munkamennyiség | Az alvállalkozó által az adott alvállalkozói szerződéses sorra fordított munkaórák teljes száma. Ha ezt az erőforrást az adott alvállalkozói szerződéshez rendelt munkaidőn túl foglalják le, figyelmeztetés jelenik meg. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
