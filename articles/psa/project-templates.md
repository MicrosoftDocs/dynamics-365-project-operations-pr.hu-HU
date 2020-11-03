---
title: Projektsablonok
description: Ez a témakör ismerteti, hogyan lehet a projektsablonokat használni a gyors projektbeállításhoz.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 1bb82a312114e9814f5ce65a1698455582fd252e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078254"
---
# <a name="project-templates"></a>Projektsablonok 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A projekt sablon egy előre meghatározott keret, amely segít a projekt gyors és egyszerű elindításában. Használhat egy előre definiált sablont egy új kattintással új projekt létrehozásához. Ami a projektet illeti, meg kell határoznia a projektsablonok előfeltételeit. Minden egyes projektsablonhoz meg kell határoznia egy projektnaptárt, a szerepeket és az árlistákat előre meg kell határozni a szervezetben, hogy a sablon összetevői hasznos adatokkal rendelkezzenek.

A projekt sablonja három összetevőből áll: ütemterv, projektbecslések és a projektcsoport tagjai.

## <a name="schedule"></a>Ütemezés

A ütemterv a projekt sablonjában ugyanazokat az elemeket tartalmazza, mint a projekt ütemezése. Létrehozhat egy feladathierarchiát, társíthat szerepeket a feladatokhoz, meghatározhat ütemezési attribútumokat és beállíthat függőségeket. Az ütemterv egy projektsablonban támogatja az egyes feladatok feladatmódjait is. Ezért támogatja az ütemezési motort. A projekt naptárát társítania kell a projekthez. A munkaterv létrehozásakor nincs különbség a projekt sablonja és a projekt között.

## <a name="project-estimates"></a>Projektbecslések

A projektminta egy projektsablonban ugyanúgy működik, mint a projektben szereplő projektbecslés. A költségeket és az eladási árakat azonban a paraméterekben meghatározott alapértelmezett költség- és eladási árlistákból vonják le.

## <a name="creating-a-project-from-a-template"></a>Projekt létrehozása sablonból
 
A projekt sablonból történő létrehozásához többféle módszer létezik:

- Amikor egy projektet árajánlatból hoz létre, kiválaszthatja a projekt sablonját a **Gyors létrehozás: Projekt** párbeszédpanelen.

> ![Gyors létrehozás: Projekt párbeszédpanel](media/project-11.png)

- Amikor egy projektet az **Új projekt** kiválasztásával hoz létre, a **Projekt** oldal jelenik meg, mielőtt a rekord mentésre kerül. A **Sablon kiválasztása** mezőben válassza ki a szervezet előre meghatározott projektsablonjait.
- Használja a **Projekt létrehozása sablonból** elemet a **Sablon entitás** oldalon.

## <a name="copying-components-of-template-to-project"></a>A sablon összetevőinek másolása a projektbe

A projekt sablonjának összetevőinek a projektbe másolásakor a projekt beállításaitól függően néhány felülbírálás fordulhat elő.

### <a name="copying-the-schedule"></a>Az ütemterv másolása

Az ütemezés másolásakor a projekt sablonból, ha a projektnek eltér a projekt naptára, mint a sablonon, a projekt naptárában szereplő munkaidő alkalmazandó a feladat ütemezésére. Ilyen módon az ütemtervet hozzáigazítják a projekt hátteréhez. Hasonlóképpen, az ütemterv első feladata a projekt kezdő dátumát veszi, és a hierarchia többi részének ütemterve frissül a sablonban megadott időtartam és függőségek alapján. 

### <a name="copying-project-estimates"></a>Projektbecslések másolása 

Ha a projektbecslési sorok között másol, az árlisták frissülnek. A költségjegyzéknél ezek a frissítések a projekt tulajdonos egységén alapulnak. Az eladási árlista alapján a vevőn alapulnak. Az értékesítési egységhez kapcsolódó projektek esetében az egységköltséget és az eladási árat ezen árlisták alapján határozzák meg.

### <a name="copying-a-project-team"></a>Projektcsoport másolása

Amikor egy projektcsoportot átmásolnak egy projekt sablonból egy projektbe, akkor az általános erőforrások másolódnak, a sablonban meghatározott készségekkel és jártasságokkal együtt. Az általános erőforrás-hozzárendeléseket szintén fenntartják, ahogy a projekt sablonjában is voltak. A megnevezett erőforrásokat a projektsablonok nem támogatják.
