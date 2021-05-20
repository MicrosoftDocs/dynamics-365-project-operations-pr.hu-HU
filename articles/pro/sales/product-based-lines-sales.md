---
title: Termékalapú lehetőségsorok - Lite
description: Ez a témakör a Project Operations termékalapú lehetőség sorelemeit ismerteti.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f7dfabd068e180c7122ede0f79aaebfe220250a1
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949547"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="94deb-103">Termékalapú lehetőségsorok - Lite</span><span class="sxs-lookup"><span data-stu-id="94deb-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="94deb-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="94deb-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="94deb-105">A termékalapuló lehetőségsorok a lehetőségen szereplő sorelemek.</span><span class="sxs-lookup"><span data-stu-id="94deb-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="94deb-106">Ezek a jól elkülöníthető sorelemek az ügyfélnek biztosított számlán vannak.</span><span class="sxs-lookup"><span data-stu-id="94deb-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="94deb-107">A számla nem tartalmaz további szolgáltatásokat.</span><span class="sxs-lookup"><span data-stu-id="94deb-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="94deb-108">A társított költés és felhasználás nem kerül követésre a kapcsolódó projektek feladatain.</span><span class="sxs-lookup"><span data-stu-id="94deb-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="94deb-109">A termékalapú sorok lehetnek katalóguselemek vagy beírandó termékek.</span><span class="sxs-lookup"><span data-stu-id="94deb-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="94deb-110">A lehetőség termékalapú soraiban a legtöbb funkció a Dynamics 365 Sales alkalmazás által biztosított funkciókat követi.</span><span class="sxs-lookup"><span data-stu-id="94deb-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="94deb-111">A termékalapú lehetőség soraira vonatkozó további információkért tekintse meg a következőt: [Termékek hozzáadása egy lehetőséghez](/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="94deb-111">For more information about product-based opportunity lines, see [Add products to an opportunity](/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="94deb-112">Az **Ügyfélköltségvetés** olyan fogalom, amely kifejezetten a projektalapú lehetőségsorokra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="94deb-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="94deb-113">Az **Ügyfélköltségvetés** mező nyomon követi azt az összeget, amit az ügyfél fizet a cikkért.</span><span class="sxs-lookup"><span data-stu-id="94deb-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="94deb-114">Ha a Lehetőség összegzésének bevételi módja **Rendszer által kiszámítva**, akkor a program a lehetőségsorok ügyfélköltségvetés értékeit összesítő módon kiszámítja a becsült bevételt.</span><span class="sxs-lookup"><span data-stu-id="94deb-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]