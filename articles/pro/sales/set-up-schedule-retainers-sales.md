---
title: Foglalóütemezés beállítása
description: Ez a témakör információt nyújt a foglalói ütemezés beállításáról a Project Operations szolgáltatásban.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a1cfd83837a91a8d1b3db6df688da6e216a90ada4735e5909a7e8cb26b87247d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994369"
---
# <a name="set-up-a-retainer-schedule"></a>Foglalóütemezés beállítása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A foglalói ütemezések beállítása a Dynamics 365 Project Operations **Projektszerződés** lapján állítható be.

1. A **projektszerződés** lap **előlegek és foglalók** lapján jelölje be a **Foglalói ütemezés beállítása** jelölőnégyzetet.
2. A megnyíló párbeszédpanelen a következő táblázatban látható mezők jelennek meg. A táblázat azt ismerteti, hogy a beírt értékek hogyan hatnak vagy befolyásolják a létrehozott foglalói ütemezést.

| Mező | Adatfolyam leírása | Alsóbb rétegbeli hatás |
| --- | --- | --- |
| Projektszerződés ügyfele | A Szerződés azon ügyfele, akinek ezt a foglalót vagy előleget kiszámlázzák. | Ha a Szerződés több ügyfelet tartalmaz, és ha mindegyiküknek ki kell számláznia egy adott foglaló vagy előleg összegét, akkor minden ügyfélhez kézzel hozzon létre egy számlát. |
| Foglaló ütemezésének kezdése | Adja meg a foglalói ütemezés kezdetének dátumát. | Ez a dátum nem lehet az első foglaló vagy előleg létrehozásának dátuma. Az első foglaló vagy az előleg létrehozásának dátumát a számla gyakorisága is befolyásolja. |
| Foglaló ütemezésének vége | Adja meg a foglalói ütemezés befejezési dátumát. | Ez a dátum nem lehet az utolsó foglaló vagy előleg létrehozásának dátuma. Az utolsó foglaló vagy az előleg létrehozásának dátumát a számla gyakorisága is befolyásolja. |
| Létrehozandó foglalók száma | Ha megadja a létrehozandó foglalók számát, a rendszer a kezdési dátumot és gyakoriságot használja a mezőben a szám létrehozásához. | A mező manuális frissítésekor a rendszer figyelmen kívül hagyja a **Foglalói ütemezési vége** mezőben szereplő értéket, és ehelyett létrehozza a foglalók vagy előlegek adott számát. |
| Számlázási gyakoriság | Milyen gyakran hozza létre az alkalmazás a foglalókat és az előlegeket? | Ez az érték közvetlenül befolyásolja a foglalók és az előlegek számát, valamint a létrehozott dátumokat. |
| Összmennyiség | A teljes összeg az az összeg, amelyet a létrehozandó egyéni foglalói vagy a előlegfizetések között oszt meg. | Ennek a mezőnek nincs későbbi hatása. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]