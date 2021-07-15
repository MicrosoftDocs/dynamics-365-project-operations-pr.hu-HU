---
title: Projektszámla-javaslatok teljesítménye
description: Ez témakör a projektszámla-javaslatok teljesítményfejlesztéséről nyújt tájékoztatást.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269793"
---
# <a name="project-invoice-proposal-performance"></a>Projektszámla-javaslatok teljesítménye

[!include [banner](../includes/banner.md)]

Új számlajavaslat létrehozásakor a projektek és alprojektek számának növekedésével teljesítményproblémák merülhetnek fel. A teljesítmény javítása érdekében rendelkezésre áll egy funkció, amely csökkenti a könyvelt projekttranzakciókra vonatkozó új számlajavaslat létrehozásához szükséges időt.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Projektszámla-javaslatok teljesítményjavításának engedélyezése
A projektszámla-javaslat teljesítményjavítási funkció engedélyezéséhez végezze el az alábbi lépéseket.

1.  Menjen a **Funkciókezelés** > **Összes** lehetőségre. A szolgáltatáslistában keresse meg a **Projektszámla-javaslatok teljesítményjavítása** lehetőséget.
2.  Válassza ki az **Engedélyezés most** lehetőséget.
3.  Frissítse böngészőjét, majd hozzon létre egy új számlajavaslatot.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Projektszámla-javaslatok teljesítményjavításának kikapcsolása
A projektszámla-javaslat teljesítményjavítási funkció kikapcsolásához végezze el az alábbi lépéseket.

1.  Menjen a **Funkciókezelés** > **Összes** lehetőségre. A szolgáltatáslistában keresse meg a **Projektszámla-javaslatok teljesítményjavítása** lehetőséget.
2.  Válassza ki a **Letiltás** lehetőséget.
3.  Frissítse a böngészőjét.

> [!NOTE]
> A számlajavaslat teljesítménye nem alkalmazható a számlázási szabályok engedélyezésekor.
> 
> A számlajavaslatok léterhozásának folyamata során az alfeladatok száma a számlázható tranzakciókkal rendelkező szerződések számától függően maximális számra osztja fel a feladatokat, függetlenül attól, hogy mit adott meg. Ha például **3**-as számot adja meg a számlajavaslat kötegben való létrehozásához szükséges alfeladatokhoz, és csak két olyan szerződés van, amely számlázható tranzakciókat tartalmaz, csak két alfeladat jön létre.
