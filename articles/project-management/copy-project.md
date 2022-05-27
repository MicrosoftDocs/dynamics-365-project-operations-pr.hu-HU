---
title: Projekt másolása
description: Ez a témakör információkat nyújt a projektek másolásáról a Dynamics 365 Project Operations alkalmazásban.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574433"
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
- Projekt-ellenőrzőlisták
- Projekt gyűjtők

## <a name="project-properties"></a>Projekt tulajdonságai

A projekt másolásakor a program átmásolja a következő mezők értékeit.

| Mező | Projektműveletek nem raktározott anyagok | Projektműveletek Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Name | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Description | :heavy_check_mark: | :heavy_check_mark: | |
| Ügyfelünk | :heavy_check_mark: | :heavy_check_mark: | |
| Naptársablon | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Pénznem | :heavy_check_mark: | :heavy_check_mark: | |
| Szerződő részleg | :heavy_check_mark: | :heavy_check_mark: | |
| Tulajdonos vállalat | :heavy_check_mark: | | |
| Projektmenedzser | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Állam | :heavy_check_mark: | :heavy_check_mark: | |
| Teljes projektállapot | :heavy_check_mark: | :heavy_check_mark: | |
| Hozzászólások | :heavy_check_mark: | :heavy_check_mark: | |
| Becslések | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Becsült kezdő dátum</p><p><strong>Megjegyzés:</strong> Ez a mező a projekt másolatból történő létrehozásának dátumát adja meg. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Becsült befejezési dátum</p><p><strong>Megjegyzés:</strong> Az ebben a mezőben szereplő dátumot a másolatból készült új projekt kezdési dátuma alapján módosítja a program.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Munkamennyiség (óra) | :heavy_check_mark: | :heavy_check_mark: | |
| Becsült munkaköltség | :heavy_check_mark: | :heavy_check_mark: | |
| Becsült önköltség | :heavy_check_mark: | :heavy_check_mark: | |
| Várható anyagköltség | | :heavy_check_mark: | |

> [!NOTE]
> A projekt másolása hosszú ideig futó művelet. A rendszer a projektrekordokat, a kapcsolódó attribútumokat és számos kapcsolódó entitást is másol. A művelet hosszú ideig futó jellege miatt a másolás indítása után a cél projekt oldala szerkesztésre zárolva van, amíg be nem fejeződik a másolási művelet.

## <a name="work-breakdown-structure"></a>Munkalebontási struktúra

A projekt másolásakor a teljes erőforrásokkal feltöltött munkalebontási struktúra másolódik. A megnevezett erőforrások helyébe általános erőforrások lépnek. Ha a megnevezett erőforrások munkaideje nem azonos az általános erőforráséval, a program újraszámítja az ütemezést, és a tevékenység időtartama megváltozhat.

## <a name="project-team-members"></a>Projektcsoporttagok

Amikor egy projektcsoportot a forrásprojektből másol, az általános erőforrásokat átmásolja a program. Az általános erőforrások hozzárendelései szintén megmaradnak, ahogy a forrásprojektben voltak. A megnevezett erőforrásokat a rendszer általános csapattagokká alakítja.

> [!NOTE]
> A csapattagok és a hozzárendelések nem másolódnak a Webes Projektben.

## <a name="estimates"></a>Becslések

A projekt másolása során a ez erőforrások, költségek és költségbecslési sorok a forrásprojektből vannak másolva. 

A projektek másolásának programozott elérésével kapcsolatos tudnivalók a [Projektsablonok fejlesztése a Projekt másolásával](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Árajánlatok és szerződések

Az ajánlatok és szerződések nem kapcsolódnak a célprojekthez.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
