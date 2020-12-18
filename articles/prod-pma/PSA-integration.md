---
title: Project Service Automation áttekintése
description: Ez a témakör a Dynamics 365 Project Service Automation és Dynamics 365 Finance közötti integrációs megoldásra vonatkozó információkat tartalmaz.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9ccbb29d5035ea061d232011af87cef2c81e76c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642456"
---
# <a name="project-service-automation-overview"></a>Project Service Automation áttekintése

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

A Project Service Automation és Finance közötti integrációs megoldás az adatintegrációs funkció segítségével szinkronizálja az adatokat a Dynamics 365 Finance és a Dynamics 365 Project Service Automation között a Common Data Service szolgáltatással. Az adatintegrációs szolgáltatással elérhető integrációs sablonok lehetővé teszik a projektek, projektszerződések, projektszerződéssorok, projektszerződéssor mérföldkövei, projektfeladatok, költségtranzakciós kategóriák, órabecslések és költségbecslések áramlását a Project Service Automation és a Finance között.

> [!NOTE]
> - Ha 7.3.0 verziót használ, akkor a KB 4074835 telepítésére van szükség. Ekkor lehetőség van a rögzített árú projektek integrálására.
> - Ha 7.3.0 verziót használ, és a Project Service Automation alkalmazásból hozza át a díjtranzakciókat, akkor a díjaknak a projekt számláján való feltümntetéséhez szükség van a KB 4345320 telepítésére.
> - Ha a 8.0 verziót használja, akkor a projektfeladatok integrációja, a kiadási tranzakciók kategóriái, az órabecslések, a kiadásbecslések és a funkciók zárolása is hasaználható.
> - Ha a 8.0.1 vagy újabb verziót használja, szinkronizálhatja a tényleges értékeket.

Mielőtt integrálhatná a Project Service Automation alkalmazást a Finance rendszerrel, konfigurálnia kell a Project Service Automation integrációs paramétereit. További információk: [Project Service Automation integrációs paraméterei](PSA-parameters.md).

Ez az integrációs megoldás a következő helyzetekben teszi lehetővé a közvetlen szinkronizálást:

- A projektszerződések karbantartása a Project Service Automation alkalmazásban, majd közvetlenül a Project Service Automation és a Finance közötti szinkronizálása.
- Projektek létrehozása a Project Service Automation alkalmazásban, majd közvetlenül a Project Service Automation és a Finance közötti szinkronizálása.
- A projektszerződéssorok karbantartása a Project Service Automation alkalmazásban, majd közvetlenül a Project Service Automation és a Finance közötti szinkronizálása.
- A projektszerződéssorok mérföldköveinek karbantartása a Project Service Automation alkalmazásban, majd közvetlenül a Project Service Automation és a Finance közötti szinkronizálása.
- A projektfeladatok karbantartása a Project Service Automation alkalmazásban, majd közvetlenül a Project Service Automation és a Finance közötti szinkronizálása.
- A költségtranzakciós kategóriák karbantartása a Finance rendszerben, majd közvetlenül a Finance és a Project Service Automation közötti szinkronizálása.
- Projektek órabecsléseinek létrehozása a Project Service Automation alkalmazásban, majd közvetlenül a Project Service Automation és a Finance közötti szinkronizálása.
- Projektek költségbecsléseinek létrehozása a Project Service Automation alkalmazásban, majd közvetlenül a Project Service Automation és a Finance közötti szinkronizálása.
- Projekt tényleges idő-, költség- és díjértékeinek létrehozása a Project Service Automation, és projekttranzakciók létrehozása a Project Service Automation integrációs naplóban, hogy azok feladhatók legyenek a Finance rendszerbe.

## <a name="data-synchronization"></a>Adatszinkronizálás

A következő ábra azt mutatja be, hogyan történik az adatok szinkronizálása az integráció részeként a Project Service Automation és a Finance rendszer között.

> [!NOTE]
> Jelenleg nem minden sablon érhető el. A sablonok megjelennek, amikor elkészültek.

[![Project Service Automation és a Finance közötti integráció](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>A Finance rendszerkövetelményei

A Project Service Automation és a Finance közötti integráció használatához telepítenie kell a Enterprise Edition 7.3 programot a 12-es vagy újabb platformfrissítéssel.

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automation rendszerkövetelményei

A Project Service Automation és a Finance közötti integrációs megoldás használatához a következő összetevőket kell telepíteni:

- Dynamics 365 Project Service Automation 9.0.0.0-es vagy újabb verzió
- Érdeklődőből készpénz megoldás a Dynamics 365 Sales 1.14.0.0 (V14) vagy újabb verziójához
- A Project Service Automation és Finance közötti megoldás a Dynamics 365 Project Service Automation 1.0.0.0 vagy újabb verziójához

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Telepítse a Project Service Automation és Finance integrációs megoldását a Project Service Automation-példányba

Töltse le a Project Service Automation és Finance közötti integrációs megoldást a [Microsoft letöltőközpontból](https://www.microsoft.com/download/details.aspx?id=57016), és kövesse a megoldásban szereplő útmutatást.
