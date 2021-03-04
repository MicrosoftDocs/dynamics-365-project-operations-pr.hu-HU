---
title: Kézi proforma számla létrehozása – Lite
description: Ez a témakör a kézi proforma számlák a Project Operations alkalmazásban való létrehozásáról nyújt tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764506"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="e5b83-103">Kézi proforma számla létrehozása – Lite</span><span class="sxs-lookup"><span data-stu-id="e5b83-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="e5b83-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="e5b83-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e5b83-105">A Dynamics 365 Project Operations-ben a proforma számlák szükség szerint manuálisan is létrehozathatóak.</span><span class="sxs-lookup"><span data-stu-id="e5b83-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="e5b83-106">A **Projektszerződések** listából vagy a **Projektszerződés** részletei oldalon manuálisan létrehozhatja a proforma számlát.</span><span class="sxs-lookup"><span data-stu-id="e5b83-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="e5b83-107">Projektszerződések listaoldala</span><span class="sxs-lookup"><span data-stu-id="e5b83-107">Project Contracts list page</span></span>

<span data-ttu-id="e5b83-108">A **Projektszerződések** listaoldalon jelöljön ki egy vagy több projektszerződést, és hozzon létre számlákat az összes kijelölt bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="e5b83-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="e5b83-109">A rendszer ellenőrzi, hogy a kijelölt projekttervek közül melyik rendelkezik **Számlázásra kész** elmaradással a mai dátum előtt.</span><span class="sxs-lookup"><span data-stu-id="e5b83-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="e5b83-110">Ezekből a szerződésekből a rendszer létrehozza a vázlat proforma számlákat.</span><span class="sxs-lookup"><span data-stu-id="e5b83-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="e5b83-111">Ha egy projektszerződés több ügyfelet tartalmaz, akkor egy-egy számla is létrehozható egy ügyfelenként, és a több számla is projektszerződésenként.</span><span class="sxs-lookup"><span data-stu-id="e5b83-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="e5b83-112">Az összes létrehozott projektszámla elérhető a **Számla** oldalon az **Számlázás** szakaszban az **Értékesítés** területen.</span><span class="sxs-lookup"><span data-stu-id="e5b83-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="e5b83-113">Projektszerződés részletei oldala</span><span class="sxs-lookup"><span data-stu-id="e5b83-113">Project Contract details page</span></span>

<span data-ttu-id="e5b83-114">Proforma számla is létrehozható a **Projektszerződés** részletei oldalon.</span><span class="sxs-lookup"><span data-stu-id="e5b83-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="e5b83-115">A rendszer jóváhagyja azt a projektet, amely **Számlázásra kész** elmaradással rendelkezik a mai dátum előtt.</span><span class="sxs-lookup"><span data-stu-id="e5b83-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="e5b83-116">Ezekből a szerződésekből a rendszer az egyes szerződéssorok ügyfeleinek számától függően létrehoz egy vázlat proforma számlát.</span><span class="sxs-lookup"><span data-stu-id="e5b83-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="e5b83-117">Ha egyetlen proforma számla létre lett hozva, megnyílik a **Számla** lap.</span><span class="sxs-lookup"><span data-stu-id="e5b83-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="e5b83-118">Ha az adott projektszerződéshez több számlát is létrehoztak, akkor megnyílik a **Számlák** listaoldal, és megjelenik az összes létrehozott számla.</span><span class="sxs-lookup"><span data-stu-id="e5b83-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>
