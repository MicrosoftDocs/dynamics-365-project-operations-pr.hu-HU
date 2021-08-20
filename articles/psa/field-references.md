---
title: Egyéni mezők hozzáadása az árbeállításhoz és a tranzakciós entitásokhoz
description: Ez a témakör információkat nyújt az egyéni mezők árbeállításhoz és tranzakciós entitásokhoz való hozzáadásáról.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3ca48b8d5d55b1b2178f9bd84e19d9599f057aa296a728cca57577c18fdaf307
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985774"
---
# <a name="add-custom-fields-to-price-setup-and-transactional-entities"></a>Egyéni mezők hozzáadása az árbeállításhoz és a tranzakciós entitásokhoz 

[!include [banner](../includes/psa-now-project-operations.md)]

Ez a témakör feltételezi, hogy elvégezte az [Egyéni mezők és entitások létrehozása](create-custom-fields-entities.md) című témakör eljárásait. Ha még nem fejezte be ezeket az eljárásokat, menjen vissza, és fejezze be őket, majd térjen vissza ehhez a témához. 

Ebben a témakörben az eljárások megmutatják, hogyan lehet hozzáadni a szükséges egyéni mező hivatkozásokat az entitásokhoz és a felhasználói felület (UI) elemeihez, például űrlapokhoz és nézetekhez.

## <a name="add-custom-pricing-dimension-fields"></a>Egyéni árképzési dimenzió mezők hozzáadása 
Az egyéni mezők és entitások létrehozása után a következő lépés az árbeállítás és a tranzakciós entitások értesítése az egyéni entitásokról és opciókészletekről referenciamezők létrehozásával. Attól függően, hogy az árképzési dimenziók listái tartalmaznak-e értékkészlet dimenziókat vagy entitás dimenziókat vagy mindkettőt csak az **Értékkészlet alapú egyéni árképzési dimenziók** vagy az **Entitás alapú egyéni árképzési dimenziók** vagy mindkettő lépéseit kövesse.

### <a name="option-set-based-custom-pricing-dimensions"></a>Értékkészlet-alapú egyéni árképzési dimenziók
Ha az egyéni árképzési dimenzió értékkészlet-alapú, mezőként adja hozzá a kulcsfontosságú Project Service entitásokhoz. A következő eljárásban az **Erőforrás munkahely** és az **Erőforrás munkaidő** értékkészlet alapú árképzési dimenziókként kerül felhasználásra. Ezeket először mezőként kell hozzáadni az árképzési entitásokhoz, a **Szerepkörár** és a **Szerepkör-árrések** entitásokhoz.

1. A Project Service Automation (PSA) szolgáltatásban kattintson a **Beállítások** > **Megoldások** elemre, majd kattintson duplán az **\<your organization name> árazási dimenziók** elemre. 
2. A Megoldástallózóban a bal oldali ablaktáblában válassza az **Entitások > Szerepkörár** elemet.
3. Bontsa ki a **Szerepkörár** entitást, és válassza a **Mezők** elemet.
4. Kattintson az **Új** elemre egy új, **Erőforrás munkahely** nevű mező létrehozásához és válassza az **Értékkészlet** elemet a mező típusaként. 
5. Válassza a **Meglévő értékkészlet használata** elemet, válassza az **Erőforrás munkahely** értékkészletet, majd kattintson a **Mentés** elemre.
6. Ismételje meg az 1-5. lépéseket, hogy hozzáadja ezt a mezőt a **Szerepkör-árrések** entitáshoz. 
7. Ismételje meg az 1-5. lépéseket az **Erőforrás munkaóra** értékkészletnél.

> [!IMPORTANT]
> Ha egynél több entitáshoz ad hozzá egy mezőt, ugyanazt a mezőnevet használja az összes entitásnál. 

> ![Az erőforrás munkahely hozzáadása a Szerepkörárhoz.](media/RWL-Field.png)

Egy projekt értékesítési és becslési fázisában megbecsülheti a **Helyi** és **Helyszíni** munkák elvégzéséhez szükséges munkaráfordítást, a **Normál munkaórák** és a **Túlórák** pedig az Árajánlat/Projekt értékének becsléséhez használhatók. A rendszer az **Erőforrás munkahely** és az **Erőforrás munkaidő** mezőket hozzáadja az **Árajánlatsor részletei**, a **Szerződéssorrészletek**, a **Projektfeladat**, a **Projektcsoporttag** és a **Becsléssor** becslési entitásokhoz.

1. A PSA-ban válassza ki a **Beállítások** > **Megoldások** lehetőséget, és kattintson duplán a(z) **\<your organization name> árazási dimenzióira**. 
2. A Megoldástallózóban a bal oldali ablaktáblában válassza az **Entitások > Árajánlatsor részletei** elemet.
3. Bontsa ki az **Árajánlatsor részletei** entitást, és válassza a **Mezők** elemet.
4. Kattintson az **Új** elemre egy új, **Erőforrás munkahely** nevű mező létrehozásához és válassza az **Értékkészlet** elemet a mező típusaként. 
5. Válassza a **Meglévő értékkészlet használata** elemet, válassza az **Erőforrás munkahely** lehetőséget, majd kattintson a **Mentés** elemre.
6. Ismételje meg az 1–5. lépéseket, hogy hozzáadja ezt a mezőt a **Projektszerződés sorának részletei**, a **Projektfeladat**, a **Projektcsoporttag** és a **Becsléssor** entitásokhoz.
7. Ismételje meg az 1-6. lépéseket az **Erőforrás munkaóra** értékkészletnél. 

> ![Az erőforrás munkahely hozzáadása a Becsléssorhoz.](media/RWL-Default-Value.png)


A kézbesítéshez és a számlázáshoz a befejezett munka árképzését pontosan kell elvégezni: ki kell választani, hogy **Helyi** vagy **Helyszíni** munkavégzés történt-e, és hogy **Normál munkaórában** vagy **Túlórában** végezték-e a Projekt tényadatai szerint. Az **Erőforrás munkahely** és az **Erőforrás munkaóra** mezőket hozzá kell adni az **Időbejegyzés**, a **Tényadat**, a **Számlasor részletei** és a **Naplósor** entitásokhoz.

1. A PSA-ban válassza ki a **Beállítások** > **Megoldások** lehetőséget, és kattintson duplán a(z) **\<your organization name> árazási dimenzióira**.
2. A Megoldástallózóban a bal oldali ablaktáblában válassza az **Entitások > Időbejegyzés** elemet.
3. Bontsa ki az **Árajánlatsor részletei** entitást, és válassza a **Mezők** elemet.
4. Kattintson az **Új** elemre egy új, **Erőforrás munkahely** nevű mező létrehozásához és válassza az **Értékkészlet** elemet a mező típusaként. 
5. Válassza a **Meglévő értékkészlet használata** elemet, válassza az **Erőforrás munkahely** értékkészletet, majd kattintson a **Mentés** elemre.
6. Ismételje meg az 1-5. lépéseket, hogy hozzáadja ezt a mezőt a **Tényadatok**, a **Számlasor részletei** és a **Naplósor** entitásokhoz.
7. Ismételje meg az 1-6. lépéseket az **Erőforrás munkaóra** értékkészletnél. 

> ![Az erőforrás munkahely hozzáadása az Időbejegyzéshez.](media/RWL-time-entry.png)

Ez kiegészíti az értékkészlet alapú egyéni dimenziókhoz szükséges sémaváltozásokat.

## <a name="entity-based-custom-pricing-dimensions"></a>Entitás alapú egyéni árképzési dimenziók

Ha az egyéni árképzési dimenzió egy entitás, 1:N kapcsolatot adhat a dimenzió entitás és a kulcsfontosságú Project Service entitások közé. A fenti Szabványos munkakör példája alapján ésszerű elvárás, hogy minden alkalmazott legyen hozzárendelve egy szabványos munkakörhöz. Ennek eredményeként szüksége lesz egy 1:N kapcsolatra a szabványos munkakörtől és a foglalható erőforrásig, vagy egy N:1 kapcsolatra a foglalható erőforrástól a szabványos munkakörig.

1. A PSA-ban válassza ki a **Beállítások** > **Megoldások** lehetőséget, és kattintson duplán a(z) **\<your organization name> árazási dimenzióira**. 
2. A Megoldástallózóban a bal oldali ablaktáblában válassza az **Entitások > Szabványos munkakör** elemet.
3. Bontsa ki a **Szabványos munkakör** entitást, és válassza az **1:N kapcsolatok** elemet.
4. Kattintson az **Új** elemre egy új, **Szabványos munkakör foglalható erőforrásokhoz** nevű 1:N kapcsolat létrehozásához. Írja be a szükséges információkat, majd kattintson a **Mentés** elemre.

> ![Szabványos munkakör hozzáadása foglalható erőforráshoz referenciamezőként.](media/ST-BR.png)

A szabványos munkakört szintén hozzá kell adni a **Szerepkörár** és a **Szerepkör-árrés** Project Service árképzési entitásokhoz. Ez is 1:N kapcsolatok létrehozásával fejeződik be a **Szabványos munkakör** és a **Szerepkörár** entitások, valamint a **Szabványos munkakör** és a **Szerepkör-árrés** entitások között.

1. A Megoldástallózóban a bal oldali ablaktáblában válassza az **Entitások > Szabványos munkakör** elemet.
2. Bontsa ki a **Szabványos munkakör** entitást, és válassza az **1:N kapcsolatok** elemet.
3. Kattintson az **Új** elemre egy új, **Szabványos munkakör szerepkörárhoz** nevű 1:N kapcsolat létrehozásához. Írja be a szükséges információkat, majd kattintson a **Mentés** elemre.
4. Ismételje meg az 1-4. lépéseket 1:N kapcsolatok létrehozásához a **Szabványos munkakör** és a **Szerepkör-árrés** entitások között.

Egy projekt értékesítési és becslési fázisában az Árajánlat/Projekt árazásához megbecsüli az egyes szabványos munkakörökhöz szükséges munkaráfordítást. Ez azt jelenti, hogy 1:N kapcsolatokra van szükség a szabványos munkakörtől a becslési entitások mindegyikéhez a Project Service szolgáltatásban: 

- **Árajánlatsor részletei**
- **Projektszerződés sorának részletei**
- **Projektfeladat**
- **Projektcsoporttag**
- **Becsléssor**

5. Ismételje meg az 1–5. lépéseket 1:N kapcsolatok létrehozásához a **Szabványos munkakör** elemtől az **Árajánlatsor részletei**, a **Projektszerződés sorának részletei**, a **Projektfeladat**, a **Projektcsoporttag** és a **Becsléssor** elemhez.

> ![Szabványos munkakör hozzáadása becsléssorhoz referenciamezőként.](media/ST-Estimate-Line.png)

A kézbesítési és a számlázási szakaszban az egyes szabvány munkakörökkel elvégzett munkának pontosan beárazottnak kell lennie a Projekt tényadatainál. Ez azt jelenti, hogy 1:N kapcsolatokra van szükség a **Szabványos munkakör** elemtől az **Időbejegyzés**, a **Tényadat**, a **Számlasor részletei** és a **Naplósor** entitásokhoz.

6. Ismételje meg az 1-6. lépéseket 1:N kapcsolatok létrehozásához a **Szabványos munkakör** elemtől az **Időbejegyzés**, a **Tényadat**, a **Számlasor részletei** és a **Naplósor** entitásokhoz.

> ![Szabványos munkakör hozzáadása időbejegyzéshez referenciamezőként.](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Állítson be alapértelmezett Dimenziós értéket a platform hozzárendelési funkciói segítségével
Az időbejegyzésnél hasznos lenne, ha a rendszer alapértelmezettként kezelné a szabványos munkakört az Időbejegyzésnél a foglalható erőforrásoktól, amelyek az időbejegyzést rögzítik. A következő lépésekkel adjon hozzá mezőleképezéseket a **Foglalható erőforrás** elemtől az **Időbejegyzés** elemre mutató 1:N kapcsolathoz.

1. A Megoldástallózóban a bal oldali ablaktáblában válassza az **Entitások > Szabványos munkakör** elemet.
2. Bontsa ki a **Szabványos munkakör** entitást, és válassza az **1:N kapcsolatok** elemet.
3. Kattintson duplán a **Foglalható erőforrástól az időbejegyzéshez** elemre. A **Kapcsolat** oldalon kattintson a **Mezőleképezések használata** elemre. 
4. Kattintson az **Új** elemre a **Foglalható erőforrás** entitás **Szabványos munkakör** mezője és az **Időbejegyzés** entitás **Szabványos munkakör** referenciamezője közötti új leképezés létrehozásához. 

> ![Állítsa be az mezőleképezéseket a szabványos munkakör alapértelmezettségének engedélyezéséhez a foglalható erőforrástól az időbejegyzéshez.](media/ST-Mapping2.png)


Ez kiegészíti az entitás alapú egyéni dimenziókhoz szükséges sémaváltozásokat.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Adjon hozzá egyéni mezőket az űrlapokhoz, nézetekhez és üzleti szabályokhoz

Az összes szükséges sémaváltoztatás elvégzése után a következő lépés a mezők láthatóvá tétele a felhasználói felületen, mezők hozzáadásával az űrlapokhoz és a nézetekhez.

1. Nyissa meg az űrlapot vagy a nézetet. A jobb oldali ablaktáblában válassza ki a mezőt, és húzza az űrlap vászonjára. 
2. Nézet szerkesztésekor használja a jobb oldali ablaktáblát, kattintson a **Mezők hozzáadása** elemre, majd a **Mezők listája** párbeszédpanelen válassza ki a szükséges mezőket, és kattintson az **Ok** elemre.

Az alábbi táblázat entitásonként felsorolva, átfogó módon biztosítja azon beépített űrlapokat és nézeteket, amelyeket új mezőkkel kell frissíteni. Ha ezeknek az entitásoknak a testreszabásaiban további nézetek vagy űrlapok vannak, akkor az új mezőket is hozzá kell adni azokhoz.

| Project Service entitás        | Az új mezőt igénylő űrlapok   |Az új mezőt igénylő nézetek      |
| ------------------------------|---------------------------------|----------------------------------|
|  Szerepkörár|• Információ |• Aktív erőforrás kategóriaárak<br> • Erőforrás-kategóriaárhoz kapcsolódó nézet|
|  Szerepkörárrés|• Információ|• Aktív szerepkör felár<br>• Aktív szerepkör felárral kapcsolatos nézet|
|  Árajánlatsor részletei|• Projektinformációk<br>• Projekt Gyors létrehozás|• Aktív ajánlati sor részlete<br>• Kombinált ajánlatsor részletei<br>• Ajánlatsorral kapcsolatos nézet|
|  A projekt szerződés sorának részlete|• Projektinformációk<br>• Projekt Gyors létrehozás|• Kombinált szerződéssorrészletek<br>• Aktív szerződéses sor részletei<br>• Szerződéssor részleteinek társított nézete|
|  Projektfeladat|• Információ<br>• Új űrlap||
|  Projektcsoporttag|• Információ<br>• Új űrlap|• Aktív projektcsapattagok<br>• Projektcsapattagok<br>• A Projektcsapattagokkal társított nézet|
|  Időbejegyzés|• Információ<br>• Időbejegyzés létrehozása|• Saját időbejegyzés dátum szerint<br>• Saját időbejegyzések erre a hétre<br>• Saját időbejegyzések jóváhagyása|
|  Naplósor|• Információ<br>• Gyors létrehozás|• Aktív naplósorok<br>• A Naplósorhoz kapcsolódó nézet|
|  Számlasor részletei|• Információ<br>• Gyors létrehozás|• Aktív számlasor részletei<br>• Díjazható számlatranzakciók<br>• Ingyenes számlatranzakciók<br>• A számlához tartozó sor részletének nézete<br>• Nem díjazható számlatranzakciók|
|  Tény|• Információ<br>• Aktív adatok|• Tényleges társított nézet|

Előfordulhat, hogy az egyéni mezőket hozzá kell adni az üzleti szabályokhoz, attól függően, hogy mit határozott meg. Az egyik out-of-box példa az **Időbejegyzés szerkeszthetősége az állapot alapján** üzleti szabályra vonatkozik. Ez a szabály meghatározza, hogy mely mezőket kell zárolni, ha az Időbejegyzés nem szerkeszthető, például **Jóváhagyott** állapotban. Adjon hozzá mezőket ehhez az üzleti szabályhoz, hogy a mezők zárolva legyenek a szerkesztésre vonatkozóan, ha az Időbejegyzés nem **Vázlat** vagy **Visszaküldött** állapotban van.


[!INCLUDE[footer-include](../includes/footer-banner.md)]