---
title: Árlisták másolása
description: Ez a témakör az árlisták Project Operations alkalmazásban való másolásáról nyújt tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 67a69d521ac0a5632371138bd4fbb9dd00fe34ee
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181500"
---
# <a name="copy-price-lists"></a>Árlisták másolása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations alkalmazásban az árlisták másolatát is létrehozhatja. Lehetőség van például arra, hogy az aktuális évhez tartozó árlistát használva a soron következő évhez tartozó árlistát hozzon létre.  Másik lehetőségként az önköltségek árlistája is átmásolható számlázási árak és eladási árak árlistájának létrehozásához. 

A következő lépések végrehajtásával készítheti el az árlista másolatát.

1. Nyissa meg azt az árlistát, amelyről másolatot szeretne készíteni, és válassza a **Másolás** lehetőséget.
2. Adja meg az árlista másolásához szükséges adatokat. A következő táblázat azt mutatja be, hogy milyen szempontokat érdemes figyelembe venni az adatok megadásakor.

| Mező | Adatfolyam leírása | Alsóbb rétegbeli hatás |
| --- | --- | --- |
| Adatfolyam neve | A forrás árlista neve, amelyhez a **másolat** van hozzáfűzve. | Az árlista ezt az étéket tartalmazza minden lista és legördülő lapon. |
| Környezet | Adja meg a célárlistához használni kívánt környezetet. | A **Költség** kontextussal rendelkező árlista a költségbecslések és a költségek tényleges árát keresi meg. A **Értékesítés** kontextussal rendelkező árlista az értékesítési becslések és a értékesítés tényleges árát keresi meg. Csak az **Értékesítés** környezetű árlisták csatolhatók az ügyfelek, ajánlatok és szerződések projektárlistáihoz. |
| Kezdő dátum | Annak az időszaknak a kezdő dátuma, amelyben az árlista érvényben van. | A **Záró dátum** mezővel együtt meghatározhatja, hogy egy adott becslésre vagy tényleges sorra vonatkozóan mely árlista alkalmazható. |
| Befejező dátum | Annak az időszaknak a záró dátuma, amelyben az árlista érvényben van. | A **Kezdő dátum** mezővel együtt meghatározhatja, hogy egy adott becslésre vagy tényleges sorra vonatkozóan mely árlista alkalmazható. |
| Pénznem | A forrás árlista pénzneme. Ez módosítható. | Ha ez módosul, a rendszer az összes, a munka, a költség és a termékkatalógus elemeiből származó sort átalakítja a cél árlista pénznemére a másolás során. |
| Időegység | A forrás árlista pénzneme. Ez módosítható. | Ha ez módosul, a rendszer az összes, a munka elemeiből származó sort átalakítja a cél árlista egységére a másolás során. Az átváltás az egységbeállításból a forrásárlista időegysége és a cél árlista időegységéhez lesz használva. |
| Adatfolyam leírása | A forrás árlista leírása, amelyhez a **másolat** van hozzáfűzve. Ez a szövegmező lehetővé teszi, hogy az árlistához többsoros leírást adjon meg. | Ez a mező az árlista **Társított** nézetében jelenik meg a kapcsolódó árlistát tartalmazó különböző entitásokokban. |

3. Az árlista mentése. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Árlista frissítése az árakra vonatkozó növelések alkalmazásával

1. Egy árlista **Szerepkör**, **Kategória** és **Árlistaelem** lapjain kiválaszthatja az **Árak frissítése** lehetőséget, hogy árrést alkalmazzon az alrácsban szereplő összes ár esetében. 
2. A megnyíló párbeszédpanel lapján adjon meg egy növelést. Negatív növelést is megadhat, ha bizonyos százalékkal csökkenti az árakat. 
3. Válassza az **OK** lehetőséget a párbeszédpanelen, és ellenőrizze, hogy az alrácsban szereplő árak tükrözik-e az elvégzett módosításokat.