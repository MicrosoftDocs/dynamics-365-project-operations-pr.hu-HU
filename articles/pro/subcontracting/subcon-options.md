---
title: Alvállalkozói lehetőségek projektcsoporttagok számára
description: Ez a cikk a Microsoft projektcsapat-tagjainak alvállalkozói lehetőségeit ismerteti Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 88a76ccf73a4b6cfa13a67b50130b007f244d831
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919787"
---
# <a name="subcontracting-options-for-project-team-members"></a>Alvállalkozói lehetőségek projektcsoporttagok számára

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoftban Dynamics 365 Project Operations kiértékelheti az egy vagy több projektcsapattag számára elérhető alvállalkozói lehetőségeket. A rendelkezésre álló alvállalkozói lehetőségek a következőket teszik lehetővé:

- Hozzon létre egy új alvállalkozói szerződést és/vagy hozzon létre új sorokat egy meglévő alvállalkozói szerződéshez a kiválasztott projektcsapat tagjai számára. 
- Tartalék egy már meglévő alvállalkozói és alvállalkozói vonallal szemben. 

Választhat az általános projektcsapatok számára elérhető alvállalkozói lehetőségek közül, vagy választhat a projektcsapat azon tagjai közül, akik olyan megnevezett erőforrással rendelkeznek, amely szerződéses dolgozó. 

A következőkre vonatkozóan nem állnak rendelkezésre alvállalkozói lehetőségek:

- A projektcsapat tagjai, akik egy alkalmazottal dolgoztak. 
- A projektcsapat tagjai, akik már társítva vannak egy alvállalkozói és alvállalkozói vonallal. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>A projektcsapat személyzettel nem rendelkező tagjának alvállalkozásba adása

Egy általános vagy személyzet nélküli projektcsapattag számára elérhető alvállalkozói lehetőségek áttekintéséhez és kiválasztásához kövesse az alábbi lépéseket:

1. Válasszon ki egy vagy több projektcsapat-tagrekordot, ahol az erőforrás egy általános erőforrás.
2. Győződjön meg arról, hogy a kiválasztott projektcsapattag-rekordok egyike sem alvállalkozásba van adva. 
3. Válassza az **Alvállalkozási beállítások lehetőséget** a projektcsapat tagjainak alrácsán. **Megnyílik az Alvállalkozási beállítások** párbeszédpanel. 
4. Ha csak egy projektcsapat-tagrekordot választott ki az 1. lépésben, akkor a következő lehetőségek lesznek elérhetők:
    - Hozzon létre új alvállalkozói sorokat. 
    - Tartalék egy meglévő alvállalkozói szerződés ellen: Ha az 1. lépésben több projektcsapat-tagrekordot választott ki, akkor az egyetlen rendelkezésre álló lehetőség egy új alvállalkozói sorok létrehozása.
5. A meglévő alvállalkozói sorra való tartalékolási lehetőség lehetővé teszi, hogy kiválasszon egy alvállalkozói és alvállalkozói sort, amely számára tartalékot szeretne képezni. Amikor alvállalkozói sort választ ki a kapacitás lefoglalásához, győződjön meg arról, hogy a kiválasztott alvállalkozói sor időhöz kötött, és hogy a projektcsapat tagjánál szükséges szerepkör megegyezik az alvállalkozói sorban megvásárolt szerepkörrel.
6. Ha úgy dönt, hogy új alvállalkozói sorokat hoz létre a projektcsapat tagjai számára, a rendszer lehetővé teszi, hogy kiválassza azt az alvállalkozói szerződést, amelyet létre szeretne hozni ezekhez a sorokhoz. Az alvállalkozói szerződésnek, amelyben új sorokat szeretne létrehozni, Vázlat **állapotban kell lennie**. Ezzel a lehetőséggel új alvállalkozói sorokat hozhat létre a kiválasztott projektcsapat tagjai számára, a rendszer egy alvállalkozói sort hoz létre az egyes projektcsapat-tagok számára. A rendszer átmásolja a szerepkört, az órákat és a dátumokat a projektcsapat tagjából az egyes létrehozott alvállalkozói sorokba. 
7. Ha egy általános csapattag alvállalkozói és alvállalkozói sorhoz van társítva, az **általános csapattag sor Dolgozó típusa** mezője Szerződés-feldolgozóra **·**, az **Alvállalkozói érvényesség** értéke pedig Érvényes **értékre** lesz állítva.

## <a name="subcontracting-a-staffed-project-team-member"></a>A projektcsapat személyzettel rendelkező tagjának alvállalkozásba adása

Az általános vagy személyzet nélküli csapattagokhoz hasonlóan a személyzettel rendelkező projektcsapattag alvállalkozói lehetőségeit is megtekintheti, ha a személyzettel rendelkező csapattag szerződéses alkalmazott. Ha át szeretné tekinteni és ki szeretne választani egy alkalmazott vagy megnevezett projektcsapattag számára elérhető alvállalkozói lehetőségek közül, kövesse az alábbi lépéseket:

1. Válasszon ki egy vagy több projektcsapat-tagrekordot, ahol az erőforrás egy megnevezett szerződéses dolgozó.
2. Győződjön meg arról, hogy a kiválasztott projektcsapattag-rekordok egyike sem alvállalkozásba van adva. 
3. Válassza az **Alvállalkozási beállítások lehetőséget** a projektcsapat tagjainak alrácsán. **Megnyílik az Alvállalkozási beállítások** párbeszédpanel. 
4. Ha csak egy projektcsapat-tagrekordot választott ki az 1. lépésben, akkor a következő lehetőségek lesznek elérhetők:
      - Hozzon létre új alvállalkozói sorokat.
      - Tartalék meglévő alvállalkozói szerződés ellenében.
  Ha az 1. lépésben több projektcsapattag-rekordot választott ki, akkor az egyetlen elérhető lehetőség egy új alvállalkozói sorok létrehozása.
5. A meglévő alvállalkozói sorra való tartalékolási lehetőség lehetővé teszi, hogy kiválasszon egy alvállalkozói és alvállalkozói sort, amely számára tartalékot szeretne képezni. Amikor alvállalkozói sort választ a kapacitás lefoglalásához, győződjön meg a következőkről:
      - A kiválasztott alvállalkozói sor az időre vonatkozik. 
      - A projektcsapat tagjánál szükséges szerepkör megegyezik az alvállalkozói vonalon megvásárolt szerepkörrel. 
      - A szállító, amelyhez a szerződéses dolgozó társítva van, megegyezik az alvállalkozói szerződésben szereplő szállítóval.
6. Ha úgy dönt, hogy új alvállalkozói sorokat hoz létre a projektcsapat tagjai számára, a rendszer lehetővé teszi, hogy kiválassza azt az alvállalkozói szerződést, amelyet létre szeretne hozni ezekhez a sorokhoz. Ezzel a beállítással meg kell győződnie arról, hogy az a szállító, amelyhez a szerződéses dolgozó tartozik, megegyezik az alvállalkozói szerződés szállítójával. 
7. Az alvállalkozói szerződésnek, amelyben új sorokat szeretne létrehozni, Vázlat **állapotban kell lennie**. Ezzel a lehetőséggel új alvállalkozói sorokat hozhat létre a kiválasztott projektcsapat tagjai számára, a rendszer egy alvállalkozói sort hoz létre az egyes projektcsapat-tagok számára. A rendszer átmásolja a szerepkört, az órákat és a dátumokat a projektcsapat tagjából az egyes létrehozott alvállalkozói sorokba.  
8. Ha egy megnevezett csapattag alvállalkozói és alvállalkozói sorhoz van társítva, a **megnevezett csapattag sor Dolgozó típusa** mezője Szerződés-feldolgozóra **·**, az **Alvállalkozói érvényesség** értéke pedig Érvényes **értékre** lesz állítva.

## <a name="re-costing-subcontractor-assignments"></a>Alvállalkozói megbízások újraköltségszámítása

Ha egy projektcsapattag (általános vagy elnevezett) alvállalkozói sorokhoz van csatolva az **Alvállalkozói beállítások** párbeszédpanelen, a csapattag feladataihoz rendelt hozzárendelések újraköltséget kapnak az alvállalkozói szerződéshez csatolt beszerzési árlista alapján. **A Projekt részletei** lap Becslések **lapján** válassza az Árak **frissítése gombot az** alvállalkozói szerződésről szóló döntésből eredő frissített árképzés és/vagy költségszámítás megtekintéséhez.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
