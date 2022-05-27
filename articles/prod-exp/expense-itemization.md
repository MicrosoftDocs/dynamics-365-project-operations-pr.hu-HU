---
title: Költségrészletezés
description: Ez a témakör bemutatja, hogyan részletezheti a költségeket az újragondolt Költség-munkaterület használatával.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 34b11c6bd8be729957973a60fccccc2dd32c2669
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574525"
---
# <a name="expense-itemization"></a>Költségrészletezés

[!include [banner](../includes/banner.md)]

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A szervezetek gyakran megkövetelik az alkalmazottaktól, hogy részletes bontásban számolják el az utazás során felmerült költségeket. Például egy szállodai fólió több tételes sort tartalmazhat a szobaárra, az adóra, a parkolásra és a tartózkodás időtartama alatt minden nap felmerülő egyéb költségekre vonatkozóan. Vagy az étkezési költség megkövetelheti, hogy részletesebb bontást biztosítson reggelire, ebédre vagy vacsorára. A szervezet igényeitől függetlenül minden költségkategória beállítható úgy, hogy tükrözze az alkategóriákat vagy a költségeket alkotó sorcikkeket. Bár a cikkezés mindig is támogatott a **Költségkezelésben**, az **újragondolt költség-munkaterület** hatékonyabb részletezést tesz lehetővé, **ha engedélyezve van az ismétlődő költségek gyors** részletezésének képessége funkció.  

## <a name="enable-quick-itemization"></a>Gyorstétel engedélyezése 

Az ismétlődő költségek részletezésének képessége gyorsan **részletezheti az** ismétlődő költségeket, miközben elkerülheti, hogy a tartózkodás időtartama alatt minden alkalommal meg kelljen adnia a napi költségeket. A gyors részletezés engedélyezéséhez hajtsa végre az alábbi lépéseket.

1. Nyissa meg a **Szolgáltatáskezelés** munkaterületet, és a szolgáltatások listájában keresse meg és válassza ki az **újragondolt** költségjelentések lehetőséget. 
2. Válassza ki az **Engedélyezés most** lehetőséget. 
3. A szolgáltatáslistában keresse meg és válassza ki az **ismétlődő költségek gyors** részletezésének lehetősége lehetőséget.
4. Válassza ki az **Engedélyezés most** lehetőséget. 

## <a name="itemization-grid"></a>Cikkezési rács 

Ha egy költségkategória alkategóriákkal vagy különböző összetevőkkel rendelkezik, amelyek ezt a költséget alkotják, akkor részletezhető. Költség részletezéséhez válassza ki a költségsort a költségjelentésben, majd a Költség részletei **ablaktáblán válassza a** Műveletek **részletezése** > **lehetőséget**. A **Itemization** csúszka mezőket tartalmazó rácsot jelenít meg. Az alábbi táblázat példákat mutat be a rács minden mezőjére és arra, hogy a mező hogyan jelenik meg a költségjelentésben. 

|     Mező          |     Description                                                                                  |     Példa              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Alkategória    |     A Költségkategória típusa (**Hotel**) alatt konfigurált alkategóriák listája.             |     Napi szobaár      |
|     Kezdési dátum     |     A költségtétel első felmerülésének dátuma.                                           |     09/13/2021           |
|     Napidíj     |     A költségtételhez felmerült összeg.                                                    |     200                  |
|     Mennyiség       |     A töltés ismétlődésének száma egy folyamatos időszakban.                       |     3                    |

![Részletezze a költségeket.](media/Itemization%20screen%201.png)

Cikktétel mentésekor a Cikkszámolás rácsban megadott mennyiséghez egy egyedi tételes sor jelenik meg. Minden sor a rácsban megadott dátummal kezdődik.

![Tételes jelentés.](media/Itemization%20screen%202.png)

