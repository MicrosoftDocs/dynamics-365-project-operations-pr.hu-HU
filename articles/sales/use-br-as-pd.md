---
title: Foglalható erőforrás használata árképzési dimenzióként
description: Ez a témakör a foglalható erőforrások árazási dimenzióként való használatának módjáról tartalmaz tájékoztatást.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dcd01d80236f0218bc6fa3a1fe1389f8314f3c9b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598630"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Foglalható erőforrás használata árképzési dimenzióként

 _**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_ 

Ez a témakör a foglalható erőforrások árazási dimenzióként való használatának módjáról tartalmaz tájékoztatást. Ha az árképzési stratégiája úgy van beállítva, hogy minden egyes foglalt erőforrásnak külön ára vagy önköltségi ára legyen, akkor használja a lefoglalható erőforrást árazási dimenzióként.

## <a name="prerequisites"></a>Előfeltételek
Az ebben a témakörben található az eljárások befejezése előtt egy új árképzési dimenzió megoldással kell rendelkeznie a szervezet számára. Ha még nem hozott létre ilyet, olvassa el az [Egyéni mezők és entitások létrehozása című témakört](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Foglalható erőforrás mező hozzáadása az űrlapokhoz és a nézetekhez
Ha azt szeretné , hogy a **Foglalható erőforrás** mező látható legyen az árképzési dimenzió megoldásban, akkor az összes űrlaphoz és nézethez hozzá kell adnia a mezőt entitásként.

Az alábbi táblázat entitásonként sorolja fel az összes előre telepített űrlapot és nézetet. Az új mezőt hozzá kell adnia a testreszabott entitások további űrlapjaihoz vagy nézeteihez is.

|   Entity        | Űrlapok   |Nézetek        |
| ------------------------------|---------------------------------|----------------------------------|
|  Szerepkörár| Tájékoztatás | - Erőforrás-kategória aktív árai<br> - Erőforrás-kategória ára társítva |
|  Szerepkörárrés| Tájékoztatás| - Aktív szerepkörárrés<br>- Szerepkörárrés társítva |
|  Árajánlatsor részletei| - Projektinformáció<br>- Projekt gyorslétrehozása| - Aktív árajánlatsor-részlet<br>- Kombinált árajánlatsor részletei<br>- Árajánlatsor-részlet társított nézete |
|  A projekt szerződés sorának részlete| - Projektinformáció<br>- Projekt gyorslétrehozása| - Kombinált szerződéssorrészletek<br>- Aktív szerződéssorrészletek<br>- Társított szerződéssor-részletek |
|  Projektfeladat| - Tájékoztatás<br>- Új űrlap| &nbsp; |
|  Projektcsoporttag| - Tájékoztatás<br>- Új űrlap| - Aktív projektcsoporttagok<br>- Projektcsoporttagok<br>- Projektcsoporttagok társítva |
|  Időbejegyzés| - Tájékoztatás<br>- Időbejegyzés létrehozása| - Saját időbejegyzések dátum szerint<br>- Saját időbejegyzések ezen a héten<br>- Jóváhagyandó időbejegyzések|
|  Naplósor| - Tájékoztatás<br>- Gyorslétrehozás| - Aktív naplósorok<br>- Naplósor társított nézete |
|  Számlasor részletei| - Tájékoztatás<br>- Gyorslétrehozás| - Aktív számlasorrészlet<br>- Számlázható számlatranzakciók<br>- Kiegészítő számlatranzakciók<br>- Társított számlasorrészlet <br>- Nem díjazható számlatranzakciók|
|  Tényadat| - Tájékoztatás<br>- Aktív tényleges adatok| Tényleges adatok társítva |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Foglalható erőforrás beállítása árazási dimenzióként
Foglalható erőforrás beállításához árazási dimenzióként kövesse az alábbi lépéseket:

1. Válassza a **Beállítások** > **Paraméterek** lehetőséget. 
2. A **Paraméter** oldal **Mennyiségalapú árazási dimenziók** fülén ellenőrizze, hogy a fülön található rács az **Árazási dimenzió** entitás bejegyzéseit mutatja. 
2. Adja hozzá a **Foglalható erőforrás** elemet az árázi dimenziók listájához **msdyn_bookableresource** elemként. 
3. A **Költségre érvényes** és az **Értékesítésre érvényes** helyeken válasszon egy értéket.
4. A **Dimenzió típusa** alatt válassza a **Mennyiségalapú** lehetőséget. 
5. Válassza ki a foglalható erőforrás költség- és értékesítési prioritását. A lefoglalható erőforrások általában a legmagasabb prioritást jelentik, amikor árazási dimenzióként szerepelnek. Állítsa be a prioritást **1** (vagy **0** értékre, attól függően, hogyan számítja ki a prioritást) a viselkedés biztosításához.

## <a name="set-up-pricing-dimension-field-names"></a>Az árazási dimenziók mezőneveinek beállítása

Ha egy árazási dimenzió mezőneve a **Szerepkör** táblázatban eltér bármely olyan entitásban lévő mezőnevétől, ahol az alapértlemezett árvan használva , az árazási dimenzió bejegyzésének értesülnie kell az eltérő nevekről.  

Foglalható erőforrás esetén, a **Projektcsoport tagjai** entitás mezőneve (msdyn_bookableresourceid) némileg eltér attól, ahogy a **Szerepkör ára** entitáson szerepel: 

 - **Projektcsapat tagjai** entitás = **msdyn_bookableresourceid**
 - **Szerepkör ára** entitás = **msdyn_bookableresource**

Az **msydn_bookableresource** árazási dimenzió bejegyzését erről a különbségről értesíteni kell.

1. Kattintson duplán az **Árazási dimenziók** rácsban található sorra; ekkor megnyílik az **msdyn_bookableresource** dimenzió oldala.
2. A dimenzió oldalán a **Kapcsolódó** lapon válassza az **Árdimenziók mezőnevei** lehetőséget.

  ![Árdimenziók mezőnevei lap.](media/PD-fieldname.png)

3. A megnyíló kapcsolódó nézeten válassza az **Új árdimenzió mezőnév hozzáadása** lehetőséget.

  ![Új árdimenzió mezőnevek hozzáadása.](media/Add-NewPD-fieldname.png)

  Ez megnyitja az **msdyn_bookableresource** elem **Új árdimenzió mezőnév** lapját. 

4. Az **Új árazási dimenzió mező neve** oldalon adja hozzá **msdyn_projectteam** elemet az **Entitás logikai neve** elemhez.
5. Az **msdyn_bookableresourceid** hozzáadása a **Mező neve** elemhez.

 ![Új árdimenzió mezőnév űrlap.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]