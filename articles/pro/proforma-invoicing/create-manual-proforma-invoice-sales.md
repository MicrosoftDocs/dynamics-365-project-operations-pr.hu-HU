---
title: Kézi proforma számla létrehozása – Lite
description: Ez a témakör a kézi proforma számlák a Project Operations alkalmazásban való létrehozásáról nyújt tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176389"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="1ab31-103">Kézi proforma számla létrehozása – Lite</span><span class="sxs-lookup"><span data-stu-id="1ab31-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="1ab31-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="1ab31-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1ab31-105">A Dynamics 365 a Project Operations alkalmazásban igény szerint manuálisan is létrehozhatók a proforma számlák.</span><span class="sxs-lookup"><span data-stu-id="1ab31-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="1ab31-106">A **Projektszerződések** listából vagy a **Projektszerződés** részletei oldalon manuálisan létrehozhatja a proforma számlát.</span><span class="sxs-lookup"><span data-stu-id="1ab31-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="1ab31-107">Projektszerződések listaoldala</span><span class="sxs-lookup"><span data-stu-id="1ab31-107">Project Contracts list page</span></span>

<span data-ttu-id="1ab31-108">A **Projektszerződések** listaoldalon jelöljön ki egy vagy több projektszerződést, és hozzon létre számlákat az összes kijelölt bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="1ab31-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="1ab31-109">A rendszer ellenőrzi, hogy a kijelölt projekttervek közül melyik rendelkezik **Számlázásra kész** elmaradással a mai dátum előtt.</span><span class="sxs-lookup"><span data-stu-id="1ab31-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="1ab31-110">Ezekből a szerződésekből a rendszer létrehozza a vázlat proforma számlákat.</span><span class="sxs-lookup"><span data-stu-id="1ab31-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="1ab31-111">Ha egy projektszerződés több ügyfelet tartalmaz, akkor egy-egy számla is létrehozható egy ügyfelenként, és a több számla is projektszerződésenként.</span><span class="sxs-lookup"><span data-stu-id="1ab31-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="1ab31-112">Az összes létrehozott projektszámla elérhető a **Számla** oldalon az **Számlázás** szakaszban az **Értékesítés** területen.</span><span class="sxs-lookup"><span data-stu-id="1ab31-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="1ab31-113">Projektszerződés részletei oldala</span><span class="sxs-lookup"><span data-stu-id="1ab31-113">Project Contract details page</span></span>

<span data-ttu-id="1ab31-114">A proforma számla a **Projektszerződés** részletek oldaláról is létrehozható , amely létrehozza a számlát az adott projekt szerződéshez.</span><span class="sxs-lookup"><span data-stu-id="1ab31-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="1ab31-115">A rendszer ellenőrzi, hogy a projektszerződés rendelkezik-e **Számlázásra kész** elmaradással a mai dátum előtt.</span><span class="sxs-lookup"><span data-stu-id="1ab31-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="1ab31-116">Ezekből a szerződésekből a rendszer az egyes szerződéssorok ügyfeleinek számától függően létrehoz egy vázlat proforma számlát.</span><span class="sxs-lookup"><span data-stu-id="1ab31-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="1ab31-117">Ha egyetlen proforma számla létre lett hozva, megnyílik a **Számla** lap.</span><span class="sxs-lookup"><span data-stu-id="1ab31-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="1ab31-118">Ha a projektszerződéshez több számlát hoz létre, a **Számlák** listaoldala nyílik meg, és megjeleníti az összes létrehozott számlát.</span><span class="sxs-lookup"><span data-stu-id="1ab31-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
