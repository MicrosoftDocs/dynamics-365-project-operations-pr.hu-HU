---
title: Erőforrás-hozzárendelések létrehozása
description: Ez a témakör az általános és a megnevezett erőforrás-hozzárendelések létrehozásával kapcsolatban tartalmaz tájékoztatást.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a6f4f12a962cb570e8b83d8ee7a01fc0cc2c6155
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287106"
---
# <a name="create-resource-assignments"></a>Erőforrás-hozzárendelések létrehozása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_


Az erőforrás-hozzárendelés a projektcsapat valamely tagjának közvetlen társítása egy levélcsomópont-feladathoz. Ez a témakör információkat nyújt az erőforrások hozzárendelésének különböző módjairól.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Általános csapattag létrehozása feladat-hozzárendeléssel


Ha a feladat-hozzárendelésen keresztül egy általános csoporttagot hoz létre, akkor létre kell hoznia egy helyőrzőt vagy egy általános erőforrást. Ez az általános erőforrás leírja annak az elnevezett erőforrásnak a jellemzőit, akit végső soron a feladaton végzett munkával akar megbízni. Ezután előállít egy követelményt (vagy kérést nyújt be a követelmény alapján), amely a megnevezett erőforrás keresésére és lefoglalására használható.

1. A feladat Ütemezés rácsán válassza az Erőforrás ikont az **Erőforrás** cellájában.
2. Gépelje be a helyőrző erőforrásának nevét. Például: Programkezelő.
3. Válassza a **Létrehozás** lehetőséget, majd a **Gyors létrehozás: Projektcsapattag** mezőben adja meg az általános erőforrás szerepkörét.
4. Szükség szerint feladatokat rendelhet hozzá e helyőrző erőforrásához, ha az **Erőforrásválasztóban** kiválasztja az erőforrást a feladathoz. Az erőforrások a **Csapattagok** területen vannak felsorolva.
5. Ha befejezte az általános erőforrás hozzárendelését, válassza ki az általános erőforrást a **Csapat** lapon, majd válassza a **Követelmény generálása** lehetőséget az általános erőforrás erőforrásigényének létrehozásához.
6. Jelölje be a **Foglalás** elemet az általános erőforráshoz, és aztán az ütemezési tábla használatával kereshet és foglalhat le egy tényleges erőforrást. El is küldheti a követelményt egy erőforrás-menedzser általi teljesítésre.
7. Ha az általános erőforrás teljes mértékben be van töltve (a részleges erőforrás-követelmény teljesítése nem eredményez erőforrás-hozzárendelést) egy névvel ellátott erőforrással, akkor a program eltávolítja az általános erőforrást a csoportból. Az általános erőforráshoz tartozó feladat-hozzárendelések ahhoz a megnevezett erőforráshoz vannak hozzárendelve, amely megfelel az általános erőforrás erőforrás-követelményének.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Elnevezett erőforrás hozzárendelése az összes foglalható erőforrás listájából

Használhatja az **Erőforrásválasztó** keresési mezőjét, hogy minden aktív, foglalható erőforrásra kereshessen, és hozzárendelhesse őket bármely levélcsomópont-feladathoz. Az így hozzárendelt erőforrások foglalás nélkül lesznek hozzáadva a csapathoz. Ez hasonló ahhoz, amikor csapattagot ad hozzá, és a **Nincs** beosztási módszert választja. Az erőforrás a **Csapat**, az **Erőforrás-hozzárendelés** és az **Egyeztetés** lapon jelenik meg csak hozzárendelésekkel és beosztási hiánnyal rendelkező erőforrásokként. Ha a rendelkezésre állásukat használni kívánja, foglalja le őket.

1. A feladat rácsa, táblája vagy idővonala alatt keresse meg a **Hozzárendelve a következőhöz:** cellát.
2. A keresőmezőbe kezdje beírni a nevet. A név keresési eredményei megjelennek az **Erőforrás választóban** az **Egyéb erőforrások** részen.
3. Jelölje ki a feladathoz hozzárendelni kívánt erőforrást, vagy jelölje ki az erőforrás nevét a **Csoport egyéb erőforrásai** között.


[!INCLUDE[footer-include](../includes/footer-banner.md)]