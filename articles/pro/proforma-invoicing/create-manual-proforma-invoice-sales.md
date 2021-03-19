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
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274191"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="15839-103">Kézi proforma számla létrehozása – Lite</span><span class="sxs-lookup"><span data-stu-id="15839-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="15839-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="15839-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="15839-105">A Dynamics 365 Project Operations-ben a proforma számlák szükség szerint manuálisan is létrehozathatóak.</span><span class="sxs-lookup"><span data-stu-id="15839-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="15839-106">A **Projektszerződések** listából vagy a **Projektszerződés** részletei oldalon manuálisan létrehozhatja a proforma számlát.</span><span class="sxs-lookup"><span data-stu-id="15839-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="15839-107">Projektszerződések listaoldala</span><span class="sxs-lookup"><span data-stu-id="15839-107">Project Contracts list page</span></span>

<span data-ttu-id="15839-108">A **Projektszerződések** listaoldalon jelöljön ki egy vagy több projektszerződést, és hozzon létre számlákat az összes kijelölt bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="15839-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="15839-109">A rendszer ellenőrzi, hogy a kijelölt projekttervek közül melyik rendelkezik **Számlázásra kész** elmaradással a mai dátum előtt.</span><span class="sxs-lookup"><span data-stu-id="15839-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="15839-110">Ezekből a szerződésekből a rendszer létrehozza a vázlat proforma számlákat.</span><span class="sxs-lookup"><span data-stu-id="15839-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="15839-111">Ha egy projektszerződés több ügyfelet tartalmaz, akkor egy-egy számla is létrehozható egy ügyfelenként, és a több számla is projektszerződésenként.</span><span class="sxs-lookup"><span data-stu-id="15839-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="15839-112">Az összes létrehozott projektszámla elérhető a **Számla** oldalon az **Számlázás** szakaszban az **Értékesítés** területen.</span><span class="sxs-lookup"><span data-stu-id="15839-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="15839-113">Projektszerződés részletei oldala</span><span class="sxs-lookup"><span data-stu-id="15839-113">Project Contract details page</span></span>

<span data-ttu-id="15839-114">Proforma számla is létrehozható a **Projektszerződés** részletei oldalon.</span><span class="sxs-lookup"><span data-stu-id="15839-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="15839-115">A rendszer jóváhagyja azt a projektet, amely **Számlázásra kész** elmaradással rendelkezik a mai dátum előtt.</span><span class="sxs-lookup"><span data-stu-id="15839-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="15839-116">Ezekből a szerződésekből a rendszer az egyes szerződéssorok ügyfeleinek számától függően létrehoz egy vázlat proforma számlát.</span><span class="sxs-lookup"><span data-stu-id="15839-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="15839-117">Ha egyetlen proforma számla létre lett hozva, megnyílik a **Számla** lap.</span><span class="sxs-lookup"><span data-stu-id="15839-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="15839-118">Ha az adott projektszerződéshez több számlát is létrehoztak, akkor megnyílik a **Számlák** listaoldal, és megjelenik az összes létrehozott számla.</span><span class="sxs-lookup"><span data-stu-id="15839-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]