---
title: Költség- és értékesítési árak beállítása a katalógustermékekhez – Lite
description: Ez a témakör a költség és értékesítési ráták beállításával kapcsolatban tartalmaz tájékoztatást a termékkatalógus cikkeire vonatkozóan.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176704"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="b50b7-103">Költség- és értékesítési árak beállítása a katalógustermékekhez – Lite</span><span class="sxs-lookup"><span data-stu-id="b50b7-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="b50b7-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="b50b7-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b50b7-105">A termékkatalógusban szereplő termékek árazásának beállítása a Dynamics 365 Project Operationsban ugyanaz, mint a Dynamics 365 Salesben.</span><span class="sxs-lookup"><span data-stu-id="b50b7-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="b50b7-106">Mivel a termékek nem becsülhető meg, illetve nem használhatók fel a Project Operations projektjeinél, nem kell megadnia a termékkatalógus árát az ajánlatokhoz és a szerződésekhez tartozó projektárlisták esetében.</span><span class="sxs-lookup"><span data-stu-id="b50b7-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="b50b7-107">A termékkatalógus árát be kell állítani az ajánlat, a szerződés vagy a partner **termék ára** mezőjében.</span><span class="sxs-lookup"><span data-stu-id="b50b7-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="b50b7-108">Ne állítson be Termékkatalógus-árakat az ilyen entitások projektárlistáiban.</span><span class="sxs-lookup"><span data-stu-id="b50b7-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="b50b7-109">A projektárlisták kizárólag a Project Operationshoz kapcsolódnak.</span><span class="sxs-lookup"><span data-stu-id="b50b7-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="b50b7-110">Van alkalmazásspecifikus üzleti logika, amely az árajánlatokból a szerződésbe másolja az árlisták listáját.</span><span class="sxs-lookup"><span data-stu-id="b50b7-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="b50b7-111">Ennek eredménye a szerződésspecifikus projektárlista.</span><span class="sxs-lookup"><span data-stu-id="b50b7-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="b50b7-112">A másolási művelet késleltetheti az árajánlat megnyerésének folyamatát, ha az árajánlaton szereplő projektárlista túl nagy lesz.</span><span class="sxs-lookup"><span data-stu-id="b50b7-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="b50b7-113">A termékárlisták nem kerülnek másolásra, ha a szerződéseken egyéni árlistát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b50b7-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="b50b7-114">Ez azt jelenti, hogy a termékárlisták nem befolyásolják az árajánlat megnyerési folyamat teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="b50b7-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
