---
title: Szerepkörök beállítása a munkalebontási struktúra sablonjaihoz
description: Ez a témakör a munkalebontási struktúra sablonok szerepkör-információinak beállításával kapcsolatban tartalmaz tájékoztatást.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 143f1094c653fb7ac0e026b7875aa162a3eb83f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078072"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Szerepkörök beállítása a munkalebontási struktúra sablonjaihoz

[!include [banner](../includes/banner.md)]

A projektmenedzserek munkalebontási struktúra (WBS)-sablonokat állíthatnak be, amelyek akkor alkalmazhatók, amikor új projektekhez hoznak létre WBS-t. A projektmenedzserek szerepköröket vehetnek fel, amikor létrehoznak egy sablont. A következő eljárással lehet szerepkört rendelni egy WBS-sablonhoz.

1. Válassza a **Projektmenedzsment és könyvelés** > **Beállítás** > **Projektek** > **Munkalebontási struktúra sablonok** lehetőséget.
2. Válassza ki a kijelölt WBS-sablon **Részletek** elemét.
3. Jelöljön ki egy feladatot a listából, majd a **Szerepkör** mezőben jelöljön ki egy szerepkört, amelyet hozzá szeretne rendelni a feladathoz.

## <a name="work-with-a-wbs"></a>WBS használata

Létrehozhat új WBS-t, vagy egy meglévő WBS-sablonból is másolhatja a WBS-t. A projektmenedzserek egyszerűen kezelhetik az erőforrásokat, ha szerepköröket rendelnek hozzá az új feladatokhoz a WBS-ben. A szerepköröket ki lehet cserélni az erőforrás megszerzését követően, illetve miután azonosításra került a feladaton dolgozó megerősített erőforrás. Ez a rugalmasság lehetővé teszi a projektmenedzserek számára a következő feladatok végrehajtását:

- A WBS munkacsomagokhoz szükséges erőforrások számának azonosítása.
- Projekt költségeinek becslése.
- Előzetes költségvetés meghatározása.
- Tevékenység időtartamának becslése a szerepkörök és erőforrások alapján.
- A rendelkezésre álló projektadatok alapján néhány projektvezetési terv kidolgozása.

A WBS további opciókkal lett bővítve az erőforrás-biztosítási funkció jobb kihasználásához.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Beállítás</th>
<th>Ismertetés</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Erőforrás-hozzárendelések</td>
<td>A WBS-ben szereplő feladatokhoz tartozó hozzárendelt erőforrások, dátumok, órák száma és foglalástípus megtekintése.</td>
</tr>
<tr class="even">
<td>Csapat automatikus generálása</td>
<td>A tervezett erőforrások automatikus hozzáadása a feladathoz társított szerepkörök használatával. A Pénzügy a szerepkörön alapuló többfeltételű döntési elemzés segítségével automatikusan javasol tervezett erőforrásokat. Miután a szerepkörök és az erőfeszítés (óra) be lett állítva a feladatokhoz a WBS-ben, és a struktúra kiadását követően válassza a <strong>Csapat automatikus generálása</strong> lehetőséget. A tervezett erőforrások szükséges száma hozzáadódik a WBS-hez, valamint a <strong>Projektcsapat és ütemezés</strong> lapon.</td>
</tr>
<tr class="odd">
<td>Erőforrás (legördülő lista)</td>
<td>Az <strong>Erőforrás-hozzárendelés indítása</strong> oldalon a megadott időtartam alapján kijelölheti az erőforrásokat a végleges vagy ideiglenes foglaláshoz. A nézet beállításainak módosításával megtekintheti és beállíthatja az erőforrás-tevékenységek időtartamát. Az erőforrásokat a munkacsomag szintjén adhatja meg és rendelheti hozzá a következő lehetőségek használatával:
<ul>
<li><strong>Elfogadás</strong> – A feladathoz rendelt erőforrás változásainak jóváhagyása.</li>
<li><strong>Visszavonás</strong> – A feladathoz rendelt erőforrás változásainak visszavonása.</li>
<li><strong>Automatikus hozzárendelés</strong> – A kijelölt feladathoz automatikusan kijelöli és hozzárendeli a rendszer a megfelelő szerepkörrel rendelkező, rendelkezésre álló munkatársakkal ellátott erőforrást.</li>
</ul></td>
</tr>
</tbody>
</table>

1. A **Minden projekt** oldalon jelölje ki az **XYZ frissítés 2. fázis** projektet.
2. Válassza a **Terv** > **Tevékenységek** > **Munkalebontási struktúra** lehetőséget.
3. Válassza az **Új** lehetőséget, ha a következő első szintű tevékenységeket szeretné hozzáadni a WBS-hez:

    - Kezdeményezés
    - Tervezés
    - Végrehajtás
    - Figyelés és vezérlés
    - Lezárva

4. Állítsa be a dátumokat és az erőfeszítést (óra), amint az a következő ábrán látható.

    [![Fátumok és erőfeszítés beállítása](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Jelölje ki a **Kezdeményezés** feladatsort, majd a **Szerepkör** mezőben válassza a **Senior projektmenedzser** lehetőséget.
6. Válassza a **Közzététel** lehetőséget.
7. Ugyanabban a sorban, az **Erőforrás** mezőben jelölje ki a **Kovács Dániel** elemet, majd válassza az **Elfogadás** lehetőséget.
8. Válassza ki a **Tervezés** feladatsort, majd a **Szerepkör** mezőben jelölje ki au **Üzleti elemző** elemet.
9. Válassza a **Közzététel** lehetőséget, majd válassza a **Csapat automatikus generálása** lehetőséget.
10. A megjelenő üzenetmezőben válassza az **Igen** lehetőséget.
11. Az **Erőforrás** mezőben ellenőrizze, hogy az érték az **1. üzleti elemző**.
12. Az **1. üzleti elemző** erőforrásnál nyissa meg a keresést, és válassza az **Erőforrás-hozzárendelések indítása** lehetőséget. Ezután válassza ki a feladathoz tartozó dolgozót.
13. Válassza az **Ideiglenes hozzárendelés** &gt; **Teljes kapacitás** lehetőséget.

    > [!NOTE] 
    > Nem kap figyelmeztetést arra vonatkozóan, hogy a megadott erőforrás most 2, mert az erőforrások száma 1 marad.

14. A **Munkalebontási struktúra** oldalon ellenőrizze az erőforrás-hozzárendelést a WBS-ben, majd válassza a **Mentés** lehetőséget.
