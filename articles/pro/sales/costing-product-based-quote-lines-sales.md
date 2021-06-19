---
title: Termékalapú árajánlatsorok költségszámítása
description: Ez a témakör az önköltség termékalapú árajánlatsorokra való alkalmazásával kapcsolatban tartalmaz információkat.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1fa7896e249abfefd3e93cba4bad789e67e14f31
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003454"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="7a45f-103">Termékalapú árajánlatsorok költségszámítása</span><span class="sxs-lookup"><span data-stu-id="7a45f-103">Costing product-based quote lines</span></span>

<span data-ttu-id="7a45f-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="7a45f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7a45f-105">A Dynamics 365 Project Operations termékalapú ajánlatsorai **Önköltségi ár** mezőt is tartalmaznak.</span><span class="sxs-lookup"><span data-stu-id="7a45f-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="7a45f-106">A mező segítségével nyomon követheti a termék önköltségi árát az árajánlatsorban és a későbbi jövedelmezőségi számításokhoz.</span><span class="sxs-lookup"><span data-stu-id="7a45f-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="7a45f-107">Ha egy termékalapú árajánlatsor jön létre egy termékkatalógushoz, akkor a termékalapú árajánlatsor költségét a rendszer alapértelmezés szerint a termékkatalógus **Általános költség** mezőjéből számítja ki.</span><span class="sxs-lookup"><span data-stu-id="7a45f-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="7a45f-108">A termékkatalógus általános költség mezőjének beállítása a szervezet alappénznemében történik.</span><span class="sxs-lookup"><span data-stu-id="7a45f-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="7a45f-109">A termékalapú árajánlatsor alapértelmezett egységköltségét az árajánlatban szereplő értékesítési pénznemre váltja át a rendszer.</span><span class="sxs-lookup"><span data-stu-id="7a45f-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="7a45f-110">Termékalapú árajánlatsor egységára</span><span class="sxs-lookup"><span data-stu-id="7a45f-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="7a45f-111">A termékalapú árajánlatsor egységköltségének a célja, hogy lehetővé tegye a különböző költségeket egy termék egyes értékesítéseinél.</span><span class="sxs-lookup"><span data-stu-id="7a45f-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="7a45f-112">Ez nem tipikus eset, de néha a termék költségét a szállító a végső értékesítés ügyfelétől függően diszkontálhatja.</span><span class="sxs-lookup"><span data-stu-id="7a45f-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="7a45f-113">Például:</span><span class="sxs-lookup"><span data-stu-id="7a45f-113">For example:</span></span>

<span data-ttu-id="7a45f-114">A Fabrikam Robotics a robotkarok telepítését végzi el az A Datum Corporation gyártósorain.</span><span class="sxs-lookup"><span data-stu-id="7a45f-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="7a45f-115">A fabrikam üzembe helyezési szolgáltatásokat biztosít, de a robotkarokat a Trey Roboticstól szerzi be.</span><span class="sxs-lookup"><span data-stu-id="7a45f-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="7a45f-116">Ha a robotkarok telepítése az A Datum Corporation helyszínén új ipari vertikumot nyit a Trey robotkarjai számára, akkor a Trey speciális engedményt adhat ehhez az üzlethez a Fabrikam számára.</span><span class="sxs-lookup"><span data-stu-id="7a45f-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="7a45f-117">Ebben az esetben a Fabrikam létrehoz egy termékalapú árajánlatsort a robotkarok számára, és az árajánlathoz külön egységköltséget ad meg.</span><span class="sxs-lookup"><span data-stu-id="7a45f-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="7a45f-118">Ez a költség eltér a Trey robotkarok általános költségétől.</span><span class="sxs-lookup"><span data-stu-id="7a45f-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]