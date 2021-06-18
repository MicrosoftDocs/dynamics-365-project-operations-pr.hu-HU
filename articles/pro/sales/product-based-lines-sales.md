---
title: Termékalapú lehetőségsorok - Lite
description: Ez a témakör a Project Operations termékalapú lehetőség sorelemeit ismerteti.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7865da682ae607f017bf59ce1ae1addc9fefa60b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994499"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="9b5be-103">Termékalapú lehetőségsorok - Lite</span><span class="sxs-lookup"><span data-stu-id="9b5be-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="9b5be-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="9b5be-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9b5be-105">A termékalapuló lehetőségsorok a lehetőségen szereplő sorelemek.</span><span class="sxs-lookup"><span data-stu-id="9b5be-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="9b5be-106">Ezek a jól elkülöníthető sorelemek az ügyfélnek biztosított számlán vannak.</span><span class="sxs-lookup"><span data-stu-id="9b5be-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="9b5be-107">A számla nem tartalmaz további szolgáltatásokat.</span><span class="sxs-lookup"><span data-stu-id="9b5be-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="9b5be-108">A társított költés és felhasználás nem kerül követésre a kapcsolódó projektek feladatain.</span><span class="sxs-lookup"><span data-stu-id="9b5be-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="9b5be-109">A termékalapú sorok lehetnek katalóguselemek vagy beírandó termékek.</span><span class="sxs-lookup"><span data-stu-id="9b5be-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="9b5be-110">A lehetőség termékalapú soraiban a legtöbb funkció a Dynamics 365 Sales alkalmazás által biztosított funkciókat követi.</span><span class="sxs-lookup"><span data-stu-id="9b5be-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="9b5be-111">A termékalapú lehetőség soraira vonatkozó további információkért tekintse meg a következőt: [Termékek hozzáadása egy lehetőséghez](/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="9b5be-111">For more information about product-based opportunity lines, see [Add products to an opportunity](/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="9b5be-112">Az **Ügyfélköltségvetés** olyan fogalom, amely kifejezetten a projektalapú lehetőségsorokra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="9b5be-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="9b5be-113">Az **Ügyfélköltségvetés** mező nyomon követi azt az összeget, amit az ügyfél fizet a cikkért.</span><span class="sxs-lookup"><span data-stu-id="9b5be-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="9b5be-114">Ha a Lehetőség összegzésének bevételi módja **Rendszer által kiszámítva**, akkor a program a lehetőségsorok ügyfélköltségvetés értékeit összesítő módon kiszámítja a becsült bevételt.</span><span class="sxs-lookup"><span data-stu-id="9b5be-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]