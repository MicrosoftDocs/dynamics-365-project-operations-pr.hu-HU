---
title: A számlázási elmaradás kezelése
description: Ez a témakör a Project Operationsban a számlázási elmaradások megtekintésével és használatával kapcsolatban tartalmaz tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c3752abd26e760d27320d2b86079d84a967d53cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287736"
---
# <a name="manage-the-billing-backlog"></a>A számlázási elmaradás kezelése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations két dedikált nézetet kínál amelyek segítséget nyújtanak a számlázási elmaradás kezelésében. Ezek a **Rögzített árú mérföldkövek**, valamint az **Idő- és anyagszámlázási hátralék**; a nézet kiválasztásához Project Operations **Értékesítés** területén, a bal oldali navigációs oldalon válassza a **Számlázás** lehetőséget. A rendszer ott tárolja a számlázási elmaradás hivatkozásait.

## <a name="fixed-price-milestones"></a>Rögzített árú mérföldkövek

Ez a nézet felsorolja az összes rögzített árú mérföldkövet a rendszerben lévő összes projekt-szerződés sorára vonatkozóan. Egy vagy több mérföldkő is megjelölhető a **Számlázásra kész** vagy **Nem kész a számlázásra** értékre ebből a nézetből. Ha egy mérföldkővet **Számlázásra kész** értékkel jelöl meg, a mérföldkő elérhetővé válik a számlavázlathoz.

Ha a többügyfeles szerződéssorok rögzített árú számlázási móddal rendelkeznek, akkor egy mérföldkő jön létre minden szerződéssorhoz. A felhasználó mérföldkövet hoz létre, és a mérföldkő az ügyfél specifikus mérföldkőrekordokra lesz felosztva, a szerződéssoron az egyes ügyfelekhez meghatározott számlázás felosztása százalékérték alapján. A **Rögzített árú mérföldkövek** nézetben az ügyfélspecifikus mérföldkőrekordok jelennek meg. A mérföldkőrekordok mindegyike **Szálázásra kész** értékkel van megjelölve a nézettől függetlenül. Ha egy vagy több kapcsolódó mérföldkőfelosztás van megjelölve a **Számlázásra kész** értékkel, akkor a fejléc a **Folyamatban** állapotról **Nincs elindítva** állapotra vált. Amikor az összes mérföldkőet kiszámlázták, a mérföldkő fejlécének állapota **Befejezett** lesz.

Ebben a nézetben egy mérföldkő szerepel a vázlat állapotú számlán, és a számlázási állapot **Ügyfélszámla létrehozva**. A számla vázlatának megerősítését követően a bejegyzésben szereplő számlázási állapot frissül a **Számla közzétéve** értékre. Az állapot értékének az egyéni kód használatával történő frissítése nem ajánlott. A Project Operations nem fog megfelelően működni, ha ezeket az állapotértékeket egyéni kóddal frissítik.

## <a name="time-and-material-billing-backlog"></a>Idő- és anyagszámlázási hátralék

Ez a nézet felsorolja azokat a nem számlázott tényleges értékesítéseket, amelyeket nem számláztak le a rendszerben lévő összes projekt-szerződésre vonatkozóan. Egy vagy több nem számlázott tényleges értékesítés is megjelölhető a **Számlázásra kész** vagy **Nem kész a számlázásra** értékre ebből a nézetből. Ha egy nem számlázott tényleges értékesítést **Számlázásra kész** értékkel jelöl meg azzal elérhetővé teszi, hogy elhelyezzék számlavázlaton.

Azok a nem számlázott tényleges értékesítéseket, amelyek **Nem haladhatja meg** állapota **Sikertelen** nem jelölheti meg a **Számlázásra készként**. Ha ezeket a tényadatokat így kell meg jelölni, akkor állítsa vissza az állapotot a szerződéssor más véglegesített tényadatain, majd értékelje ki a **Nem haladhatja meg** állapotot.

Többügyfeles szerződéssorok esetében, amelyekhez idő és anyag számlázási mód tartozik, az idő és költségek jóváhagyása esetén és az egyes ügyfelekre vonatkozóan a szerződés sorában meghatározott számlázási százalékérték szerint minden egyes ügyfélhez létre lesz hozva egy nem számlázott értékesítést. Az **Idő- és anyagszámlázási hátralék** nézetben ezek az egyéni ügyfél-specifikus, nem számlázott tényleges értékesítések láthatók. A számlázatlan tényleges értékesítési rekordok mindegyike **Szálázásra kész** értékkel van megjelölve a nézettől függetlenül.

Ebben a nézetben egy számlázatlan tényleges értékesítés szerepel a vázlat állapotú számlán, és a **Számlázási állapot** **Ügyfélszámla létrehozva**. A számla vázlatának megerősítését követően a bejegyzésben szereplő számlázási állapot frissül a **Ügyfélszámla közzétéve** értékre. Az állapot értékének az egyéni kód használatával történő frissítése nem ajánlott, amikor ebben az állapotban van. A Project Operations nem fog megfelelően működni, ha ezeket az állapotértékeket egyéni kóddal frissítik.


[!INCLUDE[footer-include](../includes/footer-banner.md)]