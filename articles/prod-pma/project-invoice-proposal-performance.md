---
title: Projektszámla-javaslatok teljesítménye
description: Ez cikk a projektszámla-javaslatok teljesítményfejlesztéséről nyújt tájékoztatást.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 70069778b7d4326cb23d6bb36e2c78a33da12573
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927193"
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
