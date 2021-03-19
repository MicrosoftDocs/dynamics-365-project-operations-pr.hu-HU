---
title: Árlisták beállítása
description: Ez a témakör a költség- és értékesítési árlisták beállításáról nyújt információkat.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 34ee7bb157426507ec7ca8c031f5cb552e85099b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275496"
---
# <a name="set-up-price-lists"></a>Árlisták beállítása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az árlisták a Dynamics 365 Project Operationsben az árfolyamok katalógusát képviselik. Az árak költség, értékesítési és számlázási árak kifejezésére szolgálnak. Attól függően, hogy az árlista a költségeket vagy az értékesítési és a számlázási díjakat tartalmazza, az árlista környezete **értékesítés** vagy **költség** lesz.

A következő kiterjesztések aProject Operationsra vonatkoznak, és a Dynamics 365 Salesből származó árlisták alapján kerülnek alkalmazásra.

- **Környezet**: Ez a mező a támogatott értékekkel rendelkezik: **költség** és **értékesítés**. A **Beszerzés** érték nem támogatott. Állítsa be a környezet **költség** értékre, hogy egy önköltségi árlistát hozzon létre, vagy állítsa a környezetet **értékesítés** értékre az értékesítési árlistához. Az önköltségi árlisták határozzák meg a költség típusának árát a becslés és a tényleges bejegyzések esetében. Az értékesítési árlisták határozzák meg a nem számlázott és számlázott értékesítési típusok becsült és tényleges rekordjainak árát.
- **Időegység**: ez az alapértelmezett időegység, amelyre vonatkozóan az ár a kapcsolódó **szerepkörár** táblában be van állítva ehhez az árlistához.
- **Árlista entitás**: Ez a rejtett mező a Project Operations segítségével megkülönbözteti az árajánlatot vagy a szerződésre jellemző árlistákat, amelyek a szabványosak, és a globálisan alkalmazandók.

## <a name="price-list-header"></a>Árlistafejléc

A következő táblázat tartalmazza az árlista **Általános** lapján található mezőket, amelyek egyediek a Project Operations esetében, vagy jelentős változásokkal rendelkeznek az értékesítésben szereplő árlisták esetében.

| Mező | Hely | Adatfolyam leírása | Alsóbb rétegbeli hatás |
| --- | --- | --- | --- |
| Adatfolyam neve | **Általános** lap és a **Gyorslétrehozás** űrlapok | Az árlista identitása. | Az árlista ezzel az értékkel jelenik meg minden lista és legördülő lapon.|
| Környezet | **Általános** lap és a **Gyorslétrehozás** űrlapok | Ez a mező a **költség** vagy **értékesítés** értékre állítható be. | A **költség** értékre beállított árlista a költségbecslések és a költségek tényleges árát keresi meg. A **Értékesítés** értékre beállított árlista az értékesítési becslések és a értékesítés tényleges árát keresi meg. Csak az **Értékesítés** környezetű árlisták csatolhatók az ügyfelek, projektárajánlatok és projektszerződések projektárlistáihoz. |
| Kezdő dátum | **Általános** lap és a **Gyorslétrehozás** űrlapok | Annak az időszaknak a kezdő dátuma, amelyben az árlista érvényben van. | A **Záró dátum** mező segítségével meghatározhatja, hogy egy adott becslésre vagy tényleges sorra vonatkozóan mely árlista alkalmazható. |
| Befejező dátum | **Általános** lap és a **Gyorslétrehozás** űrlapok | Annak az időszaknak a záró dátuma, amelyben az árlista érvényben van. | A **Kezdő dátum** mező segítségével meghatározhatja, hogy egy adott becslésre vagy tényleges sorra vonatkozóan mely árlista alkalmazható. |
| Pénznem | **Általános** lap és a **Gyorslétrehozás** űrlapok | Ez a mező az ehhez az árlistához kapcsolódó minden szerepkör, kategória vagy árlista típusú cikk sorában szereplő pénznem alapértelmezett értékének meghatározására szolgál. | Az **értékesítés** árlisták, szerepkörök, kategóriák vagy árlistacikkek nem hozhatók létre a pénznemtől eltérő pénznemben. Az **önköltségi** árlisták esetében bármilyen pénznemben létrehozható egy szerepkörár sor. Az itt megadott pénznem alapértelmezésként használatos. A szerepkörárakhoz kapcsolódó felhasználói beállítás felülírhatja ezt az értéket, ha bármilyen pénznemben engedélyezi a munkaköltségi ráta beállítását. A kategória költségrátái és árlistacikkek költségei csak az itt megadott pénznemben állíthatók be. |
| Időegység | **Általános** lap és a **Gyorslétrehozás** űrlapok | Ez a mező az ehhez az árlistához kapcsolódó minden szerepkör időegységének alapértelmezett értékének meghatározására szolgál. | Ez a mezőérték csak a kapcsolódó szerepkörár beállításokban használatos. Az **önköltségi** és **Értékesítési** árlisták esetében bármilyen időegységben létrehozható egy szerepkörár sor. Az itt megadott időegység alapértelmezésként használatos. A szerepkörárakhoz kapcsolódó felhasználói beállítás felülírhatja ezt az értéket, ha bármilyen időegységben engedélyezi a munkaköltségi és számlázási ráta beállítását. |
| Adatfolyam leírása | **Általános** lap és a **Gyorslétrehozás** űrlapok | Ez a szövegmező lehetővé teszi, hogy az árlista többsoros leírását adja meg. | Ez a mező az árlista **Társított** nézetében jelenik meg a kapcsolódó árlistát tartalmazó különböző entitásokokban. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]