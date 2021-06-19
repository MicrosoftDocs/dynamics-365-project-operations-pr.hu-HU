---
title: Költség- és értékesítési árak beállítása a katalógustermékekhez – Lite
description: Ez a témakör a költség és értékesítési ráták beállításával kapcsolatban tartalmaz tájékoztatást a termékkatalógus cikkeire vonatkozóan.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004328"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="42947-103">Költség- és értékesítési árak beállítása a katalógustermékekhez – Lite</span><span class="sxs-lookup"><span data-stu-id="42947-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="42947-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="42947-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="42947-105">A termékkatalógus-cikkek árképzésének beállítása ugyanolyan a Dynamics 365 Project Operations-ben, mint a Dynamics 365 Sales rendszerben.</span><span class="sxs-lookup"><span data-stu-id="42947-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="42947-106">A Project Operations programban a termékek nem becsülhetők meg vagy használhatók fel projektekben, így a termékkatalógus árait nem kell beállítani az ajánlatok és szerződések projektárlistáin.</span><span class="sxs-lookup"><span data-stu-id="42947-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="42947-107">A termékkatalógus árak beállításához használja az ajánlat, szerződés vagy számla lehetőség **Termékár** mezőjét.</span><span class="sxs-lookup"><span data-stu-id="42947-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="42947-108">Ne állítson be termékkatalógus-árakat a projektárlistákban.</span><span class="sxs-lookup"><span data-stu-id="42947-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="42947-109">A projektárlisták kizárólag a Project Operationshoz kapcsolódnak.</span><span class="sxs-lookup"><span data-stu-id="42947-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="42947-110">Az alkalmazásspecifikus üzleti logika az árlistákat egy ajánlatból a szerződésbe másolja.</span><span class="sxs-lookup"><span data-stu-id="42947-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="42947-111">Ennek eredménye a szerződésspecifikus projektárlista.</span><span class="sxs-lookup"><span data-stu-id="42947-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="42947-112">A másolási művelet késleltetheti az árajánlat megnyerésének folyamatát, ha az árajánlaton szereplő projektárlista túl nagy lesz.</span><span class="sxs-lookup"><span data-stu-id="42947-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="42947-113">A termékárlisták nem kerülnek másolásra, ha a szerződéseken egyéni árlistát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="42947-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="42947-114">Mivel nincs szükség másolásra, az ajánlati folyamat teljesítményét ez nem befolyásolja.</span><span class="sxs-lookup"><span data-stu-id="42947-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]