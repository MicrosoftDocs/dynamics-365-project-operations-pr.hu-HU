---
title: A projektek értékesítésének és költségeinek becslése, ha egy foglalt erőforrás több szerepkört tölt be egy projekten
description: Ez a témakör ismerteti, hogyan használhatók árképzési dimenziók a több szerepkörrel rendelkező erőforrásra vonatkozó árképzési és költségszámítási becslések támogatására.
author: rumant
manager: tfehr
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: da17f0f58623128d51fda0f5529182cd37ea41b9
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531457"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>A projektek értékesítésének és költségeinek becslése, ha egy foglalt erőforrás több szerepkört tölt be egy projekten 

_**A következőre vonatkozik:** Project Operations az erőforrás-/nem készletalapú forgatókönyvekhez, Lite központi telepítés – ajánlattól proforma számlázásig, illetve Project Operations a készlet-/termelésalapú forgatókönyvekhez_ 

A projektalapú vállalatoknak gyakran szükségük van arra, hogy egy erőforrásra több szerepkört töltsön be egy projekten. Minden szerepkör eltérő árral és költséggel is rendelkezhet. Ez azt jelenti, hogy ugyanannak az erőforrásnak az ideje a projekten eltérő pénzügyi becslést is kaphat az egyes szerepkörökre vonatkozó számlázási és költségi rátáktól függően. A nevezett erőforráshoz tartozó csoporttag bejegyzésében szereplő értékeket különböző felülírásokkal állíthatja be az egyes feladatok esetében, amelyekhez a csoporttag hozzá van rendelve.

A következő példa végigvezeti azzal, hogy egy érték egyszerű felülírása, hogyan teszi lehetővé, hogy az erőforrás több szerepkörrel rendelkezzen a projekten, ahol különböző költség-és számlázási díjak szerepeljenek.

## <a name="create-tasks"></a>Feladatok létrehozása
A feladatok létrehozásához fel kell vennie a feladatokat, valamint az összefoglaló feladatokat, és ezek után a feladat időtartamának hozzáadása előtt hozzá kell rendelnie a feladatot. 

### <a name="add-tasks-and-summary-tasks"></a>Feladatok és összefoglaló feladatok hozzáadása
Feladat hozzáadásához hajtsa végre az alábbi műveleteket.

1. Válassza a **Projektek** elemet, és nyissa meg azt a projektet, amelyikhez feladatokat szeretne hozzáadni.
2. Válassza az **Új feladat hozzáadása** lehetőséget. Nevezze el a feladatot, majd nyomja le az **Enter** billentyűt .
3. Adjon meg egy másik feladatnevet, majd nyomja le az **Enter** billentyűt . Ismételje meg ezt, amíg a feladatok teljes listájával nem rendelkezik.
3. A feladatok **Összefoglaló** feladatok alatt történő behúzásához jelölje ki a feladat nevében a három függőleges pontot, majd válassza az **Alfeladattá alakítás** lehetőséget. 

  > [!TIP]
  > Egynél több feladat kijelöléséhez jelöljön ki egy feladatot, tartsa lenyomva a **Ctrl** billentyűt, és jelöljön ki egy másik feladatot.
  >
  > Az **Alfeladat előléptetése** funkcióval a feladatokat kiveheti az **Összefoglaló** feladatok közül.

### <a name="assign-tasks"></a>Feladatok hozzárendelése

Feladatok hozzárendeléséhez hajtsa végre az alábbi műveleteket.

1. A **Hozzárendelt** oszlopban jelölje ki az adott személy ikonját.
2. Válasszon egy csapattagot a listából, vagy írjon be szöveget egy név kereséséhez.

### <a name="add-task-duration-and-columns"></a>Feladat időtartamának és oszlopainak hozzáadása

Gyakran a legkönnyebb az időtartammal kezdeni a projekt kiépítését. Feladatidőtartam hozzáadásához hajtsa végre az alábbi lépéseket.

1. A feladat **Időtartam** oszlopában adja meg, hogy mit gondol, hány napig tart a feladat végrehajtása. Ha más időegységet szeretne használni, adjon meg egy számot, valamint az **órák**, **hetek** vagy **hónapok** értékét.
2. Ha azt szeretné, hogy a feladat rombusz alakú mérföldkőként jelenjen meg az **Idősor** nézetben, akkor az **Időtartam** oszlopban adjon meg **0 napot**.
3. Az **Enter** billentyű megnyomásával léphet a következő feladat **Időtartam** mezőjébe, és folytathatja az időtartamok megadását.

  > [!NOTE]
  > Az összefoglaló feladatokhoz nem adhat meg időtartamot.

A projekthez oszlopokat vehet fel, és így további részleteket is megadhat. Ehhez válassza az **Oszlop hozzáadása** lehetőséget. 

További információkat a [Projekt létrehozása](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749) fejezetben talál.

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>A szerepkör és a szervezeti egység beállítása általános projektcsapattag számára
Hajtsa végre az alábbi lépéseket egy általános csapattag szerepkörének és szervezeti egységének beállításához.

1. A **Feladatok** lapon jelölje ki az a **Feladat** sort az **A feladathoz**. 
2. A **Hozzárendelt** beállításnál válassza az **Általános erőforrás hozzáadása** lehetőséget. Ezzel megnyitja a **Csapattag gyorslétrehozása** oldalát.
3. A **Csapattagok gyors létrehozása** lapon adja meg a feladatot végrehajtó általános csoporttag attribútumait.
4. Jelölje ki a megfelelő szerepkört és szervezeti egységet, majd kattintson a **Mentés és bezárás** lehetőségre. A rendszer létrehoz egy általános csoporttagot, és hozzárendeli ehhez a feladathoz. 
5. Ismételje meg a 1–4 lépéseket a **B feladat esetében**. Ugyanakkor a **B feladathoz** az általános csoporttag hozmásik szerepkört és szervezeti egységet kell hozzárendelni, mint az **A feladat** esetében. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>A szerepkör és a szervezeti egység beállítása projektfeladathoz
Hajtsa végre az alábbi lépéseket egy feladat szerepkörének és szervezeti egységének beállításához.

1. Miután létrehozta az **A feladatot**, jelölje ki a feladatot, majd válassza az **i** ikont a **Feladat részletei** ablaktábla megnyitásához. 
2. A **Feladat részletei** ablaktáblában görgessen az aljára, és válassza a **Részletek megtekintése** lehetőséget a **Feladat részletei** oldal megnyitásához.
3. A **Feladat részletei** lapon, a **Szerepkör** és a **Szervezeti egység** területen adja meg a feladat végrehajtásához szükséges értékeket az erőforráshoz. 

  > [!NOTE]
  > Ha ezt az forgatókönyvet a Project Operations demo-adatok segítségével hajtja végre, válassza szerepkörnek a **Vezető tanácsadó**, illetve a szervezeti egységnek a **Fabrikam US** lehetőséget.

4. Válassza ki a **B feladatot**, majd válassza ki a feladatot.
5. Válassza az **i** ikont a **Feladat részletei** ablaktábla megnyitásához. 
6. A **Feladat részletei** ablaktáblában görgessen az aljára, és válassza a **Részletek megtekintése** lehetőséget a **Feladat részletei** oldal megnyitásához.
7. A **Feladat részletei** lapon, a **Szerepkör** és a **Szervezeti egység** területen adja meg az értékeket az erőforráshoz, amely elvégezné ezt a feladatot. A **B feladat** **Szerepkör** és **Szervezeti egység** szakaszában szereplő értékeknek meg kell egyezniük az **A feladat** értékeivel. 

  > [!NOTE]
  > Ha ezt az forgatókönyvet a Project Operations demo-adatok segítségével hajtja végre, válassza szerepkörnek a **Hálózati technikus**, illetve a szervezeti egységnek a **Fabrikam US** lehetőséget.

8. Mentse és zárja be a **Feladat részletei** lapot. 

## <a name="team-member-and-estimates-behavior"></a>Csoporttag és a becslések működése 
Ha meg szeretné ismerni a **Csoporttag** rácsának és a becsléseknek a működését, hajtsa végre az alábbi lépéseket.

1. A **Csoporttag** rácson jelölön ki a két általános csoporttagot, majd válassza a **Követelmények generálása** lehetőséget. Ez létrehozza az erőforrás-követelményeket. 
2. Válassza ki a csoporttag sort a **Vezető tanácsadó** lehetőségnél, majd válassza a **Foglalás** opciót. Megnyílik az ütemezési tábla az erőforrások listájával. Jelöljön ki egy erőforrást, majd válassza a **Foglalás** lehetőséget az erőforrás adott követelményhez való lefoglalásához.
3. Válassza ki a csoporttag sort a **Hálózati technikus** lehetőségnél, majd válassza a **Foglalás** opciót. Megnyílik az ütemezési tábla az erőforrások listájával. Jelölje ki ugyanazt az erőforrást, mint fent, majd válassza a **Foglalás** lehetőséget az erőforrás adott követelményhez való lefoglalásához.

### <a name="team-member-grid"></a>Csoporttag rács 

A **Csapattagok** rácsán a két általános csoporttag rekordja törlődik, és csak egy erőforrásra cserélődik le. Az adott erőforráshoz egy sor érték tartozik, amelyek a **Szerepkör** és a **Szervezeti egység** alapértelmezett értékei.

Ha kibontja az adott csoporttag rekordjának sorát, akkor mindkét feladathoz külön hozzárendelések láthatók a csapattagok bejegyzésében. Minden hozzárendelési sornak a **Szerepkörhöz** és a **Szervezeti egységhez** kapcsolódó feladatspecifikus értékei vannak. 

### <a name="estimates-grid"></a>Becslések rács 

A **Becslések** rácsán az ugyanarra az erőforrásra vonatkozó hozzárendelések eltérő árúak. Az **A feladatnál** az erőforráshoz rendelt hozzárendelés árazása a **Vezető tanácsadó** opció **Szerepkör** attribútumának értéke szerint történik. A **B feladatnál** az ugyanazon erőforráshoz rendelt hozzárendelés árazása a **Hálózati technikus** opció **Szerepkör** attribútumának értéke szerint történik.


[!INCLUDE[footer-include](../includes/footer-banner.md)]