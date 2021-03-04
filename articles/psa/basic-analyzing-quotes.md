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
ms.openlocfilehash: 361a940261811467c46222c3d58c9504434ec882
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145226"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="85ab9-103">A projektajánlat elemzése</span><span class="sxs-lookup"><span data-stu-id="85ab9-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="85ab9-104">Dynamics 365 Project Service Automation a projektekajánlatokat a jövedelmezőség becslésére elemzi.</span><span class="sxs-lookup"><span data-stu-id="85ab9-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="85ab9-105">Azt is elemzi, hogy milyen jól illeszkedik az árajánlat az ügyfelek elvárásaihoz a szállítási dátummal vagy a teljesítési dátummal, valamint a költségvetéssel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="85ab9-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="85ab9-106">Jövedelmezőségi elemzés</span><span class="sxs-lookup"><span data-stu-id="85ab9-106">Profitability analysis</span></span>

<span data-ttu-id="85ab9-107">A Project Service Automation a bruttó nyereség és a helyesbített bruttó nyereség használatával elemezi a jövedelmezőséget.</span><span class="sxs-lookup"><span data-stu-id="85ab9-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="85ab9-108">A bruttó nyereséget a következő képlet segítségével számítja ki a rendszer:</span><span class="sxs-lookup"><span data-stu-id="85ab9-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="85ab9-109">A helyesbített bruttó nyereséget a következő képlet segítségével számítja ki a rendszer:</span><span class="sxs-lookup"><span data-stu-id="85ab9-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="85ab9-110">Ha a bruttó nyereség és a helyesbített bruttó nyereség értékei nagy mértékben eltérnek, az árajánlatban szereplő munkák nagy része nem számlázható.</span><span class="sxs-lookup"><span data-stu-id="85ab9-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="85ab9-111">Az ügyfél elvárásainak elemzése</span><span class="sxs-lookup"><span data-stu-id="85ab9-111">Analysis of customer expectations</span></span>

<span data-ttu-id="85ab9-112">A következő mezők értékeinek megadásával elemezheti az árajánlatokat, és létrehozhat diagramokat az ügyfelek elvárásaira vonatkozóan az ütemezésről és a költségvetésről:</span><span class="sxs-lookup"><span data-stu-id="85ab9-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="85ab9-113">Az **Kért szállítási dátum** az árajánlat fejléc mezőjében.</span><span class="sxs-lookup"><span data-stu-id="85ab9-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="85ab9-114">Az **Ügyfél költségvetése** mező mindegyik ajánlatsorhoz (projektalapú sorokhoz és termékalapú sorokhoz).</span><span class="sxs-lookup"><span data-stu-id="85ab9-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="85ab9-115">Az ügyfelek ütemezéssel kapcsolatos elvárásainak elemzése az árajánlatsor-részlet legutóbbi záró dátuma és a kért szállítási dátum összehasonlításával történik az árajánlat összes árajánlatsorában.</span><span class="sxs-lookup"><span data-stu-id="85ab9-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="85ab9-116">A ügyfelek költségvetéssel kapcsolatos elvárásainak elemzése a teljes ügyfélköltségvetés összegének és a megajánlott összegnek az összes ajánlatsoraiban való összehasonlításával történik.</span><span class="sxs-lookup"><span data-stu-id="85ab9-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
