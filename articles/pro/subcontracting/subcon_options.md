---
title: Alvállalkozói lehetőségek a projektcsapat tagjai számára
description: Ez a témakör ismerteti a projektcsapatok alvállalkozói lehetőségeit a Microsoft programban Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4db283db728b50ccf76eafabfd643313620bbce2
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903034"
---
# <a name="subcontracting-options-for-project-team-members"></a>Alvállalkozói lehetőségek a projektcsapat tagjai számára

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations programban kiértékelheti a projektcsapat egy vagy több tagjának alvállalkozói lehetőségeit. A rendelkezésre álló alvállalkozói lehetőségek lehetővé teszik, hogy:

- Hozzon létre egy új alvállalkozót és/vagy hozzon létre új sorokat egy meglévő alvállalkozón a kiválasztott projektcsapat tagjai számára. 
- Tartalék egy már meglévő alvállalkozói és alvállalkozói vonallal szemben. 

Választhat az általános projektcsapatok számára elérhető alvállalkozói lehetőségek közül, vagy választhat a projektcsapat azon tagjai közül, akik egy megnevezett erőforrással rendelkeznek, amely szerződéses dolgozó. 

A következőkre nem állnak rendelkezésre alvállalkozói lehetőségek:

- A projektcsapat azon tagjai, akik egy alkalmazottal dolgoznak. 
- A projektcsapat azon tagjai, akik már egy alvállalkozói és alvállalkozói vonalhoz kapcsolódnak. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>A projektcsapat egy tagjának alvállalkozásba adása

Ha általános vagy nem személyzettel rendelkező projektcsapat-tag számára elérhető alvállalkozói lehetőségek közül szeretne áttekinteni és választani, kövesse az alábbi lépéseket:

1. Válasszon ki egy vagy több projektcsapattag-rekordot, ahol az erőforrás általános erőforrás.
2. Győződjön meg arról, hogy a kiválasztott projektcsapat-tagok rekordjai közül egyik sem van már alvállalkozói. 
3. Válassza **a** Projektcsapat-tagok alrácsának Alvállalkozói beállítások lehetőséget. **Megnyílik az Alvállalkozói beállítások** párbeszédpanel. 
4. Ha csak egy projektcsapattag-rekordot jelölt ki az 1. lépésben, akkor a következő lehetőségek lesznek elérhetők:
    - Új alvállalkozói vonalak létrehozása. 
    - Tartalék egy meglévő alvállalkozóval szemben Ha az 1. lépésben több projektcsapat-rekordot választott ki, akkor az egyetlen lehetőség egy új alvállalkozói sor létrehozása.
5. A meglévő alvállalkozói vonallal szembeni tartalék lehetőség lehetővé teszi, hogy kiválassza azt az alvállalkozói és alvállalkozói vonalat, amelyre tartalékolni szeretne. A kapacitástartalékoláshoz szükséges alvállalkozói sor kiválasztásakor győződjön meg arról, hogy a kiválasztott alvállalkozói vonal időben van kiválasztva, és hogy a projektcsapat tagjánál szükséges szerepkör megegyezik az alvállalkozói sorban vásárolt szerepkörrel.
6. Amikor úgy dönt, hogy új alvállalkozói sorokat hoz létre a projektcsapat tagjai számára, a rendszer lehetővé teszi a sorok létrehozásához létre kívánt alvállalkozó kiválasztását. Az új sorok létrehozásához kiválasztott alvállalkozóknak Tervezet állapotban kell **lenniük.** Ezzel a lehetőséggel új alvállalkozói sorokat hozhat létre a kiválasztott projektcsapattagok számára, a rendszer egy alvállalkozói vonalat hoz létre az egyes projektcsapat-tagok számára. A szerepkör, az órák és a dátumok a projektcsapat tagjából minden létrehozott alvállalkozói sorba kerülnek. 
7. Ha egy általános csapattag alvállalkozói és alvállalkozói sorhoz van társítva, az **általános csapattagsor Dolgozó típusa** mezője **Szerződés-feldolgozóra frissül, és az** **Alvállalkozói érvényesség** értéke Érvényes értékre lesz állítva. **·**

## <a name="subcontracting-a-staffed-project-team-member"></a>A projektcsapat munkatársának alvállalkozásba adása

Az általános vagy személyzet nélküli csapattagokhoz hasonlóan megtekintheti a személyzettel rendelkező projektcsapat tagjának alvállalkozói lehetőségeit is, mindaddig, amíg a személyzettel rendelkező csapattag szerződéses alkalmazott. Ha át szeretne egy alkalmazott vagy megnevezett projektcsapat-tag számára rendelkezésre álló alvállalkozói lehetőségek közül választani, kövesse az alábbi lépéseket:

1. Válasszon ki egy vagy több projektcsapat-rekordot, ahol az erőforrás megnevezett szerződés-feldolgozó.
2. Győződjön meg arról, hogy a kiválasztott projektcsapattag-rekordok egyike sem van már alvállalkozó. 
3. Válassza **a** Projektcsapat-tagok alrácsának Alvállalkozói beállítások lehetőséget. **Megnyílik az Alvállalkozói beállítások** párbeszédpanel. 
4. Ha csak egy projektcsapattag-rekordot jelölt ki az 1. lépésben, akkor a következő lehetőségek lesznek elérhetők:
      - Új alvállalkozói vonalak létrehozása.
      - Tartalék egy meglévő alvállalkozóval szemben.
  Ha az 1. lépésben több projektcsapattag-rekordot választott ki, akkor az egyetlen elérhető lehetőség egy új alvállalkozói sor létrehozása.
5. A meglévő alvállalkozói vonallal szembeni tartalék lehetőség lehetővé teszi, hogy kiválassza azt az alvállalkozói és alvállalkozói vonalat, amelyre tartalékolni szeretne. A kapacitástartalékoláshoz kiválasztott alvállalkozói vonal kiválasztásakor a következőket kell biztosítania:
      - A kiválasztott alvállalkozói vonal egyelőre tart. 
      - A projektcsapat tagjánál megkövetelt szerepkör megegyezik az alvállalkozói sorban vásárolt szerepkörével. 
      - Az a szállító, akihez a szerződéses feldolgozó társítva van, megegyezik az alvállalkozó szállítójával.
6. Amikor úgy dönt, hogy új alvállalkozói sorokat hoz létre a projektcsapat tagjai számára, a rendszer lehetővé teszi a sorok létrehozásához létre kívánt alvállalkozó kiválasztását. Ezzel a beállítással biztosítania kell, hogy a szerződéses dolgozó szállítója ugyanaz legyen, mint az alvállalkozó szállítója. 
7. Az új sorok létrehozásához kiválasztott alvállalkozóknak Tervezet állapotban kell **lenniük.** Ezzel a lehetőséggel új alvállalkozói sorokat hozhat létre a kiválasztott projektcsapattagok számára, a rendszer egy alvállalkozói vonalat hoz létre az egyes projektcsapat-tagok számára. A szerepkör, az órák és a dátumok a projektcsapat tagjából minden létrehozott alvállalkozói sorba kerülnek.  
8. Ha egy megnevezett csapattag alvállalkozói és alvállalkozói sorhoz van társítva, a **megnevezett csapattagsor Dolgozó típusa** mezője **Szerződés-feldolgozóra frissül, és az** **Alvállalkozói érvényesség** értéke Érvényes értékre lesz állítva. **·**

## <a name="re-costing-subcontractor-assignments"></a>Alvállalkozói megbízások újraköltségelése

Ha egy projektcsapat tagja (általános vagy elnevezett) az Alvállalkozói beállítások párbeszédpanelen alvállalkozói sorokhoz **kapcsolódik**, a csapattag által végzett tevékenységekhez való hozzárendelések az alvállalkozóhoz csatolt beszerzési árlista alapján újraköltségezik. A **Projekt** részletei lap Becsültek lapján **válassza az Árak frissítése** gombot az **alvállalkozásról** szóló döntésből eredő frissített díjszabás és/vagy költségszámítás megtekintéséhez.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
