---
title: Projekt másolása
description: Ez a témakör információkat nyújt a projektek másolásáról a Dynamics 365 Project Operations alkalmazásban.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091257"
---
# <a name="copy-a-project"></a>Projekt másolása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations segítségével gyorsan építhet új projekteket a **Projektek** űrlap **Projektek másolása** lehetőségének kiválasztásával. Projekt másolásához nyissa meg a másolni kívánt projektet, majd válassza a **Projekt másolása** lehetőséget. A művelet a következőket másolja:

- Projekt tulajdonságai 
- Munkalebontási struktúra
- Projektcsoporttagok
- Projektbecslések
- Projekt költségbecslései
- Projektanyag-becslések

## <a name="project-properties"></a>Projekt tulajdonságai

A projekt másolásakor a következő mezők értékei kerülnek másolásra:

- Adatfolyam neve
- Adatfolyam leírása
- Ügyfél
- Naptársablon
- Pénznem
- Szerződő részleg
- Projektmenedzser
- Állapot
- Teljes projektállapot
- Hozzászólások
- Becslések
- Becsült kezdő dátum: Ez az a dátum, amikor a projektet létrehozzák a másolatból.
- Becsült befejezési dátum: Az a program az másolatból készített új projekt kezdési dátumából van korrigálva.
- Munkamennyiség (óra)
- Becsült munkaköltség
- Becsült önköltség
- Várható anyagköltség

> [!NOTE]
> A projekt másolása hosszú ideig futó művelet. A rendszer a projektrekordokat, a kapcsolódó attribútumokat és számos kapcsolódó entitást is másol. A művelet hosszú ideig futó jellege miatt a másolás indítása után a cél projekt oldala szerkesztésre zárolva van, amíg be nem fejeződik a másolási művelet.

## <a name="work-breakdown-structure"></a>Munkalebontási struktúra

A projekt másolásakor a teljes erőforrásokkal feltöltött munkalebontási struktúra másolódik. A megnevezett erőforrások helyébe általános erőforrások lépnek. Ha a megnevezett erőforrások nem rendelkeznek az általános erőforrással megegyező munkaidővel, az ütemezés újraszámításra kerül, és a feladatok időtartama változhat.

## <a name="project-team-members"></a>Projektcsoporttagok

Amikor egy projektcsoportot a forrásprojektből másol, az általános erőforrásokat átmásolja a program. Az általános erőforrások hozzárendelései szintén megmaradnak, ahogy a forrásprojektben voltak. A megnevezett erőforrásokat a rendszer általános csapattagokká alakítja.

## <a name="estimates"></a>Becslések

A projekt másolása során a ez erőforrások, költségek és költségbecslési sorok a forrásprojektből vannak másolva. 

A projektek másolásának programozott elérésével kapcsolatos tudnivalók a [Projektsablonok fejlesztése a Projekt másolásával](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
