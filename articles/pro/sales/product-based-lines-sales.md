---
title: Termékalapú lehetőségsorok
description: Ez a témakör a Project Operations termékalapú lehetőség sorelemeit ismerteti.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896239"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="e3221-103">Termékalapú lehetőségsorok</span><span class="sxs-lookup"><span data-stu-id="e3221-103">Product-based opportunity lines</span></span>

<span data-ttu-id="e3221-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="e3221-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e3221-105">A termékalapuló lehetőségsorok a lehetőségen szereplő sorelemek.</span><span class="sxs-lookup"><span data-stu-id="e3221-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="e3221-106">Ezek a sorok az adott számlán különálló sorelemekként jelennek meg az ügyfél számára, bármilyen más értéknövelt szolgáltatás nélkül.</span><span class="sxs-lookup"><span data-stu-id="e3221-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="e3221-107">A társított költés és felhasználás nem kerül követésre a kapcsolódó projektek feladatain.</span><span class="sxs-lookup"><span data-stu-id="e3221-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="e3221-108">A termékalapú sorok lehetnek katalóguselemek vagy beírandó termékek.</span><span class="sxs-lookup"><span data-stu-id="e3221-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="e3221-109">A lehetőség termékalapú soraiban a legtöbb funkció a Dynamics 365 Sales alkalmazás által biztosított funkciókat követi.</span><span class="sxs-lookup"><span data-stu-id="e3221-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="e3221-110">A termékalapú lehetőség soraira vonatkozó további információkért tekintse meg a következőt: [Termékek hozzáadása egy lehetőséghez](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="e3221-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="e3221-111">A termékalapú lehetőségsorokkal kapcsolatos egyik fogalom, amely a projektalapú lehetőségekre jellemző, az az **Ügyfél költségvetése**.</span><span class="sxs-lookup"><span data-stu-id="e3221-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="e3221-112">Ennek a mezőnek a segítségével nyomon követheti az összeget, amelyet az ügyfél a sorért hajlandó fizetni.</span><span class="sxs-lookup"><span data-stu-id="e3221-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="e3221-113">Ha a lehetőség összesítésének bevételi módja a **Rendszer által számolt**, akkor a program a becsült bevétel kiszámításához összesíti az ügyfélköltségvetés értékeit a termék- és a projektalapú sorok között.</span><span class="sxs-lookup"><span data-stu-id="e3221-113">If the revenue method of the Opportunity summary is set to **System Calculated**, the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
