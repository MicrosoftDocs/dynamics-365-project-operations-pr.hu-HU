---
title: Az alvállalkozók erőforrás-hozzárendelései költségeinek becslése
description: Ez a cikk ismerteti, hogyan számítja ki a Microsoft Dynamics 365 Project Operations alvállalkozók erőforrás-hozzárendelésének költségbecslését.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9fded1baa63d2defc134994c858dfc6c09f75082
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522657"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Az alvállalkozók erőforrás-hozzárendelései költségeinek becslése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az alvállalkozói projektcsoport tagjainak feladat-hozzárendelésének költségelése a kapcsolódó csoporttag-rekord alvállalkozói szerződéséhez csatolt **Beszerzési** árlista alapján történik. Ez eltér attól, ahogyan az alkalmazotti erőforrás-hozzárendelések költségelése történik, ahol a munkavállalói erőforrások feladat-hozzárendeléseinek költségelése a projekt szerződő egységének **Költség** árlistájával történik. 

Azon általános projektcsoport-tagok számára, akik alvállalkozók, megbízások költségelése egy szerepkörár alapú beállítással történik az alvállakozói szerződéshez csatolt beszerzési árlistában. A beszerzési árak specifikusan is beállíthatók az egyes erőforrásokhoz. Ezek az erőforrás-specifikus árak akkor kapnak prioritást, ha a megnevezett projektcsapattagok költségelési feladathozzárendelései szerződéses dolgozók. 

A szerepkör-specifikus beszerzési ár és az erőforrás-specifikus használat prioritását **Paraméterek > Mennyiségalapú árdimenziók** árdimenzió prioritás beállítása szabályozza.

Ez az árak dinamikus származtatása funkció az alvállalkozók beszerzési árainak dimenzióbeállításán alapul, hasonló ahhoz, ahogy a költség és számlázott díjak vannak származtatva a teljes munkaidős alkalmazottakhoz. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Feladat-hozzárendelések létrehozása az alvállalkozói erőforrások költségbecslésének készítéséhez

Az alvállalkozókhoz kétféleképpen lehet feladat-hozzárendelést létrehozni: 
- A **Feladatok** fül használatával.
- A **Csoport** fül használatával.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Erőforrás-hozzárendelések létrehozása a Feladatok lapon
Egy adott feladathoz a **Feladatok** lap **Erőforrások** listájának használatával feladat-hozzárendelést hozhat létre egy elnevezett erőforráshoz vagy általános erőforráshoz. Ha a feladathoz tartozó **Hozzárendelt erőforrások** legördülő menüből választ egy elnevezett erőforrást, és ez az erőforrás egy szerződés dolgozó, akkor a elnevezett erőforrás a feladathoz hozzá lesz rendelve, és a projektcsoport megfelelő tagjának rekordja úgy jön létre, hogy a dolgozó típusa **Szerződés dolgozó** és az **Érvényesség** értéke **Érvénytelen**. Következő lépésként meg kell nyitnia a projektcsoport tagjának rekordját, és ki kell választania egy alvállalkozót és alvállalkozói sort. Ez frissíti a feladat-hozzárendelést, hogy az hivatkozzon az alvállalkozóra és az alvállalkozói sorra, és a csoporttag állapotát **Érvényes** állapotra frissíti .

Ha úgy dönt, hogy létrehoz egy általános csoporttagot a **Hozzárendelt erőforrások** legördülő menüben a feladaton, akkor az **Általános csoporttagok létrehozása** párbeszédpanelen kijelölhet egy alvállalkozót és egy alvállalkozói sort. Amikor az általános erőforrást a feladathoz rendelik, és létrejön a kapcsolódó projektcsoporttag rekordja, látni fogja, hogy a projektcsoport tagjainak rekordja úgy jön létre, hogy a dolgozó típusa **Szerződéses dolgozó** és az **Érvényesség** beállítása **Érvényes**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Projektcsoport-tagok létrehozása a Csoport lap használatával
A projekt Csoport lapján létrehozhat általános vagy elnevezett csoporttagokat. A csoporttag létrehozásakor kijelölheti az alvállalkozót és az alvállalkozói sort. A csoporttag létrehozása után a **Hozzárendelt erőforrások** legördülő felhasználásával hozzá kell rendelnie a csoporttagot a feladathoz. 

## <a name="updating-estimates"></a>Becslések frissítése
Miután hozzárendelte a projektcsoport tagjait a feladatokhoz, el kell navigálnia a projekt **Becslések** lapjára, és ki kell választania az **Árak frissítése** lehetőséget annak biztosításához, hogy az alvállalkozó erőforrás-hozzárendelések önköltségi rátája az alvállalkozóhoz csatolt beszerzési árlista alapján frissüljön. A Microsoft Dynamics 365 Project Operations nem generál becslést az hozzárendeletlen feladatokhoz. Emiatt létre kell hoznia a feladat-hozzárendelést, hogy a projekt különböző feladatait árazza és költségelje. 

> [MEGJEGYZÉS!] A Projekt csoport olyan tagjai, akiknél a **Dolgozó típusa** beállítása értéke **Szerződéses dolgozó**, de nem rendelkeznek alvállalkozói hivatkozással, **Érvénytelen** értékkel lesznek megjelölve a **Projektcsoporttagok** rácsban. Ha van ezzel az állapottal rendelkező projektcsoporttag, nyissa meg a projektcsoporttag rekordját, és frissítse manuálisan az alvállakozói szerződés és alvállalkozói sor mezőket, hogy a pénzügyi költségbecslés pontosan tükrözze az alvállalkozó költségét a **Becslések** lapon. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
