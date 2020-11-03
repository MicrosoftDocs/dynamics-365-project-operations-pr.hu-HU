---
title: A projektek értékesítésének és költségeinek becslése, ha egy foglalható erőforrás több szerepkört tölt ki egy projektben
description: Ez a témakör információt nyújt arról, hogy az árképzési dimenziók hogyan használhatók fel az árképzésre és a költségszámításra olyan erőforrások esetében, amelyek több szerepkört töltenek ki egy projektben.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078144"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a>A projektek értékesítésének és költségeinek becslése, ha egy foglalható erőforrás több szerepkört tölt ki egy projektben 

A projektalapú vállalatoknak gyakran szükségük van egy olyan erőforrásra, amely több szerepkört hajt végre a projektben. Az egyes szerepkörök árazása és elszámolása eltérhet, ami azt jelenti, hogy ugyanazon erőforrás ideje a projektre vonatkozóan eltérő pénzügyi becslést kaphat az egyes szerepkörök számla- és költségmértékének függvényében. A Project Service Automation lehetővé teszi, hogy a csoporttagrekordban szereplő értékek a megadott erőforráshoz legyenek beállítva, valamint különböző felülbírálásokat tesz lehetővé a csoporttaghoz rendelt minden egyes feladat esetében.

A következő példa azt mutatja be, hogyan teszi lehetővé az érték egyszerű felülírása, hogy egy erőforrás több szerepkörrel rendelkezzen a projektben, ahol különböző költség- és számlázási mértékek szerepelnek.

## <a name="create-tasks"></a>Feladatok létrehozása
Hozzon létre két, egyenként 40 órára vonatkozó projektfeladatot, a „A” és a „B” feladatot. Válassza ki az „A” feladatot a „B” feladat elődjeként.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Szerepkör és Szervezeti egység beállítása általános projektcsoporttag számára

1. Az **Ütemezés** lapon jelölje ki a **Feladat** sort az „A” Feladathoz. 
2. Az **Erőforrások** mezőben válassza ki a **Létrehozás** elemet a legördülő listából.
3. A **Csapattagok gyors létrehozása** lapon adja meg a feladatot végrehajtó általános csoporttag attribútumait.
4. Jelölje ki a megfelelő szerepkört és szervezeti egységet, majd kattintson a **Mentés és bezárás** lehetőségre. A rendszer létrehoz egy általános csoporttagot, és hozzárendeli ehhez a feladathoz. 

Ismételje meg ezeket a lépéseket a „B” feladat esetében is, és győződjön meg arról, hogy a „B” feladathoz létrehozott általános csoporttagon létrehozott szerepkör és szervezeti egység nem egyezik meg az „A” feladatban megadottakkal. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Szerepkör és szervezeti egység beállítása egy projektfeladathoz

1. Miután létrehozta az „A” feladatot, jelölje ki a feladatot, majd válassza a **Feladat szerkesztése** lehetőséget.
2. A **Feladat részletei** lapon keresse meg a **Szerepkör** és a **Szervezeti egység** mezőket, és adja hozzá a feladatot végrehajtó erőforráshoz szükséges értékeket. 

  > [!NOTE]
  > Ha a Project Service Automation demóadatainak használatával hajtja végre ezt a műveletet, jelölje be a **Vezető tanácsadó** lehetőséget a szerepkörhöz, és a **Fabrikam US** lehetőséget a szervezeti egységhez.

3. Jelölje ki a „B” feladatot, és válassza ki a **Feladat szerkesztése** lehetőséget.
4. A **Feladat részletei** lapon keresse meg a **Szerepkör** és a **Szervezeti egység** mezőket, és adja hozzá a feladatot végrehajtó erőforráshoz szükséges értékeket. Ügyeljen arra, hogy a **Szerepkör** és a **Szervezeti egység** mezőkben szereplő értékek „B” feladat esetében eltérőek legyenek az „A” feladatban megadottaktól. 

  > [!NOTE]
  > Ha a Project Service Automation demóadatainak használatával hajtja végre ezt a műveletet, jelölje be a **Hálózati technikus** lehetőséget a szerepkörhöz, és a **Fabrikam US** lehetőséget a szervezeti egységhez.

5. Mentse és zárja be a **Feladat részletei** lapot. 

## <a name="team-member-and-estimates-behaviour"></a>Csoporttag és becslések viselkedése 

1. A **Feladat részletei** lapon a **Csoporttag** lehetőségnél jelölje ki a két általános csoporttagot, majd válassza a **Követelmények létrehozása** lehetőséget. Ez létrehozza az erőforrás-követelményeket. 
2. Válassza ki a csoporttag sort a **Vezető tanácsadó** lehetőségnél, majd válassza a **Foglalás** opciót. Megnyílik az ütemezési tábla, és lefoglalja az adott követelménynek megfelelő erőforrást.
3. Válassza ki a csoporttag sort a **Hálózati technikus** lehetőségnél, majd válassza a **Foglalás** opciót. Megnyílik az ütemezési tábla, és lefoglalja ugyanazt az erőforrást az adott követelménynek.

### <a name="team-member-grid"></a>Csoporttag rács 
A **Csoporttag** rácson figyelje meg, hogy a két általános csoporttag bejegyzése törlődik, és lecserélődik egy erőforrásra. Az adott erőforráshoz egy értékkészlet van megadva, amely a **Szerepkör** és a **Szervezeti egység** alapértelmezett értékeit jeleníti meg.
Ha kibontja a csoporttagrekord sorát, akkor mindkét feladathoz külön hozzárendelések jelennek meg a csoporttagrekordban. Minden hozzárendelési sornak a **Szerepkörhöz** és a **Szervezeti egységhez** kapcsolódó feladatspecifikus értékei vannak. 

### <a name="estimates-grid"></a>Becslések rács 
Amikor megnyitja a **Becslések** rácsot, megfigyelheti, hogy az ugyanahhoz az erőforráshoz tartozó hozzárendelések eltérően vannak árazva.
Az „A” feladatnál az erőforráshoz rendelt hozzárendelés árazása a **Vezető tanácsadó** opció **Szerepkör** attribútumának értéke szerint történik. A „B” feladatnál az ugyanazon erőforráshoz rendelt hozzárendelés árazása a **Hálózati technikus** opció **Szerepkör** attribútumának értéke szerint történik.





