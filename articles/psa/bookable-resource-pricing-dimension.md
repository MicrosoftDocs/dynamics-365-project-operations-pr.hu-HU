---
title: Foglalható erőforrás használata árazási dimenzióként
description: Ez a témakör a foglalható erőforrások árazási dimenzióként való használatáról tartalmaz tájékoztatást.
author: Rumant
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
ms.openlocfilehash: 8a5c643745d8e10887965228da7abd8f56228006
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078191"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Foglalható erőforrás használata árazási dimenzióként
Ez a témakör a foglalható erőforrások árazási dimenzióként való használatáról tartalmaz tájékoztatást. Mielőtt elkezdené, ha még nem hozott létre árképzési megoldást, akkor létre kell hoznia egy újat. Ha már van árképzési dimenziós megoldása, akkor megváltoztathatja azt. Ha még nem hozott létre új árképzési dimenziós megoldást a szervezetének, akkor hajtsa végre az [Egyéni mezők és entitások létrehozása](create-custom-fields-entities.md) témakörben szereplő eljárásokat.

## <a name="add-bookable-resource-to-forms-and-views"></a>Foglalható erőforrás hozzáadása az űrlapokhoz és a nézetekhez
Ha az árazási dimenzió megoldás felhasználói felületén láthatóvá szeretné tenni a mezőket, akkor végig kell haladnia a főbb Project Service entitások összes űrlapján és nézetén, és fel kell vennie ezeket a mezőket az entitások űrlapjaira és nézeteire.
Az alábbi táblázat átfogó entitások szerint felsorolja azon beépített űrlapokat és nézeteket, amelyeket frissíteni kell. Ha további nézetek vagy űrlapok szerepelnek az entitásokra vonatkozó testreszabásokban, akkor az új mezőket is vegye fel hozzájuk.
Nyissa meg a Megoldáskezelő alkalmazást az árképzési dimenzió megoldáshoz, majd kattintson a **Minden testreszabás közzététele** lehetőségre.


|   Entitás        | Űrlapok   |Nézetek        |
| ------------------------------|---------------------------------|----------------------------------|
|  Szerepkörár|• Információ |• Aktív erőforrás kategóriaárak<br> • Erőforrás-kategóriaárhoz kapcsolódó nézet|
|  Szerepkörárrés|• Információ|• Aktív szerepkör felár<br>• Aktív szerepkör felárral kapcsolatos nézet|
|  Árajánlatsor részletei|• Projektinformációk<br>• Projekt Gyors létrehozás|• Aktív ajánlati sor részlete<br>• Kombinált ajánlatsor részletei<br>• Ajánlatsorral kapcsolatos nézet|
|  A projekt szerződés sorának részlete|• Projektinformációk<br>• Projekt Gyors létrehozás|• Kombinált szerződés sor részletei<br>• Aktív szerződéses sor részletei<br>• A szerződéses sor részletekkel társított nézet|
|  Projektfeladat|• Információ<br>• Új űrlap||
|  Projektcsoporttag|• Információ<br>• Új űrlap|• Aktív projektcsapattagok<br>• Projektcsapattagok<br>• A Projektcsapattagokkal társított nézet|
|  Időbejegyzés|• Információ<br>• Időbejegyzés létrehozása|• Saját időbejegyzés dátum szerint<br>• Saját időbejegyzések erre a hétre<br>• Saját időbejegyzések jóváhagyása|
|  Naplósor|• Információ<br>• Gyors létrehozás|• Aktív naplósorok<br>• A Naplósorhoz kapcsolódó nézet|
|  Számlasor részletei|• Információ<br>• Gyors létrehozás|• Aktív számlasor részletei<br>• Díjazható számlatranzakciók<br>• Ingyenes számlatranzakciók<br>• A számlához tartozó sor részletének nézete<br>• Nem díjazható számlatranzakciók|
|  Tény|• Információ<br>• Aktív adatok|• Tényleges társított nézet|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Foglalható erőforrás beállítása árazási dimenzióként

1. A webes felületen lépjen a **Project Service** > **Beállítások** > **Paraméterek** oldalra. A **Paraméter** oldal **Mennyiségalapú árazási dimenziók** lapján láthatja, hogy a lapon lévő rács az árazási dimenziók entitásban található bejegyzéseket jeleníti meg. 
2. Adja hozzá a **Foglalható erőforrás** elemet az árázi dimenziók listájához **msdyn_bookableresource** elemként. 
3. Jelölje meg a környezetet, amelyben a foglalható erőforrás árazási dimenzióként működik, és állítsa be a **Költségre alkalmazható** és az **Értékesítésre alkalmazható** értékeket.
4. A **Dimenzió típusa** mezőben válassza a **Mennyiségalapú** lehetőséget. 
5. Válassza ki a foglalható erőforrás költség- és értékesítési prioritását. Rendszerint, ha árazási dimenzióként kerül alkalmazásra, a foglalható erőforrás a legmagasabb prioritással rendelkezik, így ennek **1** -re (vagy **0** -ra, a prioritás számolásának módjától függően) állítsa garantálja azt a viselkedést.

## <a name="set-up-pricing-dimension-field-names"></a>Az árazási dimenziók mezőneveinek beállítása

Ha egy árazási dimenzió mezőneve a **Szerepkör** táblázatban eltér bármely olyan entitásban lévő mezőnevétől, ahol az ár nemteljesítésnek dolgoznia kell, az árazási dimenzió bejegyzésének értesülnie kell az eltérő nevekről.    
Foglalható erőforrás esetén, a **Projektcsoport tagjai** entitás mezőneve ( **msdyn_bookableresourceid** ) némileg eltér attól, ahogy a **Szerepkör ára** entitáson ( **msdyn_bookableresource** ) szerepel. Az **msydn_bookableresource** árazási dimenzió bejegyzését erről értesíteni kell. 
1. Ehhez kattintson duplán az **Árazási dimenziók** rácsban található sorra; ekkor megnyílik az **msdyn_bookableresource** dimenzió oldala.
2. A dimenzió oldalán a **Kapcsolódó** lapon kattintson az **Árdimenziók mezőnevei** lehetőségre.

 ![Árdimenziók mezőnevei lap](media/PD-fieldname.png)

4. A megnyíló kapcsolódó nézeten kattintson az **Új árdimenzió mezőnév hozzáadása** lehetőségre.

 ![Új árdimenzió mezőnevek hozzáadása](media/Add-NewPD-fieldname.png)


Ez megnyitja az **msdyn_bookableresource** elem **Új árdimenzió mezőnév** lapját. 

5. Adja hozzá az **msdyn_projectteam** elemet az **Entitás logikai neve** mezőhöz és az **msdyn_bookableresourceid** elemet a **Mezőnév** mezőhöz. Mentse a bejegyzést.

 ![Új árdimenzió mezőnév űrlap](media/PD-fieldname-Added.png)
