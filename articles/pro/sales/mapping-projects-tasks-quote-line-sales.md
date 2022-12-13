---
title: Projektek és tevékenységek leképezése a projekt árajánlati soraira
description: Ez a cikk arról nyújt tájékoztatást, hogyan lehet projekteket és tevékenységeket leképezni a projekt árajánlati soraira.
author: rumant
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b276e7fb6ec8b98188c9396aca5092d19848afcc
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824277"
---
# <a name="map-projects-and-tasks-to-project-quote-lines"></a>Projektek és tevékenységek leképezése a projekt árajánlati soraira

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A projektajánlat-sorokon leképezheti egy olyan projekt konkrét tevékenységeit, amely már társítva van egy árajánlatsorhoz.

Ha feladatokat képez le egy árajánlatsorba, akkor az árajánlatsorban megadott következő elemek csak az adott feladatokra vonatkoznak:

- Számlázási mód
- Díjazhatósági lehetőségek
- Nem meghaladandó korlátok
- Vevők

Előfordulhat például, hogy a projektben az egyik fázis a rögzített áras, a többi fázis pedig idő- és anyagelszámolásos. Ebben az esetben az első fázist és az összes alárendelt feladatát hozzárendelheti az adott fázishoz tartozó árajánlatsorhoz egy rögzített árú számlázási móddal. Ezután az összes többi fázist hozzárendelheti az idő- és anyagalapú árajánlatsorhoz.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Feladatok hozzárendelése a projektalapú árajánlatsorokhoz

Hozzárendelhet feladatokat az árajánlatsorokhoz alábbi helyekről:

- **Projekt** oldal > **Feladat számlázása** lap (optimális)
- **Árajánlatsor** oldal > **Felszámítható feladatok** lap 

### <a name="from-the-project-page"></a>A Projekt oldalról

A **Projekt** oldal optimális felhasználói élményt nyújt a feladatok árajánlatsorokhoz való társításához. Ezen az oldalon több feladatot is kijelölhet, és az összeset, valamint alárendelt feladatait hozzárendelheti a kijelölt árajánlatsorhoz.

1. A projektalapú árajánlatsor **Általános** lapján ellenőrizze, hogy a **Projekt** mező ki van-e töltve.
2. A **Hozzáadott feladatok** mezőben válassza ki a **Csak a kiválasztott feladatok** lehetőséget.
3. Mentse a projektalapú árajánlatsorokat. Az űrlap frissítésekor a **Felszámítható feladatok** lap jelenik meg.
4. Az **Általános** lapon jelölje ki a projekthez tartozó hivatkozást a **Projekt** mezőben.
5. A **Projekt** oldalon lépjen a **Feladat számlázása** lapra.
6. A második rácson, amely a feladatspecifikus számlázási beállításra vonatkozik, válasszon ki egy vagy több feladatot, majd válassza az **Árajánlatsorok hozzárendelése** lehetőséget.
7. A megjelenő párbeszédpanelen válasszon egy árajánlatsort, amely az árajánlat projektalapú árajánlatsorait jeleníti meg.
8. A **Számlázási típus** mezőben adja meg, hogy ezek a feladatok felszámíthatók vagy nem felszámíthatók-e.
9. Jelölje be a jelölőnégyzetet, ha jelezni szeretné, hogy a hozzárendelésnek tartalmaznia kell a kiválasztott tevékenységek alárendelt feladatait. A mező kiválasztásával hozzárendeli a kiválasztott feladatok alárendelt feladatait az árajánlatsorhoz.
10. Válassza az **OK** elemet a párbeszédpanel bezárásához.

### <a name="from-the-quote-line-page"></a>Az Árajánlatsor oldalról

A projektfeladatokat az árajánlatsorokhoz társíthatja a **Felszámítható feladatok** lapon, az **Árajánlatsor** oldalon.

>[!NOTE]
>A projektfeladatok árajánlatsorokhoz történő hozzárendelésére az optimális hely a **Projekt** oldal **Feladat számlázása** lapja. Ha az **Árajánlatsor** oldal **Felszámítható feladatok** lapjáról rendel hozzá feladatokat, akkor manuálisan kell társítania az egyes projekteket.

1. A projektalapú árajánlatsor **Általános** lapján ellenőrizze, hogy a **Projekt** mezőben ki van-e választva egy projekt.
2. A **Hozzáadott feladatok** mezőben válassza ki a **Csak a kiválasztott feladatok** lehetőséget.
3. Mentse a projektalapú árajánlatsorokat. Az űrlap frissítésekor a **Felszámítható feladatok** lap jelenik meg.
4. A **Felszámítható feladatok** lapon válassza az **Árajánlatsor-feladat hozzáadása** lehetőséget.
5. Az **Árajánlatsor-feladat** oldalon, a **Feladatok** mezőben jelölje ki a feladatot, és a **Számlázás típusa** mezőben válassza a **Mentés** lehetőséget. 
6. Zárja be a lapot. A kijelölt feladat most az árajánlatsorhoz van társítva.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Feladatok projektalapú árajánlatsorokhoz való hozzárendelésének törlése

### <a name="from-the-project-page"></a>A Projekt oldalról

Ez a módszer a legoptimálisabb felhasználói élményt nyújtja a feladatok árajánlatsorokhoz való társításának törléséhez. Ezen az oldalon több feladatot is kijelölhet, és az összes, valamint alárendelt feladatainak hozzárendelését törölheti a kijelölt árajánlatsorról.

1. A projektalapú árajánlatsor **Általános** lapján, a **Projekt** mezőben válassza ki a projekt hivatkozását.
2. A **Projekt** oldalon lépjen a **Feladat számlázása** lapra.
3. A második rácson, amely a feladatspecifikus számlázási beállításra vonatkozik, válasszon ki egy vagy több feladatot, majd válassza az **Árajánlatsorok hozzárendelésének visszavonása** lehetőséget.
4. A megjelenő párbeszédpanelen jelöljön ki egy árajánlatsort.
5. Jelölje be a jelölőnégyzetet, ha jelezni szeretné, hogy a hozzárendelésnek a kiválasztott tevékenységek alárendelt feladatairól is eltávolításra kell kerülnie. A mező kiválasztásával továbbá visszavonhatja a kiválasztott feladatok alárendelt feladatait az árajánlatsorhoz való hozzárendelését.
6. Kattintson az **OK** gombra. Egy figyelmeztető üzenet arról tájékoztatja, hogy ha eltávolítja ezt a társítást, a feladathoz előzőleg rögzített tényleges adatokat a rendszer sztornírozhatja. 
7. Válassza az **OK** lehetőséget a feladat és a projektalapú árajánlatsor közötti társítás eltávolításának folytatásához.

### <a name="from-the-quote-line-page"></a>Az Árajánlatsor oldalról

Visszavonhatja továbbá a projektfeladatok és az árajánlatsorok társítását a **Felszámítható feladatok** lapon, az **Árajánlatsor** oldalon.

1. A **Felszámítható feladatok** lapon válassza az **Árajánlatsor-feladat törlése** lehetőséget.
2. Kattintson az **OK** gombra. Egy figyelmeztető üzenet arról tájékoztatja, hogy ha eltávolítja ezt a társítást, a feladathoz előzőleg rögzített tényleges adatokat a rendszer sztornírozhatja. 
3. Válassza az **OK** lehetőséget a feladat és a projektalapú árajánlatsor közötti társítás eltávolításának folytatásához.

>[!NOTE]
> Ez az eljárás nem törli a feladatot a projektből. Csak eltávolítja a feladat-hozzárendelést a projektalapú árajánlatsorból.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
