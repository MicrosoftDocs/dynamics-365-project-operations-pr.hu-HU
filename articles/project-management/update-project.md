---
title: Projekt létrehozása és frissítése
description: Ez a témakör a projektek Project Operationsben való frissítéséről nyújt tájékoztatást.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d0847b5343cf3e353b91eae04c94509f14213ba5
ms.sourcegitcommit: 51224cb3bf7cdeae6614d39fc8d899c83dbad5f2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/23/2021
ms.locfileid: "7678352"
---
# <a name="create-and-update-a-project"></a>Projekt létrehozása és frissítése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az alábbiakban összefoglaljuk a mezőket, amelyek a létrehozás után frissíthetők a projekten. Ez kiterjed az ezen frissítésekre vonatkozó esetleges következményekre is.

## <a name="project-detail-fields"></a>Projekt részletei mezők

- **Név**: A projekt címe.
- **Leírás**: A projekt áttekintése.
- **Ügyfél**: Az a vállalat, amelynek a projekt szállításra került.
- **Naptársablon**: A projekt munkaideje. A mező módosítása után a program újraszámítja a teljes ütemezést.
- **Pénznem**: A projekt pénzneme. A mező alapértelmezett értéke a szerződésegységben definiált pénznemen alapul. A szerződő részleg frissítésekor a mező frissítése is megtörténik.
- **Szerződő részleg**: Az a szervezeti egység, amely azt a vállalatot vagy részleget reprezentálja, amely elsősorban felelős az értékesítés megnyeréséért és a munka és szolgáltatások ügyfélnek történő leszállításáért.  Ha nincs meghatározva a projektvezető szervzatos egysége, akkor ez a mező alapértelmezés szerint a projektparaméterben megadott értékre van állítva.
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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
