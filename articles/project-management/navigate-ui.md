---
title: A felhasználói felületen történő navigálás
description: Ez a témakör információkat nyújt a Dynamics 365 Project Operations Projektmenedzsment funkciójáról.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: de9d0477954da664b71020ef4dfae81a14b999c6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589567"
---
# <a name="navigating-the-user-interface"></a>A felhasználói felületen történő navigálás

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

## <a name="overview"></a>Áttekintés

A fő projekt űrlapja több lapra van elválasztva. Minden lap a projekt különböző részletességi szintjének felel meg.

- **Összegzés**: A projekt leírását tartalmazza, és összesíti mind a tervezett, mind a tényleges projektteljesítményt.

    ![Összegzés lap és mezők.](media/navigation7.png)

- **Feladatok**: Egy rács nézet, egy táblázatos nézet és egy gantt segítségével ábrázolt munkalebontási struktúrára vonatkozó részleteket tartalmazza.

    ![Feladat lap és mezők.](media/navigation8.png)

- **Csoport**: A projekt résztvevőinek részletes ismertetését tartalmazza. Az egyes csoporttagokhoz rendelt erőfeszítés szintén ebben a nézetben kerül összesítésre.

    ![Csoport lap és mezők.](media/navigation9.png)

- **Erőforrás-hozzárendelések**: A projekt egyes erőforrásaira vonatkozó erőfeszítés időfázisos nézetét biztosítja.

    ![Erőforrás-hozzárendelések lap és mezők.](media/navigation10.png)

- **Erőforrás-egyeztetés**: Időfázisos nézetet biztosít az egyes megnevezett erőforrások hozzárendelései és a foglalásuk közötti különbségekről.

    ![Erőforrás-egyeztetés lap és mezők.](media/navigation11.png)

- **Becslések**: A projekt költség- és értékesítési becslésének időfázisos nézetét biztosítja.

    ![Becslések lap és mezők.](media/navigation12.png)

- **Nyomon követés**: olyan nézetet biztosít, amely mutatja a feladatok előrehaladását a munkalebontási struktúrában az erőkifejtés, a költség és az értékesítés szempontjából.

    ![Nyomon követés lap és mezők.](media/navigation13.png)

- **Értékesítés**: Mélyhivatkozásokat tartalmaz a projekthez kapcsolódó ajánlatokhoz és szerződésekhez.

- **Költségbecslések**: Olyan rácsot biztosít, amely a projektek költségeit definiálja a szervezeti költség kategóriái alapján.

    ![Költségbecslések lap és mezők.](media/navigation14.png)

## <a name="grid-controls"></a>Rácsok vezérlői

A következő rész rövid áttekintést nyújt a különböző projekttervezési lapokon található tipikus vezérlőkről.

### <a name="refresh"></a>Frissítés

**Frissítés**: A legfrissebb adatok beolvasása a kiszolgálóról, ha bármilyen változás történt a rács betöltése után.

![Frissítés gomb.](media/navigation7.png)

### <a name="group-by"></a>Csoportosítás szempontja:

**Csoportosítás alapja**: Frissíti a rács sorainak csoportosítását, hogy az az erőforrásokat, a szerepköröket vagy a kategóriákat tükrözze a felhasználó igényei alapján.

![Csoportosítás gomb szerint.](media/navigation6.png)

### <a name="previousnext"></a>Előző/Következő

**Előző**/**Következő**: A látható időszakok frissítése az időfázisos rácsokon.

![Előző és Következő gombok.](media/navigation2.png)

### <a name="timescale"></a>Időskála

**Időskála**: Az időfázisos adatok közötti összesítés váltása napok, hetek, hónapok és évek között.

![Időskála gomb.](media/navigation3.png)

### <a name="expand"></a>Kibontás

**Kibontás**: A látható rácsot teljes képernyőre teszi, így további szerepkörök is megjelenhetnek.

![Kibontás gomb.](media/navigation4.png)

### <a name="time-phase-by"></a>Időfázis alapja:

**Időfázis alapja**: A rácssorok csoportosításának frissítése az értékesítési becslések becsült költségének tükrözéséhez. Ez a vezérlő a becslési parancsfájlra és a nyomonkövetési rácsra is érvényes.

![Időfázis gomb szerint.](media/navigation0.png)

### <a name="add-column"></a>Oszlop hozzáadása

**Oszlop hozzáadása**: Lehetővé teszi, hogy a felhasználó a rácsban látható oszlopokat definiálja. A **Projekttervezés** űrlapján csak gyári oszlopok adhatók hozzá a rácsokhoz.

![Oszlop hozzáadása gomb.](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]