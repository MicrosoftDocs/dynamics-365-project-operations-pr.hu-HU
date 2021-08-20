---
title: Vállalatközi költségek
description: Ez témakör tájékoztatást nyújt arról, hogyan lehet a vállalatközi kiadások használatával a dolgozók kiadásait ahhoz a jogi entitáshoz hozzárendelni, amelynél a munkát végrehajtották.
author: Surya Vaidyanathan
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ef42bf5274ff9a5c50e6dcb93995cfbbda40a66d7471f29ebf056086320640
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001209"
---
# <a name="intercompany-expenses"></a>Vállalatközi költségek

A szervezet egyik jogi személye által alkalmazott munkavállaló végezhet munkát egy másik, ugyanabban a szervezetben lévő jogi entitásnál. A vállalatközi kiadások használatával a dolgozók kiadásait ahhoz a jogi entitáshoz tudja hozzárendelni, amelynél a munkát végrehajtották. A munkavállalót foglalkoztató jogi személy az úgynevezett kölcsönadó jogi entitás. Az a jogi személy, amelyhez a munkavállaló a költségeket generálja a kölcsönbevevő jogi személy. 

Ahhoz, hogy egy dolgozó létrehozza és elküldje a vállalatközi költségeket, engedélyeznie kell a vállalatközi költségsorokat. A kölcsönadó jogi entitás **Költségkezelési paraméterek** lapján válassza a **Vállalatközi költségsorok engedélyezése** lehetőséget. 

## <a name="tax-posting-for-intercompany-expenses"></a>Vállalatközi kiadások adójának feladása

[!include [banner](../includes/banner.md)]

Ahhoz, hogy a költségjelentésben a kölcsönkérő (cél) jogi entitás helyett a kölcsönadóhoz (forrás) tartozó adócsoportokat használjon, engedélyeznie kell a funkciót a Főkönyvi áfa beállításban. Ha a **Vállalatközi jogi entitás adójának feladása** paraméter **Forrás** lehetőségre van állítva, és az **Áfa adózási szabályok alkalmazása** beállítás **Nem** értékre van állítva, a kölcsönadó entitás adókombinációját használja a rendszer. Ha ugyanazt a paramétert a **Cél** értékre állítja , a rendszer a kölcsönvevő jogi személyhez tartozó adózási kombinációt használja. Az Egyesült államokbeli jogi entitások esetében, ha a paraméter beállítása **Forrás**, a rendszernek az **ÁFA-kinnlévőség** mezőt is be kell állítania az új **Főkönyvi feladási csoportok** lapon. A könyvelési motor az ebből a mezőből származó információkat az adózáshoz kapcsolódó könyvelési bejegyzéshez használja.   
A viselkedés összhangban van a projekttel vagy anélkül feladott költségelszámolási sorokkal.  

## <a name="new-expense-expression-builder"></a>Új költségkifejezés-szerkesztő

Az új költségkifejezés-szerkesztő a projekteket használó, vállalatközi költségforgatókönyvekkel kapcsolatos problémákat foglalkozik. Ez a szolgáltatás biztosítja, hogy egy vállalatközi költség létrehozásakor a költség-irányelv helyesen legyen ellenőrizve a költségvonalon kiválasztott projekt alapján, és hogy a költségjelentés sikeresen elküldhető legyen.

A költségkifejezés-szerkesztő funkció csak akkor használható, ha be van kapcsolva. Emellett be kell állítani a projektazonosítóval is kapcsolatos költség-irányelvet.

Ha már konfigurált olyan irányelveket, amelyek a költségsoron ellenőrzik a projektazonosítót, azokat ki kell vezetnie. Ezután bekapcsolhatja a szolgáltatást, és átkonfigurálhatja a szabályzatokat.

A funkció bekapcsolásához kövesse az alábbi lépéseket.

1. Válassza a **Munkaterületek** \> **Szolgáltatáskezelés** lehetőséget.
2. A listában válassza az **Új költségkifejezés-szerkesztő kezelje a problémákat, amikor a vállalatközi költségfogatókönyvek projekteteket használnak**. Ezután válassza az **Engedélyezés most** lehetőséget.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
