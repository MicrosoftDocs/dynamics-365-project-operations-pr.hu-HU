---
title: Értékesítési becslések és projektek
description: Ez a témakör információkat nyújt arról, hogyan lehet kihasználni az ütemezést és a becsléseket az értékesítési folyamatban.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 76e21f80e51e6f3092880dc629ba90b400805486
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148376"
---
# <a name="sales-estimates-and-projects"></a>Értékesítési becslések és projektek

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Az értékesítési folyamat során értékesítési becsléseket készíthet úgy, hogy egy projektet az értékesítési árajánlathoz kapcsol. Ilyen módon determinisztikus becslés történhet az értékesítési folyamat során, a projekt ütemezésének és becslési lehetőségeinek kihasználása érdekében. Ha az eladás végbe megy, akkor az eladási becslés céljából használt ütemezés szolgálhat a projektterv további finomításának alapjául.

## <a name="linking-a-project-to-a-quote-line"></a>Projekt összekapcsolása árajánlatsorral

Projekt alapú árajánlatsor létrehozásakor létrehozhat egy új projektet, vagy társíthat egy meglévő projektet az **Árajánlatsor** oldalon. 

> ![Árajánlat űrlapja](media/project-8.png)
 
Amikor új projektet hoz létre az árajánlatsor részleteiből, felhasználhatja a projektsablonokat. A projektsablonok olyan modellprojektek, amelyek a szervezetre jellemző szabványos projektterveket és pénzügyi becsléseket jelentenek. Jelenthetik a projekttervek másolatait és a korábbi projektek becsléseit is.

> ![Árajánlatsor részletei](media/project-9.png)
  
Amikor létrehozza a projektet az árajánlatból, a projekt automatikusan társítva lesz az árajánlatsorhoz.

## <a name="components-of-estimates-in-a-project"></a>A becslések összetevői egy projektben

Az ütemezés lehetővé teszi a munka felosztását feladatokra, a feladatok hierarchiájának fenntartását, a feladat elvégzéséhez szükséges erőforrások meghatározását és a feladat elvégzéséhez szükséges erőfeszítés megbecslését.

Az erőfeszítés és az ütemezés becslései a **Projekt** oldal **Ütemezés** fülén található mezők segítségével definiálhatók. Mivel a projekthez árlisták vannak társítva, a pénzügyi becsléseket az árlistában meghatározott költség- és eladási árak alapján számítják ki.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Becslések importálása projektből árajánlatba

A projektbecslések meghatározása után importálhatja azokat az árajánlatsorba. Az **Árajánlatsor részletei** lapon válassza a szalag **Importálás becslésekből** lehetőségét a projektbecslések összefoglalásához tranzakciós típus, szerepkör vagy feladatszint alapján.
