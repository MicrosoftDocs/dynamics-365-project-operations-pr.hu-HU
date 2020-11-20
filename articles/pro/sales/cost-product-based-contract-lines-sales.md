---
title: Termékalapú szerződéssorok költségszámítása – Lite
description: Ez a témakör a létrehozásról nyújt információkat
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177244"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="3a7e3-103">Termékalapú szerződéssorok költségszámítása – Lite</span><span class="sxs-lookup"><span data-stu-id="3a7e3-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="3a7e3-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="3a7e3-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="3a7e3-105">Termék alapú szerződéssorok a Dynamics 365 Project Operations alkalmazásban tartalmazzák az **Önköltségi ár** mezőt, amely tárolja a termék önköltségi árát a későbbi jövedelmezőségi számításokhoz.</span><span class="sxs-lookup"><span data-stu-id="3a7e3-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="3a7e3-106">Ha egy termékalapú szerződéssor jön létre egy termékkatalógushoz, akkor a termékalapú szerződéssor költségét a rendszer alapértelmezés szerint a termékkatalógus **Általános költség** mezőjéből számítja ki.</span><span class="sxs-lookup"><span data-stu-id="3a7e3-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="3a7e3-107">A termékkatalógus **Általános költség** mezőjének beállítása a szervezet alappénznemében történik.</span><span class="sxs-lookup"><span data-stu-id="3a7e3-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="3a7e3-108">Amikor az egységköltség alapértelmezésben a szerződés sorában szerepel, akkor a rendszer a szerződésben szereplő értékesítési pénznemre váltja át.</span><span class="sxs-lookup"><span data-stu-id="3a7e3-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="3a7e3-109">Termékalapú szerződéssor egységára</span><span class="sxs-lookup"><span data-stu-id="3a7e3-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="3a7e3-110">A termékalapú szerződéssor egységköltségének a célja, hogy lehetővé tegye a különböző termékköltségeket az egyes értékesítési egységekhez.</span><span class="sxs-lookup"><span data-stu-id="3a7e3-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="3a7e3-111">Bár nem minden esetben szükségesek, vannak olyan helyzetek, hogy a termék költségét engedményesen adja a szállító az ügyfélnek.</span><span class="sxs-lookup"><span data-stu-id="3a7e3-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="3a7e3-112">Gondolja át a következő példát:</span><span class="sxs-lookup"><span data-stu-id="3a7e3-112">Consider the following scenario:</span></span>

<span data-ttu-id="3a7e3-113">A Fabrikam Robotics a robotkarok telepítését végzi el az Adatum Corporation gyártósorain.</span><span class="sxs-lookup"><span data-stu-id="3a7e3-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="3a7e3-114">A fabrikam üzembe helyezési szolgáltatásokat biztosít, de a robotkarokat a Trey Researchtől szerzi be.</span><span class="sxs-lookup"><span data-stu-id="3a7e3-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="3a7e3-115">Ha a robotkarok telepítése az Adatum Corporation helyszínén új ipari vertikumot nyit a Trey Research robotkarjai számára, akkor a ők speciális engedményt adhatnak ehhez az üzlethez a Fabrikam számára.</span><span class="sxs-lookup"><span data-stu-id="3a7e3-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="3a7e3-116">Ebben az esetben a Fabrikam egy termék-alapú szerződéssort hoz létre a Robotic Arms számára, és egy olyan egységenként költséget ad meg ehhez a szerződéshez, amely eltér a Trey Research robotkarjainak szokásos költségétől.</span><span class="sxs-lookup"><span data-stu-id="3a7e3-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
