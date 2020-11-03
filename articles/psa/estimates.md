---
title: Becslések
description: Ez a témakör információkat nyújt becslésekről a Dynamics 365 Project Service Automation rendszerben.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e21511f78d92ff672e462f63f0dd0d098578516a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078294"
---
# <a name="estimates"></a>Becslések

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektalapú árajánlatok esetén az Ajánlat sor részleteit felhasználva becsülheti meg a projekt végrehajtásához szükséges munkát. Ezután megoszthatja ezt a becslést az ügyféllel.

A projektalapú árajánlati soroknak nem kell tartalmazniuk árajánlati sorok részleteit. Alternatív megoldásként sok árajánlati sorrészletet is tartalmazhatnak. Az árajánlati részleteit az idő, a költségek vagy a díjak becslésére használják. A PSA nem engedélyezi az árajánlati sor részleteiben az anyagok becslését. Ezeket tranzakciós osztályoknak nevezzük. A becsült adóösszegek tranzakciós osztályba is felvihetők.

A tranzakciós osztályokon kívül az ajánlati sorok részletei tranzakciótípust is tartalmaznak. A PSA két tranzakciótípust támogat az árajánlati sorok részleteihez: **Költség** és **Projektszerződés**.

## <a name="estimate-by-using-a-contract"></a>Becslés szerződés felhasználásával

Ha PSA-ajánlatot használt egy projektalapú szerződés létrehozásakor, akkor a becslések, amelyeket az egyes ajánlati sorokra megtett, a projektszerződésbe másolódnak. A projektszerződés felépítése olyan, mint a projektajánlat szerkezete, amely sorokat, sorrészleteket és számla ütemezéseket tartalmaz.

A becsléseket közvetlenül egy projektszerződésben lehet elvégezni, akárcsak a projektajánlatban. A projekt árajánlatához a becslést szerződési sorok és a szerződéssor-részletek felhasználásával kell elvégezni. A szerződési sorok részleteit az alulról felfelé becslési megközelítés alkalmazásával létrehozott projekttervből is elő lehet állítani.

A szerződési sorok részletei felhasználhatók az idő, a költségek vagy a díjak becslésére. A becsült adóösszegek a szerződési sorok részleteiben is megadhatók.

A PSA nem engedélyezi a szerződési sorok részleteiben az anyagok becsléseit.

A projektszerződésben támogatott folyamatok a számlalétrehozás és -megerősítés. A számla létrehozása létrehozza a projektalapú számla tervezetét, amely tartalmazza az összes érvénytelenített értékesítési tényt az aktuális dátumig.

A megerősítés a szerződést csak olvashatóvá teszi, és állapotát **Vázlat** -ról **Megerősített** -re változtatja. A művelet elvégzése után azt nem vonhatja vissza. Mivel ez a művelet állandó, a bevált gyakorlat a szerződés **Vázlat** állapotban tartása.

Az egyetlen különbség a szerződéstervezetek és a megerősített szerződések között az állapotuk és az a tény, hogy a szerződéstervezetek szerkeszthetők, míg a megerősített szerződések nem. A számlakészítés és a tényleges adatok követése mind a szerződéstervezeteken, mind a megerősített szerződéseken elvégezhető.

A PSA nem támogatja a szerződések vagy projektek megváltoztatására vonatkozó megrendeléseket.

## <a name="estimating-projects"></a>A projektek becslése

Becsülhetők a projektek ideje és költségei. A PSA nem engedélyezi a projektekben az anyagok vagy díjak becslését.

Az időbecslések akkor jönnek létre, amikor létrehoz egy feladatot, és azonosítja a feladat végrehajtásához szükséges általános erőforrás attribútumait. Az időbecsléseket az ütemezési feladatokból generálják. Az időbecslések nem kerülnek létrehozásra, ha általános csoporttagokat hoznak létre az ütemterv keretein kívül.

A költségbecsléseket a rácsba kell beírni a **Becslések** oldalon.

## <a name="understanding-estimation"></a>A becslés megértése

Az alábbi táblázatot használhatja útmutatóként az üzleti logika megértéséhez a becslési szakaszban.

| Forgatókönyv                                                                                                                                                                                                                                                                                                                                          | Entitásrekord                                                                                                                                                                                                       | Tranzakció típusa | Tranzakcióosztály | További információk                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Ha meg kell becsülnie az idő eladási értékét egy árajánlaton                                                                                                                                                                                                                                                                                    | Létrehozásra kerül az ajánlatsor-részlet (QLD) rekord                                                                                                                                                                               | Projektszerződés | Time        | A tranzakció származási mezője az eladási oldal QLD sorában a költségoldali QLD-re hivatkozik |
|                                                                                                                                                                                                                                                                                     | A rendszer létrehoz egy második QLD rekordot a megfelelő költségértékek tárolására. Az összes nem pénzbeli mezőt a rendszer az eladási QLD-ről a Költség QLD-re másolja.                                                                                                                                                                               | Költség | Time        | A tranzakció származási mezője az eladási oldalon található ajánlatsor-részlet (QLD) sorában a Költségoldali QLD-re hivatkozik |
| Ha meg kell becsülnie az idő eladási értékét egy szerződésben                                                                                                                                                                                                                                                                                 | Létrehozásra kerül a szerződéssor-részlet (CLD) rekord                                                                                                                                                                    | Projektszerződés | Time        | A tranzakció származási mezője az eladási oldal CLD sorában a költségoldali CLD-re hivatkozik      |
|                                                                                                                                                                                                                                                                                  | A rendszer létrehoz egy második CLD rekordot a megfelelő költségértékek tárolására. Az összes nem pénzbeli mezőt a rendszer az eladási CLD-ről a Költség CLD-re másolja.                                                                                                                                                                    | Költség | Time        | A tranzakció származási mezője az eladási oldal CLD sorában a költségoldali CLD-re hivatkozik      |
| Amikor a felhasználó leír egy erőforrást egy projektfeladatban                                                                                                                                                                                                                                                                                            | A feladat eladási értékét bemutató becsült sorrekord akkor jön létre, amikor egy feladatot létrehoznak az összes szükséges árazási dimenzióval. A szerepkörök és a szervezeti egységek az OOB Project Service árazási dimenziói | Projektszerződés | Time        |                                                                                   |
|     | A feladat költségértékét bemutató becsült sorrekord akkor jön létre, amikor egy feladatot létrehoznak az összes szükséges árazási dimenzióval. Az összes nem pénzbeli mezőt a rendszer az eladási becsült sorról a költség becsült sorra másolja. A szerepkör és a szervezeti egység az OOB PSA árazási dimenziója mind a költségek, mind a számlák árainak tekintetében.                                                                                                                                                                                                                | Költség             | Time           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Az Idézet sorrészleteinek és a Szerződés sorrészleteinek testreszabása

Ha hozzáadott egy egyéni mezőt az árajánlat sorrészleteihez, és azt akarja, hogy a rendszer a mező értékét alapértelmezett értékként adja meg a létrehozott kapcsolódó költségsoron, akkor használja a PreOperationContractLineDetailUpdate és PreOperationQuoteLineDetailUpdate beépülő regisztrációs eszközöket. Ezeket a beépülő modulokat újra kell regisztrálni, ha az árajánlati sorrészleteket vagy a szerződéses sorrészleteket megváltoztatták. A folyamat befejezéséhez kövesse ezeket a lépéseket.

1. Nyissa meg a PluginRegistrationTool eszközt, és csatlakozzon az online példányhoz.
2. Válassza a **Keresés** lehetőséget, és keresse meg a frissítést igénylő bővítményt.

    ![Keresési fa párbeszédpanel](media/basic-guide-19.png)

3. Válassza ki a beépülő modult, majd a főoldalon válassza a **Kiválasztás** lehetőséget.
4. Válassza ki a beépülő modul frissítésének lépését, kattintson a jobb gombbal, majd válassza a **Frissítés** lehetőséget.

    ![Egy lépés kiválasztása a beépülő modulban](media/basic-guide-20.png)

5. A **Meglévő lépés frissítése** párbeszédpanelen a **Szűrési attribútumok** mezőben válassza az ellipszis ( **...** ) gombot:
 
    ![A Meglévő lépés párbeszédpanel frissítése](media/basic-guide-21.png)

6. Az **Attribútumok kiválasztása** párbeszédpanelen jelölje be az egyedi attribútumok jelölőnégyzeteit.

    ![Az Attribútumok párbeszédpanel kiválasztása](media/basic-guide-22.png)

7. A párbeszédpanel bezárásához válassza az **OK** lehetőséget, majd válassza a **Lépés frissítése** lehetőséget.
 
    ![Lépés frissítése gomb](media/basic-guide-23.png)

8. Ismételje meg az 1-7. lépéseket a második modullal.
9. Zárja be a PluginRegistrationTool eszközt.
