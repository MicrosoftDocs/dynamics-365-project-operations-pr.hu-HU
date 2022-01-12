---
title: Költség részletezése
description: Ez a témakör ismerteti, hogyan lehet részletezni a költségeket az újragondolt Költség munkaterület használatával.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: b2077b77af036ce64aad203f52b03cacca8c4099
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944151"
---
# <a name="expense-itemization"></a>Költség részletezése

[!include [banner](../includes/banner.md)]

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A szervezetek gyakran megkövetelik az alkalmazottaktól, hogy részletes bontásban adják meg az utazás során felmerült költségeket. Például egy szállodai fólió több tételes sort is tartalmazhat a szobaár, az adó, a parkolás és egyéb egyéb költségek ésére, amelyek minden nap felmerülnek a tartózkodás időtartama alatt. Vagy az étkezési költség megkövetelheti, hogy részletesebb bontást adjon meg reggelire, ebédre vagy vacsorára. Függetlenül a szervezet igényeitől, az egyes költségkategóriák beállíthatók úgy, hogy tükrözzék a költségeket tartalmazó alkategóriákat vagy sorcikkeket. Míg a részletezés mindig támogatott a **Költségkezelésben,** az **Újragondolt költség** munkaterület hatékonyabb részletezást tesz lehetővé, ha a funkció, **az ismétlődő költségek gyors részletezésének képessége** engedélyezve van.  

## <a name="enable-quick-itemization"></a>Gyors részletezés engedélyezése 

Az ismétlődő **költségek gyors részletezésének képességével** gyorsan részletezheti az ismétlődő költségeket, elkerülve ugyanakkor a napi költségek megadásának szükségességét minden alkalommal a tartózkodás időtartama alatt. A gyors részletezés engedélyezéséhez hajtsa végre az alábbi lépéseket.

1. Lépjen a **Funkciókezelés** munkaterületre, és a funkciók listájában keresse meg és válassza a **Költségjelentések újragondolása** lehetőséget. 
2. Válassza ki az **Engedélyezés most** lehetőséget. 
3. A szolgáltatáslistában keresse meg és válassza az **Ismétlődő költségek gyors részletezésének lehetősége** lehetőséget.
4. Válassza ki az **Engedélyezés most** lehetőséget. 

## <a name="itemization-grid"></a>Elemi rács 

Ha egy költségkategóriának alkategóriái vagy különböző összetevői alkotják ezt a költséget, akkor tételessé teheti. Költség részletezéséhez jelölje ki a költségsort a költségjelentésben, a **Költség részletei** ablaktáblán pedig válassza a Műveletek **tétele** > **lehetőséget**. A **Elemezés** csúszka mezőkkel rendelkező rácsot mutat be. Az alábbi táblázat a rács minden mezőjére és a mező költségjelentésben való megjelenítésének módjára mutat példát. 

|     Mező          |     Description                                                                                  |     Példa              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Alkategória    |     A költségkategória típusa, Hotel alatt konfigurált alkategóriák **listája**.             |     Napi szobaár      |
|     Kezdési dátum     |     A költségtétel első felmerülésének dátuma.                                           |     09/13/2021           |
|     Napi árfolyam     |     A költségtételhez felmerült összeg.                                                    |     200                  |
|     Mennyiség       |     Az, hogy a töltés hányszor ismétlődik meg egy folyamatos időszakban.                       |     3                    |

![A költségek tétele.](media/Itemization%20screen%201.png)

Cikk mentésekor a Cikkessé tétel rácsban megadott mennyiséghez egy adott tételes sort fog látni. Minden sor a rácsban megadott dátumon kezdődik.

![Tételes jelentés.](media/Itemization%20screen%202.png)

