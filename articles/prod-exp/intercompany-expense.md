---
title: Vállalatközi költségek
description: A szervezet egyik jogi személye által alkalmazott munkavállaló végezhet munkát egy másik, ugyanabban a szervezetben lévő jogi entitásnál. Ebben az esetben a vállalatközi költség funkciót használhatja a munkavállalói kiadások ahhoz a jogi entitáshoz való hozzárendeléséhez, amelynél a munkát végezték.
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078243"
---
# <a name="intercompany-expenses"></a>Vállalatközi költségek

[!include [banner](../includes/banner.md)]

A szervezet egyik jogi személye által alkalmazott munkavállaló végezhet munkát egy másik, ugyanabban a szervezetben lévő jogi entitásnál. Ebben az esetben a vállalatközi költség funkciót használhatja a munkavállalói kiadások ahhoz a jogi entitáshoz való hozzárendeléséhez, amelynél a munkát végezték. A munkavállalót foglalkoztató jogi személy az úgynevezett kölcsönadó jogi entitás. Az a jogi személy, amelyhez a munkavállaló a költségeket generálja a kölcsönbevevő jogi személy. 

Mielőtt a dolgozó a másik jogi személy számára végzett munkára vonatkozóan költségeket hozzon létre és nyújtson be, a kölcsönadó jogi személynél a **Költség-kezelési paraméterek** lapon jelölje be a **Vállalatközi kiadási sorok engedélyezése** jelölőnégyzetet. 

## <a name="tax-posting-for-intercompany-expenses"></a>Vállalatközi kiadások adójának feladása

[!include [banner](../includes/banner.md)]

Ha a kölcsönadó (forrás) jogi személyhez tartozó adócsoportokat kívánja használni a kölcsönbevevő (cél) jogi személy helyett, akkor ezt a főkönyvben kell beállítania. Ha a **Vállalatközi adófeladás jogi személye** Főkönyvi paraméter beállítás **Forrás** és **Az ÁFA-adózási szabályok alkalmazása** értéke **Nem** a kölcsönadó jogi személyhez tartozó adózási kombinációt használja a rendszer. Ha ugyanazt a paramétert a **Cél** értékre állítja , a rendszer a kölcsönvevő jogi személyhez tartozó adózási kombinációt használja. Az Egyesült államokbeli jogi entitások esetében, ha a paraméter beállítása **Forrás** , a rendszernek az **ÁFA-kinnlévőség** mezőt is be kell állítania az új **Főkönyvi feladási csoportok** lapon. A könyvelési motor az ebből a mezőből származó információkat az adózáshoz kapcsolódó könyvelési bejegyzéshez használja.   
A viselkedés összhangban van a projekttel vagy anélkül feladott költségelszámolási sorokkal.  
