---
title: Költségrészletezés
description: Ez a cikk azt ismerteti, hogyan részletezheti a költségeket az újragondolt Költség munkaterület használatával.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 71bfbe83259804fc0b0355c81d430805da23dd45
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920937"
---
# <a name="expense-itemization"></a>Költségrészletezés

[!include [banner](../includes/banner.md)]

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A szervezetek gyakran megkövetelik az alkalmazottaktól, hogy részletes bontást adjanak az utazás során felmerült költségekről. Például egy szállodai fólió több tételes sort is tartalmazhat a szobaár, az adó, a parkolás és egyéb egyéb költségek tekintetében, amelyek naponta felmerülnek a tartózkodás időtartama alatt. Vagy egy étkezési költség megkövetelheti, hogy részletesebb bontást biztosítson reggelire, ebédre vagy vacsorára. Bármi legyen is a szervezet igényei, minden költségkategória beállítható úgy, hogy tükrözze a költséget alkotó alkategóriákat vagy sorokat. Bár a tételesítés mindig is támogatott volt a **Költségkezelésben**, az **Újragondolt költség** munkaterület hatékonyabb tételes megjelenítést tesz lehetővé, **ha az ismétlődő költségek gyors** tételes képessége funkció engedélyezve van.  

## <a name="enable-quick-itemization"></a>Gyors elemezés engedélyezése 

Használhatja az **Ismétlődő költségek tétele funkcióval gyorsan** tételesen tételesen, miközben elkerülheti, hogy a tartózkodás időtartamára minden alkalommal meg kelljen adnia a napi költségeket. A gyors elemezés engedélyezéséhez hajtsa végre a következő lépéseket.

1. Lépjen a **Funkciókezelés** munkaterületre, és a funkciók listájában keresse meg és válassza ki a **Költségjelentések újragondolása lehetőséget**. 
2. Válassza ki az **Engedélyezés most** lehetőséget. 
3. A funkciólistában keresse meg és válassza ki az **Ismétlődő költségek tételes lehetőség gyors** tételét.
4. Válassza ki az **Engedélyezés most** lehetőséget. 

## <a name="itemization-grid"></a>Tételenkénti rács 

Ha egy költségkategóriának vannak alkategóriái vagy különböző összetevői, amelyek a ráfordítást alkotják, akkor tételes lehet. Egy költség tételesítéséhez válassza ki a költségsort a költségjelentésben, majd a Költség részletei ablaktáblán válassza a **Műveletek tételesítése** **lehetőséget** > **.** Az **Elemi csúszka** egy mezőket tartalmazó rácsot jelenít meg. Az alábbi táblázat egy példát mutat be a rács egyes mezőire, valamint arra, hogy a mező hogyan jelenik meg a költségjelentésben. 

|     Mező          |     Description                                                                                  |     Példa              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Alkategória    |     A Hotel **költségkategória-típus** alatt konfigurált alkategóriák listája.             |     Napi szobaár      |
|     Kezdési dátum     |     A költségtétel első felmerülésének dátuma.                                           |     09/13/2021           |
|     Napi árfolyam     |     A költségtételnél felmerült összeg.                                                    |     200                  |
|     Mennyiség       |     Azon alkalmak száma, amikor a töltés egy folyamatos időszak alatt megismétlődik.                       |     3                    |

![Tételes költség.](media/Itemization%20screen%201.png)

Elemi megjelenítés mentésekor egy egyedi tételes sort fog látni az Itemization rácsban megadott mennyiséghez. Minden sor a rácsban megadott dátummal kezdődik.

![Tételes jelentés.](media/Itemization%20screen%202.png)

