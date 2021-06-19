---
title: Ütemezési módok
description: Ez a témakör az ütemezési módokkal kapcsolatban nyújt információkat.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116710"
---
# <a name="scheduling-modes"></a>Ütemezési módok

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_


A(z) Dynamics 365 Project Operations lehetővé teszi a szervezetek számára, hogy meghatározzák, hogyan kezelik a feladatok kulcsfontosságú változóinak változásait a munka lebontási struktúrájában. A szervezet egyedi igényei alapján a projektmenedzserek módosíthatják az ütemezési módot a projekt létrehozásakor.

A Project Operations három ütemezési módból áll rendelkezésre:

  - Rögzített időtartam (ez az alapértelmezett mód)
  - Fix ráfordítás (*Munka*)
  - Rögzített egységek

Az adott ütemezési mód meghatározásával érintett értékeket a következő képlet határozza meg:

  Erőfeszítés = Időtartam x Egység

Amikor beállítja a projekt ütemezési módját, beállítja az alábbi értékek egyikét, amelyet ezután nem lehet módosítani. Ha ezt az értéket állandóként tartjuk, az elsőbbséget élvez ezzel az értékkel, ami értesíti a rendszert, hogy a másik két érték változásakor ne változtassa meg azt. Az alábbi táblázat egy adott mód kiválasztásának hatásairól ad tájékoztatást.

| **Ebben a feladatban**             | **Ha felülvizsgálja az egységeket**   | **Ha felülvizsgálja az időtartamot** | **Ha felülvizsgálja a munkát**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Fix egységek feladata     | Az időtartam újraszámításra kerül. | Az erőfeszítést újraszámolják.    | Az időtartam újraszámításra kerül. |
| Fix ráfordítású feladat    | Az időtartam újraszámításra kerül. | Az egységek újraszámításra kerülnek.    | Az időtartam újraszámításra kerül. |
| Fix időtartamú feladat  | Az erőfeszítést újraszámolják.   | Az erőfeszítést újraszámolják.    | Az egységek újraszámításra kerülnek.   |

Az adott mód következményeiről a [Feladattípus módosítása](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72) című lapon tájékozódhat a pontosabb ütemezésért. A témakörben a **Munka** kifejezést használjuk **Erőfeszítés** helyett.

## <a name="change-the-organizations-scheduling-mode"></a>A szervezet ütemezési módjának módosítása

Hajtsa végre a következő lépéseket a szervezet ütemezési módjának meghatározásához.

1. Válassza a **Beállítások** \> **Általános** \> **Paraméterek** menüpontot, majd válassza ki a projekt paraméterét. 
2. A **Projektparaméterek** lapon jelölje ki a szervezet alapértelmezett ütemezési módját, majd határozza meg, hogy a projektmenedzser felülbírálhatja-e a beállítást új projekt létrehozásakor.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Projekt ütemezési módjának módosítása

Ha egy szervezet lehetővé teszi a projektmenedzser számára, hogy felülbírálja az alapértelmezett ütemezési módot, a Projektmenedzser módosíthatja ezt a módosítást, amikor új projektet hoz létre. A projekt mentése után azonban az ütemezési mód nem módosítható.

## <a name="copied-projects"></a>Átmásolt projektek

Mivel a projekt másolása a projekt másolása közben jön létre, a projektmenedzser nem tudja beállítani az ütemezési módot. A célprojekt mindig a szervezeti szinten meghatározott mód szerint fog alapértelmezett lenni.

## <a name="copied-tasks"></a>Átmásolt feladatok

Ha egy tevékenység átmásolódik egyik projektből a másikba, a tevékenység örökli a célprojekt ütemezési módját.
