---
title: Alvállalkozói lehetőségek projektcsoporttagok számára
description: Ez a témakör a Microsoft projektcsapat-tagjainak alvállalkozói lehetőségeit ismerteti Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: aacd2f97d3120a854c78fe87e512fad1c43b9651
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600193"
---
# <a name="subcontracting-options-for-project-team-members"></a>Alvállalkozói lehetőségek projektcsoporttagok számára

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations programban kiértékelheti a projektcsapat egy vagy több tagja számára elérhető alvállalkozói beállításokat. A rendelkezésre álló alvállalkozói lehetőségek lehetővé teszik, hogy:

- Hozzon létre egy új alvállalkozói szerződést és/vagy hozzon létre új sorokat egy meglévő alvállalkozói szerződésen a kijelölt projektcsapattagok számára. 
- Tartalék egy már meglévő alvállalkozói és alvállalkozói vonallal szemben. 

Választhat az általános projektcsapat-tagok számára rendelkezésre álló alvállalkozói lehetőségek közül, vagy választhat a projektcsapat azon tagjai közül, akik szerződéses dolgozóként megnevezett erőforrással vannak ellátva. 

A következőkre vonatkozóan nem állnak rendelkezésre alvállalkozói lehetőségek:

- A projektcsapat azon tagjai, akik egy alkalmazottal dolgoztak. 
- Alvállalkozói és alvállalkozói sorhoz már társított projektcsapat-tagok. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Nem álló projektcsapat-tag alvállalkozásba adása

Ha áttekintheti és ki szeretne választani egy általános vagy személyzettel nem rendelkező projektcsapat-tagra vonatkozó alvállalkozási lehetőségek közül, hajtsa végre az alábbi lépéseket:

1. Jelöljön ki egy vagy több projektcsapattag-bejegyzést, ahol az erőforrás általános erőforrás.
2. Győződjön meg arról, hogy a kijelölt projektcsapattag-bejegyzések egyike sem kapott már alvállalkozói szerződést. 
3. Válassza **az Alvállalkozói beállítások lehetőséget** a projektcsapat tagjai alrácson. Megnyílik **az Alvállalkozói beállítások** párbeszédpanel. 
4. Ha csak egy projektcsapattag-bejegyzést jelölt ki az 1. lépésben, akkor a következő lehetőségek lesznek elérhetők:
    - Hozzon létre új alvállalkozói sorokat. 
    - Foglalás meglévő alvállalkozói szerződés ellen Ha az 1. lépésben több projektcsapattag-rekordot jelölt ki, akkor az egyetlen elérhető lehetőség egy új alvállalkozói sor létrehozása.
5. A meglévő alvállalkozói sorra való foglalás lehetősége lehetővé teszi egy olyan alvállalkozói és alvállalkozói sor kiválasztását, amelyre tartalékolni szeretne. Amikor kiválaszt egy alvállalkozói sort a kapacitás lefoglalásához, győződjön meg arról, hogy a kiválasztott alvállalkozói sor időre szól, és hogy a projektcsapat-tagnál szükséges szerepkör megegyezik az alvállalkozói sorban vásárolt szerepkörrel.
6. Ha úgy dönt, hogy új alvállalkozói sorokat hoz létre a projektcsapat tagjai számára, a rendszer lehetővé teszi a sorok létrehozásához szükséges alvállalkozói szerződések kiválasztását. Annak az alvállalkozónak, amelyben új sorokat kíván létrehozni, Piszkozat **állapotúnak kell lennie**. Ezzel a beállítással új alvállalkozói sorokat hozhat létre a kiválasztott projektcsapat-tagok számára, a rendszer egy alvállalkozói sort hoz létre a projektcsapat minden egyes tagjához. A szerepkör, az órák és a dátumok a projektcsapat tagjából minden létrehozott alvállalkozói sorba átmásolódnak. 
7. Ha egy általános csapattag alvállalkozói és alvállalkozói sorhoz van társítva, az **általános csapattagsor Dolgozótípus** mezője Szerződésmunkás **dolgozóra**, az **Alvállalkozó érvényességének** értéke pedig Érvényesség **értékre** frissül.

## <a name="subcontracting-a-staffed-project-team-member"></a>A projektcsapat személyzetének tagja alvállalkozói szerződése

Az általános vagy személyzettel nem rendelkező csapattagokhoz hasonlóan megtekintheti a személyzettel rendelkező projektcsapattagok alvállalkozói lehetőségeit is, amennyiben a személyzettel rendelkező csapattag szerződéses alkalmazott. A személyzettel rendelkező vagy megnevezett projektcsapat-tagokra vonatkozó alvállalkozási lehetőségek áttekintéséhez és a választható lehetőségek közül való választáshoz hajtsa végre az alábbi lépéseket:

1. Jelöljön ki egy vagy több projektcsapat-tagbejegyzést, ahol az erőforrás neves szerződéses dolgozó.
2. Győződjön meg arról, hogy a kiválasztott projektcsapattag-bejegyzések egyike sem már alvállalkozói szerződéssel rendelkezik. 
3. Válassza **az Alvállalkozói beállítások lehetőséget** a projektcsapat tagjai alrácson. Megnyílik **az Alvállalkozói beállítások** párbeszédpanel. 
4. Ha csak egy projektcsapattag-bejegyzést jelölt ki az 1. lépésben, akkor a következő lehetőségek lesznek elérhetők:
      - Hozzon létre új alvállalkozói sorokat.
      - Tartalék egy meglévő alvállalkozói szerződéssel szemben.
  Ha az 1. lépésben több projektcsapattag-bejegyzést jelölt ki, akkor az egyetlen elérhető lehetőség egy új alvállalkozói sor létrehozása.
5. A meglévő alvállalkozói sorra való foglalás lehetősége lehetővé teszi egy olyan alvállalkozói és alvállalkozói sor kiválasztását, amelyre tartalékolni szeretne. Ha alvállalkozói sort választ a kapacitás lefoglalásához, a következőket kell biztosítania:
      - A kiválasztott alvállalkozói sor időre szól. 
      - A projektcsapat-tagnál szükséges szerepkör megegyezik az alvállalkozói sorban megvásárolt szerepkörrel. 
      - Az a szállító, amelyhez a szerződéses dolgozó társítva van, megegyezik az alvállalkozói szerződés szállítójával.
6. Ha úgy dönt, hogy új alvállalkozói sorokat hoz létre a projektcsapat tagjai számára, a rendszer lehetővé teszi a sorok létrehozásához szükséges alvállalkozói szerződések kiválasztását. Ezzel a beállítással győződjön meg arról, hogy a szállító, akihez a szerződéses dolgozó tartozik, megegyezik az alvállalkozói szerződés szállítójával. 
7. Annak az alvállalkozónak, amelyben új sorokat kíván létrehozni, Piszkozat **állapotúnak kell lennie**. Ezzel a beállítással új alvállalkozói sorokat hozhat létre a kiválasztott projektcsapat-tagok számára, a rendszer egy alvállalkozói sort hoz létre a projektcsapat minden egyes tagjához. A szerepkör, az órák és a dátumok a projektcsapat tagjából minden létrehozott alvállalkozói sorba átmásolódnak.  
8. Ha egy megnevezett csapattag alvállalkozói és alvállalkozói sorhoz van társítva, a **megnevezett csapattag sor Dolgozótípus** mezője Szerződés dolgozó **dolgozóra**, az **Alvállalkozó érvényességi** értéke pedig Érvényes **értékre** lesz frissítve.

## <a name="re-costing-subcontractor-assignments"></a>Alvállalkozói hozzárendelések újraköltségezése

Ha egy (általános vagy elnevezett) projektcsapattag az **Alvállalkozói beállítások** párbeszédpanelen alvállalkozói sorokhoz van csatolva, a csapattag tevékenységeihez való hozzárendelések az alvállalkozói szerződéshez csatolt beszerzési árlista alapján újra költségszámításra kerülnek. **A Projekt részletei** lap Becslések **lapján** válassza az Árak frissítése gombot **az** alvállalkozói szerződéskötésről szóló döntésből eredő frissített árképzés és/vagy költségszámítás megtekintéséhez.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
