---
title: A számlázási elmaradás kezelése - lite
description: Ez a témakör a számlázási elmaradás kezelése során használható különféle nézetekre vonatkozó információkat tartalmaz.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e3ca167fa53a6923727eff3e7c34c8706dc7455
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176974"
---
# <a name="manage-the-billing-backlog---lite"></a>A számlázási elmaradás kezelése - lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Dynamics 365 Project Operations dedikált nézeteket kínál amelyek segítséget nyújtanak a számlázási elmaradás kezelésében. A számlázási elmaradás kezeléséhez válassza ki a hivatkozásokat az **Értékesítés** területen, a **Számlázás** alatt. 

Az alábbi nézetek állnak rendelkezésre:

- Foglalók és előlegek
- Rendelkezésre álló foglalók és előlegek
- Rögzített árú mérföldkövek
- Termék számlázási hátraléka
- Idő- és anyagszámlázási hátralék

## <a name="retainers-and-advances"></a>Foglalók és előlegek

A **Foglalók és az előlegek** nézet felsorolja az összes foglalót és előleget a rendszerben lévő összes projekt-szerződésben. Egy foglaló vagy előleg számlázása után az előleg összege használható lesz.

## <a name="available-retainers-and-advances"></a>Rendelkezésre álló foglalók és előlegek

A **Rendelkezésre álló foglalók és előlegek** nézet felsorolja az összes rendelkezésre álló foglalót és előleget a rendszerben lévő összes projekt-szerződésben. Egy foglaló vagy előleg számlázása után az előleg összege használható lesz, és hozzá lesz adva a listához. A foglaló vagy az előleg teljes összegének felhasználása után az el lesz távolítva a listából.

## <a name="fixed-price-milestones"></a>Rögzített árú mérföldkövek

A **Rögzített árú mérföldkövek** nézet felsorolja az összes rögzített árú mérföldkövet a rendszerben szereplő összes projekt-szerződéssorra vonatkozóan. Egy vagy több mérföldkő is megjelölhető a **Számlázásra kész** vagy **Nem kész a számlázásra** értékre ebből a nézetből. Ha egy mérföldkövet **Számlázásra kész** értékkel jelöl meg az készen áll arra, hogy számlavázlatra kerüljön.

Ha a többügyfeles szerződéssorok rögzített árú számlázási móddal rendelkeznek, akkor a szerződéssor minden egyes ügyfeléhez létre lesz hozva egy mérföldkő. Mérföldkő is létrehozható, majd felosztható egyedi, ügyfélspecifikus mérföldkő-rekordokra. Ez a felosztás belső, és összhangban van a számlázási százalékos felosztás, amely az egyes ügyfelekhez van definiálva szerződéssoron. A **Rögzített árú mérföldkövek** nézetben az adott ügyfélre specifikus mérföldkő-bejegyzések jelennek meg. A mérföldkőrekordok mindegyike **Szálázásra kész** értékkel van megjelölve a nézettől függetlenül. Ha egy vagy több kapcsolódó mérföldkő felosztás **Számlázásra készként** van megjelölve , akkor a program a fejléc állapotát **Folyamatban** állapotra frissíti a **Nincs elkezdve** értékről. Amikor az összes mérföldkő-felosztás ki van számlázva, a fejléc mérföldkő-állapota **Befejezve** értékre frissül.

Ebben a nézetben egy mérföldkő szerepel a vázlat állapotú számlán, és a számlázási állapot **Ügyfélszámla létrehozva**. A számla vázlatának megerősítésekor a program a bejegyzésben szereplő számlázási állapotot frissíti az **Ügyfélszámla feladva** értékre. Ne frissítse ezt az állapotértékét egyéni kóddal. A Project Operations nem működik megfelelően, ha ezeket az értékeket egyéni kóddal frissítik.

## <a name="product-billing-backlog"></a>Termék számlázási hátraléka

A **Termék számlázási hátraléka** nézet felsorolja az összes termékalapú szerződéssort a rendszer összes projekt-szerződésben. Egy vagy több termékalapú szerződéssor is megjelölhető a **Számlázásra kész** vagy **Nem kész a számlázásra** értékre ebből a nézetből. Ha egy termék alapú szerződéssort **Számlázásra kész** értékkel jelöl meg az készen áll arra, hogy számlavázlatra kerüljön.

Ebben a nézetben egy termékalapú szerződéssor jelenik meg, amely a számlavázlaton található, és a számlázási állapota **Ügyfélszámla létrehozva**. A számla vázlatának megerősítését követően a bejegyzésben szereplő számlázási állapot frissül a **Ügyfélszámla közzétéve** értékre. Ne frissítse ezt az állapotértékét egyéni kóddal. A Project Operations nem működik megfelelően, ha ezeket az értékeket egyéni kóddal frissítik.

## <a name="time-and-material-billing-backlog"></a>Idő- és anyagszámlázási hátralék

Az **Idő- és anyagszámlázási hátralék** nézet felsorolja az összes nem számlázott értékesítési tényadatot, amely a rendszer összes olyan projekt-szerződésében szerepel, amely még nincs számlázva. Egy vagy több nem számlázott tényleges értékesítés is megjelölhető a **Számlázásra kész** vagy **Nem kész a számlázásra** értékre ebből a nézetből. Ha egy nem számlázott tényleges értékesítést **Számlázásra kész** értékkel jelöl meg azzal elérhetővé teszi, hogy elhelyezzék számlavázlaton.

Az olyan nem számlázott értékesítések, amelyeknek **Nem meghaladandó** állapota **Sikertelen**, nem jelölhető meg **Számlázásra készként**. Ha a tényadatokat **Számlázásra kész** értékkel kell megjelölni, akkor állítsa vissza az állapotot a kötött szerződéssorban szereplő egyéb tényeken. Majd értékelje újra a **Nem meghaladandó** állapotot.

Ha a több ügyfélből álló szerződéssorok idő-és anyagelszámolású számlázási móddal rendelkeznek, akkor az időpontok és a kiadások jóváhagyásakor a rendszer egy nem számlázott értékesítési tényadatot hoz létre az egyes ügyfelekhez a szerződéssoron az egyes ügyfelekhez meghatározott számlázási felosztási százalék alapján. Az **Idő- és anyagszámlázási hátralék** nézetben ezek az egyéni ügyfél-specifikus, nem számlázott tényleges értékesítések megjelennek. A számlázatlan tényleges értékesítési rekordok mindegyike **Szálázásra kész** értékkel van megjelölve a nézettől függetlenül.

Ebben a nézetben egy nem számlázott tényleges értékesítés jelenik meg, amely a számlavázlaton található, és a számlázási állapota **Ügyfélszámla létrehozva**. A számla vázlatának megerősítését követően a bejegyzésben szereplő számlázási állapot frissül a **Ügyfélszámla közzétéve** értékre. Ne frissítse ezt az állapotértékét egyéni kóddal. A Project Operations nem működik megfelelően, ha ezeket az értékeket egyéni kóddal frissítik.
