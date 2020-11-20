---
title: Egységek és egységcsoportok
description: Ez a témakör a Dynamics 365 Project Operations egységeinek és egységcsoportjainak létrehozásáról nyújt információkat.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 3f588e41d001befeac87bb6a4e28a83cf5cfa865
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131031"
---
# <a name="units-and-unit-groups"></a>Egységek és egységcsoportok

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az egység az a mennyiség vagy mértékegység, amiben a terméket vagy szolgáltatásokat értékesíti. Például a kertészeti készletek eladása esetén előfordulhat, hogy vetőmagot csomag, doboz és raklap egységben értékesíti. Az egységcsoport ezen különböző kiszerelések gyűjteménye.

A témakör lépéseinek végrehajtásához rendszergazdai, Sales Professional menedzseri vagy ezzel egyenértékű jogosultsággal kell rendelkezni.

## <a name="create-a-unit-group"></a>Egységcsoport létrehozása

1. Az Oldaltérképen válassza az **Egységek** lehetőséget.
2. Válassza az **Új** lehetőséget, és az **Egységcsoport létrehozása** párbeszédpanelen adja meg az egység nevét.
3. Az **Eelsődleges egység** mezőbe írja be azt a legkisebb közös mértékegységet, amelyben a terméket forgalmazni fogják. Megadhatja például a „darab” vagy az „uncia” értéket.
4. Kattintson az **OK** gombra.

## <a name="add-units-to-a-unit-group"></a>Egységek hozzáadása egységcsoportokhoz

1. Nyisson meg egy egységcsoportot, és a **Kapcsolódó** lapon válassza az **Egységek** lehetőséget. Látni fogja, hogy az elsődleges egység már szerepel.
2. Válassza az **Új egység hozzáadása** lehetőséget, majd az **Árlistaelem gyors létrehozása** oldal **Név** mezőjében adja meg az egység nevét.
3. A **Mennyiség** mezőben adja meg azt a mennyiséget, amelyet az egység tartalmazni fog. Ha egy doboz például két darabot tartalmaz, akkor a „2” értéket írja be. 
4. Az **Alapegység** mezőben válasszon egy alapegységet, az egység legkisebb mértékegységének megadásához. Megadhatja például a „Darab” lehetőséget.
5. Válassza a **Mentés** lehetőséget.
