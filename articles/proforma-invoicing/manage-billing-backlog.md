---
title: Számlázási elmaradás kezelése
description: Ez a témakör a Project Operationsban a számlázási elmaradások megtekintésével és használatával kapcsolatban tartalmaz tájékoztatást.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e428b551a755220cee67d54b2e63dd7a3c2ca393
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866780"
---
# <a name="manage-billing-backlog"></a>Számlázási elmaradás kezelése

**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

A Dynamics 365 Project Operations dedikált nézeteket kínál amelyek segítséget nyújtanak a számlázási elmaradás kezelésében. A számlázási elmaradás kezeléséhez válassza ki a hivatkozásokat az **Értékesítés** területen, a **Számlázás** alatt. 

Az alábbi nézetek állnak rendelkezésre:

- Foglalók és előlegek
- Rendelkezésre álló foglalók és előlegek
- Rögzített árú mérföldkövek
- Idő- és anyagszámlázási hátralék

## <a name="retainers-and-advances"></a>Foglalók és előlegek

A **Foglalók és előlegek** nézet felsorolja az összes projektszerződésben lévő foglalókat és előlegeket. Egy foglaló vagy előleg számlázása után az előleg összege használható lesz.

## <a name="available-retainers-and-advances"></a>Rendelkezésre álló foglalók és előlegek

Az **Elérhető foglalók és előlegek** nézet felsorolja az összes projektszerződésben lévő elérhető foglalókat és előlegeket. Egy foglaló vagy előleg számlázása után az előleg összege használható lesz, és hozzá lesz adva a listához. Miután a foglaló vagy előleg összegét teljesen felhasználták, eltávolítják a listáról.

## <a name="fixed-price-milestones"></a>Rögzített árú mérföldkövek

A **Rögzített árú mérföldkövek** nézet felsorolja az összes rögzített árú mérföldkövet az összes projektszerződéssorban. Ebből a nézetből az egy vagy több mérföldkő **Számlázásra készként** vagy **Nem számlázhatóként** jelölhető meg. Ha egy mérföldkövet **Számlázásra kész** értékkel jelöl meg az készen áll arra, hogy számlavázlatra kerüljön.

Ha a többügyfeles szerződéssorok rögzített árú számlázási móddal rendelkeznek, akkor a szerződéssor minden egyes ügyfeléhez létre lesz hozva egy mérföldkő. Mérföldkő is létrehozható, majd felosztható egyedi, ügyfélspecifikus mérföldkő-rekordokra. Ez a felosztás belső, és összhangban van a számlázási százalékos felosztás, amely az egyes ügyfelekhez van definiálva szerződéssoron. A **Rögzített árú mérföldkövek** nézetben az adott ügyfélre specifikus mérföldkő-bejegyzések jelennek meg. A mérföldkőrekordok mindegyike **Szálázásra kész** értékkel van megjelölve a nézettől függetlenül. Ha egy vagy több kapcsolódó mérföldkő felosztása **Számlázásra készként** van megjelölve, a fejléc állapota **Nem kezdődött el** értékről **Folyamatban** értékre vált. Ha az összes mérföldkő-felosztást számlázta, a fejléc mérföldkő állapota **Befejezett** értékre frissül.

Ebben a nézetben egy mérföldkő szerepel a vázlat állapotú számlán, és a számlázási állapot **Ügyfélszámla létrehozva**. A számla vázlatának megerősítésekor a program a bejegyzésben szereplő számlázási állapotot frissíti az **Ügyfélszámla feladva** értékre. 

> [!NOTE] 
> Ne frissítse ezt az állapotértéket egyéni kód használatával. A Project Operations nem működik megfelelően, ha ezeket az értékeket egyéni kóddal frissítik.

## <a name="time-and-material-billing-backlog"></a>Idő- és anyagszámlázási hátralék

Az **Idő- és anyagszámlázási hátralék** nézet felsorolja az összes nem számlázott értékesítési tényadatot, amely a rendszer összes olyan projekt-szerződésében szerepel, amely még nincs számlázva. Egy vagy több nem számlázott tényleges értékesítés is megjelölhető a **Számlázásra kész** vagy **Nem kész a számlázásra** értékre ebből a nézetből. Ha egy nem számlázott tényleges értékesítést **Számlázásra kész** értékkel jelöl meg azzal elérhetővé teszi, hogy elhelyezzék számlavázlaton.

Az olyan nem számlázott értékesítések, amelyeknek **Nem meghaladandó** állapota **Sikertelen**, nem jelölhető meg **Számlázásra készként**. Ha a tényadatokat **Számlázásra készként** kell megjelölni, állítsa alaphelyzetbe a lekötött szerződéssor egyéb tényadatainak állapotát, majd értékelje újra **Meg nem haladható** állapotra.

Ha a több ügyfélből álló szerződéssorok idő-és anyagelszámolású számlázási móddal rendelkeznek, akkor az időpontok és a kiadások jóváhagyásakor a rendszer egy nem számlázott értékesítési tényadatot hoz létre az egyes ügyfelekhez a szerződéssoron az egyes ügyfelekhez meghatározott számlázási felosztási százalék alapján. Az **Idő- és anyagszámlázási hátralék** nézetben ezek az egyéni ügyfél-specifikus, nem számlázott tényleges értékesítések megjelennek. A számlázatlan tényleges értékesítési rekordok mindegyike **Szálázásra kész** értékkel van megjelölve a nézettől függetlenül.

Ebben a nézetben a számlatervezeten szereplő nem számlázott értékesítési tényadat jelenik meg az **Ügyfélszámla létrehozva** számlázási állapottal. A számla vázlatának megerősítését követően a bejegyzésben szereplő számlázási állapot frissül a **Ügyfélszámla közzétéve** értékre. 

> [!NOTE] 
> Ne frissítse ezt az állapotértéket egyéni kód használatával. A Project Operations nem működik megfelelően, ha ezeket az értékeket egyéni kóddal frissítik.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
