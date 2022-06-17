---
title: Erőforrás hozzárendelése egy feladathoz
description: Ez a cikk az erőforrások tevékenységekhez való hozzárendelésével kapcsolatos információkat tartalmaz.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: dae5a81c51f34b9115ac8c267452b167a6d7bef8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913485"
---
# <a name="assign-a-resource-to-a-task"></a>Erőforrás hozzárendelése egy feladathoz

[!include [banner](../includes/psa-now-project-operations.md)]

Három módon lehet erőforrásokat hozzárendelni egy feladathoz a Microsoft Dynamics 365 Project Service Automation felületén.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Foglalja le az erőforrást csapattagként, majd rendelje hozzá az erőforrást egy feladathoz.

Felvehet erőforrást a projektcsapatba, majd hozzárendelheti az erőforrást a projekt ütemezésében szereplő feladatokhoz.

1. A **Csapattag** lapon vegyen fel új csapattagot az **Új** lehetőség kiválasztásával. 

2. Megnyílik a **Csapattagok gyors létrehozása** panel, ahol kiválaszthatja a foglalható erőforrás nevét, és beállíthat egy szerepkört. 

    Válassza ki az alábbi beosztási módszerek egyikét az erőforrás lefoglalására:

    - **Teljes kapacitás** – legfoglalja az erőforrás teljes kapacitását a megadott kezdő és záró dátum között.
    - **Százalékos kapacitás** – legfoglalja az erőforrást az erőforrás kapacitásának bizonyos százalékára a megadott kezdő és záró dátum között.
    - Az **Egyenlően elosztott órák alapján** módszer az erőforrást meghatározott óraszámban foglalja le napi szinten a megadott kezdő és befejező dátum között.
    - **Órák lefoglalása minél hamarabb** – legfoglalja az erőforrást bizonyos mennyiségű órára, minél gyorsabban felhasználva a napi órákat a megadott kezdő és záró dátum között.
    - **Nincs** – hozzáadja az erőforrást a csoporthoz, de nem hoz létre a foglalásokat, amelyek felveszik az erőforrás kapacitását.

3. A feladat **Ütemezés** rácsán válassza az **Erőforrás** ikont az erőforrás cellájában, majd a **Csapattagok** részen válassza ki az éppen hozzáadott csapattagot. 

> [!NOTE]
> A **Csapattag** és az **Egyeztetés** lapon az erőforrás megmutatja a lefoglalt és a hozzárendelt órákat. Az óráknak azonosnak kell lenniük, de ez nem követelmény, mivel a foglalások és a hozzárendelések nincsenek szorosan összekapcsolva. Az **Egyeztetés** lapon információkat kaphat róluk, ha különböznek, például amikor több órát rendel hozzá egy erőforráshoz, mint amennyit lefoglalt. Szükség esetén helyesbítheti az információkat az erőforrás foglalásainak kibővítésével vagy a hozzárendelés megváltoztatásával.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Általános csapattag létrehozása feladat-hozzárendeléssel

Amikor egy általános csapattagot feladat-hozzárendeléssel hoz létre, akkor létrehoz egy helyőrzőt vagy általános erőforrást, amely leírja annak a megnevezett erőforrásnak a tulajdonságait, amelyet végül a feladatok elvégzéséhez kíván használni. Ezután előállít egy követelményt (vagy kérést nyújt be a követelmény alapján), amely a megnevezett erőforrás keresésére és lefoglalására használható.

1. A feladat **Ütemezés** rácsán válassza az **Erőforrás** ikont az erőforrás cellájában.

2. Gépelje be a helyőrző erőforrásának nevét. Például: Programkezelő.

3. Válassza a **Létrehozás** lehetőséget, majd a **Gyors létrehozás: Projektcsapattag** mezőben adja meg az általános erőforrás szerepkörét.

4. Folytathatja a feladatok hozzárendelését e helyőrző erőforrásához, ha az **Erőforrásválasztóban** kiválasztja az erőforrást a feladathoz. Az erőforrások a **Csapattagok** területen vannak felsorolva.

5. Ha befejezte az általános erőforrás hozzárendelését, válassza ki az általános erőforrást a **Csapat** lapon, majd válassza a **Követelmény generálása** lehetőséget az általános erőforrás erőforrásigényének létrehozásához.

6. Válassza a **Foglalás** lehetőséget az általános erőforráshoz. Ezután az Ütemezés táblát használhatja valódi erőforrások megkereséséhez és lefoglalásához. El is küldheti a követelményt egy erőforrás-menedzser általi teljesítésre.

7. Ha az általános erőforrás teljesítése elnevezett erőforrással történik, az általános erőforrás törlődik a csoportból, és az általános erőforrás feladat-hozzárendelései az elnevezett erőforráshoz lesznek rendelve, aki végrehajtotta az általán erőforrás erőforrás-követelményét.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Elnevezett erőforrás hozzárendelése az összes foglalható erőforrás listájából

Használhatja az **Erőforrásválasztó** keresési mezőjét, hogy minden foglalható erőforrásra kereshessen, és hozzárendelhesse őket feladathoz.

Az így hozzárendelt erőforrások foglalás nélkül lesznek hozzáadva a csapathoz. Ez hasonló ahhoz, amikor csapattagot ad hozzá, és a „Nincs” beosztási módszert választja. Az erőforrás a **Csapat** és az **Egyeztetés** lapon jelenik meg csak hozzárendelésekkel és beosztási hiánnyal rendelkező erőforrásokként. Ha a rendelkezésre állásukat használni kívánja, foglalja le őket.

1. A feladat **Ütemezés** rácsán válassza az **Erőforrás** ikont az erőforrás cellájában.

2. Kezdjen el beírni egy nevet. A név keresési eredményei megjelennek az **Erőforrás választóban** az **Egyéb erőforrások** részen.

3. Válassza ki azt az erőforrást, amelyet hozzá szeretne rendelni a feladathoz.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
