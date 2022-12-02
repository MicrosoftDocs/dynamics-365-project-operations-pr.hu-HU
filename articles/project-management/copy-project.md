---
title: Projekt másolása
description: Ez a cikk információkat nyújt a projektek másolásáról a Microsoft Dynamics 365 Project Operations alkalmazásban.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b358f9e45278d886f3e6e8e8cd747fc0ea30212b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925767"
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
- Projektgyűjtők

## <a name="project-properties"></a>Projekt tulajdonságai

A projekt másolásakor a következő mezők értékei kerülnek másolásra.

| Mező | Project Operations – nem készletezett anyagok | Project Operations Lite | Project for the Web |
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
| <p>Becsült kezdő dátum</p><p><strong>Megjegyzés:</strong> Ez a mező azt a dátumot határozza meg, amikor a projektet létrehozzák a másolatból. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Becsült befejezési dátum</p><p><strong>Megjegyzés:</strong> A dátum ebben a mezőben másolatból készített új projekt kezdési dátumából van korrigálva.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Munkamennyiség (óra) | :heavy_check_mark: | :heavy_check_mark: | |
| Becsült munkaköltség | :heavy_check_mark: | :heavy_check_mark: | |
| Becsült önköltség | :heavy_check_mark: | :heavy_check_mark: | |
| Várható anyagköltség | | :heavy_check_mark: | |

> [!NOTE]
> A projekt másolása hosszú ideig futó művelet. A rendszer a projektrekordokat, a kapcsolódó attribútumokat és számos kapcsolódó entitást is másol. A művelet hosszú ideig futó jellege miatt a másolás indítása után a cél projekt oldala szerkesztésre zárolva van, amíg be nem fejeződik a másolási művelet.

## <a name="work-breakdown-structure"></a>Munkalebontási struktúra

A projekt másolásakor a teljes erőforrásokkal feltöltött munkalebontási struktúra másolódik. A megnevezett erőforrások helyébe általános erőforrások lépnek. Ha a megnevezett erőforrások nem rendelkeznek az általános erőforrással megegyező munkaidővel, az ütemezés újraszámításra kerül, és a feladatok időtartama változhat.

## <a name="project-team-members"></a>Projektcsoporttagok

Amikor egy projektcsoportot a forrásprojektből másol, az általános erőforrásokat átmásolja a program. Az általános erőforrások hozzárendelései szintén megmaradnak, ahogy a forrásprojektben voltak. A megnevezett erőforrásokat a rendszer általános csapattagokká alakítja.

> [!NOTE]
> A csoporttagokat és a hozzárendeléseket a rendszer nem másolja a Project for the Web szolgáltatásba.

## <a name="estimates"></a>Becslések

A projekt másolása során a ez erőforrások, költségek és költségbecslési sorok a forrásprojektből vannak másolva. 

A projektek másolásának programozott elérésével kapcsolatos tudnivalók a [Projektsablonok fejlesztése a Projekt másolásával](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Árajánlatok és szerződések

Az ajánlatok és szerződések nem kapcsolódnak a cél projekthez.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
