---
title: Projektalapú lehetőségek kezelése
description: Ez a témakör a projektekhez kapcsolódó lehetőségekkel való munkára vonatkozó információkat tartalmaz.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 39ce52d5da4c7027ee2f2fa44579c0d4bf74925e
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087956"
---
# <a name="manage-project-based-opportunities"></a>Projektalapú lehetőségek kezelése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A projektalapú vállalatok általában a több országra és földrajzi helyekre kiterjedő teljesítéssel működnek. A projekt végrehajtásának és a teljesítésnek a költsége attól függően változhat, hogy mely földrajzi terület vagy divízió kezeli a szállítást. Ez viszont hatással lehet az üzlet árrésére. A projektalapú szolgáltatások teljesítése jellemzően nagy mennyiségű humánerőforrás-időt, jelentős utazási költségeket, az anyagi költségeket és egyéb költségeket foglalja magában.

A Dynamics 365 Project Operations programban a projektalapú lehetőségek a Dynamics 365 Sales programhoz tartozó bővítményekkel rendelkeznek. A témakör részletesen ismerteti a különböző mezőket és az üzleti logikát, amely a további funkciókban szerepel, amely a projektalapú vállalatok számára szükséges a projektalapú lehetőségek kezeléséhez.

## <a name="view-all-project-based-opportunities"></a>Összes projektalapú lehetőség megtekintése

A projektalapú lehetőségek listája a **lehetőségek** listaoldalon tekinthető meg. 

1. Válassza az **Értékesítés** > **Lehetőségek** elemet.
2. A **Nézetváltó** használatával kiválaszthatja a lehetőségek más szűrt nézeteit. Egyéni szűrési feltételekkel saját nézeteket hozhat létre a nézetek és a navigációs beállítások konfigurálásához.

A projekt lehetőségeit ebből a listából, illetve a részletek oldalról is létrehozhatja, illetve törölheti.

## <a name="business-process-flow-for-project-based-deals"></a>Üzleti folyamat a projektalapú üzletekhez

A következő üzleti folyamatok támogatottak a Project Operations projektalapú üzletei esetében:

- Érdeklődőből lehetőség üzleti folyamat
- Lehetőség értékesítési folyamata

### <a name="lead-to-opportunity-business-process"></a>Érdeklődőből lehetőség üzleti folyamat 
Az Érdeklődőből lehetőség üzleti folyamat a következő fázisokat támogatja:

| Szakasz | Leképezett entitás | Funkció |
| --- | --- | --- |
| Megfelel | Érdeklődő | Minősítse az érdeklődőt egy partner, kapcsolattartó vagy lehetőség létrehozásához. |
| Fejlesztés | Lehetőség | Fejlessze tovább a lehetőséget, hogy további információkat tudjon megadni az érintett munkára, a legfontosabb résztvevőkre és a versenytársakra vonatkozóan. |
| Ajánlat | Lehetőség | Fejlessze a javaslatot, és szerezzen jóváhagyást a belső ellenőrzési csoporttól. |
| Bezárás | Lehetőség | Nyerje meg a lehetőséget, és zárja le az üzletet. |

### <a name="opportunity-sales-process"></a>Lehetőség értékesítési folyamata
A lehetőség értékesítési folyamata a Project Operations rendszerben a Sales alkalmazás lehetőség értékesítési folyamatának egy bővítményét képezi. Ez az üzleti folyamat beépített módon támogatja a projektalapú lehetőségek követekző fázisait.

| Szakasz | Leképezett entitás | Funkció |
| --- | --- | --- |
| Megfelel | Lehetőség | Minősítse az érdeklődőt egy partner, kapcsolattartó vagy lehetőség létrehozásához. |
| Ajánlat | Ajánlat | Készítsen ajánlatot projektárajánlatokkal, és szerezzen jóváhagyást a belső ellenőrzési csoporttól. |
| Szerződés | Projektszerződés | Nyerje meg az ajánlatot, hogy létrehozza a szerződést, és kezdje meg a végrehajtást és a teljesítést a projekten. |
| Bezárás | Projektszerződés | Végezze el a munkát sikeresen, és zárja be a projektszerződést. |

> [!NOTE]
> Ha a projektalapú üzlet egy érdeklődővel kezdődött, akkor az érdeklődőből lehetőség üzleti folyamatot kell használni.
>
> Ha a projektalapú üzlet egy lehetőséggel kezdődött, akkor a Lehetőség értékesítési folyamatot kell használni.

A termék üzleti folyamata szerkeszthető, vagy saját üzleti folyamatokat hozhat létre az értékesítési folyamat igény szerinti nyomon követéséhez. További információt az üzleti folyamatról itt talál: [Üzleti folyamatok áttekintése](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).
