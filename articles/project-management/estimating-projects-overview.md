---
title: Pénzügyi becslésekre vonatkozó fogalmak
description: Ez a cikk a Project Operations projektjeinek pénzügyi becsléseiről nyújt tájékoztatást.
author: rumant
ms.date: 03/22/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f8a4c3dd31cf5612c352331891178ac0ab852921
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931011"
---
# <a name="financial-estimation-concepts"></a>Pénzügyi becslésekre vonatkozó fogalmak

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations szolgáltatásban pénzügyileg két szakaszban becsülheti meg a projekteket: 
1. Az értékesítés előtti szakaszban, mielőtt az üzletet megnyerik. 
2. A projektszerződés létrejöttét követő végrehajtási szakaszban. 

A projektalapú munkához pénzügyi becslést hozhat létre az alábbi 3 oldal bármelyikével:
- Az **Árajánlatsor** lap az árajánlatsor részleteivel.  
- A **Projekt árajánlatsor** lap a szerződéssor részleteivel. 
- A **Projekt** lap, a **Feladatok** vagy **Költségbecslések** fül lapok használatával.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Projektárajánlat használata becslés létrehozásához
Projektalapú árajánlatok esetén az **Ajánlat sor részletei** entitással becsülheti meg a projekt végrehajtásához szükséges munkát. Ezután megoszthatja ezt a becslést az ügyféllel.

A projektalapú árajánlati soroknak nem feltétlenül kell árajánlati sorok részleteit tartalmaznia, de sok ilyen részletet is tartalmazhatnak. Az árajánlati részleteit az idő, a költségek vagy a díjak becslésére használják. A Microsoft Dynamics 365 Project Operations nem engedélyezi az árajánlati sor részleteiben az anyagok becslését. Ezeket tranzakciós osztályoknak nevezzük. A becsült adóösszegek tranzakciós osztályba is felvihetők.

A tranzakciós osztályokon kívül az ajánlati sorok részletei tranzakciótípust is tartalmaznak. Az árajánlatsorok részleteihez két tranzakciótípus támogatott: a **Költség** és a **Projektszerződés**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Projektszerződés használata becslés létrehozásához

Ha árajánlatot használt egy projektalapú szerződés létrehozásakor, akkor a becslések, amelyeket az egyes ajánlatsorokra tett, a projektszerződésbe másolódnak. A projektszerződés felépítése olyan, mint a projektajánlat szerkezete, amely sorokat, sorrészleteket és számla ütemezéseket tartalmaz.

A becsléseket közvetlenül egy projektszerződésben lehet elvégezni, akárcsak a projektajánlatban. A projekt árajánlatához a becslést szerződési sorok és a szerződéssor-részletek felhasználásával kell elvégezni. A szerződési sorok részleteit az alulról felfelé becslési megközelítés alkalmazásával létrehozott projekttervből is elő lehet állítani.

A szerződési sorok részletei felhasználhatók az idő, a költségek vagy a díjak becslésére. A becsült adóösszegek a szerződési sorok részleteiben is megadhatók.

A szerződési sorok részleteiben nem szerepelhetnek anyagok becslései.

## <a name="use-a-project-to-create-an-estimate"></a>Projekt használata becslés létrehozásához 

Becsülhetők a projektek ideje és költségei. A Project Operations nem támogatja a projektek anyagbecslését vagy díjait.

Az időbecslések akkor jönnek létre, amikor létrehoz egy feladatot, és azonosítja a feladat végrehajtásához szükséges általános erőforrás attribútumait. Az időbecsléseket az ütemezési feladatokból generálják. Az időbecslések nem kerülnek létrehozásra, ha általános csoporttagokat hoznak létre az ütemterv keretein kívül.

A költségbecsléseket a rácsba kell beírni a **Költségbecslések** oldalon.

A projekt becslésének létrehozása bevált gyakorlatnak minősül, mivel alulról felfelé építkezve részletes becsléseket lehet építeni a projektterv egyes feladataira vonatkozó munka-, idő- és költségbecslések alapján. Ezt a részletes becslést felhasználva becsléseket hozhat létre az egyes árajánlatsorokhoz, és hitelesebb árajánlatot hozhat létre az ügyfél számára. Amikor a projektterv használatával importál vagy hoz létre részletes becslést az árajánlatsoron, a Project Operations importálja ezeknek a becsléseknek az értékesítéso értékeit és költségértékeit. Az importálás után megtekintheti a projektárajánlat jövedelmezőségét, árrését és megvalósíthatósági metrikáit.

## <a name="understanding-estimates"></a>A becslések megértése

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
