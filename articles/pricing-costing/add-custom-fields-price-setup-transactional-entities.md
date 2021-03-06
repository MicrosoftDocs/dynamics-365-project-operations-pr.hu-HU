---
title: Kötelező egyéni mezők hozzáadása az árbeállításhoz és a tranzakciós entitásokhoz
description: Ez a témakör a kötelező egyéni mezőhivatkozások entitásokhoz, űrlapokhoz és nézetekhez való hozzáadását ismerteti.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a27bfe881fdb6431941fa860d279e3e7b526f623
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898309"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Kötelező egyéni mezők hozzáadása az árbeállításhoz és a tranzakciós entitásokhoz

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Ez a témakör feltételezi, hogy elvégezte az [Egyéni mezők és entitások létrehozása árazási dimenziókként való használathoz](create-custom-fields-entities-pricing-dimensions.md) című témakör eljárásait. Ha még nem fejezte be ezeket az eljárásokat, menjen vissza, és fejezze be őket, majd térjen vissza ehhez a témához. 

Ebben a témakörben az eljárások megmutatják, hogyan lehet hozzáadni a szükséges egyéni mező hivatkozásokat az entitásokhoz és a felhasználói felület (UI) elemeihez, például űrlapokhoz és nézetekhez.

## <a name="add-custom-pricing-dimension-fields"></a>Egyéni árképzési dimenzió mezők hozzáadása 
Az egyéni mezők és entitások létrehozása után a következő lépés az árbeállítás és a tranzakciós entitások értesítése az egyéni entitásokról és opciókészletekről referenciamezők létrehozásával. Attól függően, hogy az árképzési dimenziók listái tartalmaznak-e értékkészlet dimenziókat vagy entitás dimenziókat vagy mindkettőt csak az **Értékkészlet alapú egyéni árképzési dimenziók** vagy az **Entitás alapú egyéni árképzési dimenziók** vagy mindkettő lépéseit kövesse.

### <a name="option-set-based-custom-pricing-dimensions"></a>Értékkészlet-alapú egyéni árképzési dimenziók
Ha az egyéni árképzési dimenzió értékkészlet-alapú, mezőként adja hozzá a kulcsfontosságú entitásokhoz. A következő eljárásban az **Erőforrás munkahely** és az **Erőforrás munkaidő** értékkészlet alapú árképzési dimenziókként kerül felhasználásra. Ezeket először mezőként kell hozzáadni az árképzési entitásokhoz, a **Szerepkörár** és a **Szerepkör-árrések** entitásokhoz.

1. A projektműveletek között válassza a **Beállítások** > **Megoldások** lehetőséget, és kattintson duplán a(z) **\<your organization name> árazási dimenzióira**. 
2. A Megoldástallózóban a bal oldali ablaktáblában válassza az **Entitások > Szerepkörár** elemet.
3. Bontsa ki a **Szerepkörár** entitást, és válassza a **Mezők** elemet.
4. Kattintson az **Új** elemre egy új, **Erőforrás munkahely** nevű mező létrehozásához és válassza az **Értékkészlet** elemet a mező típusaként. 
5. Válassza a **Meglévő értékkészlet használata** elemet, válassza az **Erőforrás munkahely** értékkészletet, majd kattintson a **Mentés** elemre.
6. Ismételje meg az 1-5. lépéseket, hogy hozzáadja ezt a mezőt a **Szerepkör-árrések** entitáshoz. 
7. Ismételje meg az 1-5. lépéseket az **Erőforrás munkaóra** értékkészletnél.

> [!IMPORTANT]
> Ha egynél több entitáshoz ad hozzá egy mezőt, ugyanazt a mezőnevet használja az összes entitásnál. 

Egy projekt értékesítési és becslési fázisában megbecsülheti a **Helyi** és **Helyszíni** munkák elvégzéséhez szükséges munkaráfordítást, a **Normál munkaórák** és a **Túlórák** pedig az Árajánlat/Projekt értékének becsléséhez használhatók. A rendszer az **Erőforrás munkahely** és az **Erőforrás munkaóra** mezőket hozzáadja az **Árajánlatsor részletei**, a **Szerződéssorrészletek**, a **Projektcsoporttag** és a **Becsléssor** becslési entitásokhoz.

1. A projektműveletek között válassza a **Beállítások** > **Megoldások** lehetőséget, és kattintson duplán a(z) **\<your organization name> árazási dimenzióira**. 
2. A Megoldástallózóban a bal oldali ablaktáblában válassza az **Entitások > Árajánlatsor részletei** elemet.
3. Bontsa ki az **Árajánlatsor részletei** entitást, és válassza a **Mezők** elemet.
4. Kattintson az **Új** elemre egy új, **Erőforrás munkahely** nevű mező létrehozásához és válassza ki az **Értékkészlet** mezőtípust. 
5. Válassza a **Meglévő értékkészlet használata** elemet, válassza az **Erőforrás munkahely** lehetőséget, majd kattintson a **Mentés** elemre.
6. Ismételje meg az 1-5. lépéseket, hogy hozzáadja ezt a mezőt a **Projektszerződés sorának részletei**, a **Projektcsoporttag** és a **Becsléssor** entitásokhoz.
7. Ismételje meg az 1-6. lépéseket az **Erőforrás munkaóra** értékkészletnél. 

A kézbesítéshez és a számlázáshoz a befejezett munka árképzését pontosan kell elvégezni: ki kell választani, hogy **Helyi** vagy **Helyszíni** munkavégzés történt-e, és hogy **Normál munkaórában** vagy **Túlórában** végezték-e a Projekt tényadatai szerint. Az **Erőforrás munkahely** és az **Erőforrás munkaóra** mezőket hozzá kell adni az **Időbejegyzés**, a **Tényadat**, a **Számlasor részletei** és a **Naplósor** entitásokhoz.

1. Válassza a **Beállítások** > **Megoldások** lehetőséget, és kattintson duplán a(z) **\<your organization name> árazási dimenzióira**.
2. A Megoldástallózóban a bal oldali ablaktáblában válassza az **Entitások > Időbejegyzés** elemet.
3. Bontsa ki az **Árajánlatsor részletei** entitást, és válassza a **Mezők** elemet.
4. Kattintson az **Új** elemre egy új, **Erőforrás munkahely** nevű mező létrehozásához és válassza az **Értékkészlet** elemet a mező típusaként. 
5. Válassza a **Meglévő értékkészlet használata** elemet, válassza az **Erőforrás munkahely** értékkészletet, majd kattintson a **Mentés** elemre.
6. Ismételje meg az 1-5. lépéseket, hogy hozzáadja ezt a mezőt a **Tényadatok**, a **Számlasor részletei** és a **Naplósor** entitásokhoz.
7. Ismételje meg az 1-6. lépéseket az **Erőforrás munkaóra** értékkészletnél. 

Ez kiegészíti az értékkészlet alapú egyéni dimenziókhoz szükséges sémaváltozásokat.

## <a name="entity-based-custom-pricing-dimensions"></a>Entitás alapú egyéni árképzési dimenziók

Ha az egyéni árképzési dimenzió entitás, 1:N kapcsolatot adhat a dimenzió entitás és a kulcsfontosságú entitások közé. A fenti Szabványos munkakör példája alapján ésszerű elvárás, hogy minden alkalmazott legyen hozzárendelve egy szabványos munkakörhöz. Ennek eredményeként szüksége lesz egy 1:N kapcsolatra a szabványos munkakörtől és a foglalható erőforrásig, vagy egy N:1 kapcsolatra a foglalható erőforrástól a szabványos munkakörig.

1. A projektműveletek között válassza a **Beállítások** > **Megoldások** lehetőséget, és kattintson duplán a(z) **\<your organization name> árazási dimenzióira**. 
2. A Megoldástallózóban a bal oldali ablaktáblában válassza az **Entitások > Szabványos munkakör** elemet.
3. Bontsa ki a **Szabványos munkakör** entitást, és válassza az **1:N kapcsolatok** elemet.
4. Válassza az **Új** lehetőséget az új, **Szabványos munkakör foglalható erőforrásokhoz** nevű 1:N kapcsolat létrehozásához. Írja be a szükséges információkat, majd kattintson a **Mentés** elemre.

A szabványos munkakört szintén hozzá kell adni a **Szerepkörár** és a **Szerepkör-árrés** árképzési entitásokhoz. Ez is 1:N kapcsolatok létrehozásával fejeződik be a **Szabványos munkakör** és a **Szerepkörár** entitások, valamint a **Szabványos munkakör** és a **Szerepkör-árrés** entitások között.

1. A Megoldástallózóban a bal oldali ablaktáblában válassza az **Entitások > Szabványos munkakör** elemet.
2. Bontsa ki a **Szabványos munkakör** entitást, és válassza az **1:N kapcsolatok** elemet.
3. Kattintson az **Új** elemre egy új, **Szabványos munkakör szerepkörárhoz** nevű 1:N kapcsolat létrehozásához. Írja be a szükséges információkat, majd kattintson a **Mentés** elemre.
4. Ismételje meg az 1-4. lépéseket 1:N kapcsolatok létrehozásához a **Szabványos munkakör** és a **Szerepkör-árrés** entitások között.

Egy projekt értékesítési és becslési fázisában az Árajánlat/Projekt árazásához megbecsüli az egyes szabványos munkakörökhöz szükséges munkaráfordítást. Ez azt jelenti, hogy 1:N kapcsolatokra van szükség a szabványos munkakörtől a becslési entitások mindegyikéhez: 

- **Árajánlatsor részletei**
- **Projektszerződés sorának részletei**
- **Projektcsoporttag**
- **Becsléssor**

5. Ismételje meg az 1-5. lépéseket 1:N kapcsolatok létrehozásához a **Szabványos munkakör** elemtől az **Árajánlatsor részletei**, a **Projektszerződés sorának részletei**, a **Projektcsoporttag** és a **Becsléssor** elemhez.

  A kézbesítési és a számlázási szakaszban az egyes szabvány munkakörökkel elvégzett munkának pontosan beárazottnak kell lennie a Projekt tényadatainál. Ez azt jelenti, hogy 1:N kapcsolatokra van szükség a **Szabványos munkakör** elemtől az **Időbejegyzés**, a **Tényadat**, a **Számlasor részletei** és a **Naplósor** entitásokhoz.

6. Ismételje meg az 1-6. lépéseket 1:N kapcsolatok létrehozásához a **Szabványos munkakör** elemtől az **Időbejegyzés**, a **Tényadat**, a **Számlasor részletei** és a **Naplósor** entitásokhoz.

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Állítson be alapértelmezett Dimenziós értéket a platform hozzárendelési funkciói segítségével
Az időbejegyzésnél hasznos lenne, ha a rendszer alapértelmezettként kezelné a szabványos munkakört az Időbejegyzésnél a foglalható erőforrásoktól, amelyek az időbejegyzést rögzítik. A következő lépésekkel adjon hozzá mezőleképezéseket a **Foglalható erőforrás** elemtől az **Időbejegyzés** elemre mutató 1:N kapcsolathoz.

1. A Megoldástallózóban a bal oldali ablaktáblában válassza az **Entitások > Szabványos munkakör** elemet.
2. Bontsa ki a **Szabványos munkakör** entitást, és válassza az **1:N kapcsolatok** elemet.
3. Kattintson duplán a **Foglalható erőforrástól az időbejegyzéshez** elemre. A **Kapcsolat** oldalon válassza a **Mezőleképezések használata** lehetőséget. 
4. Válassza az **Új** lehetőséget a **Foglalható erőforrás** entitás **Szabványos munkakör** mezője és az **Időbejegyzés** entitás **Szabványos munkakör** referenciamezője közötti új leképezés létrehozásához. 

Ez kiegészíti az entitás alapú egyéni dimenziókhoz szükséges sémaváltozásokat.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Adjon hozzá egyéni mezőket az űrlapokhoz, nézetekhez és üzleti szabályokhoz

Az összes szükséges sémaváltoztatás elvégzése után a következő lépés a mezők láthatóvá tétele a felhasználói felületen, mezők hozzáadásával az űrlapokhoz és a nézetekhez.

1. Nyissa meg az űrlapot vagy a nézetet. A jobb oldali ablaktáblában válassza ki a mezőt, és húzza az űrlap vászonjára. 
2. Nézet szerkesztésekor használja a jobb oldali ablaktáblát, válassza a **Mezők hozzáadása** lehetőséget, majd a **Mezők listája** párbeszédpanelen válassza ki a szükséges mezőket, és kattintson az **Ok** elemre.

Az alábbi táblázat entitásonként felsorolva, átfogó módon biztosítja azon beépített űrlapokat és nézeteket, amelyeket új mezőkkel kell frissíteni. Ha ezeknek az entitásoknak a testreszabásaiban további nézetek vagy űrlapok vannak, akkor az új mezőket is hozzá kell adni azokhoz.

| Entity        | Az új mezőt igénylő űrlapok   |Az új mezőt igénylő nézetek      |
| ------------------------------|---------------------------------|----------------------------------|
|  Szerepkörár|• Információ |• Aktív erőforrás kategóriaárak<br> • Erőforrás-kategóriaárhoz kapcsolódó nézet|
|  Szerepkörárrés|• Információ|• Aktív szerepkör felár<br>• Aktív szerepkör felárral kapcsolatos nézet|
|  Árajánlatsor részletei|• Projektinformációk<br>• Projekt Gyors létrehozás|• Aktív ajánlati sor részlete<br>• Kombinált ajánlatsor részletei<br>• Ajánlatsorral kapcsolatos nézet|
|  A projekt szerződés sorának részlete|• Projektinformációk<br>• Projekt Gyors létrehozás|• Kombinált szerződéssorrészletek<br>• Aktív szerződéses sor részletei<br>• Szerződéssor részleteinek társított nézete|
|  Projektcsoporttag|• Információ<br>• Új űrlap|• Aktív projektcsapattagok<br>• Projektcsapattagok<br>• A Projektcsapattagokkal társított nézet|
|  Időbejegyzés|• Információ<br>• Időbejegyzés létrehozása|• Saját időbejegyzés dátum szerint<br>• Saját időbejegyzések erre a hétre<br>• Saját időbejegyzések jóváhagyása|
|  Naplósor|• Információ<br>• Gyors létrehozás|• Aktív naplósorok<br>• A Naplósorhoz kapcsolódó nézet|
|  Számlasor részletei|• Információ<br>• Gyors létrehozás|• Aktív számlasor részletei<br>• Díjazható számlatranzakciók<br>• Ingyenes számlatranzakciók<br>• A számlához tartozó sor részletének nézete<br>• Nem díjazható számlatranzakciók|
|  Tény|• Információ<br>• Aktív adatok|• Tényleges társított nézet|

Előfordulhat, hogy az egyéni mezőket hozzá kell adni az üzleti szabályokhoz, attól függően, hogy mit határozott meg. Az egyik out-of-box példa az **Időbejegyzés szerkeszthetősége az állapot alapján** üzleti szabályra vonatkozik. Ez a szabály meghatározza, hogy mely mezőket kell zárolni, ha az Időbejegyzés nem szerkeszthető, például **Jóváhagyott** állapotban. Adjon hozzá mezőket ehhez az üzleti szabályhoz, hogy a mezők zárolva legyenek a szerkesztésre vonatkozóan, ha az Időbejegyzés nem **Vázlat** vagy **Visszaküldött** állapotban van.
