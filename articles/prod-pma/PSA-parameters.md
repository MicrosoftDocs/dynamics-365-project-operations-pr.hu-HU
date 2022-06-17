---
title: A Project Service Automation integrációs paraméterei
description: Ez a cikk azt ismerteti, hogyan konfigurálhatja az alapértelmezett adatok bevitelének módját a 365 Finance szolgáltatással való Microsoft Dynamics 365 for Project Service Automation integráció során Microsoft Dynamics.
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a4abeb2960981196ed1d7c453e7daa0558e326ef
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932299"
---
# <a name="project-service-automation-integration-parameters"></a>A Project Service Automation integrációs paraméterei

[!include[banner](../includes/banner.md)]

A Project Service Automation integrációs paraméterei **lapon konfigurálhatja, hogy a** rendszer hogyan adja meg az alapértelmezett adatokat a Dynamics 365 Finance való integráláskor Dynamics 365 Project Service Automation. Ahhoz, hogy a projektek sikeresen szinkronizálhatók legyenek a Project Service Automation alkalmazásból a Finance rendszerbe, be kell állítania a következő mezőket.

A **Project Service Automation integrációs paraméterei** oldal megnyitásához nyissa meg a **Projektmenedzsment és könyvelés** \> **Beállítások** \> **Dynamics 365 for Project Service Automation integrációs paraméterei** lehetőséget. 

> [!NOTE]
> - A projektfeladatok integrációja, a kiadási tranzakciók kategóriái, az órabecslések, a kiadásbecslések és a funkciók zárolása a 8.0 verzióban érhető el.
> - A tényadatok integrációja a 8.0.1 vagy újabb verziókban érhető el.


| Tabulátor                    | Mező                | Ismertetés |
|------------------------|----------------------|-------------|
| Általános                | Alapértelmezett projekttípus | Válassza ki az alapértelmezett projekttípust. Ha a projektek szinkronizálása a Project Service Automation alkalmazásból történik, akkor ez az érték akkor használható, ha nem ad meg alapértelmezett értéket az integrációs sablonban. A szinkronizálás során az új projektek **Projekttípus** mezőjének értéke erre az értékre van beállítva. Az érték azonban frissíthető, ha a projektszerződéssorok szinkronizálása a Project Service Automation alkalmazásból történik. |
|                        | Időkategória        | Válassza ki az alapértelmezett időkategóriát. Ez az érték akkor használatos, amikor a Project Service Automation alkalmazásban az órákra vonatkozó becslések szinkronizálása megtörténik. Ha a Project Service Automation alkalmazásban szinkronizálja az órabecsléseket és a tényleges óraadatokat, akkor az új projektóra-előrejelzések **Kategória** mezője a Finance alkalmazásban erre az érték kerül beállításra. |
|                        | Díjkategória         | Válassza ki az alapértelmezett díjkategóriát. Ez az érték akkor használatos, amikor a Project Service Automation alkalmazásban a tényleges díjértékek szinkronizálása megtörténik. Ha a Project Service Automation alkalmazásban szinkronizálja a tényleges díjadatokat, akkor az új díjtranzakciók **Kategória** mezője a Finance alkalmazásban erre az érték kerül beállításra. |
| Projektcsoport alapértelmezései | Projekttípus         | Kattintson az **Új** lehetőségre egy új sor hozzáadásához, ahol kiválaszthatja a projekttípust, amelyhez az alapértelmezett projektcsoportot be kívánja állítani. Egy adott projekttípus csak egy alkalommal választható ki a konfigurációban. |
|                        | Projektcsoport        | Válassza ki a kiválasztott projekttípus alapértelmezett projektcsoportját. Amikor új projekteket szinkronizál a Project Service Automation szolgáltatásból, a **Projektcsoport** mező alapértelmezett értéke a projekttípus alapértéke, ha nem ad meg alapértelmezett értéket az integrációs sablonban. |
| A számlázási típus alapértelmezései  | Számlázás típusa         | Kattintson az **Új** lehetőségre egy új sor hozzáadásához, ahol kiválaszthatja a számlázástípust, amelyhez az alapértelmezett sortulajdonságot be kívánja állítani. Egy adott számlázástípus csak egy alkalommal választható ki a konfigurációban. |
|                        | Sortulajdonság        | Válassza ki a kiválasztott számlázástípus alapértelmezett sortulajdonságát. Ha a Project Service Automation alkalmazásból szinkronizálja az új órabecsléseket, az új költségbecsléseket, illetve az új tényleges adatokat, akkor a **Sortulajdonság** mező a számlázási típus alapértelmezett értékére van beállítva. |
| Funkció zárolása  | Nem alkalmazható       | Válassza ki a Project Service Automation alkalmazásból származó projektek és szerződések esetében a Finance rendszerben letiltandó funkciót. Kikapcsolhatja például a szerződések és projektek szerkesztésének, a munkalebontási struktúrák létrehozásának és a munkaidő-nyilvántartások beveitelének képességét a Finance rendszerben. A könyveléssel kapcsolatos mezők továbbra is engedélyezve lesznek, még akkor is, ha a paraméter beállításával elérhetetlenné vannak téve. Alapértelmezés szerint minden funkció engedélyezve van. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]