---
title: A projektajánlat elemzése
description: Ez a témakör a projectajánlatok elemzésével kapcsolatos információkat tartalmaz.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d1b79a61147bfccf13b0a33179464af91b45121e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291262"
---
# <a name="analysis-of-project-quotes"></a>A projektajánlat elemzése

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation a projektekajánlatokat a jövedelmezőség becslésére elemzi. Azt is elemzi, hogy milyen jól illeszkedik az árajánlat az ügyfelek elvárásaihoz a szállítási dátummal vagy a teljesítési dátummal, valamint a költségvetéssel kapcsolatban.

## <a name="profitability-analysis"></a>Jövedelmezőségi elemzés

A Project Service Automation a bruttó nyereség és a helyesbített bruttó nyereség használatával elemezi a jövedelmezőséget.

- A bruttó nyereséget a következő képlet segítségével számítja ki a rendszer:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- A helyesbített bruttó nyereséget a következő képlet segítségével számítja ki a rendszer:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Ha a bruttó nyereség és a helyesbített bruttó nyereség értékei nagy mértékben eltérnek, az árajánlatban szereplő munkák nagy része nem számlázható.

## <a name="analysis-of-customer-expectations"></a>Az ügyfél elvárásainak elemzése

A következő mezők értékeinek megadásával elemezheti az árajánlatokat, és létrehozhat diagramokat az ügyfelek elvárásaira vonatkozóan az ütemezésről és a költségvetésről:

- Az **Kért szállítási dátum** az árajánlat fejléc mezőjében.
- Az **Ügyfél költségvetése** mező mindegyik ajánlatsorhoz (projektalapú sorokhoz és termékalapú sorokhoz).

Az ügyfelek ütemezéssel kapcsolatos elvárásainak elemzése az árajánlatsor-részlet legutóbbi záró dátuma és a kért szállítási dátum összehasonlításával történik az árajánlat összes árajánlatsorában.

A ügyfelek költségvetéssel kapcsolatos elvárásainak elemzése a teljes ügyfélköltségvetés összegének és a megajánlott összegnek az összes ajánlatsoraiban való összehasonlításával történik.


[!INCLUDE[footer-include](../includes/footer-banner.md)]