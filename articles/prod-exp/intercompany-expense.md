---
title: Vállalatközi költségek
description: Ez témakör tájékoztatást nyújt arról, hogyan lehet a vállalatközi kiadások használatával a dolgozók kiadásait ahhoz a jogi entitáshoz hozzárendelni, amelynél a munkát végrehajtották.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271536"
---
# <a name="intercompany-expenses"></a>Vállalatközi költségek

A szervezet egyik jogi személye által alkalmazott munkavállaló végezhet munkát egy másik, ugyanabban a szervezetben lévő jogi entitásnál. A vállalatközi kiadások használatával a dolgozók kiadásait ahhoz a jogi entitáshoz tudja hozzárendelni, amelynél a munkát végrehajtották. A munkavállalót foglalkoztató jogi személy az úgynevezett kölcsönadó jogi entitás. Az a jogi személy, amelyhez a munkavállaló a költségeket generálja a kölcsönbevevő jogi személy. 

Ahhoz, hogy egy dolgozó létrehozza és elküldje a vállalatközi költségeket, engedélyeznie kell a vállalatközi költségsorokat. A kölcsönadó jogi entitás **Költségkezelési paraméterek** lapján válassza a **Vállalatközi költségsorok engedélyezése** lehetőséget. 

## <a name="tax-posting-for-intercompany-expenses"></a>Vállalatközi kiadások adójának feladása

[!include [banner](../includes/banner.md)]

Ahhoz, hogy a költségjelentésben a kölcsönkérő (cél) jogi entitás helyett a kölcsönadóhoz (forrás) tartozó adócsoportokat használjon, engedélyeznie kell a funkciót a Főkönyvi áfa beállításban. Ha a **Vállalatközi jogi entitás adójának feladása** paraméter **Forrás** lehetőségre van állítva, és az **Áfa adózási szabályok alkalmazása** beállítás **Nem** értékre van állítva, a kölcsönadó entitás adókombinációját használja a rendszer. Ha ugyanazt a paramétert a **Cél** értékre állítja , a rendszer a kölcsönvevő jogi személyhez tartozó adózási kombinációt használja. Az Egyesült államokbeli jogi entitások esetében, ha a paraméter beállítása **Forrás**, a rendszernek az **ÁFA-kinnlévőség** mezőt is be kell állítania az új **Főkönyvi feladási csoportok** lapon. A könyvelési motor az ebből a mezőből származó információkat az adózáshoz kapcsolódó könyvelési bejegyzéshez használja.   
A viselkedés összhangban van a projekttel vagy anélkül feladott költségelszámolási sorokkal.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]