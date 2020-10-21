---
title: Becslésprojektek áttekintése
description: Ez a témakör a Dynamics 365 Project Operations becsléseiről nyújt információkat.
author: ruhercul
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8e7ee4888a907b9d8c3ce06c1597f6b05be84477
ms.sourcegitcommit: 6eb26bab511ec09201ab70c3e2808dece3f74c4c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/07/2020
ms.locfileid: "3968046"
---
# <a name="estimate-projects-overview"></a>Becslésprojektek áttekintése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Projektalapú árajánlatok esetén az **Ajánlat sor részletei** entitással becsülheti meg a projekt végrehajtásához szükséges munkát. Ezután megoszthatja ezt a becslést az ügyféllel.

A projektalapú árajánlati soroknak nem feltétlenül kell árajánlati sorok részleteit tartalmaznia, de sok ilyen részletet is tartalmazhatnak. Az árajánlati részleteit az idő, a költségek vagy a díjak becslésére használják. A Microsoft Dynamics 365 Project Operations az árajánlatsor részleteiben nem engedélyezi az anyagok becslését. Ezeket tranzakciós osztályoknak nevezzük. A becsült adóösszegek tranzakciós osztályba is felvihetők.

A tranzakciós osztályokon kívül az ajánlati sorok részletei tranzakciótípust is tartalmaznak. Az árajánlatsorok részleteihez két tranzakciótípus támogatott: a **Költség** és a **Projektszerződés**.

## <a name="estimate-by-using-a-contract"></a>Becslés szerződés felhasználásával

Ha árajánlatot használt egy projektalapú szerződés létrehozásakor, akkor a becslések, amelyeket az egyes ajánlatsorokra tett, a projektszerződésbe másolódnak. A projektszerződés felépítése olyan, mint a projektajánlat szerkezete, amely sorokat, sorrészleteket és számla ütemezéseket tartalmaz.

A becsléseket közvetlenül egy projektszerződésben lehet elvégezni, akárcsak a projektajánlatban. A projekt árajánlatához a becslést szerződési sorok és a szerződéssor-részletek felhasználásával kell elvégezni. A szerződési sorok részleteit az alulról felfelé becslési megközelítés alkalmazásával létrehozott projekttervből is elő lehet állítani.

A szerződési sorok részletei felhasználhatók az idő, a költségek vagy a díjak becslésére. A becsült adóösszegek a szerződési sorok részleteiben is megadhatók.

A szerződési sorok részleteiben nem szerepelhetnek anyagok becslései.

A projektszerződésben támogatott folyamatok a számlalétrehozás és -megerősítés. A számla létrehozása létrehozza a projektalapú számla tervezetét, amely tartalmazza az összes érvénytelenített értékesítési tényt az aktuális dátumig.

A megerősítés a szerződést csak olvashatóvá teszi, és állapotát **Vázlat**-ról **Megerősített**-re változtatja. A művelet elvégzése után azt nem vonhatja vissza. Mivel ez a művelet állandó, a bevált gyakorlat a szerződés **Vázlat** állapotban tartása.

Az egyetlen különbség a szerződéstervezetek és a megerősített szerződések között az állapotuk és az a tény, hogy a szerződéstervezetek szerkeszthetők, míg a megerősített szerződések nem. A számlakészítés és a tényleges adatok követése mind a szerződéstervezeteken, mind a megerősített szerződéseken elvégezhető.

A Project Operations nem támogatja a szerződések vagy projektek megváltoztatására vonatkozó megrendeléseket.

## <a name="estimating-projects"></a>A projektek becslése

Becsülhetők a projektek ideje és költségei. A Project operations nem engedélyezi a projektekben az anyagok vagy díjak becslését.

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
| Amikor a felhasználó leír egy erőforrást egy projektfeladatban                                                                                                                                                                                                                                                                                            | A feladat eladási értékét bemutató becsült sorrekord akkor jön létre, amikor egy feladatot létrehoznak az összes szükséges árazási dimenzióval. Az árképzési dimenziók a szerepkörök és a szervezeti egységek | Projektszerződés | Időpont        |                                                                                   |
|     | A feladat költségértékét bemutató becsült sorrekord akkor jön létre, amikor egy feladatot létrehoznak az összes szükséges árazási dimenzióval. Az összes nem pénzbeli mezőt a rendszer az eladási becsült sorról a költség becsült sorra másolja. Mind a költségek, mind a számlázási díjak esetében a szerepkör és a szervezeti egység az árképzési dimenzió.                                                                                                                                                                                                                | Költség             | Időpont           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Az Árajánlat sorrészleteinek és a Szerződéssor részleteinek testreszabása

Ha egyéni mezőt adott az árajánlatsor részleteihez, és azt akarja, hogy a rendszer a mező értékét adja meg alapértelmezett értékként a létrehozott kapcsolódó költségsoron, akkor használja a **PreOperationContractLineDetailUpdate** és a **PreOperationQuoteLineDetailUpdate** beépülő regisztrációs eszközöket. Ezeket a beépülő modulokat újra kell regisztrálni, ha az árajánlati sorrészleteket vagy a szerződéses sorrészleteket megváltoztatták. A folyamat befejezéséhez kövesse ezeket a lépéseket.

1. Nyissa meg a PluginRegistrationTool eszközt, és csatlakozzon az online példányhoz.
2. Válassza a **Keresés** lehetőséget, és keresse meg a frissítést igénylő bővítményt.
3. Válassza ki a beépülő modult, majd a főoldalon kattintson a **Kiválasztás** elemre.
4. Válassza ki a beépülő modul frissítésének lépését, kattintson a jobb gombbal, majd válassza a **Frissítés** lehetőséget.
5. A **Meglévő lépés frissítése** párbeszédpanelen a **Szűrési attribútumok** mezőben válassza az ellipszis (**...**) gombot:
6. Az **Attribútumok kiválasztása** párbeszédpanelen jelölje be az egyedi attribútumok jelölőnégyzeteit.
7. A párbeszédpanel bezárásához válassza az **OK** lehetőséget, majd válassza a **Lépés frissítése** lehetőséget.
8. Ismételje meg az 1-7. lépéseket a második modullal.
9. Zárja be a **PluginRegistrationTool** eszközt.
