---
title: Általános erőforrás-követelmények teljesítése
description: Ez a témakör a nevesített erőforrásoknak egy általános erőforrás-követelmény részére történő foglalásáról nyújt tájékoztatást.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897589"
---
# <a name="generic-resource-requirement-fulfillment"></a>Általános erőforrás-követelmények teljesítése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Egy elnevezett erőforrás foglalható az erőforrás-követelménnyel rendelkező általános erőforrás lecserélése céljából.

1. A **Projektek** oldalon lépjen a **Csoport** lapra.
2. Válassza ki a listából azt az általános erőforrást, amelyhez erőforrás-követelmény tartozik, majd válassza a **Foglalás** lehetőséget. Egy másik lehetőség, hogy megnyitja az erőforrás-követelményt, majd a **Foglalás** lehetőséget választja.
3. Az **Ütemezési segéd** lapon jelöljön ki egy elnevezett erőforrást a projektcsoport számára történő foglaláshoz, majd válassza a **Foglalás**lehetőséget.

Amikor a foglalás befejeződött, és azt egy elnevezett erőforrás teljesíti, az általános erőforrást az elnevezett erőforrás váltja fel.

Továbbá az ütemezésben szereplő hozzárendelések frissülnek az elnevezett erőforrással.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Általános erőforrás követelményeinek teljesítése több elnevezett erőforrással
Egy általános erőforrás követelménye több elnevezett erőforrással is teljesíthető, hasonlóan, mint egy elnevezett erőforrás hozzárendelése esetén. Például, adott egy feladat, amely öt nap és 120 óra ráfordítást igényel. Ezt a feladatot nem lehet olyan erőforrással befejezni, amely egy ötnapos héten átlagosan napi nyolc órát dolgozik. 

A követelmény 120 órányi robotikai mérnöki tevékenység öt nap alatt, tehát napi 24 óra.

Ez egy példa arra az esetre, amikor egy általános erőforrás-kérelem teljesítéséhez több elnevezett erőforrásra van szükség. A követelmény teljesítéséhez több erőforrást is le kell foglalnia.

A fő különbség ezen forgatókönyv esetén, hogy az általános erőforrás a feladathoz rendelt csoportban marad, és a foglalt elnevezett erőforráscsoport-tagok nem lesznek hozzárendelve a pozíció részeként. A projektvezető a munkát megfelelő módon hozzárendelheti az elnevezett erőforrásokhoz. Az **Egyeztetés** segíthet a projektkezelőnek a foglalás több erőforrás közötti lebontásában a feladat-hozzárendelésekhez. Ez nem történik meg automatikusan, mert a fenti egyszerű példánál bonyolultabb forgatókönyv esetén (ha a követelményt például számos feladat teszi ki) a rendszernek feltételeznie kell a projektkezelő által igényelt hozzárendelési módot. Mivel a rendszer nem érti a szándékot, a feltételezések valószínűleg eltérnek a tervezettől, és helytelen vagy kiszámíthatatlan eredmény fordul elő. A kiszámítható eredmény az, hogy az általános erőforrás mindaddig hozzá lesz rendelve, amíg a projetkezelő szándékosan hozza létre a hozzárendeléseket az **Egyeztetés** nézet segítségével.


