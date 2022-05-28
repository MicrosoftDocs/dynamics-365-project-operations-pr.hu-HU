---
title: Munkaidősablon létrehozása
description: Ez a témakör ismerteti, hogyan hozható létre munkaidősablon a Project Service szolgáltatásban.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 5788378c7e015c4b11182aaf427aca7d1da48b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598951"
---
# <a name="create-a-work-hours-template-project-service"></a>Munkaidősablon létrehozása (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

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


### <a name="see-also"></a>Kapcsolódó információk  
 [Erőforrások beállítása](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
