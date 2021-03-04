---
title: Termékalapú szerződéssorok költségszámítása – Lite
description: Ez a témakör a létrehozásról nyújt információkat
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764462"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="80443-103">Termékalapú szerződéssorok költségszámítása – Lite</span><span class="sxs-lookup"><span data-stu-id="80443-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="80443-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="80443-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="80443-105">A Dynamics 365 Project Operations-ben lévő termékalapú szerződéssorok tartalmazzák az **Önköltségi ár** mezőt, amely a termék önköltségi árát tárolja a későbbi jövedelmezőségi számításokhoz.</span><span class="sxs-lookup"><span data-stu-id="80443-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="80443-106">Ha egy katalógustermékhez termékalapú szerződéssort hoz létre, a sor költsége alapértelmezés szerint a termékkatalógus **Standard költség** mezőjéből kerül ki.</span><span class="sxs-lookup"><span data-stu-id="80443-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="80443-107">A termékkatalógus **Általános költség** mezőjének beállítása a szervezet alappénznemében történik.</span><span class="sxs-lookup"><span data-stu-id="80443-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="80443-108">Amikor az egységköltség alapértelmezésben a szerződés sorában szerepel, akkor a rendszer a szerződésben szereplő értékesítési pénznemre váltja át.</span><span class="sxs-lookup"><span data-stu-id="80443-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="80443-109">Termékalapú szerződéssor egységára</span><span class="sxs-lookup"><span data-stu-id="80443-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="80443-110">A termékalapú szerződéssor egységköltségének a célja, hogy lehetővé tegye a különböző termékköltségeket az egyes értékesítési egységekhez.</span><span class="sxs-lookup"><span data-stu-id="80443-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="80443-111">Bár nem minden esetben szükségesek, vannak olyan helyzetek, hogy a termék költségét engedményesen adja a szállító az ügyfélnek.</span><span class="sxs-lookup"><span data-stu-id="80443-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="80443-112">Gondolja át a következő példát:</span><span class="sxs-lookup"><span data-stu-id="80443-112">Consider the following scenario:</span></span>

<span data-ttu-id="80443-113">A Fabrikam Robotics a robotkarok telepítését végzi el az Adatum Corporation gyártósorain.</span><span class="sxs-lookup"><span data-stu-id="80443-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="80443-114">A Fabrikam telepítési szolgáltatásokat nyújt, de a robotkarok a Trey Research vállalattól származnak.</span><span class="sxs-lookup"><span data-stu-id="80443-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="80443-115">Ha a robotkarok telepítése az Adatum Corporation helyszínén új ipari vertikumot nyit a Trey Research robotkarjai számára, akkor a ők speciális engedményt adhatnak ehhez az üzlethez a Fabrikam számára.</span><span class="sxs-lookup"><span data-stu-id="80443-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="80443-116">Ebben az esetben a Fabrikam termékalapú szerződéssort hoz létre a robotkarokhoz.</span><span class="sxs-lookup"><span data-stu-id="80443-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="80443-117">A szerződésben kiszerelési költséget kell megadni.</span><span class="sxs-lookup"><span data-stu-id="80443-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="80443-118">A költség eltér a Trey Research robotkarjainak költségétől.</span><span class="sxs-lookup"><span data-stu-id="80443-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>
