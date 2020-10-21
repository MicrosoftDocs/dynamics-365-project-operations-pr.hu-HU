---
title: Projekt frissítése
description: Ez a témakör a projektek Project Operationsben való frissítéséről nyújt tájékoztatást.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897815"
---
# <a name="update-a-project"></a>Projekt frissítése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az alábbiakban található egy összefoglaló a mezőkről, amelyek a létrehozást követően frissíthetők a projekten, és a frissítésre vonatkozó esetleges következmények.

## <a name="project-detail-fields"></a>Projekt részletei mezők

- **Név**: A projekt címe.
- **Leírás**: A projekt áttekintése.
- **Ügyfél**: Az a vállalat, amelynek a projekt szállításra került.
- **Naptársablon**: A projekt munkaideje. A mező módosítása után a program újraszámítja a teljes ütemezést.
- **Pénznem**: A projekt pénzneme. Ez a mező a szerződő részlegben definiált pénznem alapján veszi fel az alapértelmezett értékét. A szerződő részleg frissítésekor a mező frissítése is megtörténik.
- **Szerződő részleg**: Az a szervezeti egység, amely azt a vállalatot vagy részleget reprezentálja, amely elsősorban felelős az értékesítés megnyeréséért és a munka és szolgáltatások ügyfélnek történő leszállításáért. 
- **Projektvezető**: A projektcsapat azon tagja, akinek joga van az időbejegyzések és a kiadások áttekintésére és jóváhagyására.

## <a name="estimate-fields"></a>Becslés mezők

- **Becsült kezdő dátum**: A projekt kezdésének dátuma. A mező frissítésekor a projektben szereplő feladatok az új kezdő dátumnak megfelelően mozdulnak el.
- **Befejezési dátum**: A projekt ütemezett befejezési dátuma.
- **Erőfeszítés**: A projekt becsült erőfeszítése. Amikor feladatokat ad hozzá a projekthez, ez a mező többé nem szerkeszthető.
- **Becsült munkaköltség**: A projekt becsült munkaköltsége. Amikor munkaköltségeket ad hozzá a projekthez, ez a mező többé nem szerkeszthető.
- **Becsült kiadások**: A projekt becsült kiadásai. Amikor kiadásokat ad hozzá a projekthez, ez a mező többé nem szerkeszthető.

## <a name="project-actual-fields"></a>A projekt tényleges mezői
- **Tényleges kezdés**: A projekt elkezdésének dátuma.
- **Tényleges befejezés**: Frissíteni kell a projekt befejezésekor.

## <a name="project-status-fields"></a>Projektállapot-mezők

- **A projekt általános állapota**: A projektmenedzser által megadott általános projektegészségi állapot.
- **Megjegyzés**: A projektmenedzser által megadott aktuális állapotra vonatkozó leírás.

