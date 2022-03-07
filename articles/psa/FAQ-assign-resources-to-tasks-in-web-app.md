---
title: Hogyan rendelhető hozzá foglalható erőforrás egy feladathoz a webes alkalmazásban
description: A foglalható erőforrások hozzárendelési módjainak áttekintése.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 25cf017c53d7db23e467b3b610e2990e56e95cb56bdf9820e427dfeeeb979637
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987709"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Hogyan rendelhető hozzá foglalható erőforrás egy feladathoz a webes alkalmazásban (Project Service 2.x alkalmazás)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Két módon lehet hozzárendelni egy erőforrást egy feladathoz a Project Service esetében. Csoporttagként foglahatja le az erőforrást, és hozzárendelheti egy feladathoz. Vagy hozzon létre egy általános csoporttagot a feladatok szerepkör-hozzárendelésén keresztül, hozzon létre egy csoportot, majd teljesítse a mögöttes követelményt egy elnevezett erőforrással.

Megjegyzés: ha szeretne egy lefoglalható erőforrást hozzárendelni egy feladathoz, a foglalható erőforrás-csoport tagjának elegendő foglalással kell rendelkeznie. A foglalás állapotának a következőnek kell lennie: Véglegesítés típusa –Végleges lefoglalás és Állapot – Véglegesített. Nem nincs elegendő foglalás az erőforráshoz, a Project Service eltávolítja a hozzárendelést, és megjeleníti a következő hibaüzenetet:

*Erőforrás hozzárendelése feladathoz sikertelen – A következő erőforrások nem rendelkeznek elegendő lefoglalt órával a projekthez*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Az erőforrás lefoglalása csoporttagként, és az erőforrás hozzárendelése egy feladathoz

Ennél a módszernél a projektcsoporthoz ad egy erőforrást, és feladatokat rendel hozzá az erőforráshoz a projektütemezésben. Ennek módja itt található:
1.  A csoport tagja rácson adjon hozzá egy új csoporttagot a következő kiválasztásával: **Új**.
2.  A csoport tagja gyorslétrehozás képernyőn jelölje ki a foglalható erőforrás nevét, majd állítsa be a szerepkört.
3.  Jelölje ki a **Kezdő** és **Befejező** dátumokat.

    > [!div class="mx-imgBorder"] 
    > ![Egy csapattag hozzáadásának képernyőképe.](media/FAQ-Resources-to-Tasks2-1.png "Egy csapattag hozzáadásának képernyőképe")
 
4.  A következő hozzárendelési módok közül választhat az erőforrás foglalásához:
    - **Teljes kapacitás** – legfoglalja az erőforrás teljes kapacitását a megadott kezdő és záró dátum között.
    - **Százalékos kapacitás** – legfoglalja az erőforrást az erőforrás kapacitásának bizonyos százalékára a megadott kezdő és záró dátum között.
    - **Órák egyenletes elosztásával** – legfoglalja az erőforrást bizonyos mennyiségű órára, amelyeket egyenletesen oszt el naponta a megadott kezdő és záró dátum között.
    - **Órák lefoglalása minél hamarabb** – legfoglalja az erőforrást bizonyos mennyiségű órára, minél gyorsabban felhasználva a napi órákat a megadott kezdő és záró dátum között.

    Ne válassza a **Nincs** lehetőséget, mert az erőforrást hozzáadja a csoporthoz, de nem hoz létre a foglalásokat, amelyek felveszik az erőforrás kapacitását.
5.  Válassza a **Mentés** parancsot.

    Vegye figyelembe, hogy a lefoglalás óráinak elégnek kell lenniük arra, hogy lefedjék a munkaórákat és a dátumtartományokat a feladatokhoz, amelyekhez hozzárendeli az erőforrást. Ha nincsenek összhangban, az erőforrást nem rendelhett a feladathoz.

6.  A feladat munkalebontási struktúráján (WBS) kattintson az erőforrás cella legördülő listájára. Ekkor: 

    1. Válassza a **Hozzáadás** lehetőséget.
    2. Válassza a legördülő listát az **Erőforrások** alatt, és jelölje ki a fenti hozzáadott csoporttagot.
    3. Kattintson az **OK** gombra. A csoport tagja most már hozzá van rendelve a feladathoz.

    > [!div class="mx-imgBorder"] 
    > ![Erőforrások WBS-sel hozzáadásának képernyőképe.](media/FAQ-Resources-to-Tasks2-2.png "Erőforrások WBS-sel hozzáadásának képernyőképe")
 
A csoport tagja rácson megjelenik az erőforrás összesített hozzárendelt óraszáma a Hozzárendelt órák alatt. Az óraszám kisebb vagy egyelnő lesz, mint az erőforrás a lefoglalt óráinak száma. 

> [!div class="mx-imgBorder"] 
> ![Erőforráshoz rendelt munkaórák képernyőképe.](media/FAQ-Resources-to-Tasks2-3.png "Erőforráshoz rendelt munkaórák képernyőképe")
 
Ha az erőforráshoz hozzárendelni kívánt feladat az erőforrás-foglalások záró dátuma után kezdődik, az erőforrás nem jelenik meg a legördülő listában.

Megjegyzés: hozzárendelhet egy erőforrást a lefoglalt óráknál több órához, ha az erőforrás némi fennmaradó nem hozzárendelt kapacitással rendelkezik. Ebben az esetben az erőforrás csak részben lesz hozzárendelve a foglalások maximumáig. Megtekintheti a fennmaradó nem hozzárendelt feladatórákat a Személyzet nélküli órák oszlopot hozzáad a munkalebontási struktúrához.

Ha az erőforrások hozzá vannak rendelve a lefoglalt órák maximumáig (a lefoglat órák száma egyenlő a hozzárendelt órákkal), a következő hibaüzenetet fogja látni, amikor megkísérel további feladatok hozzájuk rendelni:

*Erőforrás hozzárendelése feladathoz sikertelen – A következő erőforrások nem rendelkeznek elegendő lefoglalt órával a projekthez.*

Ezenkívül az alapértelmezett projektvezető csoporttag, aki a a projekt létrehozásakor van hozzáadva a csoporthoz, bármely lefoglalás nélkül van hozzáadva, és nem rendelhető hozzá semmilyen feladathoz. Nem jelenik meg az erőforrás legördülő menüjében a feladatokhoz.

Ha hozzá szeretné rendelni ezt az erőforrást, el kell távolítani a csoportból, és ezután adja hozzá újra egy hozzárendelés módszerrel, amely eltérő a „Nincs”-től. A projekt létrehozásakor azért van hozzáadva a csoporthoz, hogy a projekt legalább egy projektjóváhagyóval rendelkezzen alapértelmezés szerint.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Egy általános csoporttag létrehozása szerepkör-hozzárendeléssel a feladatokon

Ez a módszer biztosítja, hogy az erőforrásoknak elég foglalásuk legyen a feladatokhoz. Első lépésként hozzon létre egy helyőrző vagy általános erőforrást, amely leírja annak az elnevezett erőforrásnak a jellemzőit, akit végső soron a feladaton végzett munkával akar megbízni, egy csoport létrehozásával szerepkörök hozzárendelése után a feladatokhoz. Ennek módja itt található:

1. Jelöljön be egy feladatot a munkalebontási struktúrában.
2. Jelölje ki a **Hozzárendelt szerepkör** legördülő ikont az erőforráscellában.
3. Válassza a **Szerepkör** legördülő listát, és jelölje ki a szerepkört az általános erőforráshoz.
4. Kattintson az **OK** gombra.

    > [!div class="mx-imgBorder"] 
    > ![Képernyőfotó: WBS használata erőforrás hozzáadásához.](media/FAQ-Resources-to-Tasks2-4.png "Képernyőfotó: WBS használata erőforrás hozzáadásához")
 
Miután befejezte a WBS segítségével a szerepkörök hozzárendelését a feladatokhoz, válassza ezt: **Projektcsoport létrehozása**. A Project Service létrehozza a minimális számú általános csoporttagot a szerepkörök alapján, erőforrás-szervezeti egységek és a projektnaptár alapján, a feladat-hozzárendelések összesítésével.

> [!div class="mx-imgBorder"] 
> ![Képernyőfotó: projektcsoport generálása.](media/FAQ-Resources-to-Tasks2-5.png "Képernyőfotó: projektcsoport generálása")
 
A Csoporttag rácsban látni fogja az általános erőforrástípusú erőforrásokat a szerepkör és a pozíció nevével. Ha a munka elvégzéséhez két erőforrás szükséges egy szerepkörhoz, a Csoport létrehozása funkció két csoporttagot hoz létre, és a pozíció neve segítségével különbözteti meg őket.

> [!div class="mx-imgBorder"] 
> ![Képernyőkép: két általános erőforrás hozzáadása.](media/FAQ-Resources-to-Tasks2-6.png "Képernyőkép: két általános erőforrás hozzáadása")
 
Az Erőforrás-követelmény alatt található hivatkozás kiválasztásával megnyithatja az általános csoporttag mögöttes erőforrás-követelményeit.

> [!div class="mx-imgBorder"] 
> ![Képernyőkép: támogató erőforráskövetelmény megnyitása.](media/FAQ-Resources-to-Tasks2-7.png "Képernyőkép: támogató erőforráskövetelmény megnyitása")

Jelölje be a **Foglalás** elemet az általános erőforráshoz, és aztán az ütemezési tábla használatával kereshet és foglalhat le egy tényleges erőforrást. A **Kérelem küldése** kiválasztásával el is küldheti a követelményt egy erőforrás-menedzser általi teljesítésre.

Ha az általános erőforrás teljesítése elnevezett erőforrással történik, az általános erőforrás törlődik a csoportból, és az általános erőforrás feladat-hozzárendelései az elnevezett erőforráshoz lesznek rendelve, aki végrehajtotta az általán erőforrás erőforrás-követelményét.
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]