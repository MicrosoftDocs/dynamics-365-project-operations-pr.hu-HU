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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997199"
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
3. Válassza ki az erőforrás **Munkaidő** lapját, és hajtsa végre a [Munkaidő beállítása erőforráshoz](/dynamics365/field-service/set-work-hours-resource.md) felületen megjelenő utasításokat a naptárszabályok konfigurálásához.

**Új naptársablon létrehozása**

1. Lépjen a **Beállítások** \> **Naptársablon** pontra.
2. Válassza az **Új** lehetőséget, és adjon meg egy nevet, leírást és sablonerőforrást.


> [!NOTE]
> Ha egy erőforrásra hivatkozik egy naptársablonban, az erőforrás naptárának egy példánya a naptársablonhoz társul. Ha módosítja a másolt sablon munkaidejét, akkor ezek a módosítások nem kerülnek át a projekt munkaidejébe.


### <a name="see-also"></a>Kapcsolódó információk  
 [Erőforrások beállítása](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
