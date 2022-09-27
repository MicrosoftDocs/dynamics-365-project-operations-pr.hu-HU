---
title: Alvállalkozói szerződéses sorok forrásai
description: Ez a cikk azt ismerteti, hogyan adhatja meg azokat a dedikált erőforrásokat, amelyeket a szállító biztosít egy adott alvállalkozói sorhoz az időre.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 04e3e5ee70c50068304a8a6c8f7e93df48ed7e85
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522375"
---
# <a name="subcontract-line-resources"></a>Alvállalkozói szerződéses sorok forrásai

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations rendszerben a szállító megadhatja azokat az erőforrásokat, amelyeket az alvállalkozói szerződéssoron megvásárolt erőforrás-kapacitás időre történő ellátására használ.

## <a name="create-subcontract-line-resources"></a>Alvállalkozói sor erőforrásainak létrehozása

Az alvállalkozói sor erőforrásainak létrehozásához hajtsa végre a következő lépéseket.

1. A navigációs ablaktáblán válassza az **Alvállalkozói szerződések** elemet, és nyissa meg azt az alvállalkozói szerződést, amellyel dolgozni szeretne.
2. Nyissa meg az alvállalkozói szerződés azon sorát, amelyre vonatkozóan meg kívánja adni a szállítói erőforrásokat.
3. Az **Alvállalkozói szerződéssor erőforrásai** lapon, az alrácson válassza a **+ Új alvállalkozói szerződéssor erőforrása** lehetőséget.
4. Az **Új alvállalkozóiszerződés-sor erőforrás** lapon adja meg a szükséges adatokat, majd válassza a **Mentés és bezárás** lehetőséget.

A következő táblázat az alvállalkozói szerződéssor erőforrás mezőit ismerteti.

| Mező | Ismertetés | Funkcionális hatás |
| ----- | ----------- | ----------------- |
| Lefoglalható erőforrás | Válassza ki a **Szerződéses munkavállaló** típusú foglalható erőforrást, amelyet az alvállalkozói soron erőforrásként kíván használni.| Ha nem hozott létre foglalható erőforrást a szerződés dolgozó számára, hagyja üresen ezt a mezőt. A bejegyzés mentésekor egy foglalható erőforrás jön létre.  |
| Kapcsolat | Az alvállalkozóiszerződéssor-erőforrás meglévő kapcsolattartóból hozható létre. A keresés segítségével megtekintheti a rendszerben lévő aktív kapcsolatok listáját. Válassza ki az alvállalkozó szállítójának kapcsolattartóját. Ha a kijelölt kapcsolattartó nem az alvállalkozói szerződés szállítójának érvényes kapcsolattartója, az alvállalkozóiszerződéssor-erőforrás rekordját nem menti a rendszer.| Ha a kiválasztott kapcsolathoz nincs foglalható erőforrás, a rendszer az alvállalkozói sor erőforrásának létrehozása előtt létrehoz egy foglalható erőforrást a kiválasztott kapcsolathoz. |
| Felhasználó | Alvállalkozóiszerződéssor-erőforrást egy aktív felhasználó kiválasztásával hozhat létre. A keresés segítségével megtekintheti a rendszerben lévő aktív felhasználók listáját.| Ha nincs foglalható erőforrás a kiválasztott felhasználó számára, a rendszer létrehoz egy foglalható erőforrást a kiválasztott felhasználó számára, mielőtt az alvállalkozói sor erőforrása létrejönne. |
| Kezdő dátum | Az alvállalkozói megbízás kezdetének időpontja.| Ha ez az erőforrás olyan időszakra van lefoglalva, amely az adott dátumtartomány előttre esik, figyelmeztetés jelenik meg. |
| Befejező dátum | Az alvállalkozói megbízás befejezésének időpontja.| Ha ezt az erőforrást olyan időszakra foglalják le, amely ezen a dátumtartományon túlra esik, figyelmeztetés jelenik meg. |
| Munkamennyiség | A munkaórák teljes száma, amit a szerződéses munkavállaló az alvállalkozói szerződéssorral tölt.| Ha ez az erőforrás túl van foglalva az alvállalkozói szerződés által biztosított munkaidőhöz képest, akkor figyelmeztetés jelenik meg. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
