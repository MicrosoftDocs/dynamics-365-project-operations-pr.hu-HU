---
title: Projekt másolása
description: Ez a témakör információkat nyújt a projektek másolásáról a Dynamics 365 Project Operations alkalmazásban.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: cf80f2a1cd27aae33d123e45dee70d94ea4d01a9
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078033"
---
# <a name="copy-a-project"></a>Projekt másolása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations segítségével gyorsan létrehozhat új projekteket a **Projekt másolása** művelet kiválasztásával a **Projektek** űrlapon. Projekt másolásához nyissa meg a másolni kívánt projektet, majd válassza a **Projekt másolása** lehetőséget. A művelet a következőket másolja:

- Projekt tulajdonságai
- A munkalebontási struktúra
- Projektcsoporttagok
- Projektbecslések
- Projekt költségbecslései

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
- Becsült kezdő dátum
- Befejezési dátum
- Munkamennyiség (óra)
- Becsült munkaköltség
- Becsült önköltség

## <a name="work-breakdown-structure"></a>Munkalebontási struktúra

A projekt másolásakor a teljes erőforrásokkal feltöltött munkalebontási struktúra másolódik. A megnevezett erőforrások helyébe általános erőforrások lépnek. Ha a megnevezett erőforrások nem rendelkeznek az általános erőforrással megegyező munkaidővel, az ütemezés újraszámításra kerül, és a feladatok időtartama változhat.

## <a name="project-team-members"></a>Projektcsoporttagok

Amikor egy projektcsoportot a forrásprojektből másol, az általános erőforrásokat átmásolja a program. Az általános erőforrások hozzárendelései szintén megmaradnak, ahogy a forrásprojektben voltak. A megnevezett erőforrásokat a rendszer általános csapattagokká alakítja.

## <a name="estimates"></a>Becslések

A projekt másolásakor az erőforrás- és költségbecslési sorok is átkerülnek a forrásprojektből. 

A projektek másolásának programozott elérésével kapcsolatos tudnivalók a [Projektsablonok fejlesztése a Projekt másolásával](dev-copy-project.md).
