---
title: Egységek és egységcsoportok
description: Ez a cikk arról nyújt tájékoztatást, hogyan hozhat létre egységeket és egységcsoportokat a Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a46b7d182d3d7fc77c1275c108f5dc569ffebff1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921443"
---
# <a name="units-and-unit-groups"></a>Egységek és egységcsoportok

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az egység az a mennyiség vagy mértékegység, amiben a terméket vagy szolgáltatásokat értékesíti. Például a kertészeti készletek eladása esetén előfordulhat, hogy vetőmagot csomag, doboz és raklap egységben értékesíti. Az egységcsoport ezen különböző kiszerelések gyűjteménye.

A cikkben található lépések végrehajtásához győződjön meg arról, hogy rendszergazdai vagy értékesítési szakmai vezetői szerepkörhöz van rendelve, vagy ezzel egyenértékű engedélyekkel rendelkezik.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]