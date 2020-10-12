---
title: Befejezéskori költség becslésének frissítése
description: Ez a témakör a projektráfordítások leképezésének frissítéséről nyújt információt.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
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
ms.openlocfilehash: 42824cc4cfc2b934f69d319944fe7ee43183955c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897769"
---
# <a name="update-estimate-at-completion"></a>Befejezéskori költség becslésének frissítése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Általában a projektmenedzser felülvizsgálja a feladat eredeti becsléseit. A projekt újratervezése a projekt menedzserének a becslésről alkotott felfogása, a projekt jelenlegi helyzetére tekintettel. Nem javasoljuk azonban, hogy a projektvezetők megváltoztassák az alapszintet, mivel a projekt alapvonala a megállapított igazságforrást képviseli a projekt ütemterve és költségbecslése szempontjából, és a projekt összes érdekeltje egyetértett azzal.

Kétféle módon tudja egy projektmenedzser újraprogramozni a feladatokat:

- Felülbírálja a befejezésre vonatkozó becslés alapértelmezett értékét a feladattal kapcsolatos tényleges hátralévő erőfeszítések becslésével. 
- A feladat valódi előrehaladásának új becslésével felülbírálja az alapértelmezett haladási százalékot.

Ezeknek a megközelítéseknek a segítségével át kell számítani a feladat ETC-jét, a befejezéskori költség becslését és az előrehaladási százalékot, valamint a feladatra várható erőfeszítési varianciát. Az EAC, az ETC-t és az összefoglaló feladatok előrehaladási százalékát újraszámolja, és új leképezést ad az erőfeszítés varianciájára.