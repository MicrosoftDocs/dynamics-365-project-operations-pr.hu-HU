---
title: Bevételi becslések kezelése
description: Ez a cikk információt nyújt a bevételi becslések használatához a projektekhez.
author: sigitac
ms.date: 11/04/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 051535ce8dd4997a923b1511d242638361076979
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928481"
---
# <a name="manage-revenue-estimates"></a>Bevételi becslések kezelése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Bevételi becsléseket hozhat létre, számíthat ki, könyvelhet, sztornírozhat vagy szűntethet meg. Ezt manuálisan vagy egy időszakos folyamattal teheti meg. Ez a cikk információt nyújt a bevételi becslések használatához a projektekhez.

### <a name="manage-revenue-estimates-manually"></a>Bevételi becslések kezelése manuálisan

A rögzített bevételbecslési projektben vagy a **Becslés lekérdezés** oldalon (**Projektvezetés és könyvelés** > **Jelentések és lekérdezések** > **Becslések lekérdezése és jelentések**) válassza a **Becslések** lehetőséget.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Bevételbecslések kezelése időszakos folyamattal

Nyissa meg a **Projektvezetés és -könyvelés** > **Időszakos** > **Becslések** lehetőséget, és válassza ki a kapcsolódó folyamatot.

## <a name="create-a-revenue-estimate"></a>Bevételi becslés létrehozása

Bevételi becslések létrehozásához hajtsa végre az alábbi lépéseket. 

1. Nyissa meg a **Projektvezetés és könyvelés** > **Időszakos** > **Becslések** menüpontot.
2. Válassza az **Új** lehetőséget. A **Becslés létrehozása** lapon adja meg az alábbi paramétereket:

   - **Időszakkód**: Ez a kód határozza meg, hogy milyen gyakran adják fel a becsléseket.
   - **Becslés dátuma**: A becslés feldolgozásának dátuma.
   - **Folyamatos**: Jelölje be ezt a jelölőnégyzetet, ha csak akkor szeretne becsléseket létrehozni, ha becsléseket adtak fel az előző időszakban, vagy ha a becslés az első létrehozott becslés. Ha ez nincs bejelölve, akkor is becslések jönnek létre, még akkor is, ha becsléseket nem adtak fel az előző időszakban.
   - **Teljesítési költség módszere**: Adja meg, hogyan kell megbecsülni a fennmaradó projektmunkát. További információ: [Teljesítési költség módszerei](cost-complete-methods.md).
   - **Teljesítési módszer**: Válasszon ki egy teljesítési módszert a következő lehetőségek közül:
     - **Automatikus** : A készültségi százalék számítása automatikusan, és a számításban szereplő költségsorok alapján történik. A költségsablon határozza meg a benne foglalt költségsorokat.
     - **Manuális**: A készültségi százalék megegyezik az utolsó becslés készültségi százalékával. A becslés létrehozása után módosíthatja a **Manuális számítást** a **Becslések** lapon.
     - **Költségsablonból**: Az automatikus és a manuális módszerek kombinációja. Ez a lehetőség automatikus vagy manuális értékre van beállítva, a költségsablon alapértelmezett értékétől függően.
   - **Előrejelzési modell**: Válasszon előrejelzési modellt a becsléshez.
   - **Becslési listanyomtatása**: Becslési lista létrehozása és megjelenítése. A lista az aktuális függvény állapotát tartalmazza. A becsléssel kapcsolatos figyelmeztetéseket a jelentésben kinyomtathatja. A következő feltételek hatására figyelmeztetések jelennek meg a becslési listában:
     - A készültségi százalék több mint 100 százalék.
     - A készültségi százalék kevesebb mint nulla százalék.
     - Negatív összeg a **Befejezéshez** oszlopban.
     - Kapcsolódó szerződésösszeg nélküli becslés.
     - Csatolt költségbecslés nélküli becslés.
   - **Információs napló megjelenítése**: Akkor válassza ezt a lehetőséget, ha egy olyan üzenetet szeretne kapni, amely a feladat futtatásakor feldolgozott becsült projektekre vonatkozó információkat tartalmazza.


## <a name="post-wip-or-accruals"></a>Folyamatban lévő munka vagy elhatárolások feladása

A becslések értékelése után azok fenntartva, csökkentve vagy növelve lesznek. Ezután feladhatja a folyamatban lévő munkát a **Befejezett szerződés** felmérési elvvel, vagy feladhatja az elhatárolásokat az **Elkészült százalék** elv használatával.
  
A becsült időszak állapota **Létrehozva** állapotról **Feladottra** változik.

## <a name="reverse-wip-or-accruals"></a>Folyamatban lévő munka vagy elhatárolás sztornírozása

A sztornírozás lehetőség használatával jóváírhatja a már feladott folyamatban lévő munkát vagy elhatárolást, majd az időszakra vonatkozóan becsléseket hozhat létre.

> [!NOTE]
> Az egyéb időszakok közötti időszak sztornózásához szotronózza a szükséges becslési időszakokat, majd adja fel ezeket újra. Mivel a későbbi időszakok az előző időszak becsléseitől függnek, nem hagyjon ki semmilyen időszakot.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>A becsülési projekt megszüntetése és a projekt befejezése

A becslési folyamat utolsó lépése a becsült projekt megszüntetése és a fix áras projekt lezárása, amikor a készültségi szint eléri a 100 százalékos értéket.

A következő akkor fordul elő, ha futtatja a megszüntetést:

- Befejezett szerződéssel rendelkező rögzített áras projekt esetén a folyamatban lévő munka értékét a rendszer az egyenlegszámlákból törli, az eredménykimutatást pedig könyveli.
- Befejezett százalékértékű rögzített árú projekt esetén az elhatárolások az eredménykimutatásból törlődnek.

A becslés az állapota **Megszüntetve** értékre változik.

> [!NOTE]
> Különleges esetekben a százalékos arány 100 százaléknál több is lehet. Amikor ez megtörténik, csökkentse a készültségi fokot a **Teljesítési költség módszere beállítása** funkcióval, amíg el nem éri a 100 százalékos értéket.

## <a name="reverse-elimination"></a>Sztornírozás megszüntetése

1. Nyissa meg a **Projektvezetés és könyvelés** > **Időszakos** > **Becslések** > **Eltávolítás sztornírozása** lehetőséget. 
2. A művelet ablaktábla **Folyamat** lapjának **Karbantartás** csoportjában válassza a **Becslés** lehetőséget. 
3. Válassza az **Eltávolítás sztornírozása** lehetőséget.

Ezen az oldalon a megadott becslési dátummal rendelkező összes eltávolítást sztornírozhatja, és megszüntetheti a **Becsült** állapotot. A tranzakció állapota a megfelelő mezők kiválasztása után módosul.

Ezzel automatikusan a projekt állapotát **Folyamatban** állapotra változtatja, ha a projekt fázisa befejezett értékre van állítva. A projekt időszakának becsült állapota a **Feladott** értékre változik vissza.


[!INCLUDE[footer-include](../includes/footer-banner.md)]