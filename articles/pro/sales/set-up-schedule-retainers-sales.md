---
title: Foglalók ütemezésének beállítása – Lite
description: Ez a témakör információt nyújt a foglalói ütemezés beállításáról a Project Operations szolgáltatásban.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e0312b89d9969f140146b6aaaa9bdcfde702c0b
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181275"
---
# <a name="set-up-a-retainer-schedule---lite"></a>Foglalók ütemezésének beállítása – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A foglalói ütemezések beállítása a Dynamics 365 Project Operations **projektszerződés** lapján állítható be.

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
