---
title: A projektajánlat elemzése
description: Ez a témakör a projectajánlatok elemzésével kapcsolatos információkat tartalmaz.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 57ac8407-26f5-49dd-97ea-e97642789ff5
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 63c826d27863df62301ec1548fdc94158220c3a2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752167"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="30e81-103">A projektajánlat elemzése</span><span class="sxs-lookup"><span data-stu-id="30e81-103">Analysis of project quotes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="30e81-104">Dynamics 365 Project Service Automation a projektekajánlatokat a jövedelmezőség becslésére elemzi.</span><span class="sxs-lookup"><span data-stu-id="30e81-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="30e81-105">Azt is elemzi, hogy milyen jól illeszkedik az árajánlat az ügyfelek elvárásaihoz a szállítási dátummal vagy a teljesítési dátummal, valamint a költségvetéssel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="30e81-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="30e81-106">Jövedelmezőségi elemzés</span><span class="sxs-lookup"><span data-stu-id="30e81-106">Profitability analysis</span></span>

<span data-ttu-id="30e81-107">A Project Service Automation a bruttó nyereség és a helyesbített bruttó nyereség használatával elemezi a jövedelmezőséget.</span><span class="sxs-lookup"><span data-stu-id="30e81-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="30e81-108">A bruttó nyereséget a következő képlet segítségével számítja ki a rendszer:</span><span class="sxs-lookup"><span data-stu-id="30e81-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="30e81-109">A helyesbített bruttó nyereséget a következő képlet segítségével számítja ki a rendszer:</span><span class="sxs-lookup"><span data-stu-id="30e81-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="30e81-110">Ha a bruttó nyereség és a helyesbített bruttó nyereség értékei nagy mértékben eltérnek, az árajánlatban szereplő munkák nagy része nem számlázható.</span><span class="sxs-lookup"><span data-stu-id="30e81-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="30e81-111">Az ügyfél elvárásainak elemzése</span><span class="sxs-lookup"><span data-stu-id="30e81-111">Analysis of customer expectations</span></span>

<span data-ttu-id="30e81-112">A következő mezők értékeinek megadásával elemezheti az árajánlatokat, és létrehozhat diagramokat az ügyfelek elvárásaira vonatkozóan az ütemezésről és a költségvetésről:</span><span class="sxs-lookup"><span data-stu-id="30e81-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="30e81-113">Az **Kért szállítási dátum** az árajánlat fejléc mezőjében.</span><span class="sxs-lookup"><span data-stu-id="30e81-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="30e81-114">Az **Ügyfél költségvetése** mező mindegyik ajánlatsorhoz (projektalapú sorokhoz és termékalapú sorokhoz).</span><span class="sxs-lookup"><span data-stu-id="30e81-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="30e81-115">Az ügyfelek ütemezéssel kapcsolatos elvárásainak elemzése az árajánlatsor-részlet legutóbbi záró dátuma és a kért szállítási dátum összehasonlításával történik az árajánlat összes árajánlatsorában.</span><span class="sxs-lookup"><span data-stu-id="30e81-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="30e81-116">A ügyfelek költségvetéssel kapcsolatos elvárásainak elemzése a teljes ügyfélköltségvetés összegének és a megajánlott összegnek az összes ajánlatsoraiban való összehasonlításával történik.</span><span class="sxs-lookup"><span data-stu-id="30e81-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
