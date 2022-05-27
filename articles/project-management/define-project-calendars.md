---
title: Projektnaptárak meghatározása
description: A témakör nyújt tájékoztatást arról, hogyan lehet naptári sablont alkalmazni a projekt ütemezésének nyomon követésére.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0e31fcaf039ae214394b08b60b5d41987dc648e7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578941"
---
# <a name="define-project-calendars"></a>Projektnaptárak meghatározása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Projekt létrehozásához és kezeléséhez naptársablont kell alkalmaznia a projektre. A naptársablon a következő projektjellemzőket határozza meg:

- Munkaidő, beleértve a kezdési és befejezési időt
- Munkanapok
- Naptárkivételek, például munkaszüneti napok

A projektre alkalmazott naptársablon a szervezet beállításaiban meghatározott naptársablon másolata.

> [!NOTE]
> Ha módosítja a naptársablont, ezek a módosítások nem kerülnek át a projekt munkaidejébe. A projekt munkaidejének módosításához új sablont kell alkalmazni.

A szervezet naptársablonának létrehozásához két fő követelmény szükséges:

- Új vagy meglévő foglalható erőforrással határozza meg a sablon kívánt munkaidejét.
- Hozzon létre egy új naptársablont, és társítsa a sablont a foglalható erőforráshoz.

**A sablon munkaidejének meghatározása**

1. Lépjen a **Források** \> **Források** oldalra.
2. Hozzon létre egy új hivatkozást a naptársablonban, vagy jelöljön ki egy meglévő erőforrást.
3. Válassza ki az erőforrás **Munkaidő** lapját, és hajtsa végre a [Munkaidő beállítása erőforráshoz](/dynamics365/field-service/set-work-hours-resource) felületen megjelenő utasításokat a naptárszabályok konfigurálásához.

**Új naptársablon létrehozása**

1. Lépjen a **Beállítások** \> **Naptársablon** pontra.
2. Válassza az **Új** lehetőséget, és adjon meg egy nevet, leírást és sablonerőforrást.

> [!NOTE]
> Ha egy erőforrásra hivatkozik egy naptársablonban, az erőforrás naptárának egy példánya a naptársablonhoz társul. Ha módosítja a másolt sablon munkaidejét, akkor ezek a módosítások nem kerülnek át a projekt munkaidejébe.

Most már hozzárendelheti a munkasablont egy projekt naptársablonhoz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

